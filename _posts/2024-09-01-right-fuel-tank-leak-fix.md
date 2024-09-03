---
layout: post
title: "Mocking left tank and filling rivets"
categories: [Wing, ~right_fuel_tank]
tags: [wing, WG-AFT-003-R-F-0, gasket_upgrade]
minutes: 180
---

# TLDR

- Conducted fuel leak test multiple times (Right tank)
- Fixed leaks (Right tank)

# Details

This is tracking a lot of small actions across a long month.

I sealed the right fuel tank at the beginning of August, and waited a week and a half to do the first round of leak test. Got a leak, tried different ways to find the leak, fixed, waited, then tested again.

## Test setup

Many people build their own manometer to test air preassure change in the tank. I hear it's more accurate but I never quite figure out how to build the jig. So I decided to go with pre-made PSI gauge.

I bought all equipments from Amazon:

- Clock with capabiilty to show temperature
- AN4 end cap
- An6 to 1/4 NPT fitting (need 2)
- Low reading pressure gauge, measing up to 3 PSI
- 1/4 NPT bike valve (need 1)
- Bike tyre pump

Set up:

- Use AN4 end cap to seal the fule overflow port
- AN6 to 1/4 NPT connect to both fuel return fitting and fuel inlet fitting
- Bike vavle to 1/4 NPT
- Pressure gauge to 1/4 NPT

Process:

- Pump air into the tank until the gauge reads 1.0 PSI
- Disconnect the pump and wait a few hours
- Pressure remain the same after it stops fluctuating in the first few minutes

## Incident before first test

When I tried to connect the gauge to fuel return fitting, it does not screw into the fitting nicely. The threads felt like it's jammed.

I asked Sling technical, and they suggested to get a new return fitting or rethread them. I don't know what rethread means so I ordered 2 new fuel return fittings (and of course they still haven't arrived when I write this blog).

I then started to research rethreading, and bought (mistakenly) an AN6 rethread die. It looks like a regular bolt, and when you thread it to the fitting it cuts away a bunch of metals from the fittings old thread and forces a clear channel for the new thread.

I tried to use it on the fuel return fitting, the die immediately jammed and required a huge force to turn. I understand how it worked but really was not comfortable turning that hard.

I returned the rethreading die resumed my research. And apparently there is something called `thread chaser`. It works in similar ways as a rethreading die, but is much less intrusive. I bought a set of thread chaser from Amazon. When it arrived, I first tried on a good AN6 fitting. The chaser die turned onto the good fitting smoothly, and did not cut anything. I was happy with the result, then I started to use it on the return fitting. It shared away so metal, and then I was finally able to install the preassure guage.

If anyone run into similar issue, DO NOT buy rethread die. Try a thread chaser first. If it doesn't work, then consider rethreading. But don't do it form the get go!

The test resumes.

## First result: leak

When I first set up the process, I only pumped to 0.5 PSI as a trail run. It's immediately clear that I have a leak. The pressure drops to 0 within 20 minutes or so.

Following what most other people do, I mixed a bottle of soapy water and sprayed to every fitting and every rivet on the tank. I could not find where the leak is.

I tried a few different ratio/mix of soap and water over 2 days period. None of them worked.

Frustrated, I bought a few new tools to help: fluresent dye, UV light and a product called snoop.

[Snoop](https://www.amazon.com/dp/B002N2T3QK) turns out to be answer. It's some kind of premade soapy water and can detect tiny holes.

I sprayed the snoop juice on the tank, and within 3 minutes I found a huge of bubble coming out of th fuel fitting.

![img](https://lh3.googleusercontent.com/pw/AP1GczMw9Z5AVnk4TSk_rPNAqpdq9AdnRwMWOVMdGChY5cTsBoVfM-TLEDm3oX37elpCLc3bz2ISTzjGxAcT_QeF-e0IJ00PcTJah9eXyqMCHro8M7HViN2kFyoFBqU6g5izsH3KuqQjmcITuy_R4iYPg4-www=w3836-h2888-s-no-gm?authuser=0)
_ Leak detected_

Looking at the fitting, I don't know what I was thinking. I did not put proseal around the washers!

Fixing the fitting is standard. I mixed a bunch of proseal and smeared it to both inside and outside of the tank, covering the washer and amost the bolt entirely.

![img](https://lh3.googleusercontent.com/pw/AP1GczO1PeIhMpDmevgexVA6UawwWeT2jwBaj_vVPjjwl6zO5b-kXDP7EPc3EnrMP5gJRPUvmXiddb6WmkzMTlg5vBzPIrje3_SNRrTwaZbkyjKmnPvmm-83qCSVmfDNVtIa6aWDBL_GBRPPhXiIYhNFZJb01A=w3836-h2888-s-no-gm?authuser=0)

## Gasket upgrade

The fixed required removing the sender cover and the gasket, so I had a chance to upgrade the gasket.

A fellow builder Greg is nice enough to manufacture 2 new gaskets using Garlock 3000 material for me. The stuff is much more durable than the cork material that came with Sling factory kit.

When I removed the old gasket, it's clearly not resuable. Many edges had already cracked, and the holes were enlarged.

![img](https://lh3.googleusercontent.com/pw/AP1GczPXLB5Z5Cr0MSKk9O1TsIj_D_cWosR2EC98gbcBoxdVqUVhEO6sxz92AGyLHQBAw4im3uiHyKzipyRwydRcv6Wr2kGg8-AAZoc5TSE58ERzl5Xx0vylDjx7xCSJiAGBEH4tB251bdJyxNeQ8lTnk1lxtg=w2174-h2888-s-no-gm?authuser=0)
_Old gasket_

![img](https://lh3.googleusercontent.com/pw/AP1GczMYIjelZzrps72KvBidDIwARyEUXCYLg0xqBKr3W1r5ki-ONQjT_mGnZQstK0Tkn52QCt6Oh1J9FL9kJORyRElgBPvf2S_m9fWQ7WHyy2W3AxVqA2s5wELCp8bUZD5aVkobgN8YQFeuAhYlavFGeaXe1Q=w2174-h2888-s-no-gm?authuser=0)
_New gasket_

## Second test

After having done all these work, I started the second round of test 2 days ago.

Friday afternoon 6:30, I pumped the air to 0.95 PSI. The gauge dropped to 0.90 within 15 minutes.

- Theory: air coming from the pump is heated so it takes a while to stablize the pressuring.

Over the next fiew hours, the pressure kept dropping. By 11:30pm, it dropped to 0.8 PSI.

- Theory: Night temperature drop significantly affected the pressure in the tank.

Next morning 7:30am, the pressure was 0.6 PSI.

- Theory: Same as above, overnight temperature and pressure fluctuation

Afternoon 6:30, the preassure came back to 0.95 PSI.

The third day, the pattern repeated and I ended the test at 7:40pm, with PSI AT 0.93 which is the same value as the day before at the same time.

![img](https://docs.google.com/spreadsheets/d/1CwRLgN0jjbZG-dR9fD5dv7syZaZwEJyF4Hcku8qmhYE/pubchart?oid=1038779643&format=image)
_Pressure change over time_

## Installing on the wing

With the results above, I concluded the tank is good.

I clecoed the tank to the wing with some help with my wife, and we riveted it on the next day.

![img](https://lh3.googleusercontent.com/pw/AP1GczNxnrg895XwLueH_r1J5PGeDN_te6cJTwcH87d7JrXefkafOSe_dzmkoyc0QJZ09kK5Sm715YDZx2jrsT3tuQ3CE6jfPSCLyqWLHPN96DKG4X023jjrvXobEVJppDS4ylGEIXsIq4lf036HAXa8HKzZHg=w1290-h1712-s-no-gm?authuser=0)
_Tank is finally on the wing!!_

I chose to use S.S. rivets near the wing root 50cm length out of precaution. This is sugggested on S.B 14 for Sling 2 but not for Tsi. I don't think it hurts though, so I just did it. I don't have duralac or
tel-gel as anti-corrosion agent on the steel rivet, so I just dabbed them in proseal. This is acceptable per the KAI.

With everything done, I moved the wing onto the rack. Time for next wing :)

![img](https://lh3.googleusercontent.com/pw/AP1GczNuRMn3nlT9i_LBCXOx8RiY2fubVnsVESYmse0jxQGJHa-0LUqQ8FlqxEehV4waMzTHv63w0LeUN5iz2FytfSPFh-AMxhLPQ-45Tx294NfK4dplXJKAN70DxWXH1aQ24AKwB79J-HakjWIECk8OEVstGg=w1290-h1712-s-no-gm?authuser=0)
_And now the wing is on a rack_

## Video

{% youtube Ib28frMpC2Y %}
