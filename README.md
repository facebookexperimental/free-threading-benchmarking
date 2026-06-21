# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (6ce088e)](results/bm-20260614-3.16.0a0-6ce088e/bm-20260614-vultr-x86_64-python-6ce088e20a13ac25320d-3.16.0a0-6ce088e-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (1b9fe5c)](results/bm-20260621-3.16.0a0-1b9fe5c-PYTHON_UOPS/bm-20260621-vultr-x86_64-python-1b9fe5c7226eccc8b269-3.16.0a0-1b9fe5c-pystats.md)
- [Most recent JIT pystats on main (bedaea0)](results/bm-20251019-3.15.0a1%2B-bedaea0-JIT/bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-06-19](results/bm-20260619-3.16.0a0-a9db5cb-NOGIL) | python/a9db5cb52fefffc8fcdd | a9db5cb (NOGIL) | 1.036x ↓<br>[📄](results/bm-20260619-3.16.0a0-a9db5cb-NOGIL/bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb-vs-3.12.6.md)[📈](results/bm-20260619-3.16.0a0-a9db5cb-NOGIL/bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb-vs-3.12.6.svg) | 1.069x ↓<br>[📄](results/bm-20260619-3.16.0a0-a9db5cb-NOGIL/bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb-vs-3.13.0rc2.md)[📈](results/bm-20260619-3.16.0a0-a9db5cb-NOGIL/bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb-vs-3.13.0rc2.svg) | 1.110x ↓<br>[📄](results/bm-20260619-3.16.0a0-a9db5cb-NOGIL/bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb-vs-base.md)[📈](results/bm-20260619-3.16.0a0-a9db5cb-NOGIL/bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb-vs-base.svg)[🧠](results/bm-20260619-3.16.0a0-a9db5cb-NOGIL/bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb-vs-base-mem.svg) |
| [2026-06-19](results/bm-20260619-3.16.0a0-a9db5cb) | python/a9db5cb52fefffc8fcdd | a9db5cb | 1.078x ↑<br>[📄](results/bm-20260619-3.16.0a0-a9db5cb/bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb-vs-3.12.6.md)[📈](results/bm-20260619-3.16.0a0-a9db5cb/bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb-vs-3.12.6.svg) | 1.041x ↑<br>[📄](results/bm-20260619-3.16.0a0-a9db5cb/bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb-vs-3.13.0rc2.md)[📈](results/bm-20260619-3.16.0a0-a9db5cb/bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb-vs-3.13.0rc2.svg) |  |
| [2026-06-19](results/bm-20260619-3.16.0a0-d701f8e-NOGIL) | python/d701f8edbe2884e3e039 | d701f8e (NOGIL) | 1.033x ↓<br>[📄](results/bm-20260619-3.16.0a0-d701f8e-NOGIL/bm-20260619-vultr-x86_64-python-d701f8edbe2884e3e039-3.16.0a0-d701f8e-vs-3.12.6.md)[📈](results/bm-20260619-3.16.0a0-d701f8e-NOGIL/bm-20260619-vultr-x86_64-python-d701f8edbe2884e3e039-3.16.0a0-d701f8e-vs-3.12.6.svg) | 1.066x ↓<br>[📄](results/bm-20260619-3.16.0a0-d701f8e-NOGIL/bm-20260619-vultr-x86_64-python-d701f8edbe2884e3e039-3.16.0a0-d701f8e-vs-3.13.0rc2.md)[📈](results/bm-20260619-3.16.0a0-d701f8e-NOGIL/bm-20260619-vultr-x86_64-python-d701f8edbe2884e3e039-3.16.0a0-d701f8e-vs-3.13.0rc2.svg) | 1.110x ↓<br>[📄](results/bm-20260619-3.16.0a0-d701f8e-NOGIL/bm-20260619-vultr-x86_64-python-d701f8edbe2884e3e039-3.16.0a0-d701f8e-vs-base.md)[📈](results/bm-20260619-3.16.0a0-d701f8e-NOGIL/bm-20260619-vultr-x86_64-python-d701f8edbe2884e3e039-3.16.0a0-d701f8e-vs-base.svg)[🧠](results/bm-20260619-3.16.0a0-d701f8e-NOGIL/bm-20260619-vultr-x86_64-python-d701f8edbe2884e3e039-3.16.0a0-d701f8e-vs-base-mem.svg) |
| [2026-06-19](results/bm-20260619-3.16.0a0-d701f8e) | python/d701f8edbe2884e3e039 | d701f8e | 1.082x ↑<br>[📄](results/bm-20260619-3.16.0a0-d701f8e/bm-20260619-vultr-x86_64-python-d701f8edbe2884e3e039-3.16.0a0-d701f8e-vs-3.12.6.md)[📈](results/bm-20260619-3.16.0a0-d701f8e/bm-20260619-vultr-x86_64-python-d701f8edbe2884e3e039-3.16.0a0-d701f8e-vs-3.12.6.svg) | 1.045x ↑<br>[📄](results/bm-20260619-3.16.0a0-d701f8e/bm-20260619-vultr-x86_64-python-d701f8edbe2884e3e039-3.16.0a0-d701f8e-vs-3.13.0rc2.md)[📈](results/bm-20260619-3.16.0a0-d701f8e/bm-20260619-vultr-x86_64-python-d701f8edbe2884e3e039-3.16.0a0-d701f8e-vs-3.13.0rc2.svg) |  |
| [2026-06-18](results/bm-20260618-3.16.0a0-8d7c6dc-NOGIL) | python/8d7c6dcde053eec618d8 | 8d7c6dc (NOGIL) | 1.035x ↓<br>[📄](results/bm-20260618-3.16.0a0-8d7c6dc-NOGIL/bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc-vs-3.12.6.md)[📈](results/bm-20260618-3.16.0a0-8d7c6dc-NOGIL/bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc-vs-3.12.6.svg) | 1.068x ↓<br>[📄](results/bm-20260618-3.16.0a0-8d7c6dc-NOGIL/bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc-vs-3.13.0rc2.md)[📈](results/bm-20260618-3.16.0a0-8d7c6dc-NOGIL/bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc-vs-3.13.0rc2.svg) | 1.102x ↓<br>[📄](results/bm-20260618-3.16.0a0-8d7c6dc-NOGIL/bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc-vs-base.md)[📈](results/bm-20260618-3.16.0a0-8d7c6dc-NOGIL/bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc-vs-base.svg)[🧠](results/bm-20260618-3.16.0a0-8d7c6dc-NOGIL/bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc-vs-base-mem.svg) |
| [2026-06-18](results/bm-20260618-3.16.0a0-8d7c6dc) | python/8d7c6dcde053eec618d8 | 8d7c6dc | 1.069x ↑<br>[📄](results/bm-20260618-3.16.0a0-8d7c6dc/bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc-vs-3.12.6.md)[📈](results/bm-20260618-3.16.0a0-8d7c6dc/bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc-vs-3.12.6.svg) | 1.033x ↑<br>[📄](results/bm-20260618-3.16.0a0-8d7c6dc/bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc-vs-3.13.0rc2.md)[📈](results/bm-20260618-3.16.0a0-8d7c6dc/bm-20260618-vultr-x86_64-python-8d7c6dcde053eec618d8-3.16.0a0-8d7c6dc-vs-3.13.0rc2.svg) |  |

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
