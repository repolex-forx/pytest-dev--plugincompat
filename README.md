# Repolex Knowledge Graph of pytest-dev/plugincompat

RDF knowledge graph data for [pytest-dev/plugincompat](https://github.com/pytest-dev/plugincompat), parsed by [repolex](https://repolex.ai).

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
rlex download pytest-dev/plugincompat
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 148b892c7969f9d8e7800af0dd259a78bd70a438
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 148b892c7969f9d8e7800af0dd259a78bd70a438
│           └── chunk-001.nq.gz
├── blob
│   ├── 031fb9971e549b332684f2e207453cda1bb81b0b.nq.gz
│   ├── 04cc43d1a7d5113ad8f7cde0583aa288b72de077.nq.gz
│   ├── 10fcbc65092b98f2b12dd5c1546af3b428fa6f23.nq.gz
│   ├── 1915e5d4224c8630475a9ce905cc845226275565.nq.gz
│   ├── 2368960080b2cdf5c5451f6cdd35780865b1ba76.nq.gz
│   ├── 2a9acf13daa95e85642ea255d3e3bd1ef8252804.nq.gz
│   ├── 2c9dd083414e9bb450f80d4c29fb0b1c48ba2be4.nq.gz
│   ├── 3ac3f245cb3d2686ebec2602df98b73025b33b51.nq.gz
│   ├── 3ee3d017d7243e9d594e539b19285cf3d9157e45.nq.gz
│   ├── 4518eabf9b5c2e3abff1095fd2ad2d3a510b439c.nq.gz
│   ├── 4b2f7ee3a0537151752c912b72456a9a41ef6dfc.nq.gz
│   ├── 622c9e71f6eb7f193393a01de584e56ce8b5d77f.nq.gz
│   ├── 722ad18408df41453a695ab695b0e64bc326a2b6.nq.gz
│   ├── 77395755d4b9405e2d514b6fba1a49abc9933ded.nq.gz
│   ├── 78620c472c9d799a14ccb02a0233f4669b3bcdcb.nq.gz
│   ├── 992fdb9a2032be5b82a550c3569c1e8937d7496a.nq.gz
│   ├── 997599391756ef56e79008da8f1d8ee22b450baa.nq.gz
│   ├── a08bb997c783efa751fa97d44cb4c7ffce7a6115.nq.gz
│   ├── a184e925aaf88cf97843337dbcf62f43e5262135.nq.gz
│   ├── a27beb3cc490bd1280c680f34eecb455ee8cd6aa.nq.gz
│   ├── a3f78d2a413fcb26fa8b16fe02970aa8d669e5d0.nq.gz
│   ├── aa4949aa1ccb9aec24c352cb132cd0f86ebe787c.nq.gz
│   ├── b261154f01d8705fe68d48493afc17b185e8bc5a.nq.gz
│   ├── b981bb0ffbae5e56d2566ea4d629c02346b1a8ae.nq.gz
│   ├── bf36119628d265306cdd7bceb5dd8f51face8f8c.nq.gz
│   ├── c498150de53cbcd8e2dbb6ca380961bf82963203.nq.gz
│   ├── d00077c6fdb38096b6094e34d1878113773b3659.nq.gz
│   ├── d03d9eed9c71a19512ca2507c9d78f478bf00443.nq.gz
│   ├── d878f59f5ac38ea61ad769ec9905ef3e27c285e0.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f34676fc18bef6b66fd91e42cdcf6fd029e798f9.nq.gz
│   ├── f77ddc90ca4817020018fe15db3a8b9afae8a97b.nq.gz
│   ├── fd57cb0b1674cf1e9ac58b5af3879125165e6bcf.nq.gz
│   ├── ffc86033cc33416a8059db967137e6b9f98137cb.nq.gz
│   └── ffd813af4e3565bf5b2518aa8bcd568e8f630796.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 148b892c7969f9d8e7800af0dd259a78bd70a438.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 43 files
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

[pytest-dev/plugincompat](https://github.com/pytest-dev/plugincompat)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
