---
title: Reusing Person in Employee
template: default
---


```cpp
class Employee{
public:
    Employee(const long cpr, const std::string& name, const double salary)
        : person_(cpr, name), salary_(salary){}

    long get_cpr() const{return person_.get_cpr();}

    std::string get_name() const{return person_.get_name();}

    int get_age() const{return person_.get_age();}

    bool has_birthday() const{return person_.has_birthday();}

    double annual_income() const{
        return 12 * salary_;
    }

private:
    Person person_;
    double salary_;
};
```
