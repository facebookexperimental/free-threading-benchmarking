# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
[Most recent pystats on main (f6cc7c8)](results/bm-20241026-3.14.0a1%2B-f6cc7c8-PYTHON_UOPS/bm-20241026-vultr-x86_64-python-f6cc7c8bd01d8468af70-3.14.0a1%2B-f6cc7c8-pystats.md)

## linux x86_64 (linux)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2024-10-22](results/bm-20241022-3.14.0a1%2B-34653bb) | python/34653bba644aa5481613 | 34653bb | 1.03x ↓<br>[📄](results/bm-20241022-3.14.0a1%2B-34653bb/bm-20241022-linux-x86_64-python-34653bba644aa5481613-3.14.0a1%2B-34653bb-vs-3.12.6.md)[📈](results/bm-20241022-3.14.0a1%2B-34653bb/bm-20241022-linux-x86_64-python-34653bba644aa5481613-3.14.0a1%2B-34653bb-vs-3.12.6.svg) | 1.05x ↓<br>[📄](results/bm-20241022-3.14.0a1%2B-34653bb/bm-20241022-linux-x86_64-python-34653bba644aa5481613-3.14.0a1%2B-34653bb-vs-3.13.0rc2.md)[📈](results/bm-20241022-3.14.0a1%2B-34653bb/bm-20241022-linux-x86_64-python-34653bba644aa5481613-3.14.0a1%2B-34653bb-vs-3.13.0rc2.svg) |  |
| [2024-10-22](results/bm-20241022-3.14.0a1%2B-34653bb-NOGIL) | python/34653bba644aa5481613 | 34653bb (NOGIL) | 1.48x ↓<br>[📄](results/bm-20241022-3.14.0a1%2B-34653bb-NOGIL/bm-20241022-linux-x86_64-python-34653bba644aa5481613-3.14.0a1%2B-34653bb-vs-3.12.6.md)[📈](results/bm-20241022-3.14.0a1%2B-34653bb-NOGIL/bm-20241022-linux-x86_64-python-34653bba644aa5481613-3.14.0a1%2B-34653bb-vs-3.12.6.svg) | 1.50x ↓<br>[📄](results/bm-20241022-3.14.0a1%2B-34653bb-NOGIL/bm-20241022-linux-x86_64-python-34653bba644aa5481613-3.14.0a1%2B-34653bb-vs-3.13.0rc2.md)[📈](results/bm-20241022-3.14.0a1%2B-34653bb-NOGIL/bm-20241022-linux-x86_64-python-34653bba644aa5481613-3.14.0a1%2B-34653bb-vs-3.13.0rc2.svg) | 1.43x ↓<br>[📄](results/bm-20241022-3.14.0a1%2B-34653bb-NOGIL/bm-20241022-linux-x86_64-python-34653bba644aa5481613-3.14.0a1%2B-34653bb-vs-base.md)[📈](results/bm-20241022-3.14.0a1%2B-34653bb-NOGIL/bm-20241022-linux-x86_64-python-34653bba644aa5481613-3.14.0a1%2B-34653bb-vs-base.svg)[🧠](results/bm-20241022-3.14.0a1%2B-34653bb-NOGIL/bm-20241022-linux-x86_64-python-34653bba644aa5481613-3.14.0a1%2B-34653bb-vs-base-mem.svg) |
| [2024-10-21](results/bm-20241021-3.14.0a1%2B-d0bfff4) | python/d0bfff47fb2aea9272b5 | d0bfff4 | 1.00x ↑<br>[📄](results/bm-20241021-3.14.0a1%2B-d0bfff4/bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1%2B-d0bfff4-vs-3.12.6.md)[📈](results/bm-20241021-3.14.0a1%2B-d0bfff4/bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1%2B-d0bfff4-vs-3.12.6.svg) | 1.01x ↓<br>[📄](results/bm-20241021-3.14.0a1%2B-d0bfff4/bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1%2B-d0bfff4-vs-3.13.0rc2.md)[📈](results/bm-20241021-3.14.0a1%2B-d0bfff4/bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1%2B-d0bfff4-vs-3.13.0rc2.svg) |  |

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2024-10-27](results/bm-20241027-3.14.0a1%2B-19e93e2-NOGIL) | python/19e93e2e269889ecb3c4 | 19e93e2 (NOGIL) | 1.54x ↓<br>[📄](results/bm-20241027-3.14.0a1%2B-19e93e2-NOGIL/bm-20241027-vultr-x86_64-python-19e93e2e269889ecb3c4-3.14.0a1%2B-19e93e2-vs-3.12.6.md)[📈](results/bm-20241027-3.14.0a1%2B-19e93e2-NOGIL/bm-20241027-vultr-x86_64-python-19e93e2e269889ecb3c4-3.14.0a1%2B-19e93e2-vs-3.12.6.svg) | 1.56x ↓<br>[📄](results/bm-20241027-3.14.0a1%2B-19e93e2-NOGIL/bm-20241027-vultr-x86_64-python-19e93e2e269889ecb3c4-3.14.0a1%2B-19e93e2-vs-3.13.0rc2.md)[📈](results/bm-20241027-3.14.0a1%2B-19e93e2-NOGIL/bm-20241027-vultr-x86_64-python-19e93e2e269889ecb3c4-3.14.0a1%2B-19e93e2-vs-3.13.0rc2.svg) | 1.53x ↓<br>[📄](results/bm-20241027-3.14.0a1%2B-19e93e2-NOGIL/bm-20241027-vultr-x86_64-python-19e93e2e269889ecb3c4-3.14.0a1%2B-19e93e2-vs-base.md)[📈](results/bm-20241027-3.14.0a1%2B-19e93e2-NOGIL/bm-20241027-vultr-x86_64-python-19e93e2e269889ecb3c4-3.14.0a1%2B-19e93e2-vs-base.svg)[🧠](results/bm-20241027-3.14.0a1%2B-19e93e2-NOGIL/bm-20241027-vultr-x86_64-python-19e93e2e269889ecb3c4-3.14.0a1%2B-19e93e2-vs-base-mem.svg) |
| [2024-10-27](results/bm-20241027-3.14.0a1%2B-19e93e2) | python/19e93e2e269889ecb3c4 | 19e93e2 | 1.00x ↓<br>[📄](results/bm-20241027-3.14.0a1%2B-19e93e2/bm-20241027-vultr-x86_64-python-19e93e2e269889ecb3c4-3.14.0a1%2B-19e93e2-vs-3.12.6.md)[📈](results/bm-20241027-3.14.0a1%2B-19e93e2/bm-20241027-vultr-x86_64-python-19e93e2e269889ecb3c4-3.14.0a1%2B-19e93e2-vs-3.12.6.svg) | 1.02x ↓<br>[📄](results/bm-20241027-3.14.0a1%2B-19e93e2/bm-20241027-vultr-x86_64-python-19e93e2e269889ecb3c4-3.14.0a1%2B-19e93e2-vs-3.13.0rc2.md)[📈](results/bm-20241027-3.14.0a1%2B-19e93e2/bm-20241027-vultr-x86_64-python-19e93e2e269889ecb3c4-3.14.0a1%2B-19e93e2-vs-3.13.0rc2.svg) |  |
| [2024-10-26](results/bm-20241026-3.14.0a1%2B-f6cc7c8) | python/f6cc7c8bd01d8468af70 | f6cc7c8 | 1.00x ↑<br>[📄](results/bm-20241026-3.14.0a1%2B-f6cc7c8/bm-20241026-vultr-x86_64-python-f6cc7c8bd01d8468af70-3.14.0a1%2B-f6cc7c8-vs-3.12.6.md)[📈](results/bm-20241026-3.14.0a1%2B-f6cc7c8/bm-20241026-vultr-x86_64-python-f6cc7c8bd01d8468af70-3.14.0a1%2B-f6cc7c8-vs-3.12.6.svg) | 1.01x ↓<br>[📄](results/bm-20241026-3.14.0a1%2B-f6cc7c8/bm-20241026-vultr-x86_64-python-f6cc7c8bd01d8468af70-3.14.0a1%2B-f6cc7c8-vs-3.13.0rc2.md)[📈](results/bm-20241026-3.14.0a1%2B-f6cc7c8/bm-20241026-vultr-x86_64-python-f6cc7c8bd01d8468af70-3.14.0a1%2B-f6cc7c8-vs-3.13.0rc2.svg) |  |
| [2024-10-26](results/bm-20241026-3.14.0a1%2B-f6cc7c8-NOGIL) | python/f6cc7c8bd01d8468af70 | f6cc7c8 (NOGIL) | 1.55x ↓<br>[📄](results/bm-20241026-3.14.0a1%2B-f6cc7c8-NOGIL/bm-20241026-vultr-x86_64-python-f6cc7c8bd01d8468af70-3.14.0a1%2B-f6cc7c8-vs-3.12.6.md)[📈](results/bm-20241026-3.14.0a1%2B-f6cc7c8-NOGIL/bm-20241026-vultr-x86_64-python-f6cc7c8bd01d8468af70-3.14.0a1%2B-f6cc7c8-vs-3.12.6.svg) | 1.57x ↓<br>[📄](results/bm-20241026-3.14.0a1%2B-f6cc7c8-NOGIL/bm-20241026-vultr-x86_64-python-f6cc7c8bd01d8468af70-3.14.0a1%2B-f6cc7c8-vs-3.13.0rc2.md)[📈](results/bm-20241026-3.14.0a1%2B-f6cc7c8-NOGIL/bm-20241026-vultr-x86_64-python-f6cc7c8bd01d8468af70-3.14.0a1%2B-f6cc7c8-vs-3.13.0rc2.svg) | 1.55x ↓<br>[📄](results/bm-20241026-3.14.0a1%2B-f6cc7c8-NOGIL/bm-20241026-vultr-x86_64-python-f6cc7c8bd01d8468af70-3.14.0a1%2B-f6cc7c8-vs-base.md)[📈](results/bm-20241026-3.14.0a1%2B-f6cc7c8-NOGIL/bm-20241026-vultr-x86_64-python-f6cc7c8bd01d8468af70-3.14.0a1%2B-f6cc7c8-vs-base.svg)[🧠](results/bm-20241026-3.14.0a1%2B-f6cc7c8-NOGIL/bm-20241026-vultr-x86_64-python-f6cc7c8bd01d8468af70-3.14.0a1%2B-f6cc7c8-vs-base-mem.svg) |
| [2024-10-25](results/bm-20241025-3.14.0a1%2B-c5b99f5) | python/c5b99f5c2c5347d66b9d | c5b99f5 | 1.01x ↓<br>[📄](results/bm-20241025-3.14.0a1%2B-c5b99f5/bm-20241025-vultr-x86_64-python-c5b99f5c2c5347d66b9d-3.14.0a1%2B-c5b99f5-vs-3.12.6.md)[📈](results/bm-20241025-3.14.0a1%2B-c5b99f5/bm-20241025-vultr-x86_64-python-c5b99f5c2c5347d66b9d-3.14.0a1%2B-c5b99f5-vs-3.12.6.svg) | 1.02x ↓<br>[📄](results/bm-20241025-3.14.0a1%2B-c5b99f5/bm-20241025-vultr-x86_64-python-c5b99f5c2c5347d66b9d-3.14.0a1%2B-c5b99f5-vs-3.13.0rc2.md)[📈](results/bm-20241025-3.14.0a1%2B-c5b99f5/bm-20241025-vultr-x86_64-python-c5b99f5c2c5347d66b9d-3.14.0a1%2B-c5b99f5-vs-3.13.0rc2.svg) |  |
| [2024-10-25](results/bm-20241025-3.14.0a1%2B-c5b99f5-NOGIL) | python/c5b99f5c2c5347d66b9d | c5b99f5 (NOGIL) | 1.56x ↓<br>[📄](results/bm-20241025-3.14.0a1%2B-c5b99f5-NOGIL/bm-20241025-vultr-x86_64-python-c5b99f5c2c5347d66b9d-3.14.0a1%2B-c5b99f5-vs-3.12.6.md)[📈](results/bm-20241025-3.14.0a1%2B-c5b99f5-NOGIL/bm-20241025-vultr-x86_64-python-c5b99f5c2c5347d66b9d-3.14.0a1%2B-c5b99f5-vs-3.12.6.svg) | 1.58x ↓<br>[📄](results/bm-20241025-3.14.0a1%2B-c5b99f5-NOGIL/bm-20241025-vultr-x86_64-python-c5b99f5c2c5347d66b9d-3.14.0a1%2B-c5b99f5-vs-3.13.0rc2.md)[📈](results/bm-20241025-3.14.0a1%2B-c5b99f5-NOGIL/bm-20241025-vultr-x86_64-python-c5b99f5c2c5347d66b9d-3.14.0a1%2B-c5b99f5-vs-3.13.0rc2.svg) | 1.55x ↓<br>[📄](results/bm-20241025-3.14.0a1%2B-c5b99f5-NOGIL/bm-20241025-vultr-x86_64-python-c5b99f5c2c5347d66b9d-3.14.0a1%2B-c5b99f5-vs-base.md)[📈](results/bm-20241025-3.14.0a1%2B-c5b99f5-NOGIL/bm-20241025-vultr-x86_64-python-c5b99f5c2c5347d66b9d-3.14.0a1%2B-c5b99f5-vs-base.svg)[🧠](results/bm-20241025-3.14.0a1%2B-c5b99f5-NOGIL/bm-20241025-vultr-x86_64-python-c5b99f5c2c5347d66b9d-3.14.0a1%2B-c5b99f5-vs-base-mem.svg) |
| [2024-10-25](results/bm-20241025-3.14.0a1%2B-e68d4b0) | python/e68d4b08ff13a06a2c28 | e68d4b0 | 1.00x ↑<br>[📄](results/bm-20241025-3.14.0a1%2B-e68d4b0/bm-20241025-vultr-x86_64-python-e68d4b08ff13a06a2c28-3.14.0a1%2B-e68d4b0-vs-3.12.6.md)[📈](results/bm-20241025-3.14.0a1%2B-e68d4b0/bm-20241025-vultr-x86_64-python-e68d4b08ff13a06a2c28-3.14.0a1%2B-e68d4b0-vs-3.12.6.svg) | 1.01x ↓<br>[📄](results/bm-20241025-3.14.0a1%2B-e68d4b0/bm-20241025-vultr-x86_64-python-e68d4b08ff13a06a2c28-3.14.0a1%2B-e68d4b0-vs-3.13.0rc2.md)[📈](results/bm-20241025-3.14.0a1%2B-e68d4b0/bm-20241025-vultr-x86_64-python-e68d4b08ff13a06a2c28-3.14.0a1%2B-e68d4b0-vs-3.13.0rc2.svg) |  |
| [2024-10-25](results/bm-20241025-3.14.0a1%2B-e68d4b0-NOGIL) | python/e68d4b08ff13a06a2c28 | e68d4b0 (NOGIL) | 1.55x ↓<br>[📄](results/bm-20241025-3.14.0a1%2B-e68d4b0-NOGIL/bm-20241025-vultr-x86_64-python-e68d4b08ff13a06a2c28-3.14.0a1%2B-e68d4b0-vs-3.12.6.md)[📈](results/bm-20241025-3.14.0a1%2B-e68d4b0-NOGIL/bm-20241025-vultr-x86_64-python-e68d4b08ff13a06a2c28-3.14.0a1%2B-e68d4b0-vs-3.12.6.svg) | 1.58x ↓<br>[📄](results/bm-20241025-3.14.0a1%2B-e68d4b0-NOGIL/bm-20241025-vultr-x86_64-python-e68d4b08ff13a06a2c28-3.14.0a1%2B-e68d4b0-vs-3.13.0rc2.md)[📈](results/bm-20241025-3.14.0a1%2B-e68d4b0-NOGIL/bm-20241025-vultr-x86_64-python-e68d4b08ff13a06a2c28-3.14.0a1%2B-e68d4b0-vs-3.13.0rc2.svg) | 1.56x ↓<br>[📄](results/bm-20241025-3.14.0a1%2B-e68d4b0-NOGIL/bm-20241025-vultr-x86_64-python-e68d4b08ff13a06a2c28-3.14.0a1%2B-e68d4b0-vs-base.md)[📈](results/bm-20241025-3.14.0a1%2B-e68d4b0-NOGIL/bm-20241025-vultr-x86_64-python-e68d4b08ff13a06a2c28-3.14.0a1%2B-e68d4b0-vs-base.svg)[🧠](results/bm-20241025-3.14.0a1%2B-e68d4b0-NOGIL/bm-20241025-vultr-x86_64-python-e68d4b08ff13a06a2c28-3.14.0a1%2B-e68d4b0-vs-base-mem.svg) |


<!-- END table -->

`*` indicates that the exact same versions of pyperformance was not used.

![Longitudinal speed improvement](/longitudinal.svg)

Improvement of the geometric mean of key merged benchmarks, computed with `pyperf compare`.
The results have a resolution of 0.01 (1%).

![Configuration speed improvement](/configs.svg)

## Documentation

### Running benchmarks from the GitHub web UI

Visit the 🔒 [benchmark action](../../actions/workflows/benchmark.yml) and click the "Run Workflow" button.

The available parameters are:

- `fork`: The fork of CPython to benchmark.
  If benchmarking a pull request, this would normally be your GitHub username.
- `ref`: The branch, tag or commit SHA to benchmark.
  If a SHA, it must be the full SHA, since finding it by a prefix is not supported.
- `machine`: The machine to run on.
  One of `linux-amd64` (default), `windows-amd64`, `darwin-arm64` or `all`.
- `benchmark_base`: If checked, the base of the selected branch will also be benchmarked.
  The base is determined by running `git merge-base upstream/main $ref`.
- `pystats`: If checked, collect the pystats from running the benchmarks.

To watch the progress of the benchmark, select it from the 🔒 [benchmark action page](../../actions/workflows/benchmark.yml).
It may be canceled from there as well.
To show only your benchmark workflows, select your GitHub ID from the "Actor" dropdown.

When the benchmarking is complete, the results are published to this repository and will appear in the [complete table](RESULTS.md).
Each set of benchmarks will have:

- The raw `.json` results from pyperformance.
- Comparisons against important reference releases, as well as the merge base of the branch if `benchmark_base` was selected. These include
  - A markdown table produced by `pyperf compare_to`.
  - A set of "violin" plots showing the distribution of results for each benchmark.

The most convenient way to get results locally is to clone this repo and `git pull` from it.

### Running benchmarks from the GitHub CLI

To automate benchmarking runs, it may be more convenient to use the [GitHub CLI](https://cli.github.com/).
Once you have `gh` installed and configured, you can run benchmarks by cloning this repository and then from inside it:

```bash session
gh workflow run benchmark.yml -f fork=me -f ref=my_branch
```

Any of the parameters described above are available at the commandline using the `-f key=value` syntax.

### Collecting Linux perf profiling data

To collect Linux perf sampling profile data for a benchmarking run, run the `_benchmark` action and check the `perf` checkbox.
Follow this by a run of the `_generate` action to regenerate the plots.

## License

This repo is licensed under the BSD 3-Clause License, as found in the LICENSE file.
