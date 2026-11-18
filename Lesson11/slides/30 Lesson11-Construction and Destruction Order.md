---
title: Constructor and Destructor Order
template: default
---

When a derived class is instantiated the constructor of the top base class is called and then constructors down the hierarchy are called successively.

In the example `curve <- ellipse <- circle`, constructing a `circle` calls the constructors in this order: `curve()`, `ellipse()`, `circle()`.

The order is set by the class declarations, not by the order in the initializer list. Write initializers in the order they run.

**Destructors are called in the opposite order!**
