---
title: Subtleties in Inheritance — Visibility
template: default
---

1. **Private** methods and attributes are not inherited
2. **Protected** and public attributes and methods are
3. **Protected** cannot be accessed from the outside like public
4. **Protected** attributes couples the derived class in a higher degree because these can be used in  the child, so beware of this.
5. If access to  privates from the base class are needed in a derived class, it is better to use protected getters and setters of some sort because you can break the invariants of the base class easily accessing privates promoted to protected  directly.
6. Of course, in some cases protected access could optimize your code say if no validation is needed. That is if the bare data type is validation in itself.
  
The next example shows how direct access to a protected field can break an invariant.
