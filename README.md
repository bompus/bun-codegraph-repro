# CodeGraph final-step fixture for Bun #45995

This repository hosts a self-contained reproduction fixture for [Bun #45995](https://github.com/oven-sh/bun/issues/45995).
The fixture calls CodeGraph's actual callback-edge synthesis and near-duplicate refresh functions.
It requires no CodeGraph build or native addon.

Download [bun45995-final-step.tar.gz](https://github.com/bompus/bun-codegraph-repro/releases/download/bun-45995-20261020/bun45995-final-step.tar.gz) and verify its checksum before extracting.
Read the included README for commands, provenance, limitations and licenses.

- Archive size: 289,640,854 bytes
- SHA256: `842b44cf34d99857001aaa93967f6deac48378cfe586dcd86ac1b45c5383b2cf`
- CodeGraph revision: `3581ae6e8624ac201babf8a8fdf459987b8fc7af`
- Public n8n source revision: `7cc0450ae47469b13406c3e4910b67251a54b9bc`

Separate correctness checks on Node 24.22.0 and Bun 1.4.3+c6da4a4d3 produced equal semantic outputs across six tables, including SQLite WAL contents.
The outputs include 1,127,062 edges, 2,624 near-duplicate rows and 16,395 cached scores.
The original peak-memory gap remains unverified for this package.
The latest controlled campaign stopped at its first safety admission, with zero workloads and zero accepted performance samples.

The reduction removes enterprise-restricted n8n files and omits the live heap from parsing and reference resolution.
It marks existing functions stale rather than rerunning extraction.

## Licenses and distribution

This fixture is shared free of charge for noncommercial reproduction.
The archive contains the original component licenses and notices, including n8n's Sustainable Use License and CodeGraph's license.
Third-party components retain their original licenses.
The fixture as a whole is not offered under a blanket MIT license.
Preserve all included licenses and notices, and follow their conditions.
See `licenses/n8n/LICENSE.md` and `licenses/codegraph/LICENSE` inside the archive.

The fixed release asset will be retained while the upstream issue needs it for reproduction.
