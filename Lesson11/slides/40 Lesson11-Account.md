---
title: Account
template: default
---

```cpp
class Account{
public:
    Account(const int acc_number) : acc_number_(acc_number), balance_(0){}
    void deposit(const double amount){balance_ += amount;}
    double get_balance() const{return balance_;}
    int get_acc_nr() const{return acc_number_; }
protected:
    void set_balance(const double balance){ balance_ = balance; }
private:
    int acc_number_;
    double balance_;
};
```
