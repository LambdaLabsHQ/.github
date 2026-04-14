# Lambda Labs

We are building the interface layer for AI-native game development.

We believe modern game development is constrained by a deep path dependence: the toolchain is built around dense, high-friction human interaction. As a result, today's AI is still far less agentic in game development than it is in other software domains — especially in gameplay implementation, bug debugging, level design, and balancing, where progress still depends heavily on humans driving interactive tools.

Most AI tooling around game engines inherits that limitation. It is still trapped in wrappers: fixed tools, brittle schemas, stateless commands, and shallow access to runtime state. We want to break that pattern.

Our goal is simple:

**make AI agents first-class operators inside game engines.**

We think that requires two core agentic capabilities:
- **Ability** — agents need the power to act across code, assets, and live engine state
- **Evaluation** — agents need the ability to inspect outcomes and judge them against clear criteria, whether that means correctness, playability, performance, visual quality, or any other dimension with a usable evaluation method

If those two capabilities exist, AI stops being a coding assistant with better autocomplete and starts becoming a real participant in the game development loop.

We are not interested in AI slop, prompt-to-junk demos, or toolchains that only generate code and hope for the best.

We are building infrastructure for **runtime-aware, evaluation-driven, agentic game development**.

## What we’re building

### `unity-repl`
A persistent C# REPL running on the Unity main thread.

This is the core interface layer. Instead of forcing agents through a menu of predefined tools, `unity-repl` lets them evaluate raw C# directly against a live Unity session. That enables stateful inspection, runtime mutation, and much tighter build-verify-fix loops.

### `unity-agent-*`
Capability libraries for `unity-repl`.

These packages extend `unity-repl` with higher-level abilities for agents. Today that includes perception and control primitives like Game View capture, overlay-aware screenshots, and reliable keyboard and mouse input in Play Mode. Together, they turn the REPL from a raw runtime interface into a more complete operator surface for agentic workflows inside Unity.

### Beyond today’s primitives
Gradually expanding AI agency across real game development workflows.

We want to keep solving concrete problems that make more of the game development process meaningfully agentic over time. That includes areas like multiplayer debugging and live state inspection across connected clients, gameplay iteration and balancing, level design workflows, regression and QA flows grounded in actual runtime behavior, and performance investigation through direct observation of live systems.

Our long-term view is not that AI should sit outside the toolchain suggesting edits. It should be able to enter more of the real development process wherever ability and evaluation can be made concrete.

## Why this matters

Game development is one of the hardest environments for AI:
- the source of truth lives across code, assets, and a live engine
- correctness depends on runtime behavior, not just static output
- iteration speed matters as much as raw generation speed
- verification is as important as creation

We think the winning stack for AI in games will not be “more tools.”
It will be infrastructure that makes real agentic ability and evaluation possible inside the development environment itself.

## Our near-term focus

Right now, our focus is on Unity and on the shortest path to real value:
- giving agents direct runtime access to the engine
- enabling visual and input feedback loops
- turning those primitives into practical workflows, especially for QA, debugging, and rapid iteration

Longer term, we want to help reshape the game development ecosystem around agents that can do more than suggest code — agents that can actually operate, verify, and improve live game systems.

## Principles

- **Runtime first.** A game is not just source files; it is a live system.
- **Verification over vibes.** Generated output matters less than whether it actually works.
- **Minimal abstraction.** The best interface is the one that gets out of the way.
- **Developer amplification, not replacement theater.** We build tools that make teams faster and sharper.
- **Real workflows over demos.** We care about repeatable leverage, not stage magic.

## Follow the work

If you want to understand the technical core, start with `unity-repl`.

We believe the future of game development belongs to teams that can combine human judgment with agents that can inspect, act, and verify in real runtime environments.
