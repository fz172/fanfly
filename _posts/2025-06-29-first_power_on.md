---
layout: post
title: "First power on!"
categories: [Fuselage, ~center_fuselage]
tags: [avionics]
minutes: 300
---

# TLDR

- Connected the rest of wires for first power on
- Turned on power for the first time
- Debugged GMU11 Issue (to be continued)

# Detail

## Wiring

In the morning, I connected the battery ground wire from the MPB harness to the airframe. This completes all the required wiring to supply power to the panel.

Then I put the panel onto the airplane for a test run. Once the panel was on, I had to connect the CPCs between the panel and the rack. It was a minor pain, but got it done.

Then I finally was able to figure out the correct length of the G3X GPS wire. I crimped a BNC connector to it.

![img](https://lh3.googleusercontent.com/pw/AP1GczPnDau2A7AJR32_bX2sSs7IUCU2e1Dg4rdKvoSb4kxUJ1ZW-7WYmicQCkl3Wfm7F5oUaH979AMFemtzhUgDVr-nDsq_KyH9FV7LWPIGg5yb5vb1HMSUta0e1B8Pm4rqoBKIIr7G-d2_ce--MBAgGCzvXQ=w4080-h3072-s-no-gm?authuser=0)

![img](https://lh3.googleusercontent.com/pw/AP1GczNugSFs5p6rQyahrBzi1ctJ92WGbaOw9fTKLLrqLYCNiwBFdp9c2hZPHv6jp5XGZYukkpzgtlk5YgEX-o2iLEejFBMJl17-FoDUgHU099I-TfUAwAL7Y50Q0WR0chU7T3SV-U63e1-YfJM6UMFn-git5g=w4080-h3072-s-no-gm?authuser=0)


After that, I put the G5, GNX 375, G3X onto the panel one by one and connected their wires.

I am not particularly happy about the 375 wires. The 375 rack has a metal piece sticking out and touching a wire bundle. And the GPS cable for the 375 unit was bending more than what I want. Once the test run is done, I will need to figure out something to protect the wire here.

![img](https://lh3.googleusercontent.com/pw/AP1GczMZGWSY_ZPCZqtEVDyxBP7RWafmnDYFLOKOve4Jl03Px21zMXn8Iavz_AV23rg-Esuxjc8G-pZWMU40ja0K8sjN109GUnvzPYi9UOFt7aaTLh7jjiqr5dTPDB1RHoYDUHU65JXbJlyLtcKH6gC80ZfHjQ=w2328-h3092-s-no-gm?authuser=0)
_Metal rubbing wire, and GPS cable over bent_

![img](https://lh3.googleusercontent.com/pw/AP1GczMClLyIlxDpC-yX0-zBY2hvBMxR1FoHn87I-W4Ov6gh1LsAvXd5PHtxD8FQ4m14PDH-2ycCwddUjgfFiE2TQLhjnj5sS_GgfyRFpLUFXuRbMT1NubxCYoANL1SmlGKL-Ox2HFvsNB1M9rvqoO7eWVvROw=w4080-h3072-s-no-gm?authuser=0)
_All important things are connected_

## Power on test

### With backup battery

With a flip of EFIS Backup switch, the screen turned on!

![img](https://lh3.googleusercontent.com/pw/AP1GczNXZYw5Hjp6XZ0648XDtsOLmmGwBTIJLI_LRHq8zLMMzNfjlPBfGADlX1Xr93bu-Tuo6WsFMcMt4b-Wt29X5bSPCBPVYemSDwm1fkyblsflM0v2Qn4EoqrAKITtfLcM78U-rQna0G8-RKUwGw1t48DM2A=w4080-h3072-s-no-gm?authuser=0)

Lots of errors, of course! I haven't connected the engine. Neither have I calibrated anything.

![img](https://lh3.googleusercontent.com/pw/AP1GczPGrsmlBkcV095Y0V1kP5Sbc8nUgWMlBe1RFUu_EMTGYAo0nQlyY4CTfFq9YOJQ-zdlFObXp17ZKGcH1kOtPXXunFEthhDcKfPzxOFolvW37wvGb_TxbUYQc34gTtnnd-Ro2BaSwjH5LUOm6Y-kb089rA=w4080-h3072-s-no-gm?authuser=0)

### With main battery

Then I turned off the backup battery and turn on master switch.

![img](https://lh3.googleusercontent.com/pw/AP1GczOAjeMgYmZ7ThgUkIF5MSa655xpJz6DUAt_n6gJnuC8vGcCd5YK0KybzWqqvz0Tn4Klsgyf3aMod58zpqPlmEY_qupZNcLSHvJVHmTy7ImkKGqvlZLqG6lycWDpIp7xHgh9p8OH6EiitxoRQCwDzXYK-A=w4080-h3072-s-no-gm?authuser=0)

This time the G5 also turned on.

## GMU 11 Issue

During the test, master caution light turned on. The PFD has a message "Magnetometer power supply fault"

![img](https://lh3.googleusercontent.com/pw/AP1GczPMdH-WSYpF3xRlPlFhD_zaUAswGMjZV0ibtKauvHJfv6NNGYaD9p0Vd4CiWen1nTLSVOsyhFDpzchf23uPV47qkqv25Yyn80x7OYcrJ4atl4a6DLqJX6plD4JbVJCDu_GwWNXbsUtwMT5dJsIWYFa7lQ=w4080-h3072-s-no-gm?authuser=0)

This is a concern. 

I emailed MPB for their opinion. They suggested to check the ground and power on GMU 11 end, which made sense.

So I took off the DSUB connector to investigate.

![img](https://lh3.googleusercontent.com/pw/AP1GczOaEM93rZzwVsXs5ZK0XiVeHF9Pe20lct-fJe1NLGjzPvcuMTMM4Lw_pLnREKoc8DLuARRwk378RCxWj1TS9PiPGSNqc9okHd_F2T7pvNe59uHAJNkf8qu9U6NDvi-l_bhq7SYshSojeZGSurZuA5TWcQ=w2328-h3092-s-no-gm?authuser=0)

This was probably one of my first connectors. Obviously I didn't have nearly enough experience. On the first glance I didn't put any silicon wrap on the stress relief. I'm glad I took it off for debug. Otherwise I might not be able to find this out and improve. 

So I took the connector apart and checked the pins. I'm not sure what steps I was following when building this, but the pins were not really where they were supposed to be at. 

I tried to use the D-sub pin extractor tool to pull the pins out. It was a PITA and was not successful. I actually pulled a wire out and left its pin in the slot.

![img](https://lh3.googleusercontent.com/pw/AP1GczNP3zaseTqmo2xQn6-ATqW9eJ2lYshCpzkK-PivABRdn36i3qlw90XHVWUblKJLlVt8yUijhQdUzCgblY5eMlN-ip-PwCJdL2W_jHTjk3jpcaN8eh5fFZazQvFpmtsXPs_hYoy_Hbg8UPnRwURnqdAKNA=w2328-h3092-s-no-gm?authuser=0)

So I decided to just buy a new connector kit and redo the wire altogether. Order placed with spruce, I will resume this work when it arrives.