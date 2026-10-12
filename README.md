# Repolex Knowledge Graph of twisted/constantly

RDF knowledge graph data for [twisted/constantly](https://github.com/twisted/constantly), parsed by [repolex](https://repolex.ai).

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
rlex download twisted/constantly
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── c0ca511f6f74b8793c2dd984b0ed202ad0f50558
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── c0ca511f6f74b8793c2dd984b0ed202ad0f50558
│           └── chunk-001.nq.gz
├── blob
│   ├── 2684131b571a26865dc4f92d647c440f14bdade5.nq.gz
│   ├── 39a505bf48af820b37a1a38698414c316214f6e7.nq.gz
│   ├── 445d5b485e85131d79e329baed70331c0ab962ab.nq.gz
│   ├── 4ac63d0e4f0fe3b38a82d7258691544f679fd0e7.nq.gz
│   ├── 4b97c3c83cf0407f99d17cb43e372d36ec3034f1.nq.gz
│   ├── 52899bc63cb6e8a63c5dde5ef88c2071654492fa.nq.gz
│   ├── 55752e3118454ab1b0807eaa496c60ba3bd5a4bf.nq.gz
│   ├── 62e514a966a71961d2dfb15f7a63da19a08d9469.nq.gz
│   ├── 7a67d7096eda6873bebab776a9e7127561a0f45f.nq.gz
│   ├── 7ea1bd2a649f2fe2dfa0d8180422def21051b0b5.nq.gz
│   ├── 989e5d2a5137d6218fb2fe7b35a192f46374c9d1.nq.gz
│   ├── c5a06230c97340bff7e2ee80471247313156c815.nq.gz
│   ├── d31b3df110590858f55eee7f115a5a88ac49b64d.nq.gz
│   ├── d4849e47b3e0629cf7bbd02305ad6ec45db92283.nq.gz
│   ├── dc3d42b0dce40409824da5de7a6f7e46ef0eaeb1.nq.gz
│   ├── e270fcb6404e7dd04fa11ed8b3b48ef5f2480a35.nq.gz
│   ├── e614953ccdcb7f9294ba9040c703e63fac37aa45.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ec3f3a5ccf932cd328fcd2d7b53fc78c1b140126.nq.gz
│   ├── ed8adf3d3d0fa85e68f90dbb218ed622e699f15b.nq.gz
│   ├── f0c477e6ef283263e55dfe80f50d32815d8be2c1.nq.gz
│   ├── f340e0401ae3ee1d3dc9d1c6c83934b3d878bc27.nq.gz
│   ├── f911f2eee1ddfa2cd7772e777ab35f87463b7680.nq.gz
│   └── fdd945a4b9902cd14b4190da43d707834fb4778f.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── c0ca511f6f74b8793c2dd984b0ed202ad0f50558.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 32 files
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

[twisted/constantly](https://github.com/twisted/constantly)

---
*Parsed on 2026-10-12 by [repolex](https://repolex.ai)*
