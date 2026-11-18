---
title: Subtleties in Inheritance — What Is Not Inherited
template: default
---
Rule of three is not inherited
1. Constructors are not inherited including copy constructor
2. Destructors are not inherited
3. Assignment operators are not inherited

But they all have default implementations if not implemented


Friend functions are not inherited not being members at all
