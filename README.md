# SilverShadow

Serial: V2.4400
Voron 2.4R2 350mm from a Formbot kit
Clockwork 2 extruder
Stealthburner toolhead
E3D Revo Voron hotend

Mods I have applied:

- Originally added in Hartk's 2 piece Stealthburner toolhead PCB, but I had some reliability issues with the 16 wires running to the toolhead, likely due to my own bad crimping skills
- Replaced the Hartk's PCB with a Mellow Fly SB2040, which offers even more functionality, and also supports CAN Bus which only needs 4 wires running from the electronics bay to the printhead instead of the "normal" 16 wires. 75% less chances of my bad crimps being a problem
- Installed an umbilical line from the printhead to the A motor mount, for the 4 wires running to the toolhead, and allowing me to remove the X cable chain
- Configured Sensorless Homing for the X and Y axes, allowing me to remove the Y cable chain
- With the reduced wire count in the Z cable chain now down to 12 wires (4 for each of the A & B motors and 4 for the CAN Bus wires running to the toolhead), I was able to replace the larger original Z cable chain with the smaller chain from the removed X and Y cable chains.
- Relocated the Z cable chain to under the rear gantry extrusion (https://www.printables.com/model/279739-voron-can-bus-z-chain-move). Using the smaller generic cable chain in my 350mm V2 build, I needed 23 chain links plus the two end pieces with the screw holes to make this work, and allow for a 310mm Z axis travel.
- My OMRON TL-Q5MC2 inductive probe would not work reliably when the printer bed/chamber was heated up to printing temperatures, so I built and configured an UnklickyNG BFP probe to replace it.
- Per clee's recommendation, as I'm running with sensorless homing for X and Y, I configured the UnklickyNG BFP probe to operate as my Z Endstop.
- Replaced the Stealthburner's original logo LED with the Rainbow Barf LED.
