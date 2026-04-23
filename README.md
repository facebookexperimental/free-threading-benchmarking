# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (4b33308)](results/bm-20260418-3.15.0a8%2B-4b33308/bm-20260418-vultr-x86_64-python-4b3330813760a3e3c75c-3.15.0a8%2B-4b33308-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (4b33308)](results/bm-20260418-3.15.0a8%2B-4b33308-PYTHON_UOPS/bm-20260418-vultr-x86_64-python-4b3330813760a3e3c75c-3.15.0a8%2B-4b33308-pystats.md)
- [Most recent JIT pystats on main (bedaea0)](results/bm-20251019-3.15.0a1%2B-bedaea0-JIT/bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-04-22](results/bm-20260422-3.15.0a8%2B-79321fd-NOGIL) | python/79321fdce3227cf09bb8 | 79321fd (NOGIL) | 1.013x ↓<br>[📄](results/bm-20260422-3.15.0a8%2B-79321fd-NOGIL/bm-20260422-vultr-x86_64-python-79321fdce3227cf09bb8-3.15.0a8%2B-79321fd-vs-3.12.6.md)[📈](results/bm-20260422-3.15.0a8%2B-79321fd-NOGIL/bm-20260422-vultr-x86_64-python-79321fdce3227cf09bb8-3.15.0a8%2B-79321fd-vs-3.12.6.svg) | 1.046x ↓<br>[📄](results/bm-20260422-3.15.0a8%2B-79321fd-NOGIL/bm-20260422-vultr-x86_64-python-79321fdce3227cf09bb8-3.15.0a8%2B-79321fd-vs-3.13.0rc2.md)[📈](results/bm-20260422-3.15.0a8%2B-79321fd-NOGIL/bm-20260422-vultr-x86_64-python-79321fdce3227cf09bb8-3.15.0a8%2B-79321fd-vs-3.13.0rc2.svg) | 1.090x ↓<br>[📄](results/bm-20260422-3.15.0a8%2B-79321fd-NOGIL/bm-20260422-vultr-x86_64-python-79321fdce3227cf09bb8-3.15.0a8%2B-79321fd-vs-base.md)[📈](results/bm-20260422-3.15.0a8%2B-79321fd-NOGIL/bm-20260422-vultr-x86_64-python-79321fdce3227cf09bb8-3.15.0a8%2B-79321fd-vs-base.svg)[🧠](results/bm-20260422-3.15.0a8%2B-79321fd-NOGIL/bm-20260422-vultr-x86_64-python-79321fdce3227cf09bb8-3.15.0a8%2B-79321fd-vs-base-mem.svg) |
| [2026-04-22](results/bm-20260422-3.15.0a8%2B-79321fd) | python/79321fdce3227cf09bb8 | 79321fd | 1.080x ↑<br>[📄](results/bm-20260422-3.15.0a8%2B-79321fd/bm-20260422-vultr-x86_64-python-79321fdce3227cf09bb8-3.15.0a8%2B-79321fd-vs-3.12.6.md)[📈](results/bm-20260422-3.15.0a8%2B-79321fd/bm-20260422-vultr-x86_64-python-79321fdce3227cf09bb8-3.15.0a8%2B-79321fd-vs-3.12.6.svg) | 1.044x ↑<br>[📄](results/bm-20260422-3.15.0a8%2B-79321fd/bm-20260422-vultr-x86_64-python-79321fdce3227cf09bb8-3.15.0a8%2B-79321fd-vs-3.13.0rc2.md)[📈](results/bm-20260422-3.15.0a8%2B-79321fd/bm-20260422-vultr-x86_64-python-79321fdce3227cf09bb8-3.15.0a8%2B-79321fd-vs-3.13.0rc2.svg) |  |
| [2026-04-21](results/bm-20260421-3.15.0a8%2B-09233bd-NOGIL) | python/09233bd19879284395af | 09233bd (NOGIL) | 1.016x ↓<br>[📄](results/bm-20260421-3.15.0a8%2B-09233bd-NOGIL/bm-20260421-vultr-x86_64-python-09233bd19879284395af-3.15.0a8%2B-09233bd-vs-3.12.6.md)[📈](results/bm-20260421-3.15.0a8%2B-09233bd-NOGIL/bm-20260421-vultr-x86_64-python-09233bd19879284395af-3.15.0a8%2B-09233bd-vs-3.12.6.svg) | 1.049x ↓<br>[📄](results/bm-20260421-3.15.0a8%2B-09233bd-NOGIL/bm-20260421-vultr-x86_64-python-09233bd19879284395af-3.15.0a8%2B-09233bd-vs-3.13.0rc2.md)[📈](results/bm-20260421-3.15.0a8%2B-09233bd-NOGIL/bm-20260421-vultr-x86_64-python-09233bd19879284395af-3.15.0a8%2B-09233bd-vs-3.13.0rc2.svg) | 1.094x ↓<br>[📄](results/bm-20260421-3.15.0a8%2B-09233bd-NOGIL/bm-20260421-vultr-x86_64-python-09233bd19879284395af-3.15.0a8%2B-09233bd-vs-base.md)[📈](results/bm-20260421-3.15.0a8%2B-09233bd-NOGIL/bm-20260421-vultr-x86_64-python-09233bd19879284395af-3.15.0a8%2B-09233bd-vs-base.svg)[🧠](results/bm-20260421-3.15.0a8%2B-09233bd-NOGIL/bm-20260421-vultr-x86_64-python-09233bd19879284395af-3.15.0a8%2B-09233bd-vs-base-mem.svg) |
| [2026-04-21](results/bm-20260421-3.15.0a8%2B-09233bd) | python/09233bd19879284395af | 09233bd | 1.081x ↑<br>[📄](results/bm-20260421-3.15.0a8%2B-09233bd/bm-20260421-vultr-x86_64-python-09233bd19879284395af-3.15.0a8%2B-09233bd-vs-3.12.6.md)[📈](results/bm-20260421-3.15.0a8%2B-09233bd/bm-20260421-vultr-x86_64-python-09233bd19879284395af-3.15.0a8%2B-09233bd-vs-3.12.6.svg) | 1.045x ↑<br>[📄](results/bm-20260421-3.15.0a8%2B-09233bd/bm-20260421-vultr-x86_64-python-09233bd19879284395af-3.15.0a8%2B-09233bd-vs-3.13.0rc2.md)[📈](results/bm-20260421-3.15.0a8%2B-09233bd/bm-20260421-vultr-x86_64-python-09233bd19879284395af-3.15.0a8%2B-09233bd-vs-3.13.0rc2.svg) |  |
| [2026-04-21](results/bm-20260421-3.15.0a8%2B-d206d42-NOGIL) | python/d206d42834b2a34aee11 | d206d42 (NOGIL) | 1.016x ↓<br>[📄](results/bm-20260421-3.15.0a8%2B-d206d42-NOGIL/bm-20260421-vultr-x86_64-python-d206d42834b2a34aee11-3.15.0a8%2B-d206d42-vs-3.12.6.md)[📈](results/bm-20260421-3.15.0a8%2B-d206d42-NOGIL/bm-20260421-vultr-x86_64-python-d206d42834b2a34aee11-3.15.0a8%2B-d206d42-vs-3.12.6.svg) | 1.048x ↓<br>[📄](results/bm-20260421-3.15.0a8%2B-d206d42-NOGIL/bm-20260421-vultr-x86_64-python-d206d42834b2a34aee11-3.15.0a8%2B-d206d42-vs-3.13.0rc2.md)[📈](results/bm-20260421-3.15.0a8%2B-d206d42-NOGIL/bm-20260421-vultr-x86_64-python-d206d42834b2a34aee11-3.15.0a8%2B-d206d42-vs-3.13.0rc2.svg) | 1.094x ↓<br>[📄](results/bm-20260421-3.15.0a8%2B-d206d42-NOGIL/bm-20260421-vultr-x86_64-python-d206d42834b2a34aee11-3.15.0a8%2B-d206d42-vs-base.md)[📈](results/bm-20260421-3.15.0a8%2B-d206d42-NOGIL/bm-20260421-vultr-x86_64-python-d206d42834b2a34aee11-3.15.0a8%2B-d206d42-vs-base.svg)[🧠](results/bm-20260421-3.15.0a8%2B-d206d42-NOGIL/bm-20260421-vultr-x86_64-python-d206d42834b2a34aee11-3.15.0a8%2B-d206d42-vs-base-mem.svg) |
| [2026-04-21](results/bm-20260421-3.15.0a8%2B-d206d42) | python/d206d42834b2a34aee11 | d206d42 | 1.082x ↑<br>[📄](results/bm-20260421-3.15.0a8%2B-d206d42/bm-20260421-vultr-x86_64-python-d206d42834b2a34aee11-3.15.0a8%2B-d206d42-vs-3.12.6.md)[📈](results/bm-20260421-3.15.0a8%2B-d206d42/bm-20260421-vultr-x86_64-python-d206d42834b2a34aee11-3.15.0a8%2B-d206d42-vs-3.12.6.svg) | 1.046x ↑<br>[📄](results/bm-20260421-3.15.0a8%2B-d206d42/bm-20260421-vultr-x86_64-python-d206d42834b2a34aee11-3.15.0a8%2B-d206d42-vs-3.13.0rc2.md)[📈](results/bm-20260421-3.15.0a8%2B-d206d42/bm-20260421-vultr-x86_64-python-d206d42834b2a34aee11-3.15.0a8%2B-d206d42-vs-3.13.0rc2.svg) |  |
| [2026-04-19](results/bm-20260419-3.15.0a8%2B-e50acef-NOGIL) | python/e50acef0b2c2057874a9 | e50acef (NOGIL) | 1.007x ↓<br>[📄](results/bm-20260419-3.15.0a8%2B-e50acef-NOGIL/bm-20260419-vultr-x86_64-python-e50acef0b2c2057874a9-3.15.0a8%2B-e50acef-vs-3.12.6.md)[📈](results/bm-20260419-3.15.0a8%2B-e50acef-NOGIL/bm-20260419-vultr-x86_64-python-e50acef0b2c2057874a9-3.15.0a8%2B-e50acef-vs-3.12.6.svg) | 1.040x ↓<br>[📄](results/bm-20260419-3.15.0a8%2B-e50acef-NOGIL/bm-20260419-vultr-x86_64-python-e50acef0b2c2057874a9-3.15.0a8%2B-e50acef-vs-3.13.0rc2.md)[📈](results/bm-20260419-3.15.0a8%2B-e50acef-NOGIL/bm-20260419-vultr-x86_64-python-e50acef0b2c2057874a9-3.15.0a8%2B-e50acef-vs-3.13.0rc2.svg) | 1.085x ↓<br>[📄](results/bm-20260419-3.15.0a8%2B-e50acef-NOGIL/bm-20260419-vultr-x86_64-python-e50acef0b2c2057874a9-3.15.0a8%2B-e50acef-vs-base.md)[📈](results/bm-20260419-3.15.0a8%2B-e50acef-NOGIL/bm-20260419-vultr-x86_64-python-e50acef0b2c2057874a9-3.15.0a8%2B-e50acef-vs-base.svg)[🧠](results/bm-20260419-3.15.0a8%2B-e50acef-NOGIL/bm-20260419-vultr-x86_64-python-e50acef0b2c2057874a9-3.15.0a8%2B-e50acef-vs-base-mem.svg) |
| [2026-04-19](results/bm-20260419-3.15.0a8%2B-e50acef) | python/e50acef0b2c2057874a9 | e50acef | 1.080x ↑<br>[📄](results/bm-20260419-3.15.0a8%2B-e50acef/bm-20260419-vultr-x86_64-python-e50acef0b2c2057874a9-3.15.0a8%2B-e50acef-vs-3.12.6.md)[📈](results/bm-20260419-3.15.0a8%2B-e50acef/bm-20260419-vultr-x86_64-python-e50acef0b2c2057874a9-3.15.0a8%2B-e50acef-vs-3.12.6.svg) | 1.043x ↑<br>[📄](results/bm-20260419-3.15.0a8%2B-e50acef/bm-20260419-vultr-x86_64-python-e50acef0b2c2057874a9-3.15.0a8%2B-e50acef-vs-3.13.0rc2.md)[📈](results/bm-20260419-3.15.0a8%2B-e50acef/bm-20260419-vultr-x86_64-python-e50acef0b2c2057874a9-3.15.0a8%2B-e50acef-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-04-22](results/bm-20260422-3.15.0a8%2B-79321fd-NOGIL) | python/79321fdce3227cf09bb8 | 79321fd (NOGIL) | 1.112x ↑<br>[📄](results/bm-20260422-3.15.0a8%2B-79321fd-NOGIL/bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8%2B-79321fd-vs-3.12.6.md)[📈](results/bm-20260422-3.15.0a8%2B-79321fd-NOGIL/bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8%2B-79321fd-vs-3.12.6.svg) | 1.032x ↑<br>[📄](results/bm-20260422-3.15.0a8%2B-79321fd-NOGIL/bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8%2B-79321fd-vs-3.13.0rc2.md)[📈](results/bm-20260422-3.15.0a8%2B-79321fd-NOGIL/bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8%2B-79321fd-vs-3.13.0rc2.svg) | 1.055x ↓<br>[📄](results/bm-20260422-3.15.0a8%2B-79321fd-NOGIL/bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8%2B-79321fd-vs-base.md)[📈](results/bm-20260422-3.15.0a8%2B-79321fd-NOGIL/bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8%2B-79321fd-vs-base.svg)[🧠](results/bm-20260422-3.15.0a8%2B-79321fd-NOGIL/bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8%2B-79321fd-vs-base-mem.svg) |
| [2026-04-22](results/bm-20260422-3.15.0a8%2B-79321fd) | python/79321fdce3227cf09bb8 | 79321fd | 1.177x ↑<br>[📄](results/bm-20260422-3.15.0a8%2B-79321fd/bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8%2B-79321fd-vs-3.12.6.md)[📈](results/bm-20260422-3.15.0a8%2B-79321fd/bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8%2B-79321fd-vs-3.12.6.svg) | 1.092x ↑<br>[📄](results/bm-20260422-3.15.0a8%2B-79321fd/bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8%2B-79321fd-vs-3.13.0rc2.md)[📈](results/bm-20260422-3.15.0a8%2B-79321fd/bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8%2B-79321fd-vs-3.13.0rc2.svg) |  |
| [2026-04-21](results/bm-20260421-3.15.0a8%2B-09233bd-NOGIL) | python/09233bd19879284395af | 09233bd (NOGIL) | 1.110x ↑<br>[📄](results/bm-20260421-3.15.0a8%2B-09233bd-NOGIL/bm-20260421-macm4pro-arm64-python-09233bd19879284395af-3.15.0a8%2B-09233bd-vs-3.12.6.md)[📈](results/bm-20260421-3.15.0a8%2B-09233bd-NOGIL/bm-20260421-macm4pro-arm64-python-09233bd19879284395af-3.15.0a8%2B-09233bd-vs-3.12.6.svg) | 1.030x ↑<br>[📄](results/bm-20260421-3.15.0a8%2B-09233bd-NOGIL/bm-20260421-macm4pro-arm64-python-09233bd19879284395af-3.15.0a8%2B-09233bd-vs-3.13.0rc2.md)[📈](results/bm-20260421-3.15.0a8%2B-09233bd-NOGIL/bm-20260421-macm4pro-arm64-python-09233bd19879284395af-3.15.0a8%2B-09233bd-vs-3.13.0rc2.svg) | 1.053x ↓<br>[📄](results/bm-20260421-3.15.0a8%2B-09233bd-NOGIL/bm-20260421-macm4pro-arm64-python-09233bd19879284395af-3.15.0a8%2B-09233bd-vs-base.md)[📈](results/bm-20260421-3.15.0a8%2B-09233bd-NOGIL/bm-20260421-macm4pro-arm64-python-09233bd19879284395af-3.15.0a8%2B-09233bd-vs-base.svg)[🧠](results/bm-20260421-3.15.0a8%2B-09233bd-NOGIL/bm-20260421-macm4pro-arm64-python-09233bd19879284395af-3.15.0a8%2B-09233bd-vs-base-mem.svg) |
| [2026-04-21](results/bm-20260421-3.15.0a8%2B-09233bd) | python/09233bd19879284395af | 09233bd | 1.171x ↑<br>[📄](results/bm-20260421-3.15.0a8%2B-09233bd/bm-20260421-macm4pro-arm64-python-09233bd19879284395af-3.15.0a8%2B-09233bd-vs-3.12.6.md)[📈](results/bm-20260421-3.15.0a8%2B-09233bd/bm-20260421-macm4pro-arm64-python-09233bd19879284395af-3.15.0a8%2B-09233bd-vs-3.12.6.svg) | 1.087x ↑<br>[📄](results/bm-20260421-3.15.0a8%2B-09233bd/bm-20260421-macm4pro-arm64-python-09233bd19879284395af-3.15.0a8%2B-09233bd-vs-3.13.0rc2.md)[📈](results/bm-20260421-3.15.0a8%2B-09233bd/bm-20260421-macm4pro-arm64-python-09233bd19879284395af-3.15.0a8%2B-09233bd-vs-3.13.0rc2.svg) |  |
| [2026-04-21](results/bm-20260421-3.15.0a8%2B-d206d42-NOGIL) | python/d206d42834b2a34aee11 | d206d42 (NOGIL) | 1.101x ↑<br>[📄](results/bm-20260421-3.15.0a8%2B-d206d42-NOGIL/bm-20260421-macm4pro-arm64-python-d206d42834b2a34aee11-3.15.0a8%2B-d206d42-vs-3.12.6.md)[📈](results/bm-20260421-3.15.0a8%2B-d206d42-NOGIL/bm-20260421-macm4pro-arm64-python-d206d42834b2a34aee11-3.15.0a8%2B-d206d42-vs-3.12.6.svg) | 1.022x ↑<br>[📄](results/bm-20260421-3.15.0a8%2B-d206d42-NOGIL/bm-20260421-macm4pro-arm64-python-d206d42834b2a34aee11-3.15.0a8%2B-d206d42-vs-3.13.0rc2.md)[📈](results/bm-20260421-3.15.0a8%2B-d206d42-NOGIL/bm-20260421-macm4pro-arm64-python-d206d42834b2a34aee11-3.15.0a8%2B-d206d42-vs-3.13.0rc2.svg) | 1.030x ↓<br>[📄](results/bm-20260421-3.15.0a8%2B-d206d42-NOGIL/bm-20260421-macm4pro-arm64-python-d206d42834b2a34aee11-3.15.0a8%2B-d206d42-vs-base.md)[📈](results/bm-20260421-3.15.0a8%2B-d206d42-NOGIL/bm-20260421-macm4pro-arm64-python-d206d42834b2a34aee11-3.15.0a8%2B-d206d42-vs-base.svg)[🧠](results/bm-20260421-3.15.0a8%2B-d206d42-NOGIL/bm-20260421-macm4pro-arm64-python-d206d42834b2a34aee11-3.15.0a8%2B-d206d42-vs-base-mem.svg) |
| [2026-04-21](results/bm-20260421-3.15.0a8%2B-d206d42) | python/d206d42834b2a34aee11 | d206d42 | 1.135x ↑<br>[📄](results/bm-20260421-3.15.0a8%2B-d206d42/bm-20260421-macm4pro-arm64-python-d206d42834b2a34aee11-3.15.0a8%2B-d206d42-vs-3.12.6.md)[📈](results/bm-20260421-3.15.0a8%2B-d206d42/bm-20260421-macm4pro-arm64-python-d206d42834b2a34aee11-3.15.0a8%2B-d206d42-vs-3.12.6.svg) | 1.053x ↑<br>[📄](results/bm-20260421-3.15.0a8%2B-d206d42/bm-20260421-macm4pro-arm64-python-d206d42834b2a34aee11-3.15.0a8%2B-d206d42-vs-3.13.0rc2.md)[📈](results/bm-20260421-3.15.0a8%2B-d206d42/bm-20260421-macm4pro-arm64-python-d206d42834b2a34aee11-3.15.0a8%2B-d206d42-vs-3.13.0rc2.svg) |  |
| [2026-04-19](results/bm-20260419-3.15.0a8%2B-e50acef-NOGIL) | python/e50acef0b2c2057874a9 | e50acef (NOGIL) | 1.099x ↑<br>[📄](results/bm-20260419-3.15.0a8%2B-e50acef-NOGIL/bm-20260419-macm4pro-arm64-python-e50acef0b2c2057874a9-3.15.0a8%2B-e50acef-vs-3.12.6.md)[📈](results/bm-20260419-3.15.0a8%2B-e50acef-NOGIL/bm-20260419-macm4pro-arm64-python-e50acef0b2c2057874a9-3.15.0a8%2B-e50acef-vs-3.12.6.svg) | 1.020x ↑<br>[📄](results/bm-20260419-3.15.0a8%2B-e50acef-NOGIL/bm-20260419-macm4pro-arm64-python-e50acef0b2c2057874a9-3.15.0a8%2B-e50acef-vs-3.13.0rc2.md)[📈](results/bm-20260419-3.15.0a8%2B-e50acef-NOGIL/bm-20260419-macm4pro-arm64-python-e50acef0b2c2057874a9-3.15.0a8%2B-e50acef-vs-3.13.0rc2.svg) | 1.054x ↓<br>[📄](results/bm-20260419-3.15.0a8%2B-e50acef-NOGIL/bm-20260419-macm4pro-arm64-python-e50acef0b2c2057874a9-3.15.0a8%2B-e50acef-vs-base.md)[📈](results/bm-20260419-3.15.0a8%2B-e50acef-NOGIL/bm-20260419-macm4pro-arm64-python-e50acef0b2c2057874a9-3.15.0a8%2B-e50acef-vs-base.svg)[🧠](results/bm-20260419-3.15.0a8%2B-e50acef-NOGIL/bm-20260419-macm4pro-arm64-python-e50acef0b2c2057874a9-3.15.0a8%2B-e50acef-vs-base-mem.svg) |
| [2026-04-19](results/bm-20260419-3.15.0a8%2B-e50acef) | python/e50acef0b2c2057874a9 | e50acef | 1.162x ↑<br>[📄](results/bm-20260419-3.15.0a8%2B-e50acef/bm-20260419-macm4pro-arm64-python-e50acef0b2c2057874a9-3.15.0a8%2B-e50acef-vs-3.12.6.md)[📈](results/bm-20260419-3.15.0a8%2B-e50acef/bm-20260419-macm4pro-arm64-python-e50acef0b2c2057874a9-3.15.0a8%2B-e50acef-vs-3.12.6.svg) | 1.078x ↑<br>[📄](results/bm-20260419-3.15.0a8%2B-e50acef/bm-20260419-macm4pro-arm64-python-e50acef0b2c2057874a9-3.15.0a8%2B-e50acef-vs-3.13.0rc2.md)[📈](results/bm-20260419-3.15.0a8%2B-e50acef/bm-20260419-macm4pro-arm64-python-e50acef0b2c2057874a9-3.15.0a8%2B-e50acef-vs-3.13.0rc2.svg) |  |


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
