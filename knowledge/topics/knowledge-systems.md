---
title: "Knowledge Systems"
created: 2026-03-28
updated: 2026-03-28
concepts:
  - knowledge-graphs
  - concept-mapping
  - personal-knowledge-management
---

# Knowledge Systems

## Overview

This topic covers the theory and practice of organizing, connecting, and visualizing knowledge — the foundational ideas behind this agency's own knowledge base.

## Key Concepts

- [Knowledge Graphs](../concepts/knowledge-graphs.md) — Structured representations of interconnected concepts
- [Concept Mapping](../concepts/concept-mapping.md) — Visual technique for displaying knowledge relationships
- [Personal Knowledge Management](../concepts/personal-knowledge-management.md) — The practice of building and maintaining a personal knowledge repository

## Narrative

These three concepts form a natural stack. **Knowledge graphs** provide the data model — nodes and edges representing concepts and their relationships. **Concept mapping** provides the visual layer — a way for humans to see and interact with the graph. **Personal knowledge management** provides the workflow — the habits and processes for continuously growing the graph.

This agency implements all three: the `knowledge/graph.yaml` file is the knowledge graph, the visual map (to be built) renders it as a concept map, and the `inbox/` → `knowledge/` pipeline is the PKM workflow.
