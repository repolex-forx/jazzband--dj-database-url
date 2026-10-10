# Repolex Knowledge Graph of jazzband/dj-database-url

RDF knowledge graph data for [jazzband/dj-database-url](https://github.com/jazzband/dj-database-url), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [rlex](https://github.com/repolex-ai/rlex) query tool:

```bash
cargo install --git https://github.com/repolex-ai/rlex
```

Verify the install:

```bash
rlex --help
```

**rlex is designed to be used primarily by LLMs in a terminal.** Start up your favorite AI assistant and ask it to use rlex. It handles the SPARQL — you just ask questions in plain English.

To load this repo's data:

```bash
rlex download jazzband/dj-database-url
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 5656563adbf9194bbe49979569b4f57c4cc39830
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 5656563adbf9194bbe49979569b4f57c4cc39830
│           └── chunk-001.nq.gz
├── blob
│   ├── 00d3cc9c1dcf4ef1fba69c594536e712d71182d6.nq.gz
│   ├── 0b2080596374f131dac9f1939ea94d4d34b29d1f.nq.gz
│   ├── 205288f46bf40f07b7f3ee750581c371cdb114fc.nq.gz
│   ├── 24722aefab001cade01af5959c618028e6b36d1d.nq.gz
│   ├── 2a681bd264bbc64a1ff206bab616e87a145b3565.nq.gz
│   ├── 2bb5a14af2762eece822d279c1f02d32efd77994.nq.gz
│   ├── 3aaf15160fdd8c073080582783ad1207ec9cf598.nq.gz
│   ├── 78e5810b17665c447498b31723d6e85dd60a9fd6.nq.gz
│   ├── 7b49b475f9dafa1d385497220471baf77bb1374c.nq.gz
│   ├── 7fdca495ad4dc0fdcfc77795d5f0d443253063ae.nq.gz
│   ├── 829a22ace1d5d01ee25a2522d3ec8ba0c68576c8.nq.gz
│   ├── b68c12acd32654005ab057d4d42632b0b5e25a87.nq.gz
│   ├── e0d5efab56fb94577e7804603eb6f21f36977cb2.nq.gz
│   └── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 5656563adbf9194bbe49979569b4f57c4cc39830.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 22 files
```

| Directory | What it contains |
|-----------|-----------------|
| `blob/` | Per-file AST graphs, content-addressed by git blob SHA. Each file in the source repo gets its own graph. |
| `aggregate/ast/` | Combined AST graph per parsed commit. Merges all blob graphs for a snapshot of the entire codebase at that point. |
| `aggregate/lsp/` | Language Server Protocol enrichment: resolved symbols, definitions, references, and type information. |
| `aggregate/dataflow/` | Interprocedural data flow edges between functions and modules. |
| `aggregate/repolex/` | Combined graph (AST + LSP + dataflow) per commit. |
| `commit/` | Git commit metadata (author, date, message, parent links). |
| `branch/` | Branch metadata. |
| `tag/` | Tag metadata. |
| `filetree/` | File tree snapshots per commit (which files existed and their blob SHAs). |
| `audit/` | Code architecture and graph audit reports per commit. |

## Source repository

[jazzband/dj-database-url](https://github.com/jazzband/dj-database-url)

---
*Parsed on 2026-10-10 by [repolex](https://repolex.ai)*
