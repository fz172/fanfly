---
layout: post
title: "Rebuilt battery cables, installed shunt cover"
categories: [Firewall, ~firewall_forward]
tags: [avionics, wiring, GNX375]
minutes: 120
---

## TLDR

- Rebuilt battery cables
- Installed shunt cover
- Got confused about avionics error message

## Detail

## Battery cable & Shunt cover

I decided to redo a segment of the battery cable - from master contact to the shunt.

The previous cable was working, but the way it was routed interfered with installing the shunt cover, so I made a new one.

Process was pretty straighforward:

- Rough measured  & and cut the cable length
- Crimped one side
- Bent the cable and test fitted it on the airplane
- While on the airplane, I "clocked" the other end of the cable lug, and marked the position using a sharpie.
- Crimped the other side.

![img](https://lh3.googleusercontent.com/pw/AP1GczMeBgzarXUuTzE5TBEtNMQrV3LyPOOU-MBFpZhpQbr46MQf7K2XlNtXXrU7424J6mJfVCx1nxdWBq44jJeh42J5GMWM1g4FGOG5aUQuGoVA-QhOLTorpjezsLuF02yAJ8bi2X7V41weLG0MnSnxpf9slg=w1213-h913-s-no-gm?authuser=0)

With the cable properly routed, I installed the shunt cover. The only tricky part was to identify the correct position to drill the screw holes on the shunt.

I laid a piece of paper on the airplane and poked the holes on top of the rivnuts. Then I transferred the hole position from the paper to the cover, then then drilled away.

![img](https://lh3.googleusercontent.com/pw/AP1GczPryAg28zvHr8AM9dXOw_pETQY1R3rJaVTZ8mudkPVqGSlKGkOmN5kHumadIHJkLc7jR34wOYGvkEhUXJBAlkVZVj6Yc73_XM-LC6cvtrzIKgTr7jZE4HR_tYZz-WudFnuqjf5BmxXQgN7Y5p3V2LK4qw=w1213-h913-s-no-gm?authuser=0)

## GNX375 Error message

I noticed several error messages on my GNX375 so I took a picture. I have not got a chance to debug the issue though.

![img](https://lh3.googleusercontent.com/pw/AP1GczO9ps7N3s1vmhVivm-Idb4PksTTYSYDDjh2TCHnDdgIHFji4dUK7tPkXNWsjSMFBqxASuDdynfj2c41gAGdOl1-Ax0Ur3ayjSegnrAOXK2NngYqlshSmqpo-cUDIAxZ3_7n0S_EAyI5Vq6uuTAj8uuOsQ=w1213-h913-s-no-gm?authuser=0)

1. GDU disconnected. External flight plan crossfill inoperative.
2. GPS searching sky. Ensures GPS antenna has unobstructed view of sky.
3. Transponder has failed.

I suppose the second message is expected, as I am working inside my hangar.

But I am unsure what to do with the other 2 messsages. For the first one "crossfill inoperative". I tried to crossfill flight plan from 375 to G3X and vice versa, and they seem to work. I also tried transponder code, they worked too.

And for the "Transponder has failed" code, I have no idea what it means. The transponder says " 1200 standby", and I was able to change to a different code. There are no red crosses on either G3X or GNX375..

Next time I go to the hangar I'm afraid I need to spend more time digging through the logs.
