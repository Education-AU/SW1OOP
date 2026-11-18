---
title: Rule of Three in the Base Class
template: default
className: slide--default slide--parent-code
---

Exactly how is rule of three implemented in a derived class?

<style>
  .slide--parent-code .code-block { font-size: 0.875rem; line-height: 1.15; margin-block: 0.4rem; }
</style>

```cpp
class parent {
public:
    parent(const int parent_data) : parent_data_(parent_data) {
        std::cout << "CTOR of parent called" << "\n";
    }

    parent(const parent &copy) : parent_data_(copy.parent_data_) {
        std::cout << "COPY CTOR of Parent called" << "\n";
    }

    parent &operator=(const parent &right) {
        if (this != &right) {
            parent_data_ = right.parent_data_;
        }
        std::cout << "ASSIGNMENT in parent called" << "\n";
        return *this;
    }

    ~parent() {
        std::cout << "DESTRUCTOR of parent called" << "\n";
    }
private:
    int parent_data_;
};
```
