---
title: materials
date: '2021'
description: "a technical paper i wrote for my materials science class."
---
<meta name="robots" content="noindex, nofollow, noarchive">

originally written in december 2021

<img id="keyboard" src="/images/comm/keys.jpg">

for my [materials class](https://catalog.northeastern.edu/search/?P=CIVE%202260) in the fall 2021 semester, students were assigned the task of designing and conducting a semester-long lab experiment to test the mechanical properties of a material of our choosing. due to my [newfound obsession with keyboards](/projects/keyboard/), i decided to test thermoplastics, as they are commonly used in keyboard switches. ultimately, it was a valuable first foray into engineering lab experience. being able to interface with genuine lab equipment and use real data to write a scientific paper was a pretty fulfilling experience. in the end i recieved no grade or feedback on the project, as is the case with most finals at northeastern. i'm proud of my work regardless, so i figured i'd highlight it.

you can read my report [here](/images/comm/CommProject_Final.pdf).

### takeaways

i had some qualms with the administration of the project, and would do a number of things differently myself were i to repeat it. the main issue rests in the fact that the project was assigned alongside the entire course, so we began the project having no knowledge about material properties or testing. we were expected to choose which material we would be testing near the beginning of the semester, at which point I didn't know whether such an experiment was even feasible or not.

due to a shortage of equipment availability, i was given a [heavy-duty compression machine](/images/comm/machine.jpg) with a load capacity far larger than what a switch could handle. this meant that my data wasn't as specific as i had hoped. keyswitches are delicate, and the machine was mostly unable to detect the small nuances in displacement of the switches throughout the application of force. the yieds i extrapolated from the resulting stress-strain curves came from very slight changes in measured stress that weren't necessarily actually indicative of a yield. the limited granularity in force application also meant that i got essentially no linear elastic deformation from the switches, which i needed to calculate [young's modulus](https://en.wikipedia.org/wiki/Young's_modulus).

i would've loved to additionally conduct fatigue testing of the springs inside various switches. this would most likely entail repeatedly applying stress to multiple switch springs until they fail. with that data, an [s-n curve](https://www.sciencedirect.com/topics/engineering/s-n-curve) can be derived by plotting various points of stress applied vs. the number of cycles at that amount of applied stress that results in the failure of the spring. with an s-n curve, [miner's rule of cumulative damages](https://www.sciencedirect.com/topics/engineering/miner-linear-damage-rule) could be used to extrapolate the amount of keypresses (based on the average human typing force) it would take to cause a keyswitch spring to fail. by the time i had learned of this in the course, the first half of the paper had already been due.

at the end of the day, given the circumstances under which the project was assigned, i'm quite happy with the report i wrote. regardless of the validity of my conclusions, the project increased my level of experience with laboratory testing and reporting, which is definitely worth something.
