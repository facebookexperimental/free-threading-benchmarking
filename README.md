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
| [2024-10-31](results/bm-20241031-3.14.0a1%2B-ac3a2c8-NOGIL) | python/ac3a2c8abceeec448486 | ac3a2c8 (NOGIL) | 1.55x ↓<br>[📄](results/bm-20241031-3.14.0a1%2B-ac3a2c8-NOGIL/bm-20241031-vultr-x86_64-python-ac3a2c8abceeec448486-3.14.0a1%2B-ac3a2c8-vs-3.12.6.md)[📈](results/bm-20241031-3.14.0a1%2B-ac3a2c8-NOGIL/bm-20241031-vultr-x86_64-python-ac3a2c8abceeec448486-3.14.0a1%2B-ac3a2c8-vs-3.12.6.svg) | 1.57x ↓<br>[📄](results/bm-20241031-3.14.0a1%2B-ac3a2c8-NOGIL/bm-20241031-vultr-x86_64-python-ac3a2c8abceeec448486-3.14.0a1%2B-ac3a2c8-vs-3.13.0rc2.md)[📈](results/bm-20241031-3.14.0a1%2B-ac3a2c8-NOGIL/bm-20241031-vultr-x86_64-python-ac3a2c8abceeec448486-3.14.0a1%2B-ac3a2c8-vs-3.13.0rc2.svg) | 1.55x ↓<br>[📄](results/bm-20241031-3.14.0a1%2B-ac3a2c8-NOGIL/bm-20241031-vultr-x86_64-python-ac3a2c8abceeec448486-3.14.0a1%2B-ac3a2c8-vs-base.md)[📈](results/bm-20241031-3.14.0a1%2B-ac3a2c8-NOGIL/bm-20241031-vultr-x86_64-python-ac3a2c8abceeec448486-3.14.0a1%2B-ac3a2c8-vs-base.svg)[🧠](results/bm-20241031-3.14.0a1%2B-ac3a2c8-NOGIL/bm-20241031-vultr-x86_64-python-ac3a2c8abceeec448486-3.14.0a1%2B-ac3a2c8-vs-base-mem.svg) |
| [2024-10-31](results/bm-20241031-3.14.0a1%2B-ac3a2c8) | python/ac3a2c8abceeec448486 | ac3a2c8 | 1.00x ↓<br>[📄](results/bm-20241031-3.14.0a1%2B-ac3a2c8/bm-20241031-vultr-x86_64-python-ac3a2c8abceeec448486-3.14.0a1%2B-ac3a2c8-vs-3.12.6.md)[📈](results/bm-20241031-3.14.0a1%2B-ac3a2c8/bm-20241031-vultr-x86_64-python-ac3a2c8abceeec448486-3.14.0a1%2B-ac3a2c8-vs-3.12.6.svg) | 1.02x ↓<br>[📄](results/bm-20241031-3.14.0a1%2B-ac3a2c8/bm-20241031-vultr-x86_64-python-ac3a2c8abceeec448486-3.14.0a1%2B-ac3a2c8-vs-3.13.0rc2.md)[📈](results/bm-20241031-3.14.0a1%2B-ac3a2c8/bm-20241031-vultr-x86_64-python-ac3a2c8abceeec448486-3.14.0a1%2B-ac3a2c8-vs-3.13.0rc2.svg) |  |
| [2024-10-29](results/bm-20241029-3.14.0a1%2B-d4b6d84) | python/d4b6d84cc84029b598fc | d4b6d84 | 1.00x ↓<br>[📄](results/bm-20241029-3.14.0a1%2B-d4b6d84/bm-20241029-vultr-x86_64-python-d4b6d84cc84029b598fc-3.14.0a1%2B-d4b6d84-vs-3.12.6.md)[📈](results/bm-20241029-3.14.0a1%2B-d4b6d84/bm-20241029-vultr-x86_64-python-d4b6d84cc84029b598fc-3.14.0a1%2B-d4b6d84-vs-3.12.6.svg) | 1.02x ↓<br>[📄](results/bm-20241029-3.14.0a1%2B-d4b6d84/bm-20241029-vultr-x86_64-python-d4b6d84cc84029b598fc-3.14.0a1%2B-d4b6d84-vs-3.13.0rc2.md)[📈](results/bm-20241029-3.14.0a1%2B-d4b6d84/bm-20241029-vultr-x86_64-python-d4b6d84cc84029b598fc-3.14.0a1%2B-d4b6d84-vs-3.13.0rc2.svg) |  |
| [2024-10-29](results/bm-20241029-3.14.0a1%2B-d4b6d84-NOGIL) | python/d4b6d84cc84029b598fc | d4b6d84 (NOGIL) | 1.55x ↓<br>[📄](results/bm-20241029-3.14.0a1%2B-d4b6d84-NOGIL/bm-20241029-vultr-x86_64-python-d4b6d84cc84029b598fc-3.14.0a1%2B-d4b6d84-vs-3.12.6.md)[📈](results/bm-20241029-3.14.0a1%2B-d4b6d84-NOGIL/bm-20241029-vultr-x86_64-python-d4b6d84cc84029b598fc-3.14.0a1%2B-d4b6d84-vs-3.12.6.svg) | 1.58x ↓<br>[📄](results/bm-20241029-3.14.0a1%2B-d4b6d84-NOGIL/bm-20241029-vultr-x86_64-python-d4b6d84cc84029b598fc-3.14.0a1%2B-d4b6d84-vs-3.13.0rc2.md)[📈](results/bm-20241029-3.14.0a1%2B-d4b6d84-NOGIL/bm-20241029-vultr-x86_64-python-d4b6d84cc84029b598fc-3.14.0a1%2B-d4b6d84-vs-3.13.0rc2.svg) | 1.55x ↓<br>[📄](results/bm-20241029-3.14.0a1%2B-d4b6d84-NOGIL/bm-20241029-vultr-x86_64-python-d4b6d84cc84029b598fc-3.14.0a1%2B-d4b6d84-vs-base.md)[📈](results/bm-20241029-3.14.0a1%2B-d4b6d84-NOGIL/bm-20241029-vultr-x86_64-python-d4b6d84cc84029b598fc-3.14.0a1%2B-d4b6d84-vs-base.svg)[🧠](results/bm-20241029-3.14.0a1%2B-d4b6d84-NOGIL/bm-20241029-vultr-x86_64-python-d4b6d84cc84029b598fc-3.14.0a1%2B-d4b6d84-vs-base-mem.svg) |
| [2024-10-28](results/bm-20241028-3.14.0a1%2B-85799f1-NOGIL) | python/85799f1ffd5f285ef93a | 85799f1 (NOGIL) | 1.55x ↓<br>[📄](results/bm-20241028-3.14.0a1%2B-85799f1-NOGIL/bm-20241028-vultr-x86_64-python-85799f1ffd5f285ef93a-3.14.0a1%2B-85799f1-vs-3.12.6.md)[📈](results/bm-20241028-3.14.0a1%2B-85799f1-NOGIL/bm-20241028-vultr-x86_64-python-85799f1ffd5f285ef93a-3.14.0a1%2B-85799f1-vs-3.12.6.svg) | 1.57x ↓<br>[📄](results/bm-20241028-3.14.0a1%2B-85799f1-NOGIL/bm-20241028-vultr-x86_64-python-85799f1ffd5f285ef93a-3.14.0a1%2B-85799f1-vs-3.13.0rc2.md)[📈](results/bm-20241028-3.14.0a1%2B-85799f1-NOGIL/bm-20241028-vultr-x86_64-python-85799f1ffd5f285ef93a-3.14.0a1%2B-85799f1-vs-3.13.0rc2.svg) | 1.55x ↓<br>[📄](results/bm-20241028-3.14.0a1%2B-85799f1-NOGIL/bm-20241028-vultr-x86_64-python-85799f1ffd5f285ef93a-3.14.0a1%2B-85799f1-vs-base.md)[📈](results/bm-20241028-3.14.0a1%2B-85799f1-NOGIL/bm-20241028-vultr-x86_64-python-85799f1ffd5f285ef93a-3.14.0a1%2B-85799f1-vs-base.svg)[🧠](results/bm-20241028-3.14.0a1%2B-85799f1-NOGIL/bm-20241028-vultr-x86_64-python-85799f1ffd5f285ef93a-3.14.0a1%2B-85799f1-vs-base-mem.svg) |
| [2024-10-28](results/bm-20241028-3.14.0a1%2B-85799f1) | python/85799f1ffd5f285ef93a | 85799f1 | 1.00x ↑<br>[📄](results/bm-20241028-3.14.0a1%2B-85799f1/bm-20241028-vultr-x86_64-python-85799f1ffd5f285ef93a-3.14.0a1%2B-85799f1-vs-3.12.6.md)[📈](results/bm-20241028-3.14.0a1%2B-85799f1/bm-20241028-vultr-x86_64-python-85799f1ffd5f285ef93a-3.14.0a1%2B-85799f1-vs-3.12.6.svg) | 1.01x ↓<br>[📄](results/bm-20241028-3.14.0a1%2B-85799f1/bm-20241028-vultr-x86_64-python-85799f1ffd5f285ef93a-3.14.0a1%2B-85799f1-vs-3.13.0rc2.md)[📈](results/bm-20241028-3.14.0a1%2B-85799f1/bm-20241028-vultr-x86_64-python-85799f1ffd5f285ef93a-3.14.0a1%2B-85799f1-vs-3.13.0rc2.svg) |  |
| [2024-10-27](results/bm-20241027-3.14.0a1%2B-19e93e2-NOGIL) | python/19e93e2e269889ecb3c4 | 19e93e2 (NOGIL) | 1.54x ↓<br>[📄](results/bm-20241027-3.14.0a1%2B-19e93e2-NOGIL/bm-20241027-vultr-x86_64-python-19e93e2e269889ecb3c4-3.14.0a1%2B-19e93e2-vs-3.12.6.md)[📈](results/bm-20241027-3.14.0a1%2B-19e93e2-NOGIL/bm-20241027-vultr-x86_64-python-19e93e2e269889ecb3c4-3.14.0a1%2B-19e93e2-vs-3.12.6.svg) | 1.56x ↓<br>[📄](results/bm-20241027-3.14.0a1%2B-19e93e2-NOGIL/bm-20241027-vultr-x86_64-python-19e93e2e269889ecb3c4-3.14.0a1%2B-19e93e2-vs-3.13.0rc2.md)[📈](results/bm-20241027-3.14.0a1%2B-19e93e2-NOGIL/bm-20241027-vultr-x86_64-python-19e93e2e269889ecb3c4-3.14.0a1%2B-19e93e2-vs-3.13.0rc2.svg) | 1.53x ↓<br>[📄](results/bm-20241027-3.14.0a1%2B-19e93e2-NOGIL/bm-20241027-vultr-x86_64-python-19e93e2e269889ecb3c4-3.14.0a1%2B-19e93e2-vs-base.md)[📈](results/bm-20241027-3.14.0a1%2B-19e93e2-NOGIL/bm-20241027-vultr-x86_64-python-19e93e2e269889ecb3c4-3.14.0a1%2B-19e93e2-vs-base.svg)[🧠](results/bm-20241027-3.14.0a1%2B-19e93e2-NOGIL/bm-20241027-vultr-x86_64-python-19e93e2e269889ecb3c4-3.14.0a1%2B-19e93e2-vs-base-mem.svg) |
| [2024-10-27](results/bm-20241027-3.14.0a1%2B-19e93e2) | python/19e93e2e269889ecb3c4 | 19e93e2 | 1.00x ↓<br>[📄](results/bm-20241027-3.14.0a1%2B-19e93e2/bm-20241027-vultr-x86_64-python-19e93e2e269889ecb3c4-3.14.0a1%2B-19e93e2-vs-3.12.6.md)[📈](results/bm-20241027-3.14.0a1%2B-19e93e2/bm-20241027-vultr-x86_64-python-19e93e2e269889ecb3c4-3.14.0a1%2B-19e93e2-vs-3.12.6.svg) | 1.02x ↓<br>[📄](results/bm-20241027-3.14.0a1%2B-19e93e2/bm-20241027-vultr-x86_64-python-19e93e2e269889ecb3c4-3.14.0a1%2B-19e93e2-vs-3.13.0rc2.md)[📈](results/bm-20241027-3.14.0a1%2B-19e93e2/bm-20241027-vultr-x86_64-python-19e93e2e269889ecb3c4-3.14.0a1%2B-19e93e2-vs-3.13.0rc2.svg) |  |
| [2024-10-31](results/bm-20241031-3.14.0a0-0a68813-NOGIL) | mpage/gh_115999_tlbc_integ | 0a68813 (NOGIL) | 1.45x ↓<br>[📄](results/bm-20241031-3.14.0a0-0a68813-NOGIL/bm-20241031-vultr-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813-vs-3.12.6.md)[📈](results/bm-20241031-3.14.0a0-0a68813-NOGIL/bm-20241031-vultr-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813-vs-3.12.6.svg) | 1.47x ↓<br>[📄](results/bm-20241031-3.14.0a0-0a68813-NOGIL/bm-20241031-vultr-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813-vs-3.13.0rc2.md)[📈](results/bm-20241031-3.14.0a0-0a68813-NOGIL/bm-20241031-vultr-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813-vs-3.13.0rc2.svg) | 1.07x ↑<br>[📄](results/bm-20241031-3.14.0a0-0a68813-NOGIL/bm-20241031-vultr-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813-vs-base.md)[📈](results/bm-20241031-3.14.0a0-0a68813-NOGIL/bm-20241031-vultr-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813-vs-base.svg)[🧠](results/bm-20241031-3.14.0a0-0a68813-NOGIL/bm-20241031-vultr-x86_64-mpage-gh_115999_tlbc_integ-3.14.0a0-0a68813-vs-base-mem.svg) |


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
