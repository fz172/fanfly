---
layout: post
title: "Engine Harness - Part 4 - Continue with Wiring Investigation"
categories: [Engine, ~harness]
tags: [avionics, ecu, fusebox]
minutes: 600
---

## TLDR

- Continued to investigate the ECU issue

## Details

### Fuses and Power Wires

So continuing the investigation on my ECU issue, I have been in touch with MWPB, and they suggested to check a bunch of things on my harness.

In no particular orders, I checked the following over a few days of work:

- Disconnect the starter relay, and turn the ignition key
  - No change in engine instruments, still all red-x.
- Opened the Rotax fusebox, and checked the fuses
  - 3 fuses were blown!! 35A, and two 7.5A fuses.
- Check the wiring on the connector that supplies power to the Rotax fusebox (ie. RE1 connect)
  - continuity test between pin 1&56, 1&7, 2&6, 2&7. Since 1 is supposed to be power and 5 is ground, I expected 1 & 6 have contunuity and 2&7 have continuity. However my test result was 1&7/2&6 have continuity.
  - Under advice from MWPB, I also tested the load between 1&5 using a incandesent light. It lit up. So there is load between 1 & 5.
  - Also tested voltage between 1 & 5. It shows -12V.

So a lot of signs pointed to that my RE1 1 & 5 were swapped. I swapped them back with the help from MWPB over phone and email. Initally I tried to depin using a special tool MWPB sent me. But I was only able to remove one out of the two pins out of the connector. Eventually I gave up on that and just cut the 2 wires, and reconnected them in the right order using a crimp splice.

Once I did that, I did another test by turning master and EMS BKUP on. On G3X the engine instrument was still blank, but the good news was that the LED lighgts on the fusebox all lit up, and the lane lights looked much more normal. It turned on for 5 seconds then went off. From what I read online this is the expeced behavior for Rtoax ECU start-up.

![img](https://lh3.googleusercontent.com/pw/AP1GczOeYJazMvo2HKkm1XgduI-7gj3aKdXJli1Obs6amOyihwasf4oEDaTGdHw89AQb5uCoWh_QymFrP3vPP598hkU9Z5jELmcGAgfNsupylv37OblYI86dWCS3zc0wsxtE0DwSBKCwOQCztgnlLkxv86ZKUg=w1229-h922-s-no-gm?authuser=0)
_Blown fuses_

![img](https://lh3.googleusercontent.com/pw/AP1GczPi0Y8tChblI7BFn1dx_5ocvN5lYyZt_V5NqQicRnHTCk-sxRv9WRTCplIsIfjTOeLUET03TwHEAKBrpzRkfx-O_9EjRU3ppE9zTd9-azv2FkSMzd9GGB6P10aDx_Ae5lo6W3U7AJPmNIVxjqPLLlAiXA=w692-h922-s-no-gm?authuser=0)
_Swapping the pins on RE1_

![img](https://lh3.googleusercontent.com/pw/AP1GczPjH1j3oo3bAAfKmjpe6YBsTq8SR5mrQaLsf3737iBcGhDJ5nStSyTsCADux07eqHdyjb0P3DIe3F4aOM6mtiAk9UCh0WdH7R2bsv9aGdYc_KVMxRAHh0kvGwDFuIirNWlNMLLiokQpy9qlIBJmW2OwRQ=w692-h922-s-no-gm?authuser=0)
_Crimped the wires in the correct order_

![img](https://lh3.googleusercontent.com/pw/AP1GczORn8rT_jsGdT4ZIkVb72doySCVujtcP5DJLIJVlCZHudnTAbJZbFISKQYROCHV-dFnBOjp8eVlo2BSg9pJpKJxDib3rtqRt0Lhm_V6OFidS9_lH5RaJrlCLD71K7GoYB7P-R_2SwKqv98eXvFDniGG7Q=w1229-h922-s-no-gm?authuser=0)
_LEDs in the fusebox_

![img](https://lh3.googleusercontent.com/pw/AP1GczMPZ0WEJEoepQcNoJpZ3DEeKFEl6-_yKu3809XAShLaw_lkbbn2xNB4ifiWwZHHPfsMe_zxCtZb5t1IlgTyAA27F47e9QAX5UZnLkS9tjynUfTBseSPGJHKujAwS2E3cw35LERPX2DIhviqN65cOHw1ug=w692-h922-s-no-gm?authuser=0)
_However still blank on G3X_

![img](https://lh3.googleusercontent.com/pw/AP1GczNb1Drqr78W86j_LqUNWD4NELtTK8gWQG-ajmZ0mObfSYxRBNvHIzBHBKnuZn4THcvfaBLlqxEoOsHCTYIlCp6gQ0vApfAdSUXPq0yfXCnRPxkmQKN9uYTJY8Qnc88rGxsQnLj1h-D5seGE-gcYaAcPuQ=w692-h922-s-no-gm?authuser=0)
_No CAN bus for FADEC_

### BUDS Reader Test

I connected the two maintainence ports on the ECU to my BUDS reader, then turned on the lane switches.

The BUDS software recognised my engine and showed no error. All instruments were ok on my computer.

So I think this means the ECU is working fine. And the problem is CAN wiring.

### Tracing CAN wires

TBD
