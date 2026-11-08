# Repolex Knowledge Graph of UKPLab/acl2019-ctest-difficulty-manipulation

RDF knowledge graph data for [UKPLab/acl2019-ctest-difficulty-manipulation](https://github.com/UKPLab/acl2019-ctest-difficulty-manipulation), parsed by [repolex](https://repolex.ai).

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
rlex download UKPLab/acl2019-ctest-difficulty-manipulation
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── ce4f368f8987b1111d92bf03f6b40710827ecf11
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── ce4f368f8987b1111d92bf03f6b40710827ecf11
│           └── chunk-001.nq.gz
├── blob
│   ├── 03a66f537c26ee232778fbe4fc1b25a1232c8558.nq.gz
│   ├── 0cf39dc7eebdb093c52e1e0812ab9f695f63f22e.nq.gz
│   ├── 2136ec3074dcc053f30defc5c8775302ccb2d507.nq.gz
│   ├── 22a6a61eb80bafb80d3604fcd11e0a0293a1dc2a.nq.gz
│   ├── 24270df42f46542807990987dd900f561b96a983.nq.gz
│   ├── 2573f09bad7e25876501f04f71926e5dd3437ce9.nq.gz
│   ├── 29d6f3ed8ff5958f5c1b6693e9544d9ed58b14a4.nq.gz
│   ├── 3e57bd765ab7673cfb3b4fdb22e09a301eb2d43e.nq.gz
│   ├── 3f8e0a0646f7d1fdb89483aa8ba6bf80d0e3ed1e.nq.gz
│   ├── 45f60fd80b8b9ec9a7586836fa2103c191f88d2f.nq.gz
│   ├── 4a6875bb7631034bcdd06b5cdfc83f4caaa45407.nq.gz
│   ├── 4db2a3a63cb19c22930fc34704ff869262b0b31c.nq.gz
│   ├── 53d376fc14e0622378d2c0797324ba423fa2b83b.nq.gz
│   ├── 57f1e601c83ddd9bd1b12ac192dea1f340891bde.nq.gz
│   ├── 6b0b1270ff0ca8f03867efcd09ba6ddb6392b1e1.nq.gz
│   ├── 6e84f87900cf17921be5b75ce2f4398cd424bc25.nq.gz
│   ├── 7372f7254a99be41a9416e054cc0fa7c4404df9b.nq.gz
│   ├── 85789c79516bf814c109ca72e5ca2c35d1fe1d98.nq.gz
│   ├── 85a056c124167b6d12a55f585703085f1bb942d2.nq.gz
│   ├── 86f3cc25d8a17a656775c443ff7544210e46d398.nq.gz
│   ├── 88443cae8b182aaf19eed83c58a205796caf936b.nq.gz
│   ├── 8bdee2bf4bc83e03b0bf26a1084c2a7b1e39c8e6.nq.gz
│   ├── 99fdd24d991b7f0599a8b03e686c2db43811fb7c.nq.gz
│   ├── bc1afcb29245357324a63c7dbb0ca9c4f32afced.nq.gz
│   ├── c7cd0449cc2fc5417012d1d835af1a85ad4c0b07.nq.gz
│   ├── c8b750e9a2403b1c675ecdfd8c0e6760b5f62c3b.nq.gz
│   ├── d1b1d9c2aba56434907b1272ffea418dfecfd253.nq.gz
│   ├── d2a686d39cb84b22745082725a87b928f62ddaa9.nq.gz
│   ├── d875786acfebe94eb1b0c205b96968b4bd3e9a56.nq.gz
│   ├── dc8e3756b3677d79855af6f86d46657c078e1d79.nq.gz
│   ├── dcb75e57add442e632173f07efc278b0ef5e0cad.nq.gz
│   ├── dcbf44ad164368f56276046a51d02678c5027639.nq.gz
│   ├── e4917e0b185d9f10115c5aafcaa3469f17098129.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e73e1bdd9426f9bd82d06a7dc95c5957cd0d40ab.nq.gz
│   ├── eb92e29ab6c98c9800e4b89eeab9465dd5255db5.nq.gz
│   └── f2f54ce3155ecace40326f8bb2767e710b8bee5a.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── ce4f368f8987b1111d92bf03f6b40710827ecf11.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 44 files
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

[UKPLab/acl2019-ctest-difficulty-manipulation](https://github.com/UKPLab/acl2019-ctest-difficulty-manipulation)

---
*Parsed on 2026-11-08 by [repolex](https://repolex.ai)*
