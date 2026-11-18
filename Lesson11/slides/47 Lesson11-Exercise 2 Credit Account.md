---
title: "Exercise 2: Credit Account"
template: default
---

4. The `credit_account` constructor should enforce `balance + credit >= 0` by throwing `std::invalid_argument`. The base `account` constructor rejects a negative initial balance, so initialize the base with a different amount and validate the requested balance afterwards. This requires using the protected `balance`. Is this really a good idea?
5. The `credit_account` implementation of `withdraw` should only enforce `balance + credit >= 0`, also by throwing `std::invalid_argument`. To allow a negative balance within the credit limit, use the protected `balance` member from `account` directly. Think about the consequences of allowing a derived object to violate the base class invariant.
