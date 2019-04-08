
---
layout: documentation
title:  "Data in Rajiformes"
---

# Data Persistance

Rajiformes deals data as **JSON** format. Data can contain simple types, complex types and data references.

> A data model including simple types data.
```JSON
{
  "name": {
    "first": "Ugur",
    "last": "karatas"
  },
  "gender": "Male",
  "age": "41",
  "title": "Enterprise Architect"
}
```

Data model can include another data model to create complex types. Complex types data lookup from an existing dynamic document (tables, document stores etc.) or static lists (enum, predefined lists etc.)

> A data model including simple types data and department info filled from another dynamic document.

```JSON
{
  "name": {
    "first": "Ugur",
    "last": "karatas"
  },
  "gender": "Male",
  "age": "41",
  "title": "Enterprise Architect",
  "department": {
    "id": "1068907e-782c-4b16-8573-39d50182f354",
    "title": "Enterprise Architecture and Innovation",
    "floor": 6
  }
}
```


> A data model including simple types data and department info filled from predefined list.

```JSON{
  "name": {
    "first": "Ugur",
    "last": "karatas"
  },
  "gender": "Male",
  "age": "41",
  "title": "Enterprise Architect",
  "department": {
    "id": "1068907e-782c-4b16-8573-39d50182f354",
    "key": "EA",
    "title": "Enterprise Architecture and Innovation",
    "floor": 6
  }
}
```
