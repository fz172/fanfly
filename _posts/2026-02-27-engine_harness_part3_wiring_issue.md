---
layout: post
title: "Engine Harness - Part 3 - Wiring Issue"
categories: [Engine, ~harness]
tags: [avionics, ecu, fusebox]
minutes: 360
---

## TLDR

- Ran into a issue with ECU power, tracing wires

## Details

Last couple of days, I fully connected the engine harness to the fusebox and ECU. And I tried to power up the ECU. But it didn't work. I spent a lot of time tracing the wires.

When I turn on the EMS BKUP switch, the LED on the switch turns on with or without switching the lane lights, but the ECU doesn't power up. I checked the lights on the Rotax fusebox, none of them lit up.

![img](https://lh3.googleusercontent.com/pw/AP1GczOjkts-_hbtWfV0BGQuvkII6X0nxHvERkzKuzgQJl37JHtpL91Rc27RppSDVC4Al0lFsFF9RQ7QS5_c724cq5GZQ16sT8cbexmMuN_zi8eWGf-NPknKrgEJ4SQw7E2adBJeIlY6YegaBER10_wAshzZzA=w1229-h922-s-no-gm?authuser=0)

![img](https://lh3.googleusercontent.com/pw/AP1GczPXkO8APpQH-Vq69xAJa76f8VMZR157QOnrzdlLtoLDm-Ly7qgjg9BOdsGAFQvF9h8oJyynlxF1Vy9vZWlF8jr_H4oZi0x_cYGTwb5GDXpnfYDoRpki_qXOlmtkYov0ukLWNxrary05OfV4uJbqYd-BUQ=w1229-h922-s-no-gm?authuser=0)

![img](https://lh3.googleusercontent.com/pw/AP1GczOddYX8YYXwMd6He7H2OKNsH5VzjjdLU-2qG_ldQG9QYeZSb4SeWccbYFJmSR1empdB3dtZ9tthu4Dp3ZMGROd1Wk_uiH8Yp3uEBTPDfFnjDdfOSm6jXorXAtOr-oPmUzQFPvVSeIjf78T5BkTl11C2wQ=w1229-h922-s-no-gm?authuser=0)

![img](https://lh3.googleusercontent.com/pw/AP1GczME6AU6zTnUQ9tRcOc59JdK52hdZuq8aXEinbvDWkIXtI9widLcUGx3B7ydU1FnU2kEPIIA9F5lfP7M56NxPhtOrmaXy4V5vGBI-g-bslFWCXrAi7EkqTS_uIw5dS8ptO137i2iRg3I6cb18-fmgP3ROA=w1480-h833-s-no-gm?authuser=0)

Things I have tried so far:

1. EMS BKUP off, starting cable disconnected, turn the ignition switch.
   - No luck
2. Add a incandenscent light between RE1 pin 1 and 5 (they are the power/ground pins sending power to the fusebox when EMS BKUP is on)
   - Light turns on.
   - This means RE1 pin 1 and 5 have a closed circuit.
3. Connected the ECU reader to my laptop.
   - No data at all.

I'm in an email thread with Midwest Panel Builders to debug the wiring issue. Needless to say, this has been a very frustrating process. I just want to see my engine ECU turn on since it's such a critical (and very expensive) part of the airplane.
