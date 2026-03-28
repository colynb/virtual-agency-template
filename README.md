# Project Knowledge Agency

A file-based virtual agency for organizing project knowledge using AI agents.

## What Is This?

This repository is a **workspace** structured as an agency. You (the agency owner) direct AI agents to research, design, build, and organize knowledge. The folder structure itself defines the organization — no app server, no dependencies, just files that Claude Code reads and acts on.

## The Team

| Agent | Role | What They Do |
|-------|------|-------------|
| **Ada** | Orchestrator | Your main contact. Breaks down tasks, delegates, tracks progress. |
| **Soren** | Research | Investigates topics, writes knowledge base entries, processes your inbox. |
| **Maya** | Design | Designs systems, architectures, and information structures. |
| **Kit** | Development | Builds scripts, automation, and implements designs. |

## Quick Start

**Talk to Ada** (default when you open the repo in Claude Code):
> "I need to organize my notes on distributed systems."

**Direct a specific agent**:
> "Have Soren research the CAP theorem and add it to the knowledge base."

**Drop a note in the inbox**:
> Create a file in `inbox/` with your raw thoughts, then say "Process the inbox."

**Hire a new agent**:
> "Hire a new agent called Rex for quality assurance."
> (Ada copies the template and customizes it.)

## Structure

```
.
├── CLAUDE.md              # Agency brain — routing, conventions, agent roster
├── agents/                # Agent personas and workspaces
│   ├── ada/               # Orchestrator
│   ├── soren/             # Research
│   ├── maya/              # Design
│   ├── kit/               # Development
│   └── _template/         # For hiring new agents
├── knowledge/             # Interconnected concept base
│   ├── graph.yaml         # Visual map data (nodes + edges)
│   ├── concepts/          # One file per concept
│   ├── topics/            # Higher-level groupings
│   └── references/        # External sources
├── inbox/                 # Drop raw notes here for processing
├── projects/              # Active project workspaces
└── logs/                  # Decision log + activity feed
```

## The Knowledge Base

Knowledge is stored as markdown files with YAML frontmatter in `knowledge/concepts/`. Each concept declares its tags, related concepts, and topic membership. Relationships between concepts are also tracked in `knowledge/graph.yaml` — a centralized adjacency list that maps how everything connects.

This graph is the data that would power a visual concept map. Concepts are nodes, relationships are labeled edges.

## The Inbox

Drop any file into `inbox/` — raw notes, bullet points, links, stream of consciousness. Say "process the inbox" and Soren will extract concepts, file them into the knowledge base, connect them to existing concepts, and archive the original.
