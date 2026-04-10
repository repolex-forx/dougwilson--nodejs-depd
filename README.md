# Repolex Knowledge Graph of dougwilson/nodejs-depd

RDF knowledge graph data for [dougwilson/nodejs-depd](https://github.com/dougwilson/nodejs-depd), parsed by [repolex](https://repolex.ai).

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
lexq download dougwilson/nodejs-depd
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 6d59c85d093092e65ec77033576417d743079fa0
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 6d59c85d093092e65ec77033576417d743079fa0.nq.gz
│   └── repolex
│       └── 6d59c85d093092e65ec77033576417d743079fa0
│           └── chunk-001.nq.gz
├── blob
│   ├── 043d1ca28403a9460a22fcd403b559b90244458f.nq.gz
│   ├── 0fa6951f088d91e437ea25699ee715cc6cf462a0.nq.gz
│   ├── 10279b6c9013289fe3e1268a0ee7547efa05340f.nq.gz
│   ├── 125e412bfde0db7858ad93a1c3a6626899c418ea.nq.gz
│   ├── 15523ca9331e0d3615818d64e7c2748fc58d6179.nq.gz
│   ├── 17cf91a6379226f21a67ed3ee75c8ded52a381eb.nq.gz
│   ├── 1bf2fcfdeffc984e5ad792eec08744c29d4a4590.nq.gz
│   ├── 248de7af2bd16cc7f2b4d8017bbeb9e7a0b2ccd6.nq.gz
│   ├── 2cb6c2fb07975729b344d2806167716c016a6bce.nq.gz
│   ├── 34f8e988be4db9f77d18a6be8108cd8c56f6138a.nq.gz
│   ├── 3857e199184a0a3f0d921e740525278af0f86ff3.nq.gz
│   ├── 5610e2f6ba6deed4ce8f660e9fbb843797e7bc59.nq.gz
│   ├── 6177b7d0dd4c39a4068b580a5b61d2fc809ae862.nq.gz
│   ├── 62562b74a3b5a79e82ca417b02e0f597d85f5e2f.nq.gz
│   ├── 6be45cc20b33f20dcdc580b9709f1a4a20bb87a1.nq.gz
│   ├── 8ba893764f4f96a7848e7f28ddb1d349051be732.nq.gz
│   ├── 9364b3af6293f5d811f648a1c2b39b62945244e8.nq.gz
│   ├── 9808c3b2b6602da61eb4afcb4caf33368e3e2bd4.nq.gz
│   ├── 9be913fa2f7577a1f62a79d93f490934f5dbc12a.nq.gz
│   ├── a7a530c245b62df36336be0567c6cebf56e3a668.nq.gz
│   ├── aa6f6fb886f891f9b95353c278a0de4776a34ab1.nq.gz
│   ├── bc0cf797a136de30e77318d00c7295b617928c51.nq.gz
│   ├── c6a7986ce8fe668508ecdfc7540228efbc9cffd4.nq.gz
│   ├── cd9ebaaa9963f794167f74e00a37d9ceb42e7b91.nq.gz
│   ├── d02d0a4ad7d94cf1f423501975cdd9788da91b3d.nq.gz
│   ├── d8d074f28424f6187c60b4ac0e4fb68bdfa69970.nq.gz
│   ├── e7ecfc93c3c8bbb828a4747d812ca0cea4871c38.nq.gz
│   ├── ee611488c58b3e9ed5936145f16b97a6a1028076.nq.gz
│   └── f2642c74fdce0f09be36503d03ce3fc19d6979e0.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 6d59c85d093092e65ec77033576417d743079fa0.nq.gz
├── filetree
│   └── 6d59c85d093092e65ec77033576417d743079fa0.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 39 files
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

[dougwilson/nodejs-depd](https://github.com/dougwilson/nodejs-depd)

---
*Parsed on 2026-04-10 by [repolex](https://repolex.ai)*
