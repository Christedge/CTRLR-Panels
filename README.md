# CTRLR-Panels

Some quick and dirty panel hacks I use. None of them can be used to control the synth. They only can be used to visualize how a patch of the synth is constructed.

## SE-02

### Poly Chain mode

In Poly Chain mode, the SE-02 sends a SysEx dump automatically each time it changes a patch. To switch it on or off:

- Hold the Exit/Comp button while powering the unit.
- Press button B/2.
- Turn the value pot to either on or off.
- Press the value pot.

### Normal mode

The panel can emit a request to the SE-02 each time it receives a program change. This way, selecting another patch at the SE-02 will automatically update the panel so as to display the values of the currently selected patch. To do so, you need to enable that the SE-02 emits program changes. To do so:

- Hold the Exit/Comp button while powering the unit.
- Press button [1]/6 ("Send PC").
- Select USB, MID, or U-M using the value dial.
- Press the vlaue dial to confirm.
- Connect the SE-02 to the panel via the chosen MIDI port.
