---
title: "Exercise 3: Implement and Test"
template: default
---

1. Implement the Rule of Three on `parent`.
2. Implement the Rule of Three on `child`.
3. Test your implementation.

Use deep copies for both classes.

To test the assignment operator, you can run the code:

```cpp
auto* c = new child(10, 3);
auto* d = new child(10, 3);
while (true) {
    *c = *d;
}
```

If memory use keeps growing, the repeated assignment may be leaking memory. Run in debug mode to monitor it, then stop the program manually.
