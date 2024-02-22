# Quirks and issues

(all of these refers to the latest 1.42 firmware, other versions may be different)

* Parameters like curves and aftertouch ("miscellaneous setup" at the "Operational Flow Chart" in the manual) are system-wide, and don't belong to a single preset, so "Preset Reset" doesn't affect them. They can't be exported by "Graphite Editor" either, but can be (not all?) by SysEx'es (see [registers.md](registers.md))

* Aftertouch value "Aft: Off" (val=172) can't be saved into NVRAM, and resets to val=144 after power cycle. Other Aftertouch values are saved OK into NVRAM, but cannot be exported to PC (even by SysEx?). I recommend setting it to val=3 (unused), and change to "Off" if needed after powering on.

* Bank change MSB/LSB: by MIDI standard, the bank only changes at the next program change, but when sending the values the device sends program# *before* bank#. So after changing bank, ENTER has to be pressed *twice* to apply the change.

* "Virtual" CCs for MMC transport specified in the manual send wrong messages (see note in [cc_table.md](cc_table.md))
