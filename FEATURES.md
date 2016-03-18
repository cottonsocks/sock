# sock API features

## Overview
| Feature Name | Description                            |
|--------------|----------------------------------------|
| enum         | Describes a pre-defined set of values. |

## enum
The enum feature describes a pre-defined set of possible values for the device.

Any enum type features must also include `value` and `values` fields.

```JSON
{
  "name": "state",
  "type": "enum",
  "value": 0,
  "values": {
    "Off": 0,
    "On": 1
  }
}
```
