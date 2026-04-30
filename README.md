# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (c5fcdb4)](results/bm-20260425-3.15.0a8%2B-c5fcdb4/bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8%2B-c5fcdb4-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (c5fcdb4)](results/bm-20260425-3.15.0a8%2B-c5fcdb4-PYTHON_UOPS/bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8%2B-c5fcdb4-pystats.md)
- [Most recent JIT pystats on main (bedaea0)](results/bm-20251019-3.15.0a1%2B-bedaea0-JIT/bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-04-29](results/bm-20260429-3.15.0a8%2B-8851a06-NOGIL) | python/8851a06e6e7ff23d91e5 | 8851a06 (NOGIL) | 1.014x ↓<br>[📄](results/bm-20260429-3.15.0a8%2B-8851a06-NOGIL/bm-20260429-vultr-x86_64-python-8851a06e6e7ff23d91e5-3.15.0a8%2B-8851a06-vs-3.12.6.md)[📈](results/bm-20260429-3.15.0a8%2B-8851a06-NOGIL/bm-20260429-vultr-x86_64-python-8851a06e6e7ff23d91e5-3.15.0a8%2B-8851a06-vs-3.12.6.svg) | 1.046x ↓<br>[📄](results/bm-20260429-3.15.0a8%2B-8851a06-NOGIL/bm-20260429-vultr-x86_64-python-8851a06e6e7ff23d91e5-3.15.0a8%2B-8851a06-vs-3.13.0rc2.md)[📈](results/bm-20260429-3.15.0a8%2B-8851a06-NOGIL/bm-20260429-vultr-x86_64-python-8851a06e6e7ff23d91e5-3.15.0a8%2B-8851a06-vs-3.13.0rc2.svg) | 1.097x ↓<br>[📄](results/bm-20260429-3.15.0a8%2B-8851a06-NOGIL/bm-20260429-vultr-x86_64-python-8851a06e6e7ff23d91e5-3.15.0a8%2B-8851a06-vs-base.md)[📈](results/bm-20260429-3.15.0a8%2B-8851a06-NOGIL/bm-20260429-vultr-x86_64-python-8851a06e6e7ff23d91e5-3.15.0a8%2B-8851a06-vs-base.svg)[🧠](results/bm-20260429-3.15.0a8%2B-8851a06-NOGIL/bm-20260429-vultr-x86_64-python-8851a06e6e7ff23d91e5-3.15.0a8%2B-8851a06-vs-base-mem.svg) |
| [2026-04-29](results/bm-20260429-3.15.0a8%2B-8851a06) | python/8851a06e6e7ff23d91e5 | 8851a06 | 1.087x ↑<br>[📄](results/bm-20260429-3.15.0a8%2B-8851a06/bm-20260429-vultr-x86_64-python-8851a06e6e7ff23d91e5-3.15.0a8%2B-8851a06-vs-3.12.6.md)[📈](results/bm-20260429-3.15.0a8%2B-8851a06/bm-20260429-vultr-x86_64-python-8851a06e6e7ff23d91e5-3.15.0a8%2B-8851a06-vs-3.12.6.svg) | 1.051x ↑<br>[📄](results/bm-20260429-3.15.0a8%2B-8851a06/bm-20260429-vultr-x86_64-python-8851a06e6e7ff23d91e5-3.15.0a8%2B-8851a06-vs-3.13.0rc2.md)[📈](results/bm-20260429-3.15.0a8%2B-8851a06/bm-20260429-vultr-x86_64-python-8851a06e6e7ff23d91e5-3.15.0a8%2B-8851a06-vs-3.13.0rc2.svg) |  |
| [2026-04-28](results/bm-20260428-3.15.0a8%2B-2674c32-NOGIL) | python/2674c322c6cc5a81ce54 | 2674c32 (NOGIL) | 1.014x ↓<br>[📄](results/bm-20260428-3.15.0a8%2B-2674c32-NOGIL/bm-20260428-vultr-x86_64-python-2674c322c6cc5a81ce54-3.15.0a8%2B-2674c32-vs-3.12.6.md)[📈](results/bm-20260428-3.15.0a8%2B-2674c32-NOGIL/bm-20260428-vultr-x86_64-python-2674c322c6cc5a81ce54-3.15.0a8%2B-2674c32-vs-3.12.6.svg) | 1.046x ↓<br>[📄](results/bm-20260428-3.15.0a8%2B-2674c32-NOGIL/bm-20260428-vultr-x86_64-python-2674c322c6cc5a81ce54-3.15.0a8%2B-2674c32-vs-3.13.0rc2.md)[📈](results/bm-20260428-3.15.0a8%2B-2674c32-NOGIL/bm-20260428-vultr-x86_64-python-2674c322c6cc5a81ce54-3.15.0a8%2B-2674c32-vs-3.13.0rc2.svg) | 1.099x ↓<br>[📄](results/bm-20260428-3.15.0a8%2B-2674c32-NOGIL/bm-20260428-vultr-x86_64-python-2674c322c6cc5a81ce54-3.15.0a8%2B-2674c32-vs-base.md)[📈](results/bm-20260428-3.15.0a8%2B-2674c32-NOGIL/bm-20260428-vultr-x86_64-python-2674c322c6cc5a81ce54-3.15.0a8%2B-2674c32-vs-base.svg)[🧠](results/bm-20260428-3.15.0a8%2B-2674c32-NOGIL/bm-20260428-vultr-x86_64-python-2674c322c6cc5a81ce54-3.15.0a8%2B-2674c32-vs-base-mem.svg) |
| [2026-04-28](results/bm-20260428-3.15.0a8%2B-2674c32) | python/2674c322c6cc5a81ce54 | 2674c32 | 1.091x ↑<br>[📄](results/bm-20260428-3.15.0a8%2B-2674c32/bm-20260428-vultr-x86_64-python-2674c322c6cc5a81ce54-3.15.0a8%2B-2674c32-vs-3.12.6.md)[📈](results/bm-20260428-3.15.0a8%2B-2674c32/bm-20260428-vultr-x86_64-python-2674c322c6cc5a81ce54-3.15.0a8%2B-2674c32-vs-3.12.6.svg) | 1.055x ↑<br>[📄](results/bm-20260428-3.15.0a8%2B-2674c32/bm-20260428-vultr-x86_64-python-2674c322c6cc5a81ce54-3.15.0a8%2B-2674c32-vs-3.13.0rc2.md)[📈](results/bm-20260428-3.15.0a8%2B-2674c32/bm-20260428-vultr-x86_64-python-2674c322c6cc5a81ce54-3.15.0a8%2B-2674c32-vs-3.13.0rc2.svg) |  |
| [2026-04-28](results/bm-20260428-3.15.0a8%2B-0efd679-NOGIL) | python/0efd679a6ce3b57ec3c5 | 0efd679 (NOGIL) | 1.009x ↓<br>[📄](results/bm-20260428-3.15.0a8%2B-0efd679-NOGIL/bm-20260428-vultr-x86_64-python-0efd679a6ce3b57ec3c5-3.15.0a8%2B-0efd679-vs-3.12.6.md)[📈](results/bm-20260428-3.15.0a8%2B-0efd679-NOGIL/bm-20260428-vultr-x86_64-python-0efd679a6ce3b57ec3c5-3.15.0a8%2B-0efd679-vs-3.12.6.svg) | 1.042x ↓<br>[📄](results/bm-20260428-3.15.0a8%2B-0efd679-NOGIL/bm-20260428-vultr-x86_64-python-0efd679a6ce3b57ec3c5-3.15.0a8%2B-0efd679-vs-3.13.0rc2.md)[📈](results/bm-20260428-3.15.0a8%2B-0efd679-NOGIL/bm-20260428-vultr-x86_64-python-0efd679a6ce3b57ec3c5-3.15.0a8%2B-0efd679-vs-3.13.0rc2.svg) | 1.092x ↓<br>[📄](results/bm-20260428-3.15.0a8%2B-0efd679-NOGIL/bm-20260428-vultr-x86_64-python-0efd679a6ce3b57ec3c5-3.15.0a8%2B-0efd679-vs-base.md)[📈](results/bm-20260428-3.15.0a8%2B-0efd679-NOGIL/bm-20260428-vultr-x86_64-python-0efd679a6ce3b57ec3c5-3.15.0a8%2B-0efd679-vs-base.svg)[🧠](results/bm-20260428-3.15.0a8%2B-0efd679-NOGIL/bm-20260428-vultr-x86_64-python-0efd679a6ce3b57ec3c5-3.15.0a8%2B-0efd679-vs-base-mem.svg) |
| [2026-04-28](results/bm-20260428-3.15.0a8%2B-0efd679) | python/0efd679a6ce3b57ec3c5 | 0efd679 | 1.086x ↑<br>[📄](results/bm-20260428-3.15.0a8%2B-0efd679/bm-20260428-vultr-x86_64-python-0efd679a6ce3b57ec3c5-3.15.0a8%2B-0efd679-vs-3.12.6.md)[📈](results/bm-20260428-3.15.0a8%2B-0efd679/bm-20260428-vultr-x86_64-python-0efd679a6ce3b57ec3c5-3.15.0a8%2B-0efd679-vs-3.12.6.svg) | 1.050x ↑<br>[📄](results/bm-20260428-3.15.0a8%2B-0efd679/bm-20260428-vultr-x86_64-python-0efd679a6ce3b57ec3c5-3.15.0a8%2B-0efd679-vs-3.13.0rc2.md)[📈](results/bm-20260428-3.15.0a8%2B-0efd679/bm-20260428-vultr-x86_64-python-0efd679a6ce3b57ec3c5-3.15.0a8%2B-0efd679-vs-3.13.0rc2.svg) |  |
| [2026-04-27](results/bm-20260427-3.15.0a8%2B-2754e9a-NOGIL) | python/2754e9a615de298b0c3a | 2754e9a (NOGIL) | 1.011x ↓<br>[📄](results/bm-20260427-3.15.0a8%2B-2754e9a-NOGIL/bm-20260427-vultr-x86_64-python-2754e9a615de298b0c3a-3.15.0a8%2B-2754e9a-vs-3.12.6.md)[📈](results/bm-20260427-3.15.0a8%2B-2754e9a-NOGIL/bm-20260427-vultr-x86_64-python-2754e9a615de298b0c3a-3.15.0a8%2B-2754e9a-vs-3.12.6.svg) | 1.044x ↓<br>[📄](results/bm-20260427-3.15.0a8%2B-2754e9a-NOGIL/bm-20260427-vultr-x86_64-python-2754e9a615de298b0c3a-3.15.0a8%2B-2754e9a-vs-3.13.0rc2.md)[📈](results/bm-20260427-3.15.0a8%2B-2754e9a-NOGIL/bm-20260427-vultr-x86_64-python-2754e9a615de298b0c3a-3.15.0a8%2B-2754e9a-vs-3.13.0rc2.svg) | 1.095x ↓<br>[📄](results/bm-20260427-3.15.0a8%2B-2754e9a-NOGIL/bm-20260427-vultr-x86_64-python-2754e9a615de298b0c3a-3.15.0a8%2B-2754e9a-vs-base.md)[📈](results/bm-20260427-3.15.0a8%2B-2754e9a-NOGIL/bm-20260427-vultr-x86_64-python-2754e9a615de298b0c3a-3.15.0a8%2B-2754e9a-vs-base.svg)[🧠](results/bm-20260427-3.15.0a8%2B-2754e9a-NOGIL/bm-20260427-vultr-x86_64-python-2754e9a615de298b0c3a-3.15.0a8%2B-2754e9a-vs-base-mem.svg) |
| [2026-04-27](results/bm-20260427-3.15.0a8%2B-2754e9a) | python/2754e9a615de298b0c3a | 2754e9a | 1.086x ↑<br>[📄](results/bm-20260427-3.15.0a8%2B-2754e9a/bm-20260427-vultr-x86_64-python-2754e9a615de298b0c3a-3.15.0a8%2B-2754e9a-vs-3.12.6.md)[📈](results/bm-20260427-3.15.0a8%2B-2754e9a/bm-20260427-vultr-x86_64-python-2754e9a615de298b0c3a-3.15.0a8%2B-2754e9a-vs-3.12.6.svg) | 1.050x ↑<br>[📄](results/bm-20260427-3.15.0a8%2B-2754e9a/bm-20260427-vultr-x86_64-python-2754e9a615de298b0c3a-3.15.0a8%2B-2754e9a-vs-3.13.0rc2.md)[📈](results/bm-20260427-3.15.0a8%2B-2754e9a/bm-20260427-vultr-x86_64-python-2754e9a615de298b0c3a-3.15.0a8%2B-2754e9a-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-04-29](results/bm-20260429-3.15.0a8%2B-8851a06-NOGIL) | python/8851a06e6e7ff23d91e5 | 8851a06 (NOGIL) | 1.120x ↑<br>[📄](results/bm-20260429-3.15.0a8%2B-8851a06-NOGIL/bm-20260429-macm4pro-arm64-python-8851a06e6e7ff23d91e5-3.15.0a8%2B-8851a06-vs-3.12.6.md)[📈](results/bm-20260429-3.15.0a8%2B-8851a06-NOGIL/bm-20260429-macm4pro-arm64-python-8851a06e6e7ff23d91e5-3.15.0a8%2B-8851a06-vs-3.12.6.svg) | 1.038x ↑<br>[📄](results/bm-20260429-3.15.0a8%2B-8851a06-NOGIL/bm-20260429-macm4pro-arm64-python-8851a06e6e7ff23d91e5-3.15.0a8%2B-8851a06-vs-3.13.0rc2.md)[📈](results/bm-20260429-3.15.0a8%2B-8851a06-NOGIL/bm-20260429-macm4pro-arm64-python-8851a06e6e7ff23d91e5-3.15.0a8%2B-8851a06-vs-3.13.0rc2.svg) | 1.056x ↓<br>[📄](results/bm-20260429-3.15.0a8%2B-8851a06-NOGIL/bm-20260429-macm4pro-arm64-python-8851a06e6e7ff23d91e5-3.15.0a8%2B-8851a06-vs-base.md)[📈](results/bm-20260429-3.15.0a8%2B-8851a06-NOGIL/bm-20260429-macm4pro-arm64-python-8851a06e6e7ff23d91e5-3.15.0a8%2B-8851a06-vs-base.svg)[🧠](results/bm-20260429-3.15.0a8%2B-8851a06-NOGIL/bm-20260429-macm4pro-arm64-python-8851a06e6e7ff23d91e5-3.15.0a8%2B-8851a06-vs-base-mem.svg) |
| [2026-04-29](results/bm-20260429-3.15.0a8%2B-8851a06) | python/8851a06e6e7ff23d91e5 | 8851a06 | 1.187x ↑<br>[📄](results/bm-20260429-3.15.0a8%2B-8851a06/bm-20260429-macm4pro-arm64-python-8851a06e6e7ff23d91e5-3.15.0a8%2B-8851a06-vs-3.12.6.md)[📈](results/bm-20260429-3.15.0a8%2B-8851a06/bm-20260429-macm4pro-arm64-python-8851a06e6e7ff23d91e5-3.15.0a8%2B-8851a06-vs-3.12.6.svg) | 1.100x ↑<br>[📄](results/bm-20260429-3.15.0a8%2B-8851a06/bm-20260429-macm4pro-arm64-python-8851a06e6e7ff23d91e5-3.15.0a8%2B-8851a06-vs-3.13.0rc2.md)[📈](results/bm-20260429-3.15.0a8%2B-8851a06/bm-20260429-macm4pro-arm64-python-8851a06e6e7ff23d91e5-3.15.0a8%2B-8851a06-vs-3.13.0rc2.svg) |  |
| [2026-04-28](results/bm-20260428-3.15.0a8%2B-2674c32-NOGIL) | python/2674c322c6cc5a81ce54 | 2674c32 (NOGIL) | 1.112x ↑<br>[📄](results/bm-20260428-3.15.0a8%2B-2674c32-NOGIL/bm-20260428-macm4pro-arm64-python-2674c322c6cc5a81ce54-3.15.0a8%2B-2674c32-vs-3.12.6.md)[📈](results/bm-20260428-3.15.0a8%2B-2674c32-NOGIL/bm-20260428-macm4pro-arm64-python-2674c322c6cc5a81ce54-3.15.0a8%2B-2674c32-vs-3.12.6.svg) | 1.031x ↑<br>[📄](results/bm-20260428-3.15.0a8%2B-2674c32-NOGIL/bm-20260428-macm4pro-arm64-python-2674c322c6cc5a81ce54-3.15.0a8%2B-2674c32-vs-3.13.0rc2.md)[📈](results/bm-20260428-3.15.0a8%2B-2674c32-NOGIL/bm-20260428-macm4pro-arm64-python-2674c322c6cc5a81ce54-3.15.0a8%2B-2674c32-vs-3.13.0rc2.svg) | 1.053x ↓<br>[📄](results/bm-20260428-3.15.0a8%2B-2674c32-NOGIL/bm-20260428-macm4pro-arm64-python-2674c322c6cc5a81ce54-3.15.0a8%2B-2674c32-vs-base.md)[📈](results/bm-20260428-3.15.0a8%2B-2674c32-NOGIL/bm-20260428-macm4pro-arm64-python-2674c322c6cc5a81ce54-3.15.0a8%2B-2674c32-vs-base.svg)[🧠](results/bm-20260428-3.15.0a8%2B-2674c32-NOGIL/bm-20260428-macm4pro-arm64-python-2674c322c6cc5a81ce54-3.15.0a8%2B-2674c32-vs-base-mem.svg) |
| [2026-04-28](results/bm-20260428-3.15.0a8%2B-2674c32) | python/2674c322c6cc5a81ce54 | 2674c32 | 1.174x ↑<br>[📄](results/bm-20260428-3.15.0a8%2B-2674c32/bm-20260428-macm4pro-arm64-python-2674c322c6cc5a81ce54-3.15.0a8%2B-2674c32-vs-3.12.6.md)[📈](results/bm-20260428-3.15.0a8%2B-2674c32/bm-20260428-macm4pro-arm64-python-2674c322c6cc5a81ce54-3.15.0a8%2B-2674c32-vs-3.12.6.svg) | 1.088x ↑<br>[📄](results/bm-20260428-3.15.0a8%2B-2674c32/bm-20260428-macm4pro-arm64-python-2674c322c6cc5a81ce54-3.15.0a8%2B-2674c32-vs-3.13.0rc2.md)[📈](results/bm-20260428-3.15.0a8%2B-2674c32/bm-20260428-macm4pro-arm64-python-2674c322c6cc5a81ce54-3.15.0a8%2B-2674c32-vs-3.13.0rc2.svg) |  |
| [2026-04-28](results/bm-20260428-3.15.0a8%2B-0efd679-NOGIL) | python/0efd679a6ce3b57ec3c5 | 0efd679 (NOGIL) | 1.108x ↑<br>[📄](results/bm-20260428-3.15.0a8%2B-0efd679-NOGIL/bm-20260428-macm4pro-arm64-python-0efd679a6ce3b57ec3c5-3.15.0a8%2B-0efd679-vs-3.12.6.md)[📈](results/bm-20260428-3.15.0a8%2B-0efd679-NOGIL/bm-20260428-macm4pro-arm64-python-0efd679a6ce3b57ec3c5-3.15.0a8%2B-0efd679-vs-3.12.6.svg) | 1.028x ↑<br>[📄](results/bm-20260428-3.15.0a8%2B-0efd679-NOGIL/bm-20260428-macm4pro-arm64-python-0efd679a6ce3b57ec3c5-3.15.0a8%2B-0efd679-vs-3.13.0rc2.md)[📈](results/bm-20260428-3.15.0a8%2B-0efd679-NOGIL/bm-20260428-macm4pro-arm64-python-0efd679a6ce3b57ec3c5-3.15.0a8%2B-0efd679-vs-3.13.0rc2.svg) | 1.056x ↓<br>[📄](results/bm-20260428-3.15.0a8%2B-0efd679-NOGIL/bm-20260428-macm4pro-arm64-python-0efd679a6ce3b57ec3c5-3.15.0a8%2B-0efd679-vs-base.md)[📈](results/bm-20260428-3.15.0a8%2B-0efd679-NOGIL/bm-20260428-macm4pro-arm64-python-0efd679a6ce3b57ec3c5-3.15.0a8%2B-0efd679-vs-base.svg)[🧠](results/bm-20260428-3.15.0a8%2B-0efd679-NOGIL/bm-20260428-macm4pro-arm64-python-0efd679a6ce3b57ec3c5-3.15.0a8%2B-0efd679-vs-base-mem.svg) |
| [2026-04-28](results/bm-20260428-3.15.0a8%2B-0efd679) | python/0efd679a6ce3b57ec3c5 | 0efd679 | 1.174x ↑<br>[📄](results/bm-20260428-3.15.0a8%2B-0efd679/bm-20260428-macm4pro-arm64-python-0efd679a6ce3b57ec3c5-3.15.0a8%2B-0efd679-vs-3.12.6.md)[📈](results/bm-20260428-3.15.0a8%2B-0efd679/bm-20260428-macm4pro-arm64-python-0efd679a6ce3b57ec3c5-3.15.0a8%2B-0efd679-vs-3.12.6.svg) | 1.089x ↑<br>[📄](results/bm-20260428-3.15.0a8%2B-0efd679/bm-20260428-macm4pro-arm64-python-0efd679a6ce3b57ec3c5-3.15.0a8%2B-0efd679-vs-3.13.0rc2.md)[📈](results/bm-20260428-3.15.0a8%2B-0efd679/bm-20260428-macm4pro-arm64-python-0efd679a6ce3b57ec3c5-3.15.0a8%2B-0efd679-vs-3.13.0rc2.svg) |  |
| [2026-04-27](results/bm-20260427-3.15.0a8%2B-2754e9a-NOGIL) | python/2754e9a615de298b0c3a | 2754e9a (NOGIL) | 1.114x ↑<br>[📄](results/bm-20260427-3.15.0a8%2B-2754e9a-NOGIL/bm-20260427-macm4pro-arm64-python-2754e9a615de298b0c3a-3.15.0a8%2B-2754e9a-vs-3.12.6.md)[📈](results/bm-20260427-3.15.0a8%2B-2754e9a-NOGIL/bm-20260427-macm4pro-arm64-python-2754e9a615de298b0c3a-3.15.0a8%2B-2754e9a-vs-3.12.6.svg) | 1.034x ↑<br>[📄](results/bm-20260427-3.15.0a8%2B-2754e9a-NOGIL/bm-20260427-macm4pro-arm64-python-2754e9a615de298b0c3a-3.15.0a8%2B-2754e9a-vs-3.13.0rc2.md)[📈](results/bm-20260427-3.15.0a8%2B-2754e9a-NOGIL/bm-20260427-macm4pro-arm64-python-2754e9a615de298b0c3a-3.15.0a8%2B-2754e9a-vs-3.13.0rc2.svg) | 1.048x ↓<br>[📄](results/bm-20260427-3.15.0a8%2B-2754e9a-NOGIL/bm-20260427-macm4pro-arm64-python-2754e9a615de298b0c3a-3.15.0a8%2B-2754e9a-vs-base.md)[📈](results/bm-20260427-3.15.0a8%2B-2754e9a-NOGIL/bm-20260427-macm4pro-arm64-python-2754e9a615de298b0c3a-3.15.0a8%2B-2754e9a-vs-base.svg)[🧠](results/bm-20260427-3.15.0a8%2B-2754e9a-NOGIL/bm-20260427-macm4pro-arm64-python-2754e9a615de298b0c3a-3.15.0a8%2B-2754e9a-vs-base-mem.svg) |
| [2026-04-27](results/bm-20260427-3.15.0a8%2B-2754e9a) | python/2754e9a615de298b0c3a | 2754e9a | 1.170x ↑<br>[📄](results/bm-20260427-3.15.0a8%2B-2754e9a/bm-20260427-macm4pro-arm64-python-2754e9a615de298b0c3a-3.15.0a8%2B-2754e9a-vs-3.12.6.md)[📈](results/bm-20260427-3.15.0a8%2B-2754e9a/bm-20260427-macm4pro-arm64-python-2754e9a615de298b0c3a-3.15.0a8%2B-2754e9a-vs-3.12.6.svg) | 1.085x ↑<br>[📄](results/bm-20260427-3.15.0a8%2B-2754e9a/bm-20260427-macm4pro-arm64-python-2754e9a615de298b0c3a-3.15.0a8%2B-2754e9a-vs-3.13.0rc2.md)[📈](results/bm-20260427-3.15.0a8%2B-2754e9a/bm-20260427-macm4pro-arm64-python-2754e9a615de298b0c3a-3.15.0a8%2B-2754e9a-vs-3.13.0rc2.svg) |  |


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
