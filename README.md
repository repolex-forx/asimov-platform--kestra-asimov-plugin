# Repolex Knowledge Graph of asimov-platform/kestra-asimov-plugin

RDF knowledge graph data for [asimov-platform/kestra-asimov-plugin](https://github.com/asimov-platform/kestra-asimov-plugin), parsed by [repolex](https://repolex.ai).

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
rlex download asimov-platform/kestra-asimov-plugin
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 4abf23e71987124f71711c4f26d0aaff409425c9
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 4abf23e71987124f71711c4f26d0aaff409425c9.nq.gz
│   └── repolex
│       └── 4abf23e71987124f71711c4f26d0aaff409425c9
│           └── chunk-001.nq.gz
├── blob
│   ├── 0586c818b018fbae829a775e368b904727533249.nq.gz
│   ├── 21557ee8992e9a4360890aca56ed53cb2d4a82c9.nq.gz
│   ├── 37f853b1c84d2e2dd1c88441fcc755d7f6643668.nq.gz
│   ├── 3c171ae1e54d0ded02bc2116e2f803ba9f269c38.nq.gz
│   ├── 3da6d1fb582b5739f3b8b1891e7b050076c9aae7.nq.gz
│   ├── 45d6b9b6f21a7f53d05435a9a13a415b30b6ec43.nq.gz
│   ├── 4873f6d0c5d164acdcbcdffe222459311ab17a5e.nq.gz
│   ├── 492b0dbf0198c29911142c94f14b594f21c50e3a.nq.gz
│   ├── 4be6e5d20e8ba23b9570e06cb0adff18957e451c.nq.gz
│   ├── 50e452dbfbbc8ef01675cf2c2fc9ffa91dc42b9e.nq.gz
│   ├── 54a1f7e2ef74528315ff03aaf672d8a799cec4a2.nq.gz
│   ├── 597602e482b388b0288a9ab24046a6fa667d123a.nq.gz
│   ├── 5b7177c3eb192a158f9b4638e96d06f98ac3a466.nq.gz
│   ├── 636ef672e025d611f2b651b9f08c544437197f6d.nq.gz
│   ├── 68570ae5d93c01d18b3dc8e6a4db7734ffb3d1b0.nq.gz
│   ├── 7971aa1a805521a382d209e4eb0959e158da315f.nq.gz
│   ├── 803c82e3f4eceb61c3130493dac7138c2c6dcc16.nq.gz
│   ├── 818e932477b931a5758562b632392d4fe99181f6.nq.gz
│   ├── 83014c34bcd3157a08f73fc3d7ebb415e29a6d3c.nq.gz
│   ├── 941851afd6b45060b4b7624ec8e4303540232f49.nq.gz
│   ├── 9d21a21834d5195c278ba17baec3115b2aaab06e.nq.gz
│   ├── a4b76b9530d66f5e68d973ea569d8e19de379189.nq.gz
│   ├── a760828960a7cafaf4cd16d772a2a96b289dd2ca.nq.gz
│   ├── aaa347f724898651911c4ede0ce37d09a37d2194.nq.gz
│   ├── b5184d6546c380e8607b2116af9652ea46db52f4.nq.gz
│   ├── b7509dae414d7fa2186dd560e504ad893f3b6e12.nq.gz
│   ├── b7ad1a9dd33244f1627d8be4acd5cd4b843cb5a5.nq.gz
│   ├── c475b05352e3a9654867e5f092d0b160a8a9c8bf.nq.gz
│   ├── cd5db577279adb46d28cbb926b10e90e2f83361b.nq.gz
│   ├── d2e8d38e7f97bcc7ff68b498789bf52ff040daec.nq.gz
│   ├── de9ab6af988322130f3cdacae8f329ed97dce6d4.nq.gz
│   ├── e452654a0d66d72cc1ce860488ebfe16b73c45f1.nq.gz
│   ├── f3b75f3b0d4faeb4b1c8a02b5c47007e6efb7dcd.nq.gz
│   ├── ff53368fd3e7148c238a87bfec0e99056eecc708.nq.gz
│   └── ff74ae5d8ca63d3be918de5d24660612de4309d9.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 4abf23e71987124f71711c4f26d0aaff409425c9.nq.gz
├── filetree
│   └── 4abf23e71987124f71711c4f26d0aaff409425c9.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

14 directories, 44 files
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

[asimov-platform/kestra-asimov-plugin](https://github.com/asimov-platform/kestra-asimov-plugin)

---
*Parsed on 2026-09-27 by [repolex](https://repolex.ai)*
