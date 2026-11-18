---
title: Visibility
template: default
---

1. **private** visibility of **members** and **methods**, which enforce that access is restricted to the class itself. **Not even child classes** have direct access to private data of parent classes.
2. **public** visibility of **members** and **methods**, which imposes **no restriction**. Objects of other classes, are free to interact with public members and methods of objects from classes with public visible data.

### Protected modifier

The new modifier **protected** restricts the visibility of members and methods **to child classes**..

That is, data with **protected visibility** is accessible to **child classes**, but **not** to other classes.

This is exemplified by this inheritance example where the **super class** is a `rectangle` class, and the child class is a `square` class.
