---
title: Method Redefinition
template: two-column
className: slide--two-column slide--l11-special-members
---

```cpp
class ProgressiveAccount : public Account{
public:
    ProgressiveAccount(const int acc_number, const double progression_limit) :
        Account(acc_number), progression_limit_(progression_limit){}
    void deposit(const double amount){
        if (amount > progression_limit_){
            Account::deposit(amount * 1.1);
        }
        else{Account::deposit(amount);}
    }
private:
    double progression_limit_;
};
```

<!-- column -->

`ProgressiveAccount::deposit` hides the base-class method and calls it explicitly using `Account::deposit`. This is **hiding**, not overriding a virtual function.

```cpp
ProgressiveAccount pa(1, 100);
pa.deposit(10);
std::cout << pa.get_balance() << std::endl;
pa.deposit(200);
std::cout << pa.get_balance() << std::endl;
```

```text
10
230
```
