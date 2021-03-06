---
layout: post
title: e-drums without a drum module
---

In my [previous post]({{site.baseurl}}/Electronic-drums-on-a-budget) I considered several options for building up an e-drum kit on a modest budget. I ended up questioning whether I actually needed a drum module at all. Is there a way to trigger drum software without one?

## How e-drums work
It helps to understand how drum modules work and the sequence of events between hitting a pad and producing sound.

This simplified schematic shows the main components and signal flow:

![Drum module schematic]({{site.baseurl}}/images/schematic.jpg)

Drum pads contain a piezo sensor that turns vibration into electric current. There may be additional piezo or switch to capture rimshots; these are known as dual-zone pads.

The resulting output is a fed through a stereo jack plug carrying the two analog signals. This is a very simple system but there are key differences between different manufacturers - specifically the wiring of the plugs.

The signal flow is something like this:

### 1. Pad hit
The vibration causes the piezo sensor to generate a variable current which is fed to the drum module trigger input as an analog signal.
### 2. Trigger Processing
Scans the incoming signal to detect the main transient and eliminate false triggers. The output is something like _"trigger input 1 hit; velocity 95"_
### 3. MIDI Processing
Turns each trigger signal into a MIDI message made up of at least a note number and a velocity. There has to be a mapping between trigger inputs and note numbers; for example _Trigger input 1 = note 39_. This MIDI message is passed to the *Sound Engine* and also output via the MIDI Out port.
### 4. Sound engine
Takes each MIDI message and generates the appropriate sound. This may involve playing a digital sample stored in memory or generating a synthetic signal, or a combination of both.

If the drum module has a MIDI In port, sounds can also be played in response to incoming MIDI messages. For example, a drum sequence can be programmed into a DAW and this can trigger the drum modules sounds.
### 5. Audio output
The final step is to convert the sound which is in digital format using a Digital-to-Analog Convertor (DAC) resulting in an analog audio signal.

## Trigger processing
This is the most complex phase as a clean trigger signal needs to be extracted from the incoming signal with minimal latency and no false triggers. Latency is the delay between the input (pad hit) and resulting output (drum sound) and we are surprisingly good at detecting this delay - anything over 10 milliseconds is noticeable.

Not only does this processing have to be performed in parallel for multiple input signals, it also needs to deal with crosstalk between these signals. Since drum pads are typically mounted on a stand there is some mechanical coupling between them. Striking the kick drum may trigger the tom drums, for example. Crosstalk cancellation algorithms are needed to prevent this happening. Trigger sensitivity is also important and varies between different types of trigger pad.

More advanced features can also be found - for example _positional sensing_ can be applied to any pad with a centre-mounted piezo sensor to determine where the pad was hit as well as how hard. This information is converted downstream to MIDI controller messages and used by the sound engine or drum software to trigger the appropriate sound or _articulation_.

![Extract from Roland patent]({{site.baseurl}}/images/roland-patent.jpg)

*Note - Roland patented many triggering techniques including their implementation of positional sensing in the late 1990s early 2000s. These patents have now expired.*

## Triggering external sounds

Why would you want to do this given drum modules have a built-in sound engine?

The main reason is to trigger sounds from drum software running on a computer. For example, [Superior Drummer 3 (SD3)](https://www.toontrack.com/product/superior-drummer-3/) is very highly regarded and comes with a huge array of samples spanning many different instruments and genres. Rather than "one shot" samples, multiple samples are captured at different hit strength (velocity) resulting in a much more realistic sound.

SD3 also has samples for many different articulations. For example, each snare can respond to positional sensing provided in MIDI controller messages, resulting in an extremely realistic tone just like a real acoustic snare.

![Image of Superior Drummer 3]({{site.baseurl}}/images/sd3.png)

Drum modules can turn off Local Control - this stops MIDI data going to the internal sound engine, but it continues to be sent to MIDI Out. In effect the drum module is operating as a trigger interface generating MIDI data, bypassing the onboard sounds completely.

Dedicated drum trigger interfaces provide the same capability but there are very few manufacturers serving what is after all a niche within a niche. However, a recent entrant into this market is the [eDRUMin](https://www.audiofront.net/eDRUMin.php):

![Image of eDRUMin 10 device]({{site.baseurl}}/images/ED10.jpg)

## Keep on eDRUMin

This device grabbed my attention as it ticked a number of boxes:
- Support for lots of pad/cymbal types from different manufacturers
- Two expression pedal inputs giving lots of options for hi-hat setup
- Plenty inputs on the eDRUMin 10 (a 4 input model is also available)
- Positional sensing support when using pads with a centre-mounted piezo
- Companion app for editing trigger settings; much better than the small displays on drum modules

The eDRUMin also has some unique features that make it even more attractive. Three-zone cymbal pads (bow/bell/edge) normally use two inputs. eDRUMin can reduce this to one input in combination with its _Bell Sense_ feature.

Single-zone pads can be turned into dual-zone pads using _Rim Sense_. Somehow, the signal processing contained in the eDRUMin is able to detect a rim hit even though single zone pads have no rim sensor.

Since this device is aimed at e-drummers triggering drum software, it includes mappings for the most common software and also addresses a known issue with hi-hat triggering in SD3.

Lastly, it struck me as good value considering it does exactly what I need and doesn't include any superfluous features. I purchased one in late 2020 from the US website and it was shipped to the UK from Taiwan in just 8 days with no import duties.

In my next article I will go through how I built up my e-drums using other secondhand parts, and got it all working with the eDRUMin 10 and Superior Drummer 3.
