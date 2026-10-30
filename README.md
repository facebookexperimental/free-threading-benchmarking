# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (7159b15)](results/bm-20261024-3.16.0a1%2Bdev-7159b15/bm-20261024-vultr-x86_64-python-7159b152a0b6205941ad-3.16.0a1%2Bdev-7159b15-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (7159b15)](results/bm-20261024-3.16.0a1%2Bdev-7159b15-PYTHON_UOPS/bm-20261024-vultr-x86_64-python-7159b152a0b6205941ad-3.16.0a1%2Bdev-7159b15-pystats.md)
- [Most recent JIT pystats on main (bedaea0)](results/bm-20251019-3.15.0a1%2B-bedaea0-JIT/bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-10-29](results/bm-20261029-3.16.0a1%2Bdev-ef1fce0-NOGIL) | python/ef1fce0a69a19360643f | ef1fce0 (NOGIL) | 1.039x ↓<br>[📄](results/bm-20261029-3.16.0a1%2Bdev-ef1fce0-NOGIL/bm-20261029-vultr-x86_64-python-ef1fce0a69a19360643f-3.16.0a1%2Bdev-ef1fce0-vs-3.12.6.md)[📈](results/bm-20261029-3.16.0a1%2Bdev-ef1fce0-NOGIL/bm-20261029-vultr-x86_64-python-ef1fce0a69a19360643f-3.16.0a1%2Bdev-ef1fce0-vs-3.12.6.svg) | 1.071x ↓<br>[📄](results/bm-20261029-3.16.0a1%2Bdev-ef1fce0-NOGIL/bm-20261029-vultr-x86_64-python-ef1fce0a69a19360643f-3.16.0a1%2Bdev-ef1fce0-vs-3.13.0rc2.md)[📈](results/bm-20261029-3.16.0a1%2Bdev-ef1fce0-NOGIL/bm-20261029-vultr-x86_64-python-ef1fce0a69a19360643f-3.16.0a1%2Bdev-ef1fce0-vs-3.13.0rc2.svg) | 1.120x ↓<br>[📄](results/bm-20261029-3.16.0a1%2Bdev-ef1fce0-NOGIL/bm-20261029-vultr-x86_64-python-ef1fce0a69a19360643f-3.16.0a1%2Bdev-ef1fce0-vs-base.md)[📈](results/bm-20261029-3.16.0a1%2Bdev-ef1fce0-NOGIL/bm-20261029-vultr-x86_64-python-ef1fce0a69a19360643f-3.16.0a1%2Bdev-ef1fce0-vs-base.svg)[🧠](results/bm-20261029-3.16.0a1%2Bdev-ef1fce0-NOGIL/bm-20261029-vultr-x86_64-python-ef1fce0a69a19360643f-3.16.0a1%2Bdev-ef1fce0-vs-base-mem.svg) |
| [2026-10-29](results/bm-20261029-3.16.0a1%2Bdev-ef1fce0) | python/ef1fce0a69a19360643f | ef1fce0 | 1.088x ↑<br>[📄](results/bm-20261029-3.16.0a1%2Bdev-ef1fce0/bm-20261029-vultr-x86_64-python-ef1fce0a69a19360643f-3.16.0a1%2Bdev-ef1fce0-vs-3.12.6.md)[📈](results/bm-20261029-3.16.0a1%2Bdev-ef1fce0/bm-20261029-vultr-x86_64-python-ef1fce0a69a19360643f-3.16.0a1%2Bdev-ef1fce0-vs-3.12.6.svg) | 1.052x ↑<br>[📄](results/bm-20261029-3.16.0a1%2Bdev-ef1fce0/bm-20261029-vultr-x86_64-python-ef1fce0a69a19360643f-3.16.0a1%2Bdev-ef1fce0-vs-3.13.0rc2.md)[📈](results/bm-20261029-3.16.0a1%2Bdev-ef1fce0/bm-20261029-vultr-x86_64-python-ef1fce0a69a19360643f-3.16.0a1%2Bdev-ef1fce0-vs-3.13.0rc2.svg) |  |
| [2026-10-28](results/bm-20261028-3.16.0a1%2Bdev-f7c39d2-NOGIL) | python/f7c39d2316e59f17148d | f7c39d2 (NOGIL) | 1.032x ↓<br>[📄](results/bm-20261028-3.16.0a1%2Bdev-f7c39d2-NOGIL/bm-20261028-vultr-x86_64-python-f7c39d2316e59f17148d-3.16.0a1%2Bdev-f7c39d2-vs-3.12.6.md)[📈](results/bm-20261028-3.16.0a1%2Bdev-f7c39d2-NOGIL/bm-20261028-vultr-x86_64-python-f7c39d2316e59f17148d-3.16.0a1%2Bdev-f7c39d2-vs-3.12.6.svg) | 1.064x ↓<br>[📄](results/bm-20261028-3.16.0a1%2Bdev-f7c39d2-NOGIL/bm-20261028-vultr-x86_64-python-f7c39d2316e59f17148d-3.16.0a1%2Bdev-f7c39d2-vs-3.13.0rc2.md)[📈](results/bm-20261028-3.16.0a1%2Bdev-f7c39d2-NOGIL/bm-20261028-vultr-x86_64-python-f7c39d2316e59f17148d-3.16.0a1%2Bdev-f7c39d2-vs-3.13.0rc2.svg) | 1.117x ↓<br>[📄](results/bm-20261028-3.16.0a1%2Bdev-f7c39d2-NOGIL/bm-20261028-vultr-x86_64-python-f7c39d2316e59f17148d-3.16.0a1%2Bdev-f7c39d2-vs-base.md)[📈](results/bm-20261028-3.16.0a1%2Bdev-f7c39d2-NOGIL/bm-20261028-vultr-x86_64-python-f7c39d2316e59f17148d-3.16.0a1%2Bdev-f7c39d2-vs-base.svg)[🧠](results/bm-20261028-3.16.0a1%2Bdev-f7c39d2-NOGIL/bm-20261028-vultr-x86_64-python-f7c39d2316e59f17148d-3.16.0a1%2Bdev-f7c39d2-vs-base-mem.svg) |
| [2026-10-28](results/bm-20261028-3.16.0a1%2Bdev-f7c39d2) | python/f7c39d2316e59f17148d | f7c39d2 | 1.092x ↑<br>[📄](results/bm-20261028-3.16.0a1%2Bdev-f7c39d2/bm-20261028-vultr-x86_64-python-f7c39d2316e59f17148d-3.16.0a1%2Bdev-f7c39d2-vs-3.12.6.md)[📈](results/bm-20261028-3.16.0a1%2Bdev-f7c39d2/bm-20261028-vultr-x86_64-python-f7c39d2316e59f17148d-3.16.0a1%2Bdev-f7c39d2-vs-3.12.6.svg) | 1.056x ↑<br>[📄](results/bm-20261028-3.16.0a1%2Bdev-f7c39d2/bm-20261028-vultr-x86_64-python-f7c39d2316e59f17148d-3.16.0a1%2Bdev-f7c39d2-vs-3.13.0rc2.md)[📈](results/bm-20261028-3.16.0a1%2Bdev-f7c39d2/bm-20261028-vultr-x86_64-python-f7c39d2316e59f17148d-3.16.0a1%2Bdev-f7c39d2-vs-3.13.0rc2.svg) |  |
| [2026-10-27](results/bm-20261027-3.16.0a1%2Bdev-6c695bf-NOGIL) | python/6c695bfad45ddde73d0d | 6c695bf (NOGIL) | 1.033x ↓<br>[📄](results/bm-20261027-3.16.0a1%2Bdev-6c695bf-NOGIL/bm-20261027-vultr-x86_64-python-6c695bfad45ddde73d0d-3.16.0a1%2Bdev-6c695bf-vs-3.12.6.md)[📈](results/bm-20261027-3.16.0a1%2Bdev-6c695bf-NOGIL/bm-20261027-vultr-x86_64-python-6c695bfad45ddde73d0d-3.16.0a1%2Bdev-6c695bf-vs-3.12.6.svg) | 1.065x ↓<br>[📄](results/bm-20261027-3.16.0a1%2Bdev-6c695bf-NOGIL/bm-20261027-vultr-x86_64-python-6c695bfad45ddde73d0d-3.16.0a1%2Bdev-6c695bf-vs-3.13.0rc2.md)[📈](results/bm-20261027-3.16.0a1%2Bdev-6c695bf-NOGIL/bm-20261027-vultr-x86_64-python-6c695bfad45ddde73d0d-3.16.0a1%2Bdev-6c695bf-vs-3.13.0rc2.svg) | 1.115x ↓<br>[📄](results/bm-20261027-3.16.0a1%2Bdev-6c695bf-NOGIL/bm-20261027-vultr-x86_64-python-6c695bfad45ddde73d0d-3.16.0a1%2Bdev-6c695bf-vs-base.md)[📈](results/bm-20261027-3.16.0a1%2Bdev-6c695bf-NOGIL/bm-20261027-vultr-x86_64-python-6c695bfad45ddde73d0d-3.16.0a1%2Bdev-6c695bf-vs-base.svg)[🧠](results/bm-20261027-3.16.0a1%2Bdev-6c695bf-NOGIL/bm-20261027-vultr-x86_64-python-6c695bfad45ddde73d0d-3.16.0a1%2Bdev-6c695bf-vs-base-mem.svg) |
| [2026-10-27](results/bm-20261027-3.16.0a1%2Bdev-6c695bf) | python/6c695bfad45ddde73d0d | 6c695bf | 1.090x ↑<br>[📄](results/bm-20261027-3.16.0a1%2Bdev-6c695bf/bm-20261027-vultr-x86_64-python-6c695bfad45ddde73d0d-3.16.0a1%2Bdev-6c695bf-vs-3.12.6.md)[📈](results/bm-20261027-3.16.0a1%2Bdev-6c695bf/bm-20261027-vultr-x86_64-python-6c695bfad45ddde73d0d-3.16.0a1%2Bdev-6c695bf-vs-3.12.6.svg) | 1.054x ↑<br>[📄](results/bm-20261027-3.16.0a1%2Bdev-6c695bf/bm-20261027-vultr-x86_64-python-6c695bfad45ddde73d0d-3.16.0a1%2Bdev-6c695bf-vs-3.13.0rc2.md)[📈](results/bm-20261027-3.16.0a1%2Bdev-6c695bf/bm-20261027-vultr-x86_64-python-6c695bfad45ddde73d0d-3.16.0a1%2Bdev-6c695bf-vs-3.13.0rc2.svg) |  |
| [2026-10-26](results/bm-20261026-3.16.0a1%2Bdev-0e35313-NOGIL) | python/0e353134844fd50628f3 | 0e35313 (NOGIL) | 1.033x ↓<br>[📄](results/bm-20261026-3.16.0a1%2Bdev-0e35313-NOGIL/bm-20261026-vultr-x86_64-python-0e353134844fd50628f3-3.16.0a1%2Bdev-0e35313-vs-3.12.6.md)[📈](results/bm-20261026-3.16.0a1%2Bdev-0e35313-NOGIL/bm-20261026-vultr-x86_64-python-0e353134844fd50628f3-3.16.0a1%2Bdev-0e35313-vs-3.12.6.svg) | 1.066x ↓<br>[📄](results/bm-20261026-3.16.0a1%2Bdev-0e35313-NOGIL/bm-20261026-vultr-x86_64-python-0e353134844fd50628f3-3.16.0a1%2Bdev-0e35313-vs-3.13.0rc2.md)[📈](results/bm-20261026-3.16.0a1%2Bdev-0e35313-NOGIL/bm-20261026-vultr-x86_64-python-0e353134844fd50628f3-3.16.0a1%2Bdev-0e35313-vs-3.13.0rc2.svg) | 1.117x ↓<br>[📄](results/bm-20261026-3.16.0a1%2Bdev-0e35313-NOGIL/bm-20261026-vultr-x86_64-python-0e353134844fd50628f3-3.16.0a1%2Bdev-0e35313-vs-base.md)[📈](results/bm-20261026-3.16.0a1%2Bdev-0e35313-NOGIL/bm-20261026-vultr-x86_64-python-0e353134844fd50628f3-3.16.0a1%2Bdev-0e35313-vs-base.svg)[🧠](results/bm-20261026-3.16.0a1%2Bdev-0e35313-NOGIL/bm-20261026-vultr-x86_64-python-0e353134844fd50628f3-3.16.0a1%2Bdev-0e35313-vs-base-mem.svg) |
| [2026-10-26](results/bm-20261026-3.16.0a1%2Bdev-0e35313) | python/0e353134844fd50628f3 | 0e35313 | 1.092x ↑<br>[📄](results/bm-20261026-3.16.0a1%2Bdev-0e35313/bm-20261026-vultr-x86_64-python-0e353134844fd50628f3-3.16.0a1%2Bdev-0e35313-vs-3.12.6.md)[📈](results/bm-20261026-3.16.0a1%2Bdev-0e35313/bm-20261026-vultr-x86_64-python-0e353134844fd50628f3-3.16.0a1%2Bdev-0e35313-vs-3.12.6.svg) | 1.054x ↑<br>[📄](results/bm-20261026-3.16.0a1%2Bdev-0e35313/bm-20261026-vultr-x86_64-python-0e353134844fd50628f3-3.16.0a1%2Bdev-0e35313-vs-3.13.0rc2.md)[📈](results/bm-20261026-3.16.0a1%2Bdev-0e35313/bm-20261026-vultr-x86_64-python-0e353134844fd50628f3-3.16.0a1%2Bdev-0e35313-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-10-29](results/bm-20261029-3.16.0a1%2Bdev-ef1fce0-NOGIL) | python/ef1fce0a69a19360643f | ef1fce0 (NOGIL) | 1.090x ↑<br>[📄](results/bm-20261029-3.16.0a1%2Bdev-ef1fce0-NOGIL/bm-20261029-macm4pro-arm64-python-ef1fce0a69a19360643f-3.16.0a1%2Bdev-ef1fce0-vs-3.12.6.md)[📈](results/bm-20261029-3.16.0a1%2Bdev-ef1fce0-NOGIL/bm-20261029-macm4pro-arm64-python-ef1fce0a69a19360643f-3.16.0a1%2Bdev-ef1fce0-vs-3.12.6.svg) | 1.010x ↑<br>[📄](results/bm-20261029-3.16.0a1%2Bdev-ef1fce0-NOGIL/bm-20261029-macm4pro-arm64-python-ef1fce0a69a19360643f-3.16.0a1%2Bdev-ef1fce0-vs-3.13.0rc2.md)[📈](results/bm-20261029-3.16.0a1%2Bdev-ef1fce0-NOGIL/bm-20261029-macm4pro-arm64-python-ef1fce0a69a19360643f-3.16.0a1%2Bdev-ef1fce0-vs-3.13.0rc2.svg) | 1.091x ↓<br>[📄](results/bm-20261029-3.16.0a1%2Bdev-ef1fce0-NOGIL/bm-20261029-macm4pro-arm64-python-ef1fce0a69a19360643f-3.16.0a1%2Bdev-ef1fce0-vs-base.md)[📈](results/bm-20261029-3.16.0a1%2Bdev-ef1fce0-NOGIL/bm-20261029-macm4pro-arm64-python-ef1fce0a69a19360643f-3.16.0a1%2Bdev-ef1fce0-vs-base.svg)[🧠](results/bm-20261029-3.16.0a1%2Bdev-ef1fce0-NOGIL/bm-20261029-macm4pro-arm64-python-ef1fce0a69a19360643f-3.16.0a1%2Bdev-ef1fce0-vs-base-mem.svg) |
| [2026-10-29](results/bm-20261029-3.16.0a1%2Bdev-ef1fce0) | python/ef1fce0a69a19360643f | ef1fce0 | 1.203x ↑<br>[📄](results/bm-20261029-3.16.0a1%2Bdev-ef1fce0/bm-20261029-macm4pro-arm64-python-ef1fce0a69a19360643f-3.16.0a1%2Bdev-ef1fce0-vs-3.12.6.md)[📈](results/bm-20261029-3.16.0a1%2Bdev-ef1fce0/bm-20261029-macm4pro-arm64-python-ef1fce0a69a19360643f-3.16.0a1%2Bdev-ef1fce0-vs-3.12.6.svg) | 1.112x ↑<br>[📄](results/bm-20261029-3.16.0a1%2Bdev-ef1fce0/bm-20261029-macm4pro-arm64-python-ef1fce0a69a19360643f-3.16.0a1%2Bdev-ef1fce0-vs-3.13.0rc2.md)[📈](results/bm-20261029-3.16.0a1%2Bdev-ef1fce0/bm-20261029-macm4pro-arm64-python-ef1fce0a69a19360643f-3.16.0a1%2Bdev-ef1fce0-vs-3.13.0rc2.svg) |  |
| [2026-10-28](results/bm-20261028-3.16.0a1%2Bdev-f7c39d2-NOGIL) | python/f7c39d2316e59f17148d | f7c39d2 (NOGIL) | 1.079x ↑<br>[📄](results/bm-20261028-3.16.0a1%2Bdev-f7c39d2-NOGIL/bm-20261028-macm4pro-arm64-python-f7c39d2316e59f17148d-3.16.0a1%2Bdev-f7c39d2-vs-3.12.6.md)[📈](results/bm-20261028-3.16.0a1%2Bdev-f7c39d2-NOGIL/bm-20261028-macm4pro-arm64-python-f7c39d2316e59f17148d-3.16.0a1%2Bdev-f7c39d2-vs-3.12.6.svg) | 1.001x ↓<br>[📄](results/bm-20261028-3.16.0a1%2Bdev-f7c39d2-NOGIL/bm-20261028-macm4pro-arm64-python-f7c39d2316e59f17148d-3.16.0a1%2Bdev-f7c39d2-vs-3.13.0rc2.md)[📈](results/bm-20261028-3.16.0a1%2Bdev-f7c39d2-NOGIL/bm-20261028-macm4pro-arm64-python-f7c39d2316e59f17148d-3.16.0a1%2Bdev-f7c39d2-vs-3.13.0rc2.svg) | 1.105x ↓<br>[📄](results/bm-20261028-3.16.0a1%2Bdev-f7c39d2-NOGIL/bm-20261028-macm4pro-arm64-python-f7c39d2316e59f17148d-3.16.0a1%2Bdev-f7c39d2-vs-base.md)[📈](results/bm-20261028-3.16.0a1%2Bdev-f7c39d2-NOGIL/bm-20261028-macm4pro-arm64-python-f7c39d2316e59f17148d-3.16.0a1%2Bdev-f7c39d2-vs-base.svg)[🧠](results/bm-20261028-3.16.0a1%2Bdev-f7c39d2-NOGIL/bm-20261028-macm4pro-arm64-python-f7c39d2316e59f17148d-3.16.0a1%2Bdev-f7c39d2-vs-base-mem.svg) |
| [2026-10-28](results/bm-20261028-3.16.0a1%2Bdev-f7c39d2) | python/f7c39d2316e59f17148d | f7c39d2 | 1.211x ↑<br>[📄](results/bm-20261028-3.16.0a1%2Bdev-f7c39d2/bm-20261028-macm4pro-arm64-python-f7c39d2316e59f17148d-3.16.0a1%2Bdev-f7c39d2-vs-3.12.6.md)[📈](results/bm-20261028-3.16.0a1%2Bdev-f7c39d2/bm-20261028-macm4pro-arm64-python-f7c39d2316e59f17148d-3.16.0a1%2Bdev-f7c39d2-vs-3.12.6.svg) | 1.119x ↑<br>[📄](results/bm-20261028-3.16.0a1%2Bdev-f7c39d2/bm-20261028-macm4pro-arm64-python-f7c39d2316e59f17148d-3.16.0a1%2Bdev-f7c39d2-vs-3.13.0rc2.md)[📈](results/bm-20261028-3.16.0a1%2Bdev-f7c39d2/bm-20261028-macm4pro-arm64-python-f7c39d2316e59f17148d-3.16.0a1%2Bdev-f7c39d2-vs-3.13.0rc2.svg) |  |
| [2026-10-27](results/bm-20261027-3.16.0a1%2Bdev-6c695bf-NOGIL) | python/6c695bfad45ddde73d0d | 6c695bf (NOGIL) | 1.077x ↑<br>[📄](results/bm-20261027-3.16.0a1%2Bdev-6c695bf-NOGIL/bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1%2Bdev-6c695bf-vs-3.12.6.md)[📈](results/bm-20261027-3.16.0a1%2Bdev-6c695bf-NOGIL/bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1%2Bdev-6c695bf-vs-3.12.6.svg) | 1.002x ↓<br>[📄](results/bm-20261027-3.16.0a1%2Bdev-6c695bf-NOGIL/bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1%2Bdev-6c695bf-vs-3.13.0rc2.md)[📈](results/bm-20261027-3.16.0a1%2Bdev-6c695bf-NOGIL/bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1%2Bdev-6c695bf-vs-3.13.0rc2.svg) | 1.107x ↓<br>[📄](results/bm-20261027-3.16.0a1%2Bdev-6c695bf-NOGIL/bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1%2Bdev-6c695bf-vs-base.md)[📈](results/bm-20261027-3.16.0a1%2Bdev-6c695bf-NOGIL/bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1%2Bdev-6c695bf-vs-base.svg)[🧠](results/bm-20261027-3.16.0a1%2Bdev-6c695bf-NOGIL/bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1%2Bdev-6c695bf-vs-base-mem.svg) |
| [2026-10-27](results/bm-20261027-3.16.0a1%2Bdev-6c695bf) | python/6c695bfad45ddde73d0d | 6c695bf | 1.212x ↑<br>[📄](results/bm-20261027-3.16.0a1%2Bdev-6c695bf/bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1%2Bdev-6c695bf-vs-3.12.6.md)[📈](results/bm-20261027-3.16.0a1%2Bdev-6c695bf/bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1%2Bdev-6c695bf-vs-3.12.6.svg) | 1.120x ↑<br>[📄](results/bm-20261027-3.16.0a1%2Bdev-6c695bf/bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1%2Bdev-6c695bf-vs-3.13.0rc2.md)[📈](results/bm-20261027-3.16.0a1%2Bdev-6c695bf/bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1%2Bdev-6c695bf-vs-3.13.0rc2.svg) |  |
| [2026-10-26](results/bm-20261026-3.16.0a1%2Bdev-0e35313-NOGIL) | python/0e353134844fd50628f3 | 0e35313 (NOGIL) | 1.084x ↑<br>[📄](results/bm-20261026-3.16.0a1%2Bdev-0e35313-NOGIL/bm-20261026-macm4pro-arm64-python-0e353134844fd50628f3-3.16.0a1%2Bdev-0e35313-vs-3.12.6.md)[📈](results/bm-20261026-3.16.0a1%2Bdev-0e35313-NOGIL/bm-20261026-macm4pro-arm64-python-0e353134844fd50628f3-3.16.0a1%2Bdev-0e35313-vs-3.12.6.svg) | 1.004x ↑<br>[📄](results/bm-20261026-3.16.0a1%2Bdev-0e35313-NOGIL/bm-20261026-macm4pro-arm64-python-0e353134844fd50628f3-3.16.0a1%2Bdev-0e35313-vs-3.13.0rc2.md)[📈](results/bm-20261026-3.16.0a1%2Bdev-0e35313-NOGIL/bm-20261026-macm4pro-arm64-python-0e353134844fd50628f3-3.16.0a1%2Bdev-0e35313-vs-3.13.0rc2.svg) | 1.096x ↓<br>[📄](results/bm-20261026-3.16.0a1%2Bdev-0e35313-NOGIL/bm-20261026-macm4pro-arm64-python-0e353134844fd50628f3-3.16.0a1%2Bdev-0e35313-vs-base.md)[📈](results/bm-20261026-3.16.0a1%2Bdev-0e35313-NOGIL/bm-20261026-macm4pro-arm64-python-0e353134844fd50628f3-3.16.0a1%2Bdev-0e35313-vs-base.svg)[🧠](results/bm-20261026-3.16.0a1%2Bdev-0e35313-NOGIL/bm-20261026-macm4pro-arm64-python-0e353134844fd50628f3-3.16.0a1%2Bdev-0e35313-vs-base-mem.svg) |
| [2026-10-26](results/bm-20261026-3.16.0a1%2Bdev-0e35313) | python/0e353134844fd50628f3 | 0e35313 | 1.205x ↑<br>[📄](results/bm-20261026-3.16.0a1%2Bdev-0e35313/bm-20261026-macm4pro-arm64-python-0e353134844fd50628f3-3.16.0a1%2Bdev-0e35313-vs-3.12.6.md)[📈](results/bm-20261026-3.16.0a1%2Bdev-0e35313/bm-20261026-macm4pro-arm64-python-0e353134844fd50628f3-3.16.0a1%2Bdev-0e35313-vs-3.12.6.svg) | 1.113x ↑<br>[📄](results/bm-20261026-3.16.0a1%2Bdev-0e35313/bm-20261026-macm4pro-arm64-python-0e353134844fd50628f3-3.16.0a1%2Bdev-0e35313-vs-3.13.0rc2.md)[📈](results/bm-20261026-3.16.0a1%2Bdev-0e35313/bm-20261026-macm4pro-arm64-python-0e353134844fd50628f3-3.16.0a1%2Bdev-0e35313-vs-3.13.0rc2.svg) |  |


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
