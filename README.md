# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (880c952)](results/bm-20251004-3.15.0a0-880c952/bm-20251004-vultr-x86_64-python-880c9526f91960b9cba5-3.15.0a0-880c952-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (880c952)](results/bm-20251004-3.15.0a0-880c952-PYTHON_UOPS/bm-20251004-vultr-x86_64-python-880c9526f91960b9cba5-3.15.0a0-880c952-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-10-10](results/bm-20251010-3.15.0a0-ff7bb56-NOGIL) | python/ff7bb565d836162eed08 | ff7bb56 (NOGIL) | 1.019x ↓<br>[📄](results/bm-20251010-3.15.0a0-ff7bb56-NOGIL/bm-20251010-vultr-x86_64-python-ff7bb565d836162eed08-3.15.0a0-ff7bb56-vs-3.12.6.md)[📈](results/bm-20251010-3.15.0a0-ff7bb56-NOGIL/bm-20251010-vultr-x86_64-python-ff7bb565d836162eed08-3.15.0a0-ff7bb56-vs-3.12.6.svg) | 1.053x ↓<br>[📄](results/bm-20251010-3.15.0a0-ff7bb56-NOGIL/bm-20251010-vultr-x86_64-python-ff7bb565d836162eed08-3.15.0a0-ff7bb56-vs-3.13.0rc2.md)[📈](results/bm-20251010-3.15.0a0-ff7bb56-NOGIL/bm-20251010-vultr-x86_64-python-ff7bb565d836162eed08-3.15.0a0-ff7bb56-vs-3.13.0rc2.svg) | 1.090x ↓<br>[📄](results/bm-20251010-3.15.0a0-ff7bb56-NOGIL/bm-20251010-vultr-x86_64-python-ff7bb565d836162eed08-3.15.0a0-ff7bb56-vs-base.md)[📈](results/bm-20251010-3.15.0a0-ff7bb56-NOGIL/bm-20251010-vultr-x86_64-python-ff7bb565d836162eed08-3.15.0a0-ff7bb56-vs-base.svg)[🧠](results/bm-20251010-3.15.0a0-ff7bb56-NOGIL/bm-20251010-vultr-x86_64-python-ff7bb565d836162eed08-3.15.0a0-ff7bb56-vs-base-mem.svg) |
| [2025-10-10](results/bm-20251010-3.15.0a0-ff7bb56) | python/ff7bb565d836162eed08 | ff7bb56 | 1.070x ↑<br>[📄](results/bm-20251010-3.15.0a0-ff7bb56/bm-20251010-vultr-x86_64-python-ff7bb565d836162eed08-3.15.0a0-ff7bb56-vs-3.12.6.md)[📈](results/bm-20251010-3.15.0a0-ff7bb56/bm-20251010-vultr-x86_64-python-ff7bb565d836162eed08-3.15.0a0-ff7bb56-vs-3.12.6.svg) | 1.035x ↑<br>[📄](results/bm-20251010-3.15.0a0-ff7bb56/bm-20251010-vultr-x86_64-python-ff7bb565d836162eed08-3.15.0a0-ff7bb56-vs-3.13.0rc2.md)[📈](results/bm-20251010-3.15.0a0-ff7bb56/bm-20251010-vultr-x86_64-python-ff7bb565d836162eed08-3.15.0a0-ff7bb56-vs-3.13.0rc2.svg) |  |
| [2025-10-10](results/bm-20251010-3.15.0a0-3450311-NOGIL) | python/34503111fe2724986701 | 3450311 (NOGIL) | 1.018x ↓<br>[📄](results/bm-20251010-3.15.0a0-3450311-NOGIL/bm-20251010-vultr-x86_64-python-34503111fe2724986701-3.15.0a0-3450311-vs-3.12.6.md)[📈](results/bm-20251010-3.15.0a0-3450311-NOGIL/bm-20251010-vultr-x86_64-python-34503111fe2724986701-3.15.0a0-3450311-vs-3.12.6.svg) | 1.051x ↓<br>[📄](results/bm-20251010-3.15.0a0-3450311-NOGIL/bm-20251010-vultr-x86_64-python-34503111fe2724986701-3.15.0a0-3450311-vs-3.13.0rc2.md)[📈](results/bm-20251010-3.15.0a0-3450311-NOGIL/bm-20251010-vultr-x86_64-python-34503111fe2724986701-3.15.0a0-3450311-vs-3.13.0rc2.svg) | 1.095x ↓<br>[📄](results/bm-20251010-3.15.0a0-3450311-NOGIL/bm-20251010-vultr-x86_64-python-34503111fe2724986701-3.15.0a0-3450311-vs-base.md)[📈](results/bm-20251010-3.15.0a0-3450311-NOGIL/bm-20251010-vultr-x86_64-python-34503111fe2724986701-3.15.0a0-3450311-vs-base.svg)[🧠](results/bm-20251010-3.15.0a0-3450311-NOGIL/bm-20251010-vultr-x86_64-python-34503111fe2724986701-3.15.0a0-3450311-vs-base-mem.svg) |
| [2025-10-10](results/bm-20251010-3.15.0a0-3450311) | python/34503111fe2724986701 | 3450311 | 1.077x ↑<br>[📄](results/bm-20251010-3.15.0a0-3450311/bm-20251010-vultr-x86_64-python-34503111fe2724986701-3.15.0a0-3450311-vs-3.12.6.md)[📈](results/bm-20251010-3.15.0a0-3450311/bm-20251010-vultr-x86_64-python-34503111fe2724986701-3.15.0a0-3450311-vs-3.12.6.svg) | 1.042x ↑<br>[📄](results/bm-20251010-3.15.0a0-3450311/bm-20251010-vultr-x86_64-python-34503111fe2724986701-3.15.0a0-3450311-vs-3.13.0rc2.md)[📈](results/bm-20251010-3.15.0a0-3450311/bm-20251010-vultr-x86_64-python-34503111fe2724986701-3.15.0a0-3450311-vs-3.13.0rc2.svg) |  |
| [2025-10-09](results/bm-20251009-3.15.0a0-e7e3d1d-NOGIL) | python/e7e3d1d4a8dece01b1bb | e7e3d1d (NOGIL) | 1.016x ↓<br>[📄](results/bm-20251009-3.15.0a0-e7e3d1d-NOGIL/bm-20251009-vultr-x86_64-python-e7e3d1d4a8dece01b1bb-3.15.0a0-e7e3d1d-vs-3.12.6.md)[📈](results/bm-20251009-3.15.0a0-e7e3d1d-NOGIL/bm-20251009-vultr-x86_64-python-e7e3d1d4a8dece01b1bb-3.15.0a0-e7e3d1d-vs-3.12.6.svg) | 1.049x ↓<br>[📄](results/bm-20251009-3.15.0a0-e7e3d1d-NOGIL/bm-20251009-vultr-x86_64-python-e7e3d1d4a8dece01b1bb-3.15.0a0-e7e3d1d-vs-3.13.0rc2.md)[📈](results/bm-20251009-3.15.0a0-e7e3d1d-NOGIL/bm-20251009-vultr-x86_64-python-e7e3d1d4a8dece01b1bb-3.15.0a0-e7e3d1d-vs-3.13.0rc2.svg) | 1.089x ↓<br>[📄](results/bm-20251009-3.15.0a0-e7e3d1d-NOGIL/bm-20251009-vultr-x86_64-python-e7e3d1d4a8dece01b1bb-3.15.0a0-e7e3d1d-vs-base.md)[📈](results/bm-20251009-3.15.0a0-e7e3d1d-NOGIL/bm-20251009-vultr-x86_64-python-e7e3d1d4a8dece01b1bb-3.15.0a0-e7e3d1d-vs-base.svg)[🧠](results/bm-20251009-3.15.0a0-e7e3d1d-NOGIL/bm-20251009-vultr-x86_64-python-e7e3d1d4a8dece01b1bb-3.15.0a0-e7e3d1d-vs-base-mem.svg) |
| [2025-10-09](results/bm-20251009-3.15.0a0-e7e3d1d) | python/e7e3d1d4a8dece01b1bb | e7e3d1d | 1.073x ↑<br>[📄](results/bm-20251009-3.15.0a0-e7e3d1d/bm-20251009-vultr-x86_64-python-e7e3d1d4a8dece01b1bb-3.15.0a0-e7e3d1d-vs-3.12.6.md)[📈](results/bm-20251009-3.15.0a0-e7e3d1d/bm-20251009-vultr-x86_64-python-e7e3d1d4a8dece01b1bb-3.15.0a0-e7e3d1d-vs-3.12.6.svg) | 1.037x ↑<br>[📄](results/bm-20251009-3.15.0a0-e7e3d1d/bm-20251009-vultr-x86_64-python-e7e3d1d4a8dece01b1bb-3.15.0a0-e7e3d1d-vs-3.13.0rc2.md)[📈](results/bm-20251009-3.15.0a0-e7e3d1d/bm-20251009-vultr-x86_64-python-e7e3d1d4a8dece01b1bb-3.15.0a0-e7e3d1d-vs-3.13.0rc2.svg) |  |
| [2025-10-08](results/bm-20251008-3.15.0a0-85ec35d-NOGIL) | python/85ec35d2ab8b764aefd6 | 85ec35d (NOGIL) | 1.016x ↓<br>[📄](results/bm-20251008-3.15.0a0-85ec35d-NOGIL/bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d-vs-3.12.6.md)[📈](results/bm-20251008-3.15.0a0-85ec35d-NOGIL/bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d-vs-3.12.6.svg) | 1.050x ↓<br>[📄](results/bm-20251008-3.15.0a0-85ec35d-NOGIL/bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d-vs-3.13.0rc2.md)[📈](results/bm-20251008-3.15.0a0-85ec35d-NOGIL/bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d-vs-3.13.0rc2.svg) | 1.091x ↓<br>[📄](results/bm-20251008-3.15.0a0-85ec35d-NOGIL/bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d-vs-base.md)[📈](results/bm-20251008-3.15.0a0-85ec35d-NOGIL/bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d-vs-base.svg)[🧠](results/bm-20251008-3.15.0a0-85ec35d-NOGIL/bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d-vs-base-mem.svg) |
| [2025-10-08](results/bm-20251008-3.15.0a0-85ec35d) | python/85ec35d2ab8b764aefd6 | 85ec35d | 1.076x ↑<br>[📄](results/bm-20251008-3.15.0a0-85ec35d/bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d-vs-3.12.6.md)[📈](results/bm-20251008-3.15.0a0-85ec35d/bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d-vs-3.12.6.svg) | 1.040x ↑<br>[📄](results/bm-20251008-3.15.0a0-85ec35d/bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d-vs-3.13.0rc2.md)[📈](results/bm-20251008-3.15.0a0-85ec35d/bm-20251008-vultr-x86_64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-10-08](results/bm-20251008-3.15.0a0-85ec35d-NOGIL) | python/85ec35d2ab8b764aefd6 | 85ec35d (NOGIL) | 1.075x ↑<br>[📄](results/bm-20251008-3.15.0a0-85ec35d-NOGIL/bm-20251008-macm4pro-arm64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d-vs-3.12.6.md)[📈](results/bm-20251008-3.15.0a0-85ec35d-NOGIL/bm-20251008-macm4pro-arm64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d-vs-3.12.6.svg) | 1.003x ↓<br>[📄](results/bm-20251008-3.15.0a0-85ec35d-NOGIL/bm-20251008-macm4pro-arm64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d-vs-3.13.0rc2.md)[📈](results/bm-20251008-3.15.0a0-85ec35d-NOGIL/bm-20251008-macm4pro-arm64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d-vs-3.13.0rc2.svg) | 1.028x ↓<br>[📄](results/bm-20251008-3.15.0a0-85ec35d-NOGIL/bm-20251008-macm4pro-arm64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d-vs-base.md)[📈](results/bm-20251008-3.15.0a0-85ec35d-NOGIL/bm-20251008-macm4pro-arm64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d-vs-base.svg)[🧠](results/bm-20251008-3.15.0a0-85ec35d-NOGIL/bm-20251008-macm4pro-arm64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d-vs-base-mem.svg) |
| [2025-10-08](results/bm-20251008-3.15.0a0-85ec35d) | python/85ec35d2ab8b764aefd6 | 85ec35d | 1.104x ↑<br>[📄](results/bm-20251008-3.15.0a0-85ec35d/bm-20251008-macm4pro-arm64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d-vs-3.12.6.md)[📈](results/bm-20251008-3.15.0a0-85ec35d/bm-20251008-macm4pro-arm64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d-vs-3.12.6.svg) | 1.024x ↑<br>[📄](results/bm-20251008-3.15.0a0-85ec35d/bm-20251008-macm4pro-arm64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d-vs-3.13.0rc2.md)[📈](results/bm-20251008-3.15.0a0-85ec35d/bm-20251008-macm4pro-arm64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d-vs-3.13.0rc2.svg) |  |
| [2025-10-06](results/bm-20251006-3.15.0a0-3311580-NOGIL) | python/331158065b7426a79121 | 3311580 (NOGIL) | 1.076x ↑<br>[📄](results/bm-20251006-3.15.0a0-3311580-NOGIL/bm-20251006-macm4pro-arm64-python-331158065b7426a79121-3.15.0a0-3311580-vs-3.12.6.md)[📈](results/bm-20251006-3.15.0a0-3311580-NOGIL/bm-20251006-macm4pro-arm64-python-331158065b7426a79121-3.15.0a0-3311580-vs-3.12.6.svg) | 1.002x ↓<br>[📄](results/bm-20251006-3.15.0a0-3311580-NOGIL/bm-20251006-macm4pro-arm64-python-331158065b7426a79121-3.15.0a0-3311580-vs-3.13.0rc2.md)[📈](results/bm-20251006-3.15.0a0-3311580-NOGIL/bm-20251006-macm4pro-arm64-python-331158065b7426a79121-3.15.0a0-3311580-vs-3.13.0rc2.svg) | 1.023x ↓<br>[📄](results/bm-20251006-3.15.0a0-3311580-NOGIL/bm-20251006-macm4pro-arm64-python-331158065b7426a79121-3.15.0a0-3311580-vs-base.md)[📈](results/bm-20251006-3.15.0a0-3311580-NOGIL/bm-20251006-macm4pro-arm64-python-331158065b7426a79121-3.15.0a0-3311580-vs-base.svg)[🧠](results/bm-20251006-3.15.0a0-3311580-NOGIL/bm-20251006-macm4pro-arm64-python-331158065b7426a79121-3.15.0a0-3311580-vs-base-mem.svg) |


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
