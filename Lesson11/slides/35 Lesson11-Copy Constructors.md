---
title: Copy Constructors in Derived Classes
template: two-column
className: slide--two-column slide--l11-special-members
---

```cpp
class child : public parent {
public:
    child(int parent_data, int child_data)
        : parent(parent_data), child_data_(child_data) {
        std::cout << "CTOR of child called" << "\n";
    }

    child(const child &to_copy)
        : parent(to_copy), child_data_(to_copy.child_data_) {
        std::cout << "COPY CTOR of child called" << "\n";
    }

private:
    int child_data_;
};
```

<!-- column -->

```cpp
class grand_child : public child {
public:
    grand_child(int parent_data, int child_data, int grand_child_data)
        : child(parent_data, child_data), grand_child_data_(grand_child_data) {
        std::cout << "CTOR of grand child called" << "\n";
    }

    grand_child(const grand_child &to_copy)
        : child(to_copy), grand_child_data_(to_copy.grand_child_data_) {
        std::cout << "COPY CTOR of grand child called" << "\n";
    }

private:
    int grand_child_data_;
};
```
