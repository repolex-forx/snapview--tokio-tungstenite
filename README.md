# Repolex Knowledge Graph of snapview/tokio-tungstenite

RDF knowledge graph data for [snapview/tokio-tungstenite](https://github.com/snapview/tokio-tungstenite), parsed by [repolex](https://repolex.ai).

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
rlex download snapview/tokio-tungstenite
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 4994a078037a18a9347b8cf49291a5031d63d9e0
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 4994a078037a18a9347b8cf49291a5031d63d9e0.nq.gz
│   └── repolex
│       └── 4994a078037a18a9347b8cf49291a5031d63d9e0
│           └── chunk-001.nq.gz
├── blob
│   ├── 0542b0dc71e5459a4c3231b0a55e6076589b926f.nq.gz
│   ├── 05a737575e9f0bd6c587f6916560f50f410712df.nq.gz
│   ├── 0c9d0486b247aac0d6622e0a8c56fdc8bdb1baa0.nq.gz
│   ├── 17fbd1f95f3738cd6f4fa75c223432f45a82a6c5.nq.gz
│   ├── 288aeaa509136b2a97ea8d5824930e02f2d1b298.nq.gz
│   ├── 2c36a0428d5c0790397506f7f1a8b9edd0c3df59.nq.gz
│   ├── 2d9f0849a25c39fcd86adec68bda3435cf114164.nq.gz
│   ├── 3091627a08b9a729fe209d934d18ba76664ebb24.nq.gz
│   ├── 4371c828a377c48782353377f6bf768987c18d52.nq.gz
│   ├── 4bf5242e2dd870f2a6ca6e8e54154cff018e0bee.nq.gz
│   ├── 5880871c18e9148a492dd631e3743eb0addad9f1.nq.gz
│   ├── 603b0f10cd95967ffdd2b8c5e164f32b855eef48.nq.gz
│   ├── 67985c7d1cb680cc4b6881b1cc37ff767690b7c3.nq.gz
│   ├── 86676b25eef6c791808fa76ba40708444e063fee.nq.gz
│   ├── 8b1ac7bbf051ec35aa0082af4518d5383c0e1baf.nq.gz
│   ├── 8d4fbff2b04f06e0ca699c42b6ecef75dc979489.nq.gz
│   ├── 989349a9708a6fbf35f14f665f7c7f0103b6863f.nq.gz
│   ├── 9ad9e67bafe883bad8193bbbc2752012bca649aa.nq.gz
│   ├── 9bfad300845d00755743344edc8442d4c236ccb4.nq.gz
│   ├── a7b879547aebcae08fa92c9127b0fa9fa333a038.nq.gz
│   ├── a9d37c560c6ab8d4afbf47eda643e8c42e857716.nq.gz
│   ├── aa51276960a061f2769e958317977399c6c78325.nq.gz
│   ├── b0bb00a12df2462151768e95f15d86ab1e5464c1.nq.gz
│   ├── daaa2395e38619846ba2b61a4afa0b8a4aa7998d.nq.gz
│   ├── e636c5bafe8a282bb46a169ed735e082e01b5a8a.nq.gz
│   └── f8b729f6f083b808ff8c437778f1ea4e7f3c7b1b.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 4994a078037a18a9347b8cf49291a5031d63d9e0.nq.gz
├── filetree
│   └── 4994a078037a18a9347b8cf49291a5031d63d9e0.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 36 files
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

[snapview/tokio-tungstenite](https://github.com/snapview/tokio-tungstenite)

---
*Parsed on 2026-11-22 by [repolex](https://repolex.ai)*
