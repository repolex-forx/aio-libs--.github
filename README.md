# Repolex Knowledge Graph of aio-libs/.github

RDF knowledge graph data for [aio-libs/.github](https://github.com/aio-libs/.github), parsed by [repolex](https://repolex.ai).

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
rlex download aio-libs/.github
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── df5def2d78949a4ff7150de6fbd5aa27eb45b090
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── df5def2d78949a4ff7150de6fbd5aa27eb45b090
│           └── chunk-001.nq.gz
├── blob
│   ├── 1a00de9ef6311eba2e0b2ae654e5258924d43ba7.nq.gz
│   ├── 2f4fed4bcb01258b6ad12864a3ccaeed2df9cda8.nq.gz
│   ├── 4e66c731a5c3d51e48796fc4228e20c3c21656f5.nq.gz
│   ├── 5230c83ce44dce0c4a17d40e80dfc1295638beff.nq.gz
│   ├── 550c3b2b0bdf84301591860020a5191d864f0a94.nq.gz
│   ├── 6c9ac2fe66e87fc43b2cbc2f5099bd0bb4530c72.nq.gz
│   ├── 70e1010d42675fafcf8f06ee2fa4a56d90d564da.nq.gz
│   ├── 7410518a44dd35b970a8b82d95ec742954a8cc45.nq.gz
│   ├── 82938a5342082e772c2dc8a8aa0fccf9cece3ba1.nq.gz
│   ├── ad4552c21f67d0e38bfde9dd8149f5b9ea570f6f.nq.gz
│   ├── af376dee5ad0fae736fe35bf66e49bcc3f707722.nq.gz
│   ├── b132ffe966a3d9244ef57bde9ef33f62b021b97c.nq.gz
│   ├── ba2c34e58dc81a0c045df8407ea6920e9576fb05.nq.gz
│   ├── cc2eb115e3fdef902a3a473f664ca27f3586715b.nq.gz
│   ├── d850cf6bf537831efa3705a95735c713e9ce6c64.nq.gz
│   ├── e11f63bea2c6410c03400b306a9ccb843050378e.nq.gz
│   ├── ecb97832992d05681eccd7ef0776c488da629b37.nq.gz
│   └── f1188eaf1027acb2dc7488cea5477a7d5059940e.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── df5def2d78949a4ff7150de6fbd5aa27eb45b090.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 25 files
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

[aio-libs/.github](https://github.com/aio-libs/.github)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
