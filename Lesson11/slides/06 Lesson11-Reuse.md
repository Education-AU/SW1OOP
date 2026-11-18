---
title: Reusing Person
template: two-column
className: slide--two-column slide--reuse-code
---

<style>
  .slide--reuse-code .code-block {
    white-space: pre-wrap;
    overflow-wrap: anywhere;
    line-height: 1.3;
  }
</style>

```cpp
class person {
public:
    long get_cpr() {return cpr_;}

    std::string get_name() {return name_;}

    int get_age() {return 10;/*In reality, calculated from cpr somehow*/ }

    int has_birthday() {return false;/*In reality, calculated from cpr somehow*/}

private:
    long cpr_;
    std::string name_;
};
```

<!-- column -->

```cpp
class Customer{
public:
    Customer(const long cpr, const std::string& name, const double credit_max, const double credit)
        : person_(cpr, name), credit_max_(credit_max), credit_(credit){}

    long get_cpr() const{return person_.get_cpr();}

    std::string get_name() const{return person_.get_name();}

    int get_age() const{return person_.get_age();}

    bool has_birthday() const{return person_.has_birthday();}

    bool can_buy_on_credit(double amount) const{
        return amount + credit_ <= credit_max_;
    }

private:
    Person person_;
    double credit_max_;
    double credit_;
};
```