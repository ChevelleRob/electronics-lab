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
- [ ] **Failure points (demo values, not from a datasheet):** the bulb starts heating toward burnout above 1.25 × its rating (7.5 V for a 6 V bulb) and goes almost at once at 2 ×; the motor above 1.6 × (about 9.6 V for a 6 V motor), and smokes before it burns out. Do these feel right for the lab's parts? *Simple Circuit → Power supply*
- [ ] **Part currents (demo values):** 6 V bulb 0.5 A, 12 V bulb 0.25 A, 6 V motor 0.3 A, 12 V motor 0.15 A, each treated as a fixed resistance. *Simple Circuit → supply ammeter, status table*

## Confirmed

Checked by the instructor; no action needed.

- [x] The class uses electron flow; electron flow is the true flow of DC electricity.
- [x] Lab bench supplies go to 30 V at 5 A; most experiments use 6 V or 12 V.
