---
layout: post
title: "Lots of things before putting on dashboard"
categories: [Fuselage, ~center_fuselage]
tags: [avionics, wiring, cabin_heater]
minutes: 480
---

# TLDR

- Did a lot of misc work before putting on the dashboard
  - Upgraded some bolts and nuts for connectors
  - Built cabin heater wire connector
  - Routed and connected cabin heater tension cable
  - Installed cabin heat duct for rear seats
  - Crimped GNX GPS connector
  - Tightened fuel lines after firewall
  - Tightened brake lines after firewall
  - Installed some firewall forward components (fusebox, master relay)
  

# Details

Today was a long day. I spent the full 12 hours in the hangar working on several items on the firewall, under dashboard, and the tail section. I will break the work on the tail section into a separate log entry.

## Upgrading RE1/RE2 connector screws

Last week when installing the RE1/RE2 CPC connectors to the firewall I used M5 self-tapping screws. They are honestly probably fine. But thinking that they are hard to access, and over time the airplane will have a lot of vibration, I decided to upgrade them to M4 screws and self-locking nuts. I then torque striped them to make it easier for future inspection.

![img](https://lh3.googleusercontent.com/pw/AP1GczMa5dRkqoAm99w4e2A3ViQ9CqqYVoQsQ232bKwS7aT35VwN3_K5_FAobDRWpLepYZFRknjxUhED6-zhR_s-g0aVF5bgwikDiwMB9djIl5nxfjPz-KMBfIXnrlfYmumXG6B9DMe6lpFTog3UDW21pcPBGA=w2274-h1712-s-no-gm?authuser=0)

## Cabin heater stuff

Since the cabin heater tension cables and electric wires are both under the dash and go all the way to firewall, I wanted to full finish the cabin heater installation before putting the dashboard on. But to determine how to route the wires, I need to dashboard and panel. 

So I temporarily fitting the panel to get an accurate routing plane for the cabin heater wires.

### Valve tension cable

For the tension cable, I ran it from the center of dashboard, all the way to the pilot side, then to the back sitting on top of the naca duct then to the right reaching the cabin heater. This way the entire cable is relaxed, doesn't touch anything, and doesn't need to be cut short. 

It took me a minute to figure out how to secure the cable onto the cabin heater. Turns out there is a metal clip thingy next to the heat air valve. I pretty much just followed the sling official build video from Evan to adjust the cable. Then clipped it to its final position.

![img](https://lh3.googleusercontent.com/pw/AP1GczPyFs0gVX1sOI-z_czHmNOR-FutYn0Q-Nc9SrDgMj4t_kEzURvzxH0imsmn9pqzo8Beyaz-H4D7tB7yOQ1sNVTX9TGJf5RgdlJPlwQ1rh9lnvw-YQUtXUGxY4LXlb_p3K0JN7r1GZJDUcgC1wODSa9JOw=w1290-h1712-s-no-gm?authuser=0)

![img](https://lh3.googleusercontent.com/pw/AP1GczMGRkAvdDXOkEIJA_pgF8zF7WRRoM7IN4_Q68yqSYNbrORkekMU_8S1Khmy5nPGK5KJe5Leyk29widAMyudpCmRsvA5X16caVLFB2VPNvAYSG-ZGwsKQi7nSPBTpZMf1ZKYjayuefwLyGMduWTYrYXn7g=w1290-h1712-s-no-gm?authuser=0)

### Air ducts

To run the duct to the rear, the center channel was too small for 2 inch ducts. So I splitted the 2 inch duct into 2x one inch ducts to reach the back. I tried to find the proper 2-to-1 splitter but couldn't find any. So I just 3D printed a set.

![img](https://lh3.googleusercontent.com/pw/AP1GczOh9fBozCTuIvoT0NRcE8xSkpDmWD35bBoZu94OQ6Dy9dqKZzCboo_gLSq9enCCw7gZ28mV-BMyTTJZtPNokppf86V9QSXNtqb5H-JWIfRsF-NCnoQYpKHE_irSP3M35IvPMNZ6txTaSnFlwnaHpxBbNw=w1290-h1712-s-no-gm?authuser=0)

![img](https://lh3.googleusercontent.com/pw/AP1GczNcQKI1G1qSk5Qvz14o9pbxfbF4LTvrntgXH5X7SC074kiQwYP7IV1jqkepWWSvXLdu1bJEoJMfNMGBWkj3wDp6g40xv0gKCsBl_K4NklbF_BeR6biaK_XephdzCw-mrDefa9t3w6kElfISsKiAAlahTA=w1290-h1712-s-no-gm?authuser=0)

![img](https://lh3.googleusercontent.com/pw/AP1GczNbbVJgH08N4XWDG65Tu2aYso46oW84hTcodw2EqBfX8Iqq_rA_GGLuwtX16Hl28r6QtHJeXbyFxLblvUyE3d80Ke7hwrRqV5Nu4svC9P5ptrPabD07kkrhaTwsEMmr4r0BB9MKySyr9AzHaxZCY7qRdQ=w1290-h1712-s-no-gm?authuser=0)


### Power wires

The cabin heater needed 4 wires: power, high, med, low signal. And the heater is grounded to the air frame so I guess technically 5 wires.

I took the turn switch off the panel, and built 4 spade connectors for the switch. It's been a while since I crimped connectors so it was a little slow. But in the end I managed to crimp all 4 connectors.

I plugged them on the switch and connected the power wire to a portable power generator to do a quick test. It ran! Cabin heater work all done!

![img](https://lh3.googleusercontent.com/pw/AP1GczN7SG9UQRj9_sy0PdAZmNxrHdod1NWN67FCGKpvXLSYBdkOXofQWPTS0S9z184mGyWN_JGtAobT3rAAL_v6VPgAGbVUCRDNj7IqeXybCGGsM6MYzp_tVQIfxaY_EeN4LDVswE_n3mPGe6QaFbvZtlZdTw=w1290-h1712-s-no-gm?authuser=0)

![img](https://lh3.googleusercontent.com/pw/AP1GczPUttBXgZeB55KJ2PKtCSAhe_LoD_6Wrv1Ddk8KwnRJg5mO9Ex-EvJfJc23Y1mhKkZ3uO0OdrLdW7inja6H3dt4Yvxe-hzvNXVSQcts_yyMKG4cw51NYSLQ_ROswhDeLjil6X0vevxnr2jDj_a6H8F74w=w1290-h1712-s-no-gm?authuser=0)

{% youtube 5S5CJ7Ma1EQ %}

## Firewall forward stuff

I also installed the fusebox and the master relay (master solenoid?) as I am pretty close to power on the entire panel.

To install these things, I needed to first remove the fire proof material from the firewall. It was just glued on the firewall using some kind of double sided adhesive. But it was surprisingly difficult to remove! I must have spent over an hour to remove just the small patches for the fusebox and the master relay. And funny thing is, I ran out o AN4-5 bolts for the master relay, so I couldn't full finish the install there. I ordered some more bolts from spruce. But it's ok though, plenty of other work to do :)

![img](https://lh3.googleusercontent.com/pw/AP1GczOlEh8b5IARRh9JdwC_QSovr5fkN1Ua4zmCFESuceQ0h06NFzs0JsJ5laeCTBew42rB5EsJ6TZnqlkBfUvUPzs1Gw745ZRxGKvLzExjAmYWwKEYbuDQ9ywL9mvACMt6bnPTvGY4WRZDC6O59NkXXMlVHg=w1290-h1712-s-no-gm?authuser=0)

## Fuel and Brake lines

Lastly, I also tightened the fuel lines and brake lines behind the firewall on their 90 degree elbows.

For the fuel line, the space was really tight I couldn't really torque it down when the fuel lines were in installed on the firewall. So I just took the 90 degree elbow off the airplane and clamped it down in a vise, then torqued the AN6 fuel lines.