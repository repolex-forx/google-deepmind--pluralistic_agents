# Repolex Knowledge Graph of google-deepmind/pluralistic_agents

RDF knowledge graph data for [google-deepmind/pluralistic_agents](https://github.com/google-deepmind/pluralistic_agents), parsed by [repolex](https://repolex.ai).

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
rlex download google-deepmind/pluralistic_agents
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 35d332f9ccf16f4cdf28211b563e539319ad5d44
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 35d332f9ccf16f4cdf28211b563e539319ad5d44
│           └── chunk-001.nq.gz
├── blob
│   ├── 09e05705fd0ad2dea389300fab8da64b615d203d.nq.gz
│   ├── 0b52973e1c483727f05a1b0aa20533cff516cd49.nq.gz
│   ├── 1d1e957c1401bbcc7b234526ccf1ba91cd727897.nq.gz
│   ├── 2ea66c559149aecab27216254b253943fed704ba.nq.gz
│   ├── 319ad171b09a8299f3388e10b6b17753f461d6f6.nq.gz
│   ├── 34bbcdbce0278d51c211f0c471ad1b8bd29ccf92.nq.gz
│   ├── 3bfc7c22003c220bde78dca996841f67d6a7850a.nq.gz
│   ├── 3ebe3b57bb2c6a3972eddec374ea78e52237c014.nq.gz
│   ├── 459d444834ffab66ead2480ab27ee4b847c1c424.nq.gz
│   ├── 45b0d17d62116c0f63bedc990c94ffde4a09a6c1.nq.gz
│   ├── 51a7c6515d687268881de815de09664803b07797.nq.gz
│   ├── 5b3235b675ca8d4d061a90b8d2673cdd0b9f4431.nq.gz
│   ├── 6bb4c5750290a2bb50c0e94ef6ba54998db837b7.nq.gz
│   ├── 7099f98e442cedacf5e00beacbad0c0815f555da.nq.gz
│   ├── 7d7616d9962861e1d9ad6b2c456744080b909a82.nq.gz
│   ├── 87df5a1cb638f2cbb0227da5e199ae74016f2423.nq.gz
│   ├── 90a5179ca045999d52fa695d19f6cf9670e14d95.nq.gz
│   ├── aebd566487aab0fd84571f818f6f1f97202f6e1e.nq.gz
│   ├── b5554eae620ae1ea90f0a0d131a2c48bedc652d3.nq.gz
│   ├── bb9e2d87208c293a0441d749adeddfa36c5d7c9f.nq.gz
│   ├── c8758b6ad65613a92ca7a2a48377ef9ba411b82b.nq.gz
│   ├── ccb101e996ed520c0d66300d4ed0558edfed38c9.nq.gz
│   ├── d645695673349e3947e8e5ae42332d0ac3164cd7.nq.gz
│   ├── de78d89fca72f5c8170e1e2a5020c7b6acfa8b7a.nq.gz
│   ├── e594d592ae40234033b073e4d0c49bc0cef6b482.nq.gz
│   ├── e85d9451a8b06aef26eecd751141c6737e1ae2f9.nq.gz
│   ├── e95bde4d1e754e3d88d351931960118c775eddea.nq.gz
│   └── ec7bb1514cdb61f92af105d84c8d0fdd451b5a48.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 35d332f9ccf16f4cdf28211b563e539319ad5d44.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 34 files
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

[google-deepmind/pluralistic_agents](https://github.com/google-deepmind/pluralistic_agents)

---
*Parsed on 2026-11-08 by [repolex](https://repolex.ai)*
