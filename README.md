# CTRLR-Panels

Some quick and dirty panel hacks I use to visualize how a patch of a synth is constructed. They surely contain bugs.

## Roland SE-02

![](Screenshots/Roland%20SE-02%20Patch%20Visualizer.png)

### Limitations

Currently only works in case the SE-02 is operating on MIDI channel 1.

### Normal mode

The panel can send bank and program changes to the SE-02. When it does, it immediately requests the current patch from the synth'sedit buffer so as to visualize its values. The required SysEx request commands can be found in the [electra forum](https://forum.electra.one/t/preset-roland-se-02-v2/1180/12).

The curent patch can be re-requested manualy or requested and saved so as to create backups. For restoration, use the SysEx tool of your choice.

### Program change mode

The panel also emits a request to the SE-02 each time it receives a program change from it. This way, selecting another patch at the SE-02 using its value dial will automatically update the panel so as to display the values of the currently selected patch. For this to work, you need to enable that the SE-02 emits program changes. To do so:

- Hold the Exit/Comp button while powering the unit.
- Press button [1]/6 ("Send PC").
- Select USB, MID, or U-M using the value dial.
- Press the value dial to confirm.
- Connect the SE-02 to the panel via the chosen MIDI port.

### Poly Chain mode

In Poly Chain mode, the SE-02 sends a SysEx dump automatically each time it changes a patch. It only makes sense in case one actually owns multiple SE-02. To switch it on or off:

- Hold the Exit/Comp button while powering the unit.
- Press button B/2.
- Turn the value pot to either on or off.
- Press the value pot.

I used this method only until I found the abovementioned SysEx request commands.

## Sequential

For further Sequential Synths like the Take 5 or TEO-5 head over to [synthmutt](https://github.com/synthmutt/CtrlrPanelSequential).
