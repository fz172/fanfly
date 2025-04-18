---
layout: post
title: "Audio jack testing"
categories: [Fuselage, ~rear_fuselage]
tags: [avionics, audio_jacks, ground_loop]
minutes: 120
---

# TLDR

- Conducted wire-to-wire continuity test on audio jacks (still in progress)

# Detail

I'm on a business trip in Taiwan this week so I didn't have much time doing work on the airplane before the trip. I managed to find a few hours to look into the ground loop issue so I started to conduct wire to wire continuity test on the audio jacks.

In the time I had, I was able to go through about half of wires on the rear passenger audio jacks, and discovered a few issues. The process is not done yet, so I haven't decided what's the best course of action. I will continue the testing when I get back home.

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

I must do more testing here to confirm.

## GMA245 disconnected

Haven't done this part yet. I will revise this section once the testing is done.
