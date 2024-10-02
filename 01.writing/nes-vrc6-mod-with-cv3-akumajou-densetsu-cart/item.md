---
title: 'NES VRC6 mod with CV3/Akumajou Densetsu cart'
media_order: 'ad1.jpg,gyro1.jpg,gyro2.jpg,gyro3.jpg,mod1.jpg,mod2.jpg,mod3.jpg,densetsu.jpg'
date: '27-01-2014 05:15'
publish_date: '27-01-2014 05:15'
taxonomy:
    category:
        - Blog
    games:
        - 'Castlevania (Classic Era)'
routes: 
  default: '/vrc6-mod'
  aliases:
    - '/nes-vrc6-mod-with-cv3-akumajou-densetsu-cart'
---

[splitbox class="splitboxsmall"]
![gyro1](gyro1.jpg?lightbox)<br>
Gyromite

![gyro2](gyro2.jpg?lightbox)<br>
Gyromite, disconnected from the FC converter

![gyro3](gyro3.jpg?lightbox)<br>
The inside of Gyromite, with FC converter

![ad1](ad1.jpg?lightbox)<br>
Akumajou Densetsu with my custom logo

![densetsu](densetsu.jpg?lightbox)<br>
I cannot explain how much hell this was to get out of that fucking case

![mod1](mod1.jpg?lightbox)<br>
Connecting to pin 54 on the other side

![mod2](mod2.jpg?lightbox)<br>
Connecting to pin 45

![mod3](mod3.jpg?lightbox)<br>
Pin 3 and Pin 9, with the pot through the front. Just need a nice dial now.
++++

<br>
So this all started with reading about how gyromites occasionally containing famicom converters. Due to early supply constraints during the NA release, the first run of gyromite carts all contained these funky little adaptor, which allowed them to resell famicom gyromite in the US. So I tracked down my gryomite cart, felt it was clearly super heavy and cracked it open.

A converter! Hooray! So immediately I decided I wanted to make my self an Akumajou Densetsu cart. CV3 is my favorite castlevania, and I much prefer the Japanese version to the US version (mostly due to the music, but also because I hate level based damage scaling). So I went and google and [found this cute mod](http://callanbrown.com/index.php/castlevania-iii-with-full-famicom-audio). Now I REALLY needed to make that cart. So I ordered an Akumajou Densetsu famicom cart and began planning out the rest of the mod. I didn’t wanna do the wire-out-of-cart mod — that’s cute but kinda ugly. So I began researching how I’d do the console mod. Turns out there are like a million small variations on how to do this, so that took me forever to work out.  

Also had to take the time to do my version of the cover. Callan’s nice looking and was the basis for mine, but certain elements, like weirdly cropped art and the logo didn’t work for me. Since there was no good scans of the CV3 splash art, I had to sorta rebuild the logo. In the end, I did the label with photo paper and some glue. Worked much better than the ‘label’ method. Label method gets the label thickness right, but lacks the clarity of a nice print.

Anyways eventually I got all my components and decided my course of action. One source of confusion for this mod was the resistors. Resistors are required to balance the audio of the VRC6 with the NES, else the VRC instruments will overpower everything. Most recommend 47k resistors, but other recommendations, especially with famicom carts, went up to 100k resistors. So instead I just got a 100k pot. There were also several different unused pins you could use on the nes for this mod and I decided to use the same one as the powerpak. I doubt I’ll be buying a 120$ powerpak any time soon, but hey, best to be careful. Then I could also adjust the volume accordingly.

The annoying thing with the powerpak pin is it required me to wrap a wire around the converter. It also sucked because that pin was harder to solder without interfering with the contacts. Worked out fine in the end. The internal mod on the NES was much simplier. The NES has extended audio capables, but they were only made to work through the expansion port on the bottom of the NES. Soldering the pot between expansion port 9 (the expansion music min) and port 3 (audio out) was all that was needed to get the mod working. The pins didn’t take solder well, so it was a bit of a pain, but working on those pins felt less risky, so it wasn’t that big a deal.  

Anyways here’s a little peak at the mod. Sorry for the poor quality and rotated video. I’ll probably stream the game tomorrow.

[plugin:youtube](https://www.youtube.com/watch?v=IoBbBhq_CLo)
[/splitbox]