---
layout: post
title: "High Fuel Pressure Investigation - Part 1"
categories: [Engine, ~accessary]
tags: [fuel_selector, fuel_pump, fluid_lines]
minutes: 240
---

## TLDR

- Investigaing an high fuel pressure issue

## Details

Since I connected the fuel lines, the fuel pressure read from the differential pressure sensor (UMA N1EU70D) has been higher than the "by the book" normal operation range (max 46 PSI).

When engine is off, with just one pump + aux pump it's at 47 PSI. I did a taxi test, and the relative pressure crept up to 55 PSI. I asked both Sling Technical and Midwest Panels. Steve and Adam have seen pressure going up to 50+ PSI when airplanes are on the ground, so it's not uncommon. Sling technical suspects there is a kink or some other restriction in the return lines. So to be on the safe side, I started to debug this issue.

Things I've done so far:

- Disconnected the return line from the engine, route the engine return fuel directly to a bucket.
  - Result: Engine off/single pump pressure stayed at 47 PSI.
  - Conclusion: my fuel pressure is high in the first place. However this doesn't fully rule out return line restrictions because I didn't start the engine and couldn't reproducce the 55PSI scenario during taxi.
- Connected the return lines and opened the fuel cap on both tanks.
  - Result: same pressure at 47 PSI
  - Conclusion: the vent lines are probably fine.
- Checked debris on the fuel pressure regulator
  - Result: no debris
- Checked gascolator for debris
  - Result: no debris

A few things I will need to try next week:

- Check return lines for debris and kink section by section
- Change the return lines to larger diameter rubber hoses
- Disconnect the fittings from fuel selector to check debris
- Install bypass checkvalve between the main return line and left tank return link near the fuel selector

![](https://lh3.googleusercontent.com/pw/AP1GczNq1gI3de7ossuID8E6aD0gFK-2Lcbg9zpvj2DvAbLXhEJJNJ6GLEBHr8JIxJWjvAgZI5-eq6q9IIGf8qiXAyFiJCacr0euiV6eF-LWc1F-DTLlCzfRHLG70ZzmbxHWh-vbNyhkU_rwqnucBh9wqBRajg=w3110-h2332-s-no-gm?authuser=0)
_Fuel pressure regulator no debris_

![](https://lh3.googleusercontent.com/pw/AP1GczNpsebf7vxwnTwuOsQEg9EkTjfCnujgWuLPpHIC1YCHYBSRnAVUBvNJNh23zIfB21y2AiabtuEzKfcIPHU9MafBSsa3B9CpKAJMrczWPJa0VXw_ld2kTsPQ-ychFmecCoVPyhFcj3wyuo8zOEkuFxgUhQ=w3110-h2332-s-no-gm?authuser=0)
_Fuel pressure regulator no debris_

![](https://lh3.googleusercontent.com/pw/AP1GczN0hhU_lhvyabu_UtWi8TsP3nYcs8dvePGnejlp1oD_B0n6xJAn0Sz6V8LNHWQVFkJQlIFd_sAvpqFvsNsH8InOSR7utnBPd7t0PStXDnObyfUYQpuXHXpWoGiGXf5CEh_yzylyAlwV5Oicy5piWlD63A=w1774-h2366-s-no-gm?authuser=0)
_Gascolator no debris_

![](https://lh3.googleusercontent.com/pw/AP1GczOmO0deuNpQgYVGLiRaXUtPga3R-B8sh8Fdu5stjI6FFiTjnWcgWLTo65GNJPOi9DoQ44i2ihF6UJWc-hDj3z2LZCrQc5QW1aXosV-ITuHYiUTIbaUXcEHkb7csozsXikOr_ZEOBDeizgokW8n-_QxnGA=w3110-h2332-s-no-gm?authuser=0)
_After taxi shutdown_
