# Entry Three: Advanced to the Intermediate!
This week, I continued the tutorial of EarSketch. In the tutorial of EarSketch, there are 24 (twenty-four)
tutorials in total. I don't think I would be able to finish it by the end of this week. However, I already
started on my song, though it's repeated.

+ **Musical Composition**-  refer to an original piece or work of music, either vocal or instrumental, the 
structure of a musical piece, or to the process of creating or writing a new piece of music. (According 
to Wikipedia)

#### Musical Form
In this chapter, I learned that a piece of music consists of a form or structure, like a poem.
+ **Sections**- Several measures that expresses an idea or feeling.
    + Chrouses, Verses, Intros, and Outros
+ **Form**- Overall structure or a layout of a song or a piece of music. <br>

One common form is the 'A-B-A' form. 
+ Section A measures 1-4.
+ SEction B measures 5-8; adds variety to section A and features contrasting sounds to Section A.
+ Section A (repeated) measures 9-12.

#### Custom Functions
+ Used to write your own functions and avoid repetitive code. <br>
    + Define and call a function: ```def myFunction()```
    + It has two parameters, which takes in two arguments: ```startMeasure``` and ```endMeasure``` <br>
    
Example of code below: <br>
```python
def myFunction(strtMeasure, endMeasure):
        fitMedia(ELECTRO_DRUM_MAIN_BEAT_003, 1, startMeasure, endMeasure)
        fitMedia(ELECTRO_ANALOGUE_PHASERBASS_003, 2, startMeasure, endMeasure)
    #calling our function, passing it two arguments:1 and 17
    myFunction(1,17)

finish()
```

#### Making Custom Beats
+ ```makeBeat()```- Compose musical note by note. This is called step sequencing on music production.
Takes in four arguments:
    + Clip Name- The clip a beat is constructed from.
    + Track Number- The track on which music is placed.
    + Measure Number (Only requires a starting measure; string length determines the end measure) 
    + Beat string- A string that specifies the rhytthm created
<br>
 
Example: <br>
```python
from earsketch import *
init()
setTempo(120)

synth = DUBSTEP_FILTERCHORD_002
cymbal = OS_CLOSEDHAT01
beat1 = "-00-00+++00--0-0"
beat2 = "0--0--000--00-0-"

makeBeat(synth, 1, 1, beat1)
makeBeat(cymbal, 2, 1, beat2)

finish()
```

#### Key Term
+ **Abstraction**- The bundling of ideas to form a single concept. An example of an abstraction is a function.
+ **String**- A data type of a series with characters with single or double quotation marks

### Takeaways
1. Key terms are important to understand the code you are learning on.
2. For EarSketch: Select audio clips that goes well together by listening to the tempo and the beat(s) 
of the measure.
3. *"Time is Money" -By Benjamin Franklin*
    - Like what Mr. Mueller said before, it doesn't take 3 weeks to complete the tutorial. Though I agree
with both Mr. Mueller and the phrase above, I need more time to learn from the tutorial. So...
### Next Steps
1. I plan to continue working on my song. When I think of something and need help, I would go back to the
tutorial to learn from it. That way, it won't take much time.
<br>

[Previous](entry02.md) | [Next](entry04.md) <br>
[Back to Table of Contents](https://github.com/victoriaf6656/independent-study)
