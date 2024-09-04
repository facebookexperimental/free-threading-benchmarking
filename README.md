# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
## linux x86_64 (linux)
| date | fork/ref | hash/flags | vs. 3.12.0b1: | vs. 3.12.5+: | vs. 3.13.0b1: | vs. 3.13.0rc1+: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: | ---: | ---: |
| [2024-09-03](results/bm-20240903-3.14.0a0-d8a840b-NOGIL) | mpage/gh_115999_thread_loc | d8a840b (NOGIL) | 1.36x ↓<br>[📄](results/bm-20240903-3.14.0a0-d8a840b-NOGIL/bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b-vs-3.12.0b1.md)[📈](results/bm-20240903-3.14.0a0-d8a840b-NOGIL/bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b-vs-3.12.0b1.svg) | 1.38x ↓<br>[📄](results/bm-20240903-3.14.0a0-d8a840b-NOGIL/bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b-vs-3.12.5%2B.md)[📈](results/bm-20240903-3.14.0a0-d8a840b-NOGIL/bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b-vs-3.12.5%2B.svg) | 1.37x ↓<br>[📄](results/bm-20240903-3.14.0a0-d8a840b-NOGIL/bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b-vs-3.13.0b1.md)[📈](results/bm-20240903-3.14.0a0-d8a840b-NOGIL/bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b-vs-3.13.0b1.svg) | 1.42x ↓<br>[📄](results/bm-20240903-3.14.0a0-d8a840b-NOGIL/bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b-vs-3.13.0rc1%2B.md)[📈](results/bm-20240903-3.14.0a0-d8a840b-NOGIL/bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b-vs-3.13.0rc1%2B.svg) |  |
| [2024-08-31](results/bm-20240831-3.14.0a0-34ddb64-NOGIL) | python/34ddb64d088dd7ccc321 | 34ddb64 (NOGIL) | 1.33x ↓<br>[📄](results/bm-20240831-3.14.0a0-34ddb64-NOGIL/bm-20240831-linux-x86_64-python-34ddb64d088dd7ccc321-3.14.0a0-34ddb64-vs-3.12.0b1.md)[📈](results/bm-20240831-3.14.0a0-34ddb64-NOGIL/bm-20240831-linux-x86_64-python-34ddb64d088dd7ccc321-3.14.0a0-34ddb64-vs-3.12.0b1.svg) | 1.34x ↓<br>[📄](results/bm-20240831-3.14.0a0-34ddb64-NOGIL/bm-20240831-linux-x86_64-python-34ddb64d088dd7ccc321-3.14.0a0-34ddb64-vs-3.12.5%2B.md)[📈](results/bm-20240831-3.14.0a0-34ddb64-NOGIL/bm-20240831-linux-x86_64-python-34ddb64d088dd7ccc321-3.14.0a0-34ddb64-vs-3.12.5%2B.svg) | 1.34x ↓<br>[📄](results/bm-20240831-3.14.0a0-34ddb64-NOGIL/bm-20240831-linux-x86_64-python-34ddb64d088dd7ccc321-3.14.0a0-34ddb64-vs-3.13.0b1.md)[📈](results/bm-20240831-3.14.0a0-34ddb64-NOGIL/bm-20240831-linux-x86_64-python-34ddb64d088dd7ccc321-3.14.0a0-34ddb64-vs-3.13.0b1.svg) | 1.38x ↓<br>[📄](results/bm-20240831-3.14.0a0-34ddb64-NOGIL/bm-20240831-linux-x86_64-python-34ddb64d088dd7ccc321-3.14.0a0-34ddb64-vs-3.13.0rc1%2B.md)[📈](results/bm-20240831-3.14.0a0-34ddb64-NOGIL/bm-20240831-linux-x86_64-python-34ddb64d088dd7ccc321-3.14.0a0-34ddb64-vs-3.13.0rc1%2B.svg) | 1.44x ↓<br>[📄](results/bm-20240831-3.14.0a0-34ddb64-NOGIL/bm-20240831-linux-x86_64-python-34ddb64d088dd7ccc321-3.14.0a0-34ddb64-vs-base.md)[📈](results/bm-20240831-3.14.0a0-34ddb64-NOGIL/bm-20240831-linux-x86_64-python-34ddb64d088dd7ccc321-3.14.0a0-34ddb64-vs-base.svg)[🧠](results/bm-20240831-3.14.0a0-34ddb64-NOGIL/bm-20240831-linux-x86_64-python-34ddb64d088dd7ccc321-3.14.0a0-34ddb64-vs-base-mem.svg) |
| [2024-08-31](results/bm-20240831-3.14.0a0-34ddb64) | python/34ddb64d088dd7ccc321 | 34ddb64 | 1.09x ↑<br>[📄](results/bm-20240831-3.14.0a0-34ddb64/bm-20240831-linux-x86_64-python-34ddb64d088dd7ccc321-3.14.0a0-34ddb64-vs-3.12.0b1.md)[📈](results/bm-20240831-3.14.0a0-34ddb64/bm-20240831-linux-x86_64-python-34ddb64d088dd7ccc321-3.14.0a0-34ddb64-vs-3.12.0b1.svg) | 1.08x ↑<br>[📄](results/bm-20240831-3.14.0a0-34ddb64/bm-20240831-linux-x86_64-python-34ddb64d088dd7ccc321-3.14.0a0-34ddb64-vs-3.12.5%2B.md)[📈](results/bm-20240831-3.14.0a0-34ddb64/bm-20240831-linux-x86_64-python-34ddb64d088dd7ccc321-3.14.0a0-34ddb64-vs-3.12.5%2B.svg) | 1.08x ↑<br>[📄](results/bm-20240831-3.14.0a0-34ddb64/bm-20240831-linux-x86_64-python-34ddb64d088dd7ccc321-3.14.0a0-34ddb64-vs-3.13.0b1.md)[📈](results/bm-20240831-3.14.0a0-34ddb64/bm-20240831-linux-x86_64-python-34ddb64d088dd7ccc321-3.14.0a0-34ddb64-vs-3.13.0b1.svg) | 1.04x ↑<br>[📄](results/bm-20240831-3.14.0a0-34ddb64/bm-20240831-linux-x86_64-python-34ddb64d088dd7ccc321-3.14.0a0-34ddb64-vs-3.13.0rc1%2B.md)[📈](results/bm-20240831-3.14.0a0-34ddb64/bm-20240831-linux-x86_64-python-34ddb64d088dd7ccc321-3.14.0a0-34ddb64-vs-3.13.0rc1%2B.svg) |  |


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
