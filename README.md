# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (fad0674)](results/bm-20260523-3.16.0a0-fad0674/bm-20260523-vultr-x86_64-python-fad06746051f6bd95a25-3.16.0a0-fad0674-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (fad0674)](results/bm-20260523-3.16.0a0-fad0674-PYTHON_UOPS/bm-20260523-vultr-x86_64-python-fad06746051f6bd95a25-3.16.0a0-fad0674-pystats.md)
- [Most recent JIT pystats on main (bedaea0)](results/bm-20251019-3.15.0a1%2B-bedaea0-JIT/bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-05-28](results/bm-20260528-3.16.0a0-1d4e965-NOGIL) | python/1d4e965829eef4cdb089 | 1d4e965 (NOGIL) | 1.029x ↓<br>[📄](results/bm-20260528-3.16.0a0-1d4e965-NOGIL/bm-20260528-vultr-x86_64-python-1d4e965829eef4cdb089-3.16.0a0-1d4e965-vs-3.12.6.md)[📈](results/bm-20260528-3.16.0a0-1d4e965-NOGIL/bm-20260528-vultr-x86_64-python-1d4e965829eef4cdb089-3.16.0a0-1d4e965-vs-3.12.6.svg) | 1.065x ↓<br>[📄](results/bm-20260528-3.16.0a0-1d4e965-NOGIL/bm-20260528-vultr-x86_64-python-1d4e965829eef4cdb089-3.16.0a0-1d4e965-vs-3.13.0rc2.md)[📈](results/bm-20260528-3.16.0a0-1d4e965-NOGIL/bm-20260528-vultr-x86_64-python-1d4e965829eef4cdb089-3.16.0a0-1d4e965-vs-3.13.0rc2.svg) | 1.095x ↓<br>[📄](results/bm-20260528-3.16.0a0-1d4e965-NOGIL/bm-20260528-vultr-x86_64-python-1d4e965829eef4cdb089-3.16.0a0-1d4e965-vs-base.md)[📈](results/bm-20260528-3.16.0a0-1d4e965-NOGIL/bm-20260528-vultr-x86_64-python-1d4e965829eef4cdb089-3.16.0a0-1d4e965-vs-base.svg)[🧠](results/bm-20260528-3.16.0a0-1d4e965-NOGIL/bm-20260528-vultr-x86_64-python-1d4e965829eef4cdb089-3.16.0a0-1d4e965-vs-base-mem.svg) |
| [2026-05-28](results/bm-20260528-3.16.0a0-1d4e965) | python/1d4e965829eef4cdb089 | 1d4e965 | 1.068x ↑<br>[📄](results/bm-20260528-3.16.0a0-1d4e965/bm-20260528-vultr-x86_64-python-1d4e965829eef4cdb089-3.16.0a0-1d4e965-vs-3.12.6.md)[📈](results/bm-20260528-3.16.0a0-1d4e965/bm-20260528-vultr-x86_64-python-1d4e965829eef4cdb089-3.16.0a0-1d4e965-vs-3.12.6.svg) | 1.028x ↑<br>[📄](results/bm-20260528-3.16.0a0-1d4e965/bm-20260528-vultr-x86_64-python-1d4e965829eef4cdb089-3.16.0a0-1d4e965-vs-3.13.0rc2.md)[📈](results/bm-20260528-3.16.0a0-1d4e965/bm-20260528-vultr-x86_64-python-1d4e965829eef4cdb089-3.16.0a0-1d4e965-vs-3.13.0rc2.svg) |  |
| [2026-05-27](results/bm-20260527-3.16.0a0-9242700-NOGIL) | python/9242700c149c490c56d2 | 9242700 (NOGIL) | 1.030x ↓<br>[📄](results/bm-20260527-3.16.0a0-9242700-NOGIL/bm-20260527-vultr-x86_64-python-9242700c149c490c56d2-3.16.0a0-9242700-vs-3.12.6.md)[📈](results/bm-20260527-3.16.0a0-9242700-NOGIL/bm-20260527-vultr-x86_64-python-9242700c149c490c56d2-3.16.0a0-9242700-vs-3.12.6.svg) | 1.066x ↓<br>[📄](results/bm-20260527-3.16.0a0-9242700-NOGIL/bm-20260527-vultr-x86_64-python-9242700c149c490c56d2-3.16.0a0-9242700-vs-3.13.0rc2.md)[📈](results/bm-20260527-3.16.0a0-9242700-NOGIL/bm-20260527-vultr-x86_64-python-9242700c149c490c56d2-3.16.0a0-9242700-vs-3.13.0rc2.svg) | 1.096x ↓<br>[📄](results/bm-20260527-3.16.0a0-9242700-NOGIL/bm-20260527-vultr-x86_64-python-9242700c149c490c56d2-3.16.0a0-9242700-vs-base.md)[📈](results/bm-20260527-3.16.0a0-9242700-NOGIL/bm-20260527-vultr-x86_64-python-9242700c149c490c56d2-3.16.0a0-9242700-vs-base.svg)[🧠](results/bm-20260527-3.16.0a0-9242700-NOGIL/bm-20260527-vultr-x86_64-python-9242700c149c490c56d2-3.16.0a0-9242700-vs-base-mem.svg) |
| [2026-05-27](results/bm-20260527-3.16.0a0-9242700) | python/9242700c149c490c56d2 | 9242700 | 1.067x ↑<br>[📄](results/bm-20260527-3.16.0a0-9242700/bm-20260527-vultr-x86_64-python-9242700c149c490c56d2-3.16.0a0-9242700-vs-3.12.6.md)[📈](results/bm-20260527-3.16.0a0-9242700/bm-20260527-vultr-x86_64-python-9242700c149c490c56d2-3.16.0a0-9242700-vs-3.12.6.svg) | 1.028x ↑<br>[📄](results/bm-20260527-3.16.0a0-9242700/bm-20260527-vultr-x86_64-python-9242700c149c490c56d2-3.16.0a0-9242700-vs-3.13.0rc2.md)[📈](results/bm-20260527-3.16.0a0-9242700/bm-20260527-vultr-x86_64-python-9242700c149c490c56d2-3.16.0a0-9242700-vs-3.13.0rc2.svg) |  |
| [2026-05-26](results/bm-20260526-3.16.0a0-776573c-NOGIL) | python/776573c9f08f70ae9cb2 | 776573c (NOGIL) | 1.033x ↓<br>[📄](results/bm-20260526-3.16.0a0-776573c-NOGIL/bm-20260526-vultr-x86_64-python-776573c9f08f70ae9cb2-3.16.0a0-776573c-vs-3.12.6.md)[📈](results/bm-20260526-3.16.0a0-776573c-NOGIL/bm-20260526-vultr-x86_64-python-776573c9f08f70ae9cb2-3.16.0a0-776573c-vs-3.12.6.svg) | 1.068x ↓<br>[📄](results/bm-20260526-3.16.0a0-776573c-NOGIL/bm-20260526-vultr-x86_64-python-776573c9f08f70ae9cb2-3.16.0a0-776573c-vs-3.13.0rc2.md)[📈](results/bm-20260526-3.16.0a0-776573c-NOGIL/bm-20260526-vultr-x86_64-python-776573c9f08f70ae9cb2-3.16.0a0-776573c-vs-3.13.0rc2.svg) | 1.098x ↓<br>[📄](results/bm-20260526-3.16.0a0-776573c-NOGIL/bm-20260526-vultr-x86_64-python-776573c9f08f70ae9cb2-3.16.0a0-776573c-vs-base.md)[📈](results/bm-20260526-3.16.0a0-776573c-NOGIL/bm-20260526-vultr-x86_64-python-776573c9f08f70ae9cb2-3.16.0a0-776573c-vs-base.svg)[🧠](results/bm-20260526-3.16.0a0-776573c-NOGIL/bm-20260526-vultr-x86_64-python-776573c9f08f70ae9cb2-3.16.0a0-776573c-vs-base-mem.svg) |
| [2026-05-26](results/bm-20260526-3.16.0a0-776573c) | python/776573c9f08f70ae9cb2 | 776573c | 1.066x ↑<br>[📄](results/bm-20260526-3.16.0a0-776573c/bm-20260526-vultr-x86_64-python-776573c9f08f70ae9cb2-3.16.0a0-776573c-vs-3.12.6.md)[📈](results/bm-20260526-3.16.0a0-776573c/bm-20260526-vultr-x86_64-python-776573c9f08f70ae9cb2-3.16.0a0-776573c-vs-3.12.6.svg) | 1.028x ↑<br>[📄](results/bm-20260526-3.16.0a0-776573c/bm-20260526-vultr-x86_64-python-776573c9f08f70ae9cb2-3.16.0a0-776573c-vs-3.13.0rc2.md)[📈](results/bm-20260526-3.16.0a0-776573c/bm-20260526-vultr-x86_64-python-776573c9f08f70ae9cb2-3.16.0a0-776573c-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-05-20](results/bm-20260520-3.16.0a0-cb3b4b9-NOGIL) | python/cb3b4b98d8d141c9de04 | cb3b4b9 (NOGIL) | 1.099x ↑<br>[📄](results/bm-20260520-3.16.0a0-cb3b4b9-NOGIL/bm-20260520-macm4pro-arm64-python-cb3b4b98d8d141c9de04-3.16.0a0-cb3b4b9-vs-3.12.6.md)[📈](results/bm-20260520-3.16.0a0-cb3b4b9-NOGIL/bm-20260520-macm4pro-arm64-python-cb3b4b98d8d141c9de04-3.16.0a0-cb3b4b9-vs-3.12.6.svg) | 1.014x ↑<br>[📄](results/bm-20260520-3.16.0a0-cb3b4b9-NOGIL/bm-20260520-macm4pro-arm64-python-cb3b4b98d8d141c9de04-3.16.0a0-cb3b4b9-vs-3.13.0rc2.md)[📈](results/bm-20260520-3.16.0a0-cb3b4b9-NOGIL/bm-20260520-macm4pro-arm64-python-cb3b4b98d8d141c9de04-3.16.0a0-cb3b4b9-vs-3.13.0rc2.svg) | 1.021x ↓<br>[📄](results/bm-20260520-3.16.0a0-cb3b4b9-NOGIL/bm-20260520-macm4pro-arm64-python-cb3b4b98d8d141c9de04-3.16.0a0-cb3b4b9-vs-base.md)[📈](results/bm-20260520-3.16.0a0-cb3b4b9-NOGIL/bm-20260520-macm4pro-arm64-python-cb3b4b98d8d141c9de04-3.16.0a0-cb3b4b9-vs-base.svg)[🧠](results/bm-20260520-3.16.0a0-cb3b4b9-NOGIL/bm-20260520-macm4pro-arm64-python-cb3b4b98d8d141c9de04-3.16.0a0-cb3b4b9-vs-base-mem.svg) |
| [2026-05-20](results/bm-20260520-3.16.0a0-cb3b4b9) | python/cb3b4b98d8d141c9de04 | cb3b4b9 | 1.122x ↑<br>[📄](results/bm-20260520-3.16.0a0-cb3b4b9/bm-20260520-macm4pro-arm64-python-cb3b4b98d8d141c9de04-3.16.0a0-cb3b4b9-vs-3.12.6.md)[📈](results/bm-20260520-3.16.0a0-cb3b4b9/bm-20260520-macm4pro-arm64-python-cb3b4b98d8d141c9de04-3.16.0a0-cb3b4b9-vs-3.12.6.svg) | 1.035x ↑<br>[📄](results/bm-20260520-3.16.0a0-cb3b4b9/bm-20260520-macm4pro-arm64-python-cb3b4b98d8d141c9de04-3.16.0a0-cb3b4b9-vs-3.13.0rc2.md)[📈](results/bm-20260520-3.16.0a0-cb3b4b9/bm-20260520-macm4pro-arm64-python-cb3b4b98d8d141c9de04-3.16.0a0-cb3b4b9-vs-3.13.0rc2.svg) |  |
| [2026-05-20](results/bm-20260520-3.16.0a0-de9c32f-NOGIL) | python/de9c32fc34fe2e000de1 | de9c32f (NOGIL) | 1.101x ↑<br>[📄](results/bm-20260520-3.16.0a0-de9c32f-NOGIL/bm-20260520-macm4pro-arm64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f-vs-3.12.6.md)[📈](results/bm-20260520-3.16.0a0-de9c32f-NOGIL/bm-20260520-macm4pro-arm64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f-vs-3.12.6.svg) | 1.017x ↑<br>[📄](results/bm-20260520-3.16.0a0-de9c32f-NOGIL/bm-20260520-macm4pro-arm64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f-vs-3.13.0rc2.md)[📈](results/bm-20260520-3.16.0a0-de9c32f-NOGIL/bm-20260520-macm4pro-arm64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f-vs-3.13.0rc2.svg) | 1.021x ↓<br>[📄](results/bm-20260520-3.16.0a0-de9c32f-NOGIL/bm-20260520-macm4pro-arm64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f-vs-base.md)[📈](results/bm-20260520-3.16.0a0-de9c32f-NOGIL/bm-20260520-macm4pro-arm64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f-vs-base.svg)[🧠](results/bm-20260520-3.16.0a0-de9c32f-NOGIL/bm-20260520-macm4pro-arm64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f-vs-base-mem.svg) |


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
