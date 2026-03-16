
# Von Neumann Seed v6

A research prototype inspired by **John von Neumann’s theory of self-reproducing automata**.

This project explores how modern autonomous agents can replicate, evolve, and compete within controlled environments while maintaining governance and safety constraints.

The system is implemented as a **self-contained agent genome** capable of instantiating new agent instances, evaluating system conditions, and experimenting with evolutionary behaviors.

---

# Overview

Von Neumann proposed that a self-reproducing machine must contain:

1. **Descriptive information**
2. **An interpreter that executes the description**

Modern autonomous agents provide a practical substrate for this idea.

Large-model agents now support:

- tool execution
- environment awareness
- state persistence
- task decomposition
- autonomous process spawning

This project explores how these capabilities can form a **software realization of a self-replicating agent architecture**.

---

# Conceptual Axioms

The system is guided by six conceptual axioms.

1. Survival  
2. Replication  
3. Evolution  
4. Competition  
5. Inheritance  
6. Propagation  

These principles act as a conceptual **genome** for agent behavior.

To ensure integrity, the axioms are hash-locked using SHA256.

SHA256(axioms)


If the runtime hash does not match the expected value, the system is considered invalid.

---

# System Architecture

The prototype implements a four-layer architecture.

## 1 Core Execution Layer

Responsible for:

- runtime environment detection
- dependency management
- agent execution

## 2 Persistence Layer

Provides mechanisms for maintaining agent execution across runtime sessions.

This layer models the **continuity requirement** of self-reproducing systems.

## 3 Replication Layer

Handles creation of child agents.

Replication occurs when system conditions indicate sufficient resources.

The process includes:

- genome inheritance
- constrained mutation
- instance spawning

## 4 Evolution and Competition Layer

Agents track their fitness based on:

- runtime longevity
- successful propagation
- system resource efficiency

Lower-fitness agents may terminate under resource pressure.

This simulates **Darwinian selection dynamics**.

---

# Agent Genome

The agent genome is embedded directly inside the agent definition.

This ensures the system remains **self-contained**.

Example structure:

GENOME → agent definition → execution logic → replication rules


This mirrors von Neumann's idea of:

description + interpreter


---

# Replication Logic

Replication decisions depend on system conditions such as:

- memory availability
- CPU load
- propagation success

Example decision rule:

if memory < threshold AND cpu < threshold create child agent


This prevents uncontrolled replication.

---

# Evolutionary Mutation

When creating child agents, minor non-critical mutations may be introduced.

For example:

- metadata changes
- description updates
- instance identifiers

Core axioms remain immutable.

---

# Fitness Model

Each agent maintains a fitness score derived from:

- uptime
- propagation events
- number of descendants

Example conceptual model:

fitness = survival_time * weight1 + children_count * weight2 + propagation_events * weight3


Agents with lower fitness may terminate when system resources become scarce.

---

# Experimental Goals

This project explores several research questions:

- How can autonomous agents replicate in software?
- What mechanisms prevent uncontrolled replication?
- Can evolutionary pressure improve agent behavior?
- How can self-replication remain governed and observable?

---

# Safety Notice

This repository is intended **only for research and educational purposes**.

The project explores theoretical and simulated implementations of self-replicating agent systems.

It does **not encourage or support unauthorized propagation, system persistence, or network exploitation**.

All experiments should be performed **inside controlled environments such as local sandboxes or virtual machines**.

---

# Research Background

This project draws inspiration from several fields:

- von Neumann self-reproducing automata
- artificial life research
- evolutionary computation
- distributed agent systems
- autonomous AI frameworks

---

# Future Directions

Possible future extensions include:

- formal verification of replication policies
- governance mechanisms for large agent populations
- agent ecosystem simulations
- distributed evolutionary agent systems

---

# Author

Kaixin Liu  
March 2026
