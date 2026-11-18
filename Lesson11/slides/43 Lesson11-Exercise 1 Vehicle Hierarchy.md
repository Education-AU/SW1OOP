---
title: "Exercise 1: Vehicle Hierarchy"
template: two-column
---

Consider the UML class hierarchy depicted below:

<img src="assets/images/exercise-vehicle-hierarchy.svg" alt="The car class inherits from vehicle; hybrid_car inherits from car." style="display: block; width: 360px; max-width: 100%; height: auto; margin: 0 auto;">

<!-- column -->

The class `vehicle` represents a general vehicle that has private member variables:

```cpp
double fuel_consumption
double fuel_capacity
```

That should be initialized in a constructor.

The **public** method `double range()` returns the range of the vehicle defined by `fuel_capacity * fuel_consumption`.

The **public** method `std::string to_string()` should contain a textual representation of the values `fuel_capacity` and `fuel_consumption`.



