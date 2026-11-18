---
title: "Exercise 1: Vehicle and Car"
template: default
---

### `car`

The `car` class inherits publicly from `vehicle` and has additional private member variables:

```cpp
std::string make
std::string model
```

These members should be initialized in the constructor of `car` along with the super-class `vehicle` constructor parameters.

The `range()` method is inherited with no re-definition.

The `to_string()` method of `car` should shadow and call the `to_string()` method of `vehicle` and concatenate a string representation of `make` and `model` to the result.
