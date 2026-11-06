# Repolex Knowledge Graph of ansible-community/meetings

RDF knowledge graph data for [ansible-community/meetings](https://github.com/ansible-community/meetings), parsed by [repolex](https://repolex.ai).

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
rlex download ansible-community/meetings
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 450a3328a3f327f89cd97dc5b3fa240ba1bcc65a
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 450a3328a3f327f89cd97dc5b3fa240ba1bcc65a
│           └── chunk-001.nq.gz
├── blob
│   ├── 05871f79fa4957a77cdd7b8be39c3888fa47b872.nq.gz
│   ├── 28dc279abde5ff6016727d9152d282beddec5af9.nq.gz
│   ├── 304d44dead57796b22134568896e40a8a9f81360.nq.gz
│   ├── 38522af49ab6517acc94c380cc99566c59caddd6.nq.gz
│   ├── 5623a062567b344679765cd4bad3f5bee5a97417.nq.gz
│   ├── 5ba6ada67bfc21172010a6770ff8ce2e30db82ef.nq.gz
│   ├── 6439e7de50e065c60c8e13c0ace9dbb0fd06d5df.nq.gz
│   ├── 6573133c6a7bd55b601071c33bf0143bbec91a0b.nq.gz
│   ├── 67dd957f1c1dac14df606c48e6ed19f1e249c570.nq.gz
│   ├── 69356e7ecabbf93357f38583d84ae4e62e48b358.nq.gz
│   ├── a6514e00e50f3992a7d87da28d84adc7791b9f70.nq.gz
│   ├── b3544922a4ea0d94ebfe79895d7bdd70e2fd7acc.nq.gz
│   ├── b899a24ac74e9aabbcf5d5a5cb2664e9830b93d0.nq.gz
│   ├── c2be83fe111b3fc6ecdd9a0f95f010d0c291ff3e.nq.gz
│   ├── c6ee89aced16368ddc6c889d7f06a508d08c4fb9.nq.gz
│   ├── ce783f5a7a8ff0b5b17167ff1b1e7f9972529810.nq.gz
│   ├── d061d80d644cfcac02784ec4e2600e933dd8a111.nq.gz
│   ├── d497e30956d2d795b3973116307220570ddacc09.nq.gz
│   ├── d936eaa40fc7ae0d5d3f70417f365f30985637d5.nq.gz
│   ├── e2a4a10167558b8bc57d963c1e748bd13761aaac.nq.gz
│   ├── e72bfddabc15be5718a7cc061ac10e47741d8219.nq.gz
│   └── f288702d2fa16d3cdf0035b15a9fcbc552cd88e7.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 450a3328a3f327f89cd97dc5b3fa240ba1bcc65a.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 29 files
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

[ansible-community/meetings](https://github.com/ansible-community/meetings)

---
*Parsed on 2026-11-06 by [repolex](https://repolex.ai)*
