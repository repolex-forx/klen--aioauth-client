# Repolex Knowledge Graph of klen/aioauth-client

RDF knowledge graph data for [klen/aioauth-client](https://github.com/klen/aioauth-client), parsed by [repolex](https://repolex.ai).

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
rlex download klen/aioauth-client
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 6b4c3d6383837c1c704a01a4003232d9d3ef19bb
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 6b4c3d6383837c1c704a01a4003232d9d3ef19bb
│           └── chunk-001.nq.gz
├── blob
│   ├── 003afa2c8c4212ed88fa63330f8aaf8281ee99f2.nq.gz
│   ├── 0b2e907c89333ea1b1c45cf476f5afdd63c69c08.nq.gz
│   ├── 15d85a76fb5021b59583a8d55267df2bb9aa5d4e.nq.gz
│   ├── 18589cef6c0c64558345c4d5b49e1093ca0fb50c.nq.gz
│   ├── 1e8d62cf8a356a16ca3af0c526de74d63b21f46c.nq.gz
│   ├── 402d6a9222a24973483dc325193a03c9156949ad.nq.gz
│   ├── 4a060cc8ce501e4a5b9157c2f5ed52285582dd60.nq.gz
│   ├── 4d2f73c027732dfe0860a3c52ea37aa8d28d497f.nq.gz
│   ├── 5c84b70a4c069fcdf756cdcdb82e09c2efb3e628.nq.gz
│   ├── 5d18ad97e8d4342a1e30a94f0d39d546180204e3.nq.gz
│   ├── 61c5ed0cf82923c7659c779b9999b7c16def70d3.nq.gz
│   ├── 756551554c2115f500f48f82ad94d1960f745f51.nq.gz
│   ├── 823ef441b3d1878c3b850d01ea95023ebec3c8aa.nq.gz
│   ├── 94f0e9a8773efb69516416c508352aec37de86f1.nq.gz
│   ├── 9539ddfe523d2639eda64b18a56bfd04f5c92f60.nq.gz
│   ├── a13fc7d1f922e28e6539a7a0243b9e605ab51c39.nq.gz
│   ├── a95f6a89e6b46e5ec65798414e4e8586a54a4b9b.nq.gz
│   ├── abc82417eb1fb25c1aba1e0b7a65acf0eb1baf4d.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f6b2f73480bd7b92696ad35121246d481a964b6b.nq.gz
│   ├── f920e74fce38bd8a095521a954b9ddd8df1aca24.nq.gz
│   └── fd06482d03719200bfcc794656c3f96a429f5958.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 6b4c3d6383837c1c704a01a4003232d9d3ef19bb.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 30 files
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

[klen/aioauth-client](https://github.com/klen/aioauth-client)

---
*Parsed on 2026-10-20 by [repolex](https://repolex.ai)*
