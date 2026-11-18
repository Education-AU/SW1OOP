---
title: Inheritance Syntax
template: two-column

---

```cpp
class employee : public person {
    public:
        employee(const long cpr, const std::string &name, const double salary)
            : person(cpr, name), salary_(salary) {}

        double annual_income() const {
            return 12 * salary_;
        }

    private:
        double salary_;
};
```
<!-- column -->

```cpp
class customer : public person {
    public:
        customer(long cpr, const std::string &name, const double credit_max, const double credit_)
            : person(cpr, name), credit_max_(credit_max), credit_(credit_) {}

        bool can_buy_on_credit(const double amount) const {
            return amount + credit_ <= credit_max_;
        }

    private:
        double credit_max_;
        double credit_;
};
```
