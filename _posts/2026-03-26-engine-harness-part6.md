---
layout: post
title: "Engine Harness - Part 6 - Fixing harness wires & testing "
categories: [Engine, ~harness]
tags: [avionics, ecu, wiring]
minutes: 150
---

## TLDR

- Fixed ELT wires
- Fixed fuel pressure sensor wires
- Organized some harness wires
- Tested as much harness wires as possible

## Details

I've been so excited for today, because the Midwest Panel Builders were scheduled to come to my hangar and help me debug the wires and finisht the last few bits of the engine harness installation.

We met in the morning. After a short greeting, we started working on the harness.

### ECU wires

Last time I already fixed the ECU wires, so Adam and Steve did an inspection on my installation, and verified the wiring on both the ECU and the maintainence ports are good.

### Shunt wires

Adam and Steven found that I reversed the shunt wires so the amperage on the G3X display was not correct. Steve was super quick to spot this out and swapped the two wires immediately.

### Feed fuel pressure sensor wires

I have had no idea, but apparently when I connected to the fuel pressure sensor, 2 of the wires were swapped. Steve again found this out and fixed it immediately.

### ELT and GPS Test

When then pulled the airplane out of the hangar, we tested the ELT and GPS.

For the GPS, both G3X and GNX375 are able to receive GPS signals. We then tested the ELT.

For my future reference, here is the procedure to test the ELT:

1. hold the test button for 1 second
2. Release then wait for the ELT to beep
3. 1 beep means the ELT is good
4. 2 - 6 beeps means the ELT is not good. 5 beeps is common, as it's the signal for no GPS lock.

I had 6 beeps, which means the ELT's G-meter was not connected properly. Steve and Adam disconnected the ELT from the harness, and we found that the G-meter wire was not connected at all. So we connected it properly.

Then we tested the ELT again, and this time we got 1 beep, which means the ELT is good.

### Other Testings

Adam walked through a bunch of other testings with me step by step. We tested the auto-pilot servos, and found that they were working properly. And we tested the fuel boost pump, which was also working.

By the end of the work, I felt much relieved that the calvery came and helped me debug the harness, and finally got the see things working!!

Remaining things not tested yet include the generator chariging fuel pump, and OAT . This cannot be tested until the wings are attached and engine start, which hopefully can be soon!

![img](https://lh3.googleusercontent.com/pw/AP1GczMXcybG8zTeExADnRA5zdEXi8eX55pYuqPqqe3tPuuwIWe29R2rBJ_fsVJC1VssU6Amh8Re5mMp7b1WRmus8i-JHK_xoY7VMhbPM7CuHVxHP_ot37h_aOsONHroIDxlZ8Bqv8_Q30fEA0GCK_XDHi7aFQ=w1440-h1080-s-no-gm?authuser=0)