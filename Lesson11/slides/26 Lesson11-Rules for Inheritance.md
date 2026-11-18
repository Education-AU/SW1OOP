---
title: Rules to Observe in Inheritance
template: two-column
---

If using inheritance be sure that

- B and C can be thought of as a TYPE of A.
- B an C are really Specializations of A in the current domain
- Another way to put it: A is a generalization of B and C in the current domain
- If A is extended with further attributes/methods, they should be desired in B and C.
- Notice that B and C must have knowledge of the inner workings of A (constructor)

<!-- column -->

<img src="assets/images/inheritance-rules.svg" alt="B and C both inherit from A." style="display: block; width: 300px; max-width: 100%; height: auto; margin: 0 auto;">

The way to decide whether these rules are upheld, is wildly dependent on the domain.

If B or C has new methods implemented, that are not in A. A-references are not adequate to access these methods, and it will demand the use of down-type casting.

Generally, inheritance couple the children and parent very tightly in a very static manner. And changes to an inheritance hierarchy can be very expensive in the sense of developing time
