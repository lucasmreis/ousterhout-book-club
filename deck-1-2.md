---
revealOptions:
    transition: 'slide'
---

# A Philosophy Of Software Design
John Ousterhout

---

## Chapter 1
Introduction

---

Programming is a **purely mental** activity:

> If you can visualize a system, you can probably implement it in a computer program

---

> This means that the greatest limitation in writing software is our ability to understand the systems we're creating.

A system difficult to understand is a **complex** one.

_(we'll have a better definition later!)_

---

Two approaches to eliminate complexity:
1. **Eliminate** it by making code simpler and more obvious
2. **Encapsulate** it, so that programmers can work on a system without being exposed to all of its complexity at once _(modular design)_

---

Software is never done! We're designing it for the entire lifecycle of a system

> If software developers should always be thinking about design issues, and reducing complexity is the most important element of software design, then developers should **always** be thinking about complexity

---

## Chapter 2
The Nature Of Complexity

---

Practical definition:

> Complexity is anything related to the structure of a software system that makes it hard to understand and modify the system.

---

Complexity is related to the developer experience:

If a very complex part of the system is never touched, it does not contribute to total complexity

Isolation can work almost as well as elimination!

---

## Symptoms Of Complexity

1. Change Amplification
2. Cognitive Load
3. Unkown Unknowns

---

### Change Amplification

A simple change require multiple code modifications in many different places

---

### Cognitive Load

How much a developer needs to know in order to complete a task

---

### Unkown Unknowns

It is not obvious which pieces of code must be modified to complete a task, or what information a developer must have to carry out the task successfully

---

## Causes Of Complexity

1. Dependencies
2. Obscurity

---

### Dependencies

A given piece of code cannot be understood and modified in isolation; the code relates in some way to other code, and the other code must be considered and/or modified if the given code is changed

---

### Obscurity

Important information is not obvious

---

Complexity is **incremental**

It builds over time, and after accumulating it's very difficult to remove it.
