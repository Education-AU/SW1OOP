---
title: Visibility in the Calling Code
template: default
---

```cpp
int main() {
    rectangle r(1, 2, 'B');
    square s(2, 'B');

    //r.circumference(); protected method not visible in public but is in child
    //r.color; protected member variable not visible in public but is in child
    r.area();// this is public and compiles
    //s.circumference(); protected method not visible in public but is in child
    //s.color; protected member variable not visible in public but is in child
    s.area();// this is public and inherited and compiles

    return 0;
}
```
