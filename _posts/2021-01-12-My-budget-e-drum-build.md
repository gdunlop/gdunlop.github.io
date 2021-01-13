---
layout: post
title: My e-drum build with eDRUMin
---

The [previous post]({{site.baseurl}}/E-drums-without-a-drum-module) explained how drum modules work and questioned if you need a dedicated drum module just to trigger sounds in Superior Drummer 3 (SD3) or other drum software. I decided to go with an 'e-drum to MIDI' device and purchased an [eDRUMin from Audiofront](https://www.audiofront.net/eDRUMin.php).

This article goes through the build of my e-drum kit using components from Jobeky, Roland and Yamaha. A full cost breakdown is provided at the end for anyone interested in going down this route as an alternative to complete e-drum kits with a module.

Future posts will give more details on eDRUMin set-up and tweaking SD3 to get the best results.

## Shopping list
After getting hold of an eDRUMin I began the search for pads and cymbals to build up a full kit:-
- Kick drum
- Pads for toms (at least two; I play "one up, one down")
- Pad for use as snare drum with support for positional sensing
- Hi-hats, cymbal pads for crashes (at least two) and ride

Since the eDRUMin supports various types of trigger I was able to look for parts from different manufacturers.

## Kick start
My first purchase was a partial [Jobeky shell pack](https://jobekydrums.co.uk/product-category/e-drums/jobeky-shell-packs/), for sale locally on Gumtree. It ticked a lot of boxes being close to a full-size acoustic kit including:-
- 20x16 mesh head kick drum
- 12x8 mesh head rack tom
- 14x12 mesh head floor tom

New, this kit would have included an additional 10-inch rack tom and 14-inch snare, but I figured I could buy these individually from Jobeky at a later date if I wanted to. Since the [Jobeky dual-zone side mounted triggers](https://jobekydrums.co.uk/product/jobeky-internal-dual-zone-side-trigger/) are available separately, I could even convert acoustic drums.

This photo shows the kick drum's internal cable routing and black fittings, both cost options when purchased new.

![Cable routed through Jobeky kick drum]({{site.baseurl}}/images/cables.png)

## Snare drum
I wanted a snare pad suitable for use on a traditional snare stand rather than a tom mount like you find on many electronic pads. My only other requirement was a centre-mounted trigger to enable positional sensing.

First choice was a lovely contrasting [Jobeky steel snare in black chrome](https://jobekydrums.co.uk/product/prestige-black-chrome-electronic-snare-drum/) but the cost and long lead time of 8-10 weeks was too much (everything is custom made to order). Instead, I found a Roland PD-128-S mesh pad for sale on Marketplace in the same black chrome finish. This pad is designed to be used as a snare and the seller threw in a couple of dual-zone cymbal pads to sweeten the deal.

Here is the pad mounted on my snare stand. You can also see the kick drum with centre-mounted trigger and my kick pedal with a Gibraltar ball beater.

![Roland PD-128S mesh pad]({{site.baseurl}}/images/snare.jpg)

## Cymbals
I assumed electronic cymbal pads would only be available in rubber. This is true for the mainstream manufacturers (Roland, Yamaha, Alesis, ATV) but there are a number of alternatives available.

Since I was looking at Jobeky products I came across their range of metal cymbals and considered buying a set of ["Real Feel" low volume cymbals](https://jobekydrums.co.uk/product-category/e-cymbals/jobeky-black-stealth/). Various budget rubber cymbals are available from online shops such as [Thomann](https://www.thomann.de/gb/electronic_drum_cymbal_pads.html) but I was not 100% confident they would work.

With plenty of options on eBay and I ended up with a pair of used Yamaha cymbals - a 13 inch PCY-130 and matching 15 inch PCY-150. Both are three-zone pads with bell/bow/edge triggers and choke function. The seller threw in a worn Yamaha hi-hat pad as well - more on that in the next section.

This photo shows all the pads in place and connected:

![Image of my e-drum kit]({{site.baseurl}}/images/edrums.jpg)

The PCY-150 is used as a ride cymbal on a boom arm attached to the tom mount on the kick drum. The PCY-130 serves as the main crash cymbal on a standard cymbal stand. The other two dual-zone pads which I got for free serve as a second crash and china, or whatever instrument I assign. Although I don't have the correct mounts they work fine.

## Hi-hats
Acoustic hi-hats can make a huge variety of sounds - from tight closed to fully open, played with stick tip or shank on the top or edge of the hi-hat, or played with the foot pedal including heal splashes.

I have play-tested several kits in the past including Roland's top model and the hi-hats have always been the weak point, so I didn't have high expectations about what I could achieve on a more modest budget.

There are several ways to try and replicate an acoustic hi-hat using a combination of pad and foot controller:-
1. Dedicated foot controller combined with a single cymbal pad
2. Cymbal pad mounted on a hi-hat stand combined with a separate hi-hat controller unit
3. As (2) but using a pair of pads like acoustic hi-hats

I chose option 2 since I had a (free) dual-zone Yamaha RHH-135 and I wanted to use my existing hi-hat stand. Although the rubber surface has a split it plays fine:

![Yamaha hihat pad]({{site.baseurl}}/images/hihat.jpg)

The hi-hat controller is an integrated part of the pad, unlike many other models that use a separate hi-hat controller unit. It also uses a _multi-step switch_ so rather than sending out a range of values (0-127) it outputs five distinct _steps_ with fixed values.

This seemed like a major limitation but results with eDRUMin and SD3 have been great - I will cover this in a future post.

## Hi-hat controller options
There are many options for hi-hat controllers so it's worth a short diversion on this topic.

Roland and others use a hi-hat controller unit that sits on top of the hi-hat stand beneath the hi-hat pad. Pressing the pedal down pushes a sprung part in the hi-hat controller attached to a Force Sensing Resistor (FSR). Here is a photo of a Roland VH-10 hi-hat controller:

![Roland VH-10 hi-hat controller unit]({{site.baseurl}}/images/roland-controller.jpg)

As this [disassembly of a Roland VH-10 controller](https://open-e-drums.tumblr.com/post/186810874399/disassemble-roland-vh-10) shows, this is a very simple mechanism and you wonder how they get away with charging so much!

Hi-hat controller options include:
- FSR controller under hi-hat pad (Roland VH-10)
- Optical controller incorporated in bottom hi-hat (ATV)
- Optical controller under foot pedal [Drone Trigger](https://www.youtube.com/watch?v=8I19X6tuN2M)
- FSR(?) controller under foot pedal [Magnatrack Remedy HC-2](https://www.magnatrack.com/shop/electronic-cymbals/remedy-hi-hat-controller-two/)
- Build your own using FSR or Hall Effect sensor [DIY options](https://www.vdrums.com/forum/advanced/diy/61236-easy-to-make-diy-hihat-controller)

## Completed kit
This shows my initial set-up with the kit facing into the room:

![Jobeky e-drum kit]({{site.baseurl}}/images/jobeky.jpg)

To make better use of space I shifted it around to face out the window:

![Jobeky e-drum kit]({{site.baseurl}}/images/window.jpg)

Finally, here is the eDRUMin mounted to a cymbal stand with the included bracket.:

![eDRUMin mounted on cymbal stand]({{site.baseurl}}/images/edrumin.jpg)

Hi-hat controller and USB cable connect to ports on the bottom. The device is powered over USB from my laptop but you can use a 9V power supply in situations where no computer is involved. Pads connect to the numbered inputs on the top. There is just enough room for the ten TCS sockets - this device really could not be any smaller!

## Cost breakdown
My reference point in terms of budget was intermediate kits such as Roland's TD-17KVX (RRP £1,599) and ATV EXS-5 (RRP £1,649) and [several other options]({{site.baseurl}}/Electronic-drums-on-a-budget). I was confident I could achieve a better result for considerably less than this.

- [Audiofront eDRUMin 10](https://www.audiofront.net/eDRUMin.php), £265 _(new)_
- Jobeky kick, rack tom & floor tom, £250 _(used)_
- Roland PD-128S-BC, £160 _(used)_
- 14 inch dual-zone cymbal unbranded, £0 _(used)_
- 12 inch dual-zone cymbal unbranded, £0 _(used)_
- Yamaha PCY-150 triple zone cymbal, £55 _(used)_
- Yamaha PCY-135 triple zone cymbal, £35 _(used)_
- Yamaha RHH-135 hi-hat, £0 _(used)_
- [Superior Drummer 3 - download](https://www.andertons.co.uk/toontrack-superior-drummer-3-%28download%29), £315 _(new)_
- [Gibraltar ball beater](https://www.amazon.co.uk/Gibraltar-Black-Beater-Cajon-drums/dp/B00T8L1RPY), £12 _(new)_
- [TRS stereo cables](https://www.ebay.co.uk/usr/electro_drum_shop), £38 _(new)_

Grand total £1,130 excluding the laptop that is needed to run SD3 _(Dec 2020)_.

I could have reduced the cost by choosing an alternative to Superior Drummer 3 - after all it has some features I may never use. However, the range and quality of the samples and the dedicated support for e-drums sold it. I was also blown away by the [meticulous process](https://www.youtube.com/watch?v=OY4Hrtble0Y) used to capture these samples.

Older intermediate Roland kits such as the TD-15KV sell on eBay for around the same price, generally with smaller pads all round and drum modules using technology that is over 10 years old, so I'm really happy with the outcome.

Having spent a total of £90 on cymbals and hi-hats these will probably be upgraded in the future, but in the meantime I am getting in to a regular practice routine. My son is also making good use of the kit for online drum lessons during lockdown.

In future articles I will cover triggering setup using the eDRUMin companion app, and playing with e-drum settings in SD3 to get the best results.

## Further reading
- [The Digital Drummer's Swiss Army Knife](http://mikedolbear.com/seriously-wired/swiss-army-knife/)
- [How to Build a DIY Electronic Drum Kit](https://medium.com/sebdrums/how-to-build-a-diy-electronic-drum-kit-f47aac24e016) - includes acoustic to electric (a2e) conversion
