# Repolex Knowledge Graph of modal-labs/pytest-markdown-docs

RDF knowledge graph data for [modal-labs/pytest-markdown-docs](https://github.com/modal-labs/pytest-markdown-docs), parsed by [repolex](https://repolex.ai).

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
rlex download modal-labs/pytest-markdown-docs
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── a11a013c89f726993fcae52718d23136bbd12767
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── a11a013c89f726993fcae52718d23136bbd12767
│           └── chunk-001.nq.gz
├── blob
│   ├── 0c140bd2ebbb4be71a6ace2cf377fdc5f551c35e.nq.gz
│   ├── 118f8d940bdbda7ff41278c427b4038ab18ad7e0.nq.gz
│   ├── 180d2745f531cc8eefef2a1e785b87f1af1d7e68.nq.gz
│   ├── 1c4ecdca4ac63fe3f59ba472467b593f98caf9cc.nq.gz
│   ├── 1d71b738c564a8ba26c84afcd9f452273abdd83a.nq.gz
│   ├── 218b9e299156097317584e201cb4a8070459a3b2.nq.gz
│   ├── 272d212ac4ce58b89ae42ab9d77c392d6d6c1f00.nq.gz
│   ├── 34a9f0efe095732c711fd33bdcac0d245fc5b519.nq.gz
│   ├── 5207abc14f9c29738599d34dbc7bb90c6c8fc9a2.nq.gz
│   ├── 57446e25d7cdf7fb7c7d4ec5814c39aac376b2bf.nq.gz
│   ├── 58a89039187d63d442e6ec17d49eedc50722d353.nq.gz
│   ├── 5fbbe2fae9e26ee8fa9d82a9869a9a6675ecc701.nq.gz
│   ├── 6f758548145b6982237cae4d3246bcfd29ac4ca8.nq.gz
│   ├── 8ab5ec1c830675d68f26c41ef97c823eaa195af0.nq.gz
│   ├── aaae02abc811b54a859f64aa495c804b2f411506.nq.gz
│   ├── b5fb4d7229773ddc8018c1a25bbcadad4fa3cf61.nq.gz
│   ├── b6e47617de110dea7ca47e087ff1347cc2646eda.nq.gz
│   ├── cec14ecab1e1f722b51559c4336cbc99fbff6568.nq.gz
│   ├── e03652f7eabea6588e64290cc4615e1a93bd35bd.nq.gz
│   ├── e1378c5234b610981330d434c0547f30d0456736.nq.gz
│   └── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── a11a013c89f726993fcae52718d23136bbd12767.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 29 files
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

[modal-labs/pytest-markdown-docs](https://github.com/modal-labs/pytest-markdown-docs)

---
*Parsed on 2026-11-08 by [repolex](https://repolex.ai)*
