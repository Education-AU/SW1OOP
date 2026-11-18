---
title: "Exercise 3: Rule of Three in an Inheritance Hierarchy"
template: default
---

This is kind of an abstract exercise that involves implementing the Rule of Three in an inheritance hierarchy.

Given is the class `resource`:

```cpp
class resource {
public:
    explicit resource(const int value) : value_(value) {}
    int get_value() const {
        return value_;
    }

private:
    int value_;
};
```
