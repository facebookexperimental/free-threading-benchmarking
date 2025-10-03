# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (48d0d0d)](results/bm-20250926-3.15.0a0-48d0d0d/bm-20250926-vultr-x86_64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (48d0d0d)](results/bm-20250926-3.15.0a0-48d0d0d-PYTHON_UOPS/bm-20250926-vultr-x86_64-python-48d0d0dd9733eae4935f-3.15.0a0-48d0d0d-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-10-02](results/bm-20251002-3.15.0a0-4e7e2dd-NOGIL) | python/4e7e2dd043c1da85b0c1 | 4e7e2dd (NOGIL) | 1.012x ↓<br>[📄](results/bm-20251002-3.15.0a0-4e7e2dd-NOGIL/bm-20251002-vultr-x86_64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd-vs-3.12.6.md)[📈](results/bm-20251002-3.15.0a0-4e7e2dd-NOGIL/bm-20251002-vultr-x86_64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd-vs-3.12.6.svg) | 1.045x ↓<br>[📄](results/bm-20251002-3.15.0a0-4e7e2dd-NOGIL/bm-20251002-vultr-x86_64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd-vs-3.13.0rc2.md)[📈](results/bm-20251002-3.15.0a0-4e7e2dd-NOGIL/bm-20251002-vultr-x86_64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd-vs-3.13.0rc2.svg) | 1.086x ↓<br>[📄](results/bm-20251002-3.15.0a0-4e7e2dd-NOGIL/bm-20251002-vultr-x86_64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd-vs-base.md)[📈](results/bm-20251002-3.15.0a0-4e7e2dd-NOGIL/bm-20251002-vultr-x86_64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd-vs-base.svg)[🧠](results/bm-20251002-3.15.0a0-4e7e2dd-NOGIL/bm-20251002-vultr-x86_64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd-vs-base-mem.svg) |
| [2025-10-02](results/bm-20251002-3.15.0a0-4e7e2dd) | python/4e7e2dd043c1da85b0c1 | 4e7e2dd | 1.074x ↑<br>[📄](results/bm-20251002-3.15.0a0-4e7e2dd/bm-20251002-vultr-x86_64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd-vs-3.12.6.md)[📈](results/bm-20251002-3.15.0a0-4e7e2dd/bm-20251002-vultr-x86_64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd-vs-3.12.6.svg) | 1.038x ↑<br>[📄](results/bm-20251002-3.15.0a0-4e7e2dd/bm-20251002-vultr-x86_64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd-vs-3.13.0rc2.md)[📈](results/bm-20251002-3.15.0a0-4e7e2dd/bm-20251002-vultr-x86_64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd-vs-3.13.0rc2.svg) |  |
| [2025-10-01](results/bm-20251001-3.15.0a0-75b1afe-NOGIL) | python/75b1afe562c02962393c | 75b1afe (NOGIL) | 1.018x ↓<br>[📄](results/bm-20251001-3.15.0a0-75b1afe-NOGIL/bm-20251001-vultr-x86_64-python-75b1afe562c02962393c-3.15.0a0-75b1afe-vs-3.12.6.md)[📈](results/bm-20251001-3.15.0a0-75b1afe-NOGIL/bm-20251001-vultr-x86_64-python-75b1afe562c02962393c-3.15.0a0-75b1afe-vs-3.12.6.svg) | 1.051x ↓<br>[📄](results/bm-20251001-3.15.0a0-75b1afe-NOGIL/bm-20251001-vultr-x86_64-python-75b1afe562c02962393c-3.15.0a0-75b1afe-vs-3.13.0rc2.md)[📈](results/bm-20251001-3.15.0a0-75b1afe-NOGIL/bm-20251001-vultr-x86_64-python-75b1afe562c02962393c-3.15.0a0-75b1afe-vs-3.13.0rc2.svg) | 1.089x ↓<br>[📄](results/bm-20251001-3.15.0a0-75b1afe-NOGIL/bm-20251001-vultr-x86_64-python-75b1afe562c02962393c-3.15.0a0-75b1afe-vs-base.md)[📈](results/bm-20251001-3.15.0a0-75b1afe-NOGIL/bm-20251001-vultr-x86_64-python-75b1afe562c02962393c-3.15.0a0-75b1afe-vs-base.svg)[🧠](results/bm-20251001-3.15.0a0-75b1afe-NOGIL/bm-20251001-vultr-x86_64-python-75b1afe562c02962393c-3.15.0a0-75b1afe-vs-base-mem.svg) |
| [2025-10-01](results/bm-20251001-3.15.0a0-75b1afe) | python/75b1afe562c02962393c | 75b1afe | 1.071x ↑<br>[📄](results/bm-20251001-3.15.0a0-75b1afe/bm-20251001-vultr-x86_64-python-75b1afe562c02962393c-3.15.0a0-75b1afe-vs-3.12.6.md)[📈](results/bm-20251001-3.15.0a0-75b1afe/bm-20251001-vultr-x86_64-python-75b1afe562c02962393c-3.15.0a0-75b1afe-vs-3.12.6.svg) | 1.035x ↑<br>[📄](results/bm-20251001-3.15.0a0-75b1afe/bm-20251001-vultr-x86_64-python-75b1afe562c02962393c-3.15.0a0-75b1afe-vs-3.13.0rc2.md)[📈](results/bm-20251001-3.15.0a0-75b1afe/bm-20251001-vultr-x86_64-python-75b1afe562c02962393c-3.15.0a0-75b1afe-vs-3.13.0rc2.svg) |  |
| [2025-09-30](results/bm-20250930-3.15.0a0-98a41af-NOGIL) | python/98a41af5b09343fa030e | 98a41af (NOGIL) | 1.017x ↓<br>[📄](results/bm-20250930-3.15.0a0-98a41af-NOGIL/bm-20250930-vultr-x86_64-python-98a41af5b09343fa030e-3.15.0a0-98a41af-vs-3.12.6.md)[📈](results/bm-20250930-3.15.0a0-98a41af-NOGIL/bm-20250930-vultr-x86_64-python-98a41af5b09343fa030e-3.15.0a0-98a41af-vs-3.12.6.svg) | 1.050x ↓<br>[📄](results/bm-20250930-3.15.0a0-98a41af-NOGIL/bm-20250930-vultr-x86_64-python-98a41af5b09343fa030e-3.15.0a0-98a41af-vs-3.13.0rc2.md)[📈](results/bm-20250930-3.15.0a0-98a41af-NOGIL/bm-20250930-vultr-x86_64-python-98a41af5b09343fa030e-3.15.0a0-98a41af-vs-3.13.0rc2.svg) | 1.091x ↓<br>[📄](results/bm-20250930-3.15.0a0-98a41af-NOGIL/bm-20250930-vultr-x86_64-python-98a41af5b09343fa030e-3.15.0a0-98a41af-vs-base.md)[📈](results/bm-20250930-3.15.0a0-98a41af-NOGIL/bm-20250930-vultr-x86_64-python-98a41af5b09343fa030e-3.15.0a0-98a41af-vs-base.svg)[🧠](results/bm-20250930-3.15.0a0-98a41af-NOGIL/bm-20250930-vultr-x86_64-python-98a41af5b09343fa030e-3.15.0a0-98a41af-vs-base-mem.svg) |
| [2025-09-30](results/bm-20250930-3.15.0a0-98a41af) | python/98a41af5b09343fa030e | 98a41af | 1.075x ↑<br>[📄](results/bm-20250930-3.15.0a0-98a41af/bm-20250930-vultr-x86_64-python-98a41af5b09343fa030e-3.15.0a0-98a41af-vs-3.12.6.md)[📈](results/bm-20250930-3.15.0a0-98a41af/bm-20250930-vultr-x86_64-python-98a41af5b09343fa030e-3.15.0a0-98a41af-vs-3.12.6.svg) | 1.039x ↑<br>[📄](results/bm-20250930-3.15.0a0-98a41af/bm-20250930-vultr-x86_64-python-98a41af5b09343fa030e-3.15.0a0-98a41af-vs-3.13.0rc2.md)[📈](results/bm-20250930-3.15.0a0-98a41af/bm-20250930-vultr-x86_64-python-98a41af5b09343fa030e-3.15.0a0-98a41af-vs-3.13.0rc2.svg) |  |
| [2025-09-29](results/bm-20250929-3.15.0a0-6b5f156-NOGIL) | python/6b5f15698a436591f7c3 | 6b5f156 (NOGIL) | 1.020x ↓<br>[📄](results/bm-20250929-3.15.0a0-6b5f156-NOGIL/bm-20250929-vultr-x86_64-python-6b5f15698a436591f7c3-3.15.0a0-6b5f156-vs-3.12.6.md)[📈](results/bm-20250929-3.15.0a0-6b5f156-NOGIL/bm-20250929-vultr-x86_64-python-6b5f15698a436591f7c3-3.15.0a0-6b5f156-vs-3.12.6.svg) | 1.053x ↓<br>[📄](results/bm-20250929-3.15.0a0-6b5f156-NOGIL/bm-20250929-vultr-x86_64-python-6b5f15698a436591f7c3-3.15.0a0-6b5f156-vs-3.13.0rc2.md)[📈](results/bm-20250929-3.15.0a0-6b5f156-NOGIL/bm-20250929-vultr-x86_64-python-6b5f15698a436591f7c3-3.15.0a0-6b5f156-vs-3.13.0rc2.svg) | 1.093x ↓<br>[📄](results/bm-20250929-3.15.0a0-6b5f156-NOGIL/bm-20250929-vultr-x86_64-python-6b5f15698a436591f7c3-3.15.0a0-6b5f156-vs-base.md)[📈](results/bm-20250929-3.15.0a0-6b5f156-NOGIL/bm-20250929-vultr-x86_64-python-6b5f15698a436591f7c3-3.15.0a0-6b5f156-vs-base.svg)[🧠](results/bm-20250929-3.15.0a0-6b5f156-NOGIL/bm-20250929-vultr-x86_64-python-6b5f15698a436591f7c3-3.15.0a0-6b5f156-vs-base-mem.svg) |
| [2025-09-29](results/bm-20250929-3.15.0a0-6b5f156) | python/6b5f15698a436591f7c3 | 6b5f156 | 1.073x ↑<br>[📄](results/bm-20250929-3.15.0a0-6b5f156/bm-20250929-vultr-x86_64-python-6b5f15698a436591f7c3-3.15.0a0-6b5f156-vs-3.12.6.md)[📈](results/bm-20250929-3.15.0a0-6b5f156/bm-20250929-vultr-x86_64-python-6b5f15698a436591f7c3-3.15.0a0-6b5f156-vs-3.12.6.svg) | 1.037x ↑<br>[📄](results/bm-20250929-3.15.0a0-6b5f156/bm-20250929-vultr-x86_64-python-6b5f15698a436591f7c3-3.15.0a0-6b5f156-vs-3.13.0rc2.md)[📈](results/bm-20250929-3.15.0a0-6b5f156/bm-20250929-vultr-x86_64-python-6b5f15698a436591f7c3-3.15.0a0-6b5f156-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-10-02](results/bm-20251002-3.15.0a0-4e7e2dd-NOGIL) | python/4e7e2dd043c1da85b0c1 | 4e7e2dd (NOGIL) | 1.083x ↑<br>[📄](results/bm-20251002-3.15.0a0-4e7e2dd-NOGIL/bm-20251002-macm4pro-arm64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd-vs-3.12.6.md)[📈](results/bm-20251002-3.15.0a0-4e7e2dd-NOGIL/bm-20251002-macm4pro-arm64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd-vs-3.12.6.svg) | 1.005x ↑<br>[📄](results/bm-20251002-3.15.0a0-4e7e2dd-NOGIL/bm-20251002-macm4pro-arm64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd-vs-3.13.0rc2.md)[📈](results/bm-20251002-3.15.0a0-4e7e2dd-NOGIL/bm-20251002-macm4pro-arm64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd-vs-3.13.0rc2.svg) | 1.001x ↓<br>[📄](results/bm-20251002-3.15.0a0-4e7e2dd-NOGIL/bm-20251002-macm4pro-arm64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd-vs-base.md)[📈](results/bm-20251002-3.15.0a0-4e7e2dd-NOGIL/bm-20251002-macm4pro-arm64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd-vs-base.svg)[🧠](results/bm-20251002-3.15.0a0-4e7e2dd-NOGIL/bm-20251002-macm4pro-arm64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd-vs-base-mem.svg) |
| [2025-10-02](results/bm-20251002-3.15.0a0-4e7e2dd) | python/4e7e2dd043c1da85b0c1 | 4e7e2dd | 1.083x ↑<br>[📄](results/bm-20251002-3.15.0a0-4e7e2dd/bm-20251002-macm4pro-arm64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd-vs-3.12.6.md)[📈](results/bm-20251002-3.15.0a0-4e7e2dd/bm-20251002-macm4pro-arm64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd-vs-3.12.6.svg) | 1.005x ↑<br>[📄](results/bm-20251002-3.15.0a0-4e7e2dd/bm-20251002-macm4pro-arm64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd-vs-3.13.0rc2.md)[📈](results/bm-20251002-3.15.0a0-4e7e2dd/bm-20251002-macm4pro-arm64-python-4e7e2dd043c1da85b0c1-3.15.0a0-4e7e2dd-vs-3.13.0rc2.svg) |  |
| [2025-10-01](results/bm-20251001-3.15.0a0-75b1afe-NOGIL) | python/75b1afe562c02962393c | 75b1afe (NOGIL) | 1.085x ↑<br>[📄](results/bm-20251001-3.15.0a0-75b1afe-NOGIL/bm-20251001-macm4pro-arm64-python-75b1afe562c02962393c-3.15.0a0-75b1afe-vs-3.12.6.md)[📈](results/bm-20251001-3.15.0a0-75b1afe-NOGIL/bm-20251001-macm4pro-arm64-python-75b1afe562c02962393c-3.15.0a0-75b1afe-vs-3.12.6.svg) | 1.007x ↑<br>[📄](results/bm-20251001-3.15.0a0-75b1afe-NOGIL/bm-20251001-macm4pro-arm64-python-75b1afe562c02962393c-3.15.0a0-75b1afe-vs-3.13.0rc2.md)[📈](results/bm-20251001-3.15.0a0-75b1afe-NOGIL/bm-20251001-macm4pro-arm64-python-75b1afe562c02962393c-3.15.0a0-75b1afe-vs-3.13.0rc2.svg) | 1.000x ↑<br>[📄](results/bm-20251001-3.15.0a0-75b1afe-NOGIL/bm-20251001-macm4pro-arm64-python-75b1afe562c02962393c-3.15.0a0-75b1afe-vs-base.md)[📈](results/bm-20251001-3.15.0a0-75b1afe-NOGIL/bm-20251001-macm4pro-arm64-python-75b1afe562c02962393c-3.15.0a0-75b1afe-vs-base.svg)[🧠](results/bm-20251001-3.15.0a0-75b1afe-NOGIL/bm-20251001-macm4pro-arm64-python-75b1afe562c02962393c-3.15.0a0-75b1afe-vs-base-mem.svg) |
| [2025-10-01](results/bm-20251001-3.15.0a0-75b1afe) | python/75b1afe562c02962393c | 75b1afe | 1.083x ↑<br>[📄](results/bm-20251001-3.15.0a0-75b1afe/bm-20251001-macm4pro-arm64-python-75b1afe562c02962393c-3.15.0a0-75b1afe-vs-3.12.6.md)[📈](results/bm-20251001-3.15.0a0-75b1afe/bm-20251001-macm4pro-arm64-python-75b1afe562c02962393c-3.15.0a0-75b1afe-vs-3.12.6.svg) | 1.005x ↑<br>[📄](results/bm-20251001-3.15.0a0-75b1afe/bm-20251001-macm4pro-arm64-python-75b1afe562c02962393c-3.15.0a0-75b1afe-vs-3.13.0rc2.md)[📈](results/bm-20251001-3.15.0a0-75b1afe/bm-20251001-macm4pro-arm64-python-75b1afe562c02962393c-3.15.0a0-75b1afe-vs-3.13.0rc2.svg) |  |
| [2025-09-30](results/bm-20250930-3.15.0a0-98a41af-NOGIL) | python/98a41af5b09343fa030e | 98a41af (NOGIL) | 1.088x ↑<br>[📄](results/bm-20250930-3.15.0a0-98a41af-NOGIL/bm-20250930-macm4pro-arm64-python-98a41af5b09343fa030e-3.15.0a0-98a41af-vs-3.12.6.md)[📈](results/bm-20250930-3.15.0a0-98a41af-NOGIL/bm-20250930-macm4pro-arm64-python-98a41af5b09343fa030e-3.15.0a0-98a41af-vs-3.12.6.svg) | 1.009x ↑<br>[📄](results/bm-20250930-3.15.0a0-98a41af-NOGIL/bm-20250930-macm4pro-arm64-python-98a41af5b09343fa030e-3.15.0a0-98a41af-vs-3.13.0rc2.md)[📈](results/bm-20250930-3.15.0a0-98a41af-NOGIL/bm-20250930-macm4pro-arm64-python-98a41af5b09343fa030e-3.15.0a0-98a41af-vs-3.13.0rc2.svg) | 1.005x ↓<br>[📄](results/bm-20250930-3.15.0a0-98a41af-NOGIL/bm-20250930-macm4pro-arm64-python-98a41af5b09343fa030e-3.15.0a0-98a41af-vs-base.md)[📈](results/bm-20250930-3.15.0a0-98a41af-NOGIL/bm-20250930-macm4pro-arm64-python-98a41af5b09343fa030e-3.15.0a0-98a41af-vs-base.svg)[🧠](results/bm-20250930-3.15.0a0-98a41af-NOGIL/bm-20250930-macm4pro-arm64-python-98a41af5b09343fa030e-3.15.0a0-98a41af-vs-base-mem.svg) |
| [2025-09-30](results/bm-20250930-3.15.0a0-98a41af) | python/98a41af5b09343fa030e | 98a41af | 1.091x ↑<br>[📄](results/bm-20250930-3.15.0a0-98a41af/bm-20250930-macm4pro-arm64-python-98a41af5b09343fa030e-3.15.0a0-98a41af-vs-3.12.6.md)[📈](results/bm-20250930-3.15.0a0-98a41af/bm-20250930-macm4pro-arm64-python-98a41af5b09343fa030e-3.15.0a0-98a41af-vs-3.12.6.svg) | 1.013x ↑<br>[📄](results/bm-20250930-3.15.0a0-98a41af/bm-20250930-macm4pro-arm64-python-98a41af5b09343fa030e-3.15.0a0-98a41af-vs-3.13.0rc2.md)[📈](results/bm-20250930-3.15.0a0-98a41af/bm-20250930-macm4pro-arm64-python-98a41af5b09343fa030e-3.15.0a0-98a41af-vs-3.13.0rc2.svg) |  |
| [2025-09-29](results/bm-20250929-3.15.0a0-6b5f156-NOGIL) | python/6b5f15698a436591f7c3 | 6b5f156 (NOGIL) | 1.082x ↑<br>[📄](results/bm-20250929-3.15.0a0-6b5f156-NOGIL/bm-20250929-macm4pro-arm64-python-6b5f15698a436591f7c3-3.15.0a0-6b5f156-vs-3.12.6.md)[📈](results/bm-20250929-3.15.0a0-6b5f156-NOGIL/bm-20250929-macm4pro-arm64-python-6b5f15698a436591f7c3-3.15.0a0-6b5f156-vs-3.12.6.svg) | 1.004x ↑<br>[📄](results/bm-20250929-3.15.0a0-6b5f156-NOGIL/bm-20250929-macm4pro-arm64-python-6b5f15698a436591f7c3-3.15.0a0-6b5f156-vs-3.13.0rc2.md)[📈](results/bm-20250929-3.15.0a0-6b5f156-NOGIL/bm-20250929-macm4pro-arm64-python-6b5f15698a436591f7c3-3.15.0a0-6b5f156-vs-3.13.0rc2.svg) | 1.006x ↓<br>[📄](results/bm-20250929-3.15.0a0-6b5f156-NOGIL/bm-20250929-macm4pro-arm64-python-6b5f15698a436591f7c3-3.15.0a0-6b5f156-vs-base.md)[📈](results/bm-20250929-3.15.0a0-6b5f156-NOGIL/bm-20250929-macm4pro-arm64-python-6b5f15698a436591f7c3-3.15.0a0-6b5f156-vs-base.svg)[🧠](results/bm-20250929-3.15.0a0-6b5f156-NOGIL/bm-20250929-macm4pro-arm64-python-6b5f15698a436591f7c3-3.15.0a0-6b5f156-vs-base-mem.svg) |
| [2025-09-29](results/bm-20250929-3.15.0a0-6b5f156) | python/6b5f15698a436591f7c3 | 6b5f156 | 1.087x ↑<br>[📄](results/bm-20250929-3.15.0a0-6b5f156/bm-20250929-macm4pro-arm64-python-6b5f15698a436591f7c3-3.15.0a0-6b5f156-vs-3.12.6.md)[📈](results/bm-20250929-3.15.0a0-6b5f156/bm-20250929-macm4pro-arm64-python-6b5f15698a436591f7c3-3.15.0a0-6b5f156-vs-3.12.6.svg) | 1.008x ↑<br>[📄](results/bm-20250929-3.15.0a0-6b5f156/bm-20250929-macm4pro-arm64-python-6b5f15698a436591f7c3-3.15.0a0-6b5f156-vs-3.13.0rc2.md)[📈](results/bm-20250929-3.15.0a0-6b5f156/bm-20250929-macm4pro-arm64-python-6b5f15698a436591f7c3-3.15.0a0-6b5f156-vs-3.13.0rc2.svg) |  |


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
