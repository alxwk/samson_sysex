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

| Byte(s)   | Description                          |
|-----------|--------------------------------------|
| F0        | SOX                                  |
| *n1* *n2* | Hardware control ID (see tables)     |
| *rr* *rr* | Assigned Samson CC# (see the manual) |
| *cc*      | Channel# (`10` means the current)    |
| *pp*      | Port# (`05` means the current)       |
| *ff*      | Flags                                |
| F7        | EOX                                  |

(for Samson's "custom CCs" (> 127), +1 (e.g. CC#152 (Master Volume) => `01 19` == 0x99 == 153))

#### Sliders (*n1* == `00`, *n2* - see the table)

(yes, the placing is *this* weird)

| Slider | Bank 1 | Bank 2 |
|--------|:------:|:------:|
| S1     |   02   |   14   |
| S2     |   01   |   15   |
| S3     |   00   |   16   |
| S4     |   03   |   17   |
| S5     |   05   |   18   |
| S6     |   07   |   19   |
| S7     |   06   |   1A   |
| S8     |   04   |   1B   |
| S9     |   0A   |    -   |

#### Encoders (*n1* == `01`, *n2* - see the table)

| Encoder | Bank 1 | Bank 2 |
|---------|:------:|:------:|
| E1      |   03   |   08   |
| E2      |   07   |   09   |
| E3      |   02   |   0A   |
| E4      |   06   |   0B   |
| E5      |   01   |   0C   |
| E6      |   05   |   0D   |
| E7      |   00   |   0E   |
| E8      |   04   |   0F   |

##### Encoder flags

| Function          | *ff* bit 0 |
|-------------------|:----------:|
| Absolute (0..127) |      0     |
| Relative (0, 127) |      1     |

#### Function Buttons (*n1*==`02`)

| Button | *n2* | Button | *n2* |
|--------|:----:|--------|:----:|
| F1     |  27  | F9     |  1F  |
| F2     |  26  | F10    |  1E  |
| F3     |  25  | F11    |  1D  |
| F4     |  24  | F12    |  1C  |
| F5     |  23  | F13    |  1B  |
| F6     |  22  | F14    |  1A  |
| F7     |  21  | F15    |  19  |
| F8     |  20  | F16    |  18  |

#### Transport Buttons (*n1*==`02`)

| Button | *n2* |
|--------|:----:|
| ⏪ REW |  2B  |
| ⏩ FF  |  2C  |
| ⏹ STOP |  2D  |
| ⏵ PLAY |  2E  |
| ⏺ REC  |  2F  |

#### Pads (*n1*==`02`)

| Pad       | *n2* | Pad       | *n2* |
|-----------|:----:|-----------|:----:|
| P1 bank A |  30  | P5 bank B |  34  |
| P2 bank A |  31  | P6 bank B |  35  |
| P3 bank A |  32  | P7 bank B |  36  |
| P4 bank A |  33  | P8 bank B |  37  |

##### Buttons and pads flags

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

## Set a control

### Request

| Byte(s)       | Description             |
|---------------|-------------------------|
| F0            | SOX                     |
| 00 20 6b      | Arturia manufacturer ID |
| 02 *op*       | Operation               |
| *n1* *n2*     | Hardware control ID     |
| *v1* *v2*     | Value to set            |
| F7            | EOX                     |

(Seems like the note about Samson CC doesn't work here. "Master Volume" is read as `01 19`, but is written as `01 18`. Weird.)

#### Operation codes

| Operation    | Code |
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
