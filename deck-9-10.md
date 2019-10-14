---
revealOptions:
    transition: 'slide'
---

# A Philosophy Of Software Design
John Ousterhout

---

Recap!

---

Modules are separated between

* Interface
* Implementation

---

Interface adds complexitiy to the _whole_ system

---

Think about interfaces as the _cost_ of a module, and implementation as the _benefit_ from the module

---

## Chapter 9
Better Together Or Better Apart?

---

Be careful when subdividing modules!

_The act of subdividing creates additional complexities that were not present before_

---

* More interfaces
* More code to manage more modules
* Code that would be easier to understand together is now separated
* Duplicated logic in different modules

---

Also, consider joining modules if they are _related_

---

* Share information
* Are always used together
* Overlap conceptually
* It's hard to understand one without looking at the other

---

<< splitting functions figure >>

---

## Chapter 10
Define Errors Out Of Existence

---

Approaches when a code reaches an exception:

* Move forward in spite of exception
* Abort operation and raise exception

---

Problems:

* Add complex componentto the interface, affecting multiple layers
* How to restore consistency?
* Exception handling is usually verbose
* Exception handling is usually far from normal-case code
* Exception handling code rarely executes

---

Solution:

_Reduce the number of places where exceptions have to be handled_

---

1. Define Errors Out Of Existence

---

2. Mask exceptions

_Deal with exceptions in a lower level of the system_

---

3. Exception aggregation

_Deal with multiple exceptions in a single place_

---

4. Just crash

---

:)
