# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (a1ec746)](results/bm-20260228-3.15.0a6%2B-a1ec746/bm-20260228-vultr-x86_64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (a1ec746)](results/bm-20260228-3.15.0a6%2B-a1ec746-PYTHON_UOPS/bm-20260228-vultr-x86_64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-pystats.md)
- [Most recent JIT pystats on main (bedaea0)](results/bm-20251019-3.15.0a1%2B-bedaea0-JIT/bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-03-05](results/bm-20260305-3.15.0a6%2B-7232883-NOGIL) | python/7232883adfc28f94a62d | 7232883 (NOGIL) | 1.028x ↓<br>[📄](results/bm-20260305-3.15.0a6%2B-7232883-NOGIL/bm-20260305-vultr-x86_64-python-7232883adfc28f94a62d-3.15.0a6%2B-7232883-vs-3.12.6.md)[📈](results/bm-20260305-3.15.0a6%2B-7232883-NOGIL/bm-20260305-vultr-x86_64-python-7232883adfc28f94a62d-3.15.0a6%2B-7232883-vs-3.12.6.svg) | 1.062x ↓<br>[📄](results/bm-20260305-3.15.0a6%2B-7232883-NOGIL/bm-20260305-vultr-x86_64-python-7232883adfc28f94a62d-3.15.0a6%2B-7232883-vs-3.13.0rc2.md)[📈](results/bm-20260305-3.15.0a6%2B-7232883-NOGIL/bm-20260305-vultr-x86_64-python-7232883adfc28f94a62d-3.15.0a6%2B-7232883-vs-3.13.0rc2.svg) | 1.101x ↓<br>[📄](results/bm-20260305-3.15.0a6%2B-7232883-NOGIL/bm-20260305-vultr-x86_64-python-7232883adfc28f94a62d-3.15.0a6%2B-7232883-vs-base.md)[📈](results/bm-20260305-3.15.0a6%2B-7232883-NOGIL/bm-20260305-vultr-x86_64-python-7232883adfc28f94a62d-3.15.0a6%2B-7232883-vs-base.svg)[🧠](results/bm-20260305-3.15.0a6%2B-7232883-NOGIL/bm-20260305-vultr-x86_64-python-7232883adfc28f94a62d-3.15.0a6%2B-7232883-vs-base-mem.svg) |
| [2026-03-05](results/bm-20260305-3.15.0a6%2B-7232883) | python/7232883adfc28f94a62d | 7232883 | 1.075x ↑<br>[📄](results/bm-20260305-3.15.0a6%2B-7232883/bm-20260305-vultr-x86_64-python-7232883adfc28f94a62d-3.15.0a6%2B-7232883-vs-3.12.6.md)[📈](results/bm-20260305-3.15.0a6%2B-7232883/bm-20260305-vultr-x86_64-python-7232883adfc28f94a62d-3.15.0a6%2B-7232883-vs-3.12.6.svg) | 1.039x ↑<br>[📄](results/bm-20260305-3.15.0a6%2B-7232883/bm-20260305-vultr-x86_64-python-7232883adfc28f94a62d-3.15.0a6%2B-7232883-vs-3.13.0rc2.md)[📈](results/bm-20260305-3.15.0a6%2B-7232883/bm-20260305-vultr-x86_64-python-7232883adfc28f94a62d-3.15.0a6%2B-7232883-vs-3.13.0rc2.svg) |  |
| [2026-03-05](results/bm-20260305-3.15.0a6%2B-8b54313-NOGIL) | python/8b5431367042672d5c6f | 8b54313 (NOGIL) | 1.024x ↓<br>[📄](results/bm-20260305-3.15.0a6%2B-8b54313-NOGIL/bm-20260305-vultr-x86_64-python-8b5431367042672d5c6f-3.15.0a6%2B-8b54313-vs-3.12.6.md)[📈](results/bm-20260305-3.15.0a6%2B-8b54313-NOGIL/bm-20260305-vultr-x86_64-python-8b5431367042672d5c6f-3.15.0a6%2B-8b54313-vs-3.12.6.svg) | 1.056x ↓<br>[📄](results/bm-20260305-3.15.0a6%2B-8b54313-NOGIL/bm-20260305-vultr-x86_64-python-8b5431367042672d5c6f-3.15.0a6%2B-8b54313-vs-3.13.0rc2.md)[📈](results/bm-20260305-3.15.0a6%2B-8b54313-NOGIL/bm-20260305-vultr-x86_64-python-8b5431367042672d5c6f-3.15.0a6%2B-8b54313-vs-3.13.0rc2.svg) | 1.094x ↓<br>[📄](results/bm-20260305-3.15.0a6%2B-8b54313-NOGIL/bm-20260305-vultr-x86_64-python-8b5431367042672d5c6f-3.15.0a6%2B-8b54313-vs-base.md)[📈](results/bm-20260305-3.15.0a6%2B-8b54313-NOGIL/bm-20260305-vultr-x86_64-python-8b5431367042672d5c6f-3.15.0a6%2B-8b54313-vs-base.svg)[🧠](results/bm-20260305-3.15.0a6%2B-8b54313-NOGIL/bm-20260305-vultr-x86_64-python-8b5431367042672d5c6f-3.15.0a6%2B-8b54313-vs-base-mem.svg) |
| [2026-03-05](results/bm-20260305-3.15.0a6%2B-8b54313) | python/8b5431367042672d5c6f | 8b54313 | 1.072x ↑<br>[📄](results/bm-20260305-3.15.0a6%2B-8b54313/bm-20260305-vultr-x86_64-python-8b5431367042672d5c6f-3.15.0a6%2B-8b54313-vs-3.12.6.md)[📈](results/bm-20260305-3.15.0a6%2B-8b54313/bm-20260305-vultr-x86_64-python-8b5431367042672d5c6f-3.15.0a6%2B-8b54313-vs-3.12.6.svg) | 1.036x ↑<br>[📄](results/bm-20260305-3.15.0a6%2B-8b54313/bm-20260305-vultr-x86_64-python-8b5431367042672d5c6f-3.15.0a6%2B-8b54313-vs-3.13.0rc2.md)[📈](results/bm-20260305-3.15.0a6%2B-8b54313/bm-20260305-vultr-x86_64-python-8b5431367042672d5c6f-3.15.0a6%2B-8b54313-vs-3.13.0rc2.svg) |  |
| [2026-03-03](results/bm-20260303-3.15.0a6%2B-dc12d19-NOGIL) | python/dc12d1999b88e84d5a6b | dc12d19 (NOGIL) | 1.025x ↓<br>[📄](results/bm-20260303-3.15.0a6%2B-dc12d19-NOGIL/bm-20260303-vultr-x86_64-python-dc12d1999b88e84d5a6b-3.15.0a6%2B-dc12d19-vs-3.12.6.md)[📈](results/bm-20260303-3.15.0a6%2B-dc12d19-NOGIL/bm-20260303-vultr-x86_64-python-dc12d1999b88e84d5a6b-3.15.0a6%2B-dc12d19-vs-3.12.6.svg) | 1.058x ↓<br>[📄](results/bm-20260303-3.15.0a6%2B-dc12d19-NOGIL/bm-20260303-vultr-x86_64-python-dc12d1999b88e84d5a6b-3.15.0a6%2B-dc12d19-vs-3.13.0rc2.md)[📈](results/bm-20260303-3.15.0a6%2B-dc12d19-NOGIL/bm-20260303-vultr-x86_64-python-dc12d1999b88e84d5a6b-3.15.0a6%2B-dc12d19-vs-3.13.0rc2.svg) | 1.097x ↓<br>[📄](results/bm-20260303-3.15.0a6%2B-dc12d19-NOGIL/bm-20260303-vultr-x86_64-python-dc12d1999b88e84d5a6b-3.15.0a6%2B-dc12d19-vs-base.md)[📈](results/bm-20260303-3.15.0a6%2B-dc12d19-NOGIL/bm-20260303-vultr-x86_64-python-dc12d1999b88e84d5a6b-3.15.0a6%2B-dc12d19-vs-base.svg)[🧠](results/bm-20260303-3.15.0a6%2B-dc12d19-NOGIL/bm-20260303-vultr-x86_64-python-dc12d1999b88e84d5a6b-3.15.0a6%2B-dc12d19-vs-base-mem.svg) |
| [2026-03-03](results/bm-20260303-3.15.0a6%2B-dc12d19) | python/dc12d1999b88e84d5a6b | dc12d19 | 1.074x ↑<br>[📄](results/bm-20260303-3.15.0a6%2B-dc12d19/bm-20260303-vultr-x86_64-python-dc12d1999b88e84d5a6b-3.15.0a6%2B-dc12d19-vs-3.12.6.md)[📈](results/bm-20260303-3.15.0a6%2B-dc12d19/bm-20260303-vultr-x86_64-python-dc12d1999b88e84d5a6b-3.15.0a6%2B-dc12d19-vs-3.12.6.svg) | 1.038x ↑<br>[📄](results/bm-20260303-3.15.0a6%2B-dc12d19/bm-20260303-vultr-x86_64-python-dc12d1999b88e84d5a6b-3.15.0a6%2B-dc12d19-vs-3.13.0rc2.md)[📈](results/bm-20260303-3.15.0a6%2B-dc12d19/bm-20260303-vultr-x86_64-python-dc12d1999b88e84d5a6b-3.15.0a6%2B-dc12d19-vs-3.13.0rc2.svg) |  |
| [2026-03-02](results/bm-20260302-3.15.0a6%2B-ea90b03-NOGIL) | python/ea90b032a016122e7871 | ea90b03 (NOGIL) | 1.025x ↓<br>[📄](results/bm-20260302-3.15.0a6%2B-ea90b03-NOGIL/bm-20260302-vultr-x86_64-python-ea90b032a016122e7871-3.15.0a6%2B-ea90b03-vs-3.12.6.md)[📈](results/bm-20260302-3.15.0a6%2B-ea90b03-NOGIL/bm-20260302-vultr-x86_64-python-ea90b032a016122e7871-3.15.0a6%2B-ea90b03-vs-3.12.6.svg) | 1.058x ↓<br>[📄](results/bm-20260302-3.15.0a6%2B-ea90b03-NOGIL/bm-20260302-vultr-x86_64-python-ea90b032a016122e7871-3.15.0a6%2B-ea90b03-vs-3.13.0rc2.md)[📈](results/bm-20260302-3.15.0a6%2B-ea90b03-NOGIL/bm-20260302-vultr-x86_64-python-ea90b032a016122e7871-3.15.0a6%2B-ea90b03-vs-3.13.0rc2.svg) | 1.094x ↓<br>[📄](results/bm-20260302-3.15.0a6%2B-ea90b03-NOGIL/bm-20260302-vultr-x86_64-python-ea90b032a016122e7871-3.15.0a6%2B-ea90b03-vs-base.md)[📈](results/bm-20260302-3.15.0a6%2B-ea90b03-NOGIL/bm-20260302-vultr-x86_64-python-ea90b032a016122e7871-3.15.0a6%2B-ea90b03-vs-base.svg)[🧠](results/bm-20260302-3.15.0a6%2B-ea90b03-NOGIL/bm-20260302-vultr-x86_64-python-ea90b032a016122e7871-3.15.0a6%2B-ea90b03-vs-base-mem.svg) |
| [2026-03-02](results/bm-20260302-3.15.0a6%2B-ea90b03) | python/ea90b032a016122e7871 | ea90b03 | 1.070x ↑<br>[📄](results/bm-20260302-3.15.0a6%2B-ea90b03/bm-20260302-vultr-x86_64-python-ea90b032a016122e7871-3.15.0a6%2B-ea90b03-vs-3.12.6.md)[📈](results/bm-20260302-3.15.0a6%2B-ea90b03/bm-20260302-vultr-x86_64-python-ea90b032a016122e7871-3.15.0a6%2B-ea90b03-vs-3.12.6.svg) | 1.035x ↑<br>[📄](results/bm-20260302-3.15.0a6%2B-ea90b03/bm-20260302-vultr-x86_64-python-ea90b032a016122e7871-3.15.0a6%2B-ea90b03-vs-3.13.0rc2.md)[📈](results/bm-20260302-3.15.0a6%2B-ea90b03/bm-20260302-vultr-x86_64-python-ea90b032a016122e7871-3.15.0a6%2B-ea90b03-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-03-05](results/bm-20260305-3.15.0a6%2B-7232883-NOGIL) | python/7232883adfc28f94a62d | 7232883 (NOGIL) | 1.100x ↑<br>[📄](results/bm-20260305-3.15.0a6%2B-7232883-NOGIL/bm-20260305-macm4pro-arm64-python-7232883adfc28f94a62d-3.15.0a6%2B-7232883-vs-3.12.6.md)[📈](results/bm-20260305-3.15.0a6%2B-7232883-NOGIL/bm-20260305-macm4pro-arm64-python-7232883adfc28f94a62d-3.15.0a6%2B-7232883-vs-3.12.6.svg) | 1.019x ↑<br>[📄](results/bm-20260305-3.15.0a6%2B-7232883-NOGIL/bm-20260305-macm4pro-arm64-python-7232883adfc28f94a62d-3.15.0a6%2B-7232883-vs-3.13.0rc2.md)[📈](results/bm-20260305-3.15.0a6%2B-7232883-NOGIL/bm-20260305-macm4pro-arm64-python-7232883adfc28f94a62d-3.15.0a6%2B-7232883-vs-3.13.0rc2.svg) | 1.032x ↓<br>[📄](results/bm-20260305-3.15.0a6%2B-7232883-NOGIL/bm-20260305-macm4pro-arm64-python-7232883adfc28f94a62d-3.15.0a6%2B-7232883-vs-base.md)[📈](results/bm-20260305-3.15.0a6%2B-7232883-NOGIL/bm-20260305-macm4pro-arm64-python-7232883adfc28f94a62d-3.15.0a6%2B-7232883-vs-base.svg)[🧠](results/bm-20260305-3.15.0a6%2B-7232883-NOGIL/bm-20260305-macm4pro-arm64-python-7232883adfc28f94a62d-3.15.0a6%2B-7232883-vs-base-mem.svg) |
| [2026-03-05](results/bm-20260305-3.15.0a6%2B-7232883) | python/7232883adfc28f94a62d | 7232883 | 1.135x ↑<br>[📄](results/bm-20260305-3.15.0a6%2B-7232883/bm-20260305-macm4pro-arm64-python-7232883adfc28f94a62d-3.15.0a6%2B-7232883-vs-3.12.6.md)[📈](results/bm-20260305-3.15.0a6%2B-7232883/bm-20260305-macm4pro-arm64-python-7232883adfc28f94a62d-3.15.0a6%2B-7232883-vs-3.12.6.svg) | 1.053x ↑<br>[📄](results/bm-20260305-3.15.0a6%2B-7232883/bm-20260305-macm4pro-arm64-python-7232883adfc28f94a62d-3.15.0a6%2B-7232883-vs-3.13.0rc2.md)[📈](results/bm-20260305-3.15.0a6%2B-7232883/bm-20260305-macm4pro-arm64-python-7232883adfc28f94a62d-3.15.0a6%2B-7232883-vs-3.13.0rc2.svg) |  |
| [2026-03-05](results/bm-20260305-3.15.0a6%2B-8b54313-NOGIL) | python/8b5431367042672d5c6f | 8b54313 (NOGIL) | 1.102x ↑<br>[📄](results/bm-20260305-3.15.0a6%2B-8b54313-NOGIL/bm-20260305-macm4pro-arm64-python-8b5431367042672d5c6f-3.15.0a6%2B-8b54313-vs-3.12.6.md)[📈](results/bm-20260305-3.15.0a6%2B-8b54313-NOGIL/bm-20260305-macm4pro-arm64-python-8b5431367042672d5c6f-3.15.0a6%2B-8b54313-vs-3.12.6.svg) | 1.023x ↑<br>[📄](results/bm-20260305-3.15.0a6%2B-8b54313-NOGIL/bm-20260305-macm4pro-arm64-python-8b5431367042672d5c6f-3.15.0a6%2B-8b54313-vs-3.13.0rc2.md)[📈](results/bm-20260305-3.15.0a6%2B-8b54313-NOGIL/bm-20260305-macm4pro-arm64-python-8b5431367042672d5c6f-3.15.0a6%2B-8b54313-vs-3.13.0rc2.svg) | 1.032x ↓<br>[📄](results/bm-20260305-3.15.0a6%2B-8b54313-NOGIL/bm-20260305-macm4pro-arm64-python-8b5431367042672d5c6f-3.15.0a6%2B-8b54313-vs-base.md)[📈](results/bm-20260305-3.15.0a6%2B-8b54313-NOGIL/bm-20260305-macm4pro-arm64-python-8b5431367042672d5c6f-3.15.0a6%2B-8b54313-vs-base.svg)[🧠](results/bm-20260305-3.15.0a6%2B-8b54313-NOGIL/bm-20260305-macm4pro-arm64-python-8b5431367042672d5c6f-3.15.0a6%2B-8b54313-vs-base-mem.svg) |
| [2026-03-05](results/bm-20260305-3.15.0a6%2B-8b54313) | python/8b5431367042672d5c6f | 8b54313 | 1.139x ↑<br>[📄](results/bm-20260305-3.15.0a6%2B-8b54313/bm-20260305-macm4pro-arm64-python-8b5431367042672d5c6f-3.15.0a6%2B-8b54313-vs-3.12.6.md)[📈](results/bm-20260305-3.15.0a6%2B-8b54313/bm-20260305-macm4pro-arm64-python-8b5431367042672d5c6f-3.15.0a6%2B-8b54313-vs-3.12.6.svg) | 1.056x ↑<br>[📄](results/bm-20260305-3.15.0a6%2B-8b54313/bm-20260305-macm4pro-arm64-python-8b5431367042672d5c6f-3.15.0a6%2B-8b54313-vs-3.13.0rc2.md)[📈](results/bm-20260305-3.15.0a6%2B-8b54313/bm-20260305-macm4pro-arm64-python-8b5431367042672d5c6f-3.15.0a6%2B-8b54313-vs-3.13.0rc2.svg) |  |
| [2026-03-03](results/bm-20260303-3.15.0a6%2B-dc12d19-NOGIL) | python/dc12d1999b88e84d5a6b | dc12d19 (NOGIL) | 1.097x ↑<br>[📄](results/bm-20260303-3.15.0a6%2B-dc12d19-NOGIL/bm-20260303-macm4pro-arm64-python-dc12d1999b88e84d5a6b-3.15.0a6%2B-dc12d19-vs-3.12.6.md)[📈](results/bm-20260303-3.15.0a6%2B-dc12d19-NOGIL/bm-20260303-macm4pro-arm64-python-dc12d1999b88e84d5a6b-3.15.0a6%2B-dc12d19-vs-3.12.6.svg) | 1.018x ↑<br>[📄](results/bm-20260303-3.15.0a6%2B-dc12d19-NOGIL/bm-20260303-macm4pro-arm64-python-dc12d1999b88e84d5a6b-3.15.0a6%2B-dc12d19-vs-3.13.0rc2.md)[📈](results/bm-20260303-3.15.0a6%2B-dc12d19-NOGIL/bm-20260303-macm4pro-arm64-python-dc12d1999b88e84d5a6b-3.15.0a6%2B-dc12d19-vs-3.13.0rc2.svg) | 1.040x ↓<br>[📄](results/bm-20260303-3.15.0a6%2B-dc12d19-NOGIL/bm-20260303-macm4pro-arm64-python-dc12d1999b88e84d5a6b-3.15.0a6%2B-dc12d19-vs-base.md)[📈](results/bm-20260303-3.15.0a6%2B-dc12d19-NOGIL/bm-20260303-macm4pro-arm64-python-dc12d1999b88e84d5a6b-3.15.0a6%2B-dc12d19-vs-base.svg)[🧠](results/bm-20260303-3.15.0a6%2B-dc12d19-NOGIL/bm-20260303-macm4pro-arm64-python-dc12d1999b88e84d5a6b-3.15.0a6%2B-dc12d19-vs-base-mem.svg) |
| [2026-03-03](results/bm-20260303-3.15.0a6%2B-dc12d19) | python/dc12d1999b88e84d5a6b | dc12d19 | 1.144x ↑<br>[📄](results/bm-20260303-3.15.0a6%2B-dc12d19/bm-20260303-macm4pro-arm64-python-dc12d1999b88e84d5a6b-3.15.0a6%2B-dc12d19-vs-3.12.6.md)[📈](results/bm-20260303-3.15.0a6%2B-dc12d19/bm-20260303-macm4pro-arm64-python-dc12d1999b88e84d5a6b-3.15.0a6%2B-dc12d19-vs-3.12.6.svg) | 1.060x ↑<br>[📄](results/bm-20260303-3.15.0a6%2B-dc12d19/bm-20260303-macm4pro-arm64-python-dc12d1999b88e84d5a6b-3.15.0a6%2B-dc12d19-vs-3.13.0rc2.md)[📈](results/bm-20260303-3.15.0a6%2B-dc12d19/bm-20260303-macm4pro-arm64-python-dc12d1999b88e84d5a6b-3.15.0a6%2B-dc12d19-vs-3.13.0rc2.svg) |  |
| [2026-03-02](results/bm-20260302-3.15.0a6%2B-ea90b03-NOGIL) | python/ea90b032a016122e7871 | ea90b03 (NOGIL) | 1.090x ↑<br>[📄](results/bm-20260302-3.15.0a6%2B-ea90b03-NOGIL/bm-20260302-macm4pro-arm64-python-ea90b032a016122e7871-3.15.0a6%2B-ea90b03-vs-3.12.6.md)[📈](results/bm-20260302-3.15.0a6%2B-ea90b03-NOGIL/bm-20260302-macm4pro-arm64-python-ea90b032a016122e7871-3.15.0a6%2B-ea90b03-vs-3.12.6.svg) | 1.011x ↑<br>[📄](results/bm-20260302-3.15.0a6%2B-ea90b03-NOGIL/bm-20260302-macm4pro-arm64-python-ea90b032a016122e7871-3.15.0a6%2B-ea90b03-vs-3.13.0rc2.md)[📈](results/bm-20260302-3.15.0a6%2B-ea90b03-NOGIL/bm-20260302-macm4pro-arm64-python-ea90b032a016122e7871-3.15.0a6%2B-ea90b03-vs-3.13.0rc2.svg) | 1.041x ↓<br>[📄](results/bm-20260302-3.15.0a6%2B-ea90b03-NOGIL/bm-20260302-macm4pro-arm64-python-ea90b032a016122e7871-3.15.0a6%2B-ea90b03-vs-base.md)[📈](results/bm-20260302-3.15.0a6%2B-ea90b03-NOGIL/bm-20260302-macm4pro-arm64-python-ea90b032a016122e7871-3.15.0a6%2B-ea90b03-vs-base.svg)[🧠](results/bm-20260302-3.15.0a6%2B-ea90b03-NOGIL/bm-20260302-macm4pro-arm64-python-ea90b032a016122e7871-3.15.0a6%2B-ea90b03-vs-base-mem.svg) |
| [2026-03-02](results/bm-20260302-3.15.0a6%2B-ea90b03) | python/ea90b032a016122e7871 | ea90b03 | 1.135x ↑<br>[📄](results/bm-20260302-3.15.0a6%2B-ea90b03/bm-20260302-macm4pro-arm64-python-ea90b032a016122e7871-3.15.0a6%2B-ea90b03-vs-3.12.6.md)[📈](results/bm-20260302-3.15.0a6%2B-ea90b03/bm-20260302-macm4pro-arm64-python-ea90b032a016122e7871-3.15.0a6%2B-ea90b03-vs-3.12.6.svg) | 1.053x ↑<br>[📄](results/bm-20260302-3.15.0a6%2B-ea90b03/bm-20260302-macm4pro-arm64-python-ea90b032a016122e7871-3.15.0a6%2B-ea90b03-vs-3.13.0rc2.md)[📈](results/bm-20260302-3.15.0a6%2B-ea90b03/bm-20260302-macm4pro-arm64-python-ea90b032a016122e7871-3.15.0a6%2B-ea90b03-vs-3.13.0rc2.svg) |  |


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
