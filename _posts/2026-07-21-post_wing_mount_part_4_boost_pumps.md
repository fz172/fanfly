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

It seems I am just unlucky with my wire harness. Last week when I connected the wires for the boost pumps for the first time, they didn't work.

I spent the last few days sitting in front my wire diagram and crawling under the panel to figure out what the issue is.

After many hours of struggle, I finally addressed the issue. The TLDR: I found some bugs on wire digram, and some bugs on the physical wiring. For reference I will leave the corrected wire diagram at the end.

### Symptom

When my master is on, I hear no boost pump sound. However I can connect to the web portal from the boost pump control module 192.168.4.1 (see my last post) which detects my fuel selector position correctly, but complains there is no voltage across both pumps.

I toggled the boost pump override switch, still nothing happened.

So I need to figure out why the pumps don't have voltage.

### Understanding the Problem

A few things I ruled out:

1. So since both pumps are getting 0 voltage, it's highly unlikely that I have 2 bad pumps.
   - It's of course still possible. To rule this possibility out, I disconnected the wires at the pump, and connected it with 12 v benchtop power supply. Both pumps worked. So the pumps are good.
2. Power supply issue from VP-X? Probably no. According to the wire diagram, both pumps and the pump control unit gets power from the same VP-X pin. So if pump control unit is working, power is there.
3. Since both pumps are displaying the same symptom, the problem is likely at a common source rather than a individual pump's wire.

Based on the above, I decided to trace in 2 ways: first trace the ground wire circuit, then trace the power wire circuilt.

### Confusion

I took out my wire diagram, and this is where things got confusing.

There are several views of the system to cross reference (wire tracing diagram, and connector pinouts). Unfortunately the 2 views I needed the most do not match.

On the wire diagram, it says the power goes out ot VP-X, then to RH1 connector's pin 30/31. But on the connector pinout sheet, RH1 connector does not have pin 30/31. Similarly, it also shows the ground wires for the 2 pumps go through RH1-30/29. But the same diagram also says the power of one of the pumps use RH1-30. So that's clearly wrong.

At this stage, the wire diagram is useful to show me the circuits, but I cannot trust the pin labeling at all.

My friend/fellow builder Kevin came to the rescue. His airplane also has the same boost pump system, so he shared his wire diagram with me. On his diagram, the labeling shows the wires actually go to RH2.

This prompted me to check my connector pinout for RH2. And the 4 pins (power+GND for each pump) are indeeded listed on there.

So, I have a few pieces of questionable information on hand:

- wire circuit tracing - the trace looks reasonable.
- pinout labeling on the diagram - definitely not trustworthy.
- connector pinout from my own diagram - RH1 not trustworthy, RH2 maybe.
- connector pinout from Kevin's diagram - useful to help clear things up when comparing my physical wiring.

### Digging Through Wires

With more questions than answers after tracing the wire diagram, I start to open up the panel and trace wires one by one.

#### VP-X Power

I started from the easier tasks: check VP-X power. This is done by connecting an ethernet cabel to my laptop, and run the VP-X configurator app. The pin supplying the power should be always on. And since the pump control unit is working, I don't expect this part to have any problem. And indeed it's configured correctly.

![](https://lh3.googleusercontent.com/pw/AP1GczM-RDkkZurloF5jiCLilK36tGhehCk506rXGlKz3BA14S2dwKekQ4-kle5xKSeEYi_ACF2VGbzRTbm55Hu91AYNgN4t317oO-R5VP56_9sXuBB34AJV9b0x6DKnlLJxio3hAWmnB-pdUXw0EEtENGPP7A=w3166-h2374-s-no-gm?authuser=0)

#### Checking FP1 Connector Pinouts

When I connected FP1 many months ago, I noticed some wires were pinned incorrectly, so the first thing I wanted to check is to make sure the pins are all correct in FP1. Since the pinouts on my FP1 and Kevin's FP1 match exactly, I felt like I could trust the pinouts on this one.

I took apart both the male and female plugs, and checked the label on each wire. They are all good.

#### Checking RH1 and RH2 Harness Side

This is the more challenging part. I needed to reach back to behind my G3X and GNX375 to unplug the RH1/RH2 harness connectors. They are the two big plugs right at the center of the rack. Fortunately I don't have a MFD, so I could get my hands into the space from the big hole on the right side of the panel.

![](https://lh3.googleusercontent.com/pw/AP1GczN6pzCFuIk0PdnQHSESUu5UuBLtIG2e_gIXBF5sPITMjU5UkrFEgRc_-de2o9rpRfWqTjNvTm24K1ptPRbuUXIcloANwRq_QyCGJU8Ra2YZgx-1ywYx466nyq_l1aIQYjsSGmlo-sya75H-7V6Xp_Wm3g=w1780-h2374-s-no-gm?authuser=0)
_RH1 Socket End_

![](https://lh3.googleusercontent.com/pw/AP1GczNIUvQqnUHP-OqlE9fwJ6ZaK-7Uw4ae2MlKIzI7AK8v4MfPV5-QHTdenZWp8409KAuLXezehV03lrzPFvFEim3h3-94FN8cKqfxBPA3fW6arIzAiM1KkmFsVaw2WjDA_pqjTb4nDAsMoZryMDyw84B3iw=w3166-h2374-s-no-gm?authuser=0)
_RH2 Socket End_

![](https://lh3.googleusercontent.com/pw/AP1GczPRr8Ncvami45e7C0XzaFAo2ijhxpdLiw8csQZyvYRuaOloSW8cHhLCQQgE1MpistwV-9zmbYm2qa9phm3BhYnv8Wug30Vp_IDpVvz9y-xApSa9yWI7oWemuWVTaDL_GPUqZPyqIE4ybXjYRqSsLMeG1A=w1780-h2374-s-no-gm?authuser=0)
_RH1 (left) RH2 (right) Pinned End_

Once disconnected, I took pictures and counted the pins on each plug. As seen from the picture, the RH1 male end has 28 pins, but the female end has 32 sockets. And RH2 male end has 21 pins but female end has only 17 sockets. It's clear there is some mismtach going on.

My theory at this point is: The male end for RH2 was connected following the connector pinout diagram, and it has the required power and ground wires at pin 19-22. But the female end 4 wires were connected following the (buggy) wire diagram and ended up on RH1. If this is true, I should find the power/ground wires I need on the RH1 female connector.

#### Disembling the RH1 Connector

So, I proceeded to take apart the RH1 connector, and traced the wires on the last 4 pins. And indeed I found my missing wires: FPCM15A, FPCM14A, FPCM4D, FPCM5D.

![](https://lh3.googleusercontent.com/pw/AP1GczPuMucPFMoOJgkrfs_QNT7ZVSrUH6Gg7Y0h1ZcL5g_WgpT32cV9tzGHsLvlQEKjEd_Gt9_KEkYumJUXqH9NHEdNe7OpTGoF4trPSrZzq8Z0u37ybJ_B2Tn6mthX4h3d2aB81zkca-sH7n0_pjDAcsnkww=w1780-h2374-s-no-gm?authuser=0)

#### Putting the Wires to the Right Location

Now that I have my 4 pump wires, I need to put them to where they belong. I know they will have to go onto RH2. And it's likely the 19-22 postion where RH2 has 4 male pins waiting. However, given the bugs I've seen on the connector pinout, I do not trust the pin numbers that's listed on there.

I crawled under the dashboard and opened the back shell of the RH2 connector, and traced the wire lables for the wires on the last 4 pins.

The space was too tight I couldn't really take pictures, but after a lot of yoga crawling I confirmed the pinout on my diagram was correct, except they got the wire's segment wrong. For example, they listed the wires as FPCM4B18 and FPCM5B18 but I found FPCM4D18 and FPCM5D18. When every connectors are connected they are the same circuit but the segment label (B versus D) is important to help me understand how the current flows and important to help design continuity test when the connectors are unplugs.

With the last piece of puzzle figured out, I corrected my wire diagram on laptop.

![](https://lh3.googleusercontent.com/pw/AP1GczPBTJe_8FiYxgu0Hq1XltVWKlPMwQWrZYkTosQUCWa3cXZ8bkbHzrASz3ztEvlh6E1UOXmzxvu0zNavh39QOCmCXLHg_fxoO6BArn0aQxdmS4Wa5uxtHLU2SF8YtSI27TcPOViE5XTCirG9zt4OklmgIQ=w704-h1018-s-no-gm?authuser=0)

![](https://lh3.googleusercontent.com/pw/AP1GczN2qfM7gGXi40xgtMwkY85tNW7GbICsWhIL2WSle-SkiSbWzwvYX2TDsVLYOWt4JgVQwq1VVxd8-7Du3zik08W3KH-h8fsOvDu4916YXOZWfd0VPEZF3Az_1QEbFSMzLqyg7wINd86SBykzAl5KinsQ6g=w1063-h492-s-no-gm?authuser=0)

Then I moved the 4 pins to RH2 position 19-22.

#### Continuity Testing

Since the power is always connected through VP-X, I assumed there should be no problem after th pins are relocated (wrong! more on this later)

I focused on testing the continuity for ground, since it involves a switch (the boost pump override).

From the diagram, the ground should flow all the way to FP1-14 and FP2-15 when the boost pump override switch is turned on AND FP1-11 is connected.

So I make a short probe wire to temporarily connect FP1-11, then turned on the pump override switch, and tested the ground continuity on the FP1 connector. And it worked.

![](https://lh3.googleusercontent.com/pw/AP1GczOUA1uOPyfzU4XFRQEhMm5K9ZKvpmvz5Z_vQX5ZoCV3wWlFZjgERY-g_7m0rlyj5YY8wgy861tePgnG2oIlGrwJpUIsDsf-yBaO8GD0qYJR0hqRItVVuun4lTt785x3XQeOe3tpNaSa03sFhqUnd4rrEw=w3166-h2374-s-no-gm?authuser=0)

I could tested more by connecting FP1 and moving to RH2, but decided to skip this test and just connect the full harness and test the end to end.

#### Testing End to End

Spent 20 minutes to reconnect everything back to operational state, then turned on the master switch.

This time, I heard the right pump clicking for a few seconds then stop. That's a good sign.

However I still don't hear the left pump working. And the web portal (192.168.4.1) confirms that the left pump's voltage still being 0.

Since this time it's a single pump, this is a separate issue (unless I missed some wire when relocating them). Time to disconnect harness again.

#### Testing Power and Ground from the Left Pump

So left pump isn' working, it could be either power or ground or both.

I disconnected the left pump's 2 pin connector, and tested voltage on the power line and ground conitnuity on the ground line.

Ground line: no continuity when boost pump override is off. Has continuity when the override switch is on. This is good. The entire ground wire is working.

Power line: with master switch on, I'm reading 0 v. For comparison, I'm reading 13v on the right pump.

So the problem is at the power line.

#### Probing Power Line Segment by Segment

I'm actually releived when I understand the problem is at the power line, but the power circuit for the pump is pretty simple. It's just a wire from VP-X all the way to the pump. The wire is separated into 2 segments at the RH2 connector.

So I disconnected RH2 once again, and also disconnected the J12 plug on VP-X. This exposed the first segment of the pump power wire.

I tested continuity between the RH2-20 and J12-7 and have a good continuity. This is for the right pump.

Then I tested RH2-19 and J12-7. Initially I got no continuity. But as I moved things around and potentially wiggled the wires unintentionaly, I started to get continuity. To me, this is an indication that the RH2-19 pin is badly crimped, a potential loose wire.

To get more confirmation, I tested the continuity between RH2-19 and -20. Since the power is spliced out of the same power pin, -19 and -20 should be internally connected. I initially read no continuity. Then I read ~40-50 ohms resistance for a few minutes, then down to 0.2 ohms.

For an aviaition wire, I expect the resistance to be always neglegible (around 0.2 neighborhood on my meter). So definitely something is wrong on the -19 pin.

#### Fixing the -19 Pin

Now that I know the problem, fixing was not hugely difficult. I cut the bad pin out, and recrimped a new pin on the -19 position.

I had to do it carefully, because the wires were not very long so I needed to do the work with a headlamp and stick the tools inside the panel.

Once crimped, I put everything back and reconnected the plugs.

![](https://lh3.googleusercontent.com/pw/AP1GczMRxO3uO6WmZTVlmY68dno4EixitxIPx9SQY6TMATzgojGrW8PUWEUJbITrjakcEKcb79tivfG6JQbg4dWOVZiSHF8ufImtlVN56DVGlajW1E38vp4MiaVmj2pXH2KyhFtNPxUX4knoGCyerMPQCajwOA=w1780-h2374-s-no-gm?authuser=0)

#### Testing End to End (Second Attempt)

Second time is the charm.

I turned on the master switch, and this time both left and right pumps started to click. Left click stoped first, then right click stop. The FPCM error cleared from G3X alert box, as the pumps passed their self-test.
