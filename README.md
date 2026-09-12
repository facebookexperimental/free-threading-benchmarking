# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (7a91841)](results/bm-20260905-3.16.0a0-7a91841/bm-20260905-vultr-x86_64-python-7a918411a300ddeef06d-3.16.0a0-7a91841-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (7a91841)](results/bm-20260905-3.16.0a0-7a91841-PYTHON_UOPS/bm-20260905-vultr-x86_64-python-7a918411a300ddeef06d-3.16.0a0-7a91841-pystats.md)
- [Most recent JIT pystats on main (bedaea0)](results/bm-20251019-3.15.0a1%2B-bedaea0-JIT/bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-09-11](results/bm-20260911-3.16.0a0-f5dd52d-NOGIL) | python/f5dd52df16e1b3f3f8cc | f5dd52d (NOGIL) | 1.053x ↓<br>[📄](results/bm-20260911-3.16.0a0-f5dd52d-NOGIL/bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d-vs-3.12.6.md)[📈](results/bm-20260911-3.16.0a0-f5dd52d-NOGIL/bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d-vs-3.12.6.svg) | 1.085x ↓<br>[📄](results/bm-20260911-3.16.0a0-f5dd52d-NOGIL/bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d-vs-3.13.0rc2.md)[📈](results/bm-20260911-3.16.0a0-f5dd52d-NOGIL/bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d-vs-3.13.0rc2.svg) | 1.108x ↓<br>[📄](results/bm-20260911-3.16.0a0-f5dd52d-NOGIL/bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d-vs-base.md)[📈](results/bm-20260911-3.16.0a0-f5dd52d-NOGIL/bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d-vs-base.svg)[🧠](results/bm-20260911-3.16.0a0-f5dd52d-NOGIL/bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d-vs-base-mem.svg) |
| [2026-09-11](results/bm-20260911-3.16.0a0-f5dd52d) | python/f5dd52df16e1b3f3f8cc | f5dd52d | 1.056x ↑<br>[📄](results/bm-20260911-3.16.0a0-f5dd52d/bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d-vs-3.12.6.md)[📈](results/bm-20260911-3.16.0a0-f5dd52d/bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d-vs-3.12.6.svg) | 1.021x ↑<br>[📄](results/bm-20260911-3.16.0a0-f5dd52d/bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d-vs-3.13.0rc2.md)[📈](results/bm-20260911-3.16.0a0-f5dd52d/bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d-vs-3.13.0rc2.svg) |  |
| [2026-09-10](results/bm-20260910-3.16.0a0-8f84787-NOGIL) | python/8f847875d60c81841e18 | 8f84787 (NOGIL) | 1.052x ↓<br>[📄](results/bm-20260910-3.16.0a0-8f84787-NOGIL/bm-20260910-vultr-x86_64-python-8f847875d60c81841e18-3.16.0a0-8f84787-vs-3.12.6.md)[📈](results/bm-20260910-3.16.0a0-8f84787-NOGIL/bm-20260910-vultr-x86_64-python-8f847875d60c81841e18-3.16.0a0-8f84787-vs-3.12.6.svg) | 1.083x ↓<br>[📄](results/bm-20260910-3.16.0a0-8f84787-NOGIL/bm-20260910-vultr-x86_64-python-8f847875d60c81841e18-3.16.0a0-8f84787-vs-3.13.0rc2.md)[📈](results/bm-20260910-3.16.0a0-8f84787-NOGIL/bm-20260910-vultr-x86_64-python-8f847875d60c81841e18-3.16.0a0-8f84787-vs-3.13.0rc2.svg) | 1.113x ↓<br>[📄](results/bm-20260910-3.16.0a0-8f84787-NOGIL/bm-20260910-vultr-x86_64-python-8f847875d60c81841e18-3.16.0a0-8f84787-vs-base.md)[📈](results/bm-20260910-3.16.0a0-8f84787-NOGIL/bm-20260910-vultr-x86_64-python-8f847875d60c81841e18-3.16.0a0-8f84787-vs-base.svg)[🧠](results/bm-20260910-3.16.0a0-8f84787-NOGIL/bm-20260910-vultr-x86_64-python-8f847875d60c81841e18-3.16.0a0-8f84787-vs-base-mem.svg) |
| [2026-09-10](results/bm-20260910-3.16.0a0-8f84787) | python/8f847875d60c81841e18 | 8f84787 | 1.067x ↑<br>[📄](results/bm-20260910-3.16.0a0-8f84787/bm-20260910-vultr-x86_64-python-8f847875d60c81841e18-3.16.0a0-8f84787-vs-3.12.6.md)[📈](results/bm-20260910-3.16.0a0-8f84787/bm-20260910-vultr-x86_64-python-8f847875d60c81841e18-3.16.0a0-8f84787-vs-3.12.6.svg) | 1.031x ↑<br>[📄](results/bm-20260910-3.16.0a0-8f84787/bm-20260910-vultr-x86_64-python-8f847875d60c81841e18-3.16.0a0-8f84787-vs-3.13.0rc2.md)[📈](results/bm-20260910-3.16.0a0-8f84787/bm-20260910-vultr-x86_64-python-8f847875d60c81841e18-3.16.0a0-8f84787-vs-3.13.0rc2.svg) |  |
| [2026-09-09](results/bm-20260909-3.16.0a0-69a6612-NOGIL) | python/69a6612ff02c022d17f9 | 69a6612 (NOGIL) | 1.046x ↓<br>[📄](results/bm-20260909-3.16.0a0-69a6612-NOGIL/bm-20260909-vultr-x86_64-python-69a6612ff02c022d17f9-3.16.0a0-69a6612-vs-3.12.6.md)[📈](results/bm-20260909-3.16.0a0-69a6612-NOGIL/bm-20260909-vultr-x86_64-python-69a6612ff02c022d17f9-3.16.0a0-69a6612-vs-3.12.6.svg) | 1.077x ↓<br>[📄](results/bm-20260909-3.16.0a0-69a6612-NOGIL/bm-20260909-vultr-x86_64-python-69a6612ff02c022d17f9-3.16.0a0-69a6612-vs-3.13.0rc2.md)[📈](results/bm-20260909-3.16.0a0-69a6612-NOGIL/bm-20260909-vultr-x86_64-python-69a6612ff02c022d17f9-3.16.0a0-69a6612-vs-3.13.0rc2.svg) | 1.112x ↓<br>[📄](results/bm-20260909-3.16.0a0-69a6612-NOGIL/bm-20260909-vultr-x86_64-python-69a6612ff02c022d17f9-3.16.0a0-69a6612-vs-base.md)[📈](results/bm-20260909-3.16.0a0-69a6612-NOGIL/bm-20260909-vultr-x86_64-python-69a6612ff02c022d17f9-3.16.0a0-69a6612-vs-base.svg)[🧠](results/bm-20260909-3.16.0a0-69a6612-NOGIL/bm-20260909-vultr-x86_64-python-69a6612ff02c022d17f9-3.16.0a0-69a6612-vs-base-mem.svg) |
| [2026-09-09](results/bm-20260909-3.16.0a0-69a6612) | python/69a6612ff02c022d17f9 | 69a6612 | 1.070x ↑<br>[📄](results/bm-20260909-3.16.0a0-69a6612/bm-20260909-vultr-x86_64-python-69a6612ff02c022d17f9-3.16.0a0-69a6612-vs-3.12.6.md)[📈](results/bm-20260909-3.16.0a0-69a6612/bm-20260909-vultr-x86_64-python-69a6612ff02c022d17f9-3.16.0a0-69a6612-vs-3.12.6.svg) | 1.035x ↑<br>[📄](results/bm-20260909-3.16.0a0-69a6612/bm-20260909-vultr-x86_64-python-69a6612ff02c022d17f9-3.16.0a0-69a6612-vs-3.13.0rc2.md)[📈](results/bm-20260909-3.16.0a0-69a6612/bm-20260909-vultr-x86_64-python-69a6612ff02c022d17f9-3.16.0a0-69a6612-vs-3.13.0rc2.svg) |  |
| [2026-09-08](results/bm-20260908-3.16.0a0-f8f8c30-NOGIL) | python/f8f8c30ed4e20208e8ba | f8f8c30 (NOGIL) | 1.044x ↓<br>[📄](results/bm-20260908-3.16.0a0-f8f8c30-NOGIL/bm-20260908-vultr-x86_64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30-vs-3.12.6.md)[📈](results/bm-20260908-3.16.0a0-f8f8c30-NOGIL/bm-20260908-vultr-x86_64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30-vs-3.12.6.svg) | 1.076x ↓<br>[📄](results/bm-20260908-3.16.0a0-f8f8c30-NOGIL/bm-20260908-vultr-x86_64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30-vs-3.13.0rc2.md)[📈](results/bm-20260908-3.16.0a0-f8f8c30-NOGIL/bm-20260908-vultr-x86_64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30-vs-3.13.0rc2.svg) | 1.108x ↓<br>[📄](results/bm-20260908-3.16.0a0-f8f8c30-NOGIL/bm-20260908-vultr-x86_64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30-vs-base.md)[📈](results/bm-20260908-3.16.0a0-f8f8c30-NOGIL/bm-20260908-vultr-x86_64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30-vs-base.svg)[🧠](results/bm-20260908-3.16.0a0-f8f8c30-NOGIL/bm-20260908-vultr-x86_64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30-vs-base-mem.svg) |
| [2026-09-08](results/bm-20260908-3.16.0a0-f8f8c30) | python/f8f8c30ed4e20208e8ba | f8f8c30 | 1.067x ↑<br>[📄](results/bm-20260908-3.16.0a0-f8f8c30/bm-20260908-vultr-x86_64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30-vs-3.12.6.md)[📈](results/bm-20260908-3.16.0a0-f8f8c30/bm-20260908-vultr-x86_64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30-vs-3.12.6.svg) | 1.032x ↑<br>[📄](results/bm-20260908-3.16.0a0-f8f8c30/bm-20260908-vultr-x86_64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30-vs-3.13.0rc2.md)[📈](results/bm-20260908-3.16.0a0-f8f8c30/bm-20260908-vultr-x86_64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-09-11](results/bm-20260911-3.16.0a0-f5dd52d-NOGIL) | python/f5dd52df16e1b3f3f8cc | f5dd52d (NOGIL) | 1.002x ↑<br>[📄](results/bm-20260911-3.16.0a0-f5dd52d-NOGIL/bm-20260911-macm4pro-arm64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d-vs-3.12.6.md)[📈](results/bm-20260911-3.16.0a0-f5dd52d-NOGIL/bm-20260911-macm4pro-arm64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d-vs-3.12.6.svg) | 1.072x ↓<br>[📄](results/bm-20260911-3.16.0a0-f5dd52d-NOGIL/bm-20260911-macm4pro-arm64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d-vs-3.13.0rc2.md)[📈](results/bm-20260911-3.16.0a0-f5dd52d-NOGIL/bm-20260911-macm4pro-arm64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d-vs-3.13.0rc2.svg) | 1.119x ↓<br>[📄](results/bm-20260911-3.16.0a0-f5dd52d-NOGIL/bm-20260911-macm4pro-arm64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d-vs-base.md)[📈](results/bm-20260911-3.16.0a0-f5dd52d-NOGIL/bm-20260911-macm4pro-arm64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d-vs-base.svg)[🧠](results/bm-20260911-3.16.0a0-f5dd52d-NOGIL/bm-20260911-macm4pro-arm64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d-vs-base-mem.svg) |
| [2026-09-11](results/bm-20260911-3.16.0a0-f5dd52d) | python/f5dd52df16e1b3f3f8cc | f5dd52d | 1.140x ↑<br>[📄](results/bm-20260911-3.16.0a0-f5dd52d/bm-20260911-macm4pro-arm64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d-vs-3.12.6.md)[📈](results/bm-20260911-3.16.0a0-f5dd52d/bm-20260911-macm4pro-arm64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d-vs-3.12.6.svg) | 1.053x ↑<br>[📄](results/bm-20260911-3.16.0a0-f5dd52d/bm-20260911-macm4pro-arm64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d-vs-3.13.0rc2.md)[📈](results/bm-20260911-3.16.0a0-f5dd52d/bm-20260911-macm4pro-arm64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d-vs-3.13.0rc2.svg) |  |
| [2026-09-10](results/bm-20260910-3.16.0a0-8f84787-NOGIL) | python/8f847875d60c81841e18 | 8f84787 (NOGIL) | 1.010x ↑<br>[📄](results/bm-20260910-3.16.0a0-8f84787-NOGIL/bm-20260910-macm4pro-arm64-python-8f847875d60c81841e18-3.16.0a0-8f84787-vs-3.12.6.md)[📈](results/bm-20260910-3.16.0a0-8f84787-NOGIL/bm-20260910-macm4pro-arm64-python-8f847875d60c81841e18-3.16.0a0-8f84787-vs-3.12.6.svg) | 1.064x ↓<br>[📄](results/bm-20260910-3.16.0a0-8f84787-NOGIL/bm-20260910-macm4pro-arm64-python-8f847875d60c81841e18-3.16.0a0-8f84787-vs-3.13.0rc2.md)[📈](results/bm-20260910-3.16.0a0-8f84787-NOGIL/bm-20260910-macm4pro-arm64-python-8f847875d60c81841e18-3.16.0a0-8f84787-vs-3.13.0rc2.svg) | 1.120x ↓<br>[📄](results/bm-20260910-3.16.0a0-8f84787-NOGIL/bm-20260910-macm4pro-arm64-python-8f847875d60c81841e18-3.16.0a0-8f84787-vs-base.md)[📈](results/bm-20260910-3.16.0a0-8f84787-NOGIL/bm-20260910-macm4pro-arm64-python-8f847875d60c81841e18-3.16.0a0-8f84787-vs-base.svg)[🧠](results/bm-20260910-3.16.0a0-8f84787-NOGIL/bm-20260910-macm4pro-arm64-python-8f847875d60c81841e18-3.16.0a0-8f84787-vs-base-mem.svg) |
| [2026-09-10](results/bm-20260910-3.16.0a0-8f84787) | python/8f847875d60c81841e18 | 8f84787 | 1.150x ↑<br>[📄](results/bm-20260910-3.16.0a0-8f84787/bm-20260910-macm4pro-arm64-python-8f847875d60c81841e18-3.16.0a0-8f84787-vs-3.12.6.md)[📈](results/bm-20260910-3.16.0a0-8f84787/bm-20260910-macm4pro-arm64-python-8f847875d60c81841e18-3.16.0a0-8f84787-vs-3.12.6.svg) | 1.062x ↑<br>[📄](results/bm-20260910-3.16.0a0-8f84787/bm-20260910-macm4pro-arm64-python-8f847875d60c81841e18-3.16.0a0-8f84787-vs-3.13.0rc2.md)[📈](results/bm-20260910-3.16.0a0-8f84787/bm-20260910-macm4pro-arm64-python-8f847875d60c81841e18-3.16.0a0-8f84787-vs-3.13.0rc2.svg) |  |
| [2026-09-09](results/bm-20260909-3.16.0a0-69a6612-NOGIL) | python/69a6612ff02c022d17f9 | 69a6612 (NOGIL) | 1.015x ↑<br>[📄](results/bm-20260909-3.16.0a0-69a6612-NOGIL/bm-20260909-macm4pro-arm64-python-69a6612ff02c022d17f9-3.16.0a0-69a6612-vs-3.12.6.md)[📈](results/bm-20260909-3.16.0a0-69a6612-NOGIL/bm-20260909-macm4pro-arm64-python-69a6612ff02c022d17f9-3.16.0a0-69a6612-vs-3.12.6.svg) | 1.060x ↓<br>[📄](results/bm-20260909-3.16.0a0-69a6612-NOGIL/bm-20260909-macm4pro-arm64-python-69a6612ff02c022d17f9-3.16.0a0-69a6612-vs-3.13.0rc2.md)[📈](results/bm-20260909-3.16.0a0-69a6612-NOGIL/bm-20260909-macm4pro-arm64-python-69a6612ff02c022d17f9-3.16.0a0-69a6612-vs-3.13.0rc2.svg) | 1.118x ↓<br>[📄](results/bm-20260909-3.16.0a0-69a6612-NOGIL/bm-20260909-macm4pro-arm64-python-69a6612ff02c022d17f9-3.16.0a0-69a6612-vs-base.md)[📈](results/bm-20260909-3.16.0a0-69a6612-NOGIL/bm-20260909-macm4pro-arm64-python-69a6612ff02c022d17f9-3.16.0a0-69a6612-vs-base.svg)[🧠](results/bm-20260909-3.16.0a0-69a6612-NOGIL/bm-20260909-macm4pro-arm64-python-69a6612ff02c022d17f9-3.16.0a0-69a6612-vs-base-mem.svg) |
| [2026-09-09](results/bm-20260909-3.16.0a0-69a6612) | python/69a6612ff02c022d17f9 | 69a6612 | 1.153x ↑<br>[📄](results/bm-20260909-3.16.0a0-69a6612/bm-20260909-macm4pro-arm64-python-69a6612ff02c022d17f9-3.16.0a0-69a6612-vs-3.12.6.md)[📈](results/bm-20260909-3.16.0a0-69a6612/bm-20260909-macm4pro-arm64-python-69a6612ff02c022d17f9-3.16.0a0-69a6612-vs-3.12.6.svg) | 1.065x ↑<br>[📄](results/bm-20260909-3.16.0a0-69a6612/bm-20260909-macm4pro-arm64-python-69a6612ff02c022d17f9-3.16.0a0-69a6612-vs-3.13.0rc2.md)[📈](results/bm-20260909-3.16.0a0-69a6612/bm-20260909-macm4pro-arm64-python-69a6612ff02c022d17f9-3.16.0a0-69a6612-vs-3.13.0rc2.svg) |  |
| [2026-09-08](results/bm-20260908-3.16.0a0-f8f8c30-NOGIL) | python/f8f8c30ed4e20208e8ba | f8f8c30 (NOGIL) | 1.009x ↑<br>[📄](results/bm-20260908-3.16.0a0-f8f8c30-NOGIL/bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30-vs-3.12.6.md)[📈](results/bm-20260908-3.16.0a0-f8f8c30-NOGIL/bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30-vs-3.12.6.svg) | 1.066x ↓<br>[📄](results/bm-20260908-3.16.0a0-f8f8c30-NOGIL/bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30-vs-3.13.0rc2.md)[📈](results/bm-20260908-3.16.0a0-f8f8c30-NOGIL/bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30-vs-3.13.0rc2.svg) | 1.117x ↓<br>[📄](results/bm-20260908-3.16.0a0-f8f8c30-NOGIL/bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30-vs-base.md)[📈](results/bm-20260908-3.16.0a0-f8f8c30-NOGIL/bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30-vs-base.svg)[🧠](results/bm-20260908-3.16.0a0-f8f8c30-NOGIL/bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30-vs-base-mem.svg) |
| [2026-09-08](results/bm-20260908-3.16.0a0-f8f8c30) | python/f8f8c30ed4e20208e8ba | f8f8c30 | 1.145x ↑<br>[📄](results/bm-20260908-3.16.0a0-f8f8c30/bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30-vs-3.12.6.md)[📈](results/bm-20260908-3.16.0a0-f8f8c30/bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30-vs-3.12.6.svg) | 1.058x ↑<br>[📄](results/bm-20260908-3.16.0a0-f8f8c30/bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30-vs-3.13.0rc2.md)[📈](results/bm-20260908-3.16.0a0-f8f8c30/bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30-vs-3.13.0rc2.svg) |  |


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
