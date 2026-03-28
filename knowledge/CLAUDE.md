# Knowledge Base Operations

This directory is the agency's shared knowledge base. It stores interconnected concepts as markdown files with YAML frontmatter, organized into topics, and indexed in a central graph.

## Structure

```
knowledge/
├── graph.yaml          # Centralized relationship map (the visual map data)
├── _index.md           # Auto-generated table of contents
├── concepts/           # One .md file per concept
├── topics/             # Higher-level groupings
└── references/         # External sources and citations
```

## Creating a Concept

1. Create a new file in `concepts/` using the slug as filename (e.g., `distributed-systems.md`)
2. Use the template at `concepts/_template.md` for the structure
3. Fill in all frontmatter fields — especially `tags`, `related`, and `topic`
4. Write the body content (Summary, Detail, Connections, Open Questions)
5. Add a node entry to `graph.yaml`
6. Add any edges to `graph.yaml` connecting it to related concepts
7. Update the relevant topic file's concept list
8. Update `_index.md`

## Creating a Topic

1. Create a new file in `topics/` using the slug as filename
2. Use the template at `topics/_template.md`
3. List all member concepts in the frontmatter
4. Write an overview narrative explaining how the concepts fit together
5. Add the topic to `graph.yaml` under `topics:`

## Creating a Reference

1. Create a new file in `references/` using a descriptive slug
2. Use the template at `references/_template.md`
3. Include the source URL, author, date, and a summary
4. Link it from any concept that cites it (via the `sources` field)

## Updating the Graph

`graph.yaml` is the centralized index. It must be kept in sync with the concept files.

**When adding a concept**: Add a node entry with title, topic, and tags.
**When connecting concepts**: Add an edge with `from`, `to`, `type`, and optional `note`.
**When removing a concept**: Remove its node and all edges referencing it.

### Edge Types

| Type | Meaning |
|------|---------|
| `relates-to` | General association |
| `depends-on` | A requires B to make sense |
| `contradicts` | A and B are in tension |
| `extends` | A builds on or elaborates B |
| `part-of` | A is a component or subset of B |
| `example-of` | A is a concrete instance of B |
| `inspires` | A led to the creation of B |

## Searching the Knowledge Base

- **By topic**: Browse `topics/` for high-level categories
- **By tag**: Search concept frontmatter for matching `tags` values
- **By relationship**: Consult `graph.yaml` edges to find connected concepts
- **By content**: Full-text search across `concepts/` files
- **By index**: Check `_index.md` for an alphabetical listing

## Merging vs. Creating

Before creating a new concept, check if it already exists:
- Search by title (exact and fuzzy)
- Search by tags that overlap
- Check `graph.yaml` nodes

If a close match exists, **merge** the new information into the existing concept rather than creating a duplicate. Update the `updated` date when merging.
