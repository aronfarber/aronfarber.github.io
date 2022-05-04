---
title: keyboard
date: '2021'
description: "a summary of my experiences building and designing a custom keyboard."
---
<meta name="robots" content="noindex, nofollow, noarchive">

<img id="keyboard" src="/images/keyboard/keyboard.jpg">

these days, a [significant portion of human uptime](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0165331) is spent on a screen, whether it be for work, academia, or even leisure. over the past year i've taken an interest in optimizing my online efficiency to reduce the time i need to spend online. i reckoned with this by attempting to master the devices that are responsible for bridging the interactional gap between us and our computers: keyboards. improving my [typing speed](https://en.wikipedia.org/wiki/words_per_minute) seemed like an obvious first step. after all, the faster that words can be translated from my mind to my screen, the faster i can finish essays, send emails, or write posts on a website.

ultimately though, what started with a half-baked effort to improve my typing speed ended with me learning to solder, learning to use an electronics design software suite, building three fully-functional keyboards, and designing my own. the world of keyboards is surprisingly rich, with a large and devoted open-source community that was vital to me succeeding with absolutely no prior experience. there are plenty of praises to sing about customizing an ergonomic, sustainable keyboard of your own, but ultimately i merely want to share my experience and document my journey. enjoy, and feel free to skip around the contents of this page. you can also find my code and files for my keyboards on [github](https://github.com/thegithubrespectorhasloggedon/candid-keyboard).

#### ergonomics [^1]

as i researched more, it became abundantly clear that my excessive use of a non-ergonomic keyboard can be conducive to repetitive strain injury (rsi), a work-related injury of the human musculoskeletal system. rsi has been greatly exacerbated worldwide since the 1970s with the rise of keyboards. the [wikipedia article for rsi](https://en.wikipedia.org/wiki/repetitive_strain_injury) even highlights keyboards as a primary cause for rsi with its choice of examples and pictures. to combat this, when choosing a keyboard design, i chose to make some drastic changes, outlined below:

- 34 keys: the deleterious repetitive motions associated with keyboard use can be mitigated by reducing the amount of movement required to type. with a 34-key design, the furthest my fingers ever have to move is one key's distance away from their home row positions. the removed keys are compensated for with layers and macro keys.

- colemak-dh: the ever-ubiquitous [qwerty](https://en.wikipedia.org/wiki/qwerty) has existed in the same form since it's conception for use with 19th century typewriters. [colemak](https://en.wikipedia.org/wiki/colemak) is a modern and well-researched alternative which arranges the letters based on mathematical analysis of letter frequencies. this leads in the most common letters being placed on the home row, resulting in even fewer repetitive finger motions.

<figure id="colemak">
  <img src="/images/keyboard/colemak.jpg" alt="colemak">
  <figcaption>the letters layer of <a href="https://github.com/thegithubrespectorhasloggedon/candid-keyboard/tree/main/layout">my custom keyboard layout</a>.           </figcaption>
</figure>

- split: a traditional keyboard requires a small amount of space between both hands while typing, which is unnatural and can be uncomfortable. being able to keep my hands at shoulder width feels less resistive, and i've also noticed it helps with my back posture while sitting in an office chair. having a keyboard split into two halves allows me to control the positioning of my hands at will, so i have infinite granularity when it comes to adjustment. 

- tenting: the default position of the human wrists is pretty much completely sideways (as they will naturally rest while standing up). however, most keyboards cause [ulnar pronation](https://pubmed.ncbi.nlm.nih.gov/10443595/) by requiring the user to align their wrists such that their hands are facing down. pronation causes unnecessary strain on the wrists, which can be deleterious over extended periods of time. using a camera tripod, i can tent the keyboard at an angle to keep my wrists in more of a natural position.

<img id="tenting" src="/images/keyboard/tenting.jpg">

- column-staggered: the rectangular form factor of most keyboards leads to a row-staggered orientation of keys, but our fingers are not all the same length. i sought out a design which staggered the five columns of keys to fit the actual shape of human hands.

<figure id="comparison">
  <img src="/images/keyboard/comparison.jpg">
  <figcaption>my keyboard juxtaposed with the conventional keyboard i used prior.<br>watch a typing test of the lower keyboard <a href="https://raw.githubusercontent.com/aronfarber/candid-keyboard/main/gallery/thocktest.mp4">here</a>.</figcaption>
</figure>

#### building

the first keyboard i built, without any experience soldering or working with bills of materials, was the [sweep](https://github.com/davidphilipbarr/sweep), an open-source project by [david barr](https://github.com/davidphilipbarr). it met my desired criteria for a build, and [tutorials](https://www.youtube.com/watch?v=fBPu7AyDtkM) were readily available online to compensate for my lack of experience. keyboards, at least the ones that i chose to build, are surprisingly simple in nature; consisting of little more than the switches, keycaps, printed circuit boards (pcbs), and repurposed arduino microcontrollers. the pcbs do most of the heavy lifting by detecting when each switch's circuit is closed and sending the appopriate signal to the microcontroller that a key has been pressed.

the building process boils down to soldering the parts onto the pcbs and programming the microcontrollers to receive and process signals from the switches. soldering small parts together requires more patience and a gentler touch than i normally have, but the promise of a fully functional device of my own was enough motivation to work meticulously. the initial build process took me about 3 hours. i then flashed an open-source firmware called [qmk](https://qmk.fm/) to the microcontrollers, which can interpret a keypress from a [json file](https://github.com/aronfarber/candid-keyboard/blob/main/layout/keymap.json) to its corresponding letter, symbol, or function. 

#### design

after building a couple of sweeps, i was inspired by a [youtube video](https://www.youtube.com/watch?v=JqpBKuEVinw) by [ben vallack](https://www.youtube.com/c/BenVallack) to modify and customize the sweep to make a design that felt more personal to me. to that end, i downloaded [kicad](https://www.kicad.org/ "kicad"), which is a free and open source electronics editing suite.

using the [sweep high](https://github.com/davidphilipbarr/sweep/tree/main/sweep%20high) as a template, i removed the empty space on the pcb while rounding the corners to keep the board smooth and easy to hold. i also overlayed some song artwork from [candid oak](https://soundcloud.com/candid_oak), one of my favorite musicians, onto the silkscreen layer. what i made is [far from an original design](https://github.com/benvallack/ferris-sweep-tweaked), but the prototype arrived looking even better than i had hoped for.

<img id="pcb" src="/images/keyboard/pcb.jpg">

#### takeaways

by far the hardest part of switching keyboards has been deviating from qwerty. while my keyboards are already built and operational, i still have fifteen years worth of qwerty muscle memory to unlearn.  i've been practicing on [keybr.com](https://www.keybr.com/), a website that provides typing tests and develops a learning progression based on ai recommendations. since november 2021, i've practiced on keybr for about twenty minutes a day, and have made substantial progress having gone from 11 wpm on my first test to averaging around 65 wpm today. 

<figure id="keybr">
  <img src="/images/keyboard/keybr.jpg">
  <figcaption>number of typing tests on the x-axis compared with my progression of wpm (green), typing mistakes (red) and number of letters (purple) on the y-axis.</figcaption>
</figure>

the caveat? my speed on qwerty was 100 wpm. ironically, that means my initial goal -- improving my wpm -- is the only one i haven't yet hit. i've actually gotten slower, despite using a more efficient keyboard layout. i see it as a worthy sacrifice; banking on my neuroplasticity to completely relearn the patterns necessary to type quickly. 

overall, my typing experience has become more fun and more comfortable. keeping my fingers in a natural position on the home row with minimal finger movement is satisfying. my wrists and fingers feel noticeably more comfortable than when i typed on a traditional keyboard. while i don't have rsi and had little intention to improve ergonomics through my optimizations initially, it has become one of the most fruitful benefits of the project.

going from having no experience working with electronics to being able to make my own design has been an immensely fulfilling experience. i've now built multiple low-cost, functional keyboards designed for ergonomic optimization. i am hugely grateful to david barr, [pierre chevalier](https://github.com/pierrechevalier83/), [kyek](https://www.youtube.com/user/KyekPS3), ben vallack, and everyone else who has contributed to the development and maintenance of the open-source projects and tools that have allowed me and others to modernize our experiences with computers and learn new skills along the way.

next; learn [zmk](https://zmk.dev/) and build a fully wireless split-ergo keyboard fit with an onboard battery.

[^1]: this section contains wording that could be construed as medical advice, so it's worth noting that i am not a lisenced medical professional. although i've done ample personal research about ergonomics, the contents of this section should not be taken as inalienable fact. 
