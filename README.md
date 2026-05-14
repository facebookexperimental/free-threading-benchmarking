# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (cc5cf14)](results/bm-20260509-3.16.0a0-cc5cf14/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (cc5cf14)](results/bm-20260509-3.16.0a0-cc5cf14-PYTHON_UOPS/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14-pystats.md)
- [Most recent JIT pystats on main (bedaea0)](results/bm-20251019-3.15.0a1%2B-bedaea0-JIT/bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-05-14](results/bm-20260514-3.16.0a0-f1a47e7-NOGIL) | python/f1a47e79fb7081d3cde6 | f1a47e7 (NOGIL) | 1.039x ↓<br>[📄](results/bm-20260514-3.16.0a0-f1a47e7-NOGIL/bm-20260514-vultr-x86_64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7-vs-3.12.6.md)[📈](results/bm-20260514-3.16.0a0-f1a47e7-NOGIL/bm-20260514-vultr-x86_64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7-vs-3.12.6.svg) | 1.073x ↓<br>[📄](results/bm-20260514-3.16.0a0-f1a47e7-NOGIL/bm-20260514-vultr-x86_64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7-vs-3.13.0rc2.md)[📈](results/bm-20260514-3.16.0a0-f1a47e7-NOGIL/bm-20260514-vultr-x86_64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7-vs-3.13.0rc2.svg) | 1.096x ↓<br>[📄](results/bm-20260514-3.16.0a0-f1a47e7-NOGIL/bm-20260514-vultr-x86_64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7-vs-base.md)[📈](results/bm-20260514-3.16.0a0-f1a47e7-NOGIL/bm-20260514-vultr-x86_64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7-vs-base.svg)[🧠](results/bm-20260514-3.16.0a0-f1a47e7-NOGIL/bm-20260514-vultr-x86_64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7-vs-base-mem.svg) |
| [2026-05-14](results/bm-20260514-3.16.0a0-f1a47e7) | python/f1a47e79fb7081d3cde6 | f1a47e7 | 1.056x ↑<br>[📄](results/bm-20260514-3.16.0a0-f1a47e7/bm-20260514-vultr-x86_64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7-vs-3.12.6.md)[📈](results/bm-20260514-3.16.0a0-f1a47e7/bm-20260514-vultr-x86_64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7-vs-3.12.6.svg) | 1.018x ↑<br>[📄](results/bm-20260514-3.16.0a0-f1a47e7/bm-20260514-vultr-x86_64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7-vs-3.13.0rc2.md)[📈](results/bm-20260514-3.16.0a0-f1a47e7/bm-20260514-vultr-x86_64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7-vs-3.13.0rc2.svg) |  |
| [2026-05-12](results/bm-20260512-3.16.0a0-76f2285-NOGIL) | python/76f22853410d3ded872c | 76f2285 (NOGIL) | 1.037x ↓<br>[📄](results/bm-20260512-3.16.0a0-76f2285-NOGIL/bm-20260512-vultr-x86_64-python-76f22853410d3ded872c-3.16.0a0-76f2285-vs-3.12.6.md)[📈](results/bm-20260512-3.16.0a0-76f2285-NOGIL/bm-20260512-vultr-x86_64-python-76f22853410d3ded872c-3.16.0a0-76f2285-vs-3.12.6.svg) | 1.071x ↓<br>[📄](results/bm-20260512-3.16.0a0-76f2285-NOGIL/bm-20260512-vultr-x86_64-python-76f22853410d3ded872c-3.16.0a0-76f2285-vs-3.13.0rc2.md)[📈](results/bm-20260512-3.16.0a0-76f2285-NOGIL/bm-20260512-vultr-x86_64-python-76f22853410d3ded872c-3.16.0a0-76f2285-vs-3.13.0rc2.svg) | 1.098x ↓<br>[📄](results/bm-20260512-3.16.0a0-76f2285-NOGIL/bm-20260512-vultr-x86_64-python-76f22853410d3ded872c-3.16.0a0-76f2285-vs-base.md)[📈](results/bm-20260512-3.16.0a0-76f2285-NOGIL/bm-20260512-vultr-x86_64-python-76f22853410d3ded872c-3.16.0a0-76f2285-vs-base.svg)[🧠](results/bm-20260512-3.16.0a0-76f2285-NOGIL/bm-20260512-vultr-x86_64-python-76f22853410d3ded872c-3.16.0a0-76f2285-vs-base-mem.svg) |
| [2026-05-12](results/bm-20260512-3.16.0a0-76f2285) | python/76f22853410d3ded872c | 76f2285 | 1.061x ↑<br>[📄](results/bm-20260512-3.16.0a0-76f2285/bm-20260512-vultr-x86_64-python-76f22853410d3ded872c-3.16.0a0-76f2285-vs-3.12.6.md)[📈](results/bm-20260512-3.16.0a0-76f2285/bm-20260512-vultr-x86_64-python-76f22853410d3ded872c-3.16.0a0-76f2285-vs-3.12.6.svg) | 1.023x ↑<br>[📄](results/bm-20260512-3.16.0a0-76f2285/bm-20260512-vultr-x86_64-python-76f22853410d3ded872c-3.16.0a0-76f2285-vs-3.13.0rc2.md)[📈](results/bm-20260512-3.16.0a0-76f2285/bm-20260512-vultr-x86_64-python-76f22853410d3ded872c-3.16.0a0-76f2285-vs-3.13.0rc2.svg) |  |
| [2026-05-11](results/bm-20260511-3.16.0a0-7a4c6df-NOGIL) | python/7a4c6dfb8839eb05fb87 | 7a4c6df (NOGIL) | 1.041x ↓<br>[📄](results/bm-20260511-3.16.0a0-7a4c6df-NOGIL/bm-20260511-vultr-x86_64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df-vs-3.12.6.md)[📈](results/bm-20260511-3.16.0a0-7a4c6df-NOGIL/bm-20260511-vultr-x86_64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df-vs-3.12.6.svg) | 1.075x ↓<br>[📄](results/bm-20260511-3.16.0a0-7a4c6df-NOGIL/bm-20260511-vultr-x86_64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df-vs-3.13.0rc2.md)[📈](results/bm-20260511-3.16.0a0-7a4c6df-NOGIL/bm-20260511-vultr-x86_64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df-vs-3.13.0rc2.svg) | 1.105x ↓<br>[📄](results/bm-20260511-3.16.0a0-7a4c6df-NOGIL/bm-20260511-vultr-x86_64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df-vs-base.md)[📈](results/bm-20260511-3.16.0a0-7a4c6df-NOGIL/bm-20260511-vultr-x86_64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df-vs-base.svg)[🧠](results/bm-20260511-3.16.0a0-7a4c6df-NOGIL/bm-20260511-vultr-x86_64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df-vs-base-mem.svg) |
| [2026-05-11](results/bm-20260511-3.16.0a0-7a4c6df) | python/7a4c6dfb8839eb05fb87 | 7a4c6df | 1.065x ↑<br>[📄](results/bm-20260511-3.16.0a0-7a4c6df/bm-20260511-vultr-x86_64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df-vs-3.12.6.md)[📈](results/bm-20260511-3.16.0a0-7a4c6df/bm-20260511-vultr-x86_64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df-vs-3.12.6.svg) | 1.027x ↑<br>[📄](results/bm-20260511-3.16.0a0-7a4c6df/bm-20260511-vultr-x86_64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df-vs-3.13.0rc2.md)[📈](results/bm-20260511-3.16.0a0-7a4c6df/bm-20260511-vultr-x86_64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df-vs-3.13.0rc2.svg) |  |
| [2026-05-10](results/bm-20260510-3.16.0a0-1978785-NOGIL) | python/197878529f20566c1e47 | 1978785 (NOGIL) | 1.040x ↓<br>[📄](results/bm-20260510-3.16.0a0-1978785-NOGIL/bm-20260510-vultr-x86_64-python-197878529f20566c1e47-3.16.0a0-1978785-vs-3.12.6.md)[📈](results/bm-20260510-3.16.0a0-1978785-NOGIL/bm-20260510-vultr-x86_64-python-197878529f20566c1e47-3.16.0a0-1978785-vs-3.12.6.svg) | 1.074x ↓<br>[📄](results/bm-20260510-3.16.0a0-1978785-NOGIL/bm-20260510-vultr-x86_64-python-197878529f20566c1e47-3.16.0a0-1978785-vs-3.13.0rc2.md)[📈](results/bm-20260510-3.16.0a0-1978785-NOGIL/bm-20260510-vultr-x86_64-python-197878529f20566c1e47-3.16.0a0-1978785-vs-3.13.0rc2.svg) | 1.100x ↓<br>[📄](results/bm-20260510-3.16.0a0-1978785-NOGIL/bm-20260510-vultr-x86_64-python-197878529f20566c1e47-3.16.0a0-1978785-vs-base.md)[📈](results/bm-20260510-3.16.0a0-1978785-NOGIL/bm-20260510-vultr-x86_64-python-197878529f20566c1e47-3.16.0a0-1978785-vs-base.svg)[🧠](results/bm-20260510-3.16.0a0-1978785-NOGIL/bm-20260510-vultr-x86_64-python-197878529f20566c1e47-3.16.0a0-1978785-vs-base-mem.svg) |
| [2026-05-10](results/bm-20260510-3.16.0a0-1978785) | python/197878529f20566c1e47 | 1978785 | 1.061x ↑<br>[📄](results/bm-20260510-3.16.0a0-1978785/bm-20260510-vultr-x86_64-python-197878529f20566c1e47-3.16.0a0-1978785-vs-3.12.6.md)[📈](results/bm-20260510-3.16.0a0-1978785/bm-20260510-vultr-x86_64-python-197878529f20566c1e47-3.16.0a0-1978785-vs-3.12.6.svg) | 1.023x ↑<br>[📄](results/bm-20260510-3.16.0a0-1978785/bm-20260510-vultr-x86_64-python-197878529f20566c1e47-3.16.0a0-1978785-vs-3.13.0rc2.md)[📈](results/bm-20260510-3.16.0a0-1978785/bm-20260510-vultr-x86_64-python-197878529f20566c1e47-3.16.0a0-1978785-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-05-14](results/bm-20260514-3.16.0a0-f1a47e7) | python/f1a47e79fb7081d3cde6 | f1a47e7 | 1.158x ↑<br>[📄](results/bm-20260514-3.16.0a0-f1a47e7/bm-20260514-macm4pro-arm64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7-vs-3.12.6.md)[📈](results/bm-20260514-3.16.0a0-f1a47e7/bm-20260514-macm4pro-arm64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7-vs-3.12.6.svg) | 1.068x ↑<br>[📄](results/bm-20260514-3.16.0a0-f1a47e7/bm-20260514-macm4pro-arm64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7-vs-3.13.0rc2.md)[📈](results/bm-20260514-3.16.0a0-f1a47e7/bm-20260514-macm4pro-arm64-python-f1a47e79fb7081d3cde6-3.16.0a0-f1a47e7-vs-3.13.0rc2.svg) |  |
| [2026-05-12](results/bm-20260512-3.16.0a0-76f2285-NOGIL) | python/76f22853410d3ded872c | 76f2285 (NOGIL) | 1.107x ↑<br>[📄](results/bm-20260512-3.16.0a0-76f2285-NOGIL/bm-20260512-macm4pro-arm64-python-76f22853410d3ded872c-3.16.0a0-76f2285-vs-3.12.6.md)[📈](results/bm-20260512-3.16.0a0-76f2285-NOGIL/bm-20260512-macm4pro-arm64-python-76f22853410d3ded872c-3.16.0a0-76f2285-vs-3.12.6.svg) | 1.021x ↑<br>[📄](results/bm-20260512-3.16.0a0-76f2285-NOGIL/bm-20260512-macm4pro-arm64-python-76f22853410d3ded872c-3.16.0a0-76f2285-vs-3.13.0rc2.md)[📈](results/bm-20260512-3.16.0a0-76f2285-NOGIL/bm-20260512-macm4pro-arm64-python-76f22853410d3ded872c-3.16.0a0-76f2285-vs-3.13.0rc2.svg) | 1.028x ↓<br>[📄](results/bm-20260512-3.16.0a0-76f2285-NOGIL/bm-20260512-macm4pro-arm64-python-76f22853410d3ded872c-3.16.0a0-76f2285-vs-base.md)[📈](results/bm-20260512-3.16.0a0-76f2285-NOGIL/bm-20260512-macm4pro-arm64-python-76f22853410d3ded872c-3.16.0a0-76f2285-vs-base.svg)[🧠](results/bm-20260512-3.16.0a0-76f2285-NOGIL/bm-20260512-macm4pro-arm64-python-76f22853410d3ded872c-3.16.0a0-76f2285-vs-base-mem.svg) |
| [2026-05-12](results/bm-20260512-3.16.0a0-76f2285) | python/76f22853410d3ded872c | 76f2285 | 1.136x ↑<br>[📄](results/bm-20260512-3.16.0a0-76f2285/bm-20260512-macm4pro-arm64-python-76f22853410d3ded872c-3.16.0a0-76f2285-vs-3.12.6.md)[📈](results/bm-20260512-3.16.0a0-76f2285/bm-20260512-macm4pro-arm64-python-76f22853410d3ded872c-3.16.0a0-76f2285-vs-3.12.6.svg) | 1.049x ↑<br>[📄](results/bm-20260512-3.16.0a0-76f2285/bm-20260512-macm4pro-arm64-python-76f22853410d3ded872c-3.16.0a0-76f2285-vs-3.13.0rc2.md)[📈](results/bm-20260512-3.16.0a0-76f2285/bm-20260512-macm4pro-arm64-python-76f22853410d3ded872c-3.16.0a0-76f2285-vs-3.13.0rc2.svg) |  |
| [2026-05-11](results/bm-20260511-3.16.0a0-7a4c6df-NOGIL) | python/7a4c6dfb8839eb05fb87 | 7a4c6df (NOGIL) | 1.115x ↑<br>[📄](results/bm-20260511-3.16.0a0-7a4c6df-NOGIL/bm-20260511-macm4pro-arm64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df-vs-3.12.6.md)[📈](results/bm-20260511-3.16.0a0-7a4c6df-NOGIL/bm-20260511-macm4pro-arm64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df-vs-3.12.6.svg) | 1.030x ↑<br>[📄](results/bm-20260511-3.16.0a0-7a4c6df-NOGIL/bm-20260511-macm4pro-arm64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df-vs-3.13.0rc2.md)[📈](results/bm-20260511-3.16.0a0-7a4c6df-NOGIL/bm-20260511-macm4pro-arm64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df-vs-3.13.0rc2.svg) | 1.041x ↓<br>[📄](results/bm-20260511-3.16.0a0-7a4c6df-NOGIL/bm-20260511-macm4pro-arm64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df-vs-base.md)[📈](results/bm-20260511-3.16.0a0-7a4c6df-NOGIL/bm-20260511-macm4pro-arm64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df-vs-base.svg)[🧠](results/bm-20260511-3.16.0a0-7a4c6df-NOGIL/bm-20260511-macm4pro-arm64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df-vs-base-mem.svg) |
| [2026-05-11](results/bm-20260511-3.16.0a0-7a4c6df) | python/7a4c6dfb8839eb05fb87 | 7a4c6df | 1.160x ↑<br>[📄](results/bm-20260511-3.16.0a0-7a4c6df/bm-20260511-macm4pro-arm64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df-vs-3.12.6.md)[📈](results/bm-20260511-3.16.0a0-7a4c6df/bm-20260511-macm4pro-arm64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df-vs-3.12.6.svg) | 1.072x ↑<br>[📄](results/bm-20260511-3.16.0a0-7a4c6df/bm-20260511-macm4pro-arm64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df-vs-3.13.0rc2.md)[📈](results/bm-20260511-3.16.0a0-7a4c6df/bm-20260511-macm4pro-arm64-python-7a4c6dfb8839eb05fb87-3.16.0a0-7a4c6df-vs-3.13.0rc2.svg) |  |
| [2026-05-10](results/bm-20260510-3.16.0a0-1978785-NOGIL) | python/197878529f20566c1e47 | 1978785 (NOGIL) | 1.096x ↑<br>[📄](results/bm-20260510-3.16.0a0-1978785-NOGIL/bm-20260510-macm4pro-arm64-python-197878529f20566c1e47-3.16.0a0-1978785-vs-3.12.6.md)[📈](results/bm-20260510-3.16.0a0-1978785-NOGIL/bm-20260510-macm4pro-arm64-python-197878529f20566c1e47-3.16.0a0-1978785-vs-3.12.6.svg) | 1.012x ↑<br>[📄](results/bm-20260510-3.16.0a0-1978785-NOGIL/bm-20260510-macm4pro-arm64-python-197878529f20566c1e47-3.16.0a0-1978785-vs-3.13.0rc2.md)[📈](results/bm-20260510-3.16.0a0-1978785-NOGIL/bm-20260510-macm4pro-arm64-python-197878529f20566c1e47-3.16.0a0-1978785-vs-3.13.0rc2.svg) | 1.052x ↓<br>[📄](results/bm-20260510-3.16.0a0-1978785-NOGIL/bm-20260510-macm4pro-arm64-python-197878529f20566c1e47-3.16.0a0-1978785-vs-base.md)[📈](results/bm-20260510-3.16.0a0-1978785-NOGIL/bm-20260510-macm4pro-arm64-python-197878529f20566c1e47-3.16.0a0-1978785-vs-base.svg)[🧠](results/bm-20260510-3.16.0a0-1978785-NOGIL/bm-20260510-macm4pro-arm64-python-197878529f20566c1e47-3.16.0a0-1978785-vs-base-mem.svg) |
| [2026-05-10](results/bm-20260510-3.16.0a0-1978785) | python/197878529f20566c1e47 | 1978785 | 1.155x ↑<br>[📄](results/bm-20260510-3.16.0a0-1978785/bm-20260510-macm4pro-arm64-python-197878529f20566c1e47-3.16.0a0-1978785-vs-3.12.6.md)[📈](results/bm-20260510-3.16.0a0-1978785/bm-20260510-macm4pro-arm64-python-197878529f20566c1e47-3.16.0a0-1978785-vs-3.12.6.svg) | 1.066x ↑<br>[📄](results/bm-20260510-3.16.0a0-1978785/bm-20260510-macm4pro-arm64-python-197878529f20566c1e47-3.16.0a0-1978785-vs-3.13.0rc2.md)[📈](results/bm-20260510-3.16.0a0-1978785/bm-20260510-macm4pro-arm64-python-197878529f20566c1e47-3.16.0a0-1978785-vs-3.13.0rc2.svg) |  |


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
