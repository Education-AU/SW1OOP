---
title: "Exercise 2: Credit Account"
template: default
---

### credit_account

#### a)

The `credit_account` constructor should enforce `balance + credit >= 0` by throwing `std::invalid_argument`.

The base `account` constructor rejects a negative initial balance, so initialize the base with a balance+credit. This
will allow a negative balance within the credit limit. Think about the consequences of allowing a derived object to
violate the base class invariant.

#### b)

The `credit_account` implementation of `withdraw` should only enforce `balance - amount >= 0`, by throwing
`std::invalid_argument`. To allow a negative balance within the credit limit, use the protected `balance` member from
`account` directly. Think about the consequences of allowing a derived object to violate the base class invariant.

#### c)

Shadow `get_balance()` in `credit_account` to return the current balance minus the credit.