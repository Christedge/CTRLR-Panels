# CTRLR-Panels

Some quick and dirty panel hacks I use. None of them can be used to control the synth. They only can be used to visualize how a patch of the synth is constructed.

## SE-02

![](Screenshots/Roland%20SE-02%20Patch%20Visualizer.png)

### Limitations

* SysEx decoding not done yet, displayed values are often off to the actual value.
* Currently only works in case the SE-02 is operating on MIDI channel 1.

### Poly Chain mode

In Poly Chain mode, the SE-02 sends a SysEx dump automatically each time it changes a patch. It only makes sense in case one actually owns multiple SE-02. To switch it on or off:

- Hold the Exit/Comp button while powering the unit.
- Press button B/2.
- Turn the value pot to either on or off.
- Press the value pot.

### Normal mode

Thanks to information in the [electra forum](https://forum.electra.one/t/preset-roland-se-02-v2/1180/12), The panel can emit a request to the SE-02 each time it receives a program change. This way, selecting another patch at the SE-02 will automatically updates the panel so as to display the values of the currently selected patch. To do so, you need to enable that the SE-02 emits program changes. To do so:

- Hold the Exit/Comp button while powering the unit.
- Press button [1]/6 ("Send PC").
- Select USB, MID, or U-M using the value dial.
- Press the vlaue dial to confirm.
- Connect the SE-02 to the panel via the chosen MIDI port.

## Sequential

For further Sequential Synths like the Take 5 or TEO-5 head over to [synthmutt](https://github.com/synthmutt/CtrlrPanelSequential).
