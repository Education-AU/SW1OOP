---
title: "Exercise 2: Accounts and Invariants"
template: two-column
---

Consider the inheritance hierarchy:

<img src="assets/images/exercise-account-hierarchy.svg" alt="Both savings_account and credit_account inherit from account, whose balance is protected." style="display: block; max-width: 100%; height: auto; margin: 0 auto;">

<!-- column -->

1. Implement the `account` class using a `std::invalid_argument` exception in the constructor to enforce the invariant `balance >= 0`.
2. Implement the `withdraw` method on `account` that enforces the same invariant by throwing `std::invalid_argument`.
3. The `savings_account` `withdraw` method should shadow the `account` version. A single withdrawal cannot exceed the withdrawal limit( max one time withdrawal) or leave `balance <= 0`. Throw `std::invalid_argument` if either check fails. You can use the parent `withdraw` method in the implementation.
