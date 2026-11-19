---
title: "Exercise 3: Implement and Test"
template: default
---

1. Implement the Rule of Three on `parent`.
2. Implement the Rule of Three on `child`.
3. Test your implementation.

Use deep copies for both classes.

Testing rule of three implementation in CLion is not that easy.

For assignment operator :

Try to run the following code and monitor the process in process explorer

```cpp
auto* c = new child(10, 3);
auto* d = new child(10, 3);
while (true) {
    *c = *d;
}
```

If memory use keeps growing, the repeated assignment may be leaking memory.
