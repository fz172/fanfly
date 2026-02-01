---
layout: page
icon: fas fa-book
order: 4
---

This is some reference/lookup charts I use throughout the build.

## Squawk issues

[Notion](https://www.notion.so/1e5f148290fe80a2bf23c3f33bdcdd68?v=1e9f148290fe80a2bc0c000c80147c8b)

## Torque

[Reference](https://www.latten.net/sling2/torque-values/)

### Metrics nuts

<https://www.fastenermart.com/files/metric_tighten_torques.pdf>

### AN nuts

| Designation | USA Size (in) | EU Size (mm) | Total torque (in.lb) | Thread Size | Wrench size (in) | AC 43.13 torque range | TAF maintenance manual | Measured friction drag torque |
| ----------- | ------------- | ------------ | -------------------- | ----------- | ---------------- | --------------------- | ---------------------- | ----------------------------- |
| AN3         | 3/16          | 4.8          | 29                   | 10-32       | 3/8              | 20-25                 | 18-24                  | 5                             |
| AN4         | 1/4           | 6.35         | 76                   | 1/4-28      | 7/16             | 50-70                 | 51-80                  | 7                             |
| AN5         | 5/16          | 7.94         | 150                  | 5/16-24     | 1/2              | 100-140               | 12                     | 12                            |
| AN6         | 3/8           | 9.53         | 159-189              | 3/8-24      | 9/16             | 160-190               | 159-189                |                               |

- AC 43.13 max torque + (measured friction drag x0.8 for torque wrench accuracy)

### Special cases

| ITEM                                                                          | TORQUE VALUE (Nm) | TORQUE VALUE (ft.lb) | NOTES                                                   |
| :---------------------------------------------------------------------------- | :---------------- | :------------------- | :------------------------------------------------------ |
| Wing mounting bolts (front) (AN7).                                            | 55                | 40.57                |                                                         |
| Wing mounting bolts (rear) (AN5).                                             | 18                | 13.28                |                                                         |
| Main spar bolts (AN4).                                                        | 7                 | 5.16                 |                                                         |
| Main landing gear mounting bolts (M10).                                       | 25                | 18.44                |                                                         |
| Propeller mounting bolts spacer to propeller hub (M8).                        | 20                | 14.75                | Airmaster AP430CTF-WWR72B propeller                     |
| Propeller mounting bolts spacer to engine flange (M8).                        | 24                | 17.70                |                                                         |
| Engine mounting bolts (suspension frame to engine mount) (M10).               | 38                | 28.023               | NOTE: 38 Nm for oiled thread. 30 Nm for greased thread. |
| Engine mount mounting bolts (securing engine mount to engine firewall) (AN5). | 16                | 11.80                |                                                         |
| Nose wheel bolts                                                              | 11.3              | 8.33                 |                                                         |
| Safety belt bolts (3 points)                                                  | 20                | 14.75                |                                                         |
| Door bolts (hinge to canopy)                                                  | 25                | 18.44                |                                                         |
| Fuel pump banjo bolts (M12)                                                   | 20.3              | 15                   |                                                         |
| Fuel pump banjo bolts (M14)                                                   | 25.8              | 19                   |                                                         |
| Master Relay mounting bolts (1/4-20)                                          | 6.2               | 4.58 (55 in-lb)      |                                                         |
| GTP59 OAT probe                                                               | 11.3              | 8.33 (100 in-lb)     |                                                         |
| Rudder middle/top bolts (AN4)                                                 | 6.2               | 4.58 (55 in-lb)      | Calculated for extended torque arm                      |
| Regulator A grounding terminal (M4)                                           | 1.2               | 0.92 (11 in-lb)      |                                                         |

## Drill size

Reference: KAI introduction chapter

| Rivet type                      | Diameter       | Drill bit hole size |
| ------------------------------- | -------------- | ------------------- |
| Dome head and Countersunk rivet | 2.4 mm (3/32”) | 2.4 mm              |
| Dome head and Countersunk rivet | 3.2 mm (1/8”)  | 3.3 mm              |
| Dome head and Countersunk rivet | 4.0 mm (5/32”) | 4.1 mm              |
| Dome head and Countersunk rivet | 4.8 mm (3/16”) | 4.9 mm              |

## Battery Lug Crimping Sizes

| Gauge | Crimper Size |
| ----- | ------------ |
| AWG2  | 35MM         |
| AWG4  | 25MM         |

## Sealants

- Loctite 222
  - Inspection panel screws, elevator trim motor installation screws.
  - Propeller extension (bolts securing propeller hub / assembly to the propeller extension).
  - VHF antenna retaining screws.
  - Instrument panel retaining screws.
  - Navigation light retaining screws.
  - Strobe light retaining screws.
  - Fuselage fairings.
  - Fuel selector valve retaining screws.

- Loctite 243
  - Autopilot aileron and elevator servo mounting screws.
  - Propeller extension (bolts securing propeller extension to engine flange).
  - Bolt securing main wheel fairing to main axle spacer.

- Loctite 557
  - Fuel hose and oil pipe fitting threads.
  - Brake line fittings.

[Reference](https://slingaircraft.com/wp-admin/admin-ajax.php?juwpfisadmin=false&action=wpfd&task=file.download&wpfd_category_id=1068&wpfd_file_id=10722&token=&preview=1)

## CAN Bus

On my harness, CAN bus always use white as High, and White/Blue as Low.

## G3X hardware

- GDU 460 screws: <https://www.mscdirect.com/product/details/01844893>
  - #6-32, 1/2"

## Important Part Numbers

Through the build I am making some mods, buying parts not included in the factory kit. And the kit comes with some pre-made parts.
| Category | Part | Description |
| :------------------ | :------------------- | :------------------------------------------------------------------ |
| Tail | Trim servo | Ray Allen T2-7A |
| | Tail light | Aveo minimax aero |
| | Nav lights | Aero Pulsar NSR |
| Wing | Pitot/AOA | Garmin GAP 26 Heated/Regulated |
| | Fuel cap | Newton Aero 200 |
| | Fuel sender | VDO 10-180 ohm |
| | Fuel sender gasket | Custom made (Garlock 3000) |
| | Fuel Pump mod | Aerospace Innovation Intelligent Fuel Boost System |
| Fuel and oil system | Fuel Manifold | Aerospace Innovation Naviflow |
| | All hoses | Aerospace Innovation LifeLine system |
| | NACA Duct connection | 3D printed parts ([ref](https://www.thingiverse.com/thing:6903645)) |
| Paint | Interior | Primer - Rustoleum self-etching |
| | | Primer - Stewart System Ekoprime |
| | | Top coat - Stewart System EkoCrylic |
| Fuselage | Static port | Vans static port |
| | Fuel Selector | FS2020 Duplex |
