# Repolex Knowledge Graph of bokeh/jupyter_bokeh

RDF knowledge graph data for [bokeh/jupyter_bokeh](https://github.com/bokeh/jupyter_bokeh), parsed by [repolex](https://repolex.ai).

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
rlex download bokeh/jupyter_bokeh
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 475f4e96f9ea4ce46b10c35119cfdd1cbeb523ab
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 475f4e96f9ea4ce46b10c35119cfdd1cbeb523ab
│           └── chunk-001.nq.gz
├── blob
│   ├── 08dc4dd09ff591e650bdc5056a833ca8f8cb830d.nq.gz
│   ├── 20e33747414c4d6de79ed1113e97f9e54dc680c4.nq.gz
│   ├── 296756349a63a327894eca0c6a7ba8e0b7a3a003.nq.gz
│   ├── 301ff3b30c08f28026722208b4628b0021b5b715.nq.gz
│   ├── 31268ebe9e21964bae520f75fd3ad58ffb9cac4b.nq.gz
│   ├── 3186f3f0795ab612d5508593672dc9ad94bccca0.nq.gz
│   ├── 322ba5f1147646c7ab3a0ec017dbbf19fcf42315.nq.gz
│   ├── 34cdd549f952e4a2f4955e98e3d880f8e582bd9c.nq.gz
│   ├── 34eed26d37456329f99f2ff0673aa4b12f299926.nq.gz
│   ├── 396fde332bb382229e9124fe0f15a429f86cec86.nq.gz
│   ├── 3bcf7f5b81727510ba20f3a8d5f95ff4b1817757.nq.gz
│   ├── 490e8f8231ed61bbd26122fb2a48797d5868291c.nq.gz
│   ├── 4b10719e5b31cdabedb685ef938b5bbaac573136.nq.gz
│   ├── 4eda7093599fb09441040b777f9a9f60660e498d.nq.gz
│   ├── 52ae99998417bf282f1f59bc8e72250b29d61e78.nq.gz
│   ├── 534fd2c3bee3c36863e76749e767ed8aaf92e3fe.nq.gz
│   ├── 5c99ba78a7a246729fee6a3c03707e5e4ce4fce5.nq.gz
│   ├── 630a2df369a67a186c49aa568c26c4ca8c5766f9.nq.gz
│   ├── 6b2061be5a606ee99420b4a1c63ca06677df9372.nq.gz
│   ├── 758436e88be219e64db66ad33374aee9f2efc87e.nq.gz
│   ├── 7cd2303e8ccda161e798efbae233d5d2073585f7.nq.gz
│   ├── 7e140b24faf89586371210270e874a80e80c0357.nq.gz
│   ├── 7ff60fe12c12f355a800078fc1aeb9c2661b5a45.nq.gz
│   ├── 830e7f22d9681cc4ea46bfdb46fdfadf352925a1.nq.gz
│   ├── 83d02192cbf28e768c4a0f6af302017096c1b01c.nq.gz
│   ├── 8a7ea29e69487a93c256fee6e15adfd533a53280.nq.gz
│   ├── 8dafd3e604df569d1f576c516a46fddc642a8e8e.nq.gz
│   ├── 8ee6c1be621506bcad3e81572cf66a424e9f8b8a.nq.gz
│   ├── 90b6ba97809808e74470baaf71ae6444560e16ac.nq.gz
│   ├── 9473845c2fd5540bf791a263864bbf4cbde43a15.nq.gz
│   ├── 987e720b88e0ebb330699826d7bc8e25963b39b3.nq.gz
│   ├── a028a76408bf46181259249b2e15e14a9bbdf7f1.nq.gz
│   ├── bdf150a3b40b1471b60e6a327d1176dd7cb77452.nq.gz
│   ├── bea2337431004d9635b7795f968ecdb7c78d9c6f.nq.gz
│   ├── befaaf264de515ff515da9a9cad028ce926e52c7.nq.gz
│   ├── dcbece71d5831b7204b6d8a1038bb4414d2368cb.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── eaae5534ff05a97e505204049425ed4d9b3565b8.nq.gz
│   ├── ee920fb70a9828c0e8e9c8bebf1677fe6317e4a2.nq.gz
│   ├── f527f9c0168f51eda16729fa7da8288f50d9f2b2.nq.gz
│   └── f731497008de962ca9f9d9773525cd5fb496caf7.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 475f4e96f9ea4ce46b10c35119cfdd1cbeb523ab.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 49 files
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

[bokeh/jupyter_bokeh](https://github.com/bokeh/jupyter_bokeh)

---
*Parsed on 2026-10-21 by [repolex](https://repolex.ai)*
