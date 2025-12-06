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

### AN nuts

| Designation | USA Size (in) | EU Size (mm) | Total torque (in.lb) | Thread Size | Wrench size (in) | AC 43.13 torque range | TAF maintenance manual | Measured friction drag torque |
| ----------- | ------------- | ------------ | -------------------- | ----------- | ---------------- | --------------------- | ---------------------- | ----------------------------- |
| AN3         | 3/16          | 4.8          | 29                   | 10-32       | 3/8              | 20-25                 | 18-24                  | 5                             |
| AN4         | 1/4           | 6.35         | 76                   | 1/4-28      | 7/16             | 50-70                 | 51-80                  | 7                             |
| AN5         | 5/16          | 7.94         | 150                  | 5/16-24     | 1/2              | 100-140               | 12                     | 12                            |
| AN6         | 3/8           | 9.53         | 159-189              | 3/8-24      | 9/16             | 160-190               | 159-189                |                               |

- AC 43.13 max torque + (measured friction drag x0.8 for torque wrench accuracy)

### Metrics nuts

<https://www.fastenermart.com/files/metric_tighten_torques.pdf>

## Drill size

Reference: KAI introduction chapter

| Rivet type                      | Diameter       | Drill bit hole size |
| ------------------------------- | -------------- | ------------------- |
| Dome head and Countersunk rivet | 2.4 mm (3/32”) | 2.4 mm              |
| Dome head and Countersunk rivet | 3.2 mm (1/8”)  | 3.3 mm              |
| Dome head and Countersunk rivet | 4.0 mm (5/32”) | 4.1 mm              |
| Dome head and Countersunk rivet | 4.8 mm (3/16”) | 4.9 mm              |

## Battery Lug Crimping Sizes

| Gauge | Crimper Size   |
| ----- | -------------- |
| AWG2  | 35MM           |
| AWG4  | 25MM           |

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

## Mods

Through the build I am making some mods, buying parts not included in the factory kit. And the kit comes with some pre-made parts.

|                     | Part                   | Description                                                         |
| ------------------- | ---------------------- | ------------------------------------------------------------------- |
| Tail                | Trim servo             | Ray Allen T2-7A                                                     |
|                     | Tail light             | Aveo minimax aero                                                   |
|                     | Nav lights             | Aero Pulsar NSR                                                     |
| Wing                | Pitot/AOA              | Garmin GAP 26 Heated/Regulated                                      |
|                     | Fuel cap               | Newton Aero 200                                                     |
|                     | Fuel sender            | VDO 10-180 ohm                                                      |
|                     | Fuel sender gasket     | Custom made (Garlock 3000)                                          |
|                     | Fuel Pump mod          | Aerospace Innovation Intelligent Fuel Boost System                  |
| Fuel and oil system | Fuel Manifold          | Aerospace Innovation Naviflow                                       |
|                     | All hoses              | Aerospace Innovation LifeLine system                                |
|                     | NACA Duct connection   | 3D printed parts ([ref](https://www.thingiverse.com/thing:6903645)) |
| Paint               | Interior               | Primer - Rustoleum self-etching                                     |
|                     |                        | Primer - Stewart System Ekoprime                                    |
|                     |                        | Top coat - Stewart System EkoCrylic                                 |
| Fuselage            | Static port            | Vans static port                                                    |
| Undercarriage       | Brake                  | Matco dual piston upgrade                                           |
|                     | Grease                 | Fuchs Renolit M2 EP Grease                                          |
|                     | Brake lines            | FS Flightline PTEF upgrade                                          |
| Firewall forward    | Cabin heater lines     | Aerospace Innovation                                                |
|                     | Radiator lines         | Aerospace Innovation                                                |
|                     | Gascalator             | Andair GAS500-AN6-M-R                                               |
|                     | Gascalator drain valve | Andair DV125                                                        |

## Service Bulletin

|       | Completion date | Reference                                                   |
| ----- | --------------- | ----------------------------------------------------------- |
| SB-2  | 8/25/2024       | Not affected                                                |
| SB-14 | 10/04/2024      | [Log]({% post_url 2024-10-04-rear_fuselage_rib_assembly %}) |
| SB-15 | 8/25/2024       | Not affected                                                |
| SB-16 | 8/25/2024       | Not affected                                                |
| SB-17 | 11/10/2024      | Not affected                                                |
| SB-19 | 8/25/2024       | Not affected                                                |
| SB-21 | 11/10/2024      | Not affected                                                |
| SB-22 | 8/25/2024       | Not affected                                                |
| SB-23 | 8/25/2024       | Not affected                                                |
| SB-25 | 11/10/2024      | Not affected                                                |
| SB-26 | 01/27/2025      | [Log]({% post_url 2025-01-27-safety_belt %})                |
|       |                 |                                                             |
|       |                 |                                                             |
|       |                 |                                                             |
|       |                 |                                                             |
