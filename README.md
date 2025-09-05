# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (d3d94e0)](results/bm-20250830-3.15.0a0-d3d94e0/bm-20250830-vultr-x86_64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (d3d94e0)](results/bm-20250830-3.15.0a0-d3d94e0-PYTHON_UOPS/bm-20250830-vultr-x86_64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-09-04](results/bm-20250904-3.15.0a0-fc0305a-NOGIL) | python/fc0305a2d8bef7cffaa4 | fc0305a (NOGIL) | 1.022x ↓<br>[📄](results/bm-20250904-3.15.0a0-fc0305a-NOGIL/bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a-vs-3.12.6.md)[📈](results/bm-20250904-3.15.0a0-fc0305a-NOGIL/bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a-vs-3.12.6.svg) | 1.054x ↓<br>[📄](results/bm-20250904-3.15.0a0-fc0305a-NOGIL/bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a-vs-3.13.0rc2.md)[📈](results/bm-20250904-3.15.0a0-fc0305a-NOGIL/bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a-vs-3.13.0rc2.svg) | 1.093x ↓<br>[📄](results/bm-20250904-3.15.0a0-fc0305a-NOGIL/bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a-vs-base.md)[📈](results/bm-20250904-3.15.0a0-fc0305a-NOGIL/bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a-vs-base.svg)[🧠](results/bm-20250904-3.15.0a0-fc0305a-NOGIL/bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a-vs-base-mem.svg) |
| [2025-09-04](results/bm-20250904-3.15.0a0-fc0305a) | python/fc0305a2d8bef7cffaa4 | fc0305a | 1.071x ↑<br>[📄](results/bm-20250904-3.15.0a0-fc0305a/bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a-vs-3.12.6.md)[📈](results/bm-20250904-3.15.0a0-fc0305a/bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a-vs-3.12.6.svg) | 1.036x ↑<br>[📄](results/bm-20250904-3.15.0a0-fc0305a/bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a-vs-3.13.0rc2.md)[📈](results/bm-20250904-3.15.0a0-fc0305a/bm-20250904-vultr-x86_64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a-vs-3.13.0rc2.svg) |  |
| [2025-09-04](results/bm-20250904-3.15.0a0-06f8d7a-NOGIL) | python/06f8d7aa9f448128d6eb | 06f8d7a (NOGIL) | 1.023x ↓<br>[📄](results/bm-20250904-3.15.0a0-06f8d7a-NOGIL/bm-20250904-vultr-x86_64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a-vs-3.12.6.md)[📈](results/bm-20250904-3.15.0a0-06f8d7a-NOGIL/bm-20250904-vultr-x86_64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a-vs-3.12.6.svg) | 1.056x ↓<br>[📄](results/bm-20250904-3.15.0a0-06f8d7a-NOGIL/bm-20250904-vultr-x86_64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a-vs-3.13.0rc2.md)[📈](results/bm-20250904-3.15.0a0-06f8d7a-NOGIL/bm-20250904-vultr-x86_64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a-vs-3.13.0rc2.svg) | 1.091x ↓<br>[📄](results/bm-20250904-3.15.0a0-06f8d7a-NOGIL/bm-20250904-vultr-x86_64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a-vs-base.md)[📈](results/bm-20250904-3.15.0a0-06f8d7a-NOGIL/bm-20250904-vultr-x86_64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a-vs-base.svg)[🧠](results/bm-20250904-3.15.0a0-06f8d7a-NOGIL/bm-20250904-vultr-x86_64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a-vs-base-mem.svg) |
| [2025-09-04](results/bm-20250904-3.15.0a0-06f8d7a) | python/06f8d7aa9f448128d6eb | 06f8d7a | 1.066x ↑<br>[📄](results/bm-20250904-3.15.0a0-06f8d7a/bm-20250904-vultr-x86_64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a-vs-3.12.6.md)[📈](results/bm-20250904-3.15.0a0-06f8d7a/bm-20250904-vultr-x86_64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a-vs-3.12.6.svg) | 1.031x ↑<br>[📄](results/bm-20250904-3.15.0a0-06f8d7a/bm-20250904-vultr-x86_64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a-vs-3.13.0rc2.md)[📈](results/bm-20250904-3.15.0a0-06f8d7a/bm-20250904-vultr-x86_64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a-vs-3.13.0rc2.svg) |  |
| [2025-09-02](results/bm-20250902-3.15.0a0-98b4cd6-NOGIL) | python/98b4cd6fe9348ac24d5c | 98b4cd6 (NOGIL) | 1.029x ↓<br>[📄](results/bm-20250902-3.15.0a0-98b4cd6-NOGIL/bm-20250902-vultr-x86_64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6-vs-3.12.6.md)[📈](results/bm-20250902-3.15.0a0-98b4cd6-NOGIL/bm-20250902-vultr-x86_64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6-vs-3.12.6.svg) | 1.061x ↓<br>[📄](results/bm-20250902-3.15.0a0-98b4cd6-NOGIL/bm-20250902-vultr-x86_64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6-vs-3.13.0rc2.md)[📈](results/bm-20250902-3.15.0a0-98b4cd6-NOGIL/bm-20250902-vultr-x86_64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6-vs-3.13.0rc2.svg) | 1.094x ↓<br>[📄](results/bm-20250902-3.15.0a0-98b4cd6-NOGIL/bm-20250902-vultr-x86_64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6-vs-base.md)[📈](results/bm-20250902-3.15.0a0-98b4cd6-NOGIL/bm-20250902-vultr-x86_64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6-vs-base.svg)[🧠](results/bm-20250902-3.15.0a0-98b4cd6-NOGIL/bm-20250902-vultr-x86_64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6-vs-base-mem.svg) |
| [2025-09-02](results/bm-20250902-3.15.0a0-98b4cd6) | python/98b4cd6fe9348ac24d5c | 98b4cd6 | 1.065x ↑<br>[📄](results/bm-20250902-3.15.0a0-98b4cd6/bm-20250902-vultr-x86_64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6-vs-3.12.6.md)[📈](results/bm-20250902-3.15.0a0-98b4cd6/bm-20250902-vultr-x86_64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6-vs-3.12.6.svg) | 1.029x ↑<br>[📄](results/bm-20250902-3.15.0a0-98b4cd6/bm-20250902-vultr-x86_64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6-vs-3.13.0rc2.md)[📈](results/bm-20250902-3.15.0a0-98b4cd6/bm-20250902-vultr-x86_64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6-vs-3.13.0rc2.svg) |  |
| [2025-09-01](results/bm-20250901-3.15.0a0-a2ba0a7-NOGIL) | python/a2ba0a7552580f616f74 | a2ba0a7 (NOGIL) | 1.024x ↓<br>[📄](results/bm-20250901-3.15.0a0-a2ba0a7-NOGIL/bm-20250901-vultr-x86_64-python-a2ba0a7552580f616f74-3.15.0a0-a2ba0a7-vs-3.12.6.md)[📈](results/bm-20250901-3.15.0a0-a2ba0a7-NOGIL/bm-20250901-vultr-x86_64-python-a2ba0a7552580f616f74-3.15.0a0-a2ba0a7-vs-3.12.6.svg) | 1.057x ↓<br>[📄](results/bm-20250901-3.15.0a0-a2ba0a7-NOGIL/bm-20250901-vultr-x86_64-python-a2ba0a7552580f616f74-3.15.0a0-a2ba0a7-vs-3.13.0rc2.md)[📈](results/bm-20250901-3.15.0a0-a2ba0a7-NOGIL/bm-20250901-vultr-x86_64-python-a2ba0a7552580f616f74-3.15.0a0-a2ba0a7-vs-3.13.0rc2.svg) | 1.097x ↓<br>[📄](results/bm-20250901-3.15.0a0-a2ba0a7-NOGIL/bm-20250901-vultr-x86_64-python-a2ba0a7552580f616f74-3.15.0a0-a2ba0a7-vs-base.md)[📈](results/bm-20250901-3.15.0a0-a2ba0a7-NOGIL/bm-20250901-vultr-x86_64-python-a2ba0a7552580f616f74-3.15.0a0-a2ba0a7-vs-base.svg)[🧠](results/bm-20250901-3.15.0a0-a2ba0a7-NOGIL/bm-20250901-vultr-x86_64-python-a2ba0a7552580f616f74-3.15.0a0-a2ba0a7-vs-base-mem.svg) |
| [2025-09-01](results/bm-20250901-3.15.0a0-a2ba0a7) | python/a2ba0a7552580f616f74 | a2ba0a7 | 1.074x ↑<br>[📄](results/bm-20250901-3.15.0a0-a2ba0a7/bm-20250901-vultr-x86_64-python-a2ba0a7552580f616f74-3.15.0a0-a2ba0a7-vs-3.12.6.md)[📈](results/bm-20250901-3.15.0a0-a2ba0a7/bm-20250901-vultr-x86_64-python-a2ba0a7552580f616f74-3.15.0a0-a2ba0a7-vs-3.12.6.svg) | 1.038x ↑<br>[📄](results/bm-20250901-3.15.0a0-a2ba0a7/bm-20250901-vultr-x86_64-python-a2ba0a7552580f616f74-3.15.0a0-a2ba0a7-vs-3.13.0rc2.md)[📈](results/bm-20250901-3.15.0a0-a2ba0a7/bm-20250901-vultr-x86_64-python-a2ba0a7552580f616f74-3.15.0a0-a2ba0a7-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-09-04](results/bm-20250904-3.15.0a0-fc0305a-NOGIL) | python/fc0305a2d8bef7cffaa4 | fc0305a (NOGIL) | 1.077x ↑<br>[📄](results/bm-20250904-3.15.0a0-fc0305a-NOGIL/bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a-vs-3.12.6.md)[📈](results/bm-20250904-3.15.0a0-fc0305a-NOGIL/bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a-vs-3.12.6.svg) | 1.001x ↓<br>[📄](results/bm-20250904-3.15.0a0-fc0305a-NOGIL/bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a-vs-3.13.0rc2.md)[📈](results/bm-20250904-3.15.0a0-fc0305a-NOGIL/bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a-vs-3.13.0rc2.svg) | 1.022x ↓<br>[📄](results/bm-20250904-3.15.0a0-fc0305a-NOGIL/bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a-vs-base.md)[📈](results/bm-20250904-3.15.0a0-fc0305a-NOGIL/bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a-vs-base.svg)[🧠](results/bm-20250904-3.15.0a0-fc0305a-NOGIL/bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a-vs-base-mem.svg) |
| [2025-09-04](results/bm-20250904-3.15.0a0-fc0305a) | python/fc0305a2d8bef7cffaa4 | fc0305a | 1.100x ↑<br>[📄](results/bm-20250904-3.15.0a0-fc0305a/bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a-vs-3.12.6.md)[📈](results/bm-20250904-3.15.0a0-fc0305a/bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a-vs-3.12.6.svg) | 1.021x ↑<br>[📄](results/bm-20250904-3.15.0a0-fc0305a/bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a-vs-3.13.0rc2.md)[📈](results/bm-20250904-3.15.0a0-fc0305a/bm-20250904-macm4pro-arm64-python-fc0305a2d8bef7cffaa4-3.15.0a0-fc0305a-vs-3.13.0rc2.svg) |  |
| [2025-09-04](results/bm-20250904-3.15.0a0-06f8d7a-NOGIL) | python/06f8d7aa9f448128d6eb | 06f8d7a (NOGIL) | 1.075x ↑<br>[📄](results/bm-20250904-3.15.0a0-06f8d7a-NOGIL/bm-20250904-macm4pro-arm64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a-vs-3.12.6.md)[📈](results/bm-20250904-3.15.0a0-06f8d7a-NOGIL/bm-20250904-macm4pro-arm64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a-vs-3.12.6.svg) | 1.003x ↓<br>[📄](results/bm-20250904-3.15.0a0-06f8d7a-NOGIL/bm-20250904-macm4pro-arm64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a-vs-3.13.0rc2.md)[📈](results/bm-20250904-3.15.0a0-06f8d7a-NOGIL/bm-20250904-macm4pro-arm64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a-vs-3.13.0rc2.svg) | 1.021x ↓<br>[📄](results/bm-20250904-3.15.0a0-06f8d7a-NOGIL/bm-20250904-macm4pro-arm64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a-vs-base.md)[📈](results/bm-20250904-3.15.0a0-06f8d7a-NOGIL/bm-20250904-macm4pro-arm64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a-vs-base.svg)[🧠](results/bm-20250904-3.15.0a0-06f8d7a-NOGIL/bm-20250904-macm4pro-arm64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a-vs-base-mem.svg) |
| [2025-09-04](results/bm-20250904-3.15.0a0-06f8d7a) | python/06f8d7aa9f448128d6eb | 06f8d7a | 1.095x ↑<br>[📄](results/bm-20250904-3.15.0a0-06f8d7a/bm-20250904-macm4pro-arm64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a-vs-3.12.6.md)[📈](results/bm-20250904-3.15.0a0-06f8d7a/bm-20250904-macm4pro-arm64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a-vs-3.12.6.svg) | 1.016x ↑<br>[📄](results/bm-20250904-3.15.0a0-06f8d7a/bm-20250904-macm4pro-arm64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a-vs-3.13.0rc2.md)[📈](results/bm-20250904-3.15.0a0-06f8d7a/bm-20250904-macm4pro-arm64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a-vs-3.13.0rc2.svg) |  |
| [2025-09-02](results/bm-20250902-3.15.0a0-98b4cd6-NOGIL) | python/98b4cd6fe9348ac24d5c | 98b4cd6 (NOGIL) | 1.075x ↑<br>[📄](results/bm-20250902-3.15.0a0-98b4cd6-NOGIL/bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6-vs-3.12.6.md)[📈](results/bm-20250902-3.15.0a0-98b4cd6-NOGIL/bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6-vs-3.12.6.svg) | 1.003x ↓<br>[📄](results/bm-20250902-3.15.0a0-98b4cd6-NOGIL/bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6-vs-3.13.0rc2.md)[📈](results/bm-20250902-3.15.0a0-98b4cd6-NOGIL/bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6-vs-3.13.0rc2.svg) | 1.022x ↓<br>[📄](results/bm-20250902-3.15.0a0-98b4cd6-NOGIL/bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6-vs-base.md)[📈](results/bm-20250902-3.15.0a0-98b4cd6-NOGIL/bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6-vs-base.svg)[🧠](results/bm-20250902-3.15.0a0-98b4cd6-NOGIL/bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6-vs-base-mem.svg) |
| [2025-09-02](results/bm-20250902-3.15.0a0-98b4cd6) | python/98b4cd6fe9348ac24d5c | 98b4cd6 | 1.096x ↑<br>[📄](results/bm-20250902-3.15.0a0-98b4cd6/bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6-vs-3.12.6.md)[📈](results/bm-20250902-3.15.0a0-98b4cd6/bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6-vs-3.12.6.svg) | 1.017x ↑<br>[📄](results/bm-20250902-3.15.0a0-98b4cd6/bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6-vs-3.13.0rc2.md)[📈](results/bm-20250902-3.15.0a0-98b4cd6/bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6-vs-3.13.0rc2.svg) |  |
| [2025-09-01](results/bm-20250901-3.15.0a0-a2ba0a7-NOGIL) | python/a2ba0a7552580f616f74 | a2ba0a7 (NOGIL) | 1.076x ↑<br>[📄](results/bm-20250901-3.15.0a0-a2ba0a7-NOGIL/bm-20250901-macm4pro-arm64-python-a2ba0a7552580f616f74-3.15.0a0-a2ba0a7-vs-3.12.6.md)[📈](results/bm-20250901-3.15.0a0-a2ba0a7-NOGIL/bm-20250901-macm4pro-arm64-python-a2ba0a7552580f616f74-3.15.0a0-a2ba0a7-vs-3.12.6.svg) | 1.001x ↓<br>[📄](results/bm-20250901-3.15.0a0-a2ba0a7-NOGIL/bm-20250901-macm4pro-arm64-python-a2ba0a7552580f616f74-3.15.0a0-a2ba0a7-vs-3.13.0rc2.md)[📈](results/bm-20250901-3.15.0a0-a2ba0a7-NOGIL/bm-20250901-macm4pro-arm64-python-a2ba0a7552580f616f74-3.15.0a0-a2ba0a7-vs-3.13.0rc2.svg) | 1.024x ↓<br>[📄](results/bm-20250901-3.15.0a0-a2ba0a7-NOGIL/bm-20250901-macm4pro-arm64-python-a2ba0a7552580f616f74-3.15.0a0-a2ba0a7-vs-base.md)[📈](results/bm-20250901-3.15.0a0-a2ba0a7-NOGIL/bm-20250901-macm4pro-arm64-python-a2ba0a7552580f616f74-3.15.0a0-a2ba0a7-vs-base.svg)[🧠](results/bm-20250901-3.15.0a0-a2ba0a7-NOGIL/bm-20250901-macm4pro-arm64-python-a2ba0a7552580f616f74-3.15.0a0-a2ba0a7-vs-base-mem.svg) |
| [2025-09-01](results/bm-20250901-3.15.0a0-a2ba0a7) | python/a2ba0a7552580f616f74 | a2ba0a7 | 1.101x ↑<br>[📄](results/bm-20250901-3.15.0a0-a2ba0a7/bm-20250901-macm4pro-arm64-python-a2ba0a7552580f616f74-3.15.0a0-a2ba0a7-vs-3.12.6.md)[📈](results/bm-20250901-3.15.0a0-a2ba0a7/bm-20250901-macm4pro-arm64-python-a2ba0a7552580f616f74-3.15.0a0-a2ba0a7-vs-3.12.6.svg) | 1.021x ↑<br>[📄](results/bm-20250901-3.15.0a0-a2ba0a7/bm-20250901-macm4pro-arm64-python-a2ba0a7552580f616f74-3.15.0a0-a2ba0a7-vs-3.13.0rc2.md)[📈](results/bm-20250901-3.15.0a0-a2ba0a7/bm-20250901-macm4pro-arm64-python-a2ba0a7552580f616f74-3.15.0a0-a2ba0a7-vs-3.13.0rc2.svg) |  |


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
