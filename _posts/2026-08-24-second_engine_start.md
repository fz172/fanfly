---
layout: post
title: "Second Engine Start"
categories: [Engine, ~install]
tags: [engine_start]
minutes: 300
---

## TLDR

- Conducted engine leak check
- Conducted crankshaft lifter check
- Completed second engine start

## Details

### Leak Check

I took off the cowling and inspected all fuel lines and oil lines.

The oil inlet fitting connecting to the right side under the engine had a leak. I noticed one drop of oil hanging on the oil fitting.

So I gave it 1/8 quarter turn.

![](https://lh3.googleusercontent.com/pw/AP1GczNQCQtFbIbNcmUcOuOPMMNlmydJHcbOjK0hadg1v19GnQhGpL6g94-cj53kP31_YdJWG1qQB6r_KnRYPKeLpgTwtcVHaqKDt9vbDGQqBXWejZ6Adp6oIVdcIs4upQF6Tka4X-wB2K9u-eINyDdf-entBA=w3154-h2366-s-no-gm?authuser=0)

![](https://lh3.googleusercontent.com/pw/AP1GczO5O3qp-EIRHnlX5iqhVINVsw5oEz4vFcsFz0aW-iqP7DZ5T1k_mRR-p9L0vkqNF-IMvG9ySG9DPvSEjUYHbbreudCes3xiFL14JFtksQU6Ns8naPf9-gq3JZomkqq9JHJB6CDXLqFcwHYBUZBzg7_UsA=w3154-h2366-s-no-gm?authuser=0)

### Lifter Check

This one required taking the sparks off, which was a litter scary even though I have done it before.

I took the 4 spark plugs off and also took off the cylinder cover #1.

![](https://lh3.googleusercontent.com/pw/AP1GczNnv4npzXgZ_Y9DGeDM_1b_gwustTx-Fv3iLbFukQzC-L5RJfmBg8TrGvjICotY2SiCsejFJu6XS_iMHfhUxYQcFGNcBBHobrS07ZuTpEbX1Ajjbr5SMgITknhkqhJ8yOdidYc0toYPAdjW1znlpEtZEQ=w1774-h2366-s-no-gm?authuser=0)

Then I turned the propeller in the direction of its normal rotation. I stuck my pinky finger in the spark plug hole to feel the compression. At some point, the air compression against my finger stopped, and the two lifter are fully closed.

I used a hammer to push on the lifter, they were pretty solid. The test was a pass. I closed the cylinder cover and repeated the same process for the other three cylinders.

### Second Engine Run

After the lifter check, I put the cowling back and pushed the airplane out for another engine run.

I kept the engine at 2500-2700 PRM for a few minutes. Interesting, I got lane A/B lights on a few minutes into the run. I noted the issue on G3X (ignition 1/2, ignition 3/4) and shutdown the engine.

I then restarted the engine, and the error was gone. I kept the engine runnig for another minute.

After shutting down, I used the BUDS dongle to extract the logs from the ECU.

![](https://lh3.googleusercontent.com/pw/AP1GczOpBaGn3MAK4qKixVmP2lUHJ--cn9jIeiIfP_GzK66Kb1nJebp9y71FdM5yG4q88n83mxXgUn3TempSyMNWaZ4tvraSrcFCrq4TTs0_UoRVGSYAoo0vM9aPgST024AS0bBYgO-2ZWtukJXPZBM6-h71UQ=w1920-h1020-s-no-gm?authuser=0)

I also sent a question to rotax-owners.com, hopefully someone has seen this before.

- https://www.rotax-owner.com/en/915is-technical-questions/11537-both-lane-a-and-b-ignition-fault
