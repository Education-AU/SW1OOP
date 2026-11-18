---
title: "Exercise 3: Child"
template: default
---

The `child` class contains an extra dynamically allocated resource:

```cpp
class child : public parent {
public:
    child(const int number_of_resources, const int value_of_extra)
        : parent(number_of_resources) {
        extra_resource_ = new resource(value_of_extra);
    }

private:
    resource* extra_resource_;
};
```
