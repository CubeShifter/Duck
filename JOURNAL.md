---
title: "Duck?"
author: "Kian Desh"
description: "A fidget toy that lets you press a keyboard switch and play a noise"
created_at: "2026-05-3"
---
# Bit of May 5th and 6th: Kinda figured out what parts I want.

I spent some time reasearching what parts I want, and made a few cart selections with what I want. I actually think I'm gonna make my own devboard so it's gonna be a bit harder but I got this. The sites i used were adafruit, digikey and aliexpress.
<img width="426" height="720" alt="Screenshot 2026-05-06 at 7 05 44 PM" src="https://github.com/user-attachments/assets/ac8f4ca4-4ff3-4a7d-bb4f-ee89e50f6bb1" />

<img width="2068" height="300" alt="Screenshot 2026-05-06 at 7 10 39 PM" src="https://github.com/user-attachments/assets/3deeeaf3-83d9-499e-b0a4-3b00e5fd2993" />

**Total time spent: 40 mins**

# May 6th: Read a bit about how to make an RP2040 board and failed to use Kicad.

I started using the hack club guides for designing an rp2040 board, a lot of it was just reading it and I placed down one thing in KiCad <img width="470" height="728" alt="Screenshot 2026-05-07 at 5 26 12 PM" src="https://github.com/user-attachments/assets/ac6d68a8-13de-4334-9b00-b54f9f082eaf" />


**Total time spent: 30 mins**

# May 7th: Started designing the pcb

I used the hackclub guides and starting getting the basics of the boards down and just getting better at learning KiCad. I also now know what capictors do. Hardware is fun :) <img width="1668" height="844" alt="Screenshot 2026-05-08 at 9 28 18 AM" src="https://github.com/user-attachments/assets/95cb1418-a28e-44f4-a61e-6abf9bb67ec1" />


**Total time spent: 30 mins**

# May 8th: Made the USB, Oscillator and started on the Flash

The hackclub guide is so nice, I made a lil oscillator thing which taught me what an oscialltor is also <img width="1442" height="604" alt="Screenshot 2026-05-08 at 9 50 22 PM" src="https://github.com/user-attachments/assets/e2151355-b781-43ee-9df8-e0e8da8898fe" />. I also made a usb port thing so my circuit will have usb power, and I will implement battery charging later.![Uploading Screenshot 2026-05-08 at 9.54.40 PM.jpg…]()
<img width="1322" height="812" alt="Screenshot 2026-05-08 at 9 51 22 PM" src="https://github.com/user-attachments/assets/11a59467-5296-4c17-ac33-b82537837645" />
Didnt really get that far on the flash, but I know how it works now.




**Total time spent: 1 hour**

# May 9th-10th: Finished Flash, Researched audio/battery charging, started on audio.

So I finished the flash, and thats all for the Hackclub guides.<img width="762" height="534" alt="Screenshot 2026-05-12 at 6 30 22 PM" src="https://github.com/user-attachments/assets/f540234d-d435-4200-8e12-70f12de1ceed" /> Then I looked at how some circuts use audio and battery, gave up on battery because it confused me and focused on audio. For audio I first learnt which chip I want to use, the MAX98375A. I started looking at the datasheets that confused me, so I found a prebuilt board that makes it easier to interface with the chip and copied the schematic for it. W adafruit.<img width="530" height="632" alt="Screenshot 2026-05-12 at 7 01 19 PM" src="https://github.com/user-attachments/assets/7c97c4d5-d76a-4ffb-b81d-c27da1b52145" /> I did learn how i2s works



**Total time spent: 2 hours 20 mins**

# May 18th: Worked on the MAX98375A and MCP73831
For context, today is may 25th and my lapse is being weird so my recollection of what happened won't be the best. I definetly worked on audio and got the wiring pretty easy as the adafruit guide on it was pretty good, and also claude was being useful. <img width="806" height="826" alt="Screenshot 2026-05-25 at 12 00 26 PM" src="https://github.com/user-attachments/assets/b0e8b478-91d6-4e0e-80bf-76428ce8912a" /> This image is my current schmatic, but at that point I didn't have the MAXSLEEP pin and some of the resistor and cap values were probably off. I also worked on the lipo circuit, which I orignally thought was going to be off before it got pressed, but that wont work as the RP2040 takes a couple second to boot up. Instead its gonna be in deepsleep mode until the keyboard switch gets pressed which I also wired up. <img width="1134" height="810" alt="Screenshot 2026-05-25 at 12 32 40 PM" src="https://github.com/user-attachments/assets/4bc6c2eb-6fb0-49cf-8f7a-2a7d904521d4" /> This is my lipo circuit currently, but like the amp I think I had changed some values to make it go from a 200mah to 500mah charging rate. I also copied the adafruit schematic for it along with some help from claude. I know I shouldnt be using AI but it's kinda helpful especially with me taaking an ambitious hardware project. 
**Total time spent: 2 hours**

# May 20th: Worked on the charging chip and audio chip
For context, today is may 25th and my lapse is being weird so my recollection of what happened won't be the best. I definetly worked on audio and got the wiring pretty easy as the adafruit guide on it was pretty good, and also claude was being useful. <img width="806" height="826" alt="Screenshot 2026-05-25 at 12 00 26 PM" src="https://github.com/user-attachments/assets/b0e8b478-91d6-4e0e-80bf-76428ce8912a" /> This image is my current schmatic, but at that point I didn't have the MAXSLEEP pin and some of the resistor and cap values were probably off. I also worked on the lipo circuit, which I orignally thought was going to be off before it got pressed, but that wont work as the RP2040 takes a couple second to boot up. Instead its gonna be in deepsleep mode until the keyboard switch gets pressed which I also wired up. <img width="1134" height="810" alt="Screenshot 2026-05-25 at 12 32 40 PM" src="https://github.com/user-attachments/assets/4bc6c2eb-6fb0-49cf-8f7a-2a7d904521d4" /> This is my lipo circuit currently, but like the amp I think I had changed some values to make it go from a 200mah to 500mah charging rate. I also copied the adafruit schematic for it along with some help from claude. I know I shouldnt be using AI but it's kinda helpful especially with me taaking an ambitious hardware project. 
**Total time spent: 40 mins**

# May 22nd: Revised my schematic and it should be done.
So I posted my schematic in the hackclub slack, and some few really nice people gave me some feedback. First of all they told me to run ERC, and I had to clean up the mess I had made. So I first of all put the litlle x thingies on any pins that were unused, and then also fixed some wires that werent connected properly. I also updated the amp and charging chip, I forget what i did to the amp but i changed the charging chip to 500mAh, which would be much better. I also asked claude and questioned my life choices, and the best way to do what I want is the way I am going. This is an image of my finalized schematic. [Symbol.pdf](https://github.com/user-attachments/files/28236979/Symbol.pdf)

**Total time spent: 1 hour 30 mins**

# May 23rd: Looked for footprints and imported them and it was being annoying.
So I started to assign footprints to all my parts. I thought this would be relatively easy as probably within the first hour I was done withe everything exept a few. The remaining three, however, were not easy. The USB receptable was annoying because I had to import it from jlcpcb which did not have an easy export so I had to download a tool just to do it and had to work with terminal which was really annoying. I eventually got that, but I also had to change the crystal to make it work better, but after that it was fine. The last thing which was by far the most annoying was the keyboard switch. I had to look through a repo and couldnt find anything and then looked through another one then went insane and realised I didnt need a keyboard switch footprint with an LED as they are seperate. Overall this was a really annoying process, and I did not help that I had to blow my nose every other second cause I was really sick. .<img width="1302" height="1204" alt="Screenshot 2026-05-25 at 4 10 49 PM" src="https://github.com/user-attachments/assets/824273fa-7f04-4c9f-8e08-a06a63a7b245" />


**Total time spent: 2 hours 30 mins**

# May 24th:Started and failed on the footprint.
This was really annoying. I first of all imported all the parts into the the footprint, and it worked fine. I played around with arrangement and I had enough space. I then reimported my schematic, and saw some errors with the USB. I then tried for 30 mins to fix them and managed to find a correct footprint, and fore some reason whenever I reimport a footprint my KiCad crashes. This was normally fine, but I pressed the wrong button but this journal and half of the last ones progress got erased. <img width="2582" height="1682" alt="Screenshot 2026-05-25 at 4 11 15 PM" src="https://github.com/user-attachments/assets/121f79e2-c38e-41bc-90e7-db9abf10efd6" />
**Total time spent: 1 hour 15 mins **

# May 25th: I worked on this journal.
Whoa this is so meta, I worked really hard and forgot about the journal but I updated it

**Total time spent: 50 mins**





