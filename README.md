# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (e3287f6)](results/bm-20260815-3.16.0a0-e3287f6/bm-20260815-vultr-x86_64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (e3287f6)](results/bm-20260815-3.16.0a0-e3287f6-PYTHON_UOPS/bm-20260815-vultr-x86_64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-pystats.md)
- [Most recent JIT pystats on main (bedaea0)](results/bm-20251019-3.15.0a1%2B-bedaea0-JIT/bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-08-15](results/bm-20260815-3.16.0a0-e3287f6-NOGIL) | python/e3287f631f3c88ed8019 | e3287f6 (NOGIL) | 1.036x ↓<br>[📄](results/bm-20260815-3.16.0a0-e3287f6-NOGIL/bm-20260815-vultr-x86_64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-3.12.6.md)[📈](results/bm-20260815-3.16.0a0-e3287f6-NOGIL/bm-20260815-vultr-x86_64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-3.12.6.svg) | 1.068x ↓<br>[📄](results/bm-20260815-3.16.0a0-e3287f6-NOGIL/bm-20260815-vultr-x86_64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-3.13.0rc2.md)[📈](results/bm-20260815-3.16.0a0-e3287f6-NOGIL/bm-20260815-vultr-x86_64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-3.13.0rc2.svg) | 1.100x ↓<br>[📄](results/bm-20260815-3.16.0a0-e3287f6-NOGIL/bm-20260815-vultr-x86_64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-base.md)[📈](results/bm-20260815-3.16.0a0-e3287f6-NOGIL/bm-20260815-vultr-x86_64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-base.svg)[🧠](results/bm-20260815-3.16.0a0-e3287f6-NOGIL/bm-20260815-vultr-x86_64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-base-mem.svg) |
| [2026-08-15](results/bm-20260815-3.16.0a0-e3287f6-JIT) | python/e3287f631f3c88ed8019 | e3287f6 (JIT) | 1.164x ↑<br>[📄](results/bm-20260815-3.16.0a0-e3287f6-JIT/bm-20260815-vultr-x86_64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-3.12.6.md)[📈](results/bm-20260815-3.16.0a0-e3287f6-JIT/bm-20260815-vultr-x86_64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-3.12.6.svg) | 1.126x ↑<br>[📄](results/bm-20260815-3.16.0a0-e3287f6-JIT/bm-20260815-vultr-x86_64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-3.13.0rc2.md)[📈](results/bm-20260815-3.16.0a0-e3287f6-JIT/bm-20260815-vultr-x86_64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-3.13.0rc2.svg) | 1.083x ↑<br>[📄](results/bm-20260815-3.16.0a0-e3287f6-JIT/bm-20260815-vultr-x86_64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-base.md)[📈](results/bm-20260815-3.16.0a0-e3287f6-JIT/bm-20260815-vultr-x86_64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-base.svg)[🧠](results/bm-20260815-3.16.0a0-e3287f6-JIT/bm-20260815-vultr-x86_64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-base-mem.svg) |
| [2026-08-15](results/bm-20260815-3.16.0a0-e3287f6-CLANG) | python/e3287f631f3c88ed8019 | e3287f6 (CLANG) | 1.093x ↑<br>[📄](results/bm-20260815-3.16.0a0-e3287f6-CLANG/bm-20260815-vultr-x86_64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-3.12.6.md)[📈](results/bm-20260815-3.16.0a0-e3287f6-CLANG/bm-20260815-vultr-x86_64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-3.12.6.svg) | 1.057x ↑<br>[📄](results/bm-20260815-3.16.0a0-e3287f6-CLANG/bm-20260815-vultr-x86_64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-3.13.0rc2.md)[📈](results/bm-20260815-3.16.0a0-e3287f6-CLANG/bm-20260815-vultr-x86_64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-3.13.0rc2.svg) | 1.026x ↑<br>[📄](results/bm-20260815-3.16.0a0-e3287f6-CLANG/bm-20260815-vultr-x86_64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-base.md)[📈](results/bm-20260815-3.16.0a0-e3287f6-CLANG/bm-20260815-vultr-x86_64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-base.svg)[🧠](results/bm-20260815-3.16.0a0-e3287f6-CLANG/bm-20260815-vultr-x86_64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-base-mem.svg) |
| [2026-08-15](results/bm-20260815-3.16.0a0-e3287f6) | python/e3287f631f3c88ed8019 | e3287f6 | 1.067x ↑<br>[📄](results/bm-20260815-3.16.0a0-e3287f6/bm-20260815-vultr-x86_64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-3.12.6.md)[📈](results/bm-20260815-3.16.0a0-e3287f6/bm-20260815-vultr-x86_64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-3.12.6.svg) | 1.031x ↑<br>[📄](results/bm-20260815-3.16.0a0-e3287f6/bm-20260815-vultr-x86_64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-3.13.0rc2.md)[📈](results/bm-20260815-3.16.0a0-e3287f6/bm-20260815-vultr-x86_64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-3.13.0rc2.svg) |  |
| [2026-08-14](results/bm-20260814-3.16.0a0-dffac61-NOGIL) | python/dffac6163e693cf80ed4 | dffac61 (NOGIL) | 1.031x ↓<br>[📄](results/bm-20260814-3.16.0a0-dffac61-NOGIL/bm-20260814-vultr-x86_64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61-vs-3.12.6.md)[📈](results/bm-20260814-3.16.0a0-dffac61-NOGIL/bm-20260814-vultr-x86_64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61-vs-3.12.6.svg) | 1.063x ↓<br>[📄](results/bm-20260814-3.16.0a0-dffac61-NOGIL/bm-20260814-vultr-x86_64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61-vs-3.13.0rc2.md)[📈](results/bm-20260814-3.16.0a0-dffac61-NOGIL/bm-20260814-vultr-x86_64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61-vs-3.13.0rc2.svg) | 1.090x ↓<br>[📄](results/bm-20260814-3.16.0a0-dffac61-NOGIL/bm-20260814-vultr-x86_64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61-vs-base.md)[📈](results/bm-20260814-3.16.0a0-dffac61-NOGIL/bm-20260814-vultr-x86_64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61-vs-base.svg)[🧠](results/bm-20260814-3.16.0a0-dffac61-NOGIL/bm-20260814-vultr-x86_64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61-vs-base-mem.svg) |
| [2026-08-14](results/bm-20260814-3.16.0a0-dffac61) | python/dffac6163e693cf80ed4 | dffac61 | 1.059x ↑<br>[📄](results/bm-20260814-3.16.0a0-dffac61/bm-20260814-vultr-x86_64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61-vs-3.12.6.md)[📈](results/bm-20260814-3.16.0a0-dffac61/bm-20260814-vultr-x86_64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61-vs-3.12.6.svg) | 1.025x ↑<br>[📄](results/bm-20260814-3.16.0a0-dffac61/bm-20260814-vultr-x86_64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61-vs-3.13.0rc2.md)[📈](results/bm-20260814-3.16.0a0-dffac61/bm-20260814-vultr-x86_64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61-vs-3.13.0rc2.svg) |  |
| [2026-08-13](results/bm-20260813-3.16.0a0-46c355f-NOGIL) | python/46c355fabff5833b77f7 | 46c355f (NOGIL) | 1.039x ↓<br>[📄](results/bm-20260813-3.16.0a0-46c355f-NOGIL/bm-20260813-vultr-x86_64-python-46c355fabff5833b77f7-3.16.0a0-46c355f-vs-3.12.6.md)[📈](results/bm-20260813-3.16.0a0-46c355f-NOGIL/bm-20260813-vultr-x86_64-python-46c355fabff5833b77f7-3.16.0a0-46c355f-vs-3.12.6.svg) | 1.070x ↓<br>[📄](results/bm-20260813-3.16.0a0-46c355f-NOGIL/bm-20260813-vultr-x86_64-python-46c355fabff5833b77f7-3.16.0a0-46c355f-vs-3.13.0rc2.md)[📈](results/bm-20260813-3.16.0a0-46c355f-NOGIL/bm-20260813-vultr-x86_64-python-46c355fabff5833b77f7-3.16.0a0-46c355f-vs-3.13.0rc2.svg) | 1.107x ↓<br>[📄](results/bm-20260813-3.16.0a0-46c355f-NOGIL/bm-20260813-vultr-x86_64-python-46c355fabff5833b77f7-3.16.0a0-46c355f-vs-base.md)[📈](results/bm-20260813-3.16.0a0-46c355f-NOGIL/bm-20260813-vultr-x86_64-python-46c355fabff5833b77f7-3.16.0a0-46c355f-vs-base.svg)[🧠](results/bm-20260813-3.16.0a0-46c355f-NOGIL/bm-20260813-vultr-x86_64-python-46c355fabff5833b77f7-3.16.0a0-46c355f-vs-base-mem.svg) |
| [2026-08-13](results/bm-20260813-3.16.0a0-46c355f) | python/46c355fabff5833b77f7 | 46c355f | 1.072x ↑<br>[📄](results/bm-20260813-3.16.0a0-46c355f/bm-20260813-vultr-x86_64-python-46c355fabff5833b77f7-3.16.0a0-46c355f-vs-3.12.6.md)[📈](results/bm-20260813-3.16.0a0-46c355f/bm-20260813-vultr-x86_64-python-46c355fabff5833b77f7-3.16.0a0-46c355f-vs-3.12.6.svg) | 1.036x ↑<br>[📄](results/bm-20260813-3.16.0a0-46c355f/bm-20260813-vultr-x86_64-python-46c355fabff5833b77f7-3.16.0a0-46c355f-vs-3.13.0rc2.md)[📈](results/bm-20260813-3.16.0a0-46c355f/bm-20260813-vultr-x86_64-python-46c355fabff5833b77f7-3.16.0a0-46c355f-vs-3.13.0rc2.svg) |  |
| [2026-08-13](results/bm-20260813-3.16.0a0-ee4fe00-NOGIL) | python/ee4fe00a8f72ea84a421 | ee4fe00 (NOGIL) | 1.037x ↓<br>[📄](results/bm-20260813-3.16.0a0-ee4fe00-NOGIL/bm-20260813-vultr-x86_64-python-ee4fe00a8f72ea84a421-3.16.0a0-ee4fe00-vs-3.12.6.md)[📈](results/bm-20260813-3.16.0a0-ee4fe00-NOGIL/bm-20260813-vultr-x86_64-python-ee4fe00a8f72ea84a421-3.16.0a0-ee4fe00-vs-3.12.6.svg) | 1.069x ↓<br>[📄](results/bm-20260813-3.16.0a0-ee4fe00-NOGIL/bm-20260813-vultr-x86_64-python-ee4fe00a8f72ea84a421-3.16.0a0-ee4fe00-vs-3.13.0rc2.md)[📈](results/bm-20260813-3.16.0a0-ee4fe00-NOGIL/bm-20260813-vultr-x86_64-python-ee4fe00a8f72ea84a421-3.16.0a0-ee4fe00-vs-3.13.0rc2.svg) | 1.099x ↓<br>[📄](results/bm-20260813-3.16.0a0-ee4fe00-NOGIL/bm-20260813-vultr-x86_64-python-ee4fe00a8f72ea84a421-3.16.0a0-ee4fe00-vs-base.md)[📈](results/bm-20260813-3.16.0a0-ee4fe00-NOGIL/bm-20260813-vultr-x86_64-python-ee4fe00a8f72ea84a421-3.16.0a0-ee4fe00-vs-base.svg)[🧠](results/bm-20260813-3.16.0a0-ee4fe00-NOGIL/bm-20260813-vultr-x86_64-python-ee4fe00a8f72ea84a421-3.16.0a0-ee4fe00-vs-base-mem.svg) |
| [2026-08-13](results/bm-20260813-3.16.0a0-ee4fe00) | python/ee4fe00a8f72ea84a421 | ee4fe00 | 1.065x ↑<br>[📄](results/bm-20260813-3.16.0a0-ee4fe00/bm-20260813-vultr-x86_64-python-ee4fe00a8f72ea84a421-3.16.0a0-ee4fe00-vs-3.12.6.md)[📈](results/bm-20260813-3.16.0a0-ee4fe00/bm-20260813-vultr-x86_64-python-ee4fe00a8f72ea84a421-3.16.0a0-ee4fe00-vs-3.12.6.svg) | 1.030x ↑<br>[📄](results/bm-20260813-3.16.0a0-ee4fe00/bm-20260813-vultr-x86_64-python-ee4fe00a8f72ea84a421-3.16.0a0-ee4fe00-vs-3.13.0rc2.md)[📈](results/bm-20260813-3.16.0a0-ee4fe00/bm-20260813-vultr-x86_64-python-ee4fe00a8f72ea84a421-3.16.0a0-ee4fe00-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-08-15](results/bm-20260815-3.16.0a0-e3287f6-NOGIL) | python/e3287f631f3c88ed8019 | e3287f6 (NOGIL) | 1.017x ↑<br>[📄](results/bm-20260815-3.16.0a0-e3287f6-NOGIL/bm-20260815-macm4pro-arm64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-3.12.6.md)[📈](results/bm-20260815-3.16.0a0-e3287f6-NOGIL/bm-20260815-macm4pro-arm64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-3.12.6.svg) | 1.058x ↓<br>[📄](results/bm-20260815-3.16.0a0-e3287f6-NOGIL/bm-20260815-macm4pro-arm64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-3.13.0rc2.md)[📈](results/bm-20260815-3.16.0a0-e3287f6-NOGIL/bm-20260815-macm4pro-arm64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-3.13.0rc2.svg) | 1.097x ↓<br>[📄](results/bm-20260815-3.16.0a0-e3287f6-NOGIL/bm-20260815-macm4pro-arm64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-base.md)[📈](results/bm-20260815-3.16.0a0-e3287f6-NOGIL/bm-20260815-macm4pro-arm64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-base.svg)[🧠](results/bm-20260815-3.16.0a0-e3287f6-NOGIL/bm-20260815-macm4pro-arm64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-base-mem.svg) |
| [2026-08-15](results/bm-20260815-3.16.0a0-e3287f6-JIT) | python/e3287f631f3c88ed8019 | e3287f6 (JIT) | 1.257x ↑<br>[📄](results/bm-20260815-3.16.0a0-e3287f6-JIT/bm-20260815-macm4pro-arm64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-3.12.6.md)[📈](results/bm-20260815-3.16.0a0-e3287f6-JIT/bm-20260815-macm4pro-arm64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-3.12.6.svg) | 1.162x ↑<br>[📄](results/bm-20260815-3.16.0a0-e3287f6-JIT/bm-20260815-macm4pro-arm64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-3.13.0rc2.md)[📈](results/bm-20260815-3.16.0a0-e3287f6-JIT/bm-20260815-macm4pro-arm64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-3.13.0rc2.svg) | 1.116x ↑<br>[📄](results/bm-20260815-3.16.0a0-e3287f6-JIT/bm-20260815-macm4pro-arm64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-base.md)[📈](results/bm-20260815-3.16.0a0-e3287f6-JIT/bm-20260815-macm4pro-arm64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-base.svg)[🧠](results/bm-20260815-3.16.0a0-e3287f6-JIT/bm-20260815-macm4pro-arm64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-base-mem.svg) |
| [2026-08-15](results/bm-20260815-3.16.0a0-e3287f6-CLANG) | python/e3287f631f3c88ed8019 | e3287f6 (CLANG) | 1.143x ↑<br>[📄](results/bm-20260815-3.16.0a0-e3287f6-CLANG/bm-20260815-macm4pro-arm64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-3.12.6.md)[📈](results/bm-20260815-3.16.0a0-e3287f6-CLANG/bm-20260815-macm4pro-arm64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-3.12.6.svg) | 1.056x ↑<br>[📄](results/bm-20260815-3.16.0a0-e3287f6-CLANG/bm-20260815-macm4pro-arm64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-3.13.0rc2.md)[📈](results/bm-20260815-3.16.0a0-e3287f6-CLANG/bm-20260815-macm4pro-arm64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-3.13.0rc2.svg) | 1.014x ↑<br>[📄](results/bm-20260815-3.16.0a0-e3287f6-CLANG/bm-20260815-macm4pro-arm64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-base.md)[📈](results/bm-20260815-3.16.0a0-e3287f6-CLANG/bm-20260815-macm4pro-arm64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-base.svg)[🧠](results/bm-20260815-3.16.0a0-e3287f6-CLANG/bm-20260815-macm4pro-arm64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-base-mem.svg) |
| [2026-08-15](results/bm-20260815-3.16.0a0-e3287f6) | python/e3287f631f3c88ed8019 | e3287f6 | 1.128x ↑<br>[📄](results/bm-20260815-3.16.0a0-e3287f6/bm-20260815-macm4pro-arm64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-3.12.6.md)[📈](results/bm-20260815-3.16.0a0-e3287f6/bm-20260815-macm4pro-arm64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-3.12.6.svg) | 1.041x ↑<br>[📄](results/bm-20260815-3.16.0a0-e3287f6/bm-20260815-macm4pro-arm64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-3.13.0rc2.md)[📈](results/bm-20260815-3.16.0a0-e3287f6/bm-20260815-macm4pro-arm64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-vs-3.13.0rc2.svg) |  |
| [2026-08-14](results/bm-20260814-3.16.0a0-dffac61-NOGIL) | python/dffac6163e693cf80ed4 | dffac61 (NOGIL) | 1.007x ↑<br>[📄](results/bm-20260814-3.16.0a0-dffac61-NOGIL/bm-20260814-macm4pro-arm64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61-vs-3.12.6.md)[📈](results/bm-20260814-3.16.0a0-dffac61-NOGIL/bm-20260814-macm4pro-arm64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61-vs-3.12.6.svg) | 1.067x ↓<br>[📄](results/bm-20260814-3.16.0a0-dffac61-NOGIL/bm-20260814-macm4pro-arm64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61-vs-3.13.0rc2.md)[📈](results/bm-20260814-3.16.0a0-dffac61-NOGIL/bm-20260814-macm4pro-arm64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61-vs-3.13.0rc2.svg) | 1.104x ↓<br>[📄](results/bm-20260814-3.16.0a0-dffac61-NOGIL/bm-20260814-macm4pro-arm64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61-vs-base.md)[📈](results/bm-20260814-3.16.0a0-dffac61-NOGIL/bm-20260814-macm4pro-arm64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61-vs-base.svg)[🧠](results/bm-20260814-3.16.0a0-dffac61-NOGIL/bm-20260814-macm4pro-arm64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61-vs-base-mem.svg) |
| [2026-08-14](results/bm-20260814-3.16.0a0-dffac61) | python/dffac6163e693cf80ed4 | dffac61 | 1.126x ↑<br>[📄](results/bm-20260814-3.16.0a0-dffac61/bm-20260814-macm4pro-arm64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61-vs-3.12.6.md)[📈](results/bm-20260814-3.16.0a0-dffac61/bm-20260814-macm4pro-arm64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61-vs-3.12.6.svg) | 1.040x ↑<br>[📄](results/bm-20260814-3.16.0a0-dffac61/bm-20260814-macm4pro-arm64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61-vs-3.13.0rc2.md)[📈](results/bm-20260814-3.16.0a0-dffac61/bm-20260814-macm4pro-arm64-python-dffac6163e693cf80ed4-3.16.0a0-dffac61-vs-3.13.0rc2.svg) |  |


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
