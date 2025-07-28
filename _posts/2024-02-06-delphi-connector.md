---
layout: post
title: "Wiring delphi connector for tail light"
categories: [Empennage, ~rudder]
tags: [taillight, avionics, video]
minutes: 90
mermaid: true
---

### TLDR

- Installed Delphi GT150 style connector to rudder

### Details

After watching some videos on how to install Delphi connectors, I tried to install the first one on the rudder. This will be used to connect
the tail light cable between rudder and vertical stabilizer.

The tail harness I bought from Midwest Panel comes with a female connector pre-wired, so I decided to make a male connector for my rudder. This
way I can test the connection when I'm done.

### Crimping

I cut the 4 conductors on the rudder cable to size and put 4 silicon grommet on each conductor. Then I put the male pin and crimped them using an open barrel crimper.

I did not have the proper tool to crimp the part that holds the grommet. I tried to use a larger size open barrel crimping hole. It did crimp the pin but did not give me perfect circle.

This was actually a problem. I will discuss later.

### Pinning the connector

Since this was my first GT150 connector job, it took me a while to get familiar with the tool and the process.

After crimping all 4 pins, I matched the pin layout with the female connector pins from Midwest. The wire color was all messed up but Midwest did a great job labeling the conductors. I matched the pins using 3 sources:

- The pinout from the Aveo Minimax light spec
- The pin mapping I wrote down when first connecting the light
- The wire label that came from Midwest Panel Builders.

Once I figured out which conductor goes where, I inserted them to the connector housing.

This is where I discovered my miss when crimping. I made 2 mistakes:

1. The copper was too long when I striped the cable jacket. It actually interfered the locking mechanism from the connector housing. One of the the cables would not lock. I had to wiggle it and push it really hard and it eventually locked. I re-watched a bunch of videos on Youtube, the lesson is I only need about 5mm copper when crimping it to the pin. Longer is not better.
2. The crimping on the cable grommet was not perfect circle. This caused issue when inserting it to the connector housing. The fix was simple, I reshaped them using a hand crimper. But I immediately went to Amazon and bought a crimper designed for GT150. So hopefully next time the crimping will be done better.

### Testing

Once the connector is properly pinned, I connected it to the female connector that came from Midwest Panel. It came with a pigtail so I just hooked it up to a battery to test the light. The light needs 12v or above battery, so I used 2 9Vs. The light worked in both nav mode and stroke mode. I am happy with the work. This fully concludes the work on rudder.

## Video

{% youtube bsZI_hAsbKo %}
