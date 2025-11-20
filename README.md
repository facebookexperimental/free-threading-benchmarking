# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (2f60b8f)](results/bm-20251101-3.15.0a1%2B-2f60b8f/bm-20251101-vultr-x86_64-python-2f60b8f02fe7cb83dd58-3.15.0a1%2B-2f60b8f-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (2f60b8f)](results/bm-20251101-3.15.0a1%2B-2f60b8f-PYTHON_UOPS/bm-20251101-vultr-x86_64-python-2f60b8f02fe7cb83dd58-3.15.0a1%2B-2f60b8f-pystats.md)
- [Most recent JIT pystats on main (bedaea0)](results/bm-20251019-3.15.0a1%2B-bedaea0-JIT/bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-11-19](results/bm-20251119-3.15.0a2%2B-ca1e86f-NOGIL) | python/ca1e86f9d963dc298d9a | ca1e86f (NOGIL) | 1.012x ↓<br>[📄](results/bm-20251119-3.15.0a2%2B-ca1e86f-NOGIL/bm-20251119-vultr-x86_64-python-ca1e86f9d963dc298d9a-3.15.0a2%2B-ca1e86f-vs-3.12.6.md)[📈](results/bm-20251119-3.15.0a2%2B-ca1e86f-NOGIL/bm-20251119-vultr-x86_64-python-ca1e86f9d963dc298d9a-3.15.0a2%2B-ca1e86f-vs-3.12.6.svg) | 1.045x ↓<br>[📄](results/bm-20251119-3.15.0a2%2B-ca1e86f-NOGIL/bm-20251119-vultr-x86_64-python-ca1e86f9d963dc298d9a-3.15.0a2%2B-ca1e86f-vs-3.13.0rc2.md)[📈](results/bm-20251119-3.15.0a2%2B-ca1e86f-NOGIL/bm-20251119-vultr-x86_64-python-ca1e86f9d963dc298d9a-3.15.0a2%2B-ca1e86f-vs-3.13.0rc2.svg) | 1.083x ↓<br>[📄](results/bm-20251119-3.15.0a2%2B-ca1e86f-NOGIL/bm-20251119-vultr-x86_64-python-ca1e86f9d963dc298d9a-3.15.0a2%2B-ca1e86f-vs-base.md)[📈](results/bm-20251119-3.15.0a2%2B-ca1e86f-NOGIL/bm-20251119-vultr-x86_64-python-ca1e86f9d963dc298d9a-3.15.0a2%2B-ca1e86f-vs-base.svg)[🧠](results/bm-20251119-3.15.0a2%2B-ca1e86f-NOGIL/bm-20251119-vultr-x86_64-python-ca1e86f9d963dc298d9a-3.15.0a2%2B-ca1e86f-vs-base-mem.svg) |
| [2025-11-19](results/bm-20251119-3.15.0a2%2B-ca1e86f) | python/ca1e86f9d963dc298d9a | ca1e86f | 1.073x ↑<br>[📄](results/bm-20251119-3.15.0a2%2B-ca1e86f/bm-20251119-vultr-x86_64-python-ca1e86f9d963dc298d9a-3.15.0a2%2B-ca1e86f-vs-3.12.6.md)[📈](results/bm-20251119-3.15.0a2%2B-ca1e86f/bm-20251119-vultr-x86_64-python-ca1e86f9d963dc298d9a-3.15.0a2%2B-ca1e86f-vs-3.12.6.svg) | 1.037x ↑<br>[📄](results/bm-20251119-3.15.0a2%2B-ca1e86f/bm-20251119-vultr-x86_64-python-ca1e86f9d963dc298d9a-3.15.0a2%2B-ca1e86f-vs-3.13.0rc2.md)[📈](results/bm-20251119-3.15.0a2%2B-ca1e86f/bm-20251119-vultr-x86_64-python-ca1e86f9d963dc298d9a-3.15.0a2%2B-ca1e86f-vs-3.13.0rc2.svg) |  |
| [2025-11-19](results/bm-20251119-3.15.0a1%2B-652c764-NOGIL) | python/652c764a59913327b28b | 652c764 (NOGIL) | 1.019x ↓<br>[📄](results/bm-20251119-3.15.0a1%2B-652c764-NOGIL/bm-20251119-vultr-x86_64-python-652c764a59913327b28b-3.15.0a1%2B-652c764-vs-3.12.6.md)[📈](results/bm-20251119-3.15.0a1%2B-652c764-NOGIL/bm-20251119-vultr-x86_64-python-652c764a59913327b28b-3.15.0a1%2B-652c764-vs-3.12.6.svg) | 1.052x ↓<br>[📄](results/bm-20251119-3.15.0a1%2B-652c764-NOGIL/bm-20251119-vultr-x86_64-python-652c764a59913327b28b-3.15.0a1%2B-652c764-vs-3.13.0rc2.md)[📈](results/bm-20251119-3.15.0a1%2B-652c764-NOGIL/bm-20251119-vultr-x86_64-python-652c764a59913327b28b-3.15.0a1%2B-652c764-vs-3.13.0rc2.svg) | 1.092x ↓<br>[📄](results/bm-20251119-3.15.0a1%2B-652c764-NOGIL/bm-20251119-vultr-x86_64-python-652c764a59913327b28b-3.15.0a1%2B-652c764-vs-base.md)[📈](results/bm-20251119-3.15.0a1%2B-652c764-NOGIL/bm-20251119-vultr-x86_64-python-652c764a59913327b28b-3.15.0a1%2B-652c764-vs-base.svg)[🧠](results/bm-20251119-3.15.0a1%2B-652c764-NOGIL/bm-20251119-vultr-x86_64-python-652c764a59913327b28b-3.15.0a1%2B-652c764-vs-base-mem.svg) |
| [2025-11-19](results/bm-20251119-3.15.0a1%2B-652c764) | python/652c764a59913327b28b | 652c764 | 1.076x ↑<br>[📄](results/bm-20251119-3.15.0a1%2B-652c764/bm-20251119-vultr-x86_64-python-652c764a59913327b28b-3.15.0a1%2B-652c764-vs-3.12.6.md)[📈](results/bm-20251119-3.15.0a1%2B-652c764/bm-20251119-vultr-x86_64-python-652c764a59913327b28b-3.15.0a1%2B-652c764-vs-3.12.6.svg) | 1.040x ↑<br>[📄](results/bm-20251119-3.15.0a1%2B-652c764/bm-20251119-vultr-x86_64-python-652c764a59913327b28b-3.15.0a1%2B-652c764-vs-3.13.0rc2.md)[📈](results/bm-20251119-3.15.0a1%2B-652c764/bm-20251119-vultr-x86_64-python-652c764a59913327b28b-3.15.0a1%2B-652c764-vs-3.13.0rc2.svg) |  |
| [2025-11-17](results/bm-20251117-3.15.0a1%2B-16ea950-NOGIL) | python/16ea9505ce690485bab3 | 16ea950 (NOGIL) | 1.015x ↓<br>[📄](results/bm-20251117-3.15.0a1%2B-16ea950-NOGIL/bm-20251117-vultr-x86_64-python-16ea9505ce690485bab3-3.15.0a1%2B-16ea950-vs-3.12.6.md)[📈](results/bm-20251117-3.15.0a1%2B-16ea950-NOGIL/bm-20251117-vultr-x86_64-python-16ea9505ce690485bab3-3.15.0a1%2B-16ea950-vs-3.12.6.svg) | 1.048x ↓<br>[📄](results/bm-20251117-3.15.0a1%2B-16ea950-NOGIL/bm-20251117-vultr-x86_64-python-16ea9505ce690485bab3-3.15.0a1%2B-16ea950-vs-3.13.0rc2.md)[📈](results/bm-20251117-3.15.0a1%2B-16ea950-NOGIL/bm-20251117-vultr-x86_64-python-16ea9505ce690485bab3-3.15.0a1%2B-16ea950-vs-3.13.0rc2.svg) | 1.090x ↓<br>[📄](results/bm-20251117-3.15.0a1%2B-16ea950-NOGIL/bm-20251117-vultr-x86_64-python-16ea9505ce690485bab3-3.15.0a1%2B-16ea950-vs-base.md)[📈](results/bm-20251117-3.15.0a1%2B-16ea950-NOGIL/bm-20251117-vultr-x86_64-python-16ea9505ce690485bab3-3.15.0a1%2B-16ea950-vs-base.svg)[🧠](results/bm-20251117-3.15.0a1%2B-16ea950-NOGIL/bm-20251117-vultr-x86_64-python-16ea9505ce690485bab3-3.15.0a1%2B-16ea950-vs-base-mem.svg) |
| [2025-11-17](results/bm-20251117-3.15.0a1%2B-16ea950) | python/16ea9505ce690485bab3 | 16ea950 | 1.078x ↑<br>[📄](results/bm-20251117-3.15.0a1%2B-16ea950/bm-20251117-vultr-x86_64-python-16ea9505ce690485bab3-3.15.0a1%2B-16ea950-vs-3.12.6.md)[📈](results/bm-20251117-3.15.0a1%2B-16ea950/bm-20251117-vultr-x86_64-python-16ea9505ce690485bab3-3.15.0a1%2B-16ea950-vs-3.12.6.svg) | 1.042x ↑<br>[📄](results/bm-20251117-3.15.0a1%2B-16ea950/bm-20251117-vultr-x86_64-python-16ea9505ce690485bab3-3.15.0a1%2B-16ea950-vs-3.13.0rc2.md)[📈](results/bm-20251117-3.15.0a1%2B-16ea950/bm-20251117-vultr-x86_64-python-16ea9505ce690485bab3-3.15.0a1%2B-16ea950-vs-3.13.0rc2.svg) |  |
| [2025-11-16](results/bm-20251116-3.15.0a1%2B-8be3b2f-NOGIL) | python/8be3b2f479431f670f2e | 8be3b2f (NOGIL) | 1.017x ↓<br>[📄](results/bm-20251116-3.15.0a1%2B-8be3b2f-NOGIL/bm-20251116-vultr-x86_64-python-8be3b2f479431f670f2e-3.15.0a1%2B-8be3b2f-vs-3.12.6.md)[📈](results/bm-20251116-3.15.0a1%2B-8be3b2f-NOGIL/bm-20251116-vultr-x86_64-python-8be3b2f479431f670f2e-3.15.0a1%2B-8be3b2f-vs-3.12.6.svg) | 1.051x ↓<br>[📄](results/bm-20251116-3.15.0a1%2B-8be3b2f-NOGIL/bm-20251116-vultr-x86_64-python-8be3b2f479431f670f2e-3.15.0a1%2B-8be3b2f-vs-3.13.0rc2.md)[📈](results/bm-20251116-3.15.0a1%2B-8be3b2f-NOGIL/bm-20251116-vultr-x86_64-python-8be3b2f479431f670f2e-3.15.0a1%2B-8be3b2f-vs-3.13.0rc2.svg) | 1.090x ↓<br>[📄](results/bm-20251116-3.15.0a1%2B-8be3b2f-NOGIL/bm-20251116-vultr-x86_64-python-8be3b2f479431f670f2e-3.15.0a1%2B-8be3b2f-vs-base.md)[📈](results/bm-20251116-3.15.0a1%2B-8be3b2f-NOGIL/bm-20251116-vultr-x86_64-python-8be3b2f479431f670f2e-3.15.0a1%2B-8be3b2f-vs-base.svg)[🧠](results/bm-20251116-3.15.0a1%2B-8be3b2f-NOGIL/bm-20251116-vultr-x86_64-python-8be3b2f479431f670f2e-3.15.0a1%2B-8be3b2f-vs-base-mem.svg) |
| [2025-11-16](results/bm-20251116-3.15.0a1%2B-8be3b2f) | python/8be3b2f479431f670f2e | 8be3b2f | 1.076x ↑<br>[📄](results/bm-20251116-3.15.0a1%2B-8be3b2f/bm-20251116-vultr-x86_64-python-8be3b2f479431f670f2e-3.15.0a1%2B-8be3b2f-vs-3.12.6.md)[📈](results/bm-20251116-3.15.0a1%2B-8be3b2f/bm-20251116-vultr-x86_64-python-8be3b2f479431f670f2e-3.15.0a1%2B-8be3b2f-vs-3.12.6.svg) | 1.040x ↑<br>[📄](results/bm-20251116-3.15.0a1%2B-8be3b2f/bm-20251116-vultr-x86_64-python-8be3b2f479431f670f2e-3.15.0a1%2B-8be3b2f-vs-3.13.0rc2.md)[📈](results/bm-20251116-3.15.0a1%2B-8be3b2f/bm-20251116-vultr-x86_64-python-8be3b2f479431f670f2e-3.15.0a1%2B-8be3b2f-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-11-19](results/bm-20251119-3.15.0a2%2B-ca1e86f-NOGIL) | python/ca1e86f9d963dc298d9a | ca1e86f (NOGIL) | 1.120x ↑<br>[📄](results/bm-20251119-3.15.0a2%2B-ca1e86f-NOGIL/bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2%2B-ca1e86f-vs-3.12.6.md)[📈](results/bm-20251119-3.15.0a2%2B-ca1e86f-NOGIL/bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2%2B-ca1e86f-vs-3.12.6.svg) | 1.033x ↑<br>[📄](results/bm-20251119-3.15.0a2%2B-ca1e86f-NOGIL/bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2%2B-ca1e86f-vs-3.13.0rc2.md)[📈](results/bm-20251119-3.15.0a2%2B-ca1e86f-NOGIL/bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2%2B-ca1e86f-vs-3.13.0rc2.svg) | 1.008x ↓<br>[📄](results/bm-20251119-3.15.0a2%2B-ca1e86f-NOGIL/bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2%2B-ca1e86f-vs-base.md)[📈](results/bm-20251119-3.15.0a2%2B-ca1e86f-NOGIL/bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2%2B-ca1e86f-vs-base.svg)[🧠](results/bm-20251119-3.15.0a2%2B-ca1e86f-NOGIL/bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2%2B-ca1e86f-vs-base-mem.svg) |
| [2025-11-19](results/bm-20251119-3.15.0a2%2B-ca1e86f) | python/ca1e86f9d963dc298d9a | ca1e86f | 1.128x ↑<br>[📄](results/bm-20251119-3.15.0a2%2B-ca1e86f/bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2%2B-ca1e86f-vs-3.12.6.md)[📈](results/bm-20251119-3.15.0a2%2B-ca1e86f/bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2%2B-ca1e86f-vs-3.12.6.svg) | 1.040x ↑<br>[📄](results/bm-20251119-3.15.0a2%2B-ca1e86f/bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2%2B-ca1e86f-vs-3.13.0rc2.md)[📈](results/bm-20251119-3.15.0a2%2B-ca1e86f/bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2%2B-ca1e86f-vs-3.13.0rc2.svg) |  |
| [2025-11-19](results/bm-20251119-3.15.0a1%2B-652c764-NOGIL) | python/652c764a59913327b28b | 652c764 (NOGIL) | 1.105x ↑<br>[📄](results/bm-20251119-3.15.0a1%2B-652c764-NOGIL/bm-20251119-macm4pro-arm64-python-652c764a59913327b28b-3.15.0a1%2B-652c764-vs-3.12.6.md)[📈](results/bm-20251119-3.15.0a1%2B-652c764-NOGIL/bm-20251119-macm4pro-arm64-python-652c764a59913327b28b-3.15.0a1%2B-652c764-vs-3.12.6.svg) | 1.019x ↑<br>[📄](results/bm-20251119-3.15.0a1%2B-652c764-NOGIL/bm-20251119-macm4pro-arm64-python-652c764a59913327b28b-3.15.0a1%2B-652c764-vs-3.13.0rc2.md)[📈](results/bm-20251119-3.15.0a1%2B-652c764-NOGIL/bm-20251119-macm4pro-arm64-python-652c764a59913327b28b-3.15.0a1%2B-652c764-vs-3.13.0rc2.svg) | 1.031x ↓<br>[📄](results/bm-20251119-3.15.0a1%2B-652c764-NOGIL/bm-20251119-macm4pro-arm64-python-652c764a59913327b28b-3.15.0a1%2B-652c764-vs-base.md)[📈](results/bm-20251119-3.15.0a1%2B-652c764-NOGIL/bm-20251119-macm4pro-arm64-python-652c764a59913327b28b-3.15.0a1%2B-652c764-vs-base.svg)[🧠](results/bm-20251119-3.15.0a1%2B-652c764-NOGIL/bm-20251119-macm4pro-arm64-python-652c764a59913327b28b-3.15.0a1%2B-652c764-vs-base-mem.svg) |
| [2025-11-19](results/bm-20251119-3.15.0a1%2B-652c764) | python/652c764a59913327b28b | 652c764 | 1.139x ↑<br>[📄](results/bm-20251119-3.15.0a1%2B-652c764/bm-20251119-macm4pro-arm64-python-652c764a59913327b28b-3.15.0a1%2B-652c764-vs-3.12.6.md)[📈](results/bm-20251119-3.15.0a1%2B-652c764/bm-20251119-macm4pro-arm64-python-652c764a59913327b28b-3.15.0a1%2B-652c764-vs-3.12.6.svg) | 1.050x ↑<br>[📄](results/bm-20251119-3.15.0a1%2B-652c764/bm-20251119-macm4pro-arm64-python-652c764a59913327b28b-3.15.0a1%2B-652c764-vs-3.13.0rc2.md)[📈](results/bm-20251119-3.15.0a1%2B-652c764/bm-20251119-macm4pro-arm64-python-652c764a59913327b28b-3.15.0a1%2B-652c764-vs-3.13.0rc2.svg) |  |
| [2025-11-17](results/bm-20251117-3.15.0a1%2B-16ea950-NOGIL) | python/16ea9505ce690485bab3 | 16ea950 (NOGIL) | 1.114x ↑<br>[📄](results/bm-20251117-3.15.0a1%2B-16ea950-NOGIL/bm-20251117-macm4pro-arm64-python-16ea9505ce690485bab3-3.15.0a1%2B-16ea950-vs-3.12.6.md)[📈](results/bm-20251117-3.15.0a1%2B-16ea950-NOGIL/bm-20251117-macm4pro-arm64-python-16ea9505ce690485bab3-3.15.0a1%2B-16ea950-vs-3.12.6.svg) | 1.027x ↑<br>[📄](results/bm-20251117-3.15.0a1%2B-16ea950-NOGIL/bm-20251117-macm4pro-arm64-python-16ea9505ce690485bab3-3.15.0a1%2B-16ea950-vs-3.13.0rc2.md)[📈](results/bm-20251117-3.15.0a1%2B-16ea950-NOGIL/bm-20251117-macm4pro-arm64-python-16ea9505ce690485bab3-3.15.0a1%2B-16ea950-vs-3.13.0rc2.svg) | 1.031x ↓<br>[📄](results/bm-20251117-3.15.0a1%2B-16ea950-NOGIL/bm-20251117-macm4pro-arm64-python-16ea9505ce690485bab3-3.15.0a1%2B-16ea950-vs-base.md)[📈](results/bm-20251117-3.15.0a1%2B-16ea950-NOGIL/bm-20251117-macm4pro-arm64-python-16ea9505ce690485bab3-3.15.0a1%2B-16ea950-vs-base.svg)[🧠](results/bm-20251117-3.15.0a1%2B-16ea950-NOGIL/bm-20251117-macm4pro-arm64-python-16ea9505ce690485bab3-3.15.0a1%2B-16ea950-vs-base-mem.svg) |
| [2025-11-17](results/bm-20251117-3.15.0a1%2B-16ea950) | python/16ea9505ce690485bab3 | 16ea950 | 1.147x ↑<br>[📄](results/bm-20251117-3.15.0a1%2B-16ea950/bm-20251117-macm4pro-arm64-python-16ea9505ce690485bab3-3.15.0a1%2B-16ea950-vs-3.12.6.md)[📈](results/bm-20251117-3.15.0a1%2B-16ea950/bm-20251117-macm4pro-arm64-python-16ea9505ce690485bab3-3.15.0a1%2B-16ea950-vs-3.12.6.svg) | 1.058x ↑<br>[📄](results/bm-20251117-3.15.0a1%2B-16ea950/bm-20251117-macm4pro-arm64-python-16ea9505ce690485bab3-3.15.0a1%2B-16ea950-vs-3.13.0rc2.md)[📈](results/bm-20251117-3.15.0a1%2B-16ea950/bm-20251117-macm4pro-arm64-python-16ea9505ce690485bab3-3.15.0a1%2B-16ea950-vs-3.13.0rc2.svg) |  |
| [2025-11-17](results/bm-20251117-3.15.0a1%2B-cc6b62a-JIT) | python/main | cc6b62a (JIT) | 1.138x ↑<br>[📄](results/bm-20251117-3.15.0a1%2B-cc6b62a-JIT/bm-20251117-macm4pro-arm64-python-main-3.15.0a1%2B-cc6b62a-vs-3.12.6.md)[📈](results/bm-20251117-3.15.0a1%2B-cc6b62a-JIT/bm-20251117-macm4pro-arm64-python-main-3.15.0a1%2B-cc6b62a-vs-3.12.6.svg) | 1.049x ↑<br>[📄](results/bm-20251117-3.15.0a1%2B-cc6b62a-JIT/bm-20251117-macm4pro-arm64-python-main-3.15.0a1%2B-cc6b62a-vs-3.13.0rc2.md)[📈](results/bm-20251117-3.15.0a1%2B-cc6b62a-JIT/bm-20251117-macm4pro-arm64-python-main-3.15.0a1%2B-cc6b62a-vs-3.13.0rc2.svg) |  |
| [2025-11-16](results/bm-20251116-3.15.0a1%2B-b748f45-JIT) | Fidget-Spinner/llvm_19 | b748f45 (JIT) | 1.138x ↑<br>[📄](results/bm-20251116-3.15.0a1%2B-b748f45-JIT/bm-20251116-macm4pro-arm64-Fidget%252dSpinner-llvm_19-3.15.0a1%2B-b748f45-vs-3.12.6.md)[📈](results/bm-20251116-3.15.0a1%2B-b748f45-JIT/bm-20251116-macm4pro-arm64-Fidget%252dSpinner-llvm_19-3.15.0a1%2B-b748f45-vs-3.12.6.svg) | 1.048x ↑<br>[📄](results/bm-20251116-3.15.0a1%2B-b748f45-JIT/bm-20251116-macm4pro-arm64-Fidget%252dSpinner-llvm_19-3.15.0a1%2B-b748f45-vs-3.13.0rc2.md)[📈](results/bm-20251116-3.15.0a1%2B-b748f45-JIT/bm-20251116-macm4pro-arm64-Fidget%252dSpinner-llvm_19-3.15.0a1%2B-b748f45-vs-3.13.0rc2.svg) |  |
| [2025-11-16](results/bm-20251116-3.15.0a1%2B-8be3b2f-NOGIL) | python/8be3b2f479431f670f2e | 8be3b2f (NOGIL) | 1.104x ↑<br>[📄](results/bm-20251116-3.15.0a1%2B-8be3b2f-NOGIL/bm-20251116-macm4pro-arm64-python-8be3b2f479431f670f2e-3.15.0a1%2B-8be3b2f-vs-3.12.6.md)[📈](results/bm-20251116-3.15.0a1%2B-8be3b2f-NOGIL/bm-20251116-macm4pro-arm64-python-8be3b2f479431f670f2e-3.15.0a1%2B-8be3b2f-vs-3.12.6.svg) | 1.018x ↑<br>[📄](results/bm-20251116-3.15.0a1%2B-8be3b2f-NOGIL/bm-20251116-macm4pro-arm64-python-8be3b2f479431f670f2e-3.15.0a1%2B-8be3b2f-vs-3.13.0rc2.md)[📈](results/bm-20251116-3.15.0a1%2B-8be3b2f-NOGIL/bm-20251116-macm4pro-arm64-python-8be3b2f479431f670f2e-3.15.0a1%2B-8be3b2f-vs-3.13.0rc2.svg) | 1.040x ↓<br>[📄](results/bm-20251116-3.15.0a1%2B-8be3b2f-NOGIL/bm-20251116-macm4pro-arm64-python-8be3b2f479431f670f2e-3.15.0a1%2B-8be3b2f-vs-base.md)[📈](results/bm-20251116-3.15.0a1%2B-8be3b2f-NOGIL/bm-20251116-macm4pro-arm64-python-8be3b2f479431f670f2e-3.15.0a1%2B-8be3b2f-vs-base.svg)[🧠](results/bm-20251116-3.15.0a1%2B-8be3b2f-NOGIL/bm-20251116-macm4pro-arm64-python-8be3b2f479431f670f2e-3.15.0a1%2B-8be3b2f-vs-base-mem.svg) |
| [2025-11-16](results/bm-20251116-3.15.0a1%2B-8be3b2f) | python/8be3b2f479431f670f2e | 8be3b2f | 1.149x ↑<br>[📄](results/bm-20251116-3.15.0a1%2B-8be3b2f/bm-20251116-macm4pro-arm64-python-8be3b2f479431f670f2e-3.15.0a1%2B-8be3b2f-vs-3.12.6.md)[📈](results/bm-20251116-3.15.0a1%2B-8be3b2f/bm-20251116-macm4pro-arm64-python-8be3b2f479431f670f2e-3.15.0a1%2B-8be3b2f-vs-3.12.6.svg) | 1.059x ↑<br>[📄](results/bm-20251116-3.15.0a1%2B-8be3b2f/bm-20251116-macm4pro-arm64-python-8be3b2f479431f670f2e-3.15.0a1%2B-8be3b2f-vs-3.13.0rc2.md)[📈](results/bm-20251116-3.15.0a1%2B-8be3b2f/bm-20251116-macm4pro-arm64-python-8be3b2f479431f670f2e-3.15.0a1%2B-8be3b2f-vs-3.13.0rc2.svg) |  |


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
