---
layout: post
title: "Firewall Wiring Cleanup, and Master Relay"
categories: [Firewall, ~forward]
tags: [avionics, wiring, master_relay]
minutes: 180
---

## TLDR

- Routed firewall forward wires before installing the engine
- Ran into an issue with master relay

## Details

### Wiring

Following the work from last week, I continued to route the ground wires to the single point grounding lug.

I rebuilt the regulator B grounding wire using black colored #12 tefzel cable (previously was red which could be confusing). And I also extended the battery ground wire by about 10 inches to reach the ground lug.

I bundled the two grounding wires together, and also bundled them with the sensor wires for the fuel pressure sensors. The total of ~8 wires ran from the right side of the firewall to left, with the sensor wires branching off at about the middle point. All the wires are held together with silicone tape and adel clamps so they don't move around during engine run.

![img](https://lh3.googleusercontent.com/pw/AP1GczPqosA_iZq-hBwkb5AfQievkKbMYIcyvvZp3gWl4FVIkdcwVQ7CvgAMzAhMxlYaGtrrSJ9GiVItmY2D2naGE3wyiRAkxs6GwxIedXl_QBVoKvUomBy3woUldf0sD6G6EVBIyiYTYFZ5Vfvyg5Kg1xtvPw=w2418-h1814-s-no-gm?authuser=0)

![img](https://lh3.googleusercontent.com/pw/AP1GczOSZJGhg20mDdMQC_6VYFabcuHOT0yEYBLG1aDUxNlnkENTJ-2oFuprrBTZ9Tayw0e9UMzBIrxcmTsjK5iVx6bcOumx9qQgJ8A6GcxtoBk_pMJmsNBc4yDJJSiTLeyr8rxkxC0q_PE3fYF5Re9ib31Owg=w2418-h1814-s-no-gm?authuser=0)

### Master Relay

I ran into a very frustrating issue though. After I cleaned up the wires I turned on the master switch. But to my surprise nothing happened. I could not hear the click sound that master relay usually makes.

I took a multimeter and tested the resistance between the two small terminals on the relay, and it showed 120 M omh which made no sense. I'm not electrical expert but I think this meant the coils circuit was open ie broken. I also used my power supply and gave the 2 terminals 12 volt directly, no click. So I think the relay is gone.

I bought a new one on aircraft spruce. It should come next week. I will try to bench test it and replace. We will see what happens then.
