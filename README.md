# One Lab Per Kernel

A technical field note by Yossi Eliaz: a design proposal (not yet run) for a
reproducible SOL-ExecBench GPU-kernel research campaign on Islo.

Live article: <https://zozo123.github.io/sol-exec-bench/>

The article distinguishes public benchmark results from the proposed Islo
implementation. It does not claim that an Islo SOL-ExecBench campaign has
already run.

The Islo angle is intentionally split into two planes:

- Islo provides the CPU agent control plane: persistent microVMs, jobs,
  snapshots, native Claude/Codex access, scoped gateways, and logs.
- A separate external or BYOC service must provide hardened B200 execution,
  verification, benchmarking, and evidence receipts. Islo's public job schema
  does not currently expose a GPU resource field.

The illustrative [`jobs/sol-kernel/job.toml`](jobs/sol-kernel/job.toml)
manifest has been checked with the current Islo CLI. Its referenced snapshot,
gateway profile, and campaign command are inputs to the proposed implementation,
not assets that exist in this repository.

Last primary-source audit: 28 July 2026.

Disclosure: the author is Principal Engineer, AI Systems at Incredibuild /
islo.dev.

## Sources

The primary sources are linked inline and collected at the end of the article:
NVIDIA SOL-ExecBench, Databricks/KDA/Humanize/Omnigent, Cursor, doubleAI,
Recursive, and Islo documentation.
