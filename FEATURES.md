# sock API features

## Overview
| Feature Name | Description                                           |
|--------------|-------------------------------------------------------|
| enum         | Describes a pre-defined set of values.                |
| int          | Describes an integer between two values.              |
| float        | Describes a floating point number between two values. |

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

## int
The int feature describes a range of possible integer values for the device.

Any int type features must also include `value`, `min` and `max` fields.

```JSON
{
  "name": "mode",
  "type": "int",
  "value": 0,
  "min": 0,
  "max": 4
}
```

## float
The int feature describes a range of possible floating point values for the
device.

Any float type features must also include `value`, `min` and `max` fields.

```JSON
{
  "name": "mode",
  "type": "float",
  "value": 0.0,
  "min": 0,
  "max": 100
}
```
