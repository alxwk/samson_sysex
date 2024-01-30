# samson_sysex

This is an attempt to reverse engineer the control protocol of a pretty old MIDI-keyboard SAMSON Graphite 49 (other models probably are similar).
The info here is for the latest available "version 1" firmware `1.42`. As there exists "version 2" too (for the units with different LCD) it can have some differences.

Files included:

* [sysex.md](sysex.md) — the main list of SysEx'es used for reading and writing settings for the device
* [hardware_ids.md](hardware_ids.md) — IDs used in the SysEx'es for addressing the device physical controls
* [cc_table.md](cc_table.md) — CC numbers used for assigning functions to conrols, standard MIDI and vendor extended "virtual CC" ones
* [registers.md](registers.md) — byte registers used for miscellaneous device-wide settings (zones setup mostly)
* [rc_presets.md](rc_presets.md) — short description of "Remote Control" presets
