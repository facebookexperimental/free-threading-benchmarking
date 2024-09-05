# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
## linux x86_64 (linux)
| date | fork/ref | hash/flags | vs. 3.12.0b1: | vs. 3.12.5+: | vs. 3.13.0b1: | vs. 3.13.0rc1+: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: | ---: | ---: |
| [2024-09-04](results/bm-20240904-3.14.0a0-aa5b4de) | mpage/gh_115999_measure_sp | aa5b4de | 1.18x ↓<br>[📄](results/bm-20240904-3.14.0a0-aa5b4de/bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de-vs-3.12.0b1.md)[📈](results/bm-20240904-3.14.0a0-aa5b4de/bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de-vs-3.12.0b1.svg) | 1.19x ↓<br>[📄](results/bm-20240904-3.14.0a0-aa5b4de/bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de-vs-3.12.5%2B.md)[📈](results/bm-20240904-3.14.0a0-aa5b4de/bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de-vs-3.12.5%2B.svg) | 1.19x ↓<br>[📄](results/bm-20240904-3.14.0a0-aa5b4de/bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de-vs-3.13.0b1.md)[📈](results/bm-20240904-3.14.0a0-aa5b4de/bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de-vs-3.13.0b1.svg) | 1.23x ↓<br>[📄](results/bm-20240904-3.14.0a0-aa5b4de/bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de-vs-3.13.0rc1%2B.md)[📈](results/bm-20240904-3.14.0a0-aa5b4de/bm-20240904-linux-x86_64-mpage-gh_115999_measure_sp-3.14.0a0-aa5b4de-vs-3.13.0rc1%2B.svg) |  |
| [2024-09-04](results/bm-20240904-3.14.0a0-54aaf26) | mpage/54aaf26e128d0a2658d3 | 54aaf26 | 1.14x ↓<br>[📄](results/bm-20240904-3.14.0a0-54aaf26/bm-20240904-linux-x86_64-mpage-54aaf26e128d0a2658d3-3.14.0a0-54aaf26-vs-3.12.0b1.md)[📈](results/bm-20240904-3.14.0a0-54aaf26/bm-20240904-linux-x86_64-mpage-54aaf26e128d0a2658d3-3.14.0a0-54aaf26-vs-3.12.0b1.svg) | 1.15x ↓<br>[📄](results/bm-20240904-3.14.0a0-54aaf26/bm-20240904-linux-x86_64-mpage-54aaf26e128d0a2658d3-3.14.0a0-54aaf26-vs-3.12.5%2B.md)[📈](results/bm-20240904-3.14.0a0-54aaf26/bm-20240904-linux-x86_64-mpage-54aaf26e128d0a2658d3-3.14.0a0-54aaf26-vs-3.12.5%2B.svg) | 1.15x ↓<br>[📄](results/bm-20240904-3.14.0a0-54aaf26/bm-20240904-linux-x86_64-mpage-54aaf26e128d0a2658d3-3.14.0a0-54aaf26-vs-3.13.0b1.md)[📈](results/bm-20240904-3.14.0a0-54aaf26/bm-20240904-linux-x86_64-mpage-54aaf26e128d0a2658d3-3.14.0a0-54aaf26-vs-3.13.0b1.svg) | 1.19x ↓<br>[📄](results/bm-20240904-3.14.0a0-54aaf26/bm-20240904-linux-x86_64-mpage-54aaf26e128d0a2658d3-3.14.0a0-54aaf26-vs-3.13.0rc1%2B.md)[📈](results/bm-20240904-3.14.0a0-54aaf26/bm-20240904-linux-x86_64-mpage-54aaf26e128d0a2658d3-3.14.0a0-54aaf26-vs-3.13.0rc1%2B.svg) |  |
| [2024-09-04](results/bm-20240904-3.14.0a0-4e34246) | mpage/4e342460d0e29cb8aa37 | 4e34246 | 1.12x ↓<br>[📄](results/bm-20240904-3.14.0a0-4e34246/bm-20240904-linux-x86_64-mpage-4e342460d0e29cb8aa37-3.14.0a0-4e34246-vs-3.12.0b1.md)[📈](results/bm-20240904-3.14.0a0-4e34246/bm-20240904-linux-x86_64-mpage-4e342460d0e29cb8aa37-3.14.0a0-4e34246-vs-3.12.0b1.svg) | 1.13x ↓<br>[📄](results/bm-20240904-3.14.0a0-4e34246/bm-20240904-linux-x86_64-mpage-4e342460d0e29cb8aa37-3.14.0a0-4e34246-vs-3.12.5%2B.md)[📈](results/bm-20240904-3.14.0a0-4e34246/bm-20240904-linux-x86_64-mpage-4e342460d0e29cb8aa37-3.14.0a0-4e34246-vs-3.12.5%2B.svg) | 1.12x ↓<br>[📄](results/bm-20240904-3.14.0a0-4e34246/bm-20240904-linux-x86_64-mpage-4e342460d0e29cb8aa37-3.14.0a0-4e34246-vs-3.13.0b1.md)[📈](results/bm-20240904-3.14.0a0-4e34246/bm-20240904-linux-x86_64-mpage-4e342460d0e29cb8aa37-3.14.0a0-4e34246-vs-3.13.0b1.svg) | 1.16x ↓<br>[📄](results/bm-20240904-3.14.0a0-4e34246/bm-20240904-linux-x86_64-mpage-4e342460d0e29cb8aa37-3.14.0a0-4e34246-vs-3.13.0rc1%2B.md)[📈](results/bm-20240904-3.14.0a0-4e34246/bm-20240904-linux-x86_64-mpage-4e342460d0e29cb8aa37-3.14.0a0-4e34246-vs-3.13.0rc1%2B.svg) |  |
| [2024-09-04](results/bm-20240904-3.14.0a0-46bf4ea) | mpage/46bf4eaf725277b31d1e | 46bf4ea | 1.22x ↓<br>[📄](results/bm-20240904-3.14.0a0-46bf4ea/bm-20240904-linux-x86_64-mpage-46bf4eaf725277b31d1e-3.14.0a0-46bf4ea-vs-3.12.0b1.md)[📈](results/bm-20240904-3.14.0a0-46bf4ea/bm-20240904-linux-x86_64-mpage-46bf4eaf725277b31d1e-3.14.0a0-46bf4ea-vs-3.12.0b1.svg) | 1.23x ↓<br>[📄](results/bm-20240904-3.14.0a0-46bf4ea/bm-20240904-linux-x86_64-mpage-46bf4eaf725277b31d1e-3.14.0a0-46bf4ea-vs-3.12.5%2B.md)[📈](results/bm-20240904-3.14.0a0-46bf4ea/bm-20240904-linux-x86_64-mpage-46bf4eaf725277b31d1e-3.14.0a0-46bf4ea-vs-3.12.5%2B.svg) | 1.22x ↓<br>[📄](results/bm-20240904-3.14.0a0-46bf4ea/bm-20240904-linux-x86_64-mpage-46bf4eaf725277b31d1e-3.14.0a0-46bf4ea-vs-3.13.0b1.md)[📈](results/bm-20240904-3.14.0a0-46bf4ea/bm-20240904-linux-x86_64-mpage-46bf4eaf725277b31d1e-3.14.0a0-46bf4ea-vs-3.13.0b1.svg) | 1.27x ↓<br>[📄](results/bm-20240904-3.14.0a0-46bf4ea/bm-20240904-linux-x86_64-mpage-46bf4eaf725277b31d1e-3.14.0a0-46bf4ea-vs-3.13.0rc1%2B.md)[📈](results/bm-20240904-3.14.0a0-46bf4ea/bm-20240904-linux-x86_64-mpage-46bf4eaf725277b31d1e-3.14.0a0-46bf4ea-vs-3.13.0rc1%2B.svg) |  |
| [2024-09-04](results/bm-20240904-3.14.0a0-e9703fe) | mpage/e9703fe2c8a71be5a555 | e9703fe | 1.21x ↓<br>[📄](results/bm-20240904-3.14.0a0-e9703fe/bm-20240904-linux-x86_64-mpage-e9703fe2c8a71be5a555-3.14.0a0-e9703fe-vs-3.12.0b1.md)[📈](results/bm-20240904-3.14.0a0-e9703fe/bm-20240904-linux-x86_64-mpage-e9703fe2c8a71be5a555-3.14.0a0-e9703fe-vs-3.12.0b1.svg) | 1.22x ↓<br>[📄](results/bm-20240904-3.14.0a0-e9703fe/bm-20240904-linux-x86_64-mpage-e9703fe2c8a71be5a555-3.14.0a0-e9703fe-vs-3.12.5%2B.md)[📈](results/bm-20240904-3.14.0a0-e9703fe/bm-20240904-linux-x86_64-mpage-e9703fe2c8a71be5a555-3.14.0a0-e9703fe-vs-3.12.5%2B.svg) | 1.22x ↓<br>[📄](results/bm-20240904-3.14.0a0-e9703fe/bm-20240904-linux-x86_64-mpage-e9703fe2c8a71be5a555-3.14.0a0-e9703fe-vs-3.13.0b1.md)[📈](results/bm-20240904-3.14.0a0-e9703fe/bm-20240904-linux-x86_64-mpage-e9703fe2c8a71be5a555-3.14.0a0-e9703fe-vs-3.13.0b1.svg) | 1.27x ↓<br>[📄](results/bm-20240904-3.14.0a0-e9703fe/bm-20240904-linux-x86_64-mpage-e9703fe2c8a71be5a555-3.14.0a0-e9703fe-vs-3.13.0rc1%2B.md)[📈](results/bm-20240904-3.14.0a0-e9703fe/bm-20240904-linux-x86_64-mpage-e9703fe2c8a71be5a555-3.14.0a0-e9703fe-vs-3.13.0rc1%2B.svg) |  |
| [2024-09-04](results/bm-20240904-3.14.0a0-92f0820) | mpage/92f0820644f2f4312161 | 92f0820 | 1.23x ↓<br>[📄](results/bm-20240904-3.14.0a0-92f0820/bm-20240904-linux-x86_64-mpage-92f0820644f2f4312161-3.14.0a0-92f0820-vs-3.12.0b1.md)[📈](results/bm-20240904-3.14.0a0-92f0820/bm-20240904-linux-x86_64-mpage-92f0820644f2f4312161-3.14.0a0-92f0820-vs-3.12.0b1.svg) | 1.24x ↓<br>[📄](results/bm-20240904-3.14.0a0-92f0820/bm-20240904-linux-x86_64-mpage-92f0820644f2f4312161-3.14.0a0-92f0820-vs-3.12.5%2B.md)[📈](results/bm-20240904-3.14.0a0-92f0820/bm-20240904-linux-x86_64-mpage-92f0820644f2f4312161-3.14.0a0-92f0820-vs-3.12.5%2B.svg) | 1.24x ↓<br>[📄](results/bm-20240904-3.14.0a0-92f0820/bm-20240904-linux-x86_64-mpage-92f0820644f2f4312161-3.14.0a0-92f0820-vs-3.13.0b1.md)[📈](results/bm-20240904-3.14.0a0-92f0820/bm-20240904-linux-x86_64-mpage-92f0820644f2f4312161-3.14.0a0-92f0820-vs-3.13.0b1.svg) | 1.29x ↓<br>[📄](results/bm-20240904-3.14.0a0-92f0820/bm-20240904-linux-x86_64-mpage-92f0820644f2f4312161-3.14.0a0-92f0820-vs-3.13.0rc1%2B.md)[📈](results/bm-20240904-3.14.0a0-92f0820/bm-20240904-linux-x86_64-mpage-92f0820644f2f4312161-3.14.0a0-92f0820-vs-3.13.0rc1%2B.svg) |  |
| [2024-09-04](results/bm-20240904-3.14.0a0-fa662e0) | mpage/fa662e0b71a91c279cd2 | fa662e0 | 1.15x ↓<br>[📄](results/bm-20240904-3.14.0a0-fa662e0/bm-20240904-linux-x86_64-mpage-fa662e0b71a91c279cd2-3.14.0a0-fa662e0-vs-3.12.0b1.md)[📈](results/bm-20240904-3.14.0a0-fa662e0/bm-20240904-linux-x86_64-mpage-fa662e0b71a91c279cd2-3.14.0a0-fa662e0-vs-3.12.0b1.svg) | 1.16x ↓<br>[📄](results/bm-20240904-3.14.0a0-fa662e0/bm-20240904-linux-x86_64-mpage-fa662e0b71a91c279cd2-3.14.0a0-fa662e0-vs-3.12.5%2B.md)[📈](results/bm-20240904-3.14.0a0-fa662e0/bm-20240904-linux-x86_64-mpage-fa662e0b71a91c279cd2-3.14.0a0-fa662e0-vs-3.12.5%2B.svg) | 1.15x ↓<br>[📄](results/bm-20240904-3.14.0a0-fa662e0/bm-20240904-linux-x86_64-mpage-fa662e0b71a91c279cd2-3.14.0a0-fa662e0-vs-3.13.0b1.md)[📈](results/bm-20240904-3.14.0a0-fa662e0/bm-20240904-linux-x86_64-mpage-fa662e0b71a91c279cd2-3.14.0a0-fa662e0-vs-3.13.0b1.svg) | 1.20x ↓<br>[📄](results/bm-20240904-3.14.0a0-fa662e0/bm-20240904-linux-x86_64-mpage-fa662e0b71a91c279cd2-3.14.0a0-fa662e0-vs-3.13.0rc1%2B.md)[📈](results/bm-20240904-3.14.0a0-fa662e0/bm-20240904-linux-x86_64-mpage-fa662e0b71a91c279cd2-3.14.0a0-fa662e0-vs-3.13.0rc1%2B.svg) |  |
| [2024-09-04](results/bm-20240904-3.14.0a0-5772b0d) | mpage/5772b0d9ab7cfd06d6df | 5772b0d | 1.20x ↓<br>[📄](results/bm-20240904-3.14.0a0-5772b0d/bm-20240904-linux-x86_64-mpage-5772b0d9ab7cfd06d6df-3.14.0a0-5772b0d-vs-3.12.0b1.md)[📈](results/bm-20240904-3.14.0a0-5772b0d/bm-20240904-linux-x86_64-mpage-5772b0d9ab7cfd06d6df-3.14.0a0-5772b0d-vs-3.12.0b1.svg) | 1.21x ↓<br>[📄](results/bm-20240904-3.14.0a0-5772b0d/bm-20240904-linux-x86_64-mpage-5772b0d9ab7cfd06d6df-3.14.0a0-5772b0d-vs-3.12.5%2B.md)[📈](results/bm-20240904-3.14.0a0-5772b0d/bm-20240904-linux-x86_64-mpage-5772b0d9ab7cfd06d6df-3.14.0a0-5772b0d-vs-3.12.5%2B.svg) | 1.21x ↓<br>[📄](results/bm-20240904-3.14.0a0-5772b0d/bm-20240904-linux-x86_64-mpage-5772b0d9ab7cfd06d6df-3.14.0a0-5772b0d-vs-3.13.0b1.md)[📈](results/bm-20240904-3.14.0a0-5772b0d/bm-20240904-linux-x86_64-mpage-5772b0d9ab7cfd06d6df-3.14.0a0-5772b0d-vs-3.13.0b1.svg) | 1.25x ↓<br>[📄](results/bm-20240904-3.14.0a0-5772b0d/bm-20240904-linux-x86_64-mpage-5772b0d9ab7cfd06d6df-3.14.0a0-5772b0d-vs-3.13.0rc1%2B.md)[📈](results/bm-20240904-3.14.0a0-5772b0d/bm-20240904-linux-x86_64-mpage-5772b0d9ab7cfd06d6df-3.14.0a0-5772b0d-vs-3.13.0rc1%2B.svg) |  |
| [2024-09-04](results/bm-20240904-3.14.0a0-4a8e3ba) | mpage/4a8e3ba765dc0858d743 | 4a8e3ba | 1.17x ↓<br>[📄](results/bm-20240904-3.14.0a0-4a8e3ba/bm-20240904-linux-x86_64-mpage-4a8e3ba765dc0858d743-3.14.0a0-4a8e3ba-vs-3.12.0b1.md)[📈](results/bm-20240904-3.14.0a0-4a8e3ba/bm-20240904-linux-x86_64-mpage-4a8e3ba765dc0858d743-3.14.0a0-4a8e3ba-vs-3.12.0b1.svg) | 1.18x ↓<br>[📄](results/bm-20240904-3.14.0a0-4a8e3ba/bm-20240904-linux-x86_64-mpage-4a8e3ba765dc0858d743-3.14.0a0-4a8e3ba-vs-3.12.5%2B.md)[📈](results/bm-20240904-3.14.0a0-4a8e3ba/bm-20240904-linux-x86_64-mpage-4a8e3ba765dc0858d743-3.14.0a0-4a8e3ba-vs-3.12.5%2B.svg) | 1.18x ↓<br>[📄](results/bm-20240904-3.14.0a0-4a8e3ba/bm-20240904-linux-x86_64-mpage-4a8e3ba765dc0858d743-3.14.0a0-4a8e3ba-vs-3.13.0b1.md)[📈](results/bm-20240904-3.14.0a0-4a8e3ba/bm-20240904-linux-x86_64-mpage-4a8e3ba765dc0858d743-3.14.0a0-4a8e3ba-vs-3.13.0b1.svg) | 1.22x ↓<br>[📄](results/bm-20240904-3.14.0a0-4a8e3ba/bm-20240904-linux-x86_64-mpage-4a8e3ba765dc0858d743-3.14.0a0-4a8e3ba-vs-3.13.0rc1%2B.md)[📈](results/bm-20240904-3.14.0a0-4a8e3ba/bm-20240904-linux-x86_64-mpage-4a8e3ba765dc0858d743-3.14.0a0-4a8e3ba-vs-3.13.0rc1%2B.svg) |  |
| [2024-09-03](results/bm-20240903-3.14.0a0-d8a840b-NOGIL) | mpage/gh_115999_thread_loc | d8a840b (NOGIL) | 1.36x ↓<br>[📄](results/bm-20240903-3.14.0a0-d8a840b-NOGIL/bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b-vs-3.12.0b1.md)[📈](results/bm-20240903-3.14.0a0-d8a840b-NOGIL/bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b-vs-3.12.0b1.svg) | 1.38x ↓<br>[📄](results/bm-20240903-3.14.0a0-d8a840b-NOGIL/bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b-vs-3.12.5%2B.md)[📈](results/bm-20240903-3.14.0a0-d8a840b-NOGIL/bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b-vs-3.12.5%2B.svg) | 1.37x ↓<br>[📄](results/bm-20240903-3.14.0a0-d8a840b-NOGIL/bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b-vs-3.13.0b1.md)[📈](results/bm-20240903-3.14.0a0-d8a840b-NOGIL/bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b-vs-3.13.0b1.svg) | 1.42x ↓<br>[📄](results/bm-20240903-3.14.0a0-d8a840b-NOGIL/bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b-vs-3.13.0rc1%2B.md)[📈](results/bm-20240903-3.14.0a0-d8a840b-NOGIL/bm-20240903-linux-x86_64-mpage-gh_115999_thread_loc-3.14.0a0-d8a840b-vs-3.13.0rc1%2B.svg) |  |


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
