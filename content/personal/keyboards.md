---
title: Keyboards
---

I type on a split, ergonomic, 34-key keyboard.

<p>
<img id="pcb" style="vertical-align: middle" src="/images/keyboards/final.jpg"/>
</p>

This is the result of a rabbit hole I went down in 2021 or so. In retrospect it was quite a valuable hobby to pick up; I learned how to solder microelectronics, the basics of PCB design, and to this day I type faster and more efficiently than I ever did before.

## Sweep

The first keyboard I built, without any experience soldering or working with a bill of materials, was the [Sweep](https://github.com/davidphilipbarr/Sweep), a popular open-source keyboard design. It's the top one in the above image. Custom keyboards are surprisingly simple in nature. The only required parts are microcontrollers, TRRS jacks, PCBs, switches, and caps. 

Upon sourcing those, the building process comes down to soldering the TRRS jacks and microcontrollers onto both halves of the PCB, setting the switches, soldering those to the PCBs, and applying the keycaps. Soldering small parts requires a gentle touch and ample patience, which was a challenge for sure.

Once the keyboard is built, the microcontrollers need to be flashed with firmware to assign letters and symbols to each key. I used an open-source firmware called [QMK](https://qmk.fm/), which can interpret my layout from a JSON file. After that, the keyboard was ready to use. It has a low-profile footprint, and the switches are effortless to type on. To this day I usually prefer typing on the Sweep than the keyboard I designed afterwards.

## Candid Keyboard

After the Sweep, I wanted to try my hand at designing my own keyboard with a more personal design. What resulted is the Candid Keyboard.

<p>
<img id="candid" style="vertical-align: middle" src="/images/keyboards/candid.jpg"/>
</p>

The PCB is a modified version of the [Sweep High](https://github.com/davidphilipbarr/Sweep/tree/main/Sweep%20High), a version of the Sweep that accommodates full-sized switches. The design also has holes to fit camera tripods, allowing for adjustmest of the angle of the keyboard for a more natural wrist position. 

I used [KiCad](https://www.kicad.org/), a free and open-source electronics editing suite, to reroute some of the traces and alter the shape of the PCB to my liking. I also overlayed some artwork from [one of my favorite artists](https://candidoak.bandcamp.com/music) to make the keyboard feel more personal, hence the name I ascribed to it.

<p>
<img id="pcb" style="vertical-align: middle" src="/images/keyboards/pcb.jpg"/>
</p>

## Layout

While soldering tested my patience and dexterity, and programming the microcontrollers was convoluted at times, the hardest part of switching keyboards was what essentially amounted to fully relearning how to type. I was retraining my fingers from the two-finger QWERTY technique I had gotten by with my whole life, to ten-finger touch typing on Colemak-DH on with a third of the keys available. This required a few months of daily practice.

The ever-ubiquitous and oh-so-arbitrary [QWERTY](https://en.wikipedia.org/wiki/QWERTY) has existed in the same form since its conception as a layout for 19th century typewriters. [Colemak](https://en.wikipedia.org/wiki/Colemak) is a modern and well-researched alternative which arranges the letters based on analysis of letter frequencies. This leads to the most common letters being placed on the home row, resulting in even fewer repetitive finger motions.

<figure id="colemak">
  <img src="/images/keyboards/colemak.jpg" alt="colemak">
  <figcaption>The letters layer of my custom keyboard layout.</figcaption>
</figure>

I used [keybr.com](https://www.keybr.com/) to learn how to touch type. Starting in around November 2021, I practiced for 10-30 minutes a day, as well as using the keyboard consistently throughout the day for assignments. I made it a point to never look down at the keyboard while typing. I started at about 11 WPM, and by the end of the below screenshot (June 2022), I was averaging 62 WPM. 

<figure id="keybr">
  <img src="/images/keyboards/keybr.jpg">
  <figcaption>My keybr progress. On the x-axis is the number of typing tests compared with my progression of WPM (green), typing mistakes (red) and number of letters used (purple) on the y-axis.</figcaption>
</figure>

By now I no longer dedicate time to practicing but I type at around 100 WPM. You can watch a fun typing test video [here](/images/keyboards/typingtest.webm)!
