---
title: Constructor Output
template: two-column
---

```cpp
int main() {
    grand_child gc(1, 10, 100);
    return 0;
}
```

<!-- column -->

```text
CTOR of parent called
CTOR of child called
CTOR of grand child called
DESTRUCTOR of parent called
```
