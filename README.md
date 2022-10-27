# SilverShadow
Serial: V2.4400

Hardware:

- Voron 2.4R2 350mm Formbot kit
- CW2 (Clockwork 2) extruder
- Stealthburner toolhead
- E3D Revo Voron hotend
- Labist Raspberry Pi 4b with 4 GB
- BigTreeTech Octopus Pro as primary MCU
- BigTreeTech TMC5160HV stepper motor drivers
- Mellow Fly SB2040 as secondary MCU
- LDO-36STH20-1004AH pancake stepper motor for the CW2
- Moon's MS17HD6P420I stepper motors for X, Y, and Z

Mods I have applied:

- Originally added in Hartk's 2 piece Stealthburner toolhead PCB (https://github.com/hartk1213/Voron-Hardware-SBPCB/tree/master/Stealthburner_Toolhead_PCB), but I had some reliability issues with the 16 wires running to the toolhead, likely due to my own bad crimping skills
- Replaced the Hartk's PCB with a Mellow Fly SB2040 (https://mellow.klipper.cn/?spm=a2g0o.detail.1000023.17.73937885EgBMV3#/board/fly_sb2040/README?id=sb2040), which offers even more functionality, and also supports CAN Bus which only needs 4 wires running from the electronics bay to the printhead instead of the "normal" 16 wires. That equates to 75% less chances of my bad crimps being a problem ;-)
- Installed an umbilical line (https://github.com/hartk1213/MISC/tree/main/Voron%20Mods/Voron%202/2.4/CW2_SB2040_CAN_Umbilical) from the printhead to the A motor mount, for the 4 wires running to the toolhead, and allowing me to remove the X cable chain
- Configured Sensorless Homing for the X and Y axes (https://docs.vorondesign.com/community/howto/clee/sensorless_xy_homing.html), allowing me to remove the Y cable chain
- With the reduced wire count in the Z cable chain now down from 28 wires to 12 wires (4 for each of the A & B motors and 4 for the CAN Bus wires running to the toolhead), I was able to replace the larger original Z cable chain with the smaller chain from the removed X and Y cable chains.
- Relocated the Z cable chain to under the rear gantry extrusion (https://www.printables.com/model/279739-voron-can-bus-z-chain-move). Using the smaller generic cable chain in my 350mm V2 build, I needed 23 chain links plus the two end pieces with the screw holes to make this work, and allow for a 310mm Z axis travel.
- My OMRON TL-Q5MC2 inductive probe would not work reliably when the printer bed/chamber was heated up to printing temperatures, so I built and configured an UnklickyNG BFP probe (https://github.com/majarspeed/Unklicky) to replace it.
- As I'm running with sensorless homing for X and Y, I configured the UnklickyNG BFP probe to operate as my Z Endstop (https://docs.vorondesign.com/community/howto/Takuya/Klicky_Probe_AutoZ_Alternative.html), which means I no longer need the stock Z Endstop.
- Replaced the Stealthburner's original logo LED with the Rainbow Barf LED (https://github.com/tanaes/whopping_Voron_mods/tree/main/LEDs/Rainbow_Barf_Logo_LED?_ga=2.177043557.1718150233.1666884598-749777185.1666884598).
- In the first month after assembling the printer, already the floor acrylic panel was pretty badly warped, so I replaced the stock black acrylic floor and rear panels with black panels made from ACM (Aluminum Composite Material). ACM should also help retain/reflect some heat back into the chamber, which is desirable for printing with ABS.
- Installed the Decontaminator nozzle brush and purge bucket (https://github.com/VoronDesign/VoronUsers/tree/master/abandoned_mods/printer_mods/edwardyeeks/Decontaminator_Purge_Bucket_&_Nozzle_Scrubber)

Mods I still wish to apply:

- Install some LED lighting in the chamber
- Install a 48V PSU to drive the stepper motors, allowing for faster printing speeds
- Replace the clear acrylic panels and doors with ones made from polaycarbonate
- Configure and try out the Phaetus Dragon HF, and the E3D V6 hotends
