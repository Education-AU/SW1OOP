---
title: Silly Inheritance — Database Connection
template: two-column
---

Just because all your domain objects are to be stored in a database does not make customers and so forth into database connections

As you have seen from just the constructor implementation the children must know about the parent’s inner workings. Now imagine the mess if you want to change your database.

<!-- column -->

<img src="assets/images/database-inheritance.svg" alt="An example of misuse: Product, Order, and Customer are shown inheriting from Database connection." style="display: block; max-width: 100%; height: auto; margin: 0 auto;">
