---
title: Redefine or Shadow Methods
template: default
---

A derived class can

- Have its own redefined version of the base class function. Redefined meaning the same signature though
- This method can even call the base class version if necessary
- It can implement its own separate methods
- It can have its own attributes

In C++, a derived declaration can hide base-class functions with the same name even if the parameter lists differ.
