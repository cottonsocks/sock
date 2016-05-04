# sock API

## Overview
| Request Type | Endpoint     | Description                   |
|--------------|--------------|-------------------------------|
| GET          | `/devices`   | A list of all devices.        |
| GET          | `/devices/1` | Information about device 1.   |
| POST         | `/devices/1` | Sets properties for device 1. |

## GET `/devices`
#### Response
```JSON
{
  "devices": [
    {
      "id": 1,
      "name": "Ceiling Light",
    },
    {
      "id": 2,
      "name": "Desk Lamp"
    }
  ]
}
```

## GET `/devices/1`
#### Response
```JSON
{
  "device": {
    "id": 1,
    "name": "Ceiling Light",
    "features": [
      {
        "name": "state",
        "type": "enum",
        "value": 0,
        "values": {
          "Off": 0,
          "On": 1
        }
      }
    ]
  }
}
```

## GET `/devices/99`
#### Response
```
HTTP/1.1 404 Not Found
```

Status code will be 404.

## POST `/devices/1`
#### Request
```JSON
{
  "device": {
    "features": [
      {
        "name": "state",
        "value": 1
      }
    ]
  }
}
```

#### Response
```JSON
{
  "device": {
    "id": 1,
    "name": "Ceiling Light",
    "features": [
      {
        "name": "state",
        "type": "enum",
        "value": 1,
        "values": {
          "Off": 0,
          "On": 1
        }
      }
    ]
  }
}
```

Same response as [GET `/devices/1`](#get-devices1) with updated values.
