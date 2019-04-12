---
layout: documentation
title: Concept - 4. Submit Form Data
---

# Concept

## 4. Submit Form Data

### Request
```
POST https://.../raji/data/absence-request/modify-absence-request-submit/3cebc6b9-79a0-42db-807f-9a9d9507388e
```
```JSON
{
  "instance-id": "3cebc6b9-79a0-42db-807f-9a9d9507388e",
  "fields": [
    {
      "id": "type",
      "value": "vacation"
    },
    {
      "id": "reason",
      "value": "Private family trip."
    },
    {
      "id": "start-date",
      "value": "2019-08-13"
    },
    {
      "id": "finish-date",
      "value": "2019-08-21"
    }
  ]
}
```


