# Changelog

Every change gets a version bump and an entry here, newest first.
Each tool has its own version number, shown in its header bar.

## Home page (`index.html`)

- **v1.1** Simple Circuit card: v1.1
- **v1.0** First version: home page with the Simple Circuit card (v1.0)

## Simple Circuit (`simple-circuit/`)

- **v1.1** Bottom bar rearranged: battery/supply readings on the left, switch on the right. New vertical HEAT bar graph next to the readings, with a white line at the damage threshold: heat rises with voltage, reaches the line at the point where the part starts being damaged, and climbs to the top as it burns out. It replaces the heat bar in the status table
- **v1.0** First version. A 6 V battery or a 0–30 V power supply, a switch, and a bulb or a motor with a fan, rated 6 V or 12 V. Animated flow with an Electron flow / Conventional switch (electron flow by default) and a note on why electron flow is the true flow. The circuit as a picture and as a schematic; tap the switch in either to open or close it. Bulb glows from dull red to bright, motor speeds up with voltage; over the rating they heat up and burn out (filament breaks, motor smokes), which opens the circuit. Replace button puts in a new part and turns the supply back to 0 V. Status table, Try this boxes, notes on the four parts of a circuit and ratings, and a 7-question check
