# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
[Most recent pystats on main (7d7d56d)](results/bm-20241102-3.14.0a1%2B-7d7d56d-PYTHON_UOPS/bm-20241102-vultr-x86_64-python-7d7d56d8b1147a6b85e1-3.14.0a1%2B-7d7d56d-pystats.md)

## linux x86_64 (linux)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2024-11-05](results/bm-20241105-3.14.0a1%2B-83ba8c2-NOGIL) | python/83ba8c2bba834c0b92de | 83ba8c2 (NOGIL) | 1.58x ↓<br>[📄](results/bm-20241105-3.14.0a1%2B-83ba8c2-NOGIL/bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1%2B-83ba8c2-vs-3.12.6.md)[📈](results/bm-20241105-3.14.0a1%2B-83ba8c2-NOGIL/bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1%2B-83ba8c2-vs-3.12.6.svg) | 1.60x ↓<br>[📄](results/bm-20241105-3.14.0a1%2B-83ba8c2-NOGIL/bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1%2B-83ba8c2-vs-3.13.0rc2.md)[📈](results/bm-20241105-3.14.0a1%2B-83ba8c2-NOGIL/bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1%2B-83ba8c2-vs-3.13.0rc2.svg) | 1.41x ↓<br>[📄](results/bm-20241105-3.14.0a1%2B-83ba8c2-NOGIL/bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1%2B-83ba8c2-vs-base.md)[📈](results/bm-20241105-3.14.0a1%2B-83ba8c2-NOGIL/bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1%2B-83ba8c2-vs-base.svg)[🧠](results/bm-20241105-3.14.0a1%2B-83ba8c2-NOGIL/bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1%2B-83ba8c2-vs-base-mem.svg) |
| [2024-11-05](results/bm-20241105-3.14.0a1%2B-83ba8c2) | python/83ba8c2bba834c0b92de | 83ba8c2 | 1.12x ↓<br>[📄](results/bm-20241105-3.14.0a1%2B-83ba8c2/bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1%2B-83ba8c2-vs-3.12.6.md)[📈](results/bm-20241105-3.14.0a1%2B-83ba8c2/bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1%2B-83ba8c2-vs-3.12.6.svg) | 1.14x ↓<br>[📄](results/bm-20241105-3.14.0a1%2B-83ba8c2/bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1%2B-83ba8c2-vs-3.13.0rc2.md)[📈](results/bm-20241105-3.14.0a1%2B-83ba8c2/bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1%2B-83ba8c2-vs-3.13.0rc2.svg) |  |
| [2024-11-04](results/bm-20241104-3.14.0a1%2B-532fc08-NOGIL) | python/532fc08102d62c04d55f | 532fc08 (NOGIL) | 1.57x ↓<br>[📄](results/bm-20241104-3.14.0a1%2B-532fc08-NOGIL/bm-20241104-linux-x86_64-python-532fc08102d62c04d55f-3.14.0a1%2B-532fc08-vs-3.12.6.md)[📈](results/bm-20241104-3.14.0a1%2B-532fc08-NOGIL/bm-20241104-linux-x86_64-python-532fc08102d62c04d55f-3.14.0a1%2B-532fc08-vs-3.12.6.svg) | 1.59x ↓<br>[📄](results/bm-20241104-3.14.0a1%2B-532fc08-NOGIL/bm-20241104-linux-x86_64-python-532fc08102d62c04d55f-3.14.0a1%2B-532fc08-vs-3.13.0rc2.md)[📈](results/bm-20241104-3.14.0a1%2B-532fc08-NOGIL/bm-20241104-linux-x86_64-python-532fc08102d62c04d55f-3.14.0a1%2B-532fc08-vs-3.13.0rc2.svg) | 1.39x ↓<br>[📄](results/bm-20241104-3.14.0a1%2B-532fc08-NOGIL/bm-20241104-linux-x86_64-python-532fc08102d62c04d55f-3.14.0a1%2B-532fc08-vs-base.md)[📈](results/bm-20241104-3.14.0a1%2B-532fc08-NOGIL/bm-20241104-linux-x86_64-python-532fc08102d62c04d55f-3.14.0a1%2B-532fc08-vs-base.svg)[🧠](results/bm-20241104-3.14.0a1%2B-532fc08-NOGIL/bm-20241104-linux-x86_64-python-532fc08102d62c04d55f-3.14.0a1%2B-532fc08-vs-base-mem.svg) |
| [2024-11-04](results/bm-20241104-3.14.0a1%2B-532fc08) | python/532fc08102d62c04d55f | 532fc08 | 1.13x ↓<br>[📄](results/bm-20241104-3.14.0a1%2B-532fc08/bm-20241104-linux-x86_64-python-532fc08102d62c04d55f-3.14.0a1%2B-532fc08-vs-3.12.6.md)[📈](results/bm-20241104-3.14.0a1%2B-532fc08/bm-20241104-linux-x86_64-python-532fc08102d62c04d55f-3.14.0a1%2B-532fc08-vs-3.12.6.svg) | 1.15x ↓<br>[📄](results/bm-20241104-3.14.0a1%2B-532fc08/bm-20241104-linux-x86_64-python-532fc08102d62c04d55f-3.14.0a1%2B-532fc08-vs-3.13.0rc2.md)[📈](results/bm-20241104-3.14.0a1%2B-532fc08/bm-20241104-linux-x86_64-python-532fc08102d62c04d55f-3.14.0a1%2B-532fc08-vs-3.13.0rc2.svg) |  |

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2024-11-05](results/bm-20241105-3.14.0a1%2B-83ba8c2-NOGIL) | python/83ba8c2bba834c0b92de | 83ba8c2 (NOGIL) | 1.55x ↓<br>[📄](results/bm-20241105-3.14.0a1%2B-83ba8c2-NOGIL/bm-20241105-vultr-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1%2B-83ba8c2-vs-3.12.6.md)[📈](results/bm-20241105-3.14.0a1%2B-83ba8c2-NOGIL/bm-20241105-vultr-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1%2B-83ba8c2-vs-3.12.6.svg) | 1.57x ↓<br>[📄](results/bm-20241105-3.14.0a1%2B-83ba8c2-NOGIL/bm-20241105-vultr-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1%2B-83ba8c2-vs-3.13.0rc2.md)[📈](results/bm-20241105-3.14.0a1%2B-83ba8c2-NOGIL/bm-20241105-vultr-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1%2B-83ba8c2-vs-3.13.0rc2.svg) | 1.55x ↓<br>[📄](results/bm-20241105-3.14.0a1%2B-83ba8c2-NOGIL/bm-20241105-vultr-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1%2B-83ba8c2-vs-base.md)[📈](results/bm-20241105-3.14.0a1%2B-83ba8c2-NOGIL/bm-20241105-vultr-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1%2B-83ba8c2-vs-base.svg)[🧠](results/bm-20241105-3.14.0a1%2B-83ba8c2-NOGIL/bm-20241105-vultr-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1%2B-83ba8c2-vs-base-mem.svg) |
| [2024-11-05](results/bm-20241105-3.14.0a1%2B-83ba8c2) | python/83ba8c2bba834c0b92de | 83ba8c2 | 1.00x ↑<br>[📄](results/bm-20241105-3.14.0a1%2B-83ba8c2/bm-20241105-vultr-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1%2B-83ba8c2-vs-3.12.6.md)[📈](results/bm-20241105-3.14.0a1%2B-83ba8c2/bm-20241105-vultr-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1%2B-83ba8c2-vs-3.12.6.svg) | 1.01x ↓<br>[📄](results/bm-20241105-3.14.0a1%2B-83ba8c2/bm-20241105-vultr-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1%2B-83ba8c2-vs-3.13.0rc2.md)[📈](results/bm-20241105-3.14.0a1%2B-83ba8c2/bm-20241105-vultr-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1%2B-83ba8c2-vs-3.13.0rc2.svg) |  |
| [2024-11-04](results/bm-20241104-3.14.0a1%2B-532fc08-NOGIL) | python/532fc08102d62c04d55f | 532fc08 (NOGIL) | 1.56x ↓<br>[📄](results/bm-20241104-3.14.0a1%2B-532fc08-NOGIL/bm-20241104-vultr-x86_64-python-532fc08102d62c04d55f-3.14.0a1%2B-532fc08-vs-3.12.6.md)[📈](results/bm-20241104-3.14.0a1%2B-532fc08-NOGIL/bm-20241104-vultr-x86_64-python-532fc08102d62c04d55f-3.14.0a1%2B-532fc08-vs-3.12.6.svg) | 1.58x ↓<br>[📄](results/bm-20241104-3.14.0a1%2B-532fc08-NOGIL/bm-20241104-vultr-x86_64-python-532fc08102d62c04d55f-3.14.0a1%2B-532fc08-vs-3.13.0rc2.md)[📈](results/bm-20241104-3.14.0a1%2B-532fc08-NOGIL/bm-20241104-vultr-x86_64-python-532fc08102d62c04d55f-3.14.0a1%2B-532fc08-vs-3.13.0rc2.svg) | 1.55x ↓<br>[📄](results/bm-20241104-3.14.0a1%2B-532fc08-NOGIL/bm-20241104-vultr-x86_64-python-532fc08102d62c04d55f-3.14.0a1%2B-532fc08-vs-base.md)[📈](results/bm-20241104-3.14.0a1%2B-532fc08-NOGIL/bm-20241104-vultr-x86_64-python-532fc08102d62c04d55f-3.14.0a1%2B-532fc08-vs-base.svg)[🧠](results/bm-20241104-3.14.0a1%2B-532fc08-NOGIL/bm-20241104-vultr-x86_64-python-532fc08102d62c04d55f-3.14.0a1%2B-532fc08-vs-base-mem.svg) |
| [2024-11-04](results/bm-20241104-3.14.0a1%2B-532fc08) | python/532fc08102d62c04d55f | 532fc08 | 1.01x ↓<br>[📄](results/bm-20241104-3.14.0a1%2B-532fc08/bm-20241104-vultr-x86_64-python-532fc08102d62c04d55f-3.14.0a1%2B-532fc08-vs-3.12.6.md)[📈](results/bm-20241104-3.14.0a1%2B-532fc08/bm-20241104-vultr-x86_64-python-532fc08102d62c04d55f-3.14.0a1%2B-532fc08-vs-3.12.6.svg) | 1.02x ↓<br>[📄](results/bm-20241104-3.14.0a1%2B-532fc08/bm-20241104-vultr-x86_64-python-532fc08102d62c04d55f-3.14.0a1%2B-532fc08-vs-3.13.0rc2.md)[📈](results/bm-20241104-3.14.0a1%2B-532fc08/bm-20241104-vultr-x86_64-python-532fc08102d62c04d55f-3.14.0a1%2B-532fc08-vs-3.13.0rc2.svg) |  |
| [2024-11-03](results/bm-20241103-3.14.0a1%2B-9441993-NOGIL) | python/9441993f272f42e4a97d | 9441993 (NOGIL) | 1.55x ↓<br>[📄](results/bm-20241103-3.14.0a1%2B-9441993-NOGIL/bm-20241103-vultr-x86_64-python-9441993f272f42e4a97d-3.14.0a1%2B-9441993-vs-3.12.6.md)[📈](results/bm-20241103-3.14.0a1%2B-9441993-NOGIL/bm-20241103-vultr-x86_64-python-9441993f272f42e4a97d-3.14.0a1%2B-9441993-vs-3.12.6.svg) | 1.57x ↓<br>[📄](results/bm-20241103-3.14.0a1%2B-9441993-NOGIL/bm-20241103-vultr-x86_64-python-9441993f272f42e4a97d-3.14.0a1%2B-9441993-vs-3.13.0rc2.md)[📈](results/bm-20241103-3.14.0a1%2B-9441993-NOGIL/bm-20241103-vultr-x86_64-python-9441993f272f42e4a97d-3.14.0a1%2B-9441993-vs-3.13.0rc2.svg) | 1.54x ↓<br>[📄](results/bm-20241103-3.14.0a1%2B-9441993-NOGIL/bm-20241103-vultr-x86_64-python-9441993f272f42e4a97d-3.14.0a1%2B-9441993-vs-base.md)[📈](results/bm-20241103-3.14.0a1%2B-9441993-NOGIL/bm-20241103-vultr-x86_64-python-9441993f272f42e4a97d-3.14.0a1%2B-9441993-vs-base.svg)[🧠](results/bm-20241103-3.14.0a1%2B-9441993-NOGIL/bm-20241103-vultr-x86_64-python-9441993f272f42e4a97d-3.14.0a1%2B-9441993-vs-base-mem.svg) |
| [2024-11-03](results/bm-20241103-3.14.0a1%2B-9441993) | python/9441993f272f42e4a97d | 9441993 | 1.01x ↓<br>[📄](results/bm-20241103-3.14.0a1%2B-9441993/bm-20241103-vultr-x86_64-python-9441993f272f42e4a97d-3.14.0a1%2B-9441993-vs-3.12.6.md)[📈](results/bm-20241103-3.14.0a1%2B-9441993/bm-20241103-vultr-x86_64-python-9441993f272f42e4a97d-3.14.0a1%2B-9441993-vs-3.12.6.svg) | 1.02x ↓<br>[📄](results/bm-20241103-3.14.0a1%2B-9441993/bm-20241103-vultr-x86_64-python-9441993f272f42e4a97d-3.14.0a1%2B-9441993-vs-3.13.0rc2.md)[📈](results/bm-20241103-3.14.0a1%2B-9441993/bm-20241103-vultr-x86_64-python-9441993f272f42e4a97d-3.14.0a1%2B-9441993-vs-3.13.0rc2.svg) |  |
| [2024-11-02](results/bm-20241102-3.14.0a1%2B-7d7d56d-NOGIL) | python/7d7d56d8b1147a6b85e1 | 7d7d56d (NOGIL) | 1.55x ↓<br>[📄](results/bm-20241102-3.14.0a1%2B-7d7d56d-NOGIL/bm-20241102-vultr-x86_64-python-7d7d56d8b1147a6b85e1-3.14.0a1%2B-7d7d56d-vs-3.12.6.md)[📈](results/bm-20241102-3.14.0a1%2B-7d7d56d-NOGIL/bm-20241102-vultr-x86_64-python-7d7d56d8b1147a6b85e1-3.14.0a1%2B-7d7d56d-vs-3.12.6.svg) | 1.57x ↓<br>[📄](results/bm-20241102-3.14.0a1%2B-7d7d56d-NOGIL/bm-20241102-vultr-x86_64-python-7d7d56d8b1147a6b85e1-3.14.0a1%2B-7d7d56d-vs-3.13.0rc2.md)[📈](results/bm-20241102-3.14.0a1%2B-7d7d56d-NOGIL/bm-20241102-vultr-x86_64-python-7d7d56d8b1147a6b85e1-3.14.0a1%2B-7d7d56d-vs-3.13.0rc2.svg) | 1.54x ↓<br>[📄](results/bm-20241102-3.14.0a1%2B-7d7d56d-NOGIL/bm-20241102-vultr-x86_64-python-7d7d56d8b1147a6b85e1-3.14.0a1%2B-7d7d56d-vs-base.md)[📈](results/bm-20241102-3.14.0a1%2B-7d7d56d-NOGIL/bm-20241102-vultr-x86_64-python-7d7d56d8b1147a6b85e1-3.14.0a1%2B-7d7d56d-vs-base.svg)[🧠](results/bm-20241102-3.14.0a1%2B-7d7d56d-NOGIL/bm-20241102-vultr-x86_64-python-7d7d56d8b1147a6b85e1-3.14.0a1%2B-7d7d56d-vs-base-mem.svg) |
| [2024-11-02](results/bm-20241102-3.14.0a1%2B-7d7d56d) | python/7d7d56d8b1147a6b85e1 | 7d7d56d | 1.01x ↓<br>[📄](results/bm-20241102-3.14.0a1%2B-7d7d56d/bm-20241102-vultr-x86_64-python-7d7d56d8b1147a6b85e1-3.14.0a1%2B-7d7d56d-vs-3.12.6.md)[📈](results/bm-20241102-3.14.0a1%2B-7d7d56d/bm-20241102-vultr-x86_64-python-7d7d56d8b1147a6b85e1-3.14.0a1%2B-7d7d56d-vs-3.12.6.svg) | 1.02x ↓<br>[📄](results/bm-20241102-3.14.0a1%2B-7d7d56d/bm-20241102-vultr-x86_64-python-7d7d56d8b1147a6b85e1-3.14.0a1%2B-7d7d56d-vs-3.13.0rc2.md)[📈](results/bm-20241102-3.14.0a1%2B-7d7d56d/bm-20241102-vultr-x86_64-python-7d7d56d8b1147a6b85e1-3.14.0a1%2B-7d7d56d-vs-3.13.0rc2.svg) |  |


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
