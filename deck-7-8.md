---
revealOptions:
    transition: 'slide'
---

# A Philosophy Of Software Design
John Ousterhout

---

Recap!

---

## Modules should be deep!

---

## Chapter 7
Different Layer, Different Abstraction

---

> In a well-designed system, each layer provides a different abstraction from the layers above and below it

Adjacent layers with similar abstractions = _FLAG!_

---

Interfaces should be different from its implementations

_you may be creating lots of shallow modules_

---

Be careful with:

* Pass-through methods
* Decorators
* Pass-through variables

---

## Chapter 8
Pull Complexity Downwards

---

> Most modules have more users than developers, so it is better for the developers to suffer than the users

---

It's more important for a module to have a simple interface than a simple implementation

---

Be careful with exposing configuration without sensible defaults

_They usually mean you are postponing important decisions, and adding complexity to users of the modules_

---

:)