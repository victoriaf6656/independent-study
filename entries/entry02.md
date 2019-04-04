# Entry Two: Learn the Basics

During this week, I start to learn the basic syntax of EarSketch.<br>

**Digital Audio Workstation (DAW):** A timeline view of your current song, which shows the audio clips you have added to
the song. It lets you hear your song and visualize its structure.<br>

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
#### **Important Key Terms**
+ **Rhythm**
+ **Beat(s)**
+ **Measure**<br>
![Bar Structure](https://victoriaf6656.github.com/independent-study/images/barStructure.png)