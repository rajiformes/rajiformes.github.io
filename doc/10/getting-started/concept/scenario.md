---
layout: documentation
title: Concept - 1. Scenario
---

# Concept

## 1. Scenario

Let start with simple process, with requesting an absence form.

>Absence Form State Machine flow

<div class="mermaid">
  graph LR
  Start((Start)) -- Init --> B(Request)
  B -- Submit Request --> D(Evaluation)
  D -- Approve --> Finish
  D -- Reject --> Finish
</div>

  
