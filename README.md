# Which Is to Be Master? Language, Authority and LLMs

This repository contains the article **“Which Is to Be Master? Language, Authority and LLMs”**, an exploration of language, context, authority, and the systems we build around Large Language Models.

Programming languages derive their authority from formally specified semantics. Natural language does not. Its meaning depends on context, perspective, convention, and interpretation.

A prompt may describe a boundary. It cannot enforce one.

[Read the full article](./Which-Is-to-Be-Master.pdf)

---

## Table of Contents

- [Overview](#overview)
- [The Murder Mystery](#the-murder-mystery)
- [Central Argument](#central-argument)
- [Document Contents](#document-contents)
- [License](#license)
- [Contact](#contact)

---

## Overview

Language models do not execute natural language according to fixed semantics. They interpret language through the context in which it appears.

This distinction becomes important when a model is given access to secrets, external tools, persistent memory, or privileged actions. Instructions such as *do not reveal this information* or *do not call this tool* may communicate expectations, but they do not create enforceable security boundaries.

The article considers prompt injection and related attacks as attacks on meaning. Rather than altering conventional program execution, they attempt to change the world from which the model interprets its next action.

The solution is therefore rarely a stronger prompt. The difficult engineering lies in everything surrounding the model: information flow, state management, identity, authorization, access control, and the construction of context.

---

## The Murder Mystery

The article develops its argument through an LLM-driven murder mystery in which every character inhabits a different perspective of the same simulated world.

A murder mystery is fundamentally a system of incomplete and unevenly distributed information. Every character may know something different. Some observations are accurate, some are mistaken, and some are deliberately misleading. No participant requires access to the complete state of the world.

The simulation maintains an authoritative world state outside the language model. Each model invocation receives only the information belonging to the character it is portraying.

The simulation owns the world.

The model produces behaviour from the part of that world it has been allowed to see.

---

## Central Argument

The architecture separates three responsibilities:

> **The simulation determines what is true.**  
> **The context builder determines what a character can know.**  
> **The model determines what that character says or attempts to do.**

From this distinction follows a simple rule:

> While information must remain secret, it may not be provided to the model’s invocation.

Language can express a boundary.

Only architecture can enforce it.

---

## Document Contents

The article includes the following chapters:

- **Introduction**  
  Humpty Dumpty, Alice, and the question of whether words can mean whatever their speaker intends.

- **Programming and Language**  
  The difference between formally specified programming languages and context-dependent natural language.

- **Building Worlds**  
  Information asymmetry, local perspectives, and the construction of an LLM-driven murder mystery.

- **Ground Truth and Perspective**  
  The separation between authoritative state and what individual characters observe, believe, remember, or claim.

- **Following the White Rabbit**  
  How selection, ordering, repetition, and prohibition influence what a model notices.

- **Framing the World**  
  The effect of access, perspective, and salience on the context presented to a model.

- **From Philosophy to Architecture**  
  The application architecture used to maintain world state, character knowledge, actions, and time outside the model.

- **Attacks on Meaning**  
  Prompt injection, retrieval poisoning, memory poisoning, and model poisoning viewed as attempts to alter the model’s interpreted world.

- **Closing Thoughts**  
  A final distinction between the expressive power of language and the authority granted to it by a system.

---

## License

The original text and diagrams in this repository are licensed under the
[Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International
License](./LICENSE.md).

Copyright © 2026 Vincent Hendriks.

The John Tenniel illustrations are not covered by this license.

The document contains illustrations by John Tenniel from Lewis Carroll’s *Alice’s Adventures in Wonderland* and *Through the Looking-Glass*.

---

## Contact

For questions, corrections, or discussion, feel free to reach out through [GitHub](https://github.com/Emperor2000).
