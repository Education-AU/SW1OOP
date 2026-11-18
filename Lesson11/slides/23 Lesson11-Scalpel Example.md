---
title: Silly Inheritance — Scalpel
template: two-column
---

The scalpel though used by both a surgeon and a foot-therapist should not be reused by inheritance. Why?

- A surgeon and a foot therapist do not get autoclaved say
- The weight and length are not attributes that are interesting for surgeons and foot therapists
- Many methods and data will appear on surgeon and therapist that are of no significance to a scalpel
- The specialization, generalization aspect is out the window

<!-- column -->

<img src="assets/images/scalpel-inheritance.svg" alt="An example of misuse: Foot Therapist and Surgeon are shown inheriting from Scalpel." style="display: block; width: 480px; max-width: 100%; height: auto; margin: 0 auto;">
