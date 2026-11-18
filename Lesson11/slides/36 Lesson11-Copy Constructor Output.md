---
title: Copy Constructor Output
template: two-column
className: slide--two-column slide--l11-special-members
---

```cpp
int main() {
    std::cout << "first object" << "\n";
    grand_child gc(1, 10, 100);
    std::cout << "\n" << "\n";
    std::cout << "Copy construction:" << "\n";
    grand_child gcc(gc);
    return 0;
}
```

<!-- column -->

```text
first object
CTOR of parent called
CTOR of child called
CTOR of grand child called


Copy construction:
COPY CTOR of Parent called
COPY CTOR of child called
COPY CTOR of grand child called
DESTRUCTOR of parent called
DESTRUCTOR of parent called
```
