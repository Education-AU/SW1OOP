---
title: "Exercise 1: Hybrid Car"
template: default
---

The `hybrid_car` class inherits publicly from `car` and has additional private member variables:

```cpp
double battery_capacity;
double battery_efficiency;
```

These members should be initialized in the constructor of `hybrid_car` along with the super-class `car` constructor parameters.

The `range()` method is shadowed. It returns the value returned from `car` plus the electric range, `battery_capacity * battery_efficiency`.

The `to_string()` method of `hybrid_car` should call and shadow the `to_string()` method of `car` and concatenate a string representation of `battery_capacity` and `battery_efficiency` to the result.
