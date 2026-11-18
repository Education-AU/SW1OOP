---
title: "Exercise 3: Random Number Helper"
template: default
---

This is a helper function you can place in a separate header file:

```cpp
#pragma once
#include <random>

std::random_device rd;
std::mt19937 rng(rd());
std::uniform_int_distribution<int> distribution(1, 100);

inline int get_number() {
    return distribution(rng);
}
```
