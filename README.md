# MFOS VC LFO sync mod

This is a modification for the MFOS VC LFO. It adds a sync input with which an input gate resets the LFO's triangle core to either the maximum or the minimum peak (switch selectable). This allows LFO modulation to begin in sync with e.g. the start of a note. Other outputs also are synced at either the "beginning" or the "midpoint" (in time) of the waveform.

Modification is based on Tim Parkhurst's [sync mod](https://electro-music.com/forum/post-387749.html#387749). Resistances were changed to accommodate the MFOS LFO's larger integrating capacitor, and I used J113 for the JFET instead of 2N3819. 2N5458 was also found to work, J112 did not. One resistor was made a trimmer to allow tuning the voltage to which the oscillator resets.

The sync circuit goes on an auxiliary board along with footprints for a Eurorack style power header with reversal protection diodes and bypass capacitors (which should be mounted there instead on on the MFOS board, where they are C2 and C6) and a terminal block. Wires from the terminal block connect to ±12 V and ground on the MFOS board. Wires from a 2-pin Molex connector connect to U2-A pins 1 and 2 on the MFOS board. Panel controls (SYNC IN jack and SYNC +/- switch) connect to the auxiliary board via Molex connectors.

This mod has been tested on breadboard. I have not yet built the module with the auxiliary PCB.

A Kosmo format front panel is also provided. It includes attenuator pots for the FM 1 and PWM control voltages. Width is 10 cm.

![Auxiliary PCB](Docs/MFOS_VCLFO_aux.png  "Auxiliary PCB")
![Kosmo front panel](Hardware/Panel/mfos_vclfo_panel.png  "Kosmo front panel")
