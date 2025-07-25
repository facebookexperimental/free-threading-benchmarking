# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (800d37f)](results/bm-20250719-3.15.0a0-800d37f/bm-20250719-vultr-x86_64-python-800d37feca2e0ea33439-3.15.0a0-800d37f-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (800d37f)](results/bm-20250719-3.15.0a0-800d37f-PYTHON_UOPS/bm-20250719-vultr-x86_64-python-800d37feca2e0ea33439-3.15.0a0-800d37f-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-07-25](results/bm-20250725-3.15.0a0-1e69cd1-NOGIL) | python/1e69cd1634e4f0f8c375 | 1e69cd1 (NOGIL) | 1.032x ↓<br>[📄](results/bm-20250725-3.15.0a0-1e69cd1-NOGIL/bm-20250725-vultr-x86_64-python-1e69cd1634e4f0f8c375-3.15.0a0-1e69cd1-vs-3.12.6.md)[📈](results/bm-20250725-3.15.0a0-1e69cd1-NOGIL/bm-20250725-vultr-x86_64-python-1e69cd1634e4f0f8c375-3.15.0a0-1e69cd1-vs-3.12.6.svg) | 1.064x ↓<br>[📄](results/bm-20250725-3.15.0a0-1e69cd1-NOGIL/bm-20250725-vultr-x86_64-python-1e69cd1634e4f0f8c375-3.15.0a0-1e69cd1-vs-3.13.0rc2.md)[📈](results/bm-20250725-3.15.0a0-1e69cd1-NOGIL/bm-20250725-vultr-x86_64-python-1e69cd1634e4f0f8c375-3.15.0a0-1e69cd1-vs-3.13.0rc2.svg) | 1.098x ↓<br>[📄](results/bm-20250725-3.15.0a0-1e69cd1-NOGIL/bm-20250725-vultr-x86_64-python-1e69cd1634e4f0f8c375-3.15.0a0-1e69cd1-vs-base.md)[📈](results/bm-20250725-3.15.0a0-1e69cd1-NOGIL/bm-20250725-vultr-x86_64-python-1e69cd1634e4f0f8c375-3.15.0a0-1e69cd1-vs-base.svg)[🧠](results/bm-20250725-3.15.0a0-1e69cd1-NOGIL/bm-20250725-vultr-x86_64-python-1e69cd1634e4f0f8c375-3.15.0a0-1e69cd1-vs-base-mem.svg) |
| [2025-07-25](results/bm-20250725-3.15.0a0-1e69cd1) | python/1e69cd1634e4f0f8c375 | 1e69cd1 | 1.068x ↑<br>[📄](results/bm-20250725-3.15.0a0-1e69cd1/bm-20250725-vultr-x86_64-python-1e69cd1634e4f0f8c375-3.15.0a0-1e69cd1-vs-3.12.6.md)[📈](results/bm-20250725-3.15.0a0-1e69cd1/bm-20250725-vultr-x86_64-python-1e69cd1634e4f0f8c375-3.15.0a0-1e69cd1-vs-3.12.6.svg) | 1.032x ↑<br>[📄](results/bm-20250725-3.15.0a0-1e69cd1/bm-20250725-vultr-x86_64-python-1e69cd1634e4f0f8c375-3.15.0a0-1e69cd1-vs-3.13.0rc2.md)[📈](results/bm-20250725-3.15.0a0-1e69cd1/bm-20250725-vultr-x86_64-python-1e69cd1634e4f0f8c375-3.15.0a0-1e69cd1-vs-3.13.0rc2.svg) |  |
| [2025-07-24](results/bm-20250724-3.15.0a0-d5e75c0-NOGIL) | python/d5e75c07682864e9d265 | d5e75c0 (NOGIL) | 1.029x ↓<br>[📄](results/bm-20250724-3.15.0a0-d5e75c0-NOGIL/bm-20250724-vultr-x86_64-python-d5e75c07682864e9d265-3.15.0a0-d5e75c0-vs-3.12.6.md)[📈](results/bm-20250724-3.15.0a0-d5e75c0-NOGIL/bm-20250724-vultr-x86_64-python-d5e75c07682864e9d265-3.15.0a0-d5e75c0-vs-3.12.6.svg) | 1.061x ↓<br>[📄](results/bm-20250724-3.15.0a0-d5e75c0-NOGIL/bm-20250724-vultr-x86_64-python-d5e75c07682864e9d265-3.15.0a0-d5e75c0-vs-3.13.0rc2.md)[📈](results/bm-20250724-3.15.0a0-d5e75c0-NOGIL/bm-20250724-vultr-x86_64-python-d5e75c07682864e9d265-3.15.0a0-d5e75c0-vs-3.13.0rc2.svg) | 1.091x ↓<br>[📄](results/bm-20250724-3.15.0a0-d5e75c0-NOGIL/bm-20250724-vultr-x86_64-python-d5e75c07682864e9d265-3.15.0a0-d5e75c0-vs-base.md)[📈](results/bm-20250724-3.15.0a0-d5e75c0-NOGIL/bm-20250724-vultr-x86_64-python-d5e75c07682864e9d265-3.15.0a0-d5e75c0-vs-base.svg)[🧠](results/bm-20250724-3.15.0a0-d5e75c0-NOGIL/bm-20250724-vultr-x86_64-python-d5e75c07682864e9d265-3.15.0a0-d5e75c0-vs-base-mem.svg) |
| [2025-07-24](results/bm-20250724-3.15.0a0-d5e75c0) | python/d5e75c07682864e9d265 | d5e75c0 | 1.062x ↑<br>[📄](results/bm-20250724-3.15.0a0-d5e75c0/bm-20250724-vultr-x86_64-python-d5e75c07682864e9d265-3.15.0a0-d5e75c0-vs-3.12.6.md)[📈](results/bm-20250724-3.15.0a0-d5e75c0/bm-20250724-vultr-x86_64-python-d5e75c07682864e9d265-3.15.0a0-d5e75c0-vs-3.12.6.svg) | 1.027x ↑<br>[📄](results/bm-20250724-3.15.0a0-d5e75c0/bm-20250724-vultr-x86_64-python-d5e75c07682864e9d265-3.15.0a0-d5e75c0-vs-3.13.0rc2.md)[📈](results/bm-20250724-3.15.0a0-d5e75c0/bm-20250724-vultr-x86_64-python-d5e75c07682864e9d265-3.15.0a0-d5e75c0-vs-3.13.0rc2.svg) |  |
| [2025-07-23](results/bm-20250723-3.15.0a0-ec7fad7-NOGIL) | python/ec7fad79d24e79961b86 | ec7fad7 (NOGIL) | 1.028x ↓<br>[📄](results/bm-20250723-3.15.0a0-ec7fad7-NOGIL/bm-20250723-vultr-x86_64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7-vs-3.12.6.md)[📈](results/bm-20250723-3.15.0a0-ec7fad7-NOGIL/bm-20250723-vultr-x86_64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7-vs-3.12.6.svg) | 1.060x ↓<br>[📄](results/bm-20250723-3.15.0a0-ec7fad7-NOGIL/bm-20250723-vultr-x86_64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7-vs-3.13.0rc2.md)[📈](results/bm-20250723-3.15.0a0-ec7fad7-NOGIL/bm-20250723-vultr-x86_64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7-vs-3.13.0rc2.svg) | 1.098x ↓<br>[📄](results/bm-20250723-3.15.0a0-ec7fad7-NOGIL/bm-20250723-vultr-x86_64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7-vs-base.md)[📈](results/bm-20250723-3.15.0a0-ec7fad7-NOGIL/bm-20250723-vultr-x86_64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7-vs-base.svg)[🧠](results/bm-20250723-3.15.0a0-ec7fad7-NOGIL/bm-20250723-vultr-x86_64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7-vs-base-mem.svg) |
| [2025-07-23](results/bm-20250723-3.15.0a0-ec7fad7) | python/ec7fad79d24e79961b86 | ec7fad7 | 1.072x ↑<br>[📄](results/bm-20250723-3.15.0a0-ec7fad7/bm-20250723-vultr-x86_64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7-vs-3.12.6.md)[📈](results/bm-20250723-3.15.0a0-ec7fad7/bm-20250723-vultr-x86_64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7-vs-3.12.6.svg) | 1.036x ↑<br>[📄](results/bm-20250723-3.15.0a0-ec7fad7/bm-20250723-vultr-x86_64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7-vs-3.13.0rc2.md)[📈](results/bm-20250723-3.15.0a0-ec7fad7/bm-20250723-vultr-x86_64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7-vs-3.13.0rc2.svg) |  |
| [2025-07-22](results/bm-20250722-3.15.0a0-b13a5df-NOGIL) | python/b13a5df52fc854d1097e | b13a5df (NOGIL) | 1.028x ↓<br>[📄](results/bm-20250722-3.15.0a0-b13a5df-NOGIL/bm-20250722-vultr-x86_64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df-vs-3.12.6.md)[📈](results/bm-20250722-3.15.0a0-b13a5df-NOGIL/bm-20250722-vultr-x86_64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df-vs-3.12.6.svg) | 1.060x ↓<br>[📄](results/bm-20250722-3.15.0a0-b13a5df-NOGIL/bm-20250722-vultr-x86_64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df-vs-3.13.0rc2.md)[📈](results/bm-20250722-3.15.0a0-b13a5df-NOGIL/bm-20250722-vultr-x86_64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df-vs-3.13.0rc2.svg) | 1.097x ↓<br>[📄](results/bm-20250722-3.15.0a0-b13a5df-NOGIL/bm-20250722-vultr-x86_64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df-vs-base.md)[📈](results/bm-20250722-3.15.0a0-b13a5df-NOGIL/bm-20250722-vultr-x86_64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df-vs-base.svg)[🧠](results/bm-20250722-3.15.0a0-b13a5df-NOGIL/bm-20250722-vultr-x86_64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df-vs-base-mem.svg) |
| [2025-07-22](results/bm-20250722-3.15.0a0-b13a5df) | python/b13a5df52fc854d1097e | b13a5df | 1.070x ↑<br>[📄](results/bm-20250722-3.15.0a0-b13a5df/bm-20250722-vultr-x86_64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df-vs-3.12.6.md)[📈](results/bm-20250722-3.15.0a0-b13a5df/bm-20250722-vultr-x86_64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df-vs-3.12.6.svg) | 1.034x ↑<br>[📄](results/bm-20250722-3.15.0a0-b13a5df/bm-20250722-vultr-x86_64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df-vs-3.13.0rc2.md)[📈](results/bm-20250722-3.15.0a0-b13a5df/bm-20250722-vultr-x86_64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-07-25](results/bm-20250725-3.15.0a0-1e69cd1-NOGIL) | python/1e69cd1634e4f0f8c375 | 1e69cd1 (NOGIL) | 1.087x ↑<br>[📄](results/bm-20250725-3.15.0a0-1e69cd1-NOGIL/bm-20250725-macm4pro-arm64-python-1e69cd1634e4f0f8c375-3.15.0a0-1e69cd1-vs-3.12.6.md)[📈](results/bm-20250725-3.15.0a0-1e69cd1-NOGIL/bm-20250725-macm4pro-arm64-python-1e69cd1634e4f0f8c375-3.15.0a0-1e69cd1-vs-3.12.6.svg) | 1.008x ↑<br>[📄](results/bm-20250725-3.15.0a0-1e69cd1-NOGIL/bm-20250725-macm4pro-arm64-python-1e69cd1634e4f0f8c375-3.15.0a0-1e69cd1-vs-3.13.0rc2.md)[📈](results/bm-20250725-3.15.0a0-1e69cd1-NOGIL/bm-20250725-macm4pro-arm64-python-1e69cd1634e4f0f8c375-3.15.0a0-1e69cd1-vs-3.13.0rc2.svg) | 1.004x ↓<br>[📄](results/bm-20250725-3.15.0a0-1e69cd1-NOGIL/bm-20250725-macm4pro-arm64-python-1e69cd1634e4f0f8c375-3.15.0a0-1e69cd1-vs-base.md)[📈](results/bm-20250725-3.15.0a0-1e69cd1-NOGIL/bm-20250725-macm4pro-arm64-python-1e69cd1634e4f0f8c375-3.15.0a0-1e69cd1-vs-base.svg)[🧠](results/bm-20250725-3.15.0a0-1e69cd1-NOGIL/bm-20250725-macm4pro-arm64-python-1e69cd1634e4f0f8c375-3.15.0a0-1e69cd1-vs-base-mem.svg) |
| [2025-07-25](results/bm-20250725-3.15.0a0-1e69cd1) | python/1e69cd1634e4f0f8c375 | 1e69cd1 | 1.090x ↑<br>[📄](results/bm-20250725-3.15.0a0-1e69cd1/bm-20250725-macm4pro-arm64-python-1e69cd1634e4f0f8c375-3.15.0a0-1e69cd1-vs-3.12.6.md)[📈](results/bm-20250725-3.15.0a0-1e69cd1/bm-20250725-macm4pro-arm64-python-1e69cd1634e4f0f8c375-3.15.0a0-1e69cd1-vs-3.12.6.svg) | 1.011x ↑<br>[📄](results/bm-20250725-3.15.0a0-1e69cd1/bm-20250725-macm4pro-arm64-python-1e69cd1634e4f0f8c375-3.15.0a0-1e69cd1-vs-3.13.0rc2.md)[📈](results/bm-20250725-3.15.0a0-1e69cd1/bm-20250725-macm4pro-arm64-python-1e69cd1634e4f0f8c375-3.15.0a0-1e69cd1-vs-3.13.0rc2.svg) |  |
| [2025-07-24](results/bm-20250724-3.15.0a0-d5e75c0-NOGIL) | python/d5e75c07682864e9d265 | d5e75c0 (NOGIL) | 1.087x ↑<br>[📄](results/bm-20250724-3.15.0a0-d5e75c0-NOGIL/bm-20250724-macm4pro-arm64-python-d5e75c07682864e9d265-3.15.0a0-d5e75c0-vs-3.12.6.md)[📈](results/bm-20250724-3.15.0a0-d5e75c0-NOGIL/bm-20250724-macm4pro-arm64-python-d5e75c07682864e9d265-3.15.0a0-d5e75c0-vs-3.12.6.svg) | 1.008x ↑<br>[📄](results/bm-20250724-3.15.0a0-d5e75c0-NOGIL/bm-20250724-macm4pro-arm64-python-d5e75c07682864e9d265-3.15.0a0-d5e75c0-vs-3.13.0rc2.md)[📈](results/bm-20250724-3.15.0a0-d5e75c0-NOGIL/bm-20250724-macm4pro-arm64-python-d5e75c07682864e9d265-3.15.0a0-d5e75c0-vs-3.13.0rc2.svg) | 1.007x ↓<br>[📄](results/bm-20250724-3.15.0a0-d5e75c0-NOGIL/bm-20250724-macm4pro-arm64-python-d5e75c07682864e9d265-3.15.0a0-d5e75c0-vs-base.md)[📈](results/bm-20250724-3.15.0a0-d5e75c0-NOGIL/bm-20250724-macm4pro-arm64-python-d5e75c07682864e9d265-3.15.0a0-d5e75c0-vs-base.svg)[🧠](results/bm-20250724-3.15.0a0-d5e75c0-NOGIL/bm-20250724-macm4pro-arm64-python-d5e75c07682864e9d265-3.15.0a0-d5e75c0-vs-base-mem.svg) |
| [2025-07-24](results/bm-20250724-3.15.0a0-d5e75c0) | python/d5e75c07682864e9d265 | d5e75c0 | 1.093x ↑<br>[📄](results/bm-20250724-3.15.0a0-d5e75c0/bm-20250724-macm4pro-arm64-python-d5e75c07682864e9d265-3.15.0a0-d5e75c0-vs-3.12.6.md)[📈](results/bm-20250724-3.15.0a0-d5e75c0/bm-20250724-macm4pro-arm64-python-d5e75c07682864e9d265-3.15.0a0-d5e75c0-vs-3.12.6.svg) | 1.014x ↑<br>[📄](results/bm-20250724-3.15.0a0-d5e75c0/bm-20250724-macm4pro-arm64-python-d5e75c07682864e9d265-3.15.0a0-d5e75c0-vs-3.13.0rc2.md)[📈](results/bm-20250724-3.15.0a0-d5e75c0/bm-20250724-macm4pro-arm64-python-d5e75c07682864e9d265-3.15.0a0-d5e75c0-vs-3.13.0rc2.svg) |  |
| [2025-07-23](results/bm-20250723-3.15.0a0-ec7fad7-NOGIL) | python/ec7fad79d24e79961b86 | ec7fad7 (NOGIL) | 1.090x ↑<br>[📄](results/bm-20250723-3.15.0a0-ec7fad7-NOGIL/bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7-vs-3.12.6.md)[📈](results/bm-20250723-3.15.0a0-ec7fad7-NOGIL/bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7-vs-3.12.6.svg) | 1.011x ↑<br>[📄](results/bm-20250723-3.15.0a0-ec7fad7-NOGIL/bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7-vs-3.13.0rc2.md)[📈](results/bm-20250723-3.15.0a0-ec7fad7-NOGIL/bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7-vs-3.13.0rc2.svg) | 1.001x ↓<br>[📄](results/bm-20250723-3.15.0a0-ec7fad7-NOGIL/bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7-vs-base.md)[📈](results/bm-20250723-3.15.0a0-ec7fad7-NOGIL/bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7-vs-base.svg)[🧠](results/bm-20250723-3.15.0a0-ec7fad7-NOGIL/bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7-vs-base-mem.svg) |
| [2025-07-23](results/bm-20250723-3.15.0a0-ec7fad7) | python/ec7fad79d24e79961b86 | ec7fad7 | 1.090x ↑<br>[📄](results/bm-20250723-3.15.0a0-ec7fad7/bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7-vs-3.12.6.md)[📈](results/bm-20250723-3.15.0a0-ec7fad7/bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7-vs-3.12.6.svg) | 1.011x ↑<br>[📄](results/bm-20250723-3.15.0a0-ec7fad7/bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7-vs-3.13.0rc2.md)[📈](results/bm-20250723-3.15.0a0-ec7fad7/bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7-vs-3.13.0rc2.svg) |  |
| [2025-07-22](results/bm-20250722-3.15.0a0-b13a5df-NOGIL) | python/b13a5df52fc854d1097e | b13a5df (NOGIL) | 1.088x ↑<br>[📄](results/bm-20250722-3.15.0a0-b13a5df-NOGIL/bm-20250722-macm4pro-arm64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df-vs-3.12.6.md)[📈](results/bm-20250722-3.15.0a0-b13a5df-NOGIL/bm-20250722-macm4pro-arm64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df-vs-3.12.6.svg) | 1.009x ↑<br>[📄](results/bm-20250722-3.15.0a0-b13a5df-NOGIL/bm-20250722-macm4pro-arm64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df-vs-3.13.0rc2.md)[📈](results/bm-20250722-3.15.0a0-b13a5df-NOGIL/bm-20250722-macm4pro-arm64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df-vs-3.13.0rc2.svg) | 1.002x ↓<br>[📄](results/bm-20250722-3.15.0a0-b13a5df-NOGIL/bm-20250722-macm4pro-arm64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df-vs-base.md)[📈](results/bm-20250722-3.15.0a0-b13a5df-NOGIL/bm-20250722-macm4pro-arm64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df-vs-base.svg)[🧠](results/bm-20250722-3.15.0a0-b13a5df-NOGIL/bm-20250722-macm4pro-arm64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df-vs-base-mem.svg) |
| [2025-07-22](results/bm-20250722-3.15.0a0-b13a5df) | python/b13a5df52fc854d1097e | b13a5df | 1.088x ↑<br>[📄](results/bm-20250722-3.15.0a0-b13a5df/bm-20250722-macm4pro-arm64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df-vs-3.12.6.md)[📈](results/bm-20250722-3.15.0a0-b13a5df/bm-20250722-macm4pro-arm64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df-vs-3.12.6.svg) | 1.009x ↑<br>[📄](results/bm-20250722-3.15.0a0-b13a5df/bm-20250722-macm4pro-arm64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df-vs-3.13.0rc2.md)[📈](results/bm-20250722-3.15.0a0-b13a5df/bm-20250722-macm4pro-arm64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df-vs-3.13.0rc2.svg) |  |


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
