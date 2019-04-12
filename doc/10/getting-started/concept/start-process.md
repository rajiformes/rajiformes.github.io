---
layout: documentation
title:  Concept - 2. Start A Process
---

# Concept

## 2. Start A Process 

First of all we have tell to Raji that we want start to submit a absense form. Let assume absence request form registered as **absence-request**

### Request
```
POST https://.../raji/data/absence-request/new
```

### Response
As a response you get an instance item id and available transtitions of item.

```JSON
{
  "$instance-id": "3cebc6b9-79a0-42db-807f-9a9d9507388e",
  "$process": {
    "code": "absence-request",
    "label": "Absense Request",
    "display-view": "display-absence-request",
    "active-states": [
      {
        "label": "Request Absence",
        "code": "request-absence",
        "transitions": [
          {
            "label": "Submit Absense Request",
            "code": "submit",
            "modify-view": "modify-absence-request-submit"
          }
        ]
      }
    ]
  }
}
```
What we get and see:
1. An unique item id as **\$instance-id** for intereaction and queriying item. notice **$** started simple or complex all types.
2. **\$process** object contains information about process, existing state and available transtions.
3.  View names are required for requesting view definition metadata.
