# Repolex Knowledge Graph of samuelcolvin/nextcall

RDF knowledge graph data for [samuelcolvin/nextcall](https://github.com/samuelcolvin/nextcall), parsed by [repolex](https://repolex.ai).

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
rlex download samuelcolvin/nextcall
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 3ef572168c79a54014a8543021c338ce2636170e
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 3ef572168c79a54014a8543021c338ce2636170e
│           └── chunk-001.nq.gz
├── blob
│   ├── 08066000f06720bf28486a7d9f103f2b9e38448c.nq.gz
│   ├── 0ce12693e5dae2a48ae5ed2af0d7028faeadb060.nq.gz
│   ├── 151cacd9fcf743fd6dcd291bb4fab0b8805b522d.nq.gz
│   ├── 239b13166040434741942daaea7761e61338981e.nq.gz
│   ├── 28adf1a6b072c43784df5b993e8f01085311c22c.nq.gz
│   ├── 39c583e936ed9fb4073e1e3b3abe857c1083b5ac.nq.gz
│   ├── 3f48eee86fdd70299ca76bc013931a25c0cec925.nq.gz
│   ├── 40fd201de7af6bd53cc06b09287c051af3ad2a54.nq.gz
│   ├── 4801e9948fd9996a683e8d8d18d509dc951ce752.nq.gz
│   ├── 4baddb90ae2a9cf219b0ea63d7e2ee3d0857906a.nq.gz
│   ├── 5675820a9fd4c2f1b62be20d4f3a9b6ead3af9af.nq.gz
│   ├── 56c13a82217f3d7e4bf84b75e821a190e6597dee.nq.gz
│   ├── 5cbc9421e1cffa7ae8f84fb17c03c4ef9ccff637.nq.gz
│   ├── 5d2f10ab9ddbb77089022a0998358f2110c60fc3.nq.gz
│   ├── 66419e55055e029ba859b07c4fff03b35033a44d.nq.gz
│   ├── 6fb54fa35172fa0d8446439465f3aa83e2856bfb.nq.gz
│   ├── 74d638ab610bee293d5ea40dcf833f48191195a7.nq.gz
│   ├── 75306517965a54731b94dca8bace640e856af115.nq.gz
│   ├── 786dfba64a573119faed475dd28921e1e134b1cc.nq.gz
│   ├── 7c6f2c3dd506890bfb1d2dea65f73ee33a512926.nq.gz
│   ├── 804e16c36de21dcc105c5096e4950f256e92aa54.nq.gz
│   ├── b34f64f6c3c2328b3cc762730bfec5ce0bc025be.nq.gz
│   ├── bbbaa5f99a695285b50106d16f37211cf92a196b.nq.gz
│   ├── c481295028fba0f8dd8ed9ca93583ed8d65a0e5d.nq.gz
│   ├── dc0ce7bdc68664c9d19a0e7627f00791e937854a.nq.gz
│   ├── de9730c5e9747be215921cae70ef7d5c7b0cc147.nq.gz
│   ├── e7d01d73541c7e12e929384fcc25b70b7acf59df.nq.gz
│   ├── eaeb327be1d766e196a1161194fd52c5ce683f8b.nq.gz
│   ├── ef63924a3b63b72fe874fa9d63551d2cfb6512be.nq.gz
│   ├── f62dd684483ab39b435ba0e920b2b9c3b52a4829.nq.gz
│   └── fc62bba95a9f06076025b510edf00d7226ba7462.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 3ef572168c79a54014a8543021c338ce2636170e.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 37 files
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

[samuelcolvin/nextcall](https://github.com/samuelcolvin/nextcall)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
