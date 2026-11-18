---
title: "Exercise 3: Parent"
template: default
---

The `parent` class contains a pointer to an array of pointers to `resource` objects and an attribute storing the size of the array, `size_of_resources_`.

The constructor is implemented:

```cpp
class parent {
public:
    parent(const int number_of_resources) : size_of_resources_(number_of_resources) {
        random_resources_ = new resource*[size_of_resources_];
        for (int i = 0; i < number_of_resources; i++) {
            random_resources_[i] = new resource(get_number());
        }
    }

private:
    int size_of_resources_;
    resource** random_resources_;
};
```
