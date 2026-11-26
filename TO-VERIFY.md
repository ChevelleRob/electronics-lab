# Things to verify

Facts in Electronics Lab that came from memory or general references and still
need a check against a datasheet, the textbook or real hardware. Tick an item
when it's confirmed, or tell Claude what's wrong and it will fix the tool (with
a version bump) and move the item to **Confirmed** at the bottom.

Each item says where it appears: tool → section.

## Simple Circuit

- [ ] **Conventional current history:** chosen by Benjamin Franklin, before electrons were known. *Simple Circuit → "Electron flow and conventional current" note*
- [ ] **Diode arrow:** points in the conventional-current direction. *Simple Circuit → "Electron flow and conventional current" note; quiz question 7*
- [ ] **Four parts of a circuit:** source, conductors, load, control. Is this the wording you teach? *Simple Circuit → "The four parts of a circuit" note; quiz question 3*
- [ ] **Bulb at low voltage:** current flows before the filament glows; it then glows dull red before it gets bright. *Simple Circuit → Power supply + Bulb → Try this; status pill*
- [ ] **Motor start:** a motor needs a little voltage before it starts to turn (the tool uses about 15% of its rating). *Simple Circuit → Power supply + Motor → Try this; status pill*
- [ ] **Failure points (demo values, not from a datasheet):** the bulb starts heating toward burnout above 1.25 × its rating (7.5 V for a 6 V bulb) and goes almost at once at 2 ×; the motor above 1.6 × (about 9.6 V for a 6 V motor), and smokes before it burns out. The HEAT bar reaches its damage line at those points. Do these feel right for the lab's parts? *Simple Circuit → Power supply*
- [ ] **Part currents (demo values):** 6 V bulb 0.5 A, 12 V bulb 0.25 A, 6 V motor 0.3 A, 12 V motor 0.15 A, each treated as a fixed resistance. *Simple Circuit → supply ammeter, status table*

## Rechargeable Cells

- [ ] **Per-cell voltages (nominal / full / empty / damage):** NiCd and NiMH 1.2 / 1.4 / 1.0 / 0.9 V; lead-acid 2.0 / 2.12 / 1.8 / 1.75 V; Li-ion/LiPo 3.7 / 4.2 / 3.0 / 2.5 V; LiFePO4 3.2 / 3.65 / 2.5 / 2.0 V. *Rechargeable → chemistry table, discharge graph lines*
- [ ] **Demo cells:** AA NiCd 1.0 Ah, AA NiMH 2.0 Ah, one 2 V lead-acid cell 7 Ah (six make a 12 V SLA), LiPo 2.2 Ah rated 25C, LiFePO4 3.0 Ah; max continuous discharge NiCd 10C, NiMH 5C, lead-acid 3C, LiPo 25C, LiFePO4 10C; internal resistances 20, 30, 4, 6 and 15 mΩ. *Rechargeable → chemistry note, Advanced table and stats*
- [ ] **Discharge curve shapes:** NiCd/NiMH flat then a steep drop; lead-acid slopes steadily (voltage shows state of charge); lithium gently sloping then a cliff; LiFePO4 very flat. *Rechargeable → Discharge → graph and Try this*
- [ ] **Over-discharge damage:** lithium below about 2.5 V dissolves copper and can form internal shorts later (don't recharge); lead-acid left flat sulfates; NiCd/NiMH cells get reversed in packs. *Rechargeable → Discharge → over-discharge note*
- [ ] **Lead-acid capacity at high current:** rated at the 20-hour rate (0.05C); at 1C it may give about half (Peukert's law). *Rechargeable → Discharge → C rate note (Advanced)*
- [ ] **Charging:** lithium CC/CV to 4.2 V (LiFePO4 3.65 V), stop near 5% of the starting current, usually 0.5C to 1C, never below freezing; NiCd/NiMH constant current 0.5C to 1C stopping on a −ΔV dip or temperature, or about 14 hours on a timer at 0.1C; lead-acid bulk (0.1C to 0.3C) to about 2.4 V per cell (14.4 V), absorption, then float about 2.27 V per cell (13.6 V). *Rechargeable → Charging notes and simulation*
- [ ] **LiPo temperatures:** damage and swelling from about 60 °C; a point of no return around 90 °C (it varies by cell); the anode's protective film breaks down, then the separator melts, the electrolyte makes flammable gas and the cathode can release oxygen. The simulation runs about 20× faster than real life. *Rechargeable → LiPo safety → thermometer, stages and thermal runaway note*
- [ ] **LiPo causes of swelling and fire:** too much current, short circuit, overcharge, puncture or crushing, heat (hot car), charging after over-discharge, charging below freezing. *Rechargeable → LiPo safety → scenarios*
- [ ] **LiPo handling:** balance charger, fireproof bag, never charge unattended, stay within the C rating and cutoff, store at about 3.8 V per cell, retire puffed or damaged packs. *Rechargeable → LiPo safety → safe-handling list; practice*

## Batteries & Solar

- [ ] **Cell values (typical, for the demo):** AA alkaline 2.5 Ah, about 0.15 Ω internal resistance; AA carbon-zinc 1.0 Ah, about 0.4 Ω; CR2032 lithium coin 3 V, 0.22 Ah (220 mAh), about 15 Ω; 9 V alkaline 0.55 Ah (550 mAh), about 1.7 Ω. *Batteries & Solar → Primary (amp-hours, run time, voltage sag)*
- [ ] **Primary cells can leak or burst** if recharged or forced backward by other cells. *Batteries & Solar → Primary intro and "Don't mix cells" note*
- [ ] **Coin cells** have high internal resistance and suit watches and calculators, not motors. *Batteries & Solar → Primary → Try this*
- [ ] **Solar cell voltage:** about 0.5 V working and 0.6 V with nothing connected, whatever the cell's size. *Batteries & Solar → Solar intro and notes*
- [ ] **Solar panels:** a "12 V" panel is 36 cells in series, about 18 V working and 21–22 V unloaded; rooftop panels are 60 or 72 cells, about 30–40 V; home systems string panels to about 300–600 V DC. *Batteries & Solar → Solar → "Cells, panels and arrays" note; practice*
- [ ] **Solar current values (demo):** one cell 0.5 A and one panel 6 A (about 5.5 A working) in full sun. *Batteries & Solar → Solar*
- [ ] **Shade and bypass diodes:** one shaded cell limits its whole series row; panels have bypass diodes to route around shaded groups; cold raises cell voltage a little, heat lowers it. *Batteries & Solar → Solar → "Why shade matters" note*

## Engineering Notation

- [ ] **Windows Calculator (Scientific mode):** type 4.7, **exp**, 3, **+/−** to enter 4.7E-3; **F-E** switches to E notation; there is no engineering mode. *Engineering Notation → "What does 4.7E-3 mean?" note*
- [ ] **Where each prefix is used:** petabytes in data centers; terabytes on drives, terahertz in research, teravolts and teraohms rare; gigahertz processors and Wi-Fi (2.4 GHz), gigohms on insulation testers; megohm resistors, MHz radio, megawatt power plants; kilohm resistors most common, kHz audio, kV power lines; mA through LEDs, mV from sensors, mH, ms; µF capacitors, "u" typed for µ; nF capacitors, ns in fast digital circuits; pF small ceramic capacitors; femto mostly in science labs. *Engineering Notation → Ladder → "Where you'll see each prefix"*

## Ohm's Law

- [ ] **Resistor color code:** black 0, brown 1, red 2, orange 3, yellow 4, green 5, blue 6, violet 7, gray 8, white 9; gold tolerance band = ±5%; 4-band order is digit, digit, multiplier, tolerance. *Ohm's Law → resistor picture and the OHMS stepper in the bottom bar*
- [ ] **E12 values:** 10, 12, 15, 18, 22, 27, 33, 39, 47, 56, 68, 82 in each decade (the tool uses 10 Ω to 1 MΩ). *Ohm's Law → OHMS stepper*
- [ ] **Burnout timing (demo values):** a ¼ W resistor starts being damaged above ¼ W and goes in about 6 s at twice that, almost at once far above it. *Ohm's Law → Circuit*
- [ ] **A voltmeter across an open (burned) resistor reads the full supply voltage.** *Ohm's Law → Circuit → "Too much current" note and the math box*

## Confirmed

Checked by the instructor; no action needed.

- [x] The class uses electron flow; electron flow is the true flow of DC electricity.
- [x] Lab bench supplies go to 30 V at 5 A; most experiments use 6 V or 12 V.
- [x] The class writes voltage as E (E = I × R).
- [x] Practice answers within ±5% count as right.
- [x] Engineering Notation covers peta (P) down to pico (p), with a note on where each is used.
- [x] The class uses Windows Calculator; E notation (4.7E-3) is the main way to write it.
- [x] Batteries & Solar: primary cells are alkaline, carbon-zinc and lithium coin; a 9 V battery has six cells inside (instructor's teardown); load is a resistor with a voltmeter and ammeter; solar has cell and panel zoom levels.
- [x] Ohm's Law: E stands for electromotive force; I stands for the intensity of the current.
- [x] Ohm's Law: ¼ W resistors are right for the examples (resistor wattage may become a choice in the Power tool).
- [x] Batteries & Solar: an alkaline 9 V battery holds six AAAA cells in series; some other kinds use six stacked flat cells.
- [x] Rechargeable Cells: theory only (no secondary cells in the lab); Beginner/Advanced modes; no memory effect, but a note that discharging too fast damages a battery; visual LiPo fire animation is fine.
