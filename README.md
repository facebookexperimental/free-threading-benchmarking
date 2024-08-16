# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
## linux x86_64 (linux)
| date | fork/ref | hash/flags | vs. 3.12.0b1: | vs. 3.12.5+: | vs. 3.13.0b1: | vs. 3.13.0rc1+: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: | ---: | ---: |
| [2024-08-15](results/bm-20240815-3.14.0a0-d7a3df9) | python/d7a3df91505faa56c51d | d7a3df9 | 1.06x ↑<br>[📄](results/bm-20240815-3.14.0a0-d7a3df9/bm-20240815-linux-x86_64-python-d7a3df91505faa56c51d-3.14.0a0-d7a3df9-vs-3.12.0b1.md)[📈](results/bm-20240815-3.14.0a0-d7a3df9/bm-20240815-linux-x86_64-python-d7a3df91505faa56c51d-3.14.0a0-d7a3df9-vs-3.12.0b1.svg) | 1.05x ↑<br>[📄](results/bm-20240815-3.14.0a0-d7a3df9/bm-20240815-linux-x86_64-python-d7a3df91505faa56c51d-3.14.0a0-d7a3df9-vs-3.12.5%2B.md)[📈](results/bm-20240815-3.14.0a0-d7a3df9/bm-20240815-linux-x86_64-python-d7a3df91505faa56c51d-3.14.0a0-d7a3df9-vs-3.12.5%2B.svg) | 1.05x ↑<br>[📄](results/bm-20240815-3.14.0a0-d7a3df9/bm-20240815-linux-x86_64-python-d7a3df91505faa56c51d-3.14.0a0-d7a3df9-vs-3.13.0b1.md)[📈](results/bm-20240815-3.14.0a0-d7a3df9/bm-20240815-linux-x86_64-python-d7a3df91505faa56c51d-3.14.0a0-d7a3df9-vs-3.13.0b1.svg) | 1.01x ↑<br>[📄](results/bm-20240815-3.14.0a0-d7a3df9/bm-20240815-linux-x86_64-python-d7a3df91505faa56c51d-3.14.0a0-d7a3df9-vs-3.13.0rc1%2B.md)[📈](results/bm-20240815-3.14.0a0-d7a3df9/bm-20240815-linux-x86_64-python-d7a3df91505faa56c51d-3.14.0a0-d7a3df9-vs-3.13.0rc1%2B.svg) |  |
| [2024-08-15](results/bm-20240815-3.14.0a0-e001027-NOGIL) | python/main | e001027 (NOGIL) | 1.39x ↓<br>[📄](results/bm-20240815-3.14.0a0-e001027-NOGIL/bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027-vs-3.12.0b1.md)[📈](results/bm-20240815-3.14.0a0-e001027-NOGIL/bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027-vs-3.12.0b1.svg) | 1.41x ↓<br>[📄](results/bm-20240815-3.14.0a0-e001027-NOGIL/bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027-vs-3.12.5%2B.md)[📈](results/bm-20240815-3.14.0a0-e001027-NOGIL/bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027-vs-3.12.5%2B.svg) | 1.40x ↓<br>[📄](results/bm-20240815-3.14.0a0-e001027-NOGIL/bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027-vs-3.13.0b1.md)[📈](results/bm-20240815-3.14.0a0-e001027-NOGIL/bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027-vs-3.13.0b1.svg) | 1.45x ↓<br>[📄](results/bm-20240815-3.14.0a0-e001027-NOGIL/bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027-vs-3.13.0rc1%2B.md)[📈](results/bm-20240815-3.14.0a0-e001027-NOGIL/bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027-vs-3.13.0rc1%2B.svg) | 1.01x ↓<br>[📄](results/bm-20240815-3.14.0a0-e001027-NOGIL/bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027-vs-base.md)[📈](results/bm-20240815-3.14.0a0-e001027-NOGIL/bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027-vs-base.svg)[🧠](results/bm-20240815-3.14.0a0-e001027-NOGIL/bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027-vs-base-mem.svg) |
| [2024-08-15](results/bm-20240815-3.14.0a0-e913d2c) | python/main | e913d2c | 1.05x ↑<br>[📄](results/bm-20240815-3.14.0a0-e913d2c/bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c-vs-3.12.0b1.md)[📈](results/bm-20240815-3.14.0a0-e913d2c/bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c-vs-3.12.0b1.svg) | 1.04x ↑<br>[📄](results/bm-20240815-3.14.0a0-e913d2c/bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c-vs-3.12.5%2B.md)[📈](results/bm-20240815-3.14.0a0-e913d2c/bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c-vs-3.12.5%2B.svg) | 1.05x ↑<br>[📄](results/bm-20240815-3.14.0a0-e913d2c/bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c-vs-3.13.0b1.md)[📈](results/bm-20240815-3.14.0a0-e913d2c/bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c-vs-3.13.0b1.svg) | 1.01x ↑<br>[📄](results/bm-20240815-3.14.0a0-e913d2c/bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c-vs-3.13.0rc1%2B.md)[📈](results/bm-20240815-3.14.0a0-e913d2c/bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c-vs-3.13.0rc1%2B.svg) | 1.00x ↓<br>[📄](results/bm-20240815-3.14.0a0-e913d2c/bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c-vs-base.md)[📈](results/bm-20240815-3.14.0a0-e913d2c/bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c-vs-base.svg)[🧠](results/bm-20240815-3.14.0a0-e913d2c/bm-20240815-linux-x86_64-python-main-3.14.0a0-e913d2c-vs-base-mem.svg) |
| [2024-08-15](results/bm-20240815-3.14.0a0-1dad23e-NOGIL) | python/1dad23edbc9db3a13268 | 1dad23e (NOGIL) | 1.38x ↓<br>[📄](results/bm-20240815-3.14.0a0-1dad23e-NOGIL/bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e-vs-3.12.0b1.md)[📈](results/bm-20240815-3.14.0a0-1dad23e-NOGIL/bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e-vs-3.12.0b1.svg) | 1.40x ↓<br>[📄](results/bm-20240815-3.14.0a0-1dad23e-NOGIL/bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e-vs-3.12.5%2B.md)[📈](results/bm-20240815-3.14.0a0-1dad23e-NOGIL/bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e-vs-3.12.5%2B.svg) | 1.39x ↓<br>[📄](results/bm-20240815-3.14.0a0-1dad23e-NOGIL/bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e-vs-3.13.0b1.md)[📈](results/bm-20240815-3.14.0a0-1dad23e-NOGIL/bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e-vs-3.13.0b1.svg) | 1.44x ↓<br>[📄](results/bm-20240815-3.14.0a0-1dad23e-NOGIL/bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e-vs-3.13.0rc1%2B.md)[📈](results/bm-20240815-3.14.0a0-1dad23e-NOGIL/bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e-vs-3.13.0rc1%2B.svg) |  |
| [2024-08-13](results/bm-20240813-3.14.0a0-901d949-NOGIL) | python/901d94992eddd84ded2e | 901d949 (NOGIL) | 1.35x ↓<br>[📄](results/bm-20240813-3.14.0a0-901d949-NOGIL/bm-20240813-linux-x86_64-python-901d94992eddd84ded2e-3.14.0a0-901d949-vs-3.12.0b1.md)[📈](results/bm-20240813-3.14.0a0-901d949-NOGIL/bm-20240813-linux-x86_64-python-901d94992eddd84ded2e-3.14.0a0-901d949-vs-3.12.0b1.svg) | 1.37x ↓<br>[📄](results/bm-20240813-3.14.0a0-901d949-NOGIL/bm-20240813-linux-x86_64-python-901d94992eddd84ded2e-3.14.0a0-901d949-vs-3.12.5%2B.md)[📈](results/bm-20240813-3.14.0a0-901d949-NOGIL/bm-20240813-linux-x86_64-python-901d94992eddd84ded2e-3.14.0a0-901d949-vs-3.12.5%2B.svg) | 1.36x ↓<br>[📄](results/bm-20240813-3.14.0a0-901d949-NOGIL/bm-20240813-linux-x86_64-python-901d94992eddd84ded2e-3.14.0a0-901d949-vs-3.13.0b1.md)[📈](results/bm-20240813-3.14.0a0-901d949-NOGIL/bm-20240813-linux-x86_64-python-901d94992eddd84ded2e-3.14.0a0-901d949-vs-3.13.0b1.svg) | 1.41x ↓<br>[📄](results/bm-20240813-3.14.0a0-901d949-NOGIL/bm-20240813-linux-x86_64-python-901d94992eddd84ded2e-3.14.0a0-901d949-vs-3.13.0rc1%2B.md)[📈](results/bm-20240813-3.14.0a0-901d949-NOGIL/bm-20240813-linux-x86_64-python-901d94992eddd84ded2e-3.14.0a0-901d949-vs-3.13.0rc1%2B.svg) |  |
| [2024-08-13](results/bm-20240813-3.14.0a0-5f68511-NOGIL) | python/main | 5f68511 (NOGIL) | 1.38x ↓<br>[📄](results/bm-20240813-3.14.0a0-5f68511-NOGIL/bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511-vs-3.12.0b1.md)[📈](results/bm-20240813-3.14.0a0-5f68511-NOGIL/bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511-vs-3.12.0b1.svg) | 1.39x ↓<br>[📄](results/bm-20240813-3.14.0a0-5f68511-NOGIL/bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511-vs-3.12.5%2B.md)[📈](results/bm-20240813-3.14.0a0-5f68511-NOGIL/bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511-vs-3.12.5%2B.svg) | 1.39x ↓<br>[📄](results/bm-20240813-3.14.0a0-5f68511-NOGIL/bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511-vs-3.13.0b1.md)[📈](results/bm-20240813-3.14.0a0-5f68511-NOGIL/bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511-vs-3.13.0b1.svg) | 1.44x ↓<br>[📄](results/bm-20240813-3.14.0a0-5f68511-NOGIL/bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511-vs-3.13.0rc1%2B.md)[📈](results/bm-20240813-3.14.0a0-5f68511-NOGIL/bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511-vs-3.13.0rc1%2B.svg) | 1.02x ↓<br>[📄](results/bm-20240813-3.14.0a0-5f68511-NOGIL/bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511-vs-base.md)[📈](results/bm-20240813-3.14.0a0-5f68511-NOGIL/bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511-vs-base.svg)[🧠](results/bm-20240813-3.14.0a0-5f68511-NOGIL/bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511-vs-base-mem.svg) |
| [2024-08-14](results/bm-20240814-3.13.0rc1%2B-79452b1) | python/3.13 | 79452b1 | 1.04x ↑<br>[📄](results/bm-20240814-3.13.0rc1%2B-79452b1/bm-20240814-linux-x86_64-python-3.13-3.13.0rc1%2B-79452b1-vs-3.12.0b1.md)[📈](results/bm-20240814-3.13.0rc1%2B-79452b1/bm-20240814-linux-x86_64-python-3.13-3.13.0rc1%2B-79452b1-vs-3.12.0b1.svg) | 1.03x ↑<br>[📄](results/bm-20240814-3.13.0rc1%2B-79452b1/bm-20240814-linux-x86_64-python-3.13-3.13.0rc1%2B-79452b1-vs-3.12.5%2B.md)[📈](results/bm-20240814-3.13.0rc1%2B-79452b1/bm-20240814-linux-x86_64-python-3.13-3.13.0rc1%2B-79452b1-vs-3.12.5%2B.svg) | 1.03x ↑<br>[📄](results/bm-20240814-3.13.0rc1%2B-79452b1/bm-20240814-linux-x86_64-python-3.13-3.13.0rc1%2B-79452b1-vs-3.13.0b1.md)[📈](results/bm-20240814-3.13.0rc1%2B-79452b1/bm-20240814-linux-x86_64-python-3.13-3.13.0rc1%2B-79452b1-vs-3.13.0b1.svg) |  |  |
| [2024-05-08](results/bm-20240508-3.13.0b1-2268289) | python/2268289a47c6e3c9a220 | 2268289 | 1.01x ↑<br>[📄](results/bm-20240508-3.13.0b1-2268289/bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289-vs-3.12.0b1.md)[📈](results/bm-20240508-3.13.0b1-2268289/bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289-vs-3.12.0b1.svg) | 1.00x ↓<br>[📄](results/bm-20240508-3.13.0b1-2268289/bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289-vs-3.12.5%2B.md)[📈](results/bm-20240508-3.13.0b1-2268289/bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289-vs-3.12.5%2B.svg) |  | 1.03x ↓<br>[📄](results/bm-20240508-3.13.0b1-2268289/bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289-vs-3.13.0rc1%2B.md)[📈](results/bm-20240508-3.13.0b1-2268289/bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289-vs-3.13.0rc1%2B.svg) |  |
| [2024-08-14](results/bm-20240814-3.12.5%2B-9f153a2) | python/3.12 | 9f153a2 | 1.01x ↑<br>[📄](results/bm-20240814-3.12.5%2B-9f153a2/bm-20240814-linux-x86_64-python-3.12-3.12.5%2B-9f153a2-vs-3.12.0b1.md)[📈](results/bm-20240814-3.12.5%2B-9f153a2/bm-20240814-linux-x86_64-python-3.12-3.12.5%2B-9f153a2-vs-3.12.0b1.svg) |  | 1.00x ↑<br>[📄](results/bm-20240814-3.12.5%2B-9f153a2/bm-20240814-linux-x86_64-python-3.12-3.12.5%2B-9f153a2-vs-3.13.0b1.md)[📈](results/bm-20240814-3.12.5%2B-9f153a2/bm-20240814-linux-x86_64-python-3.12-3.12.5%2B-9f153a2-vs-3.13.0b1.svg) | 1.03x ↓<br>[📄](results/bm-20240814-3.12.5%2B-9f153a2/bm-20240814-linux-x86_64-python-3.12-3.12.5%2B-9f153a2-vs-3.13.0rc1%2B.md)[📈](results/bm-20240814-3.12.5%2B-9f153a2/bm-20240814-linux-x86_64-python-3.12-3.12.5%2B-9f153a2-vs-3.13.0rc1%2B.svg) |  |
| [2023-05-22](results/bm-20230522-3.12.0b1-5612078) | python/5612078f68e9688fbf3b | 5612078 |  | 1.01x ↓<br>[📄](results/bm-20230522-3.12.0b1-5612078/bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078-vs-3.12.5%2B.md)[📈](results/bm-20230522-3.12.0b1-5612078/bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078-vs-3.12.5%2B.svg) | 1.01x ↓<br>[📄](results/bm-20230522-3.12.0b1-5612078/bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078-vs-3.13.0b1.md)[📈](results/bm-20230522-3.12.0b1-5612078/bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078-vs-3.13.0b1.svg) | 1.04x ↓<br>[📄](results/bm-20230522-3.12.0b1-5612078/bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078-vs-3.13.0rc1%2B.md)[📈](results/bm-20230522-3.12.0b1-5612078/bm-20230522-linux-x86_64-python-5612078f68e9688fbf3b-3.12.0b1-5612078-vs-3.13.0rc1%2B.svg) |  |


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
