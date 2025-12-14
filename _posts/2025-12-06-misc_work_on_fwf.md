---
layout: post
title: "Misc Work on Firewall Forward"
categories: [Firewall, ~firewall_forward]
tags: [starter, wiring, fusebox, avionics]
minutes: 220
---

## TLDR

- Continued to debug GNX375 "GDU disconnected" message
- Started to install starter relay and Rotax fusebox
- Removed nose wheel fork angle
- Studied throttle cable connection

## Details

This week I multi-threaded on quite a few small projects, although none of them made huge progress.

### GNX375 Debugging

I continued my debugging journey on the GNX375 message "GDU Disconnected, external flight plan crossfill inoperative".

Sent email to g3xpert@, and their answer was that I should set GDU to ***NOT PRESENT*** in the configuration mode. Reason: that setting is for TXi system, not G3X system.

 So I did that. But the message was not cleared.

I then turned off "Crossfill flight plan" in the GNX375 settings, the message went away. When I turn the setting back on however, the message went back.

I will need to check if the crossfill still works when I turn it off. The setting might not have been for G3X.

### Starter Solenoid

I went ahead and started to work on the starter solenoid and the Rotax fusebox. Both required a bit of work so I didn't get to finish them.

I installed the M6 rivnuts and the rubber stands for both. And torqued one of the bolts of the starter solenoid.

![img](https://lh3.googleusercontent.com/pw/AP1GczOPhn_ZO4UNyIpBR8LhjROCkJnuAZxO50Gul7SnZK52leToWQgszZHFQ8XYV6d9fjtSm03Om5vzL55-m9M7el2-66s6vxjLk8e9V6uxFYYLwXCxuHEusDjvUuP5fgJR3FqicgB9r5tkq224tQv3ilBjRQ=w1164-h873-s-no-gm?authuser=0)

Leaving the other bolt off for now, as I need to connect the starter ground wire once the engine is installed.

And before installing the fusebox, I needed to route a #4 wire from the master solenoid to the starter solenoid. My first attempt is to stack 2 battery lugs on the master relay. But the lugs were too thick, I don't see any reasonable way to stack them safely.

So I decided to buy a small bus bar from Amazon and install it next to the master solenoid. The idea is that I will run a wire from the master to the bus bar, then two wires from bus bar to the shunt (existing wire), and to the starter relay (new wire). I'm currently waiting for the bus bar to arrive, which should be next week.

### Rotax Fusebox

The fusebox (in theory) sits on top of the wires aforementioned, on the top right section of the firewall.

![img](https://lh3.googleusercontent.com/pw/AP1GczNMkVFnvg_Dx3XsYLyWfyYXaR0axf0lid5JuLqqoOXlrCmohUXZj7ulLrKc_83F_EfAAb63jalWEgFYtPcqBhT6ZkBazwPJzgw9MbNScZ6xrtUFA2YUPqa064Ukf2a7mylxspiUC9qgLwZNZ0BjI_tkIg=w655-h873-s-no-gm?authuser=0)

I did a quick fit, it seems to work. Once I complete the bus bar & wiring for the starter solenoid, I will do the fusebox.

One special note is that I need to remove the regulator B from the fusebox when installing, and put it directly on the engine mount for better cooling.

### Engine Mount Angle Plate

So another thing I had to deal with this week is the direction of this angle.

![img](https://lh3.googleusercontent.com/pw/AP1GczNATBrc6JKm8jHXBkFZyPW4yHkGnINb0V2nLsVudmbQMlgdv-N66vCu4o8fgPgdM1b3U9uBE2nmMIMHXYEgciQgJPtNA5pFKnoHpqxMSvcfn_pnNBYDlUCK8VugAXwRWgKq1ljDWnyd0tan-08chewjJg=w1164-h873-s-no-gm?authuser=0)

This angle was already installed months ago (8 rivets) following the fuselage instruction.

The most recent firewall KAI instruction calls out the plate should face down.

So I took pain to drill out the rivets for re-install. Since the nose wheel fork is already installed, and blocks the access for getting the rivet butts out, the process took significantly longer than it should...

So what I did was remove the nuts of the two long bolts holding the bushings secure. Then it gave me access to remove the lower 2 plates holding the bushings in place, and also removed the lower half bushing.

![img](https://lh3.googleusercontent.com/pw/AP1GczOag9Eryxkw2TunWEVNLI6hC5uAR8GBkWDOn8gnrHuaxNoyXU8pdxKrJFYv9u5j7nbHgFWGF1_16mr20pfSIDXeDYdSIhj6yBmFNTllDqz3fAzHVClNrnce-np-Tt06gXxfwU8JnepV9Gc5AgwBkGxqLw=w655-h873-s-no-gm?authuser=0)

With the extra space I was able to remove the drilled-out lower rivet butts.

For the other 6 rivets, I had to do it one side at a time.  It required removing the top bushing too.

After the whole process, I flipped the plate for a test fit. And of course the holes did not line up at all.

![img](https://lh3.googleusercontent.com/pw/AP1GczNAr0XV3U-Tk3i28NzAL6gG_V8ubVDsZ6s9efBV23sKfO_DppBmaVIL97Si2Lb-wDDkHOqGMPMl5EpKxNSJFJg--AoGY3NBUBFgWj6iKHyNJU0wB12qCBZuIp6fyx64UT_mfRL8gcUrjkqo5ArQ3vijwA=w1164-h873-s-no-gm?authuser=0)
*old orientation*

![img](https://lh3.googleusercontent.com/pw/AP1GczNWdT3UuffYPIxua8hFiSlOVyK3PfIy5ZTQQFAE9oz4ud1FajX3CaTEcB7_B0AwiKJew-0bUT4o_pUfJIt2C9bulF0qUffLewMuA9tOdDXpAhxWO0tBAzFX6bByDp0TUNvsdVdoY9Ec4b5Kl9gDF1oMhg=w655-h873-s-no-gm?authuser=0)
*New orientation*

I asked Facebook builder group. It seems the orientation depends on the cowling version. 915 should use my original orientation, and 916 should use the flipped down version. Since my cowling is for 916 (even though I have 915 engine), I might have to get a new part that fits. I sent a question to the factory. Once they respond I will decide what to do.

#### Update on 12/13

Got an answer back from Sling technical. The correct orientation is to have the flat side facing down. When installing in this orientation, only 4 of the 8 holes would align. Technical said this is ok, so I will do this.

![img](https://lh3.googleusercontent.com/pw/AP1GczPJaRX6xuxEPQyA46SavMhiNXBJOksp7gVOaEf6yzVpalPWWRfGLv5oMgCkAzQuqS_fS5kej0xLl6zyo1Y5JAYliqO3Ko252HRas67TQxMsP_NRsXKwTMiQMEqg62RJMfCjcrrhJLj9ZDDz6-2C_e7y9Q=w1164-h873-s-no-gm?authuser=0)
*Only the center row of rivets will fit, which is ok per Sling Technical*

### Throttle Cable Connection

In theory, once I install the fusebox and the starter my next step is to install the throttle quadrant and bleed the brake lines.

So I started to study the throttle cable and throttle quadrant connection.

I have the cable, but it seems I'm missing the clevis part that connects the cable to the throttle quadrant.

![img](https://lh3.googleusercontent.com/pw/AP1GczNJ1b64taAWU6QCjNMRkrHxiPVSn85EisDLgvDF2fhOLwSp-ia9HBqBORC1hdx3DsKf2mubs5kKVX_E-Krh3Wk5Fa2r_Dnm94aoWV0Yqnjy0FRDYXOV3JrB-MpRNK4YMbAKimZi1x0ygpKR0jkz98cFMA=w561-h622-s-no-gm?authuser=0)

I put in SlingShot a missing part. Not sure when I will be able to get it :-/
