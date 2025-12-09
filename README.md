# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (572c780)](results/bm-20251206-3.15.0a2%2B-572c780/bm-20251206-vultr-x86_64-python-572c780aa875e4eb0096-3.15.0a2%2B-572c780-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (572c780)](results/bm-20251206-3.15.0a2%2B-572c780-PYTHON_UOPS/bm-20251206-vultr-x86_64-python-572c780aa875e4eb0096-3.15.0a2%2B-572c780-pystats.md)
- [Most recent JIT pystats on main (bedaea0)](results/bm-20251019-3.15.0a1%2B-bedaea0-JIT/bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-12-07](results/bm-20251207-3.15.0a2%2B-ef51a7c-NOGIL) | python/ef51a7c8f3f4511ad18e | ef51a7c (NOGIL) | 1.037x ↓<br>[📄](results/bm-20251207-3.15.0a2%2B-ef51a7c-NOGIL/bm-20251207-vultr-x86_64-python-ef51a7c8f3f4511ad18e-3.15.0a2%2B-ef51a7c-vs-3.12.6.md)[📈](results/bm-20251207-3.15.0a2%2B-ef51a7c-NOGIL/bm-20251207-vultr-x86_64-python-ef51a7c8f3f4511ad18e-3.15.0a2%2B-ef51a7c-vs-3.12.6.svg) | 1.070x ↓<br>[📄](results/bm-20251207-3.15.0a2%2B-ef51a7c-NOGIL/bm-20251207-vultr-x86_64-python-ef51a7c8f3f4511ad18e-3.15.0a2%2B-ef51a7c-vs-3.13.0rc2.md)[📈](results/bm-20251207-3.15.0a2%2B-ef51a7c-NOGIL/bm-20251207-vultr-x86_64-python-ef51a7c8f3f4511ad18e-3.15.0a2%2B-ef51a7c-vs-3.13.0rc2.svg) | 1.109x ↓<br>[📄](results/bm-20251207-3.15.0a2%2B-ef51a7c-NOGIL/bm-20251207-vultr-x86_64-python-ef51a7c8f3f4511ad18e-3.15.0a2%2B-ef51a7c-vs-base.md)[📈](results/bm-20251207-3.15.0a2%2B-ef51a7c-NOGIL/bm-20251207-vultr-x86_64-python-ef51a7c8f3f4511ad18e-3.15.0a2%2B-ef51a7c-vs-base.svg)[🧠](results/bm-20251207-3.15.0a2%2B-ef51a7c-NOGIL/bm-20251207-vultr-x86_64-python-ef51a7c8f3f4511ad18e-3.15.0a2%2B-ef51a7c-vs-base-mem.svg) |
| [2025-12-07](results/bm-20251207-3.15.0a2%2B-ef51a7c) | python/ef51a7c8f3f4511ad18e | ef51a7c | 1.075x ↑<br>[📄](results/bm-20251207-3.15.0a2%2B-ef51a7c/bm-20251207-vultr-x86_64-python-ef51a7c8f3f4511ad18e-3.15.0a2%2B-ef51a7c-vs-3.12.6.md)[📈](results/bm-20251207-3.15.0a2%2B-ef51a7c/bm-20251207-vultr-x86_64-python-ef51a7c8f3f4511ad18e-3.15.0a2%2B-ef51a7c-vs-3.12.6.svg) | 1.040x ↑<br>[📄](results/bm-20251207-3.15.0a2%2B-ef51a7c/bm-20251207-vultr-x86_64-python-ef51a7c8f3f4511ad18e-3.15.0a2%2B-ef51a7c-vs-3.13.0rc2.md)[📈](results/bm-20251207-3.15.0a2%2B-ef51a7c/bm-20251207-vultr-x86_64-python-ef51a7c8f3f4511ad18e-3.15.0a2%2B-ef51a7c-vs-3.13.0rc2.svg) |  |
| [2025-12-06](results/bm-20251206-3.15.0a2%2B-572c780-NOGIL) | python/572c780aa875e4eb0096 | 572c780 (NOGIL) | 1.037x ↓<br>[📄](results/bm-20251206-3.15.0a2%2B-572c780-NOGIL/bm-20251206-vultr-x86_64-python-572c780aa875e4eb0096-3.15.0a2%2B-572c780-vs-3.12.6.md)[📈](results/bm-20251206-3.15.0a2%2B-572c780-NOGIL/bm-20251206-vultr-x86_64-python-572c780aa875e4eb0096-3.15.0a2%2B-572c780-vs-3.12.6.svg) | 1.070x ↓<br>[📄](results/bm-20251206-3.15.0a2%2B-572c780-NOGIL/bm-20251206-vultr-x86_64-python-572c780aa875e4eb0096-3.15.0a2%2B-572c780-vs-3.13.0rc2.md)[📈](results/bm-20251206-3.15.0a2%2B-572c780-NOGIL/bm-20251206-vultr-x86_64-python-572c780aa875e4eb0096-3.15.0a2%2B-572c780-vs-3.13.0rc2.svg) | 1.109x ↓<br>[📄](results/bm-20251206-3.15.0a2%2B-572c780-NOGIL/bm-20251206-vultr-x86_64-python-572c780aa875e4eb0096-3.15.0a2%2B-572c780-vs-base.md)[📈](results/bm-20251206-3.15.0a2%2B-572c780-NOGIL/bm-20251206-vultr-x86_64-python-572c780aa875e4eb0096-3.15.0a2%2B-572c780-vs-base.svg)[🧠](results/bm-20251206-3.15.0a2%2B-572c780-NOGIL/bm-20251206-vultr-x86_64-python-572c780aa875e4eb0096-3.15.0a2%2B-572c780-vs-base-mem.svg) |
| [2025-12-06](results/bm-20251206-3.15.0a2%2B-572c780-JIT) | python/572c780aa875e4eb0096 | 572c780 (JIT) | 1.105x ↑<br>[📄](results/bm-20251206-3.15.0a2%2B-572c780-JIT/bm-20251206-vultr-x86_64-python-572c780aa875e4eb0096-3.15.0a2%2B-572c780-vs-3.12.6.md)[📈](results/bm-20251206-3.15.0a2%2B-572c780-JIT/bm-20251206-vultr-x86_64-python-572c780aa875e4eb0096-3.15.0a2%2B-572c780-vs-3.12.6.svg) | 1.068x ↑<br>[📄](results/bm-20251206-3.15.0a2%2B-572c780-JIT/bm-20251206-vultr-x86_64-python-572c780aa875e4eb0096-3.15.0a2%2B-572c780-vs-3.13.0rc2.md)[📈](results/bm-20251206-3.15.0a2%2B-572c780-JIT/bm-20251206-vultr-x86_64-python-572c780aa875e4eb0096-3.15.0a2%2B-572c780-vs-3.13.0rc2.svg) | 1.023x ↑<br>[📄](results/bm-20251206-3.15.0a2%2B-572c780-JIT/bm-20251206-vultr-x86_64-python-572c780aa875e4eb0096-3.15.0a2%2B-572c780-vs-base.md)[📈](results/bm-20251206-3.15.0a2%2B-572c780-JIT/bm-20251206-vultr-x86_64-python-572c780aa875e4eb0096-3.15.0a2%2B-572c780-vs-base.svg)[🧠](results/bm-20251206-3.15.0a2%2B-572c780-JIT/bm-20251206-vultr-x86_64-python-572c780aa875e4eb0096-3.15.0a2%2B-572c780-vs-base-mem.svg) |
| [2025-12-06](results/bm-20251206-3.15.0a2%2B-572c780-CLANG) | python/572c780aa875e4eb0096 | 572c780 (CLANG) | 1.131x ↑<br>[📄](results/bm-20251206-3.15.0a2%2B-572c780-CLANG/bm-20251206-vultr-x86_64-python-572c780aa875e4eb0096-3.15.0a2%2B-572c780-vs-3.12.6.md)[📈](results/bm-20251206-3.15.0a2%2B-572c780-CLANG/bm-20251206-vultr-x86_64-python-572c780aa875e4eb0096-3.15.0a2%2B-572c780-vs-3.12.6.svg) | 1.093x ↑<br>[📄](results/bm-20251206-3.15.0a2%2B-572c780-CLANG/bm-20251206-vultr-x86_64-python-572c780aa875e4eb0096-3.15.0a2%2B-572c780-vs-3.13.0rc2.md)[📈](results/bm-20251206-3.15.0a2%2B-572c780-CLANG/bm-20251206-vultr-x86_64-python-572c780aa875e4eb0096-3.15.0a2%2B-572c780-vs-3.13.0rc2.svg) | 1.049x ↑<br>[📄](results/bm-20251206-3.15.0a2%2B-572c780-CLANG/bm-20251206-vultr-x86_64-python-572c780aa875e4eb0096-3.15.0a2%2B-572c780-vs-base.md)[📈](results/bm-20251206-3.15.0a2%2B-572c780-CLANG/bm-20251206-vultr-x86_64-python-572c780aa875e4eb0096-3.15.0a2%2B-572c780-vs-base.svg)[🧠](results/bm-20251206-3.15.0a2%2B-572c780-CLANG/bm-20251206-vultr-x86_64-python-572c780aa875e4eb0096-3.15.0a2%2B-572c780-vs-base-mem.svg) |
| [2025-12-06](results/bm-20251206-3.15.0a2%2B-572c780) | python/572c780aa875e4eb0096 | 572c780 | 1.076x ↑<br>[📄](results/bm-20251206-3.15.0a2%2B-572c780/bm-20251206-vultr-x86_64-python-572c780aa875e4eb0096-3.15.0a2%2B-572c780-vs-3.12.6.md)[📈](results/bm-20251206-3.15.0a2%2B-572c780/bm-20251206-vultr-x86_64-python-572c780aa875e4eb0096-3.15.0a2%2B-572c780-vs-3.12.6.svg) | 1.040x ↑<br>[📄](results/bm-20251206-3.15.0a2%2B-572c780/bm-20251206-vultr-x86_64-python-572c780aa875e4eb0096-3.15.0a2%2B-572c780-vs-3.13.0rc2.md)[📈](results/bm-20251206-3.15.0a2%2B-572c780/bm-20251206-vultr-x86_64-python-572c780aa875e4eb0096-3.15.0a2%2B-572c780-vs-3.13.0rc2.svg) |  |
| [2025-12-05](results/bm-20251205-3.15.0a2%2B-eba449a-NOGIL) | python/eba449a1989265a92317 | eba449a (NOGIL) | 1.033x ↓<br>[📄](results/bm-20251205-3.15.0a2%2B-eba449a-NOGIL/bm-20251205-vultr-x86_64-python-eba449a1989265a92317-3.15.0a2%2B-eba449a-vs-3.12.6.md)[📈](results/bm-20251205-3.15.0a2%2B-eba449a-NOGIL/bm-20251205-vultr-x86_64-python-eba449a1989265a92317-3.15.0a2%2B-eba449a-vs-3.12.6.svg) | 1.066x ↓<br>[📄](results/bm-20251205-3.15.0a2%2B-eba449a-NOGIL/bm-20251205-vultr-x86_64-python-eba449a1989265a92317-3.15.0a2%2B-eba449a-vs-3.13.0rc2.md)[📈](results/bm-20251205-3.15.0a2%2B-eba449a-NOGIL/bm-20251205-vultr-x86_64-python-eba449a1989265a92317-3.15.0a2%2B-eba449a-vs-3.13.0rc2.svg) | 1.110x ↓<br>[📄](results/bm-20251205-3.15.0a2%2B-eba449a-NOGIL/bm-20251205-vultr-x86_64-python-eba449a1989265a92317-3.15.0a2%2B-eba449a-vs-base.md)[📈](results/bm-20251205-3.15.0a2%2B-eba449a-NOGIL/bm-20251205-vultr-x86_64-python-eba449a1989265a92317-3.15.0a2%2B-eba449a-vs-base.svg)[🧠](results/bm-20251205-3.15.0a2%2B-eba449a-NOGIL/bm-20251205-vultr-x86_64-python-eba449a1989265a92317-3.15.0a2%2B-eba449a-vs-base-mem.svg) |
| [2025-12-05](results/bm-20251205-3.15.0a2%2B-eba449a) | python/eba449a1989265a92317 | eba449a | 1.081x ↑<br>[📄](results/bm-20251205-3.15.0a2%2B-eba449a/bm-20251205-vultr-x86_64-python-eba449a1989265a92317-3.15.0a2%2B-eba449a-vs-3.12.6.md)[📈](results/bm-20251205-3.15.0a2%2B-eba449a/bm-20251205-vultr-x86_64-python-eba449a1989265a92317-3.15.0a2%2B-eba449a-vs-3.12.6.svg) | 1.045x ↑<br>[📄](results/bm-20251205-3.15.0a2%2B-eba449a/bm-20251205-vultr-x86_64-python-eba449a1989265a92317-3.15.0a2%2B-eba449a-vs-3.13.0rc2.md)[📈](results/bm-20251205-3.15.0a2%2B-eba449a/bm-20251205-vultr-x86_64-python-eba449a1989265a92317-3.15.0a2%2B-eba449a-vs-3.13.0rc2.svg) |  |

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
