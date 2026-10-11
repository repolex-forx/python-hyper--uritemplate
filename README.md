# Repolex Knowledge Graph of python-hyper/uritemplate

RDF knowledge graph data for [python-hyper/uritemplate](https://github.com/python-hyper/uritemplate), parsed by [repolex](https://repolex.ai).

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
rlex download python-hyper/uritemplate
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 4a38e9f6e78a1b8888e7699dd19f37d1d09570f3
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 4a38e9f6e78a1b8888e7699dd19f37d1d09570f3
│           └── chunk-001.nq.gz
├── blob
│   ├── 01c8ecae78bda8b8b6209ac35a34062f73f73a48.nq.gz
│   ├── 045100d95db5dfc44b31b3fa7abb06ad6037c7c2.nq.gz
│   ├── 09ac18a6df3c586e6dca2f7e0357efe536b1ec57.nq.gz
│   ├── 0fccdb3af8e6af3ad00460b04f6a0de4cd186c6e.nq.gz
│   ├── 17b73e7175e5a71fccea7172d95e795e5822c29b.nq.gz
│   ├── 1f7993c23166570fe28482bf84600c36d3ea9022.nq.gz
│   ├── 1fa3f4b4aa1d23784d89f7dd35ba915a826dd9a7.nq.gz
│   ├── 2573a7f17376af537e08f46c79faeae3f6f74459.nq.gz
│   ├── 2581f4d84c9f3da391a86d53d6625e75678e8e9c.nq.gz
│   ├── 2decd8cd6400b04ead8789b5b0efabcaaf3eef30.nq.gz
│   ├── 368696c81fa98c61056438660d993a0e7788d226.nq.gz
│   ├── 3e96f4a4c044577d0ed62e7488c9db4cd4f51369.nq.gz
│   ├── 41c87e7cf26b0f948798e79b1b882a0940fbcb32.nq.gz
│   ├── 552a6bf07e98ab5dbef609a386d7a2aa0352ef57.nq.gz
│   ├── 5c7b5b33df8d626ee1d8aabd3e9fb86c2c6e2a26.nq.gz
│   ├── 5e394eb9a0b1f15e13939031f2de8b73393fc51c.nq.gz
│   ├── 617eb0a15e677a0ccb3f498d24578fed78facc88.nq.gz
│   ├── 652acfa9606cf7647079d1e3cdbb0a1b3a1198f8.nq.gz
│   ├── 6f9a0eb246acd840753dc2ce2583e587e9328b1c.nq.gz
│   ├── 7060b3c98e1b789748860e00ce787da8d4011189.nq.gz
│   ├── 7582f2f047eb7b86af581f90d5956c128b84f0f8.nq.gz
│   ├── 7e79d94e919f6e3073236fe965a4f10f807a1d31.nq.gz
│   ├── 7fbcd49bc3ab8acb2bb5297ba9334928abc8fbc8.nq.gz
│   ├── b22774767876685b6efc2e478c57bde886530ef5.nq.gz
│   ├── b574330d345404a3cba6ccaf8775f5674bdb9102.nq.gz
│   ├── b5aaf872e2dcd103b420dea6db995531a770bc7f.nq.gz
│   ├── b908cbe55cb344569d32de1dfc10ca7323828dc5.nq.gz
│   ├── cb06598492391c1b8989a3e46140b865c0d7cd94.nq.gz
│   ├── d4975102cb23d0ff10898df860eb0c629b01c449.nq.gz
│   ├── d60778d3787088cff2918fb554aa163e4d3cdbb9.nq.gz
│   ├── d645695673349e3947e8e5ae42332d0ac3164cd7.nq.gz
│   ├── d956b6bdb656757766c50ccfbcc35f8b72372d08.nq.gz
│   ├── dd7cd1a5867d472fdae1cd065b7586c2f17a22c2.nq.gz
│   ├── df27d957eff50bbdc4d82b6e073e32858e040fc0.nq.gz
│   ├── dfe19f54d39435c49353835870e4432850d2b721.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── eadb1d474be788294fb5a0ec2fac4dc0dd39a5fa.nq.gz
│   └── f545e0f037052fb40efcd254dff7409a202e7af5.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 4a38e9f6e78a1b8888e7699dd19f37d1d09570f3.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 46 files
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

[python-hyper/uritemplate](https://github.com/python-hyper/uritemplate)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
