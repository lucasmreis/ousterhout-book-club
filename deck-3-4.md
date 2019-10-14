---
revealOptions:
    transition: 'slide'
---

# A Philosophy Of Software Design
John Ousterhout

---

Recap!

---

## Symptoms Of Complexity

1. Change Amplification
2. Cognitive Load
3. Unkown Unknowns

---

## Causes Of Complexity

1. Dependencies
2. Obscurity

---

## Fighting Complexity

1. Elimination
2. Encapsulation

---

## Chapter 3
Working Code Isn't Enough
(Strategic Vs. Tactical Programming)

---

## Tactical Programming

Main focus: get something working as quick as possible

_"It's ok to add a bit of complexity in order to deliver faster!"_

---

This is how a codebase become complex - remember **complexity is incremental**

Think about projects that are so complex it doesn't even make sense trying to fix it anymore

---

## Strategic Programming

Main focus: produce a great design, which also happens to work

_Working code isn't enough!_

---

> Most of the code in any system is written by **extending** the existing code base, so your most important job as a developer is to facilitate those future extensions

---

Huge up-front investment, such as trying to design the entire system, **won't work**

The best approach is **continually** making small investments, adding up to about 10-20% of your total development time

---

> Once a code base turns to spaghetti, it's nearly impossible to fix. You will probably pay high development costs for the life of the product

---

## Chapter 4
Modules Should Be Deep

---

A software system can be decomposed into a collection of modules that are relatively independent

> The goal of modular design is to minimize the dependencies between modules

---

A module has two parts:

1. Interface
2. Implementation

---

## Interface

> Everything a developer working in a different module must know in order to use the given module

---

## Implementation

The code that carries out the promises made by the interface

---

> A developer working in a particular module must understand the interface and implementation of that module, plus the interfaces of any other modules invoked by the given module

---

Interface should be much simpler than implementations. Why?

1. It minimizes the complexity that a module **imposes on the rest** of the system
2. Changes that do not affect the interface **do not affect the rest** of the system

---

Interfaces contain **two** kins of information

1. Formal: specified explicitly in code
2. Informal: elements that are not specified in a way that can be codified

---

> In general, if a developer needs to know a particular piece of information in order to use a module, then that information is part of the module's interface

---

## Abstractions

A simplified view of an entity, which omits unimportant details

_Each module provides an abstraction in form of its interface!_

---

Abstractions can go wrong in two ways:

1. Including details that are _not_ important (needs more **cognitive load**)
2. Omitting details that _are_ important (creates **obscurity**)

---

### Modules Should Be Deep

---

Interface is a **cost** on the system

Implementation is **benefits** to the system

_It's a cost/benefit analysis!_

---

> Interfaces should be designed to make the common case as simple as possible

The effective complexity of an interface is the complexity of the most used features

---

### Conclusions

1. By separating the interface of a module from its implementation, we can hide the complexity of the implementation from the rest of the system

---

### Conclusions

2. Users of a module need only to understand the abstraction provided by the interface

---

### Conclusions

3. The most important issue in designing modules is to make them deep, so that they have simple interfaces for the common use cases, yet still provide significant functionality. This maximizes the amount of complexity that is concealed