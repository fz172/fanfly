---
layout: post
title: "Audio jack issues"
categories: [Fuselage, ~rear_fuselage]
tags: [avionics, audio_jacks, ground_loop]
minutes: 460
---

# TLDR

- Conducted wire-to-wire continuity test on audio jacks (still in progress)
- Fixed the wiring after the test

# Detail

I'm on a business trip in Taiwan recently so I didn't have much time doing work on the airplane before the trip. I managed to find a few hours to look into the ground loop issue so I started to conduct wire to wire continuity test on the audio jacks.

In the time I had, I was able to go through about half of wires on the rear passenger audio jacks, and discovered a few issues. The process is not done yet, so I haven't decided what's the best course of action.

I continued the testing when I got back home.

## Expected behavior

According to Midwest Panel Builders, the audio jack barrel seeks ground through GMA245R.

- When the harness is not connected to GMA245R, everything should be open. ie, barrel should have no ground to the airframe.
- When connected, it should show continuity with airframe.

## Test

According to my wire diagram, audio wires connects to GMA245R through HC connector.

So I designed my test to 3 parts:

1. HC disconnected, test continuity between audio jack and HC connector
2. GMA245 disconnected, test continuity between audio jack and GMA245 connectors
3. All connected, test continuity between audio jack and airframe.

## All connected

5 out of 8 shows ground. The ones not showing ground are

- Right passenger Mic
- Left passenger Mic
- Left passenger Headset

This is the original state from last week when the whole situation drew my attention.

## HC disconnected

No ground to airframe. This is expected, good.

Wire to wire. This is where things get interesting. I discovered 4 pins mismatch according to my wire diagram. See table below

![image](/assets/img/20250401/rear_audio_jacks.png)

I **_think_** HC pin 4 and 5 are swapped, and 7 and 8 are swapped.

MPB sent me a new set of reference to match the wire color coding on the two ends of the connector. I took apart the connectors to check. The colors are actually all matching. So it shows the connectors are fine.

I then showed a picture of the audio jack wires to MPB. They confirmed the soldered wires on the jacks are indeed incorrect. Mystery solved!!

![img](https://lh3.googleusercontent.com/pw/AP1GczMczfrCrS6z39N9so3hLPPht_vznZeQMHzMHdkC9CdSiDRCIWb37HU61I_B4D2QEcTpLDpDVIMg5VMWxNM9lT45-G8ErRDveJoYIHq5IBDh1ES660J80kPPRX_i8Q9vH5aIzUcxkyM4lr1Q3iOlhjubZg=w1284-h1712-s-no-gm?authuser=0)

## GMA245 disconnected

With HC connected but GMA disconnected, the test covers end-to-end audio jack wiring up to the GMA unit itself.

In this test, the passenger headset pins should go to J2401 connector pin #40 #41 #42. However my #41 #42 slot on the connector has no pin at all. Instead, the pins are inserted to #38 #39. I confirmed with MPB that these need to be moved.

## Test conclusion

The not-so-good news is that some wires are misconfigured.

The good news is that MPB has been very helpful with the debugging process, and now I know what to do to fix the wires. Even though this is some unanticipated work, I am feeling pretty good about the progress so far.

## Fixes

### J2401

I opened up the d-sub connector J2401, and rearranged the wires #38 #39 #40 to #40 #41 #42.

### Audio jacks

I cut the wires on both the left jacks and used crimp connector to reconnect them the correct way
* Mic: swap the two wires
* Headset: swap the ring and top wires

Then I put the jacks back to the rib and permanently secured them to the airplane.

![img](https://lh3.googleusercontent.com/pw/AP1GczO1bldFmHS2fMB8qtZzwwV-yp0lxgdEAwwY7IJY5DDuY_2BBvJndWl4BMIsfNxOxyfoPL5V3-CELN-mEZ_b3_rGiW5dAvUfA8I-xRvUk4iLekPlZ01pPbmnSkfGSrn8etDUS6LoK2eywZEF4p1sAcmliw=w2282-h1712-s-no-gm?authuser=0)