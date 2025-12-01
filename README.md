# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (2f60b8f)](results/bm-20251101-3.15.0a1%2B-2f60b8f/bm-20251101-vultr-x86_64-python-2f60b8f02fe7cb83dd58-3.15.0a1%2B-2f60b8f-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (2f60b8f)](results/bm-20251101-3.15.0a1%2B-2f60b8f-PYTHON_UOPS/bm-20251101-vultr-x86_64-python-2f60b8f02fe7cb83dd58-3.15.0a1%2B-2f60b8f-pystats.md)
- [Most recent JIT pystats on main (bedaea0)](results/bm-20251019-3.15.0a1%2B-bedaea0-JIT/bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-12-01](results/bm-20251201-3.15.0a2%2B-e32c975) | python/main | e32c975 | 1.098x ↑<br>[📄](results/bm-20251201-3.15.0a2%2B-e32c975/bm-20251201-vultr-x86_64-python-main-3.15.0a2%2B-e32c975-vs-3.12.6.md)[📈](results/bm-20251201-3.15.0a2%2B-e32c975/bm-20251201-vultr-x86_64-python-main-3.15.0a2%2B-e32c975-vs-3.12.6.svg) | 1.037x ↑<br>[📄](results/bm-20251201-3.15.0a2%2B-e32c975/bm-20251201-vultr-x86_64-python-main-3.15.0a2%2B-e32c975-vs-3.13.0rc2.md)[📈](results/bm-20251201-3.15.0a2%2B-e32c975/bm-20251201-vultr-x86_64-python-main-3.15.0a2%2B-e32c975-vs-3.13.0rc2.svg) |  |
| [2025-12-01](results/bm-20251201-3.15.0a2%2B-e32c975) | python/e32c9756408a3b88394f | e32c975 | 1.073x ↑<br>[📄](results/bm-20251201-3.15.0a2%2B-e32c975/bm-20251201-vultr-x86_64-python-e32c9756408a3b88394f-3.15.0a2%2B-e32c975-vs-3.12.6.md)[📈](results/bm-20251201-3.15.0a2%2B-e32c975/bm-20251201-vultr-x86_64-python-e32c9756408a3b88394f-3.15.0a2%2B-e32c975-vs-3.12.6.svg) | 1.037x ↑<br>[📄](results/bm-20251201-3.15.0a2%2B-e32c975/bm-20251201-vultr-x86_64-python-e32c9756408a3b88394f-3.15.0a2%2B-e32c975-vs-3.13.0rc2.md)[📈](results/bm-20251201-3.15.0a2%2B-e32c975/bm-20251201-vultr-x86_64-python-e32c9756408a3b88394f-3.15.0a2%2B-e32c975-vs-3.13.0rc2.svg) |  |
| [2025-11-24](results/bm-20251124-3.15.0a2%2B-f96af45-JIT) | Fidget-Spinner/jit_lower_trace_limi | f96af45 (JIT) | 1.093x ↑<br>[📄](results/bm-20251124-3.15.0a2%2B-f96af45-JIT/bm-20251124-vultr-x86_64-Fidget%252dSpinner-jit_lower_trace_limi-3.15.0a2%2B-f96af45-vs-3.12.6.md)[📈](results/bm-20251124-3.15.0a2%2B-f96af45-JIT/bm-20251124-vultr-x86_64-Fidget%252dSpinner-jit_lower_trace_limi-3.15.0a2%2B-f96af45-vs-3.12.6.svg) | 1.056x ↑<br>[📄](results/bm-20251124-3.15.0a2%2B-f96af45-JIT/bm-20251124-vultr-x86_64-Fidget%252dSpinner-jit_lower_trace_limi-3.15.0a2%2B-f96af45-vs-3.13.0rc2.md)[📈](results/bm-20251124-3.15.0a2%2B-f96af45-JIT/bm-20251124-vultr-x86_64-Fidget%252dSpinner-jit_lower_trace_limi-3.15.0a2%2B-f96af45-vs-3.13.0rc2.svg) | 1.042x ↓<br>[📄](results/bm-20251124-3.15.0a2%2B-f96af45-JIT/bm-20251124-vultr-x86_64-Fidget%252dSpinner-jit_lower_trace_limi-3.15.0a2%2B-f96af45-vs-base.md)[📈](results/bm-20251124-3.15.0a2%2B-f96af45-JIT/bm-20251124-vultr-x86_64-Fidget%252dSpinner-jit_lower_trace_limi-3.15.0a2%2B-f96af45-vs-base.svg)[🧠](results/bm-20251124-3.15.0a2%2B-f96af45-JIT/bm-20251124-vultr-x86_64-Fidget%252dSpinner-jit_lower_trace_limi-3.15.0a2%2B-f96af45-vs-base-mem.svg) |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-11-24](results/bm-20251124-3.15.0a2%2B-f96af45-JIT) | Fidget-Spinner/jit_lower_trace_limi | f96af45 (JIT) | 1.162x ↑<br>[📄](results/bm-20251124-3.15.0a2%2B-f96af45-JIT/bm-20251124-macm4pro-arm64-Fidget%252dSpinner-jit_lower_trace_limi-3.15.0a2%2B-f96af45-vs-3.12.6.md)[📈](results/bm-20251124-3.15.0a2%2B-f96af45-JIT/bm-20251124-macm4pro-arm64-Fidget%252dSpinner-jit_lower_trace_limi-3.15.0a2%2B-f96af45-vs-3.12.6.svg) | 1.070x ↑<br>[📄](results/bm-20251124-3.15.0a2%2B-f96af45-JIT/bm-20251124-macm4pro-arm64-Fidget%252dSpinner-jit_lower_trace_limi-3.15.0a2%2B-f96af45-vs-3.13.0rc2.md)[📈](results/bm-20251124-3.15.0a2%2B-f96af45-JIT/bm-20251124-macm4pro-arm64-Fidget%252dSpinner-jit_lower_trace_limi-3.15.0a2%2B-f96af45-vs-3.13.0rc2.svg) | 1.002x ↓<br>[📄](results/bm-20251124-3.15.0a2%2B-f96af45-JIT/bm-20251124-macm4pro-arm64-Fidget%252dSpinner-jit_lower_trace_limi-3.15.0a2%2B-f96af45-vs-base.md)[📈](results/bm-20251124-3.15.0a2%2B-f96af45-JIT/bm-20251124-macm4pro-arm64-Fidget%252dSpinner-jit_lower_trace_limi-3.15.0a2%2B-f96af45-vs-base.svg)[🧠](results/bm-20251124-3.15.0a2%2B-f96af45-JIT/bm-20251124-macm4pro-arm64-Fidget%252dSpinner-jit_lower_trace_limi-3.15.0a2%2B-f96af45-vs-base-mem.svg) |
| [2025-11-24](results/bm-20251124-3.15.0a2%2B-dc62b62-NOGIL) | python/dc62b622524bf49eb539 | dc62b62 (NOGIL) | 1.109x ↑<br>[📄](results/bm-20251124-3.15.0a2%2B-dc62b62-NOGIL/bm-20251124-macm4pro-arm64-python-dc62b622524bf49eb539-3.15.0a2%2B-dc62b62-vs-3.12.6.md)[📈](results/bm-20251124-3.15.0a2%2B-dc62b62-NOGIL/bm-20251124-macm4pro-arm64-python-dc62b622524bf49eb539-3.15.0a2%2B-dc62b62-vs-3.12.6.svg) | 1.023x ↑<br>[📄](results/bm-20251124-3.15.0a2%2B-dc62b62-NOGIL/bm-20251124-macm4pro-arm64-python-dc62b622524bf49eb539-3.15.0a2%2B-dc62b62-vs-3.13.0rc2.md)[📈](results/bm-20251124-3.15.0a2%2B-dc62b62-NOGIL/bm-20251124-macm4pro-arm64-python-dc62b622524bf49eb539-3.15.0a2%2B-dc62b62-vs-3.13.0rc2.svg) | 1.020x ↓<br>[📄](results/bm-20251124-3.15.0a2%2B-dc62b62-NOGIL/bm-20251124-macm4pro-arm64-python-dc62b622524bf49eb539-3.15.0a2%2B-dc62b62-vs-base.md)[📈](results/bm-20251124-3.15.0a2%2B-dc62b62-NOGIL/bm-20251124-macm4pro-arm64-python-dc62b622524bf49eb539-3.15.0a2%2B-dc62b62-vs-base.svg)[🧠](results/bm-20251124-3.15.0a2%2B-dc62b62-NOGIL/bm-20251124-macm4pro-arm64-python-dc62b622524bf49eb539-3.15.0a2%2B-dc62b62-vs-base-mem.svg) |
| [2025-11-24](results/bm-20251124-3.15.0a2%2B-dc62b62-JIT) | python/main | dc62b62 (JIT) | 1.166x ↑<br>[📄](results/bm-20251124-3.15.0a2%2B-dc62b62-JIT/bm-20251124-macm4pro-arm64-python-main-3.15.0a2%2B-dc62b62-vs-3.12.6.md)[📈](results/bm-20251124-3.15.0a2%2B-dc62b62-JIT/bm-20251124-macm4pro-arm64-python-main-3.15.0a2%2B-dc62b62-vs-3.12.6.svg) | 1.073x ↑<br>[📄](results/bm-20251124-3.15.0a2%2B-dc62b62-JIT/bm-20251124-macm4pro-arm64-python-main-3.15.0a2%2B-dc62b62-vs-3.13.0rc2.md)[📈](results/bm-20251124-3.15.0a2%2B-dc62b62-JIT/bm-20251124-macm4pro-arm64-python-main-3.15.0a2%2B-dc62b62-vs-3.13.0rc2.svg) | 1.002x ↓<br>[📄](results/bm-20251124-3.15.0a2%2B-dc62b62-JIT/bm-20251124-macm4pro-arm64-python-main-3.15.0a2%2B-dc62b62-vs-base.md)[📈](results/bm-20251124-3.15.0a2%2B-dc62b62-JIT/bm-20251124-macm4pro-arm64-python-main-3.15.0a2%2B-dc62b62-vs-base.svg)[🧠](results/bm-20251124-3.15.0a2%2B-dc62b62-JIT/bm-20251124-macm4pro-arm64-python-main-3.15.0a2%2B-dc62b62-vs-base-mem.svg) |


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
