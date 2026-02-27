# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (2be2dd5)](results/bm-20260221-3.15.0a6%2B-2be2dd5/bm-20260221-vultr-x86_64-python-2be2dd5fc219a5c252d7-3.15.0a6%2B-2be2dd5-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (2be2dd5)](results/bm-20260221-3.15.0a6%2B-2be2dd5-PYTHON_UOPS/bm-20260221-vultr-x86_64-python-2be2dd5fc219a5c252d7-3.15.0a6%2B-2be2dd5-pystats.md)
- [Most recent JIT pystats on main (bedaea0)](results/bm-20251019-3.15.0a1%2B-bedaea0-JIT/bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-02-26](results/bm-20260226-3.15.0a6%2B-06b0920-NOGIL) | python/06b0920f1292690a22ab | 06b0920 (NOGIL) | 1.035x ↓<br>[📄](results/bm-20260226-3.15.0a6%2B-06b0920-NOGIL/bm-20260226-vultr-x86_64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-3.12.6.md)[📈](results/bm-20260226-3.15.0a6%2B-06b0920-NOGIL/bm-20260226-vultr-x86_64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-3.12.6.svg) | 1.068x ↓<br>[📄](results/bm-20260226-3.15.0a6%2B-06b0920-NOGIL/bm-20260226-vultr-x86_64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-3.13.0rc2.md)[📈](results/bm-20260226-3.15.0a6%2B-06b0920-NOGIL/bm-20260226-vultr-x86_64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-3.13.0rc2.svg) | 1.106x ↓<br>[📄](results/bm-20260226-3.15.0a6%2B-06b0920-NOGIL/bm-20260226-vultr-x86_64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-base.md)[📈](results/bm-20260226-3.15.0a6%2B-06b0920-NOGIL/bm-20260226-vultr-x86_64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-base.svg)[🧠](results/bm-20260226-3.15.0a6%2B-06b0920-NOGIL/bm-20260226-vultr-x86_64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-base-mem.svg) |
| [2026-02-26](results/bm-20260226-3.15.0a6%2B-06b0920) | python/06b0920f1292690a22ab | 06b0920 | 1.074x ↑<br>[📄](results/bm-20260226-3.15.0a6%2B-06b0920/bm-20260226-vultr-x86_64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-3.12.6.md)[📈](results/bm-20260226-3.15.0a6%2B-06b0920/bm-20260226-vultr-x86_64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-3.12.6.svg) | 1.038x ↑<br>[📄](results/bm-20260226-3.15.0a6%2B-06b0920/bm-20260226-vultr-x86_64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-3.13.0rc2.md)[📈](results/bm-20260226-3.15.0a6%2B-06b0920/bm-20260226-vultr-x86_64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-3.13.0rc2.svg) |  |
| [2026-02-26](results/bm-20260226-3.15.0a6%2B-43fdb70-NOGIL) | python/43fdb7037e76c18d9545 | 43fdb70 (NOGIL) | 1.027x ↓<br>[📄](results/bm-20260226-3.15.0a6%2B-43fdb70-NOGIL/bm-20260226-vultr-x86_64-python-43fdb7037e76c18d9545-3.15.0a6%2B-43fdb70-vs-3.12.6.md)[📈](results/bm-20260226-3.15.0a6%2B-43fdb70-NOGIL/bm-20260226-vultr-x86_64-python-43fdb7037e76c18d9545-3.15.0a6%2B-43fdb70-vs-3.12.6.svg) | 1.059x ↓<br>[📄](results/bm-20260226-3.15.0a6%2B-43fdb70-NOGIL/bm-20260226-vultr-x86_64-python-43fdb7037e76c18d9545-3.15.0a6%2B-43fdb70-vs-3.13.0rc2.md)[📈](results/bm-20260226-3.15.0a6%2B-43fdb70-NOGIL/bm-20260226-vultr-x86_64-python-43fdb7037e76c18d9545-3.15.0a6%2B-43fdb70-vs-3.13.0rc2.svg) | 1.095x ↓<br>[📄](results/bm-20260226-3.15.0a6%2B-43fdb70-NOGIL/bm-20260226-vultr-x86_64-python-43fdb7037e76c18d9545-3.15.0a6%2B-43fdb70-vs-base.md)[📈](results/bm-20260226-3.15.0a6%2B-43fdb70-NOGIL/bm-20260226-vultr-x86_64-python-43fdb7037e76c18d9545-3.15.0a6%2B-43fdb70-vs-base.svg)[🧠](results/bm-20260226-3.15.0a6%2B-43fdb70-NOGIL/bm-20260226-vultr-x86_64-python-43fdb7037e76c18d9545-3.15.0a6%2B-43fdb70-vs-base-mem.svg) |
| [2026-02-26](results/bm-20260226-3.15.0a6%2B-43fdb70) | python/43fdb7037e76c18d9545 | 43fdb70 | 1.070x ↑<br>[📄](results/bm-20260226-3.15.0a6%2B-43fdb70/bm-20260226-vultr-x86_64-python-43fdb7037e76c18d9545-3.15.0a6%2B-43fdb70-vs-3.12.6.md)[📈](results/bm-20260226-3.15.0a6%2B-43fdb70/bm-20260226-vultr-x86_64-python-43fdb7037e76c18d9545-3.15.0a6%2B-43fdb70-vs-3.12.6.svg) | 1.034x ↑<br>[📄](results/bm-20260226-3.15.0a6%2B-43fdb70/bm-20260226-vultr-x86_64-python-43fdb7037e76c18d9545-3.15.0a6%2B-43fdb70-vs-3.13.0rc2.md)[📈](results/bm-20260226-3.15.0a6%2B-43fdb70/bm-20260226-vultr-x86_64-python-43fdb7037e76c18d9545-3.15.0a6%2B-43fdb70-vs-3.13.0rc2.svg) |  |
| [2026-02-24](results/bm-20260224-3.15.0a6%2B-4e45c9c-NOGIL) | python/4e45c9c309abb12c6223 | 4e45c9c (NOGIL) | 1.029x ↓<br>[📄](results/bm-20260224-3.15.0a6%2B-4e45c9c-NOGIL/bm-20260224-vultr-x86_64-python-4e45c9c309abb12c6223-3.15.0a6%2B-4e45c9c-vs-3.12.6.md)[📈](results/bm-20260224-3.15.0a6%2B-4e45c9c-NOGIL/bm-20260224-vultr-x86_64-python-4e45c9c309abb12c6223-3.15.0a6%2B-4e45c9c-vs-3.12.6.svg) | 1.061x ↓<br>[📄](results/bm-20260224-3.15.0a6%2B-4e45c9c-NOGIL/bm-20260224-vultr-x86_64-python-4e45c9c309abb12c6223-3.15.0a6%2B-4e45c9c-vs-3.13.0rc2.md)[📈](results/bm-20260224-3.15.0a6%2B-4e45c9c-NOGIL/bm-20260224-vultr-x86_64-python-4e45c9c309abb12c6223-3.15.0a6%2B-4e45c9c-vs-3.13.0rc2.svg) | 1.103x ↓<br>[📄](results/bm-20260224-3.15.0a6%2B-4e45c9c-NOGIL/bm-20260224-vultr-x86_64-python-4e45c9c309abb12c6223-3.15.0a6%2B-4e45c9c-vs-base.md)[📈](results/bm-20260224-3.15.0a6%2B-4e45c9c-NOGIL/bm-20260224-vultr-x86_64-python-4e45c9c309abb12c6223-3.15.0a6%2B-4e45c9c-vs-base.svg)[🧠](results/bm-20260224-3.15.0a6%2B-4e45c9c-NOGIL/bm-20260224-vultr-x86_64-python-4e45c9c309abb12c6223-3.15.0a6%2B-4e45c9c-vs-base-mem.svg) |
| [2026-02-24](results/bm-20260224-3.15.0a6%2B-4e45c9c) | python/4e45c9c309abb12c6223 | 4e45c9c | 1.078x ↑<br>[📄](results/bm-20260224-3.15.0a6%2B-4e45c9c/bm-20260224-vultr-x86_64-python-4e45c9c309abb12c6223-3.15.0a6%2B-4e45c9c-vs-3.12.6.md)[📈](results/bm-20260224-3.15.0a6%2B-4e45c9c/bm-20260224-vultr-x86_64-python-4e45c9c309abb12c6223-3.15.0a6%2B-4e45c9c-vs-3.12.6.svg) | 1.042x ↑<br>[📄](results/bm-20260224-3.15.0a6%2B-4e45c9c/bm-20260224-vultr-x86_64-python-4e45c9c309abb12c6223-3.15.0a6%2B-4e45c9c-vs-3.13.0rc2.md)[📈](results/bm-20260224-3.15.0a6%2B-4e45c9c/bm-20260224-vultr-x86_64-python-4e45c9c309abb12c6223-3.15.0a6%2B-4e45c9c-vs-3.13.0rc2.svg) |  |
| [2026-02-23](results/bm-20260223-3.15.0a6%2B-ae7fc4a-NOGIL) | python/ae7fc4a4f6b711173bb7 | ae7fc4a (NOGIL) | 1.033x ↓<br>[📄](results/bm-20260223-3.15.0a6%2B-ae7fc4a-NOGIL/bm-20260223-vultr-x86_64-python-ae7fc4a4f6b711173bb7-3.15.0a6%2B-ae7fc4a-vs-3.12.6.md)[📈](results/bm-20260223-3.15.0a6%2B-ae7fc4a-NOGIL/bm-20260223-vultr-x86_64-python-ae7fc4a4f6b711173bb7-3.15.0a6%2B-ae7fc4a-vs-3.12.6.svg) | 1.065x ↓<br>[📄](results/bm-20260223-3.15.0a6%2B-ae7fc4a-NOGIL/bm-20260223-vultr-x86_64-python-ae7fc4a4f6b711173bb7-3.15.0a6%2B-ae7fc4a-vs-3.13.0rc2.md)[📈](results/bm-20260223-3.15.0a6%2B-ae7fc4a-NOGIL/bm-20260223-vultr-x86_64-python-ae7fc4a4f6b711173bb7-3.15.0a6%2B-ae7fc4a-vs-3.13.0rc2.svg) | 1.105x ↓<br>[📄](results/bm-20260223-3.15.0a6%2B-ae7fc4a-NOGIL/bm-20260223-vultr-x86_64-python-ae7fc4a4f6b711173bb7-3.15.0a6%2B-ae7fc4a-vs-base.md)[📈](results/bm-20260223-3.15.0a6%2B-ae7fc4a-NOGIL/bm-20260223-vultr-x86_64-python-ae7fc4a4f6b711173bb7-3.15.0a6%2B-ae7fc4a-vs-base.svg)[🧠](results/bm-20260223-3.15.0a6%2B-ae7fc4a-NOGIL/bm-20260223-vultr-x86_64-python-ae7fc4a4f6b711173bb7-3.15.0a6%2B-ae7fc4a-vs-base-mem.svg) |
| [2026-02-23](results/bm-20260223-3.15.0a6%2B-ae7fc4a) | python/ae7fc4a4f6b711173bb7 | ae7fc4a | 1.076x ↑<br>[📄](results/bm-20260223-3.15.0a6%2B-ae7fc4a/bm-20260223-vultr-x86_64-python-ae7fc4a4f6b711173bb7-3.15.0a6%2B-ae7fc4a-vs-3.12.6.md)[📈](results/bm-20260223-3.15.0a6%2B-ae7fc4a/bm-20260223-vultr-x86_64-python-ae7fc4a4f6b711173bb7-3.15.0a6%2B-ae7fc4a-vs-3.12.6.svg) | 1.040x ↑<br>[📄](results/bm-20260223-3.15.0a6%2B-ae7fc4a/bm-20260223-vultr-x86_64-python-ae7fc4a4f6b711173bb7-3.15.0a6%2B-ae7fc4a-vs-3.13.0rc2.md)[📈](results/bm-20260223-3.15.0a6%2B-ae7fc4a/bm-20260223-vultr-x86_64-python-ae7fc4a4f6b711173bb7-3.15.0a6%2B-ae7fc4a-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-02-26](results/bm-20260226-3.15.0a6%2B-06b0920-NOGIL) | python/06b0920f1292690a22ab | 06b0920 (NOGIL) | 1.087x ↑<br>[📄](results/bm-20260226-3.15.0a6%2B-06b0920-NOGIL/bm-20260226-macm4pro-arm64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-3.12.6.md)[📈](results/bm-20260226-3.15.0a6%2B-06b0920-NOGIL/bm-20260226-macm4pro-arm64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-3.12.6.svg) | 1.009x ↑<br>[📄](results/bm-20260226-3.15.0a6%2B-06b0920-NOGIL/bm-20260226-macm4pro-arm64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-3.13.0rc2.md)[📈](results/bm-20260226-3.15.0a6%2B-06b0920-NOGIL/bm-20260226-macm4pro-arm64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-3.13.0rc2.svg) | 1.059x ↓<br>[📄](results/bm-20260226-3.15.0a6%2B-06b0920-NOGIL/bm-20260226-macm4pro-arm64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-base.md)[📈](results/bm-20260226-3.15.0a6%2B-06b0920-NOGIL/bm-20260226-macm4pro-arm64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-base.svg)[🧠](results/bm-20260226-3.15.0a6%2B-06b0920-NOGIL/bm-20260226-macm4pro-arm64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-base-mem.svg) |
| [2026-02-26](results/bm-20260226-3.15.0a6%2B-06b0920) | python/06b0920f1292690a22ab | 06b0920 | 1.154x ↑<br>[📄](results/bm-20260226-3.15.0a6%2B-06b0920/bm-20260226-macm4pro-arm64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-3.12.6.md)[📈](results/bm-20260226-3.15.0a6%2B-06b0920/bm-20260226-macm4pro-arm64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-3.12.6.svg) | 1.070x ↑<br>[📄](results/bm-20260226-3.15.0a6%2B-06b0920/bm-20260226-macm4pro-arm64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-3.13.0rc2.md)[📈](results/bm-20260226-3.15.0a6%2B-06b0920/bm-20260226-macm4pro-arm64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-3.13.0rc2.svg) |  |
| [2026-02-26](results/bm-20260226-3.15.0a6%2B-43fdb70-NOGIL) | python/43fdb7037e76c18d9545 | 43fdb70 (NOGIL) | 1.089x ↑<br>[📄](results/bm-20260226-3.15.0a6%2B-43fdb70-NOGIL/bm-20260226-macm4pro-arm64-python-43fdb7037e76c18d9545-3.15.0a6%2B-43fdb70-vs-3.12.6.md)[📈](results/bm-20260226-3.15.0a6%2B-43fdb70-NOGIL/bm-20260226-macm4pro-arm64-python-43fdb7037e76c18d9545-3.15.0a6%2B-43fdb70-vs-3.12.6.svg) | 1.010x ↑<br>[📄](results/bm-20260226-3.15.0a6%2B-43fdb70-NOGIL/bm-20260226-macm4pro-arm64-python-43fdb7037e76c18d9545-3.15.0a6%2B-43fdb70-vs-3.13.0rc2.md)[📈](results/bm-20260226-3.15.0a6%2B-43fdb70-NOGIL/bm-20260226-macm4pro-arm64-python-43fdb7037e76c18d9545-3.15.0a6%2B-43fdb70-vs-3.13.0rc2.svg) | 1.057x ↓<br>[📄](results/bm-20260226-3.15.0a6%2B-43fdb70-NOGIL/bm-20260226-macm4pro-arm64-python-43fdb7037e76c18d9545-3.15.0a6%2B-43fdb70-vs-base.md)[📈](results/bm-20260226-3.15.0a6%2B-43fdb70-NOGIL/bm-20260226-macm4pro-arm64-python-43fdb7037e76c18d9545-3.15.0a6%2B-43fdb70-vs-base.svg)[🧠](results/bm-20260226-3.15.0a6%2B-43fdb70-NOGIL/bm-20260226-macm4pro-arm64-python-43fdb7037e76c18d9545-3.15.0a6%2B-43fdb70-vs-base-mem.svg) |
| [2026-02-26](results/bm-20260226-3.15.0a6%2B-43fdb70) | python/43fdb7037e76c18d9545 | 43fdb70 | 1.153x ↑<br>[📄](results/bm-20260226-3.15.0a6%2B-43fdb70/bm-20260226-macm4pro-arm64-python-43fdb7037e76c18d9545-3.15.0a6%2B-43fdb70-vs-3.12.6.md)[📈](results/bm-20260226-3.15.0a6%2B-43fdb70/bm-20260226-macm4pro-arm64-python-43fdb7037e76c18d9545-3.15.0a6%2B-43fdb70-vs-3.12.6.svg) | 1.070x ↑<br>[📄](results/bm-20260226-3.15.0a6%2B-43fdb70/bm-20260226-macm4pro-arm64-python-43fdb7037e76c18d9545-3.15.0a6%2B-43fdb70-vs-3.13.0rc2.md)[📈](results/bm-20260226-3.15.0a6%2B-43fdb70/bm-20260226-macm4pro-arm64-python-43fdb7037e76c18d9545-3.15.0a6%2B-43fdb70-vs-3.13.0rc2.svg) |  |
| [2026-02-24](results/bm-20260224-3.15.0a6%2B-4e45c9c-NOGIL) | python/4e45c9c309abb12c6223 | 4e45c9c (NOGIL) | 1.091x ↑<br>[📄](results/bm-20260224-3.15.0a6%2B-4e45c9c-NOGIL/bm-20260224-macm4pro-arm64-python-4e45c9c309abb12c6223-3.15.0a6%2B-4e45c9c-vs-3.12.6.md)[📈](results/bm-20260224-3.15.0a6%2B-4e45c9c-NOGIL/bm-20260224-macm4pro-arm64-python-4e45c9c309abb12c6223-3.15.0a6%2B-4e45c9c-vs-3.12.6.svg) | 1.012x ↑<br>[📄](results/bm-20260224-3.15.0a6%2B-4e45c9c-NOGIL/bm-20260224-macm4pro-arm64-python-4e45c9c309abb12c6223-3.15.0a6%2B-4e45c9c-vs-3.13.0rc2.md)[📈](results/bm-20260224-3.15.0a6%2B-4e45c9c-NOGIL/bm-20260224-macm4pro-arm64-python-4e45c9c309abb12c6223-3.15.0a6%2B-4e45c9c-vs-3.13.0rc2.svg) | 1.025x ↓<br>[📄](results/bm-20260224-3.15.0a6%2B-4e45c9c-NOGIL/bm-20260224-macm4pro-arm64-python-4e45c9c309abb12c6223-3.15.0a6%2B-4e45c9c-vs-base.md)[📈](results/bm-20260224-3.15.0a6%2B-4e45c9c-NOGIL/bm-20260224-macm4pro-arm64-python-4e45c9c309abb12c6223-3.15.0a6%2B-4e45c9c-vs-base.svg)[🧠](results/bm-20260224-3.15.0a6%2B-4e45c9c-NOGIL/bm-20260224-macm4pro-arm64-python-4e45c9c309abb12c6223-3.15.0a6%2B-4e45c9c-vs-base-mem.svg) |
| [2026-02-24](results/bm-20260224-3.15.0a6%2B-4e45c9c) | python/4e45c9c309abb12c6223 | 4e45c9c | 1.119x ↑<br>[📄](results/bm-20260224-3.15.0a6%2B-4e45c9c/bm-20260224-macm4pro-arm64-python-4e45c9c309abb12c6223-3.15.0a6%2B-4e45c9c-vs-3.12.6.md)[📈](results/bm-20260224-3.15.0a6%2B-4e45c9c/bm-20260224-macm4pro-arm64-python-4e45c9c309abb12c6223-3.15.0a6%2B-4e45c9c-vs-3.12.6.svg) | 1.038x ↑<br>[📄](results/bm-20260224-3.15.0a6%2B-4e45c9c/bm-20260224-macm4pro-arm64-python-4e45c9c309abb12c6223-3.15.0a6%2B-4e45c9c-vs-3.13.0rc2.md)[📈](results/bm-20260224-3.15.0a6%2B-4e45c9c/bm-20260224-macm4pro-arm64-python-4e45c9c309abb12c6223-3.15.0a6%2B-4e45c9c-vs-3.13.0rc2.svg) |  |
| [2026-02-23](results/bm-20260223-3.15.0a6%2B-ae7fc4a-NOGIL) | python/ae7fc4a4f6b711173bb7 | ae7fc4a (NOGIL) | 1.088x ↑<br>[📄](results/bm-20260223-3.15.0a6%2B-ae7fc4a-NOGIL/bm-20260223-macm4pro-arm64-python-ae7fc4a4f6b711173bb7-3.15.0a6%2B-ae7fc4a-vs-3.12.6.md)[📈](results/bm-20260223-3.15.0a6%2B-ae7fc4a-NOGIL/bm-20260223-macm4pro-arm64-python-ae7fc4a4f6b711173bb7-3.15.0a6%2B-ae7fc4a-vs-3.12.6.svg) | 1.009x ↑<br>[📄](results/bm-20260223-3.15.0a6%2B-ae7fc4a-NOGIL/bm-20260223-macm4pro-arm64-python-ae7fc4a4f6b711173bb7-3.15.0a6%2B-ae7fc4a-vs-3.13.0rc2.md)[📈](results/bm-20260223-3.15.0a6%2B-ae7fc4a-NOGIL/bm-20260223-macm4pro-arm64-python-ae7fc4a4f6b711173bb7-3.15.0a6%2B-ae7fc4a-vs-3.13.0rc2.svg) | 1.059x ↓<br>[📄](results/bm-20260223-3.15.0a6%2B-ae7fc4a-NOGIL/bm-20260223-macm4pro-arm64-python-ae7fc4a4f6b711173bb7-3.15.0a6%2B-ae7fc4a-vs-base.md)[📈](results/bm-20260223-3.15.0a6%2B-ae7fc4a-NOGIL/bm-20260223-macm4pro-arm64-python-ae7fc4a4f6b711173bb7-3.15.0a6%2B-ae7fc4a-vs-base.svg)[🧠](results/bm-20260223-3.15.0a6%2B-ae7fc4a-NOGIL/bm-20260223-macm4pro-arm64-python-ae7fc4a4f6b711173bb7-3.15.0a6%2B-ae7fc4a-vs-base-mem.svg) |
| [2026-02-23](results/bm-20260223-3.15.0a6%2B-ae7fc4a) | python/ae7fc4a4f6b711173bb7 | ae7fc4a | 1.154x ↑<br>[📄](results/bm-20260223-3.15.0a6%2B-ae7fc4a/bm-20260223-macm4pro-arm64-python-ae7fc4a4f6b711173bb7-3.15.0a6%2B-ae7fc4a-vs-3.12.6.md)[📈](results/bm-20260223-3.15.0a6%2B-ae7fc4a/bm-20260223-macm4pro-arm64-python-ae7fc4a4f6b711173bb7-3.15.0a6%2B-ae7fc4a-vs-3.12.6.svg) | 1.071x ↑<br>[📄](results/bm-20260223-3.15.0a6%2B-ae7fc4a/bm-20260223-macm4pro-arm64-python-ae7fc4a4f6b711173bb7-3.15.0a6%2B-ae7fc4a-vs-3.13.0rc2.md)[📈](results/bm-20260223-3.15.0a6%2B-ae7fc4a/bm-20260223-macm4pro-arm64-python-ae7fc4a4f6b711173bb7-3.15.0a6%2B-ae7fc4a-vs-3.13.0rc2.svg) |  |


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
