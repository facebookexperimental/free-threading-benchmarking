# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (2e15a50)](results/bm-20250614-3.15.0a0-2e15a50/bm-20250614-vultr-x86_64-python-2e15a50851da66eb8227-3.15.0a0-2e15a50-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (2e15a50)](results/bm-20250614-3.15.0a0-2e15a50-PYTHON_UOPS/bm-20250614-vultr-x86_64-python-2e15a50851da66eb8227-3.15.0a0-2e15a50-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-06-20](results/bm-20250620-3.15.0a0-4ddf505-NOGIL) | python/4ddf505d9982dc8afead | 4ddf505 (NOGIL) | 1.019x ↑<br>[📄](results/bm-20250620-3.15.0a0-4ddf505-NOGIL/bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505-vs-3.12.6.md)[📈](results/bm-20250620-3.15.0a0-4ddf505-NOGIL/bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505-vs-3.12.6.svg) | 1.017x ↓<br>[📄](results/bm-20250620-3.15.0a0-4ddf505-NOGIL/bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505-vs-3.13.0rc2.md)[📈](results/bm-20250620-3.15.0a0-4ddf505-NOGIL/bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505-vs-3.13.0rc2.svg) | 1.087x ↓<br>[📄](results/bm-20250620-3.15.0a0-4ddf505-NOGIL/bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505-vs-base.md)[📈](results/bm-20250620-3.15.0a0-4ddf505-NOGIL/bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505-vs-base.svg)[🧠](results/bm-20250620-3.15.0a0-4ddf505-NOGIL/bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505-vs-base-mem.svg) |
| [2025-06-20](results/bm-20250620-3.15.0a0-4ddf505) | python/4ddf505d9982dc8afead | 4ddf505 | 1.108x ↑<br>[📄](results/bm-20250620-3.15.0a0-4ddf505/bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505-vs-3.12.6.md)[📈](results/bm-20250620-3.15.0a0-4ddf505/bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505-vs-3.12.6.svg) | 1.070x ↑<br>[📄](results/bm-20250620-3.15.0a0-4ddf505/bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505-vs-3.13.0rc2.md)[📈](results/bm-20250620-3.15.0a0-4ddf505/bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505-vs-3.13.0rc2.svg) |  |
| [2025-06-20](results/bm-20250620-3.15.0a0-c8c13f8-NOGIL) | python/c8c13f8036051c285895 | c8c13f8 (NOGIL) | 1.013x ↑<br>[📄](results/bm-20250620-3.15.0a0-c8c13f8-NOGIL/bm-20250620-vultr-x86_64-python-c8c13f8036051c285895-3.15.0a0-c8c13f8-vs-3.12.6.md)[📈](results/bm-20250620-3.15.0a0-c8c13f8-NOGIL/bm-20250620-vultr-x86_64-python-c8c13f8036051c285895-3.15.0a0-c8c13f8-vs-3.12.6.svg) | 1.022x ↓<br>[📄](results/bm-20250620-3.15.0a0-c8c13f8-NOGIL/bm-20250620-vultr-x86_64-python-c8c13f8036051c285895-3.15.0a0-c8c13f8-vs-3.13.0rc2.md)[📈](results/bm-20250620-3.15.0a0-c8c13f8-NOGIL/bm-20250620-vultr-x86_64-python-c8c13f8036051c285895-3.15.0a0-c8c13f8-vs-3.13.0rc2.svg) | 1.094x ↓<br>[📄](results/bm-20250620-3.15.0a0-c8c13f8-NOGIL/bm-20250620-vultr-x86_64-python-c8c13f8036051c285895-3.15.0a0-c8c13f8-vs-base.md)[📈](results/bm-20250620-3.15.0a0-c8c13f8-NOGIL/bm-20250620-vultr-x86_64-python-c8c13f8036051c285895-3.15.0a0-c8c13f8-vs-base.svg)[🧠](results/bm-20250620-3.15.0a0-c8c13f8-NOGIL/bm-20250620-vultr-x86_64-python-c8c13f8036051c285895-3.15.0a0-c8c13f8-vs-base-mem.svg) |
| [2025-06-20](results/bm-20250620-3.15.0a0-c8c13f8) | python/c8c13f8036051c285895 | c8c13f8 | 1.113x ↑<br>[📄](results/bm-20250620-3.15.0a0-c8c13f8/bm-20250620-vultr-x86_64-python-c8c13f8036051c285895-3.15.0a0-c8c13f8-vs-3.12.6.md)[📈](results/bm-20250620-3.15.0a0-c8c13f8/bm-20250620-vultr-x86_64-python-c8c13f8036051c285895-3.15.0a0-c8c13f8-vs-3.12.6.svg) | 1.075x ↑<br>[📄](results/bm-20250620-3.15.0a0-c8c13f8/bm-20250620-vultr-x86_64-python-c8c13f8036051c285895-3.15.0a0-c8c13f8-vs-3.13.0rc2.md)[📈](results/bm-20250620-3.15.0a0-c8c13f8/bm-20250620-vultr-x86_64-python-c8c13f8036051c285895-3.15.0a0-c8c13f8-vs-3.13.0rc2.svg) |  |
| [2025-06-18](results/bm-20250618-3.15.0a0-725da50-NOGIL) | python/725da50520c5cc3002f6 | 725da50 (NOGIL) | 1.010x ↑<br>[📄](results/bm-20250618-3.15.0a0-725da50-NOGIL/bm-20250618-vultr-x86_64-python-725da50520c5cc3002f6-3.15.0a0-725da50-vs-3.12.6.md)[📈](results/bm-20250618-3.15.0a0-725da50-NOGIL/bm-20250618-vultr-x86_64-python-725da50520c5cc3002f6-3.15.0a0-725da50-vs-3.12.6.svg) | 1.025x ↓<br>[📄](results/bm-20250618-3.15.0a0-725da50-NOGIL/bm-20250618-vultr-x86_64-python-725da50520c5cc3002f6-3.15.0a0-725da50-vs-3.13.0rc2.md)[📈](results/bm-20250618-3.15.0a0-725da50-NOGIL/bm-20250618-vultr-x86_64-python-725da50520c5cc3002f6-3.15.0a0-725da50-vs-3.13.0rc2.svg) | 1.088x ↓<br>[📄](results/bm-20250618-3.15.0a0-725da50-NOGIL/bm-20250618-vultr-x86_64-python-725da50520c5cc3002f6-3.15.0a0-725da50-vs-base.md)[📈](results/bm-20250618-3.15.0a0-725da50-NOGIL/bm-20250618-vultr-x86_64-python-725da50520c5cc3002f6-3.15.0a0-725da50-vs-base.svg)[🧠](results/bm-20250618-3.15.0a0-725da50-NOGIL/bm-20250618-vultr-x86_64-python-725da50520c5cc3002f6-3.15.0a0-725da50-vs-base-mem.svg) |
| [2025-06-18](results/bm-20250618-3.15.0a0-725da50) | python/725da50520c5cc3002f6 | 725da50 | 1.102x ↑<br>[📄](results/bm-20250618-3.15.0a0-725da50/bm-20250618-vultr-x86_64-python-725da50520c5cc3002f6-3.15.0a0-725da50-vs-3.12.6.md)[📈](results/bm-20250618-3.15.0a0-725da50/bm-20250618-vultr-x86_64-python-725da50520c5cc3002f6-3.15.0a0-725da50-vs-3.12.6.svg) | 1.064x ↑<br>[📄](results/bm-20250618-3.15.0a0-725da50/bm-20250618-vultr-x86_64-python-725da50520c5cc3002f6-3.15.0a0-725da50-vs-3.13.0rc2.md)[📈](results/bm-20250618-3.15.0a0-725da50/bm-20250618-vultr-x86_64-python-725da50520c5cc3002f6-3.15.0a0-725da50-vs-3.13.0rc2.svg) |  |
| [2025-06-18](results/bm-20250618-3.15.0a0-52be7f4-NOGIL) | python/52be7f445e454ccb44e3 | 52be7f4 (NOGIL) | 1.014x ↑<br>[📄](results/bm-20250618-3.15.0a0-52be7f4-NOGIL/bm-20250618-vultr-x86_64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4-vs-3.12.6.md)[📈](results/bm-20250618-3.15.0a0-52be7f4-NOGIL/bm-20250618-vultr-x86_64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4-vs-3.12.6.svg) | 1.022x ↓<br>[📄](results/bm-20250618-3.15.0a0-52be7f4-NOGIL/bm-20250618-vultr-x86_64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4-vs-3.13.0rc2.md)[📈](results/bm-20250618-3.15.0a0-52be7f4-NOGIL/bm-20250618-vultr-x86_64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4-vs-3.13.0rc2.svg) | 1.092x ↓<br>[📄](results/bm-20250618-3.15.0a0-52be7f4-NOGIL/bm-20250618-vultr-x86_64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4-vs-base.md)[📈](results/bm-20250618-3.15.0a0-52be7f4-NOGIL/bm-20250618-vultr-x86_64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4-vs-base.svg)[🧠](results/bm-20250618-3.15.0a0-52be7f4-NOGIL/bm-20250618-vultr-x86_64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4-vs-base-mem.svg) |
| [2025-06-18](results/bm-20250618-3.15.0a0-52be7f4) | python/52be7f445e454ccb44e3 | 52be7f4 | 1.110x ↑<br>[📄](results/bm-20250618-3.15.0a0-52be7f4/bm-20250618-vultr-x86_64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4-vs-3.12.6.md)[📈](results/bm-20250618-3.15.0a0-52be7f4/bm-20250618-vultr-x86_64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4-vs-3.12.6.svg) | 1.072x ↑<br>[📄](results/bm-20250618-3.15.0a0-52be7f4/bm-20250618-vultr-x86_64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4-vs-3.13.0rc2.md)[📈](results/bm-20250618-3.15.0a0-52be7f4/bm-20250618-vultr-x86_64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-06-20](results/bm-20250620-3.15.0a0-4ddf505-NOGIL) | python/4ddf505d9982dc8afead | 4ddf505 (NOGIL) | 1.096x ↑<br>[📄](results/bm-20250620-3.15.0a0-4ddf505-NOGIL/bm-20250620-macm4pro-arm64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505-vs-3.12.6.md)[📈](results/bm-20250620-3.15.0a0-4ddf505-NOGIL/bm-20250620-macm4pro-arm64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505-vs-3.12.6.svg) | 1.017x ↑<br>[📄](results/bm-20250620-3.15.0a0-4ddf505-NOGIL/bm-20250620-macm4pro-arm64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505-vs-3.13.0rc2.md)[📈](results/bm-20250620-3.15.0a0-4ddf505-NOGIL/bm-20250620-macm4pro-arm64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505-vs-3.13.0rc2.svg) | 1.008x ↓<br>[📄](results/bm-20250620-3.15.0a0-4ddf505-NOGIL/bm-20250620-macm4pro-arm64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505-vs-base.md)[📈](results/bm-20250620-3.15.0a0-4ddf505-NOGIL/bm-20250620-macm4pro-arm64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505-vs-base.svg)[🧠](results/bm-20250620-3.15.0a0-4ddf505-NOGIL/bm-20250620-macm4pro-arm64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505-vs-base-mem.svg) |
| [2025-06-20](results/bm-20250620-3.15.0a0-4ddf505) | python/4ddf505d9982dc8afead | 4ddf505 | 1.103x ↑<br>[📄](results/bm-20250620-3.15.0a0-4ddf505/bm-20250620-macm4pro-arm64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505-vs-3.12.6.md)[📈](results/bm-20250620-3.15.0a0-4ddf505/bm-20250620-macm4pro-arm64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505-vs-3.12.6.svg) | 1.023x ↑<br>[📄](results/bm-20250620-3.15.0a0-4ddf505/bm-20250620-macm4pro-arm64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505-vs-3.13.0rc2.md)[📈](results/bm-20250620-3.15.0a0-4ddf505/bm-20250620-macm4pro-arm64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505-vs-3.13.0rc2.svg) |  |
| [2025-06-20](results/bm-20250620-3.15.0a0-c8c13f8-NOGIL) | python/c8c13f8036051c285895 | c8c13f8 (NOGIL) | 1.094x ↑<br>[📄](results/bm-20250620-3.15.0a0-c8c13f8-NOGIL/bm-20250620-macm4pro-arm64-python-c8c13f8036051c285895-3.15.0a0-c8c13f8-vs-3.12.6.md)[📈](results/bm-20250620-3.15.0a0-c8c13f8-NOGIL/bm-20250620-macm4pro-arm64-python-c8c13f8036051c285895-3.15.0a0-c8c13f8-vs-3.12.6.svg) | 1.015x ↑<br>[📄](results/bm-20250620-3.15.0a0-c8c13f8-NOGIL/bm-20250620-macm4pro-arm64-python-c8c13f8036051c285895-3.15.0a0-c8c13f8-vs-3.13.0rc2.md)[📈](results/bm-20250620-3.15.0a0-c8c13f8-NOGIL/bm-20250620-macm4pro-arm64-python-c8c13f8036051c285895-3.15.0a0-c8c13f8-vs-3.13.0rc2.svg) | 1.015x ↓<br>[📄](results/bm-20250620-3.15.0a0-c8c13f8-NOGIL/bm-20250620-macm4pro-arm64-python-c8c13f8036051c285895-3.15.0a0-c8c13f8-vs-base.md)[📈](results/bm-20250620-3.15.0a0-c8c13f8-NOGIL/bm-20250620-macm4pro-arm64-python-c8c13f8036051c285895-3.15.0a0-c8c13f8-vs-base.svg)[🧠](results/bm-20250620-3.15.0a0-c8c13f8-NOGIL/bm-20250620-macm4pro-arm64-python-c8c13f8036051c285895-3.15.0a0-c8c13f8-vs-base-mem.svg) |
| [2025-06-20](results/bm-20250620-3.15.0a0-c8c13f8) | python/c8c13f8036051c285895 | c8c13f8 | 1.109x ↑<br>[📄](results/bm-20250620-3.15.0a0-c8c13f8/bm-20250620-macm4pro-arm64-python-c8c13f8036051c285895-3.15.0a0-c8c13f8-vs-3.12.6.md)[📈](results/bm-20250620-3.15.0a0-c8c13f8/bm-20250620-macm4pro-arm64-python-c8c13f8036051c285895-3.15.0a0-c8c13f8-vs-3.12.6.svg) | 1.029x ↑<br>[📄](results/bm-20250620-3.15.0a0-c8c13f8/bm-20250620-macm4pro-arm64-python-c8c13f8036051c285895-3.15.0a0-c8c13f8-vs-3.13.0rc2.md)[📈](results/bm-20250620-3.15.0a0-c8c13f8/bm-20250620-macm4pro-arm64-python-c8c13f8036051c285895-3.15.0a0-c8c13f8-vs-3.13.0rc2.svg) |  |
| [2025-06-18](results/bm-20250618-3.15.0a0-725da50-NOGIL) | python/725da50520c5cc3002f6 | 725da50 (NOGIL) | 1.090x ↑<br>[📄](results/bm-20250618-3.15.0a0-725da50-NOGIL/bm-20250618-macm4pro-arm64-python-725da50520c5cc3002f6-3.15.0a0-725da50-vs-3.12.6.md)[📈](results/bm-20250618-3.15.0a0-725da50-NOGIL/bm-20250618-macm4pro-arm64-python-725da50520c5cc3002f6-3.15.0a0-725da50-vs-3.12.6.svg) | 1.011x ↑<br>[📄](results/bm-20250618-3.15.0a0-725da50-NOGIL/bm-20250618-macm4pro-arm64-python-725da50520c5cc3002f6-3.15.0a0-725da50-vs-3.13.0rc2.md)[📈](results/bm-20250618-3.15.0a0-725da50-NOGIL/bm-20250618-macm4pro-arm64-python-725da50520c5cc3002f6-3.15.0a0-725da50-vs-3.13.0rc2.svg) | 1.019x ↓<br>[📄](results/bm-20250618-3.15.0a0-725da50-NOGIL/bm-20250618-macm4pro-arm64-python-725da50520c5cc3002f6-3.15.0a0-725da50-vs-base.md)[📈](results/bm-20250618-3.15.0a0-725da50-NOGIL/bm-20250618-macm4pro-arm64-python-725da50520c5cc3002f6-3.15.0a0-725da50-vs-base.svg)[🧠](results/bm-20250618-3.15.0a0-725da50-NOGIL/bm-20250618-macm4pro-arm64-python-725da50520c5cc3002f6-3.15.0a0-725da50-vs-base-mem.svg) |
| [2025-06-18](results/bm-20250618-3.15.0a0-725da50) | python/725da50520c5cc3002f6 | 725da50 | 1.109x ↑<br>[📄](results/bm-20250618-3.15.0a0-725da50/bm-20250618-macm4pro-arm64-python-725da50520c5cc3002f6-3.15.0a0-725da50-vs-3.12.6.md)[📈](results/bm-20250618-3.15.0a0-725da50/bm-20250618-macm4pro-arm64-python-725da50520c5cc3002f6-3.15.0a0-725da50-vs-3.12.6.svg) | 1.029x ↑<br>[📄](results/bm-20250618-3.15.0a0-725da50/bm-20250618-macm4pro-arm64-python-725da50520c5cc3002f6-3.15.0a0-725da50-vs-3.13.0rc2.md)[📈](results/bm-20250618-3.15.0a0-725da50/bm-20250618-macm4pro-arm64-python-725da50520c5cc3002f6-3.15.0a0-725da50-vs-3.13.0rc2.svg) |  |
| [2025-06-18](results/bm-20250618-3.15.0a0-52be7f4-NOGIL) | python/52be7f445e454ccb44e3 | 52be7f4 (NOGIL) | 1.089x ↑<br>[📄](results/bm-20250618-3.15.0a0-52be7f4-NOGIL/bm-20250618-macm4pro-arm64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4-vs-3.12.6.md)[📈](results/bm-20250618-3.15.0a0-52be7f4-NOGIL/bm-20250618-macm4pro-arm64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4-vs-3.12.6.svg) | 1.011x ↑<br>[📄](results/bm-20250618-3.15.0a0-52be7f4-NOGIL/bm-20250618-macm4pro-arm64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4-vs-3.13.0rc2.md)[📈](results/bm-20250618-3.15.0a0-52be7f4-NOGIL/bm-20250618-macm4pro-arm64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4-vs-3.13.0rc2.svg) | 1.013x ↓<br>[📄](results/bm-20250618-3.15.0a0-52be7f4-NOGIL/bm-20250618-macm4pro-arm64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4-vs-base.md)[📈](results/bm-20250618-3.15.0a0-52be7f4-NOGIL/bm-20250618-macm4pro-arm64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4-vs-base.svg)[🧠](results/bm-20250618-3.15.0a0-52be7f4-NOGIL/bm-20250618-macm4pro-arm64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4-vs-base-mem.svg) |
| [2025-06-18](results/bm-20250618-3.15.0a0-52be7f4) | python/52be7f445e454ccb44e3 | 52be7f4 | 1.102x ↑<br>[📄](results/bm-20250618-3.15.0a0-52be7f4/bm-20250618-macm4pro-arm64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4-vs-3.12.6.md)[📈](results/bm-20250618-3.15.0a0-52be7f4/bm-20250618-macm4pro-arm64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4-vs-3.12.6.svg) | 1.022x ↑<br>[📄](results/bm-20250618-3.15.0a0-52be7f4/bm-20250618-macm4pro-arm64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4-vs-3.13.0rc2.md)[📈](results/bm-20250618-3.15.0a0-52be7f4/bm-20250618-macm4pro-arm64-python-52be7f445e454ccb44e3-3.15.0a0-52be7f4-vs-3.13.0rc2.svg) |  |


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
