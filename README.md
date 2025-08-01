# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (a852c7b)](results/bm-20250726-3.15.0a0-a852c7b/bm-20250726-vultr-x86_64-python-a852c7bdd48979218a0c-3.15.0a0-a852c7b-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (a852c7b)](results/bm-20250726-3.15.0a0-a852c7b-PYTHON_UOPS/bm-20250726-vultr-x86_64-python-a852c7bdd48979218a0c-3.15.0a0-a852c7b-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-08-01](results/bm-20250801-3.15.0a0-fe0e921-NOGIL) | python/fe0e921817a7f96c62c9 | fe0e921 (NOGIL) | 1.028x ↓<br>[📄](results/bm-20250801-3.15.0a0-fe0e921-NOGIL/bm-20250801-vultr-x86_64-python-fe0e921817a7f96c62c9-3.15.0a0-fe0e921-vs-3.12.6.md)[📈](results/bm-20250801-3.15.0a0-fe0e921-NOGIL/bm-20250801-vultr-x86_64-python-fe0e921817a7f96c62c9-3.15.0a0-fe0e921-vs-3.12.6.svg) | 1.061x ↓<br>[📄](results/bm-20250801-3.15.0a0-fe0e921-NOGIL/bm-20250801-vultr-x86_64-python-fe0e921817a7f96c62c9-3.15.0a0-fe0e921-vs-3.13.0rc2.md)[📈](results/bm-20250801-3.15.0a0-fe0e921-NOGIL/bm-20250801-vultr-x86_64-python-fe0e921817a7f96c62c9-3.15.0a0-fe0e921-vs-3.13.0rc2.svg) | 1.100x ↓<br>[📄](results/bm-20250801-3.15.0a0-fe0e921-NOGIL/bm-20250801-vultr-x86_64-python-fe0e921817a7f96c62c9-3.15.0a0-fe0e921-vs-base.md)[📈](results/bm-20250801-3.15.0a0-fe0e921-NOGIL/bm-20250801-vultr-x86_64-python-fe0e921817a7f96c62c9-3.15.0a0-fe0e921-vs-base.svg)[🧠](results/bm-20250801-3.15.0a0-fe0e921-NOGIL/bm-20250801-vultr-x86_64-python-fe0e921817a7f96c62c9-3.15.0a0-fe0e921-vs-base-mem.svg) |
| [2025-08-01](results/bm-20250801-3.15.0a0-fe0e921) | python/fe0e921817a7f96c62c9 | fe0e921 | 1.074x ↑<br>[📄](results/bm-20250801-3.15.0a0-fe0e921/bm-20250801-vultr-x86_64-python-fe0e921817a7f96c62c9-3.15.0a0-fe0e921-vs-3.12.6.md)[📈](results/bm-20250801-3.15.0a0-fe0e921/bm-20250801-vultr-x86_64-python-fe0e921817a7f96c62c9-3.15.0a0-fe0e921-vs-3.12.6.svg) | 1.038x ↑<br>[📄](results/bm-20250801-3.15.0a0-fe0e921/bm-20250801-vultr-x86_64-python-fe0e921817a7f96c62c9-3.15.0a0-fe0e921-vs-3.13.0rc2.md)[📈](results/bm-20250801-3.15.0a0-fe0e921/bm-20250801-vultr-x86_64-python-fe0e921817a7f96c62c9-3.15.0a0-fe0e921-vs-3.13.0rc2.svg) |  |
| [2025-07-31](results/bm-20250731-3.15.0a0-2a87af0-NOGIL) | python/2a87af062b79d914ce01 | 2a87af0 (NOGIL) | 1.027x ↓<br>[📄](results/bm-20250731-3.15.0a0-2a87af0-NOGIL/bm-20250731-vultr-x86_64-python-2a87af062b79d914ce01-3.15.0a0-2a87af0-vs-3.12.6.md)[📈](results/bm-20250731-3.15.0a0-2a87af0-NOGIL/bm-20250731-vultr-x86_64-python-2a87af062b79d914ce01-3.15.0a0-2a87af0-vs-3.12.6.svg) | 1.060x ↓<br>[📄](results/bm-20250731-3.15.0a0-2a87af0-NOGIL/bm-20250731-vultr-x86_64-python-2a87af062b79d914ce01-3.15.0a0-2a87af0-vs-3.13.0rc2.md)[📈](results/bm-20250731-3.15.0a0-2a87af0-NOGIL/bm-20250731-vultr-x86_64-python-2a87af062b79d914ce01-3.15.0a0-2a87af0-vs-3.13.0rc2.svg) | 1.094x ↓<br>[📄](results/bm-20250731-3.15.0a0-2a87af0-NOGIL/bm-20250731-vultr-x86_64-python-2a87af062b79d914ce01-3.15.0a0-2a87af0-vs-base.md)[📈](results/bm-20250731-3.15.0a0-2a87af0-NOGIL/bm-20250731-vultr-x86_64-python-2a87af062b79d914ce01-3.15.0a0-2a87af0-vs-base.svg)[🧠](results/bm-20250731-3.15.0a0-2a87af0-NOGIL/bm-20250731-vultr-x86_64-python-2a87af062b79d914ce01-3.15.0a0-2a87af0-vs-base-mem.svg) |
| [2025-07-31](results/bm-20250731-3.15.0a0-2a87af0) | python/2a87af062b79d914ce01 | 2a87af0 | 1.067x ↑<br>[📄](results/bm-20250731-3.15.0a0-2a87af0/bm-20250731-vultr-x86_64-python-2a87af062b79d914ce01-3.15.0a0-2a87af0-vs-3.12.6.md)[📈](results/bm-20250731-3.15.0a0-2a87af0/bm-20250731-vultr-x86_64-python-2a87af062b79d914ce01-3.15.0a0-2a87af0-vs-3.12.6.svg) | 1.032x ↑<br>[📄](results/bm-20250731-3.15.0a0-2a87af0/bm-20250731-vultr-x86_64-python-2a87af062b79d914ce01-3.15.0a0-2a87af0-vs-3.13.0rc2.md)[📈](results/bm-20250731-3.15.0a0-2a87af0/bm-20250731-vultr-x86_64-python-2a87af062b79d914ce01-3.15.0a0-2a87af0-vs-3.13.0rc2.svg) |  |
| [2025-07-30](results/bm-20250730-3.15.0a0-d591b5e-NOGIL) | python/d591b5effb8ec8177a95 | d591b5e (NOGIL) | 1.026x ↓<br>[📄](results/bm-20250730-3.15.0a0-d591b5e-NOGIL/bm-20250730-vultr-x86_64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e-vs-3.12.6.md)[📈](results/bm-20250730-3.15.0a0-d591b5e-NOGIL/bm-20250730-vultr-x86_64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e-vs-3.12.6.svg) | 1.059x ↓<br>[📄](results/bm-20250730-3.15.0a0-d591b5e-NOGIL/bm-20250730-vultr-x86_64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e-vs-3.13.0rc2.md)[📈](results/bm-20250730-3.15.0a0-d591b5e-NOGIL/bm-20250730-vultr-x86_64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e-vs-3.13.0rc2.svg) | 1.094x ↓<br>[📄](results/bm-20250730-3.15.0a0-d591b5e-NOGIL/bm-20250730-vultr-x86_64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e-vs-base.md)[📈](results/bm-20250730-3.15.0a0-d591b5e-NOGIL/bm-20250730-vultr-x86_64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e-vs-base.svg)[🧠](results/bm-20250730-3.15.0a0-d591b5e-NOGIL/bm-20250730-vultr-x86_64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e-vs-base-mem.svg) |
| [2025-07-30](results/bm-20250730-3.15.0a0-d591b5e) | python/d591b5effb8ec8177a95 | d591b5e | 1.068x ↑<br>[📄](results/bm-20250730-3.15.0a0-d591b5e/bm-20250730-vultr-x86_64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e-vs-3.12.6.md)[📈](results/bm-20250730-3.15.0a0-d591b5e/bm-20250730-vultr-x86_64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e-vs-3.12.6.svg) | 1.032x ↑<br>[📄](results/bm-20250730-3.15.0a0-d591b5e/bm-20250730-vultr-x86_64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e-vs-3.13.0rc2.md)[📈](results/bm-20250730-3.15.0a0-d591b5e/bm-20250730-vultr-x86_64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e-vs-3.13.0rc2.svg) |  |
| [2025-07-29](results/bm-20250729-3.15.0a0-98d462c-NOGIL) | python/98d462cf4de82d4ef40b | 98d462c (NOGIL) | 1.029x ↓<br>[📄](results/bm-20250729-3.15.0a0-98d462c-NOGIL/bm-20250729-vultr-x86_64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c-vs-3.12.6.md)[📈](results/bm-20250729-3.15.0a0-98d462c-NOGIL/bm-20250729-vultr-x86_64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c-vs-3.12.6.svg) | 1.062x ↓<br>[📄](results/bm-20250729-3.15.0a0-98d462c-NOGIL/bm-20250729-vultr-x86_64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c-vs-3.13.0rc2.md)[📈](results/bm-20250729-3.15.0a0-98d462c-NOGIL/bm-20250729-vultr-x86_64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c-vs-3.13.0rc2.svg) | 1.096x ↓<br>[📄](results/bm-20250729-3.15.0a0-98d462c-NOGIL/bm-20250729-vultr-x86_64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c-vs-base.md)[📈](results/bm-20250729-3.15.0a0-98d462c-NOGIL/bm-20250729-vultr-x86_64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c-vs-base.svg)[🧠](results/bm-20250729-3.15.0a0-98d462c-NOGIL/bm-20250729-vultr-x86_64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c-vs-base-mem.svg) |
| [2025-07-29](results/bm-20250729-3.15.0a0-98d462c) | python/98d462cf4de82d4ef40b | 98d462c | 1.068x ↑<br>[📄](results/bm-20250729-3.15.0a0-98d462c/bm-20250729-vultr-x86_64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c-vs-3.12.6.md)[📈](results/bm-20250729-3.15.0a0-98d462c/bm-20250729-vultr-x86_64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c-vs-3.12.6.svg) | 1.032x ↑<br>[📄](results/bm-20250729-3.15.0a0-98d462c/bm-20250729-vultr-x86_64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c-vs-3.13.0rc2.md)[📈](results/bm-20250729-3.15.0a0-98d462c/bm-20250729-vultr-x86_64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-08-01](results/bm-20250801-3.15.0a0-fe0e921-NOGIL) | python/fe0e921817a7f96c62c9 | fe0e921 (NOGIL) | 1.077x ↑<br>[📄](results/bm-20250801-3.15.0a0-fe0e921-NOGIL/bm-20250801-macm4pro-arm64-python-fe0e921817a7f96c62c9-3.15.0a0-fe0e921-vs-3.12.6.md)[📈](results/bm-20250801-3.15.0a0-fe0e921-NOGIL/bm-20250801-macm4pro-arm64-python-fe0e921817a7f96c62c9-3.15.0a0-fe0e921-vs-3.12.6.svg) | 1.001x ↓<br>[📄](results/bm-20250801-3.15.0a0-fe0e921-NOGIL/bm-20250801-macm4pro-arm64-python-fe0e921817a7f96c62c9-3.15.0a0-fe0e921-vs-3.13.0rc2.md)[📈](results/bm-20250801-3.15.0a0-fe0e921-NOGIL/bm-20250801-macm4pro-arm64-python-fe0e921817a7f96c62c9-3.15.0a0-fe0e921-vs-3.13.0rc2.svg) | 1.020x ↓<br>[📄](results/bm-20250801-3.15.0a0-fe0e921-NOGIL/bm-20250801-macm4pro-arm64-python-fe0e921817a7f96c62c9-3.15.0a0-fe0e921-vs-base.md)[📈](results/bm-20250801-3.15.0a0-fe0e921-NOGIL/bm-20250801-macm4pro-arm64-python-fe0e921817a7f96c62c9-3.15.0a0-fe0e921-vs-base.svg)[🧠](results/bm-20250801-3.15.0a0-fe0e921-NOGIL/bm-20250801-macm4pro-arm64-python-fe0e921817a7f96c62c9-3.15.0a0-fe0e921-vs-base-mem.svg) |
| [2025-08-01](results/bm-20250801-3.15.0a0-fe0e921) | python/fe0e921817a7f96c62c9 | fe0e921 | 1.097x ↑<br>[📄](results/bm-20250801-3.15.0a0-fe0e921/bm-20250801-macm4pro-arm64-python-fe0e921817a7f96c62c9-3.15.0a0-fe0e921-vs-3.12.6.md)[📈](results/bm-20250801-3.15.0a0-fe0e921/bm-20250801-macm4pro-arm64-python-fe0e921817a7f96c62c9-3.15.0a0-fe0e921-vs-3.12.6.svg) | 1.018x ↑<br>[📄](results/bm-20250801-3.15.0a0-fe0e921/bm-20250801-macm4pro-arm64-python-fe0e921817a7f96c62c9-3.15.0a0-fe0e921-vs-3.13.0rc2.md)[📈](results/bm-20250801-3.15.0a0-fe0e921/bm-20250801-macm4pro-arm64-python-fe0e921817a7f96c62c9-3.15.0a0-fe0e921-vs-3.13.0rc2.svg) |  |
| [2025-07-31](results/bm-20250731-3.15.0a0-2a87af0-NOGIL) | python/2a87af062b79d914ce01 | 2a87af0 (NOGIL) | 1.098x ↑<br>[📄](results/bm-20250731-3.15.0a0-2a87af0-NOGIL/bm-20250731-macm4pro-arm64-python-2a87af062b79d914ce01-3.15.0a0-2a87af0-vs-3.12.6.md)[📈](results/bm-20250731-3.15.0a0-2a87af0-NOGIL/bm-20250731-macm4pro-arm64-python-2a87af062b79d914ce01-3.15.0a0-2a87af0-vs-3.12.6.svg) | 1.019x ↑<br>[📄](results/bm-20250731-3.15.0a0-2a87af0-NOGIL/bm-20250731-macm4pro-arm64-python-2a87af062b79d914ce01-3.15.0a0-2a87af0-vs-3.13.0rc2.md)[📈](results/bm-20250731-3.15.0a0-2a87af0-NOGIL/bm-20250731-macm4pro-arm64-python-2a87af062b79d914ce01-3.15.0a0-2a87af0-vs-3.13.0rc2.svg) | 1.000x ↓<br>[📄](results/bm-20250731-3.15.0a0-2a87af0-NOGIL/bm-20250731-macm4pro-arm64-python-2a87af062b79d914ce01-3.15.0a0-2a87af0-vs-base.md)[📈](results/bm-20250731-3.15.0a0-2a87af0-NOGIL/bm-20250731-macm4pro-arm64-python-2a87af062b79d914ce01-3.15.0a0-2a87af0-vs-base.svg)[🧠](results/bm-20250731-3.15.0a0-2a87af0-NOGIL/bm-20250731-macm4pro-arm64-python-2a87af062b79d914ce01-3.15.0a0-2a87af0-vs-base-mem.svg) |
| [2025-07-31](results/bm-20250731-3.15.0a0-2a87af0) | python/2a87af062b79d914ce01 | 2a87af0 | 1.097x ↑<br>[📄](results/bm-20250731-3.15.0a0-2a87af0/bm-20250731-macm4pro-arm64-python-2a87af062b79d914ce01-3.15.0a0-2a87af0-vs-3.12.6.md)[📈](results/bm-20250731-3.15.0a0-2a87af0/bm-20250731-macm4pro-arm64-python-2a87af062b79d914ce01-3.15.0a0-2a87af0-vs-3.12.6.svg) | 1.018x ↑<br>[📄](results/bm-20250731-3.15.0a0-2a87af0/bm-20250731-macm4pro-arm64-python-2a87af062b79d914ce01-3.15.0a0-2a87af0-vs-3.13.0rc2.md)[📈](results/bm-20250731-3.15.0a0-2a87af0/bm-20250731-macm4pro-arm64-python-2a87af062b79d914ce01-3.15.0a0-2a87af0-vs-3.13.0rc2.svg) |  |
| [2025-07-30](results/bm-20250730-3.15.0a0-d591b5e-NOGIL) | python/d591b5effb8ec8177a95 | d591b5e (NOGIL) | 1.085x ↑<br>[📄](results/bm-20250730-3.15.0a0-d591b5e-NOGIL/bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e-vs-3.12.6.md)[📈](results/bm-20250730-3.15.0a0-d591b5e-NOGIL/bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e-vs-3.12.6.svg) | 1.007x ↑<br>[📄](results/bm-20250730-3.15.0a0-d591b5e-NOGIL/bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e-vs-3.13.0rc2.md)[📈](results/bm-20250730-3.15.0a0-d591b5e-NOGIL/bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e-vs-3.13.0rc2.svg) | 1.017x ↓<br>[📄](results/bm-20250730-3.15.0a0-d591b5e-NOGIL/bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e-vs-base.md)[📈](results/bm-20250730-3.15.0a0-d591b5e-NOGIL/bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e-vs-base.svg)[🧠](results/bm-20250730-3.15.0a0-d591b5e-NOGIL/bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e-vs-base-mem.svg) |
| [2025-07-30](results/bm-20250730-3.15.0a0-d591b5e) | python/d591b5effb8ec8177a95 | d591b5e | 1.102x ↑<br>[📄](results/bm-20250730-3.15.0a0-d591b5e/bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e-vs-3.12.6.md)[📈](results/bm-20250730-3.15.0a0-d591b5e/bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e-vs-3.12.6.svg) | 1.022x ↑<br>[📄](results/bm-20250730-3.15.0a0-d591b5e/bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e-vs-3.13.0rc2.md)[📈](results/bm-20250730-3.15.0a0-d591b5e/bm-20250730-macm4pro-arm64-python-d591b5effb8ec8177a95-3.15.0a0-d591b5e-vs-3.13.0rc2.svg) |  |
| [2025-07-29](results/bm-20250729-3.15.0a0-98d462c-NOGIL) | python/98d462cf4de82d4ef40b | 98d462c (NOGIL) | 1.084x ↑<br>[📄](results/bm-20250729-3.15.0a0-98d462c-NOGIL/bm-20250729-macm4pro-arm64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c-vs-3.12.6.md)[📈](results/bm-20250729-3.15.0a0-98d462c-NOGIL/bm-20250729-macm4pro-arm64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c-vs-3.12.6.svg) | 1.005x ↑<br>[📄](results/bm-20250729-3.15.0a0-98d462c-NOGIL/bm-20250729-macm4pro-arm64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c-vs-3.13.0rc2.md)[📈](results/bm-20250729-3.15.0a0-98d462c-NOGIL/bm-20250729-macm4pro-arm64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c-vs-3.13.0rc2.svg) | 1.010x ↓<br>[📄](results/bm-20250729-3.15.0a0-98d462c-NOGIL/bm-20250729-macm4pro-arm64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c-vs-base.md)[📈](results/bm-20250729-3.15.0a0-98d462c-NOGIL/bm-20250729-macm4pro-arm64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c-vs-base.svg)[🧠](results/bm-20250729-3.15.0a0-98d462c-NOGIL/bm-20250729-macm4pro-arm64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c-vs-base-mem.svg) |
| [2025-07-29](results/bm-20250729-3.15.0a0-98d462c) | python/98d462cf4de82d4ef40b | 98d462c | 1.094x ↑<br>[📄](results/bm-20250729-3.15.0a0-98d462c/bm-20250729-macm4pro-arm64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c-vs-3.12.6.md)[📈](results/bm-20250729-3.15.0a0-98d462c/bm-20250729-macm4pro-arm64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c-vs-3.12.6.svg) | 1.015x ↑<br>[📄](results/bm-20250729-3.15.0a0-98d462c/bm-20250729-macm4pro-arm64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c-vs-3.13.0rc2.md)[📈](results/bm-20250729-3.15.0a0-98d462c/bm-20250729-macm4pro-arm64-python-98d462cf4de82d4ef40b-3.15.0a0-98d462c-vs-3.13.0rc2.svg) |  |


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
