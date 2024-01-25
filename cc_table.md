The descriptions was taken literally from the manual.

The column **LSB @ read** specifies the codes returned by "Get Settings" sysex, which are different for certain CCs (see [sysex.md](sysex.md)).

**Note regarding MMC codes**: the manual specifies them from 158 for `STOP` to 170 for `MMC RESET`. Actually punching in `158` for the control on the device gives non-standard code `0` instead of `1` for `STOP`, and the others similarly are shifted by -1. So to be useful the codes need to be incremented by 1 (which is done in this table), but it makes the code for `MMC RESET` unavailable, as it overlaps with `171` for "Pitch Bend". (It's clearly a firmware bug, which was even reported to Samson's support long time ago, but got never addressed in a number of firmware updates.)

| CC  | Description                       | Type        | MSB | LSB | LSB @ read |
|-----|-----------------------------------|-------------|-----|-----|------------|
| 0   | Bank Select                       | Controller  | 00  | 00  |            |
| 1   | Modulation wheel                  | Controller  | 00  | 01  |            |
| 2   | Breath control                    | Controller  | 00  | 02  |            |
| 3   | Undefined                         | Controller  | 00  | 03  |            |
| 4   | Foot controller                   | Controller  | 00  | 04  |            |
| 5   | Portamento time                   | Controller  | 00  | 05  |            |
| 6   | Data Entry                        | Controller  | 00  | 06  |            |
| 7   | Channel Volume                    | Controller  | 00  | 07  |            |
| 8   | Balance                           | Controller  | 00  | 08  |            |
| 9   | Undefined                         | Controller  | 00  | 09  |            |
| 10  | Pan                               | Controller  | 00  | 0A  |            |
| 11  | Expression                        | Controller  | 00  | 0B  |            |
| 12  | Effect control 1                  | Controller  | 00  | 0C  |            |
| 13  | Effect control 2                  | Controller  | 00  | 0D  |            |
| 14  | Undefined                         | Controller  | 00  | 0E  |            |
| 15  | Undefined                         | Controller  | 00  | 0F  |            |
| 16  | General Purpose \#1               | Controller  | 00  | 10  |            |
| 17  | General Purpose \#2               | Controller  | 00  | 11  |            |
| 18  | General Purpose \#3               | Controller  | 00  | 12  |            |
| 19  | General Purpose \#4               | Controller  | 00  | 13  |            |
| 20  | Undefined                         | Controller  | 00  | 14  |            |
| 21  | Undefined                         | Controller  | 00  | 15  |            |
| 22  | Undefined                         | Controller  | 00  | 16  |            |
| 23  | Undefined                         | Controller  | 00  | 17  |            |
| 24  | Undefined                         | Controller  | 00  | 18  |            |
| 25  | Undefined                         | Controller  | 00  | 19  |            |
| 26  | Undefined                         | Controller  | 00  | 1A  |            |
| 27  | Undefined                         | Controller  | 00  | 1B  |            |
| 28  | Undefined                         | Controller  | 00  | 1C  |            |
| 29  | Undefined                         | Controller  | 00  | 1D  |            |
| 30  | Undefined                         | Controller  | 00  | 1E  |            |
| 31  | Undefined                         | Controller  | 00  | 1F  |            |
| 32  | Bank Select                       | Controller  | 00  | 20  |            |
| 33  | Modulation wheel                  | Controller  | 00  | 21  |            |
| 34  | Breath control                    | Controller  | 00  | 22  |            |
| 35  | Undefined                         | Controller  | 00  | 23  |            |
| 36  | Foot controller                   | Controller  | 00  | 24  |            |
| 37  | Portamento time                   | Controller  | 00  | 25  |            |
| 38  | Data entry                        | Controller  | 00  | 26  |            |
| 39  | Channel Volume                    | Controller  | 00  | 27  |            |
| 40  | Balance                           | Controller  | 00  | 28  |            |
| 41  | Undefined                         | Controller  | 00  | 29  |            |
| 42  | Pan                               | Controller  | 00  | 2A  |            |
| 43  | Expression                        | Controller  | 00  | 2B  |            |
| 44  | Effect control 1                  | Controller  | 00  | 2C  |            |
| 45  | Effect control 2                  | Controller  | 00  | 2D  |            |
| 46  | Undefined                         | Controller  | 00  | 2E  |            |
| 47  | Undefined                         | Controller  | 00  | 2F  |            |
| 48  | General Purpose \#1               | Controller  | 00  | 30  |            |
| 49  | General Purpose \#2               | Controller  | 00  | 31  |            |
| 50  | General Purpose \#3               | Controller  | 00  | 32  |            |
| 51  | General Purpose \#4               | Controller  | 00  | 33  |            |
| 52  | Undefined                         | Controller  | 00  | 34  |            |
| 53  | Undefined                         | Controller  | 00  | 35  |            |
| 54  | Undefined                         | Controller  | 00  | 36  |            |
| 55  | Undefined                         | Controller  | 00  | 37  |            |
| 56  | Undefined                         | Controller  | 00  | 38  |            |
| 57  | Undefined                         | Controller  | 00  | 39  |            |
| 58  | Undefined                         | Controller  | 00  | 3A  |            |
| 59  | Undefined                         | Controller  | 00  | 3B  |            |
| 60  | Undefined                         | Controller  | 00  | 3C  |            |
| 61  | Undefined                         | Controller  | 00  | 3D  |            |
| 62  | Undefined                         | Controller  | 00  | 3E  |            |
| 63  | Undefined                         | Controller  | 00  | 3F  |            |
| 64  | Damper pedal                      | Controller  | 00  | 40  |            |
| 65  | Portamento on/off                 | Controller  | 00  | 41  |            |
| 66  | Sostenuto on/off                  | Controller  | 00  | 42  |            |
| 67  | Soft pedal on/off                 | Controller  | 00  | 43  |            |
| 68  | Legato Footswitch                 | Controller  | 00  | 44  |            |
| 69  | Hold 2                            | Controller  | 00  | 45  |            |
| 70  | Sound Variation                   | Controller  | 00  | 46  |            |
| 71  | Timbre/Harmonic Intens.           | Controller  | 00  | 47  |            |
| 72  | Release Time                      | Controller  | 00  | 48  |            |
| 73  | Attack Time                       | Controller  | 00  | 49  |            |
| 74  | Brightness                        | Controller  | 00  | 4A  |            |
| 75  | Decay Time                        | Controller  | 00  | 4B  |            |
| 76  | Vibrato Rate)                     | Controller  | 00  | 4C  |            |
| 77  | Vibrato Depth                     | Controller  | 00  | 4D  |            |
| 78  | Vibrato Delay                     | Controller  | 00  | 4E  |            |
| 79  | Sound Cont.                       | Controller  | 00  | 4F  |            |
| 80  | General Purpose \#5               | Controller  | 00  | 50  |            |
| 81  | General Purpose \#6               | Controller  | 00  | 51  |            |
| 82  | General Purpose \#7               | Controller  | 00  | 52  |            |
| 83  | General Purpose \#8               | Controller  | 00  | 53  |            |
| 84  | Portamento Control                | Controller  | 00  | 54  |            |
| 85  | Undefined                         | Controller  | 00  | 55  |            |
| 86  | Undefined                         | Controller  | 00  | 56  |            |
| 87  | Undefined                         | Controller  | 00  | 57  |            |
| 88  | Undefined                         | Controller  | 00  | 58  |            |
| 89  | Undefined                         | Controller  | 00  | 59  |            |
| 90  | Undefined                         | Controller  | 00  | 5A  |            |
| 91  | Reverb Send Level                 | Controller  | 00  | 5B  |            |
| 92  | Tremolo Depth                     | Controller  | 00  | 5C  |            |
| 93  | Chorus Send Level                 | Controller  | 00  | 5D  |            |
| 94  | Celeste/Detune Depth              | Controller  | 00  | 5E  |            |
| 95  | Phaser Depth                      | Controller  | 00  | 5F  |            |
| 96  | Data entry +1                     | Controller  | 00  | 60  |            |
| 97  | Data entry -1                     | Controller  | 00  | 61  |            |
| 98  | NRPN LSB                          | Controller  | 00  | 62  |            |
| 99  | NRPN MSB                          | Controller  | 00  | 63  |            |
| 100 | RPN LSB                           | Controller  | 00  | 64  |            |
| 101 | RPN MSB                           | Controller  | 00  | 65  |            |
| 102 | Undefined                         | Controller  | 00  | 66  |            |
| 103 | Undefined                         | Controller  | 00  | 67  |            |
| 104 | Undefined                         | Controller  | 00  | 68  |            |
| 105 | Undefined                         | Controller  | 00  | 69  |            |
| 106 | Undefined                         | Controller  | 00  | 6A  |            |
| 107 | Undefined                         | Controller  | 00  | 6B  |            |
| 108 | Undefined                         | Controller  | 00  | 6C  |            |
| 109 | Undefined                         | Controller  | 00  | 6D  |            |
| 110 | Undefined                         | Controller  | 00  | 6E  |            |
| 111 | Undefined                         | Controller  | 00  | 6F  |            |
| 112 | Undefined                         | Controller  | 00  | 70  |            |
| 113 | Undefined                         | Controller  | 00  | 71  |            |
| 114 | Undefined                         | Controller  | 00  | 72  |            |
| 115 | Undefined                         | Controller  | 00  | 73  |            |
| 116 | Undefined                         | Controller  | 00  | 74  |            |
| 117 | Undefined                         | Controller  | 00  | 75  |            |
| 118 | Undefined                         | Controller  | 00  | 76  |            |
| 119 | Undefined                         | Controller  | 00  | 77  |            |
| 120 | All Sound Off                     | Controller  | 00  | 78  |            |
| 121 | Reset All Controllers             | Controller  | 00  | 79  |            |
| 122 | Local control on/off              | Controller  | 00  | 7A  |            |
| 123 | All notes off                     | Controller  | 00  | 7B  |            |
| 124 | Omni mode off                     | Controller  | 00  | 7C  |            |
| 125 | Omni mode on                      | Controller  | 00  | 7D  |            |
| 126 | Poly mode off                     | Controller  | 00  | 7E  |            |
| 127 | Poly mode on                      | Controller  | 00  | 7F  |            |
| 128 | Pitch Bend Sensitivity            | RPN         | 01  | 00  | 01         |
| 129 | Fine Tuning                       | RPN         | 01  | 01  | 02         |
| 130 | Coarse Tuning                     | RPN         | 01  | 02  | 03         |
| 131 | Vibrato Rate                      | NRPN        | 01  | 03  | 04         |
| 132 | Vibrato Depth                     | NRPN        | 01  | 04  | 05         |
| 133 | Vibrato Delay                     | NRPN        | 01  | 05  | 06         |
| 134 | Low Pass Filter Cutoff Frequency  | NRPN        | 01  | 06  | 07         |
| 135 | Low Pass Filter Resonance         | NRPN        | 01  | 07  | 08         |
| 136 | High Pass Filter Cutoff Frequency | NRPN        | 01  | 08  | 09         |
| 137 | EQ Low Gain                       | NRPN        | 01  | 09  | 0A         |
| 138 | EQ High Gain                      | NRPN        | 01  | 0A  | 0B         |
| 139 | EQ Low Frequency                  | NRPN        | 01  | 0B  | 0C         |
| 140 | EQ High Frequency                 | NRPN        | 01  | 0C  | 0D         |
| 141 | EG Attack Time                    | NRPN        | 01  | 0D  | 0E         |
| 142 | EG Decay Time                     | NRPN        | 01  | 0E  | 0F         |
| 143 | EG Release Time                   | NRPN        | 01  | 0F  | 10         |
| 144 | Channel Pressure                  | After Touch | 01  | 10  | 11         |
| 145 | Program Change                    | Others 0xCn | 01  | 11  | 12         |
| 146 | Song Select(Song \#)              | Others 0xF3 | 01  | 12  | 13         |
| 147 | Tune request                      | Others 0xF6 | 01  | 13  | 14         |
| 148 | Start                             | Others 0xFA | 01  | 14  | 15         |
| 149 | Continue                          | Others 0xFB | 01  | 15  | 16         |
| 150 | Stop                              | Others      | 01  | 16  | 17         |
| 151 | System Reset                      | Others      | 01  | 17  | 18         |
| 152 | Master Volume                     | SysE        | 01  | 18  | 19         |
| 153 | Master Balance                    | SysE        | 01  | 19  | 1A         |
| 154 | GM ON                             | SysE        | 01  | 1A  | 1B         |
| 155 | XG ON                             | SysE        | 01  | 1B  | 1C         |
| 156 | GS ON                             | SysE        | 01  | 1C  | 1D         |
| 157 | GM2 ON                            | SysE        | 01  | 1D  | 1E         |
|*159*| Stop                              | MMC         | 01  | 1F  | 20         |
|*160*| PLAY                              | MMC         | 01  | 20  | 21         |
|*161*| DEFERRED PLAY                     | MMC         | 01  | 21  | 22         |
|*162*| FORWARD                           | MMC         | 01  | 22  | 23         |
|*163*| REWIND                            | MMC         | 01  | 23  | 24         |
|*164*| RECORD STROBE                     | MMC         | 01  | 24  | 25         |
|*165*| RECORD EXIT                       | MMC         | 01  | 25  | 26         |
|*166*| RECORD PAUSE                      | MMC         | 01  | 26  | 27         |
|*167*| PAUSE                             | MMC         | 01  | 27  | 28         |
|*168*| EJECT                             | MMC         | 01  | 28  | 29         |
|*169*| CHASE                             | MMC         | 01  | 29  | 2A         |
|*170*| COMMAND ERROR RESET               | MMC         | 01  | 2A  | 2B         |
|~~170~~| ~~MMC RESET~~                     | MMC         |     |     |            |
| 171 | Pitch Bend                        | Pitch Bend  | 01  | 2B  | 2C         |
