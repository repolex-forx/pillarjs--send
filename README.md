# Repolex Knowledge Graph of pillarjs/send

RDF knowledge graph data for [pillarjs/send](https://github.com/pillarjs/send), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [lexq](https://github.com/repolex-ai/lexq) query tool using [uv](https://docs.astral.sh/uv/getting-started/installation/).

If you have uv installed, just copy/paste this into your terminal:

```bash
uv tool install git+https://github.com/repolex-ai/lexq
```

This installs lexq onto your system, in your user context. Verify the install:

```bash
lexq --help
```

**lexq is designed to be used primarily by LLMs in a terminal.** Start up your favorite LLM and ask it to use the lexq tool. It's that easy!

To load this repo's data:

```bash
lexq download pillarjs/send
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 91c184e649942d67d7beaf34f46b22ac603198bc
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 91c184e649942d67d7beaf34f46b22ac603198bc.nq.gz
│   └── repolex
│       └── 91c184e649942d67d7beaf34f46b22ac603198bc
│           └── chunk-001.nq.gz
├── blob
│   ├── 050e4b91b71ecc267e36de7a1191bcaff6e266f1.nq.gz
│   ├── 0e064f47bff27efdbdb6abc4063f834b7ea6a0b5.nq.gz
│   ├── 1332a99136df80a6b2f25c931ce81c5f04e0f8f8.nq.gz
│   ├── 2b31011cf9de6c82d52dc386cd7d1a9be83188c1.nq.gz
│   ├── 46b48f7b0733cdfa849734a92b51bfc213a2ee49.nq.gz
│   ├── 531b88511457195a712473b95dbc23374d383742.nq.gz
│   ├── 536aca34dbae6b2b8af26bebdcba83543c9546f0.nq.gz
│   ├── 546c717e0ced3651e81b5211d55bb0af53df32db.nq.gz
│   ├── 62562b74a3b5a79e82ca417b02e0f597d85f5e2f.nq.gz
│   ├── 6256eb58895524051ca8c6fd5911e19fa5e5c08a.nq.gz
│   ├── 789c47ab13a523803dd653520c787a93cb98ca2c.nq.gz
│   ├── 90a1d60ab71387c42694fa4b6335c37f51255fc2.nq.gz
│   ├── 9808c3b2b6602da61eb4afcb4caf33368e3e2bd4.nq.gz
│   ├── b6ea1c1fd44ff6f4af6a8e4e5d4793004b9e8524.nq.gz
│   ├── c58268ad26e98c128bf936c8fd32c63453d23f82.nq.gz
│   ├── cbad4bfbdd8fc4214a9385a67c17a886b26da565.nq.gz
│   ├── d97c5eada5d8c52079031eef0107a4430a9617c5.nq.gz
│   ├── e2e107ac61ac259b87c544f6e7a4eb03422c6c21.nq.gz
│   ├── e4f03fba61b0fabdebe763c8ffa6db3fc383ffe9.nq.gz
│   ├── f15b98e249d653f23d7e121037bde0eae1817582.nq.gz
│   ├── f492b6f5d00653538e28e07fc050ecb4f5c34be6.nq.gz
│   ├── f6ea0495187600e7b2288c8ac19c5886383a4632.nq.gz
│   └── fa66f37ff2170afebb34dd2da5a1ba69d3657270.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 91c184e649942d67d7beaf34f46b22ac603198bc.nq.gz
├── filetree
│   └── 91c184e649942d67d7beaf34f46b22ac603198bc.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 33 files
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

## Source repository

[pillarjs/send](https://github.com/pillarjs/send)

---
*Parsed on 2026-04-10 by [repolex](https://repolex.ai)*
