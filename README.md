# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (979d92f)](results/bm-20260124-3.15.0a5%2B-979d92f/bm-20260124-vultr-x86_64-python-979d92fefc0b6863c978-3.15.0a5%2B-979d92f-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (979d92f)](results/bm-20260124-3.15.0a5%2B-979d92f-PYTHON_UOPS/bm-20260124-vultr-x86_64-python-979d92fefc0b6863c978-3.15.0a5%2B-979d92f-pystats.md)
- [Most recent JIT pystats on main (bedaea0)](results/bm-20251019-3.15.0a1%2B-bedaea0-JIT/bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-01-30](results/bm-20260130-3.15.0a5%2B-5f57f69-NOGIL) | python/5f57f6970bdea45cc2b1 | 5f57f69 (NOGIL) | 1.036x ↓<br>[📄](results/bm-20260130-3.15.0a5%2B-5f57f69-NOGIL/bm-20260130-vultr-x86_64-python-5f57f6970bdea45cc2b1-3.15.0a5%2B-5f57f69-vs-3.12.6.md)[📈](results/bm-20260130-3.15.0a5%2B-5f57f69-NOGIL/bm-20260130-vultr-x86_64-python-5f57f6970bdea45cc2b1-3.15.0a5%2B-5f57f69-vs-3.12.6.svg) | 1.069x ↓<br>[📄](results/bm-20260130-3.15.0a5%2B-5f57f69-NOGIL/bm-20260130-vultr-x86_64-python-5f57f6970bdea45cc2b1-3.15.0a5%2B-5f57f69-vs-3.13.0rc2.md)[📈](results/bm-20260130-3.15.0a5%2B-5f57f69-NOGIL/bm-20260130-vultr-x86_64-python-5f57f6970bdea45cc2b1-3.15.0a5%2B-5f57f69-vs-3.13.0rc2.svg) | 1.110x ↓<br>[📄](results/bm-20260130-3.15.0a5%2B-5f57f69-NOGIL/bm-20260130-vultr-x86_64-python-5f57f6970bdea45cc2b1-3.15.0a5%2B-5f57f69-vs-base.md)[📈](results/bm-20260130-3.15.0a5%2B-5f57f69-NOGIL/bm-20260130-vultr-x86_64-python-5f57f6970bdea45cc2b1-3.15.0a5%2B-5f57f69-vs-base.svg)[🧠](results/bm-20260130-3.15.0a5%2B-5f57f69-NOGIL/bm-20260130-vultr-x86_64-python-5f57f6970bdea45cc2b1-3.15.0a5%2B-5f57f69-vs-base-mem.svg) |
| [2026-01-30](results/bm-20260130-3.15.0a5%2B-5f57f69) | python/5f57f6970bdea45cc2b1 | 5f57f69 | 1.078x ↑<br>[📄](results/bm-20260130-3.15.0a5%2B-5f57f69/bm-20260130-vultr-x86_64-python-5f57f6970bdea45cc2b1-3.15.0a5%2B-5f57f69-vs-3.12.6.md)[📈](results/bm-20260130-3.15.0a5%2B-5f57f69/bm-20260130-vultr-x86_64-python-5f57f6970bdea45cc2b1-3.15.0a5%2B-5f57f69-vs-3.12.6.svg) | 1.042x ↑<br>[📄](results/bm-20260130-3.15.0a5%2B-5f57f69/bm-20260130-vultr-x86_64-python-5f57f6970bdea45cc2b1-3.15.0a5%2B-5f57f69-vs-3.13.0rc2.md)[📈](results/bm-20260130-3.15.0a5%2B-5f57f69/bm-20260130-vultr-x86_64-python-5f57f6970bdea45cc2b1-3.15.0a5%2B-5f57f69-vs-3.13.0rc2.svg) |  |
| [2026-01-29](results/bm-20260129-3.15.0a5%2B-6543720-NOGIL) | python/6543720b63a62363de54 | 6543720 (NOGIL) | 1.027x ↓<br>[📄](results/bm-20260129-3.15.0a5%2B-6543720-NOGIL/bm-20260129-vultr-x86_64-python-6543720b63a62363de54-3.15.0a5%2B-6543720-vs-3.12.6.md)[📈](results/bm-20260129-3.15.0a5%2B-6543720-NOGIL/bm-20260129-vultr-x86_64-python-6543720b63a62363de54-3.15.0a5%2B-6543720-vs-3.12.6.svg) | 1.060x ↓<br>[📄](results/bm-20260129-3.15.0a5%2B-6543720-NOGIL/bm-20260129-vultr-x86_64-python-6543720b63a62363de54-3.15.0a5%2B-6543720-vs-3.13.0rc2.md)[📈](results/bm-20260129-3.15.0a5%2B-6543720-NOGIL/bm-20260129-vultr-x86_64-python-6543720b63a62363de54-3.15.0a5%2B-6543720-vs-3.13.0rc2.svg) | 1.102x ↓<br>[📄](results/bm-20260129-3.15.0a5%2B-6543720-NOGIL/bm-20260129-vultr-x86_64-python-6543720b63a62363de54-3.15.0a5%2B-6543720-vs-base.md)[📈](results/bm-20260129-3.15.0a5%2B-6543720-NOGIL/bm-20260129-vultr-x86_64-python-6543720b63a62363de54-3.15.0a5%2B-6543720-vs-base.svg)[🧠](results/bm-20260129-3.15.0a5%2B-6543720-NOGIL/bm-20260129-vultr-x86_64-python-6543720b63a62363de54-3.15.0a5%2B-6543720-vs-base-mem.svg) |
| [2026-01-29](results/bm-20260129-3.15.0a5%2B-6543720) | python/6543720b63a62363de54 | 6543720 | 1.077x ↑<br>[📄](results/bm-20260129-3.15.0a5%2B-6543720/bm-20260129-vultr-x86_64-python-6543720b63a62363de54-3.15.0a5%2B-6543720-vs-3.12.6.md)[📈](results/bm-20260129-3.15.0a5%2B-6543720/bm-20260129-vultr-x86_64-python-6543720b63a62363de54-3.15.0a5%2B-6543720-vs-3.12.6.svg) | 1.041x ↑<br>[📄](results/bm-20260129-3.15.0a5%2B-6543720/bm-20260129-vultr-x86_64-python-6543720b63a62363de54-3.15.0a5%2B-6543720-vs-3.13.0rc2.md)[📈](results/bm-20260129-3.15.0a5%2B-6543720/bm-20260129-vultr-x86_64-python-6543720b63a62363de54-3.15.0a5%2B-6543720-vs-3.13.0rc2.svg) |  |
| [2026-01-27](results/bm-20260127-3.15.0a5%2B-6ea3f8c-NOGIL) | python/6ea3f8cd7ff4ff9769ae | 6ea3f8c (NOGIL) | 1.032x ↓<br>[📄](results/bm-20260127-3.15.0a5%2B-6ea3f8c-NOGIL/bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5%2B-6ea3f8c-vs-3.12.6.md)[📈](results/bm-20260127-3.15.0a5%2B-6ea3f8c-NOGIL/bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5%2B-6ea3f8c-vs-3.12.6.svg) | 1.065x ↓<br>[📄](results/bm-20260127-3.15.0a5%2B-6ea3f8c-NOGIL/bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5%2B-6ea3f8c-vs-3.13.0rc2.md)[📈](results/bm-20260127-3.15.0a5%2B-6ea3f8c-NOGIL/bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5%2B-6ea3f8c-vs-3.13.0rc2.svg) | 1.105x ↓<br>[📄](results/bm-20260127-3.15.0a5%2B-6ea3f8c-NOGIL/bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5%2B-6ea3f8c-vs-base.md)[📈](results/bm-20260127-3.15.0a5%2B-6ea3f8c-NOGIL/bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5%2B-6ea3f8c-vs-base.svg)[🧠](results/bm-20260127-3.15.0a5%2B-6ea3f8c-NOGIL/bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5%2B-6ea3f8c-vs-base-mem.svg) |
| [2026-01-27](results/bm-20260127-3.15.0a5%2B-6ea3f8c) | python/6ea3f8cd7ff4ff9769ae | 6ea3f8c | 1.077x ↑<br>[📄](results/bm-20260127-3.15.0a5%2B-6ea3f8c/bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5%2B-6ea3f8c-vs-3.12.6.md)[📈](results/bm-20260127-3.15.0a5%2B-6ea3f8c/bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5%2B-6ea3f8c-vs-3.12.6.svg) | 1.041x ↑<br>[📄](results/bm-20260127-3.15.0a5%2B-6ea3f8c/bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5%2B-6ea3f8c-vs-3.13.0rc2.md)[📈](results/bm-20260127-3.15.0a5%2B-6ea3f8c/bm-20260127-vultr-x86_64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5%2B-6ea3f8c-vs-3.13.0rc2.svg) |  |
| [2026-01-27](results/bm-20260127-3.15.0a5%2B-8fd3f20) | DinoV/lazy_review_updates2 | 8fd3f20 | 1.073x ↑<br>[📄](results/bm-20260127-3.15.0a5%2B-8fd3f20/bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5%2B-8fd3f20-vs-3.12.6.md)[📈](results/bm-20260127-3.15.0a5%2B-8fd3f20/bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5%2B-8fd3f20-vs-3.12.6.svg) | 1.038x ↑<br>[📄](results/bm-20260127-3.15.0a5%2B-8fd3f20/bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5%2B-8fd3f20-vs-3.13.0rc2.md)[📈](results/bm-20260127-3.15.0a5%2B-8fd3f20/bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5%2B-8fd3f20-vs-3.13.0rc2.svg) | 1.001x ↑<br>[📄](results/bm-20260127-3.15.0a5%2B-8fd3f20/bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5%2B-8fd3f20-vs-base.md)[📈](results/bm-20260127-3.15.0a5%2B-8fd3f20/bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5%2B-8fd3f20-vs-base.svg)[🧠](results/bm-20260127-3.15.0a5%2B-8fd3f20/bm-20260127-vultr-x86_64-DinoV-lazy_review_updates2-3.15.0a5%2B-8fd3f20-vs-base-mem.svg) |
| [2026-01-26](results/bm-20260126-3.15.0a5%2B-2520617-NOGIL) | python/25206173619f5f387c88 | 2520617 (NOGIL) | 1.031x ↓<br>[📄](results/bm-20260126-3.15.0a5%2B-2520617-NOGIL/bm-20260126-vultr-x86_64-python-25206173619f5f387c88-3.15.0a5%2B-2520617-vs-3.12.6.md)[📈](results/bm-20260126-3.15.0a5%2B-2520617-NOGIL/bm-20260126-vultr-x86_64-python-25206173619f5f387c88-3.15.0a5%2B-2520617-vs-3.12.6.svg) | 1.064x ↓<br>[📄](results/bm-20260126-3.15.0a5%2B-2520617-NOGIL/bm-20260126-vultr-x86_64-python-25206173619f5f387c88-3.15.0a5%2B-2520617-vs-3.13.0rc2.md)[📈](results/bm-20260126-3.15.0a5%2B-2520617-NOGIL/bm-20260126-vultr-x86_64-python-25206173619f5f387c88-3.15.0a5%2B-2520617-vs-3.13.0rc2.svg) | 1.109x ↓<br>[📄](results/bm-20260126-3.15.0a5%2B-2520617-NOGIL/bm-20260126-vultr-x86_64-python-25206173619f5f387c88-3.15.0a5%2B-2520617-vs-base.md)[📈](results/bm-20260126-3.15.0a5%2B-2520617-NOGIL/bm-20260126-vultr-x86_64-python-25206173619f5f387c88-3.15.0a5%2B-2520617-vs-base.svg)[🧠](results/bm-20260126-3.15.0a5%2B-2520617-NOGIL/bm-20260126-vultr-x86_64-python-25206173619f5f387c88-3.15.0a5%2B-2520617-vs-base-mem.svg) |
| [2026-01-26](results/bm-20260126-3.15.0a5%2B-2520617) | python/25206173619f5f387c88 | 2520617 | 1.083x ↑<br>[📄](results/bm-20260126-3.15.0a5%2B-2520617/bm-20260126-vultr-x86_64-python-25206173619f5f387c88-3.15.0a5%2B-2520617-vs-3.12.6.md)[📈](results/bm-20260126-3.15.0a5%2B-2520617/bm-20260126-vultr-x86_64-python-25206173619f5f387c88-3.15.0a5%2B-2520617-vs-3.12.6.svg) | 1.047x ↑<br>[📄](results/bm-20260126-3.15.0a5%2B-2520617/bm-20260126-vultr-x86_64-python-25206173619f5f387c88-3.15.0a5%2B-2520617-vs-3.13.0rc2.md)[📈](results/bm-20260126-3.15.0a5%2B-2520617/bm-20260126-vultr-x86_64-python-25206173619f5f387c88-3.15.0a5%2B-2520617-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-01-30](results/bm-20260130-3.15.0a5%2B-5f57f69-NOGIL) | python/5f57f6970bdea45cc2b1 | 5f57f69 (NOGIL) | 1.118x ↑<br>[📄](results/bm-20260130-3.15.0a5%2B-5f57f69-NOGIL/bm-20260130-macm4pro-arm64-python-5f57f6970bdea45cc2b1-3.15.0a5%2B-5f57f69-vs-3.12.6.md)[📈](results/bm-20260130-3.15.0a5%2B-5f57f69-NOGIL/bm-20260130-macm4pro-arm64-python-5f57f6970bdea45cc2b1-3.15.0a5%2B-5f57f69-vs-3.12.6.svg) | 1.037x ↑<br>[📄](results/bm-20260130-3.15.0a5%2B-5f57f69-NOGIL/bm-20260130-macm4pro-arm64-python-5f57f6970bdea45cc2b1-3.15.0a5%2B-5f57f69-vs-3.13.0rc2.md)[📈](results/bm-20260130-3.15.0a5%2B-5f57f69-NOGIL/bm-20260130-macm4pro-arm64-python-5f57f6970bdea45cc2b1-3.15.0a5%2B-5f57f69-vs-3.13.0rc2.svg) | 1.069x ↓<br>[📄](results/bm-20260130-3.15.0a5%2B-5f57f69-NOGIL/bm-20260130-macm4pro-arm64-python-5f57f6970bdea45cc2b1-3.15.0a5%2B-5f57f69-vs-base.md)[📈](results/bm-20260130-3.15.0a5%2B-5f57f69-NOGIL/bm-20260130-macm4pro-arm64-python-5f57f6970bdea45cc2b1-3.15.0a5%2B-5f57f69-vs-base.svg)[🧠](results/bm-20260130-3.15.0a5%2B-5f57f69-NOGIL/bm-20260130-macm4pro-arm64-python-5f57f6970bdea45cc2b1-3.15.0a5%2B-5f57f69-vs-base-mem.svg) |
| [2026-01-30](results/bm-20260130-3.15.0a5%2B-5f57f69) | python/5f57f6970bdea45cc2b1 | 5f57f69 | 1.200x ↑<br>[📄](results/bm-20260130-3.15.0a5%2B-5f57f69/bm-20260130-macm4pro-arm64-python-5f57f6970bdea45cc2b1-3.15.0a5%2B-5f57f69-vs-3.12.6.md)[📈](results/bm-20260130-3.15.0a5%2B-5f57f69/bm-20260130-macm4pro-arm64-python-5f57f6970bdea45cc2b1-3.15.0a5%2B-5f57f69-vs-3.12.6.svg) | 1.113x ↑<br>[📄](results/bm-20260130-3.15.0a5%2B-5f57f69/bm-20260130-macm4pro-arm64-python-5f57f6970bdea45cc2b1-3.15.0a5%2B-5f57f69-vs-3.13.0rc2.md)[📈](results/bm-20260130-3.15.0a5%2B-5f57f69/bm-20260130-macm4pro-arm64-python-5f57f6970bdea45cc2b1-3.15.0a5%2B-5f57f69-vs-3.13.0rc2.svg) |  |
| [2026-01-29](results/bm-20260129-3.15.0a5%2B-6543720-NOGIL) | python/6543720b63a62363de54 | 6543720 (NOGIL) | 1.114x ↑<br>[📄](results/bm-20260129-3.15.0a5%2B-6543720-NOGIL/bm-20260129-macm4pro-arm64-python-6543720b63a62363de54-3.15.0a5%2B-6543720-vs-3.12.6.md)[📈](results/bm-20260129-3.15.0a5%2B-6543720-NOGIL/bm-20260129-macm4pro-arm64-python-6543720b63a62363de54-3.15.0a5%2B-6543720-vs-3.12.6.svg) | 1.033x ↑<br>[📄](results/bm-20260129-3.15.0a5%2B-6543720-NOGIL/bm-20260129-macm4pro-arm64-python-6543720b63a62363de54-3.15.0a5%2B-6543720-vs-3.13.0rc2.md)[📈](results/bm-20260129-3.15.0a5%2B-6543720-NOGIL/bm-20260129-macm4pro-arm64-python-6543720b63a62363de54-3.15.0a5%2B-6543720-vs-3.13.0rc2.svg) | 1.069x ↓<br>[📄](results/bm-20260129-3.15.0a5%2B-6543720-NOGIL/bm-20260129-macm4pro-arm64-python-6543720b63a62363de54-3.15.0a5%2B-6543720-vs-base.md)[📈](results/bm-20260129-3.15.0a5%2B-6543720-NOGIL/bm-20260129-macm4pro-arm64-python-6543720b63a62363de54-3.15.0a5%2B-6543720-vs-base.svg)[🧠](results/bm-20260129-3.15.0a5%2B-6543720-NOGIL/bm-20260129-macm4pro-arm64-python-6543720b63a62363de54-3.15.0a5%2B-6543720-vs-base-mem.svg) |
| [2026-01-29](results/bm-20260129-3.15.0a5%2B-6543720) | python/6543720b63a62363de54 | 6543720 | 1.195x ↑<br>[📄](results/bm-20260129-3.15.0a5%2B-6543720/bm-20260129-macm4pro-arm64-python-6543720b63a62363de54-3.15.0a5%2B-6543720-vs-3.12.6.md)[📈](results/bm-20260129-3.15.0a5%2B-6543720/bm-20260129-macm4pro-arm64-python-6543720b63a62363de54-3.15.0a5%2B-6543720-vs-3.12.6.svg) | 1.109x ↑<br>[📄](results/bm-20260129-3.15.0a5%2B-6543720/bm-20260129-macm4pro-arm64-python-6543720b63a62363de54-3.15.0a5%2B-6543720-vs-3.13.0rc2.md)[📈](results/bm-20260129-3.15.0a5%2B-6543720/bm-20260129-macm4pro-arm64-python-6543720b63a62363de54-3.15.0a5%2B-6543720-vs-3.13.0rc2.svg) |  |
| [2026-01-27](results/bm-20260127-3.15.0a5%2B-6ea3f8c-NOGIL) | python/6ea3f8cd7ff4ff9769ae | 6ea3f8c (NOGIL) | 1.123x ↑<br>[📄](results/bm-20260127-3.15.0a5%2B-6ea3f8c-NOGIL/bm-20260127-macm4pro-arm64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5%2B-6ea3f8c-vs-3.12.6.md)[📈](results/bm-20260127-3.15.0a5%2B-6ea3f8c-NOGIL/bm-20260127-macm4pro-arm64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5%2B-6ea3f8c-vs-3.12.6.svg) | 1.042x ↑<br>[📄](results/bm-20260127-3.15.0a5%2B-6ea3f8c-NOGIL/bm-20260127-macm4pro-arm64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5%2B-6ea3f8c-vs-3.13.0rc2.md)[📈](results/bm-20260127-3.15.0a5%2B-6ea3f8c-NOGIL/bm-20260127-macm4pro-arm64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5%2B-6ea3f8c-vs-3.13.0rc2.svg) | 1.053x ↓<br>[📄](results/bm-20260127-3.15.0a5%2B-6ea3f8c-NOGIL/bm-20260127-macm4pro-arm64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5%2B-6ea3f8c-vs-base.md)[📈](results/bm-20260127-3.15.0a5%2B-6ea3f8c-NOGIL/bm-20260127-macm4pro-arm64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5%2B-6ea3f8c-vs-base.svg)[🧠](results/bm-20260127-3.15.0a5%2B-6ea3f8c-NOGIL/bm-20260127-macm4pro-arm64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5%2B-6ea3f8c-vs-base-mem.svg) |
| [2026-01-27](results/bm-20260127-3.15.0a5%2B-6ea3f8c) | python/6ea3f8cd7ff4ff9769ae | 6ea3f8c | 1.185x ↑<br>[📄](results/bm-20260127-3.15.0a5%2B-6ea3f8c/bm-20260127-macm4pro-arm64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5%2B-6ea3f8c-vs-3.12.6.md)[📈](results/bm-20260127-3.15.0a5%2B-6ea3f8c/bm-20260127-macm4pro-arm64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5%2B-6ea3f8c-vs-3.12.6.svg) | 1.100x ↑<br>[📄](results/bm-20260127-3.15.0a5%2B-6ea3f8c/bm-20260127-macm4pro-arm64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5%2B-6ea3f8c-vs-3.13.0rc2.md)[📈](results/bm-20260127-3.15.0a5%2B-6ea3f8c/bm-20260127-macm4pro-arm64-python-6ea3f8cd7ff4ff9769ae-3.15.0a5%2B-6ea3f8c-vs-3.13.0rc2.svg) |  |
| [2026-01-26](results/bm-20260126-3.15.0a5%2B-2520617-NOGIL) | python/25206173619f5f387c88 | 2520617 (NOGIL) | 1.117x ↑<br>[📄](results/bm-20260126-3.15.0a5%2B-2520617-NOGIL/bm-20260126-macm4pro-arm64-python-25206173619f5f387c88-3.15.0a5%2B-2520617-vs-3.12.6.md)[📈](results/bm-20260126-3.15.0a5%2B-2520617-NOGIL/bm-20260126-macm4pro-arm64-python-25206173619f5f387c88-3.15.0a5%2B-2520617-vs-3.12.6.svg) | 1.037x ↑<br>[📄](results/bm-20260126-3.15.0a5%2B-2520617-NOGIL/bm-20260126-macm4pro-arm64-python-25206173619f5f387c88-3.15.0a5%2B-2520617-vs-3.13.0rc2.md)[📈](results/bm-20260126-3.15.0a5%2B-2520617-NOGIL/bm-20260126-macm4pro-arm64-python-25206173619f5f387c88-3.15.0a5%2B-2520617-vs-3.13.0rc2.svg) | 1.068x ↓<br>[📄](results/bm-20260126-3.15.0a5%2B-2520617-NOGIL/bm-20260126-macm4pro-arm64-python-25206173619f5f387c88-3.15.0a5%2B-2520617-vs-base.md)[📈](results/bm-20260126-3.15.0a5%2B-2520617-NOGIL/bm-20260126-macm4pro-arm64-python-25206173619f5f387c88-3.15.0a5%2B-2520617-vs-base.svg)[🧠](results/bm-20260126-3.15.0a5%2B-2520617-NOGIL/bm-20260126-macm4pro-arm64-python-25206173619f5f387c88-3.15.0a5%2B-2520617-vs-base-mem.svg) |
| [2026-01-26](results/bm-20260126-3.15.0a5%2B-2520617) | python/25206173619f5f387c88 | 2520617 | 1.198x ↑<br>[📄](results/bm-20260126-3.15.0a5%2B-2520617/bm-20260126-macm4pro-arm64-python-25206173619f5f387c88-3.15.0a5%2B-2520617-vs-3.12.6.md)[📈](results/bm-20260126-3.15.0a5%2B-2520617/bm-20260126-macm4pro-arm64-python-25206173619f5f387c88-3.15.0a5%2B-2520617-vs-3.12.6.svg) | 1.111x ↑<br>[📄](results/bm-20260126-3.15.0a5%2B-2520617/bm-20260126-macm4pro-arm64-python-25206173619f5f387c88-3.15.0a5%2B-2520617-vs-3.13.0rc2.md)[📈](results/bm-20260126-3.15.0a5%2B-2520617/bm-20260126-macm4pro-arm64-python-25206173619f5f387c88-3.15.0a5%2B-2520617-vs-3.13.0rc2.svg) |  |


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
