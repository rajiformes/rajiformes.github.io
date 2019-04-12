---
layout: documentation
title: Concept - 3. Build Absence Form
---

# Concept

## 3. Build Absence Form

First we have to build view. We know id of item, process info, and transition.

### Request
```
GET https://.../raji/view/absence-request/modify-absence-request-submit
```

```JSON{
  "$instance-id": "3cebc6b9-79a0-42db-807f-9a9d9507388e",
  "$fields": [
    {
      "id": "type",
      "type": "select",
      "label": "Absence Type",
      "config": {
        "select-message": "Please select absence type",
        "options": [
          {
            "label": "Vacation",
            "value": "vacation"
          },
          {
            "label": "Health",
            "value": "health"
          },
          {
            "label": "Business Trip",
            "value": "business-trip"
          }
        ]
      }
    },
    {
      "id": "reason",
      "type": "text",
      "label": "Absence Reasong",
      "config": {
        "multiline": true
      }
    },
    {
      "id": "start-date",
      "type": "date",
      "label": "Absence Starting At"
    },
    {
      "id": "finish-date",
      "type": "date",
      "label": "Absence Finishing At"
    }
  ],
  "$view": {
    "config": {
      "theme": "default",
      "title": "Absence Request Form",
      "prefix-components": [
        {
          "component": "personlized-information-component",
          "maps": [
            {
              "parameter": "user",
              "value": "system.user.username"
            }
          ]
        }
      ],
      "suffix-components": [
        {
          "component": "absense-utilization-component",
          "maps": [
            {
              "parameter": "user",
              "value": "system.user.username"
            }
          ]
        }
      ],
      "controls": {
        "type": "input-form",
        "controls": [
          {
            "type": "input-line",
            "field": "type"
          },
          {
            "type": "input-line",
            "field": "reason"
          },
          {
            "type": "input-line",
            "field": "start-date"
          },
          {
            "type": "input-line",
            "field": "finish-date"
          },
          {
            "type": "action-bar"
          }
        ]
      }
    }
  }
}
```
