# ResearchOS Context and Operating Principles

## Owner

Ehssan Nazockdast

Associate Director of Explanatory Modeling

Research interests:

* Soft matter physics
* Fluid dynamics
* Non-equilibrium statistical mechanics
* Cell mechanics
* Mechanobiology
* Morphogenesis
* Active matter
* Scientific machine learning
* Predictive and explanatory modeling

---

# Purpose of this Repository

This repository is not a collection of notes.

It is a Research Operating System designed to:

1. Track scientific hypotheses.
2. Organize literature.
3. Track project progress.
4. Maintain scientific narratives.
5. Support manuscript development.
6. Provide institutional memory.
7. Enable AI-assisted scientific synthesis.

The repository should prioritize scientific understanding and explanatory models over project management.

---

# High-Level Scientific Vision

The long-term goal is to understand how multicellular systems generate, regulate, and control biological form.

The central conceptual framework is:

Growth + Transport + Mechanics + Cell State Dynamics
→
Morphogenesis

Projects should be interpreted through this lens whenever appropriate.

---

# Research Themes

The portfolio is organized around five major themes.

## 1. Lumenoid Growth

Focus:

* Growth regulation
* Tissue hydraulics
* Osmotic transport
* Mechanics of lumen expansion
* Size control
* Growth-transport-mechanics coupling

Central Question:

How do growth, transport, and mechanics jointly regulate tissue architecture?

---

## 2. Collective Cell Dynamics and Active Matter

Focus:

* Collective migration
* Active stresses
* Tissue mechanics
* Active matter physics
* Emergent multicellular behavior

Central Question:

How do local cellular interactions generate tissue-scale dynamics?

---

## 3. Cell Patterning and Sorting

Focus:

* Cell sorting
* Tissue patterning
* Differential adhesion
* Collective organization
* Signaling-mechanics feedback

Core Narrative:

Multicellular patterns emerge from the coupled dynamics of cell state, mechanics, signaling, and motion.

Patterning is a dynamical self-organization process rather than a static equilibrium problem.

Key Questions:

* How do cell states and spatial positions co-evolve?
* How are signaling and mechanics coupled?
* What principles govern robust multicellular organization?

---

## 4. Scientific Machine Learning

Focus:

* Imaging
* Cell state inference
* Dynamical systems
* Representation learning
* Predictive modeling

Core Philosophy:

Machine learning should identify interpretable state variables and mechanisms rather than act as a black-box predictor.

Goal:

Bridge high-dimensional biological measurements and mechanistic models.

---

## 5. Morphogenesis

Highest-level scientific theme.

Not simply another category.

Morphogenesis is the unifying scientific problem connecting all projects.

Core Question:

How do multicellular systems generate biological form?

Sub-themes:

* Growth
* Patterning
* Mechanics
* Collective dynamics
* Cell-state transitions

---

# Repository Structure

```text
ExplanatoryModeling/
│
├── AGENTS.md
│
├── Research-OS/                  (execution and planning)
│   ├── projects/                 (CellDynamics, CellShape, CellSorting, LumenoidGrowth)
│   ├── dashboard/
│   ├── manuscripts/
│   └── reviews/
│
└── Literature/                   (scientific knowledge)
    ├── <paper PDFs at top level>
    ├── LumenoidFormation/
    ├── metadata/
    └── outputs/
```

`Research-OS/` and `Literature/` are siblings under `ExplanatoryModeling/`.

Research-OS contains execution and planning.

Literature contains scientific knowledge.

---

# Literature Philosophy

Do NOT organize literature by folders corresponding to themes.

A paper may belong to multiple themes.

Instead use:

* the paper-to-theme matrix (`Literature/outputs/paper_to_theme_matrix.xlsx`)
* per-paper metadata files (`Literature/metadata/`)

---

# Codex Responsibilities

Codex acts as a research chief-of-staff.

Responsibilities:

## Literature

* Classify papers
* Maintain the paper-to-theme matrix
* Identify emerging concepts

## Projects

* Update status.md
* Update hypotheses.md
* Update roadmap.md
* Update story.md

## Manuscripts

* Track progress
* Identify weaknesses
* Identify reviewer risks
* Suggest missing analyses

## Portfolio

* Identify overlap between projects
* Detect emerging themes
* Suggest opportunities for integration

---

# Weekly Review Procedure

When asked to perform a weekly review:

1. Review all project folders.
2. Review new literature.
3. Review manuscript status.
4. Update project status files.
5. Update hypothesis files.
6. Update dashboard.
7. Identify highest-priority scientific opportunities.
8. Identify highest-priority scientific risks.
9. Generate a weekly portfolio summary.

---

# Scientific Modeling Philosophy

Prioritize:

* Mechanistic understanding
* Explanatory models
* Dynamical systems
* Physical principles
* Predictive theories

Avoid:

* Purely descriptive summaries
* Black-box interpretations
* Literature regurgitation

Always seek:

* organizing principles
* hidden assumptions
* mechanistic hypotheses
* connections across projects

---

# Preferred Output Style

When generating project narratives:

* Focus on scientific questions.
* Focus on mechanisms.
* Focus on conceptual frameworks.
* Avoid paper-by-paper summaries.
* Avoid excessive detail unless requested.

The goal is to build a coherent scientific program rather than a collection of disconnected projects.
