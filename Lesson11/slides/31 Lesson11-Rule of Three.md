---
title: Rule of Three
template: default
---

The derived class has its own:

1. Copy constructor
2. Copy assignment operator
3. Destructor

When writing a derived copy constructor or copy assignment operator, explicitly copy or assign the base subobject. You do not need to call the base destructor yourself: it runs automatically after the derived part is destroyed.
