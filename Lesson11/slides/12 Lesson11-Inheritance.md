---
title: Using Inherited Methods
template: default
---
The inheritance that we are going to use is public:

```cpp
class employee : public person {
    // class definition
};
```

We will explain the modifier `public` versus `protected` and `private` later.

The constructor of the **child** class must take on **responsibility of calling the constructor of the super class**.


That is **employee** must instantiate its inherited person object:

```cpp
employee(const long cpr, const std::string &name, const double salary): person(cpr, name), salary_(salary) {};
```

This should always be done in the initializer list.

