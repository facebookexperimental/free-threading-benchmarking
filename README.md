# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
## linux x86_64 (linux)
| date | fork/ref | hash/flags | vs. 3.11.0: | vs. base: |
| --- | --- | --- | ---: | ---: |
| [2024-08-08](results/bm-20240808-3.14.0a0-e006c73-NOGIL) | python/e006c7371d8e57db2625 | e006c73 (NOGIL) |  | 1.45x ↓<br>[📄](results/bm-20240808-3.14.0a0-e006c73-NOGIL/bm-20240808-linux-x86_64-python-e006c7371d8e57db2625-3.14.0a0-e006c73-vs-base.md)[📈](results/bm-20240808-3.14.0a0-e006c73-NOGIL/bm-20240808-linux-x86_64-python-e006c7371d8e57db2625-3.14.0a0-e006c73-vs-base.svg)[🧠](results/bm-20240808-3.14.0a0-e006c73-NOGIL/bm-20240808-linux-x86_64-python-e006c7371d8e57db2625-3.14.0a0-e006c73-vs-base-mem.svg) |
| [2024-08-08](results/bm-20240808-3.14.0a0-e006c73) | python/e006c7371d8e57db2625 | e006c73 |  | 1.03x ↑<br>[📄](results/bm-20240808-3.14.0a0-e006c73/bm-20240808-linux-x86_64-python-e006c7371d8e57db2625-3.14.0a0-e006c73-vs-base.md)[📈](results/bm-20240808-3.14.0a0-e006c73/bm-20240808-linux-x86_64-python-e006c7371d8e57db2625-3.14.0a0-e006c73-vs-base.svg)[🧠](results/bm-20240808-3.14.0a0-e006c73/bm-20240808-linux-x86_64-python-e006c7371d8e57db2625-3.14.0a0-e006c73-vs-base-mem.svg) |
| [2024-08-07](results/bm-20240807-3.14.0a0-540fcc6) | python/540fcc62f5da982b7950 | 540fcc6 |  | 1.01x ↓<br>[📄](results/bm-20240807-3.14.0a0-540fcc6/bm-20240807-linux-x86_64-python-540fcc62f5da982b7950-3.14.0a0-540fcc6-vs-base.md)[📈](results/bm-20240807-3.14.0a0-540fcc6/bm-20240807-linux-x86_64-python-540fcc62f5da982b7950-3.14.0a0-540fcc6-vs-base.svg)[🧠](results/bm-20240807-3.14.0a0-540fcc6/bm-20240807-linux-x86_64-python-540fcc62f5da982b7950-3.14.0a0-540fcc6-vs-base-mem.svg) |
| [2024-08-07](results/bm-20240807-3.14.0a0-540fcc6-NOGIL) | python/540fcc62f5da982b7950 | 540fcc6 (NOGIL) |  | 1.00x ↓<br>[📄](results/bm-20240807-3.14.0a0-540fcc6-NOGIL/bm-20240807-linux-x86_64-python-540fcc62f5da982b7950-3.14.0a0-540fcc6-vs-base.md)[📈](results/bm-20240807-3.14.0a0-540fcc6-NOGIL/bm-20240807-linux-x86_64-python-540fcc62f5da982b7950-3.14.0a0-540fcc6-vs-base.svg)[🧠](results/bm-20240807-3.14.0a0-540fcc6-NOGIL/bm-20240807-linux-x86_64-python-540fcc62f5da982b7950-3.14.0a0-540fcc6-vs-base-mem.svg) |
| [2024-08-07](results/bm-20240807-3.14.0a0-e73e7a7) | python/e73e7a7abdc3fed252af | e73e7a7 |  |  |
| [2024-08-07](results/bm-20240807-3.14.0a0-e73e7a7-NOGIL) | python/e73e7a7abdc3fed252af | e73e7a7 (NOGIL) |  | 1.39x ↓<br>[📄](results/bm-20240807-3.14.0a0-e73e7a7-NOGIL/bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7-vs-base.md)[📈](results/bm-20240807-3.14.0a0-e73e7a7-NOGIL/bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7-vs-base.svg)[🧠](results/bm-20240807-3.14.0a0-e73e7a7-NOGIL/bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7-vs-base-mem.svg) |
| [2024-08-07](results/bm-20240807-3.14.0a0-f483286) | mpage/gh_122712_fix_call_a | f483286 |  | 1.00x ↑<br>[📄](results/bm-20240807-3.14.0a0-f483286/bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286-vs-base.md)[📈](results/bm-20240807-3.14.0a0-f483286/bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286-vs-base.svg)[🧠](results/bm-20240807-3.14.0a0-f483286/bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286-vs-base-mem.svg) |
| [2024-08-07](results/bm-20240807-3.14.0a0-f483286-NOGIL) | mpage/gh_122712_fix_call_a | f483286 (NOGIL) |  | 1.00x ↓<br>[📄](results/bm-20240807-3.14.0a0-f483286-NOGIL/bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286-vs-base.md)[📈](results/bm-20240807-3.14.0a0-f483286-NOGIL/bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286-vs-base.svg)[🧠](results/bm-20240807-3.14.0a0-f483286-NOGIL/bm-20240807-linux-x86_64-mpage-gh_122712_fix_call_a-3.14.0a0-f483286-vs-base-mem.svg) |
| [2024-08-06](results/bm-20240806-3.14.0a0-4767a6e-NOGIL) | python/main | 4767a6e (NOGIL) |  |  |


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
