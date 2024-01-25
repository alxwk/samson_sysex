# Samson Graphite 49 SysEx control messages

The requests need to be sent to the virtual MIDI input port `:1` (named "In Port B" in the manual) of the device,
and the responses get received from the output port `:4` ("Out Port 5").

## Device ID

### Request

| Byte(s)  | Description            |
|----------|------------------------|
| F0       | SOX                    |
| 00 00 66 | Mackie manufacturer ID |
| 14 1a 00 | device ID request?     |
| F7       | EOX                    |

### Response

| Byte(s)                    | Description            |
|----------------------------|------------------------|
| F0                         | SOX                    |
| 00 00 66                   | Mackie manufacturer ID |
| 14 1b 58 59 5a 74 13 2c 64 | device ID answer       |
| F7                         | EOX                    |

## Getting settings

### Request

| Byte(s)       | Description                                                            |
|---------------|------------------------------------------------------------------------|
| F0            | SOX                                                                    |
| 00 20 6b      | Arturia manufacturer ID                                                |
| 02 05 *nn* 00 | request of the *nn*'th preset (0-based, `7f` means the current preset) |
| F7            | EOX                                                                    |

### Response type 1 (preset controls)

(numbers are 0-based, usual MIDI MSB/LSB 7-bit format)

| Byte(s)   | Description                               |
|-----------|-------------------------------------------|
| F0        | SOX                                       |
| *n1* *n2* | Hardware control ID (see [hardware_ids.md](hardware_ids.md)) |
| *rr* *rr* | Assigned Samson CC# (see the manual)      |
| *cc*      | Channel# (`10` means the current)         |
| *pp*      | Port# (`05` means the current)            |
| *ff*      | Flags                                     |
| F7        | EOX                                       |

(for Samson's "custom CCs" (> 127), +1 (e.g. CC#152 (Master Volume) => `01 19` == 0x99 == 153))

#### Encoder flags

| Function                    | *ff* bit 0 |
|-----------------------------|:----------:|
| Absolute (0..127)           |      0     |
| Relative (left=65, right=1) |      1     |

#### Buttons and pads flags

| Type       | *ff* bit 0 |
|------------|:----------:|
| Controller |      0     |
| Note       |      1     |

| Mode       | *ff* bit 1 |
|------------|:----------:|
| Toggle     |      0     |
| Momentary  |      1     |

### Response type 2 (misc. settings)

[todo]

## Setting a control

### Request

| Byte(s)       | Description             |
|---------------|-------------------------|
| F0            | SOX                     |
| 00 20 6b      | Arturia manufacturer ID |
| 02 *op*       | Operation code          |
| *n1* *n2*     | Hardware control ID     |
| *v1* *v2*     | Value to set            |
| F7            | EOX                     |

(Seems like the note about Samson CC doesn't work here. "Master Volume" is read as `01 19`, but is written as `01 18`. Weird.)

#### Operation codes

| Operation    | *op* |
|--------------|:----:|
| set CC#      |  01  |
| set channel# |  02  |
| set port#    |  03  |
| set flags    |  04  |

### Response

| Byte(s) | Description    |
|---------|----------------|
| F0      | SOX            |
| 0A      | ???            |
| *op*    | operation code |
| ?? ??   |                |
| F7      | EOX            |

## Saving the current setup into a preset

### Request

| Byte(s)       | Description                          |
|---------------|--------------------------------------|
| F0            | SOX                                  |
| 00 20 6b      | Arturia manufacturer ID              |
| 02 07 *nn* 00 | save to the *nn*'th preset (0-based) |
| F7            | EOX                                  |

