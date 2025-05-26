# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (2fd09b0)](results/bm-20250524-3.15.0a0-2fd09b0/bm-20250524-linux-x86_64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (2fd09b0)](results/bm-20250524-3.15.0a0-2fd09b0-PYTHON_UOPS/bm-20250524-linux-x86_64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-pystats.md)

## linux x86_64 (linux)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-05-22](results/bm-20250522-3.15.0a0-a3d0306-NOGIL) | python/a3d0306ca08d09b1417d | a3d0306 (NOGIL) | 1.109x ↑<br>[📄](results/bm-20250522-3.15.0a0-a3d0306-NOGIL/bm-20250522-linux-x86_64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306-vs-3.12.6.md)[📈](results/bm-20250522-3.15.0a0-a3d0306-NOGIL/bm-20250522-linux-x86_64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306-vs-3.12.6.svg) | 1.068x ↑<br>[📄](results/bm-20250522-3.15.0a0-a3d0306-NOGIL/bm-20250522-linux-x86_64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306-vs-3.13.0rc2.md)[📈](results/bm-20250522-3.15.0a0-a3d0306-NOGIL/bm-20250522-linux-x86_64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306-vs-3.13.0rc2.svg) | 1.087x ↓<br>[📄](results/bm-20250522-3.15.0a0-a3d0306-NOGIL/bm-20250522-linux-x86_64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306-vs-base.md)[📈](results/bm-20250522-3.15.0a0-a3d0306-NOGIL/bm-20250522-linux-x86_64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306-vs-base.svg)[🧠](results/bm-20250522-3.15.0a0-a3d0306-NOGIL/bm-20250522-linux-x86_64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306-vs-base-mem.svg) |
| [2025-05-22](results/bm-20250522-3.15.0a0-a3d0306) | python/a3d0306ca08d09b1417d | a3d0306 | 1.205x ↑<br>[📄](results/bm-20250522-3.15.0a0-a3d0306/bm-20250522-linux-x86_64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306-vs-3.12.6.md)[📈](results/bm-20250522-3.15.0a0-a3d0306/bm-20250522-linux-x86_64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306-vs-3.12.6.svg) | 1.160x ↑<br>[📄](results/bm-20250522-3.15.0a0-a3d0306/bm-20250522-linux-x86_64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306-vs-3.13.0rc2.md)[📈](results/bm-20250522-3.15.0a0-a3d0306/bm-20250522-linux-x86_64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306-vs-3.13.0rc2.svg) |  |
| [2025-05-22](results/bm-20250522-3.15.0a0-b1b8962-NOGIL) | python/b1b8962443e7d4186016 | b1b8962 (NOGIL) | 1.139x ↑<br>[📄](results/bm-20250522-3.15.0a0-b1b8962-NOGIL/bm-20250522-linux-x86_64-python-b1b8962443e7d4186016-3.15.0a0-b1b8962-vs-3.12.6.md)[📈](results/bm-20250522-3.15.0a0-b1b8962-NOGIL/bm-20250522-linux-x86_64-python-b1b8962443e7d4186016-3.15.0a0-b1b8962-vs-3.12.6.svg) | 1.098x ↑<br>[📄](results/bm-20250522-3.15.0a0-b1b8962-NOGIL/bm-20250522-linux-x86_64-python-b1b8962443e7d4186016-3.15.0a0-b1b8962-vs-3.13.0rc2.md)[📈](results/bm-20250522-3.15.0a0-b1b8962-NOGIL/bm-20250522-linux-x86_64-python-b1b8962443e7d4186016-3.15.0a0-b1b8962-vs-3.13.0rc2.svg) | 1.075x ↓<br>[📄](results/bm-20250522-3.15.0a0-b1b8962-NOGIL/bm-20250522-linux-x86_64-python-b1b8962443e7d4186016-3.15.0a0-b1b8962-vs-base.md)[📈](results/bm-20250522-3.15.0a0-b1b8962-NOGIL/bm-20250522-linux-x86_64-python-b1b8962443e7d4186016-3.15.0a0-b1b8962-vs-base.svg)[🧠](results/bm-20250522-3.15.0a0-b1b8962-NOGIL/bm-20250522-linux-x86_64-python-b1b8962443e7d4186016-3.15.0a0-b1b8962-vs-base-mem.svg) |

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-05-24](results/bm-20250524-3.15.0a0-2fd09b0-NOGIL) | python/2fd09b011031f3c00c34 | 2fd09b0 (NOGIL) | 1.008x ↑<br>[📄](results/bm-20250524-3.15.0a0-2fd09b0-NOGIL/bm-20250524-vultr-x86_64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-3.12.6.md)[📈](results/bm-20250524-3.15.0a0-2fd09b0-NOGIL/bm-20250524-vultr-x86_64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-3.12.6.svg) | 1.027x ↓<br>[📄](results/bm-20250524-3.15.0a0-2fd09b0-NOGIL/bm-20250524-vultr-x86_64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-3.13.0rc2.md)[📈](results/bm-20250524-3.15.0a0-2fd09b0-NOGIL/bm-20250524-vultr-x86_64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-3.13.0rc2.svg) | 1.093x ↓<br>[📄](results/bm-20250524-3.15.0a0-2fd09b0-NOGIL/bm-20250524-vultr-x86_64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-base.md)[📈](results/bm-20250524-3.15.0a0-2fd09b0-NOGIL/bm-20250524-vultr-x86_64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-base.svg)[🧠](results/bm-20250524-3.15.0a0-2fd09b0-NOGIL/bm-20250524-vultr-x86_64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-base-mem.svg) |
| [2025-05-24](results/bm-20250524-3.15.0a0-2fd09b0-JIT) | python/2fd09b011031f3c00c34 | 2fd09b0 (JIT) | 1.104x ↑<br>[📄](results/bm-20250524-3.15.0a0-2fd09b0-JIT/bm-20250524-vultr-x86_64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-3.12.6.md)[📈](results/bm-20250524-3.15.0a0-2fd09b0-JIT/bm-20250524-vultr-x86_64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-3.12.6.svg) | 1.067x ↑<br>[📄](results/bm-20250524-3.15.0a0-2fd09b0-JIT/bm-20250524-vultr-x86_64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-3.13.0rc2.md)[📈](results/bm-20250524-3.15.0a0-2fd09b0-JIT/bm-20250524-vultr-x86_64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-3.13.0rc2.svg) | 1.002x ↓<br>[📄](results/bm-20250524-3.15.0a0-2fd09b0-JIT/bm-20250524-vultr-x86_64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-base.md)[📈](results/bm-20250524-3.15.0a0-2fd09b0-JIT/bm-20250524-vultr-x86_64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-base.svg)[🧠](results/bm-20250524-3.15.0a0-2fd09b0-JIT/bm-20250524-vultr-x86_64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-base-mem.svg) |
| [2025-05-24](results/bm-20250524-3.15.0a0-2fd09b0-CLANG) | python/2fd09b011031f3c00c34 | 2fd09b0 (CLANG) | 1.148x ↑<br>[📄](results/bm-20250524-3.15.0a0-2fd09b0-CLANG/bm-20250524-vultr-x86_64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-3.12.6.md)[📈](results/bm-20250524-3.15.0a0-2fd09b0-CLANG/bm-20250524-vultr-x86_64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-3.12.6.svg) | 1.108x ↑<br>[📄](results/bm-20250524-3.15.0a0-2fd09b0-CLANG/bm-20250524-vultr-x86_64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-3.13.0rc2.md)[📈](results/bm-20250524-3.15.0a0-2fd09b0-CLANG/bm-20250524-vultr-x86_64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-3.13.0rc2.svg) | 1.035x ↑<br>[📄](results/bm-20250524-3.15.0a0-2fd09b0-CLANG/bm-20250524-vultr-x86_64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-base.md)[📈](results/bm-20250524-3.15.0a0-2fd09b0-CLANG/bm-20250524-vultr-x86_64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-base.svg)[🧠](results/bm-20250524-3.15.0a0-2fd09b0-CLANG/bm-20250524-vultr-x86_64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-base-mem.svg) |
| [2025-05-24](results/bm-20250524-3.15.0a0-2fd09b0) | python/2fd09b011031f3c00c34 | 2fd09b0 | 1.105x ↑<br>[📄](results/bm-20250524-3.15.0a0-2fd09b0/bm-20250524-vultr-x86_64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-3.12.6.md)[📈](results/bm-20250524-3.15.0a0-2fd09b0/bm-20250524-vultr-x86_64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-3.12.6.svg) | 1.068x ↑<br>[📄](results/bm-20250524-3.15.0a0-2fd09b0/bm-20250524-vultr-x86_64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-3.13.0rc2.md)[📈](results/bm-20250524-3.15.0a0-2fd09b0/bm-20250524-vultr-x86_64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-3.13.0rc2.svg) |  |
| [2025-05-23](results/bm-20250523-3.15.0a0-f478331-NOGIL) | python/f478331f98930d94f7ef | f478331 (NOGIL) | 1.009x ↑<br>[📄](results/bm-20250523-3.15.0a0-f478331-NOGIL/bm-20250523-vultr-x86_64-python-f478331f98930d94f7ef-3.15.0a0-f478331-vs-3.12.6.md)[📈](results/bm-20250523-3.15.0a0-f478331-NOGIL/bm-20250523-vultr-x86_64-python-f478331f98930d94f7ef-3.15.0a0-f478331-vs-3.12.6.svg) | 1.026x ↓<br>[📄](results/bm-20250523-3.15.0a0-f478331-NOGIL/bm-20250523-vultr-x86_64-python-f478331f98930d94f7ef-3.15.0a0-f478331-vs-3.13.0rc2.md)[📈](results/bm-20250523-3.15.0a0-f478331-NOGIL/bm-20250523-vultr-x86_64-python-f478331f98930d94f7ef-3.15.0a0-f478331-vs-3.13.0rc2.svg) | 1.088x ↓<br>[📄](results/bm-20250523-3.15.0a0-f478331-NOGIL/bm-20250523-vultr-x86_64-python-f478331f98930d94f7ef-3.15.0a0-f478331-vs-base.md)[📈](results/bm-20250523-3.15.0a0-f478331-NOGIL/bm-20250523-vultr-x86_64-python-f478331f98930d94f7ef-3.15.0a0-f478331-vs-base.svg)[🧠](results/bm-20250523-3.15.0a0-f478331-NOGIL/bm-20250523-vultr-x86_64-python-f478331f98930d94f7ef-3.15.0a0-f478331-vs-base-mem.svg) |
| [2025-05-23](results/bm-20250523-3.15.0a0-f478331) | python/f478331f98930d94f7ef | f478331 | 1.100x ↑<br>[📄](results/bm-20250523-3.15.0a0-f478331/bm-20250523-vultr-x86_64-python-f478331f98930d94f7ef-3.15.0a0-f478331-vs-3.12.6.md)[📈](results/bm-20250523-3.15.0a0-f478331/bm-20250523-vultr-x86_64-python-f478331f98930d94f7ef-3.15.0a0-f478331-vs-3.12.6.svg) | 1.062x ↑<br>[📄](results/bm-20250523-3.15.0a0-f478331/bm-20250523-vultr-x86_64-python-f478331f98930d94f7ef-3.15.0a0-f478331-vs-3.13.0rc2.md)[📈](results/bm-20250523-3.15.0a0-f478331/bm-20250523-vultr-x86_64-python-f478331f98930d94f7ef-3.15.0a0-f478331-vs-3.13.0rc2.svg) |  |
| [2025-05-22](results/bm-20250522-3.15.0a0-a3d0306-NOGIL) | python/a3d0306ca08d09b1417d | a3d0306 (NOGIL) | 1.009x ↑<br>[📄](results/bm-20250522-3.15.0a0-a3d0306-NOGIL/bm-20250522-vultr-x86_64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306-vs-3.12.6.md)[📈](results/bm-20250522-3.15.0a0-a3d0306-NOGIL/bm-20250522-vultr-x86_64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306-vs-3.12.6.svg) | 1.026x ↓<br>[📄](results/bm-20250522-3.15.0a0-a3d0306-NOGIL/bm-20250522-vultr-x86_64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306-vs-3.13.0rc2.md)[📈](results/bm-20250522-3.15.0a0-a3d0306-NOGIL/bm-20250522-vultr-x86_64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306-vs-3.13.0rc2.svg) | 1.091x ↓<br>[📄](results/bm-20250522-3.15.0a0-a3d0306-NOGIL/bm-20250522-vultr-x86_64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306-vs-base.md)[📈](results/bm-20250522-3.15.0a0-a3d0306-NOGIL/bm-20250522-vultr-x86_64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306-vs-base.svg)[🧠](results/bm-20250522-3.15.0a0-a3d0306-NOGIL/bm-20250522-vultr-x86_64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306-vs-base-mem.svg) |
| [2025-05-22](results/bm-20250522-3.15.0a0-a3d0306) | python/a3d0306ca08d09b1417d | a3d0306 | 1.104x ↑<br>[📄](results/bm-20250522-3.15.0a0-a3d0306/bm-20250522-vultr-x86_64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306-vs-3.12.6.md)[📈](results/bm-20250522-3.15.0a0-a3d0306/bm-20250522-vultr-x86_64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306-vs-3.12.6.svg) | 1.066x ↑<br>[📄](results/bm-20250522-3.15.0a0-a3d0306/bm-20250522-vultr-x86_64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306-vs-3.13.0rc2.md)[📈](results/bm-20250522-3.15.0a0-a3d0306/bm-20250522-vultr-x86_64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-05-24](results/bm-20250524-3.15.0a0-2fd09b0-NOGIL) | python/2fd09b011031f3c00c34 | 2fd09b0 (NOGIL) | 1.098x ↑<br>[📄](results/bm-20250524-3.15.0a0-2fd09b0-NOGIL/bm-20250524-macm4pro-arm64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-3.12.6.md)[📈](results/bm-20250524-3.15.0a0-2fd09b0-NOGIL/bm-20250524-macm4pro-arm64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-3.12.6.svg) | 1.018x ↑<br>[📄](results/bm-20250524-3.15.0a0-2fd09b0-NOGIL/bm-20250524-macm4pro-arm64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-3.13.0rc2.md)[📈](results/bm-20250524-3.15.0a0-2fd09b0-NOGIL/bm-20250524-macm4pro-arm64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-3.13.0rc2.svg) | 1.015x ↓<br>[📄](results/bm-20250524-3.15.0a0-2fd09b0-NOGIL/bm-20250524-macm4pro-arm64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-base.md)[📈](results/bm-20250524-3.15.0a0-2fd09b0-NOGIL/bm-20250524-macm4pro-arm64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-base.svg)[🧠](results/bm-20250524-3.15.0a0-2fd09b0-NOGIL/bm-20250524-macm4pro-arm64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-base-mem.svg) |
| [2025-05-24](results/bm-20250524-3.15.0a0-2fd09b0-JIT) | python/2fd09b011031f3c00c34 | 2fd09b0 (JIT) | 1.123x ↑<br>[📄](results/bm-20250524-3.15.0a0-2fd09b0-JIT/bm-20250524-macm4pro-arm64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-3.12.6.md)[📈](results/bm-20250524-3.15.0a0-2fd09b0-JIT/bm-20250524-macm4pro-arm64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-3.12.6.svg) | 1.042x ↑<br>[📄](results/bm-20250524-3.15.0a0-2fd09b0-JIT/bm-20250524-macm4pro-arm64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-3.13.0rc2.md)[📈](results/bm-20250524-3.15.0a0-2fd09b0-JIT/bm-20250524-macm4pro-arm64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-3.13.0rc2.svg) | 1.010x ↑<br>[📄](results/bm-20250524-3.15.0a0-2fd09b0-JIT/bm-20250524-macm4pro-arm64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-base.md)[📈](results/bm-20250524-3.15.0a0-2fd09b0-JIT/bm-20250524-macm4pro-arm64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-base.svg)[🧠](results/bm-20250524-3.15.0a0-2fd09b0-JIT/bm-20250524-macm4pro-arm64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-base-mem.svg) |
| [2025-05-24](results/bm-20250524-3.15.0a0-2fd09b0-CLANG) | python/2fd09b011031f3c00c34 | 2fd09b0 (CLANG) | 1.150x ↑<br>[📄](results/bm-20250524-3.15.0a0-2fd09b0-CLANG/bm-20250524-macm4pro-arm64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-3.12.6.md)[📈](results/bm-20250524-3.15.0a0-2fd09b0-CLANG/bm-20250524-macm4pro-arm64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-3.12.6.svg) | 1.067x ↑<br>[📄](results/bm-20250524-3.15.0a0-2fd09b0-CLANG/bm-20250524-macm4pro-arm64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-3.13.0rc2.md)[📈](results/bm-20250524-3.15.0a0-2fd09b0-CLANG/bm-20250524-macm4pro-arm64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-3.13.0rc2.svg) | 1.037x ↑<br>[📄](results/bm-20250524-3.15.0a0-2fd09b0-CLANG/bm-20250524-macm4pro-arm64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-base.md)[📈](results/bm-20250524-3.15.0a0-2fd09b0-CLANG/bm-20250524-macm4pro-arm64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-base.svg)[🧠](results/bm-20250524-3.15.0a0-2fd09b0-CLANG/bm-20250524-macm4pro-arm64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-base-mem.svg) |
| [2025-05-24](results/bm-20250524-3.15.0a0-2fd09b0) | python/2fd09b011031f3c00c34 | 2fd09b0 | 1.112x ↑<br>[📄](results/bm-20250524-3.15.0a0-2fd09b0/bm-20250524-macm4pro-arm64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-3.12.6.md)[📈](results/bm-20250524-3.15.0a0-2fd09b0/bm-20250524-macm4pro-arm64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-3.12.6.svg) | 1.031x ↑<br>[📄](results/bm-20250524-3.15.0a0-2fd09b0/bm-20250524-macm4pro-arm64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-3.13.0rc2.md)[📈](results/bm-20250524-3.15.0a0-2fd09b0/bm-20250524-macm4pro-arm64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-3.13.0rc2.svg) |  |
| [2025-05-23](results/bm-20250523-3.15.0a0-f478331-NOGIL) | python/f478331f98930d94f7ef | f478331 (NOGIL) | 1.105x ↑<br>[📄](results/bm-20250523-3.15.0a0-f478331-NOGIL/bm-20250523-macm4pro-arm64-python-f478331f98930d94f7ef-3.15.0a0-f478331-vs-3.12.6.md)[📈](results/bm-20250523-3.15.0a0-f478331-NOGIL/bm-20250523-macm4pro-arm64-python-f478331f98930d94f7ef-3.15.0a0-f478331-vs-3.12.6.svg) | 1.024x ↑<br>[📄](results/bm-20250523-3.15.0a0-f478331-NOGIL/bm-20250523-macm4pro-arm64-python-f478331f98930d94f7ef-3.15.0a0-f478331-vs-3.13.0rc2.md)[📈](results/bm-20250523-3.15.0a0-f478331-NOGIL/bm-20250523-macm4pro-arm64-python-f478331f98930d94f7ef-3.15.0a0-f478331-vs-3.13.0rc2.svg) | 1.022x ↓<br>[📄](results/bm-20250523-3.15.0a0-f478331-NOGIL/bm-20250523-macm4pro-arm64-python-f478331f98930d94f7ef-3.15.0a0-f478331-vs-base.md)[📈](results/bm-20250523-3.15.0a0-f478331-NOGIL/bm-20250523-macm4pro-arm64-python-f478331f98930d94f7ef-3.15.0a0-f478331-vs-base.svg)[🧠](results/bm-20250523-3.15.0a0-f478331-NOGIL/bm-20250523-macm4pro-arm64-python-f478331f98930d94f7ef-3.15.0a0-f478331-vs-base-mem.svg) |
| [2025-05-23](results/bm-20250523-3.15.0a0-f478331) | python/f478331f98930d94f7ef | f478331 | 1.127x ↑<br>[📄](results/bm-20250523-3.15.0a0-f478331/bm-20250523-macm4pro-arm64-python-f478331f98930d94f7ef-3.15.0a0-f478331-vs-3.12.6.md)[📈](results/bm-20250523-3.15.0a0-f478331/bm-20250523-macm4pro-arm64-python-f478331f98930d94f7ef-3.15.0a0-f478331-vs-3.12.6.svg) | 1.045x ↑<br>[📄](results/bm-20250523-3.15.0a0-f478331/bm-20250523-macm4pro-arm64-python-f478331f98930d94f7ef-3.15.0a0-f478331-vs-3.13.0rc2.md)[📈](results/bm-20250523-3.15.0a0-f478331/bm-20250523-macm4pro-arm64-python-f478331f98930d94f7ef-3.15.0a0-f478331-vs-3.13.0rc2.svg) |  |
| [2025-05-22](results/bm-20250522-3.15.0a0-a3d0306-NOGIL) | python/a3d0306ca08d09b1417d | a3d0306 (NOGIL) | 1.092x ↑<br>[📄](results/bm-20250522-3.15.0a0-a3d0306-NOGIL/bm-20250522-macm4pro-arm64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306-vs-3.12.6.md)[📈](results/bm-20250522-3.15.0a0-a3d0306-NOGIL/bm-20250522-macm4pro-arm64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306-vs-3.12.6.svg) | 1.012x ↑<br>[📄](results/bm-20250522-3.15.0a0-a3d0306-NOGIL/bm-20250522-macm4pro-arm64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306-vs-3.13.0rc2.md)[📈](results/bm-20250522-3.15.0a0-a3d0306-NOGIL/bm-20250522-macm4pro-arm64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306-vs-3.13.0rc2.svg) | 1.016x ↓<br>[📄](results/bm-20250522-3.15.0a0-a3d0306-NOGIL/bm-20250522-macm4pro-arm64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306-vs-base.md)[📈](results/bm-20250522-3.15.0a0-a3d0306-NOGIL/bm-20250522-macm4pro-arm64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306-vs-base.svg)[🧠](results/bm-20250522-3.15.0a0-a3d0306-NOGIL/bm-20250522-macm4pro-arm64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306-vs-base-mem.svg) |
| [2025-05-22](results/bm-20250522-3.15.0a0-a3d0306) | python/a3d0306ca08d09b1417d | a3d0306 | 1.107x ↑<br>[📄](results/bm-20250522-3.15.0a0-a3d0306/bm-20250522-macm4pro-arm64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306-vs-3.12.6.md)[📈](results/bm-20250522-3.15.0a0-a3d0306/bm-20250522-macm4pro-arm64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306-vs-3.12.6.svg) | 1.027x ↑<br>[📄](results/bm-20250522-3.15.0a0-a3d0306/bm-20250522-macm4pro-arm64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306-vs-3.13.0rc2.md)[📈](results/bm-20250522-3.15.0a0-a3d0306/bm-20250522-macm4pro-arm64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306-vs-3.13.0rc2.svg) |  |


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
