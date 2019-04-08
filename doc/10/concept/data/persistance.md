---
layout: documentation
title:  "Data Persistance in Rajiformes"
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

>Data model can include another data model to create complex types. Complex types data lookup from an existing entity (tables, document stores etc.) or static lists (enum, predefined lists etc.)
> A data model including simple types data and department info filled from another dynamic document.

- Depertmant property has  **_id** property that is reference id to item in **departments** entity
  
- Also title and floor properties is populated from referenced entity. This means referenced item data populated to item. *This is Simple versioning !*

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
    "_id": "1068907e-782c-4b16-8573-39d50182f354",
    "_entity":"departments",
    "title": "Enterprise Architecture and Innovation",
    "floor": 6
  }
}
```

> A data model including simple types data and department info filled from predefined list.

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
    "key": "EA",
    "title": "Enterprise Architecture and Innovation",
    "floor": 6
  }
}
```

>Of cource reference property can be designed as one-to-many pattern.

- Referenced items can be sourced from any entity

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
    "_id": "1068907e-782c-4b16-8573-39d50182f354",
    "_entity": "departments",
    "title": "Enterprise Architecture and Innovation",
    "floor": 6
  },
  "project": [
    {
      "_id": "2068907e-782c-4b16-8573-39d50182f352",
      "_entity": "internal-project",
      "title": "Document Management System"
    },
    {
      "_id": "3068907e-782c-4b16-8573-39d50182f352",
      "_entity": "internal-project",
      "title": "Fund Trading Platform"
    },
    {
      "_id": "4068907e-782c-4b16-8573-39d50182f352",
      "_entity": "external-projects",
      "title": "Rajiformes"
    }
  ]
}
```