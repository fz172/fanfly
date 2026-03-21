---
layout: post
title: "Engine Harness - Part 5 - Debugging CAN wires"
categories: [Engine, ~harness]
tags: [avionics, ecu, wiring]
minutes: 120
---

## TLDR

- Traced and fixed the CAN wires.

## Details

### Tracing CAN wires

Continuing the work from last week, I focused on the CAN wiring between the ECU and the G3X. Three sets of connectors are involved: HIC-A & HIC-B, the J244 connector on the GEA24, and a jumper connector in between.

The most probable issue was with the jumper connector, so I cut several zip-ties to reach it and disconnected it from the harness.

With the connector on the bench, it became clear that the wires were not jumped at all; it was just a pigtail. I suspect MWPB left the connector as a pigtail to provide the option to either use it as a jumper or connect it to an SCU. Since I don't have an SCU, I needed to jump the wires myself.

I used a multimeter to test the continuity of the wires between the jumper connector and the J244 pins, as well as between the jumper and the HIC-A/B pins, to understand how the wires were internally connected.

Here is what I found:

![img](https://lh3.googleusercontent.com/pw/AP1GczMG2pq1TuFz80YV2TTlsWijghhycCeiqwpyAaifVng1J5Wvd9kOg1AsQa5kTVNZ6w-37JToAf2Kradoy-MUeYFqyIcyZQT3AH455an72p10D8GSxikdExIPIQMW6v_bzZ157MKnMkKc-9t7oiY-a1_Lzg=w692-h922-s-no-gm?authuser=0)

Based on the diagram, it was clear that I needed to connect the six jumper wires into two groups:

- Pin 5+7+4
- Pin 6+8+3

I used crimp splices to connect the wires in the correct configuration.

![img](https://lh3.googleusercontent.com/pw/AP1GczNWODP7wAsDh-IsczT_5rysVurvCD41whflsdEHPzbJdHDdBHEA7x8QfTq4ZGrl2yjE8vAG9UMt_1lU56PUy5F50SxuSkRtGKnd0mMkR7SDJwnczkeaqjYwp2hVglgaqfCS5jMogw_KuOXpU5JP8tUKiw=w1229-h922-s-no-gm?authuser=0)

![img](https://lh3.googleusercontent.com/pw/AP1GczO_IX7BT5CEki_HLv34hl63tzvqcvLD2Py3tgXdAiWHS_XcBgPqlBw_dTua3mJll7y0jUuweGW2kwCFSsw783RPzUWBR8lSz7sVk6fByxyOe750zPwZB2qMODNWZgZmau0O6qVffIKLHKZi_yWC6PcFOw=w1229-h922-s-no-gm?authuser=0)

I then wrapped the connections in silicone tape for protection.

![img](https://lh3.googleusercontent.com/pw/AP1GczPgBQWdylKEuv_Wbirk-tuCA8Jy6RaIQp9138_d43IZmGrEY7GbbbK8xi8Rvs6aOAXAGNYm58vf74qi0iCc3f4REv843NHpTfh_-_d1-1IZumJf5JH29-t30Uqz0GkfpucsMmwTT9gVBsyiTOOTD5PP5w=w1229-h922-s-no-gm?authuser=0)

Afterward, I put everything back together in reverse order and turned the power back on.

![img](https://lh3.googleusercontent.com/pw/AP1GczMJx2-lAbdAkhE2SwOxyr8PO4Q6Kd-rsf1pU_sZTEgjDcltqKS7HBU5HyjpMLe9W168ixb7dEkxGrTL1n1YvDFAHmWiUC7l_20hnvMuMjjYrMHDN3xkD6hGwhYHJPNnViaIaZNZxl1PlKkQnbzL4W1XQQ=w1229-h922-s-no-gm?authuser=0)

Success! The engine instruments are now showing the correct values.
