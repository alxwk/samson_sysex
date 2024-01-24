# Samson Graphite 49 SysEx control messages

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

| Byte(s)       | Description                                                            |
|---------------|------------------------------------------------------------------------|
| F0            | SOX                                                                    |
| 00 20 6b      | Arturia manufacturer ID                                                |
| 02 05 *nn* 00 | request of the *nn*'th preset (0 based, `7f` means the current preset) |
| F7            | EOX                                                                    |
