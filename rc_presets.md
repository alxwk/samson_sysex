# Remote Control presets

The following 15 presets are special and denoted as "Remote Control":

| #  | Name     |
|----|----------|
| 02 | Logic\*   |
| 03 | Protools |
| 04 | Cubase   |
| 05 | Ableton\* |
| 06 | Cakewalk |
| 07 | Reason\*  |
| 08 | Traktion |
| 09 | Motu     |
| 10 | MK Ctrl\* |
| 11 | Acid Pro\*|
| 12 | Audition\*|
| 13 | FLStudio\*|
| 14 | Nuendo\*  |
| 15 | Magix\*   |
| 16 | Presonus\*|

These presets (except "03 Protools") use variants of Mackie Universal Control protocol
for interacting with various DAW software. "03 Protools" attempts to emulate older HUI protocol
which is much more complicated, so the implementation is only partial and seemingly wacky, and I have no particular intent to venture all the way to HUI yet
(Slavs will understand).
10 out of 15 presets (marked with \*) actually use *the same* variant of the protocol, and 13 of 15
use *the same* controls mapping (there *can* be some subtle differences in controls realization and feedback processing though,
otherwise all that "support of oh so many DAWs" would look like a sham).

## MCU controls

### Notes

|Note#| 02 Logic |03 Protools|04 Cubase|06 Cakewalk|08 Traktion|09 Motu |
|-----|----------|----------|----------|----------|----------|----------|
| 0   | Rec1     | Rec1     | Rec1     | Rec1     | Rec1     | Rec1     |
| 1   | Rec2     | Rec2     | Rec2     | Rec2     | Rec2     | Rec2     |
| 2   | Rec3     | Rec3     | Rec3     | Rec3     | Rec3     | Rec3     |
| 3   | Rec4     | Rec4     | Rec4     | Rec4     | Rec4     | Rec4     |
| 4   | Rec5     | Rec5     | Rec5     | Rec5     | Rec5     | Rec5     |
| 5   | Rec6     | Rec6     | Rec6     | Rec6     | Rec6     | Rec6     |
| 6   | Rec7     | Rec7     | Rec7     | Rec7     | Rec7     | Rec7     |
| 7   | Rec8     | Rec8     | Rec8     | Rec8     | Rec8     | Rec8     |
| 8   | Solo1    | Solo1    | Solo1    | Solo1    | Solo1    | Solo1    |
| 9   | Solo2    | Solo2    | Solo2    | Solo2    | Solo2    | Solo2    |
| 10  | Solo3    | Solo3    | Solo3    | Solo3    | Solo3    | Solo3    |
| 11  | Solo4    | Solo4    | Solo4    | Solo4    | Solo4    | Solo4    |
| 12  | Solo5    | Solo5    | Solo5    | Solo5    | Solo5    | Solo5    |
| 13  | Solo6    | Solo6    | Solo6    | Solo6    | Solo6    | Solo6    |
| 14  | Solo7    | Solo7    | Solo7    | Solo7    | Solo7    | Solo7    |
| 15  | Solo8    | Solo8    | Solo8    | Solo8    | Solo8    | Solo8    |
| 16  | Mute1    | Mute1    | Mute1    | Mute1    | Mute1    | Mute1    |
| 17  | Mute2    | Mute2    | Mute2    | Mute2    | Mute2    | Mute2    |
| 18  | Mute3    | Mute3    | Mute3    | Mute3    | Mute3    | Mute3    |
| 19  | Mute4    | Mute4    | Mute4    | Mute4    | Mute4    | Mute4    |
| 20  | Mute5    | Mute5    | Mute5    | Mute5    | Mute5    | Mute5    |
| 21  | Mute6    | Mute6    | Mute6    | Mute6    | Mute6    | Mute6    |
| 22  | Mute7    | Mute7    | Mute7    | Mute7    | Mute7    | Mute7    |
| 23  | Mute8    | Mute8    | Mute8    | Mute8    | Mute8    | Mute8    |
| 24  | Slct1    | Slct1    | Slct1    | Slct1    | Slct1    | Slct1    |
| 25  | Slct2    | Slct2    | Slct2    | Slct2    | Slct2    | Slct2    |
| 26  | Slct3    | Slct3    | Slct3    | Slct3    | Slct3    | Slct3    |
| 27  | Slct4    | Slct4    | Slct4    | Slct4    | Slct4    | Slct4    |
| 28  | Slct5    | Slct5    | Slct5    | Slct5    | Slct5    | Slct5    |
| 29  | Slct6    | Slct6    | Slct6    | Slct6    | Slct6    | Slct6    |
| 30  | Slct7    | Slct7    | Slct7    | Slct7    | Slct7    | Slct7    |
| 31  | Slct8    | Slct8    | Slct8    | Slct8    | Slct8    | Slct8    |
| 32  | E1down   | E1down   | E1down   | E1down   | E1down   | E1down   |
| 33  | E2down   | E2down   | E2down   | E2down   | E2down   | E2down   |
| 34  | E3down   | E3down   | E3down   | E3down   | E3down   | E3down   |
| 35  | E4down   | E4down   | E4down   | E4down   | E4down   | E4down   |
| 36  | E5down   | E5down   | E5down   | E5down   | E5down   | E5down   |
| 37  | E6down   | E6down   | E6down   | E6down   | E6down   | E6down   |
| 38  | E7down   | E7down   | E7down   | E7down   | E7down   | E7down   |
| 39  | E8down   | E8down   | E8down   | E8down   | E8down   | E8down   |
| 40  | Track    | Pan      | Track    | Track    | Pan      | Mode     |
| 41  | Send     | Plug-in  | Send     | Send     | Aux      | Send     |
| 42  | Pan      | Assign   | Pan      | Pan      | Plug-in  | Pan      |
| 43  | Plug-in  | Send     | Plug-in  | Plug-in  | Marker   | Effect   |
| 44  | Eq       | Input    | Eq       | Eq       | Page l   | None     |
| 45  | Instrum. | Output   | Dyn      | Compress | Page r   | Preset   |
| 46  | Bank-    | Meters   | Bank-    | Bank-    | Bank-    | Bank-    |
| 47  | Bank+    | Clear    | Bank+    | Bank+    | Bank+    | Bank+    |
| 48  | Channel- | Edit     | Channel- | Channel- | Channel- | Channel- |
| 49  | Channel+ | Mix      | Channel+ | Channel+ | Channel+ | Channel+ |
| 50  | Flip     | Transp.  | Flip     | Flip     | Flip     | Flip     |
| 51  | Glo.view | Mem loc  | Edit     | Edit     | Edit     | Edit     |
| 52  | Name     | Alt view | Name     | Name     | Cpu %    | Level    |
| 53  | Smpte    | Cut      | Smpte    | Smpte    | Smpte    | Time     |
| 54  | F1       | Separate | F1       | F1/cut   | Filters  | Enter    |
| 55  | F2       | Paste    | F2       | F2/copy  | M.filter | Escape   |
| 56  | F3       | Read     | F3       | F3/pas   | Mark in  | Group    |
| 57  | F4       | Write    | F4       | F4/del   | Mark out | Ungroup  |
| 58  | F5       | Touch    | F5       | F5/spa   | Cut      | Suspend  |
| 59  | F6       | Latch    | F6       | F6/alt/  | Copy     | Sequence |
| 60  | F7       | Trim     | F7       | F7/tab   | Paste    | Tracks   |
| 61  | F8       | Off      | F8       | F8/back  | Delete   | Board    |
| 62  | Mi.track | Auto     | F.bank1  | Newaudio | Fit all  | Click    |
| 63  | Inputs   | Default  | F.bank2  | Newmidi  | Zoom out | Countoff |
| 64  | A.tracks | Shift    | F.bank3  | Fittrack | Prev m.  | Overdub  |
| 65  | A.instru | Option   | F.bank4  | Fitproj  | Next m.  | Patch    |
| 66  | Aux      | Fader    | F.bank5  | Enter    | Insert   | Clear    |
| 67  | Busses   | Mute     | F.bank6  | Cancel   | Project  | Save     |
| 68  | Outputs  | Plug-in  | F.bank7  | Nextwin  | Setting  | Memory   |
| 69  | User     | Save     | F.bank8  | Closewin | Edit     | Pre/post |
| 70  | Shift    | Undo     | Undo     | M1       | Shift    | Shift    |
| 71  | Option   | V-sel    | Redo     | M2       | Addmark  | Control  |
| 72  | Control  | Ctrl     | Save     | M3       | Nudge\<  | Option   |
| 73  | Alt      | Alt      | Revert   | M4       | Nudge\>  | Command  |
| 74  | Read/off | Pan      | Read     | Read/off | S.meters | Read/off |
| 75  | Write    | Send     | Write    | Snapshot | S.racks  | Touch    |
| 76  | Trim     | Sendmute | Sends    | Track    | S.fliter | Trim tou |
| 77  | Touch    | Esc      | Project  | Disarm   | Save     | Overwrit |
| 78  | Latch    | Enter    | Mixer    | Offset   | Undo     | Latch    |
| 79  | Group    | Insert   | Motors   | Save     | Redo     | Trim lat |
| 80  | Save     | In       | Instrum  | Aux      | Auto rec | Save     |
| 81  | Undo     | Out      | Master   | Main     | Autoplay | Audible  |
| 82  | Cancel   | Loop     | Solodef  | Undo     | Clear    | Undo     |
| 83  | Enter    | Online   | Shift    | Redo     | Freeze   | Redo     |
| 84  | Marker   | T.func   | Left     | Marker   | Loop     | Rtz      |
| 85  | Nudge    | Cue mgr  | Right    | Loop     | Punch    | Marker   |
| 86  | Cycle    | Suspend  | Cycle    | Select   | Click    | Editgrid |
| 87  | Drop     | None     | Punch    | Punch    | Snap     | Cycle    |
| 88  | Replace  | Rew      | Previous | Jogparam | Endtoend | Punch    |
| 89  | Click    | FF       | Add      | Loop     | Scroll   | Select   |
| 90  | Solo     | Stop     | Next     | Home     | Mtc chas | Solo     |
| 91  | Rew      | Play     | Rew      | Rew      | Rew      | Rew      |
| 92  | FF       | Rec      | FF       | FF       | FF       | FF       |
| 93  | Stop     |          | Stop     | Stop     | Stop     | Stop     |
| 94  | Play     |          | Play     | Play     | Play     | Play     |
| 95  | Rec      |          | Rec      | Rec      | Rec      | Rec      |
| 104 | FdrTch1  |          | FdrTch1  | FdrTch1  | FdrTch1  | FdrTch1  |
| 105 | FdrTch2  |          | FdrTch2  | FdrTch2  | FdrTch2  | FdrTch2  |
| 106 | FdrTch3  |          | FdrTch3  | FdrTch3  | FdrTch3  | FdrTch3  |
| 107 | FdrTch4  |          | FdrTch4  | FdrTch4  | FdrTch4  | FdrTch4  |
| 108 | FdrTch5  |          | FdrTch5  | FdrTch5  | FdrTch5  | FdrTch5  |
| 109 | FdrTch6  |          | FdrTch6  | FdrTch6  | FdrTch6  | FdrTch6  |
| 110 | FdrTch7  |          | FdrTch7  | FdrTch7  | FdrTch7  | FdrTch7  |
| 111 | FdrTch8  |          | FdrTch8  | FdrTch8  | FdrTch8  | FdrTch8  |
| 112 | FdrTchM  |          | FdrTchM  | FdrTchM  | FdrTchM  | FdrTchM  |

### Controllers

| CC# | Name     |
|-----|----------|
| 16  | V-pot1   |
| 17  | V-pot2   |
| 18  | V-pot3   |
| 19  | V-pot4   |
| 20  | V-pot5   |
| 21  | V-pot6   |
| 22  | V-pot7   |
| 23  | V-pot8   |

## HUI controls

[Meh, too much work. Maybe, someday...]

## Controls mapping

The controls mapping of buttons and pads (but not sliders nor encoders) can be customized
by "Setup" mode in the device. These presets also permit changing the mappings of the
CHANNEL buttons, which aren't assignable in user presets.

he defaults are as follows:

### For MCU modes

* Sliders S1..S9 send `FdrTch1`..`FdrTch2` notes at the start and the end of movement
(as they lack touch sensors), and Pitch Bend at the corresponding channel for position change.

* Encoders E1..E8 send `V-pot1`..`V-pot8` CCs as relative controls, with control value 65..127 for counterclockwise,
1..64 for clockwise, the faster the turn, the larger.

* Buttons F1..F8 are mapped to the corresponing `Solo1`..`Solo8` notes (except for "02 Logic", where they're mapped to `Rec1`..`Rec8`).
 Buttons F9..F16 are mapped to `Mute1`..`Mute8` notes. Transport buttons are mapped as the corresponding trasport notes (91..95).
BANK and CHANNEL buttons are mapped to `Bank-`/`Bank+` and `Channel-`/`Channel+` notes.

### For the HUI "03 Protools" mode

* Sliders and encoders send HUI touch/move/release messages, like in MCU modes. Those are more complex though,
google for docs for HUI controls for details. S9 is funny, as it sends touch/release messages, but *not* the movement (as HUI has only 8 sliders).

* Buttons F1..F8, F9..F16, and transport are mapped to the corresponding Solo, Mute and transport controls (I won't get into zone/port mess here).
BANK and CHANNEL buttons are mapped to `Out`/`Online` and `In`/`Loop` correspondingly.
