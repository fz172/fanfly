---
layout: post
title: "Airmaster controller, FP1 connector, and passenger door latch"
categories: [Fuselage, ~center_fuselage]
tags: [avionics, wiring, door_latch]
minutes: 360
---

## TLDR

- Installed Airmaster controller onto the panel
- Fixed and installed FP1 connector
- Rebuilt the door latch on passenger side

## Detail

### Airmaster Controller

There are 2 parts of the airmaster controller to install - the main controller box, and the fine/coarse manual adjust lever.

There are three wires that goes between the main box, the manual lever, and the harness to wire them all together.

I first took the G5 out to allow more work space, then installed the manual lever and connected wires between the manual lever and the main controller box.

As I double-checked the wiring labels, something didn't add up. On my wiring diagram I am supposed to connect ENG7B22 to power the box, and ENG8C22 as the ground for the box. Well I don't have a ENG8C22 wire. Instead, I had 2 wires eng7B22 and eng7C22. I measured the continuity for these 2 wires to airframe. Neither of them were grounded.

![img](https://lh3.googleusercontent.com/pw/AP1GczOPEynH4IT9PGDxqtzbspMrKo0u59w3xMOBx80sd3WKlhenqrwRKKEuUfeNMpQOPgUczK0ohsmmggopUo5iz0GPi0YIQf4P9fvgzypQWVoZFaTDzo8guAX1HX9vYwSvK7l0608Dqn4kWoUs87EF_622Bg=w654-h869-s-no-gm?authuser=0)

I sent an email question to MWPB, and they confirmed it's ok to run a new wire directly from the box to ground bus. It's not ideal, but simple enough. So the wiring question was solved and I fully connected all the controller stuff to the panel.

After the controller, most of the holes are filled on the panel!

![img](https://lh3.googleusercontent.com/pw/AP1GczMd2zZiCDjniL5LxLwt1K2yWhedpDr_70pOvOgF98Na6lid2t2o9Oyk64aLu96WfrWxVpnnHdlDMUG_hwhRQrwGbB7YaVt5ZGvc8oEa9mD1apxGt52EqoJd2JpCcyY3gwUdx7dtIeNqC8NnWyT49C33DA=w1154-h869-s-no-gm?authuser=0)

### FP1 Connector

Another issue is the FP1 connector. Last time when connecting the panel I noticed the female side of FP1 connector's pinout didn't match the wire diagrm. The diagram listed pins 1-15, but the connector I had came with pin 1-13, 14 empty, then 15 & 16. So at least one of the pins is incorrect.

Today I used a pin extractor to remove pin 15, 16 and checked them against the diagra. It turned out they should be in pin 14 15. So I just swapped the pins and connected the connector behind the dash.

![img](https://lh3.googleusercontent.com/pw/AP1GczMftAW854qBB9pnRYdU1hO3hiq4UhNhWTN92EWFqi5rpQM-U1R7PuMTGZef5yYvTEEeHKJL7qB7M10Poh4KEgwGIb9VnGkJt-AhIOd85tQaTYn2beKi2ep9xrOg6TxK0Sn8EIxXPglT7-pi3jcOVuyu0w=w654-h869-s-no-gm?authuser=0)

![img](https://lh3.googleusercontent.com/pw/AP1GczP1h0I1Zx-wszVp9YwYvu1VhyOH4Xs63-biYRQNadwxi24DlP0ju81ZrJsvzI_XtMRqfwUMHIlOvGBsZh1FewTO8lOSMrSN56nXOYktKTiV2Rw4td8_JH3qYL0vJalf8S-R61UzKwSNOlUoKyhwgpSHEA=w654-h869-s-no-gm?authuser=0)

### Passenger Door Latch

I wasn't happy with the latching motion on the passenger side door since I installed it last month. Today I decided to redo the latch.

I took off the rolling pin holding the lock/latch, and re-measured the position for the rolling pin. Then I drilled a new hole and put the pin back. It's abou3 millimeters next to the original position, but the locking motion is a lot smoother. Once the door is locked, there is no movement on the latch at all. This feels a lot safer than my previous installation. I used some structural epoxy to fill the original hole. I am much happier about the new installation.
