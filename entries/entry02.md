# Entry Two: Learn the Basics

During this week, I start to learn the basic syntax of EarSketch.<br>

**Digital Audio Workstation (DAW):** A timeline view of your current song, which shows the audio clips you have added to
the song. It lets you hear your song and visualize its structure.<br>
#### **Important Key Terms**
+ **Rhythm**- The arrangement of sound as music flows through time.
+ **Beat(s)**- A primary unit of time
+ **Measure**- 
+ **Tempo**- The speed at which a piece of music is played, measured in beats per minutes (bpm).
    + Hip Hop: 85-95 bpm
    + Pop: 118 bpm
    + Techno: 120-125 bpm
    + Electro: 128 bpm
    + House: 115-130 bpm
    + Dubstep and Trap: 140 bpm
    + Drum & Bass: 160 - 180 bpm
+ **Pitch**- Determines how high or low the sounds are.
<br>
**The key of a song defines a scale, or group of pitches, in which the song is composed. Keys are either minor or major.**

<br>
### Python

#### **Sections of EarSketch Script**
+ **Comments**- Used to describe the whole project (anywhere)
+ **Setup Section**- This code tells the DAW how to prepare the music
    + ```init()``` initializes/turns on the DAW. 
    + ```setTempo()``` allows you to choose a tempo. 
    + ```from earsketch import *``` adds the EarSketch API to the project.
+ **Music Section**- All of the details of composition go here.
    + ```fitMedia(Y18_DRUM_SAMPLES_2, 1, 1, 5)```
+ **Finish Section**- It tells the DAW that you are done composing and are ready to play your music.
   + ```finish()```
#### **Understanding the Code**
+ Example: ```fitMedia(Y18_DRUM_SAMPLES_2, 1, 1, 5)```
    + After the parentheses, the ```1``` is the track number. Next, is the start measure of the audio clip. Lastly, it
is the end measure.
### **Effects and Envelopes**
Effects change qualities of the sounds in a project. 
+ ```setEffect()``` To create or make new unique sounds. It takes in four arguments.
    + Track Number- The track the effect is addes to.
    + Effect Name- The specific effect being used.
    + Effect Parameter- The setting for the effect.
    + Effect Value- The value of the effect.
<br>
+ **Syntax**- ```setEffect(trackNumber, effectName, effectParameter, effectValue)```
+ ```setEffect(1, DELAY, DELAY_TIME, 500)``` > (Adds a delay (echo) effect, at intervals of 500ms)

Envelopes allow us to add effects to smaller portions of a track and define how an effect's pararmeter
change over time.
<br> <img src= "/images/newenvelope.png"/><br>
+ ```setEffect()``` now takes in 7 arguments:
    + Track Number
    + Effect Name
    + Effect Parameter
    + Effect Start/Value- The starting value of a parameter.
    + Effect Start Location- The measure at which the starting value is set.
    + Effect End Value- The ending value of a parameter. 
    + Effect End Location- The measure at which the ending value is set. 
+ **Volume**- Related to loudness, in which sounds are ordered on a scale from quiet to loud. 
+ **Filter Effect**- Removes certain frequency components of a sound.
```python
#Setup
from earsketch import *
init()
setTempo(120)

#Music
fitMedia(ELECTRO_ANALOGUE_LEAD_012, 1, 1, 9)

# Envelope time points (in measures)
pointA = 1
pointB = 4
pointC = 6.5
pointD = 7
pointE = 8.5
pointF = 9

setEffect(1, FILTER, FILTER_FREQ, 20, pointA, 10000, pointB) # first effect, filter sweep

# second effect, volume changes
setEffect(1, VOLUME, GAIN, -10, pointB, 0, pointC)  # crescendo
setEffect(1, VOLUME, GAIN, 0, pointD, -10, pointE)  # begin fade out
setEffect(1, VOLUME, GAIN, -10, pointE, -60, pointF) # end of fade out

#Finish
finish()
```
+ **Reverb**- Creates delaying ambiance. Controls the decay time and amount of effect presented. 
### Takeaways
1. Learn what you need to know.


[Previous](entry01-plan.md) | [Next](entry03.md) <br>
[Back to Table of Conents](https://github.com/victoriaf6656/independent-study)