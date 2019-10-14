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

## Tactical vs Strategic Programming

---

## Modules Should Be Deep

Interfaces vs Implementation

---

## Chapter 5
Information Hiding (and Leakage)

---

Information hidden: _how to implement some mechanism_

* Data structures
* Algorithms
* Decisions (ex. "page size")
* Assumptions (ex. "all images are small")

---

### Information Leakage

Details of the mechanisms are reflected/known by multiple modules

*Dependency!*

---

### Temporal Decomposition

Separating modules by _order_ and not by _knowledge_

---

### Taking it too far

If the information is needed outside the module, then you _must not hide it_

---

## Chapter 6
General-Purpose Modules Are Deeper

---

General-purpose seems consistent with the *investment* mindset

_Strategically thinking about the future!_

---

Special-purpose seems consistent with the *incremental* approach to development

_We can't predict the future!_

---

> The module's functionality should reflect your current needs, but its interface should not

---

General interfaces tend to be _smaller_, and modules tend to get _deeper_

(just don't make it difficult to use in your particular case)

---

1. What's the simplest interface that will cover all my current needs?
2. In how many situations will this function be used?
3. Is this API easy to use for my current needs?

---

:)