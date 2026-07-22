---
layout: post
title: "Post Wing Mounting Work - Part 4 - The Boost Pump Saga"
categories: [Wing, ~boost_pump]
tags: [fuel_pump, avionics, wiring]
minutes: 840
---

## TLDR

- Identified and fixed the boost pump power issue

## Details

It seems I am just unlucky with my wire harness. Last week, when I connected the wires for the boost pumps for the first time, they did not work.

I spent the last few days sitting in front of my wiring diagram and crawling under the panel to figure out what the issue was.

After many hours of struggle, I finally addressed it. The TL;DR: I found bugs in the wiring diagram and in the physical wiring. For reference, I will leave the corrected wiring diagram at the end.

### Symptom

When my master switch is on, I hear no boost pump sound. However, I can still connect to the web portal from the boost pump control module at 192.168.4.1 (see my last post), which detects my fuel selector position correctly but reports that there is no voltage across either pump.

I toggled the boost pump override switch, but still nothing happened.

So I needed to figure out why the pumps did not have voltage.

### Understanding the Problem

A few things I ruled out:

1. Since both pumps are getting 0 volts, it is highly unlikely that I have two bad pumps.
   - It is still possible, of course. To rule that out, I disconnected the wires at the pump and connected them to a 12 V benchtop power supply. Both pumps worked. So the pumps are good.
2. A power supply issue from the VP-X? Probably not. According to the wiring diagram, both pumps and the pump control unit receive power from the same VP-X pin. If the pump control unit is working, power is there.
3. Since both pumps show the same symptom, the problem is likely at a common source rather than an individual pump's wire.

Based on that, I decided to trace the issue in two ways: first, the ground wire circuit, and then the power wire circuit.

### Confusion

I pulled out my wiring diagram, and this is where things got confusing.

There are several views of the system to cross-reference: the wiring tracing diagram and the connector pinout diagrams. Unfortunately, the two views I needed most do not match.

On the wiring diagram, it says the power goes out of the VP-X and then to RH1 connector pins 30/31. But on the connector pinout sheet, RH1 does not have pins 30/31. Similarly, it also shows the ground wires for the two pumps going through RH1-30/29. But the same diagram also says the power for one of the pumps uses RH1-30, which is clearly wrong.

At this stage, the wiring diagram is useful for showing me the circuits, but I cannot trust the pin labeling at all.

My friend and fellow builder, Kevin, came to the rescue. His airplane also has the same boost pump system, so he shared his wiring diagram with me. On his diagram, the labels show the wires actually go to RH2.

That prompted me to check my connector pinout for RH2. The four pins (power and ground for each pump) are indeed listed there.

So, I had a few pieces of questionable information in hand:

- wiring circuit tracing: the trace looked reasonable.
- pinout labeling on the diagram: definitely not trustworthy.
- connector pinout from my own diagram: RH1 not trustworthy; RH2 maybe.
- connector pinout from Kevin's diagram: useful for helping clear things up when comparing my physical wiring.

### Digging Through Wires

With more questions than answers after tracing the wiring diagram, I started to open up the panel and trace the wires one by one.

#### VP-X Power

I started with the easier task: checking VP-X power. This was done by connecting an Ethernet cable to my laptop and running the VP-X configurator app. The pin supplying the power should be always on. Since the pump control unit is working, I did not expect this part to be a problem. And indeed it was configured correctly.

![](https://lh3.googleusercontent.com/pw/AP1GczM-RDkkZurloF5jiCLilK36tGhehCk506rXGlKz3BA14S2dwKekQ4-kle5xKSeEYi_ACF2VGbzRTbm55Hu91AYNgN4t317oO-R5VP56_9sXuBB34AJV9b0x6DKnlLJxio3hAWmnB-pdUXw0EEtENGPP7A=w3166-h2374-s-no-gm?authuser=0)

#### Checking FP1 Connector Pinouts

When I connected FP1 many months ago, I noticed some wires were pinned incorrectly, so the first thing I wanted to check was to make sure the pins were all correct in FP1. Since the pinouts on my FP1 and Kevin's FP1 match exactly, I felt like I could trust the pinouts on this one.

I took apart both the male and female plugs and checked the label on each wire. They were all good.

#### Checking RH1 and RH2 Harness Side

This was the more challenging part. I needed to reach back behind my G3X and GNX375 to unplug the RH1/RH2 harness connectors. They are the two big plugs right at the center of the rack. Fortunately, I do not have an MFD, so I could get my hands into the space from the big hole on the right side of the panel.

![](https://lh3.googleusercontent.com/pw/AP1GczN6pzCFuIk0PdnQHSESUu5UuBLtIG2e_gIXBF5sPITMjU5UkrFEgRc_-de2o9rpRfWqTjNvTm24K1ptPRbuUXIcloANwRq_QyCGJU8Ra2YZgx-1ywYx466nyq_l1aIQYjsSGmlo-sya75H-7V6Xp_Wm3g=w1780-h2374-s-no-gm?authuser=0)
_RH1 Socket End_

![](https://lh3.googleusercontent.com/pw/AP1GczNIUvQqnUHP-OqlE9fwJ6ZaK-7Uw4ae2MlKIzI7AK8v4MfPV5-QHTdenZWp8409KAuLXezehV03lrzPFvFEim3h3-94FN8cKqfxBPA3fW6arIzAiM1KkmFsVaw2WjDA_pqjTb4nDAsMoZryMDyw84B3iw=w3166-h2374-s-no-gm?authuser=0)
_RH2 Socket End_

![](https://lh3.googleusercontent.com/pw/AP1GczPRr8Ncvami45e7C0XzaFAo2ijhxpdLiw8csQZyvYRuaOloSW8cHhLCQQgE1MpistwV-9zmbYm2qa9phm3BhYnv8Wug30Vp_IDpVvz9y-xApSa9yWI7oWemuWVTaDL_GPUqZPyqIE4ybXjYRqSsLMeG1A=w1780-h2374-s-no-gm?authuser=0)
_RH1 (left) RH2 (right) Pinned End_

Once disconnected, I took pictures and counted the pins on each plug. As seen in the picture, the RH1 male end has 28 pins, but the female end has 32 sockets. And the RH2 male end has 21 pins, but the female end has only 17 sockets. It is clear there is some mismatch going on.

My theory at this point is: the male end for RH2 was connected following the connector pinout diagram, and it has the required power and ground wires at pins 19-22. But the female end's four wires were connected following the (buggy) wiring diagram and ended up on RH1. If that is true, I should find the power and ground wires I need on the RH1 female connector.

#### Disassembling the RH1 Connector

So, I proceeded to take apart the RH1 connector and trace the wires on the last four pins. And indeed I found my missing wires: FPCM15A, FPCM14A, FPCM4D, and FPCM5D.

![](https://lh3.googleusercontent.com/pw/AP1GczPuMucPFMoOJgkrfs_QNT7ZVSrUH6Gg7Y0h1ZcL5g_WgpT32cV9tzGHsLvlQEKjEd_Gt9_KEkYumJUXqH9NHEdNe7OpTGoF4trPSrZzq8Z0u37ybJ_B2Tn6mthX4h3d2aB81zkca-sH7n0_pjDAcsnkww=w1780-h2374-s-no-gm?authuser=0)

#### Putting the Wires to the Right Location

Now that I have my four pump wires, I need to put them where they belong. I know they will have to go onto RH2. And it is likely the 19-22 position, where RH2 has four male pins waiting. However, given the bugs I have seen on the connector pinout, I do not trust the pin numbers listed there.

I crawled under the dashboard and opened the back shell of the RH2 connector and traced the wire labels for the wires on the last four pins.

The space was too tight for me to take pictures, but after a lot of yoga-style crawling, I confirmed that the pinout on my diagram was correct, except they had the wire's segment wrong. For example, they listed the wires as FPCM4B18 and FPCM5B18, but I found FPCM4D18 and FPCM5D18. When all connectors are connected, they are the same circuit, but the segment label (B versus D) is important because it helps me understand how the current flows and helps me design continuity tests when the connectors are unplugged.

With the last piece of the puzzle figured out, I corrected my wiring diagram on my laptop.

![](https://lh3.googleusercontent.com/pw/AP1GczPBTJe_8FiYxgu0Hq1XltVWKlPMwQWrZYkTosQUCWa3cXZ8bkbHzrASz3ztEvlh6E1UOXmzxvu0zNavh39QOCmCXLHg_fxoO6BArn0aQxdmS4Wa5uxtHLU2SF8YtSI27TcPOViE5XTCirG9zt4OklmgIQ=w704-h1018-s-no-gm?authuser=0)

![](https://lh3.googleusercontent.com/pw/AP1GczN2qfM7gGXi40xgtMwkY85tNW7GbICsWhIL2WSle-SkiSbWzwvYX2TDsVLYOWt4JgVQwq1VVxd8-7Du3zik08W3KH-h8fsOvDu4916YXOZWfd0VPEZF3Az_1QEbFSMzLqyg7wINd86SBykzAl5KinsQ6g=w1063-h492-s-no-gm?authuser=0)

Then I moved the four pins to RH2 positions 19-22.

#### Continuity Testing

Since the power is always connected through the VP-X, I assumed there should be no problem after the pins were relocated. I was wrong. More on that later.

I focused on testing the continuity for ground, since it involves a switch (the boost pump override).

From the diagram, the ground should flow all the way to FP1-14 and FP2-15 when the boost pump override switch is turned on and FP1-11 is connected.

So I made a short probe wire to temporarily connect FP1-11, then turned on the pump override switch and tested the ground continuity on the FP1 connector. And it worked.

![](https://lh3.googleusercontent.com/pw/AP1GczOUA1uOPyfzU4XFRQEhMm5K9ZKvpmvz5Z_vQX5ZoCV3wWlFZjgERY-g_7m0rlyj5YY8wgy861tePgnG2oIlGrwJpUIsDsf-yBaO8GD0qYJR0hqRItVVuun4lTt785x3XQeOe3tpNaSa03sFhqUnd4rrEw=w3166-h2374-s-no-gm?authuser=0)

I could have tested more by connecting FP1 and moving to RH2, but I decided to skip that test and just connect the full harness and test it end to end.

### Testing End to End But Running into a Second Problem

I spent 20 minutes reconnecting everything back to an operational state, then turned on the master switch.

This time, I heard the right pump clicking for a few seconds and then stop. That is a good sign.

However, I still do not hear the left pump working. And the web portal (192.168.4.1) confirms that the left pump's voltage is still 0.

Since this time it is a single pump, this is a separate issue (unless I missed some wire when relocating them). It was time to disconnect the harness again.

#### Testing Power and Ground from the Left Pump

So the left pump is not working. It could be either power, ground, or both.

I disconnected the left pump's two-pin connector and tested the voltage on the power line and the ground continuity on the ground line.

Ground line: no continuity when the boost pump override is off. Continuity when the override switch is on. This is good. The entire ground wire is working.

Power line: with the master switch on, I am reading 0 V. For comparison, I am reading 13 V on the right pump.

So the problem is on the power line.

#### Probing the Power Line Segment by Segment

I was actually relieved when I understood that the problem was on the power line, but the power circuit for the pump is pretty simple. It is just a wire from the VP-X all the way to the pump. The wire is separated into two segments at the RH2 connector.

So I disconnected RH2 once again and also disconnected the J12 plug on the VP-X. That exposed the first segment of the pump power wire.

I tested continuity between RH2-20 and J12-7 and got good continuity. This was for the right pump.

Then I tested RH2-19 and J12-7. Initially I got no continuity. But as I moved things around and potentially wiggled the wires unintentionally, I started to get continuity. To me, this indicated that RH2-19 pin was badly crimped, a potential loose wire.

To get more confirmation, I tested continuity between RH2-19 and -20. Since the power is spliced out of the same power pin, -19 and -20 should be internally connected. I initially read no continuity. Then I read about 40-50 ohms resistance for a few minutes, then down to 0.2 ohms.

For an aviation wire, I expected the resistance to be negligible (around the 0.2 neighborhood on my meter). So something was definitely wrong on the -19 pin.

#### Fixing the -19 Pin

Now that I knew the problem, fixing it was not hugely difficult. I cut the bad pin out and recrimped a new pin on the -19 position.

I had to do it carefully, because the wires were not very long, so I needed to do the work with a headlamp and stick the tools inside the panel.

Once crimped, I put everything back and reconnected the plugs.

![](https://lh3.googleusercontent.com/pw/AP1GczMRxO3uO6WmZTVlmY68dno4EixitxIPx9SQY6TMATzgojGrW8PUWEUJbITrjakcEKcb79tivfG6JQbg4dWOVZiSHF8ufImtlVN56DVGlajW1E38vp4MiaVmj2pXH2KyhFtNPxUX4knoGCyerMPQCajwOA=w1780-h2374-s-no-gm?authuser=0)

### Testing End to End (Second Attempt)

Second time was the charm.

I turned on the master switch, and this time both left and right pumps started to click. The left click stopped first, then the right click stopped. The FPCM error cleared from the G3X alert box as the pumps passed their self-test.
