---
editable: false
sourcePath: en/_api-ref/video/v1/api-ref/Stream/index.md
---

# Video API, REST: Stream methods
Stream management service.
## JSON Representation {#representation}
```json 
{
  "id": "string",
  "channelId": "string",
  "lineId": "string",
  "title": "string",
  "description": "string",
  "thumbnailId": "string",
  "status": "string",
  "startTime": "string",
  "publishTime": "string",
  "finishTime": "string",
  "createdAt": "string",
  "updatedAt": "string",
  "labels": "object",

  //  includes only one of the fields `onDemand`, `schedule`
  "onDemand": {},
  "schedule": {
    "startTime": "string",
    "finishTime": "string"
  },
  // end of the list of possible fields

}
```
 
Field | Description
--- | ---
id | **string**<br><p>ID of the stream.</p> 
channelId | **string**<br><p>ID of the channel where the stream was created.</p> 
lineId | **string**<br><p>ID of the line to which stream is linked.</p> 
title | **string**<br><p>Stream title.</p> 
description | **string**<br><p>Stream description.</p> 
thumbnailId | **string**<br><p>ID of the thumbnail.</p> 
status | **string**<br>Stream status.<br><ul> <li>OFFLINE: Stream offline.</li> <li>PREPARING: Preparing the infrastructure for receiving video signal.</li> <li>READY: Everything is ready to launch stream.</li> <li>ONAIR: Stream onair.</li> <li>FINISHED: Stream finished.</li> </ul> 
startTime | **string** (date-time)<br><p>Stream start time.</p> <p>String in <a href="https://www.ietf.org/rfc/rfc3339.txt">RFC3339</a> text format. The range of possible values is from ``0001-01-01T00:00:00Z`` to ``9999-12-31T23:59:59.999999999Z``, i.e. from 0 to 9 digits for fractions of a second.</p> <p>To work with values in this field, use the APIs described in the <a href="https://developers.google.com/protocol-buffers/docs/reference/overview">Protocol Buffers reference</a>. In some languages, built-in datetime utilities do not support nanosecond precision (9 digits).</p> 
publishTime | **string** (date-time)<br><p>Stream publish time. Time when stream switched to ONAIR status.</p> <p>String in <a href="https://www.ietf.org/rfc/rfc3339.txt">RFC3339</a> text format. The range of possible values is from ``0001-01-01T00:00:00Z`` to ``9999-12-31T23:59:59.999999999Z``, i.e. from 0 to 9 digits for fractions of a second.</p> <p>To work with values in this field, use the APIs described in the <a href="https://developers.google.com/protocol-buffers/docs/reference/overview">Protocol Buffers reference</a>. In some languages, built-in datetime utilities do not support nanosecond precision (9 digits).</p> 
finishTime | **string** (date-time)<br><p>Stream finish time.</p> <p>String in <a href="https://www.ietf.org/rfc/rfc3339.txt">RFC3339</a> text format. The range of possible values is from ``0001-01-01T00:00:00Z`` to ``9999-12-31T23:59:59.999999999Z``, i.e. from 0 to 9 digits for fractions of a second.</p> <p>To work with values in this field, use the APIs described in the <a href="https://developers.google.com/protocol-buffers/docs/reference/overview">Protocol Buffers reference</a>. In some languages, built-in datetime utilities do not support nanosecond precision (9 digits).</p> 
createdAt | **string** (date-time)<br><p>Time when stream was created.</p> <p>String in <a href="https://www.ietf.org/rfc/rfc3339.txt">RFC3339</a> text format. The range of possible values is from ``0001-01-01T00:00:00Z`` to ``9999-12-31T23:59:59.999999999Z``, i.e. from 0 to 9 digits for fractions of a second.</p> <p>To work with values in this field, use the APIs described in the <a href="https://developers.google.com/protocol-buffers/docs/reference/overview">Protocol Buffers reference</a>. In some languages, built-in datetime utilities do not support nanosecond precision (9 digits).</p> 
updatedAt | **string** (date-time)<br><p>Time of last stream update.</p> <p>String in <a href="https://www.ietf.org/rfc/rfc3339.txt">RFC3339</a> text format. The range of possible values is from ``0001-01-01T00:00:00Z`` to ``9999-12-31T23:59:59.999999999Z``, i.e. from 0 to 9 digits for fractions of a second.</p> <p>To work with values in this field, use the APIs described in the <a href="https://developers.google.com/protocol-buffers/docs/reference/overview">Protocol Buffers reference</a>. In some languages, built-in datetime utilities do not support nanosecond precision (9 digits).</p> 
labels | **object**<br><p>Custom labels as ``key:value`` pairs. Maximum 64 per resource.</p> 
onDemand | **object** <br> includes only one of the fields `onDemand`, `schedule`<br><br><p>If "OnDemand" is used, client should start and finish explicitly.</p> 
schedule | **object** <br> includes only one of the fields `onDemand`, `schedule`<br><br><p>If "Schedule" is used, stream automatically start and finish at this time.</p> 
schedule.<br>startTime | **string** (date-time)<br><p>String in <a href="https://www.ietf.org/rfc/rfc3339.txt">RFC3339</a> text format. The range of possible values is from ``0001-01-01T00:00:00Z`` to ``9999-12-31T23:59:59.999999999Z``, i.e. from 0 to 9 digits for fractions of a second.</p> <p>To work with values in this field, use the APIs described in the <a href="https://developers.google.com/protocol-buffers/docs/reference/overview">Protocol Buffers reference</a>. In some languages, built-in datetime utilities do not support nanosecond precision (9 digits).</p> 
schedule.<br>finishTime | **string** (date-time)<br><p>String in <a href="https://www.ietf.org/rfc/rfc3339.txt">RFC3339</a> text format. The range of possible values is from ``0001-01-01T00:00:00Z`` to ``9999-12-31T23:59:59.999999999Z``, i.e. from 0 to 9 digits for fractions of a second.</p> <p>To work with values in this field, use the APIs described in the <a href="https://developers.google.com/protocol-buffers/docs/reference/overview">Protocol Buffers reference</a>. In some languages, built-in datetime utilities do not support nanosecond precision (9 digits).</p> 

## Methods {#methods}
Method | Description
--- | ---
[create](create.md) | Create stream.
[delete](delete.md) | Delete stream.
[get](get.md) | Returns the specific stream.
[list](list.md) | List streams for channel.
[performAction](performAction.md) | Perform an action on the episode.
[update](update.md) | Update stream.