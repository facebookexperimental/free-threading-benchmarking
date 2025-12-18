# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (6cddf04)](results/bm-20251214-3.15.0a2%2B-6cddf04/bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2%2B-6cddf04-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (6cddf04)](results/bm-20251214-3.15.0a2%2B-6cddf04-PYTHON_UOPS/bm-20251214-vultr-x86_64-python-6cddf04344a1e8ca9df5-3.15.0a2%2B-6cddf04-pystats.md)
- [Most recent JIT pystats on main (bedaea0)](results/bm-20251019-3.15.0a1%2B-bedaea0-JIT/bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-12-17](results/bm-20251217-3.15.0a3%2B-2f39aa8-JIT%2CNOGIL) | Fidget-Spinner/jit_ft | 2f39aa8 (JIT) (NOGIL) | 1.008x ↓<br>[📄](results/bm-20251217-3.15.0a3%2B-2f39aa8-JIT%2CNOGIL/bm-20251217-vultr-x86_64-Fidget%252dSpinner-jit_ft-3.15.0a3%2B-2f39aa8-vs-3.12.6.md)[📈](results/bm-20251217-3.15.0a3%2B-2f39aa8-JIT%2CNOGIL/bm-20251217-vultr-x86_64-Fidget%252dSpinner-jit_ft-3.15.0a3%2B-2f39aa8-vs-3.12.6.svg) | 1.040x ↓<br>[📄](results/bm-20251217-3.15.0a3%2B-2f39aa8-JIT%2CNOGIL/bm-20251217-vultr-x86_64-Fidget%252dSpinner-jit_ft-3.15.0a3%2B-2f39aa8-vs-3.13.0rc2.md)[📈](results/bm-20251217-3.15.0a3%2B-2f39aa8-JIT%2CNOGIL/bm-20251217-vultr-x86_64-Fidget%252dSpinner-jit_ft-3.15.0a3%2B-2f39aa8-vs-3.13.0rc2.svg) |  |
| [2025-12-17](results/bm-20251217-3.15.0a3%2B-89729f2-NOGIL) | python/89729f2ef7f9473d9e4b | 89729f2 (NOGIL) | 1.021x ↓<br>[📄](results/bm-20251217-3.15.0a3%2B-89729f2-NOGIL/bm-20251217-vultr-x86_64-python-89729f2ef7f9473d9e4b-3.15.0a3%2B-89729f2-vs-3.12.6.md)[📈](results/bm-20251217-3.15.0a3%2B-89729f2-NOGIL/bm-20251217-vultr-x86_64-python-89729f2ef7f9473d9e4b-3.15.0a3%2B-89729f2-vs-3.12.6.svg) | 1.055x ↓<br>[📄](results/bm-20251217-3.15.0a3%2B-89729f2-NOGIL/bm-20251217-vultr-x86_64-python-89729f2ef7f9473d9e4b-3.15.0a3%2B-89729f2-vs-3.13.0rc2.md)[📈](results/bm-20251217-3.15.0a3%2B-89729f2-NOGIL/bm-20251217-vultr-x86_64-python-89729f2ef7f9473d9e4b-3.15.0a3%2B-89729f2-vs-3.13.0rc2.svg) | 1.098x ↓<br>[📄](results/bm-20251217-3.15.0a3%2B-89729f2-NOGIL/bm-20251217-vultr-x86_64-python-89729f2ef7f9473d9e4b-3.15.0a3%2B-89729f2-vs-base.md)[📈](results/bm-20251217-3.15.0a3%2B-89729f2-NOGIL/bm-20251217-vultr-x86_64-python-89729f2ef7f9473d9e4b-3.15.0a3%2B-89729f2-vs-base.svg)[🧠](results/bm-20251217-3.15.0a3%2B-89729f2-NOGIL/bm-20251217-vultr-x86_64-python-89729f2ef7f9473d9e4b-3.15.0a3%2B-89729f2-vs-base-mem.svg) |
| [2025-12-17](results/bm-20251217-3.15.0a3%2B-89729f2) | python/89729f2ef7f9473d9e4b | 89729f2 | 1.078x ↑<br>[📄](results/bm-20251217-3.15.0a3%2B-89729f2/bm-20251217-vultr-x86_64-python-89729f2ef7f9473d9e4b-3.15.0a3%2B-89729f2-vs-3.12.6.md)[📈](results/bm-20251217-3.15.0a3%2B-89729f2/bm-20251217-vultr-x86_64-python-89729f2ef7f9473d9e4b-3.15.0a3%2B-89729f2-vs-3.12.6.svg) | 1.042x ↑<br>[📄](results/bm-20251217-3.15.0a3%2B-89729f2/bm-20251217-vultr-x86_64-python-89729f2ef7f9473d9e4b-3.15.0a3%2B-89729f2-vs-3.13.0rc2.md)[📈](results/bm-20251217-3.15.0a3%2B-89729f2/bm-20251217-vultr-x86_64-python-89729f2ef7f9473d9e4b-3.15.0a3%2B-89729f2-vs-3.13.0rc2.svg) |  |
| [2025-12-16](results/bm-20251216-3.15.0a3%2B-16a305f-CLANG%2CNOGIL) | python/16a305f15242ed2acac9 | 16a305f (CLANG) (NOGIL) | 1.026x ↑<br>[📄](results/bm-20251216-3.15.0a3%2B-16a305f-CLANG%2CNOGIL/bm-20251216-vultr-x86_64-python-16a305f15242ed2acac9-3.15.0a3%2B-16a305f-vs-3.12.6.md)[📈](results/bm-20251216-3.15.0a3%2B-16a305f-CLANG%2CNOGIL/bm-20251216-vultr-x86_64-python-16a305f15242ed2acac9-3.15.0a3%2B-16a305f-vs-3.12.6.svg) | 1.008x ↓<br>[📄](results/bm-20251216-3.15.0a3%2B-16a305f-CLANG%2CNOGIL/bm-20251216-vultr-x86_64-python-16a305f15242ed2acac9-3.15.0a3%2B-16a305f-vs-3.13.0rc2.md)[📈](results/bm-20251216-3.15.0a3%2B-16a305f-CLANG%2CNOGIL/bm-20251216-vultr-x86_64-python-16a305f15242ed2acac9-3.15.0a3%2B-16a305f-vs-3.13.0rc2.svg) |  |
| [2025-12-16](results/bm-20251216-3.15.0a3%2B-afd3eff-CLANG%2CNOGIL) | colesbury/gh_129068_rangeiter_ | afd3eff (CLANG) (NOGIL) | 1.025x ↑<br>[📄](results/bm-20251216-3.15.0a3%2B-afd3eff-CLANG%2CNOGIL/bm-20251216-vultr-x86_64-colesbury-gh_129068_rangeiter_-3.15.0a3%2B-afd3eff-vs-3.12.6.md)[📈](results/bm-20251216-3.15.0a3%2B-afd3eff-CLANG%2CNOGIL/bm-20251216-vultr-x86_64-colesbury-gh_129068_rangeiter_-3.15.0a3%2B-afd3eff-vs-3.12.6.svg) | 1.009x ↓<br>[📄](results/bm-20251216-3.15.0a3%2B-afd3eff-CLANG%2CNOGIL/bm-20251216-vultr-x86_64-colesbury-gh_129068_rangeiter_-3.15.0a3%2B-afd3eff-vs-3.13.0rc2.md)[📈](results/bm-20251216-3.15.0a3%2B-afd3eff-CLANG%2CNOGIL/bm-20251216-vultr-x86_64-colesbury-gh_129068_rangeiter_-3.15.0a3%2B-afd3eff-vs-3.13.0rc2.svg) | 1.001x ↑<br>[📄](results/bm-20251216-3.15.0a3%2B-afd3eff-CLANG%2CNOGIL/bm-20251216-vultr-x86_64-colesbury-gh_129068_rangeiter_-3.15.0a3%2B-afd3eff-vs-base.md)[📈](results/bm-20251216-3.15.0a3%2B-afd3eff-CLANG%2CNOGIL/bm-20251216-vultr-x86_64-colesbury-gh_129068_rangeiter_-3.15.0a3%2B-afd3eff-vs-base.svg)[🧠](results/bm-20251216-3.15.0a3%2B-afd3eff-CLANG%2CNOGIL/bm-20251216-vultr-x86_64-colesbury-gh_129068_rangeiter_-3.15.0a3%2B-afd3eff-vs-base-mem.svg) |
| [2025-12-15](results/bm-20251215-3.15.0a2%2B-bef63d2-NOGIL) | python/bef63d2fb81ae2876004 | bef63d2 (NOGIL) | 1.031x ↓<br>[📄](results/bm-20251215-3.15.0a2%2B-bef63d2-NOGIL/bm-20251215-vultr-x86_64-python-bef63d2fb81ae2876004-3.15.0a2%2B-bef63d2-vs-3.12.6.md)[📈](results/bm-20251215-3.15.0a2%2B-bef63d2-NOGIL/bm-20251215-vultr-x86_64-python-bef63d2fb81ae2876004-3.15.0a2%2B-bef63d2-vs-3.12.6.svg) | 1.064x ↓<br>[📄](results/bm-20251215-3.15.0a2%2B-bef63d2-NOGIL/bm-20251215-vultr-x86_64-python-bef63d2fb81ae2876004-3.15.0a2%2B-bef63d2-vs-3.13.0rc2.md)[📈](results/bm-20251215-3.15.0a2%2B-bef63d2-NOGIL/bm-20251215-vultr-x86_64-python-bef63d2fb81ae2876004-3.15.0a2%2B-bef63d2-vs-3.13.0rc2.svg) | 1.100x ↓<br>[📄](results/bm-20251215-3.15.0a2%2B-bef63d2-NOGIL/bm-20251215-vultr-x86_64-python-bef63d2fb81ae2876004-3.15.0a2%2B-bef63d2-vs-base.md)[📈](results/bm-20251215-3.15.0a2%2B-bef63d2-NOGIL/bm-20251215-vultr-x86_64-python-bef63d2fb81ae2876004-3.15.0a2%2B-bef63d2-vs-base.svg)[🧠](results/bm-20251215-3.15.0a2%2B-bef63d2-NOGIL/bm-20251215-vultr-x86_64-python-bef63d2fb81ae2876004-3.15.0a2%2B-bef63d2-vs-base-mem.svg) |
| [2025-12-15](results/bm-20251215-3.15.0a2%2B-bef63d2) | python/bef63d2fb81ae2876004 | bef63d2 | 1.072x ↑<br>[📄](results/bm-20251215-3.15.0a2%2B-bef63d2/bm-20251215-vultr-x86_64-python-bef63d2fb81ae2876004-3.15.0a2%2B-bef63d2-vs-3.12.6.md)[📈](results/bm-20251215-3.15.0a2%2B-bef63d2/bm-20251215-vultr-x86_64-python-bef63d2fb81ae2876004-3.15.0a2%2B-bef63d2-vs-3.12.6.svg) | 1.036x ↑<br>[📄](results/bm-20251215-3.15.0a2%2B-bef63d2/bm-20251215-vultr-x86_64-python-bef63d2fb81ae2876004-3.15.0a2%2B-bef63d2-vs-3.13.0rc2.md)[📈](results/bm-20251215-3.15.0a2%2B-bef63d2/bm-20251215-vultr-x86_64-python-bef63d2fb81ae2876004-3.15.0a2%2B-bef63d2-vs-3.13.0rc2.svg) |  |
| [2025-12-14](results/bm-20251214-3.15.0a2%2B-d844d22-NOGIL) | python/d844d22cb00e4a8a224a | d844d22 (NOGIL) | 1.039x ↓<br>[📄](results/bm-20251214-3.15.0a2%2B-d844d22-NOGIL/bm-20251214-vultr-x86_64-python-d844d22cb00e4a8a224a-3.15.0a2%2B-d844d22-vs-3.12.6.md)[📈](results/bm-20251214-3.15.0a2%2B-d844d22-NOGIL/bm-20251214-vultr-x86_64-python-d844d22cb00e4a8a224a-3.15.0a2%2B-d844d22-vs-3.12.6.svg) | 1.072x ↓<br>[📄](results/bm-20251214-3.15.0a2%2B-d844d22-NOGIL/bm-20251214-vultr-x86_64-python-d844d22cb00e4a8a224a-3.15.0a2%2B-d844d22-vs-3.13.0rc2.md)[📈](results/bm-20251214-3.15.0a2%2B-d844d22-NOGIL/bm-20251214-vultr-x86_64-python-d844d22cb00e4a8a224a-3.15.0a2%2B-d844d22-vs-3.13.0rc2.svg) | 1.111x ↓<br>[📄](results/bm-20251214-3.15.0a2%2B-d844d22-NOGIL/bm-20251214-vultr-x86_64-python-d844d22cb00e4a8a224a-3.15.0a2%2B-d844d22-vs-base.md)[📈](results/bm-20251214-3.15.0a2%2B-d844d22-NOGIL/bm-20251214-vultr-x86_64-python-d844d22cb00e4a8a224a-3.15.0a2%2B-d844d22-vs-base.svg)[🧠](results/bm-20251214-3.15.0a2%2B-d844d22-NOGIL/bm-20251214-vultr-x86_64-python-d844d22cb00e4a8a224a-3.15.0a2%2B-d844d22-vs-base-mem.svg) |
| [2025-12-14](results/bm-20251214-3.15.0a2%2B-d844d22) | python/d844d22cb00e4a8a224a | d844d22 | 1.075x ↑<br>[📄](results/bm-20251214-3.15.0a2%2B-d844d22/bm-20251214-vultr-x86_64-python-d844d22cb00e4a8a224a-3.15.0a2%2B-d844d22-vs-3.12.6.md)[📈](results/bm-20251214-3.15.0a2%2B-d844d22/bm-20251214-vultr-x86_64-python-d844d22cb00e4a8a224a-3.15.0a2%2B-d844d22-vs-3.12.6.svg) | 1.040x ↑<br>[📄](results/bm-20251214-3.15.0a2%2B-d844d22/bm-20251214-vultr-x86_64-python-d844d22cb00e4a8a224a-3.15.0a2%2B-d844d22-vs-3.13.0rc2.md)[📈](results/bm-20251214-3.15.0a2%2B-d844d22/bm-20251214-vultr-x86_64-python-d844d22cb00e4a8a224a-3.15.0a2%2B-d844d22-vs-3.13.0rc2.svg) |  |

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
