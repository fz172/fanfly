---
layout: post
title: "Firewall Wiring Cleanup, and Master Relay"
categories: [Firewall, ~forward]
tags: [avionics, wiring, master_relay, sensors]
minutes: 260
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

In the meantime, removing the old one from the airplane proved to be a huge pain in the ass. I bolted it on the firewall with 2 AN4. The nuts behind the firewall was extremely inaccessible from the back of the firewall. I crawled under the cockpit and tried several times with ratcheting wrench and finally was able to grab onto the nuts so I could loosen them from the firewall forward side.  With such difficulty to remove, I highly doubt I will be able to put them back when the new relay comes. I known I certainly won't have the patience. So I decided to install two 1/4-20 rivnuts instead of using AN4s. I still have a bunch of 1/4 brass bolts left over from building ground lug. I will use the 1/4 bolts to attach the relay.

I think I learned a lesson about Murphy's law here. In the future I will think twice about serviceability before installing anything.
