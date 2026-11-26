# Changelog

Every change gets a version bump and an entry here, newest first.
Each tool has its own version number, shown in its header bar.

## Home page (`index.html`)

- **v2.0** Added the Rechargeable Cells card (v1.0)
- **v1.9** Batteries & Solar card: v1.2; Ohm's Law card: v1.3
- **v1.8** Batteries & Solar card: v1.1 (mentions 9 V batteries); Ohm's Law card: v1.2
- **v1.7** Added the Batteries & Solar card (v1.0)
- **v1.6** Engineering Notation card: v1.1, with Beginner and Advanced in its description
- **v1.5** Added the Engineering Notation card (v1.0), before Ohm's Law
- **v1.4** Simple Circuit card: v1.3; Ohm's Law card: v1.1
- **v1.3** Added the Ohm's Law card (v1.0)
- **v1.2** Site icon in the browser tab (and on the home screen when saved), and a preview image when a link to this page is shared; cards updated to the new tool versions
- **v1.1** Simple Circuit card: v1.1
- **v1.0** First version: home page with the Simple Circuit card (v1.0)

## Rechargeable Cells (`rechargeable/`)

- **v1.0** First version, with Beginner and Advanced modes. NiCd, NiMH, lead-acid, Li-ion/LiPo and LiFePO4 with a table of nominal, full, empty and damage voltages. Discharge: cells in series, load current (amps, plus C rate in Advanced), a sped-up clock, a charge gauge, amp-hours used, a live voltage curve with empty and damage lines, a protection circuit (BMS) switch, heat and damage from too much current, and fewer amp-hours at high rates (Advanced). Charging: CC/CV for lithium, constant current with −ΔV or timer for NiCd/NiMH, bulk/absorption/float for lead-acid, on a live voltage and current graph, with too-fast warnings; Advanced adds a wrong charger setting and an unbalanced pack with and without a balance charger. LiPo safety: scenarios (normal, too much current, short circuit, overcharge, puncture, hot car; Advanced adds charging after over-discharge and below freezing), a thermometer with 60 °C damage and 90 °C point-of-no-return lines, a swelling meter, and a cell that vents and burns in thermal runaway; safe-handling list. Notes on discharging too fast and over-discharge. Practice with ±5% answers

## Batteries & Solar (`batteries-solar/`)

- **v1.2** Meter digits are dark on the light display in dark mode too (they were white and hard to read). The series, parallel and series-parallel symbols are larger, with + on each cell’s long line and − on its short line, and a sentence saying which is which
- **v1.1** 9 V battery is now a cell choice, drawn as a rectangular 9 V battery with snap terminals (replaces the Build a 9 V battery button); the Inside a 9 V battery note shows the six AAAA cells. Series, parallel and series-parallel explained as a plain list with schematic symbols instead of boxes that looked like buttons. Stepper numbers keep room for two digits (10S to 12S). The voltmeter’s black lead has a light outline so it shows in dark mode
- **v1.0** First version. Series, parallel and series-parallel (3S2P) explained, then a live pack built with SERIES and PARALLEL steppers feeding a load resistor with an ammeter in series and a voltmeter across it, with electron-flow dashes in each row. Primary cells: alkaline, carbon-zinc or lithium coin (each with its own amp-hours and internal resistance), a Build a 9 V battery button (six cells in series), pack voltage, amp-hours and run time, and tap-to-flip cells (series loses voltage; parallel becomes a short with a warning and hot cells). Solar: 0.5 V cells or 18 V (36-cell) panels, a sunlight slider, and tap-to-shade (one shaded cell holds back its whole series row). Row table, notes, Try this boxes and practice with ±5% answers

## Engineering Notation (`eng-notation/`)

- **v1.1** Beginner / Advanced switch at the top (Beginner by default, remembered on each device). Beginner covers only regular numbers and prefixes: a short prefix intro, the number shown with its prefix (4.7 mA) instead of a power of ten, a “Means” column (× 1,000) on the ladder, and practice that goes regular ↔ prefix and prefix ↔ prefix with steps named by prefix. Advanced is the v1.0 layout. Practice levels renamed Common (M, k, m, µ) and All (P to p); prefix-to-prefix problems stick to prefixes normal for the unit (no millifarads or millihertz)
- **v1.0** First version. Intro with one number written four ways (decimal, scientific, engineering, prefix), what 4.7E-3 means, and Windows Calculator tips. Move the point: the decimal point slides 3 places (or 1 for scientific) with Point buttons in the bottom bar, and the exponent, E notation and prefix update, with a note on what each move did; type your own number (0.0047, 4.7E-3, 4.7m, 47u) and pick a unit. Prefix ladder from peta to pico with the number on every rung and the 1-to-999 rung highlighted, and where each prefix is used (terabytes yes, teravolts rarely). Practice: decimal or scientific to engineering, E notation or decimal to a prefix, and prefix to prefix, at Basic (M, k, m, µ) or Full (P to p), with worked steps

## Ohm's Law (`ohms-law/`)

- **v1.3** Meter digits are dark on the light display in dark mode too (they were white and hard to read)
- **v1.2** The voltmeter’s black lead has a light outline so it shows in dark mode
- **v1.1** Replace resistor also opens the switch (as well as turning the supply back to 0 V)
- **v1.0** First version. Intro to E (voltage), I (current) and R (resistance), E = I × R, and why the letters are E and I. Circuit: 0–30 V supply, switch, ammeter in series, E12 resistor from 10 Ω to 1 MΩ with color bands (gold ±5%), voltmeter in parallel, picture and schematic, electron/conventional flow, and a live triangle with the math worked out. ¼ W resistors heat up and burn open (ammeter 0, voltmeter reads the full supply), with a HEAT bar and Replace. Triangle: tap the letter to find, enter the other two with units, get the worked steps; prefix table. Practice: find E, I or R, Basic or With prefixes, ±5% answers, worked solutions and a hint when an answer is off by 1,000

## Simple Circuit (`simple-circuit/`)

- **v1.3** Replace bulb / Replace motor also opens the switch (as well as turning the supply back to 0 V)
- **v1.2** Site icon in the browser tab (and on the home screen when saved), and a preview image when a link to this page is shared
- **v1.1** Bottom bar rearranged: battery/supply readings on the left, switch on the right. New vertical HEAT bar graph next to the readings, with a white line at the damage threshold: heat rises with voltage, reaches the line at the point where the part starts being damaged, and climbs to the top as it burns out. It replaces the heat bar in the status table
- **v1.0** First version. A 6 V battery or a 0–30 V power supply, a switch, and a bulb or a motor with a fan, rated 6 V or 12 V. Animated flow with an Electron flow / Conventional switch (electron flow by default) and a note on why electron flow is the true flow. The circuit as a picture and as a schematic; tap the switch in either to open or close it. Bulb glows from dull red to bright, motor speeds up with voltage; over the rating they heat up and burn out (filament breaks, motor smokes), which opens the circuit. Replace button puts in a new part and turns the supply back to 0 V. Status table, Try this boxes, notes on the four parts of a circuit and ratings, and a 7-question check
