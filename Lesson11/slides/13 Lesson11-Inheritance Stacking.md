---
title: "Inheritance: Think in Layers"
template: default
---

Picture a derived object as two layers: a base class part and the fields the derived class adds. Both are part of the same object.

<img src="assets/images/inheritance-stacking.svg" alt="Conceptual diagram showing two objects. Each has a Person part with cpr and name, stacked above its own fields: salary for employee, and credit_max and credit for customer." style="display: block; max-width: 100%; height: auto; margin: 0 auto;">

Each `employee` and `customer` object has its own `Person` base class subobject, which holds `cpr` and `name`. An `employee` adds `salary`; a `customer` adds `credit_max` and `credit`.

The diagram shows the parts of each object, not their exact layout in memory.