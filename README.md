# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
## linux x86_64 (linux)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2024-09-30](results/bm-20240930-3.14.0a0-e44eebf) | python/main | e44eebf | not sig<br>[📄](results/bm-20240930-3.14.0a0-e44eebf/bm-20240930-linux-x86_64-python-main-3.14.0a0-e44eebf-vs-3.12.6.md)[📈](results/bm-20240930-3.14.0a0-e44eebf/bm-20240930-linux-x86_64-python-main-3.14.0a0-e44eebf-vs-3.12.6.svg) | not sig<br>[📄](results/bm-20240930-3.14.0a0-e44eebf/bm-20240930-linux-x86_64-python-main-3.14.0a0-e44eebf-vs-3.13.0rc2.md)[📈](results/bm-20240930-3.14.0a0-e44eebf/bm-20240930-linux-x86_64-python-main-3.14.0a0-e44eebf-vs-3.13.0rc2.svg) |  |
| [2024-09-30](results/bm-20240930-3.14.0a0-fac5e7a) | python/fac5e7aa171f8547fcb5 | fac5e7a | not sig<br>[📄](results/bm-20240930-3.14.0a0-fac5e7a/bm-20240930-linux-x86_64-python-fac5e7aa171f8547fcb5-3.14.0a0-fac5e7a-vs-3.12.6.md)[📈](results/bm-20240930-3.14.0a0-fac5e7a/bm-20240930-linux-x86_64-python-fac5e7aa171f8547fcb5-3.14.0a0-fac5e7a-vs-3.12.6.svg) | not sig<br>[📄](results/bm-20240930-3.14.0a0-fac5e7a/bm-20240930-linux-x86_64-python-fac5e7aa171f8547fcb5-3.14.0a0-fac5e7a-vs-3.13.0rc2.md)[📈](results/bm-20240930-3.14.0a0-fac5e7a/bm-20240930-linux-x86_64-python-fac5e7aa171f8547fcb5-3.14.0a0-fac5e7a-vs-3.13.0rc2.svg) |  |
| [2024-09-30](results/bm-20240930-3.14.0a0-fac5e7a-NOGIL) | python/fac5e7aa171f8547fcb5 | fac5e7a (NOGIL) | not sig<br>[📄](results/bm-20240930-3.14.0a0-fac5e7a-NOGIL/bm-20240930-linux-x86_64-python-fac5e7aa171f8547fcb5-3.14.0a0-fac5e7a-vs-3.12.6.md)[📈](results/bm-20240930-3.14.0a0-fac5e7a-NOGIL/bm-20240930-linux-x86_64-python-fac5e7aa171f8547fcb5-3.14.0a0-fac5e7a-vs-3.12.6.svg) | not sig<br>[📄](results/bm-20240930-3.14.0a0-fac5e7a-NOGIL/bm-20240930-linux-x86_64-python-fac5e7aa171f8547fcb5-3.14.0a0-fac5e7a-vs-3.13.0rc2.md)[📈](results/bm-20240930-3.14.0a0-fac5e7a-NOGIL/bm-20240930-linux-x86_64-python-fac5e7aa171f8547fcb5-3.14.0a0-fac5e7a-vs-3.13.0rc2.svg) | not sig<br>[📄](results/bm-20240930-3.14.0a0-fac5e7a-NOGIL/bm-20240930-linux-x86_64-python-fac5e7aa171f8547fcb5-3.14.0a0-fac5e7a-vs-base.md)[📈](results/bm-20240930-3.14.0a0-fac5e7a-NOGIL/bm-20240930-linux-x86_64-python-fac5e7aa171f8547fcb5-3.14.0a0-fac5e7a-vs-base.svg)[🧠](results/bm-20240930-3.14.0a0-fac5e7a-NOGIL/bm-20240930-linux-x86_64-python-fac5e7aa171f8547fcb5-3.14.0a0-fac5e7a-vs-base-mem.svg) |

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2024-10-17](results/bm-20241017-3.14.0a1%2B-a0f5c8e) | python/main | a0f5c8e | 1.00x ↑<br>[📄](results/bm-20241017-3.14.0a1%2B-a0f5c8e/bm-20241017-vultr-x86_64-python-main-3.14.0a1%2B-a0f5c8e-vs-3.12.6.md)[📈](results/bm-20241017-3.14.0a1%2B-a0f5c8e/bm-20241017-vultr-x86_64-python-main-3.14.0a1%2B-a0f5c8e-vs-3.12.6.svg) | 1.01x ↓<br>[📄](results/bm-20241017-3.14.0a1%2B-a0f5c8e/bm-20241017-vultr-x86_64-python-main-3.14.0a1%2B-a0f5c8e-vs-3.13.0rc2.md)[📈](results/bm-20241017-3.14.0a1%2B-a0f5c8e/bm-20241017-vultr-x86_64-python-main-3.14.0a1%2B-a0f5c8e-vs-3.13.0rc2.svg) |  |
| [2024-10-16](results/bm-20241016-3.14.0a1%2B-28871ed) | colesbury/gh_125608_dict_watch | 28871ed | 1.00x ↑<br>[📄](results/bm-20241016-3.14.0a1%2B-28871ed/bm-20241016-vultr-x86_64-colesbury-gh_125608_dict_watch-3.14.0a1%2B-28871ed-vs-3.12.6.md)[📈](results/bm-20241016-3.14.0a1%2B-28871ed/bm-20241016-vultr-x86_64-colesbury-gh_125608_dict_watch-3.14.0a1%2B-28871ed-vs-3.12.6.svg) | 1.01x ↓<br>[📄](results/bm-20241016-3.14.0a1%2B-28871ed/bm-20241016-vultr-x86_64-colesbury-gh_125608_dict_watch-3.14.0a1%2B-28871ed-vs-3.13.0rc2.md)[📈](results/bm-20241016-3.14.0a1%2B-28871ed/bm-20241016-vultr-x86_64-colesbury-gh_125608_dict_watch-3.14.0a1%2B-28871ed-vs-3.13.0rc2.svg) | 1.00x ↓<br>[📄](results/bm-20241016-3.14.0a1%2B-28871ed/bm-20241016-vultr-x86_64-colesbury-gh_125608_dict_watch-3.14.0a1%2B-28871ed-vs-base.md)[📈](results/bm-20241016-3.14.0a1%2B-28871ed/bm-20241016-vultr-x86_64-colesbury-gh_125608_dict_watch-3.14.0a1%2B-28871ed-vs-base.svg)[🧠](results/bm-20241016-3.14.0a1%2B-28871ed/bm-20241016-vultr-x86_64-colesbury-gh_125608_dict_watch-3.14.0a1%2B-28871ed-vs-base-mem.svg) |
| [2024-10-16](results/bm-20241016-3.14.0a1%2B-3a126a8) | colesbury/gh_125610_STORE_ATTR | 3a126a8 | 1.01x ↓<br>[📄](results/bm-20241016-3.14.0a1%2B-3a126a8/bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1%2B-3a126a8-vs-3.12.6.md)[📈](results/bm-20241016-3.14.0a1%2B-3a126a8/bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1%2B-3a126a8-vs-3.12.6.svg) | 1.02x ↓<br>[📄](results/bm-20241016-3.14.0a1%2B-3a126a8/bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1%2B-3a126a8-vs-3.13.0rc2.md)[📈](results/bm-20241016-3.14.0a1%2B-3a126a8/bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1%2B-3a126a8-vs-3.13.0rc2.svg) | 1.01x ↓<br>[📄](results/bm-20241016-3.14.0a1%2B-3a126a8/bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1%2B-3a126a8-vs-base.md)[📈](results/bm-20241016-3.14.0a1%2B-3a126a8/bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1%2B-3a126a8-vs-base.svg)[🧠](results/bm-20241016-3.14.0a1%2B-3a126a8/bm-20241016-vultr-x86_64-colesbury-gh_125610_STORE_ATTR-3.14.0a1%2B-3a126a8-vs-base-mem.svg) |
| [2024-10-16](results/bm-20241016-3.14.0a1%2B-760872e) | python/760872efecb95017db8e | 760872e | 1.00x ↑<br>[📄](results/bm-20241016-3.14.0a1%2B-760872e/bm-20241016-vultr-x86_64-python-760872efecb95017db8e-3.14.0a1%2B-760872e-vs-3.12.6.md)[📈](results/bm-20241016-3.14.0a1%2B-760872e/bm-20241016-vultr-x86_64-python-760872efecb95017db8e-3.14.0a1%2B-760872e-vs-3.12.6.svg) | 1.01x ↓<br>[📄](results/bm-20241016-3.14.0a1%2B-760872e/bm-20241016-vultr-x86_64-python-760872efecb95017db8e-3.14.0a1%2B-760872e-vs-3.13.0rc2.md)[📈](results/bm-20241016-3.14.0a1%2B-760872e/bm-20241016-vultr-x86_64-python-760872efecb95017db8e-3.14.0a1%2B-760872e-vs-3.13.0rc2.svg) |  |
| [2024-10-14](results/bm-20241014-3.14.0a0-cf0f4ec-NOGIL) | mpage/gh_115999_tlbc_load_ | cf0f4ec (NOGIL) | 1.45x ↓<br>[📄](results/bm-20241014-3.14.0a0-cf0f4ec-NOGIL/bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-cf0f4ec-vs-3.12.6.md)[📈](results/bm-20241014-3.14.0a0-cf0f4ec-NOGIL/bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-cf0f4ec-vs-3.12.6.svg) | 1.48x ↓<br>[📄](results/bm-20241014-3.14.0a0-cf0f4ec-NOGIL/bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-cf0f4ec-vs-3.13.0rc2.md)[📈](results/bm-20241014-3.14.0a0-cf0f4ec-NOGIL/bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-cf0f4ec-vs-3.13.0rc2.svg) | 1.06x ↑<br>[📄](results/bm-20241014-3.14.0a0-cf0f4ec-NOGIL/bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-cf0f4ec-vs-base.md)[📈](results/bm-20241014-3.14.0a0-cf0f4ec-NOGIL/bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-cf0f4ec-vs-base.svg)[🧠](results/bm-20241014-3.14.0a0-cf0f4ec-NOGIL/bm-20241014-vultr-x86_64-mpage-gh_115999_tlbc_load_-3.14.0a0-cf0f4ec-vs-base-mem.svg) |
| [2024-10-13](results/bm-20241013-3.14.0a0-f1d33db-NOGIL) | python/f1d33dbddd3496b062e1 | f1d33db (NOGIL) | 1.54x ↓<br>[📄](results/bm-20241013-3.14.0a0-f1d33db-NOGIL/bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db-vs-3.12.6.md)[📈](results/bm-20241013-3.14.0a0-f1d33db-NOGIL/bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db-vs-3.12.6.svg) | 1.57x ↓<br>[📄](results/bm-20241013-3.14.0a0-f1d33db-NOGIL/bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db-vs-3.13.0rc2.md)[📈](results/bm-20241013-3.14.0a0-f1d33db-NOGIL/bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db-vs-3.13.0rc2.svg) |  |


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
