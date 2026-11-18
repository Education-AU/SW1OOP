---
title: Inherited Protected Attributes
template: two-column
className: slide--two-column slide--protected-account
---

<style>
  .slide--protected-account .code-block {
    white-space: pre-wrap;
    overflow-wrap: anywhere;
    line-height: 1.25;
  }
</style>

```cpp
class Account{
public:
    Account(const double balance) : balance_(balance<0?0:balance){}
    void withdraw(const double amount){
        if (amount > balance_){
            throw std::invalid_argument("Not enough credit");
        }
        balance_ -= amount;
    }
    void deposit(const double amount){
        balance_ += amount;
    }
    double get_balance() const{
        return balance_;
    }
protected:
    double balance_;
};
```

<!-- column -->

```cpp
class CreditAccount : public Account{
public:
    explicit CreditAccount(const double balance)
        : Account(balance){}
    void transfer(const double amount, Account& account){
        account.deposit(amount);
        balance_ -= amount;
    }
};
```

In this example Credit account can clearly break the invariant that is being established in the base class Account.
