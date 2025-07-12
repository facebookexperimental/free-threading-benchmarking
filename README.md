# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (1953713)](results/bm-20250705-3.15.0a0-1953713/bm-20250705-vultr-x86_64-python-1953713d0d67a4f54ff7-3.15.0a0-1953713-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (1953713)](results/bm-20250705-3.15.0a0-1953713-PYTHON_UOPS/bm-20250705-vultr-x86_64-python-1953713d0d67a4f54ff7-3.15.0a0-1953713-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-07-11](results/bm-20250711-3.15.0a0-db47f4d-NOGIL) | python/db47f4d844acf2b6e52e | db47f4d (NOGIL) | 1.022x ↓<br>[📄](results/bm-20250711-3.15.0a0-db47f4d-NOGIL/bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d-vs-3.12.6.md)[📈](results/bm-20250711-3.15.0a0-db47f4d-NOGIL/bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d-vs-3.12.6.svg) | 1.055x ↓<br>[📄](results/bm-20250711-3.15.0a0-db47f4d-NOGIL/bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d-vs-3.13.0rc2.md)[📈](results/bm-20250711-3.15.0a0-db47f4d-NOGIL/bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d-vs-3.13.0rc2.svg) | 1.093x ↓<br>[📄](results/bm-20250711-3.15.0a0-db47f4d-NOGIL/bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d-vs-base.md)[📈](results/bm-20250711-3.15.0a0-db47f4d-NOGIL/bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d-vs-base.svg)[🧠](results/bm-20250711-3.15.0a0-db47f4d-NOGIL/bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d-vs-base-mem.svg) |
| [2025-07-11](results/bm-20250711-3.15.0a0-db47f4d) | python/db47f4d844acf2b6e52e | db47f4d | 1.071x ↑<br>[📄](results/bm-20250711-3.15.0a0-db47f4d/bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d-vs-3.12.6.md)[📈](results/bm-20250711-3.15.0a0-db47f4d/bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d-vs-3.12.6.svg) | 1.036x ↑<br>[📄](results/bm-20250711-3.15.0a0-db47f4d/bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d-vs-3.13.0rc2.md)[📈](results/bm-20250711-3.15.0a0-db47f4d/bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d-vs-3.13.0rc2.svg) |  |
| [2025-07-10](results/bm-20250710-3.15.0a0-49365bd-NOGIL) | python/49365bd110a254a6a304 | 49365bd (NOGIL) | 1.025x ↓<br>[📄](results/bm-20250710-3.15.0a0-49365bd-NOGIL/bm-20250710-vultr-x86_64-python-49365bd110a254a6a304-3.15.0a0-49365bd-vs-3.12.6.md)[📈](results/bm-20250710-3.15.0a0-49365bd-NOGIL/bm-20250710-vultr-x86_64-python-49365bd110a254a6a304-3.15.0a0-49365bd-vs-3.12.6.svg) | 1.057x ↓<br>[📄](results/bm-20250710-3.15.0a0-49365bd-NOGIL/bm-20250710-vultr-x86_64-python-49365bd110a254a6a304-3.15.0a0-49365bd-vs-3.13.0rc2.md)[📈](results/bm-20250710-3.15.0a0-49365bd-NOGIL/bm-20250710-vultr-x86_64-python-49365bd110a254a6a304-3.15.0a0-49365bd-vs-3.13.0rc2.svg) | 1.095x ↓<br>[📄](results/bm-20250710-3.15.0a0-49365bd-NOGIL/bm-20250710-vultr-x86_64-python-49365bd110a254a6a304-3.15.0a0-49365bd-vs-base.md)[📈](results/bm-20250710-3.15.0a0-49365bd-NOGIL/bm-20250710-vultr-x86_64-python-49365bd110a254a6a304-3.15.0a0-49365bd-vs-base.svg)[🧠](results/bm-20250710-3.15.0a0-49365bd-NOGIL/bm-20250710-vultr-x86_64-python-49365bd110a254a6a304-3.15.0a0-49365bd-vs-base-mem.svg) |
| [2025-07-10](results/bm-20250710-3.15.0a0-49365bd) | python/49365bd110a254a6a304 | 49365bd | 1.071x ↑<br>[📄](results/bm-20250710-3.15.0a0-49365bd/bm-20250710-vultr-x86_64-python-49365bd110a254a6a304-3.15.0a0-49365bd-vs-3.12.6.md)[📈](results/bm-20250710-3.15.0a0-49365bd/bm-20250710-vultr-x86_64-python-49365bd110a254a6a304-3.15.0a0-49365bd-vs-3.12.6.svg) | 1.036x ↑<br>[📄](results/bm-20250710-3.15.0a0-49365bd/bm-20250710-vultr-x86_64-python-49365bd110a254a6a304-3.15.0a0-49365bd-vs-3.13.0rc2.md)[📈](results/bm-20250710-3.15.0a0-49365bd/bm-20250710-vultr-x86_64-python-49365bd110a254a6a304-3.15.0a0-49365bd-vs-3.13.0rc2.svg) |  |
| [2025-07-10](results/bm-20250710-3.15.0a0-61dd9fd-NOGIL) | python/61dd9fdad729fe02d91c | 61dd9fd (NOGIL) | 1.027x ↓<br>[📄](results/bm-20250710-3.15.0a0-61dd9fd-NOGIL/bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd-vs-3.12.6.md)[📈](results/bm-20250710-3.15.0a0-61dd9fd-NOGIL/bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd-vs-3.12.6.svg) | 1.059x ↓<br>[📄](results/bm-20250710-3.15.0a0-61dd9fd-NOGIL/bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd-vs-3.13.0rc2.md)[📈](results/bm-20250710-3.15.0a0-61dd9fd-NOGIL/bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd-vs-3.13.0rc2.svg) | 1.092x ↓<br>[📄](results/bm-20250710-3.15.0a0-61dd9fd-NOGIL/bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd-vs-base.md)[📈](results/bm-20250710-3.15.0a0-61dd9fd-NOGIL/bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd-vs-base.svg)[🧠](results/bm-20250710-3.15.0a0-61dd9fd-NOGIL/bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd-vs-base-mem.svg) |
| [2025-07-10](results/bm-20250710-3.15.0a0-61dd9fd) | python/61dd9fdad729fe02d91c | 61dd9fd | 1.067x ↑<br>[📄](results/bm-20250710-3.15.0a0-61dd9fd/bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd-vs-3.12.6.md)[📈](results/bm-20250710-3.15.0a0-61dd9fd/bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd-vs-3.12.6.svg) | 1.031x ↑<br>[📄](results/bm-20250710-3.15.0a0-61dd9fd/bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd-vs-3.13.0rc2.md)[📈](results/bm-20250710-3.15.0a0-61dd9fd/bm-20250710-vultr-x86_64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd-vs-3.13.0rc2.svg) |  |
| [2025-07-08](results/bm-20250708-3.15.0a0-a6566e4-NOGIL) | python/a6566e49e63219b6dad6 | a6566e4 (NOGIL) | 1.025x ↓<br>[📄](results/bm-20250708-3.15.0a0-a6566e4-NOGIL/bm-20250708-vultr-x86_64-python-a6566e49e63219b6dad6-3.15.0a0-a6566e4-vs-3.12.6.md)[📈](results/bm-20250708-3.15.0a0-a6566e4-NOGIL/bm-20250708-vultr-x86_64-python-a6566e49e63219b6dad6-3.15.0a0-a6566e4-vs-3.12.6.svg) | 1.058x ↓<br>[📄](results/bm-20250708-3.15.0a0-a6566e4-NOGIL/bm-20250708-vultr-x86_64-python-a6566e49e63219b6dad6-3.15.0a0-a6566e4-vs-3.13.0rc2.md)[📈](results/bm-20250708-3.15.0a0-a6566e4-NOGIL/bm-20250708-vultr-x86_64-python-a6566e49e63219b6dad6-3.15.0a0-a6566e4-vs-3.13.0rc2.svg) | 1.094x ↓<br>[📄](results/bm-20250708-3.15.0a0-a6566e4-NOGIL/bm-20250708-vultr-x86_64-python-a6566e49e63219b6dad6-3.15.0a0-a6566e4-vs-base.md)[📈](results/bm-20250708-3.15.0a0-a6566e4-NOGIL/bm-20250708-vultr-x86_64-python-a6566e49e63219b6dad6-3.15.0a0-a6566e4-vs-base.svg)[🧠](results/bm-20250708-3.15.0a0-a6566e4-NOGIL/bm-20250708-vultr-x86_64-python-a6566e49e63219b6dad6-3.15.0a0-a6566e4-vs-base-mem.svg) |
| [2025-07-08](results/bm-20250708-3.15.0a0-a6566e4) | python/a6566e49e63219b6dad6 | a6566e4 | 1.070x ↑<br>[📄](results/bm-20250708-3.15.0a0-a6566e4/bm-20250708-vultr-x86_64-python-a6566e49e63219b6dad6-3.15.0a0-a6566e4-vs-3.12.6.md)[📈](results/bm-20250708-3.15.0a0-a6566e4/bm-20250708-vultr-x86_64-python-a6566e49e63219b6dad6-3.15.0a0-a6566e4-vs-3.12.6.svg) | 1.034x ↑<br>[📄](results/bm-20250708-3.15.0a0-a6566e4/bm-20250708-vultr-x86_64-python-a6566e49e63219b6dad6-3.15.0a0-a6566e4-vs-3.13.0rc2.md)[📈](results/bm-20250708-3.15.0a0-a6566e4/bm-20250708-vultr-x86_64-python-a6566e49e63219b6dad6-3.15.0a0-a6566e4-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-07-11](results/bm-20250711-3.15.0a0-db47f4d-NOGIL) | python/db47f4d844acf2b6e52e | db47f4d (NOGIL) | 1.096x ↑<br>[📄](results/bm-20250711-3.15.0a0-db47f4d-NOGIL/bm-20250711-macm4pro-arm64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d-vs-3.12.6.md)[📈](results/bm-20250711-3.15.0a0-db47f4d-NOGIL/bm-20250711-macm4pro-arm64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d-vs-3.12.6.svg) | 1.017x ↑<br>[📄](results/bm-20250711-3.15.0a0-db47f4d-NOGIL/bm-20250711-macm4pro-arm64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d-vs-3.13.0rc2.md)[📈](results/bm-20250711-3.15.0a0-db47f4d-NOGIL/bm-20250711-macm4pro-arm64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d-vs-3.13.0rc2.svg) | 1.007x ↑<br>[📄](results/bm-20250711-3.15.0a0-db47f4d-NOGIL/bm-20250711-macm4pro-arm64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d-vs-base.md)[📈](results/bm-20250711-3.15.0a0-db47f4d-NOGIL/bm-20250711-macm4pro-arm64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d-vs-base.svg)[🧠](results/bm-20250711-3.15.0a0-db47f4d-NOGIL/bm-20250711-macm4pro-arm64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d-vs-base-mem.svg) |
| [2025-07-11](results/bm-20250711-3.15.0a0-db47f4d) | python/db47f4d844acf2b6e52e | db47f4d | 1.089x ↑<br>[📄](results/bm-20250711-3.15.0a0-db47f4d/bm-20250711-macm4pro-arm64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d-vs-3.12.6.md)[📈](results/bm-20250711-3.15.0a0-db47f4d/bm-20250711-macm4pro-arm64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d-vs-3.12.6.svg) | 1.010x ↑<br>[📄](results/bm-20250711-3.15.0a0-db47f4d/bm-20250711-macm4pro-arm64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d-vs-3.13.0rc2.md)[📈](results/bm-20250711-3.15.0a0-db47f4d/bm-20250711-macm4pro-arm64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d-vs-3.13.0rc2.svg) |  |
| [2025-07-10](results/bm-20250710-3.15.0a0-49365bd-NOGIL) | python/49365bd110a254a6a304 | 49365bd (NOGIL) | 1.093x ↑<br>[📄](results/bm-20250710-3.15.0a0-49365bd-NOGIL/bm-20250710-macm4pro-arm64-python-49365bd110a254a6a304-3.15.0a0-49365bd-vs-3.12.6.md)[📈](results/bm-20250710-3.15.0a0-49365bd-NOGIL/bm-20250710-macm4pro-arm64-python-49365bd110a254a6a304-3.15.0a0-49365bd-vs-3.12.6.svg) | 1.014x ↑<br>[📄](results/bm-20250710-3.15.0a0-49365bd-NOGIL/bm-20250710-macm4pro-arm64-python-49365bd110a254a6a304-3.15.0a0-49365bd-vs-3.13.0rc2.md)[📈](results/bm-20250710-3.15.0a0-49365bd-NOGIL/bm-20250710-macm4pro-arm64-python-49365bd110a254a6a304-3.15.0a0-49365bd-vs-3.13.0rc2.svg) | 1.002x ↑<br>[📄](results/bm-20250710-3.15.0a0-49365bd-NOGIL/bm-20250710-macm4pro-arm64-python-49365bd110a254a6a304-3.15.0a0-49365bd-vs-base.md)[📈](results/bm-20250710-3.15.0a0-49365bd-NOGIL/bm-20250710-macm4pro-arm64-python-49365bd110a254a6a304-3.15.0a0-49365bd-vs-base.svg)[🧠](results/bm-20250710-3.15.0a0-49365bd-NOGIL/bm-20250710-macm4pro-arm64-python-49365bd110a254a6a304-3.15.0a0-49365bd-vs-base-mem.svg) |
| [2025-07-10](results/bm-20250710-3.15.0a0-49365bd) | python/49365bd110a254a6a304 | 49365bd | 1.088x ↑<br>[📄](results/bm-20250710-3.15.0a0-49365bd/bm-20250710-macm4pro-arm64-python-49365bd110a254a6a304-3.15.0a0-49365bd-vs-3.12.6.md)[📈](results/bm-20250710-3.15.0a0-49365bd/bm-20250710-macm4pro-arm64-python-49365bd110a254a6a304-3.15.0a0-49365bd-vs-3.12.6.svg) | 1.009x ↑<br>[📄](results/bm-20250710-3.15.0a0-49365bd/bm-20250710-macm4pro-arm64-python-49365bd110a254a6a304-3.15.0a0-49365bd-vs-3.13.0rc2.md)[📈](results/bm-20250710-3.15.0a0-49365bd/bm-20250710-macm4pro-arm64-python-49365bd110a254a6a304-3.15.0a0-49365bd-vs-3.13.0rc2.svg) |  |
| [2025-07-10](results/bm-20250710-3.15.0a0-61dd9fd-NOGIL) | python/61dd9fdad729fe02d91c | 61dd9fd (NOGIL) | 1.102x ↑<br>[📄](results/bm-20250710-3.15.0a0-61dd9fd-NOGIL/bm-20250710-macm4pro-arm64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd-vs-3.12.6.md)[📈](results/bm-20250710-3.15.0a0-61dd9fd-NOGIL/bm-20250710-macm4pro-arm64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd-vs-3.12.6.svg) | 1.022x ↑<br>[📄](results/bm-20250710-3.15.0a0-61dd9fd-NOGIL/bm-20250710-macm4pro-arm64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd-vs-3.13.0rc2.md)[📈](results/bm-20250710-3.15.0a0-61dd9fd-NOGIL/bm-20250710-macm4pro-arm64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd-vs-3.13.0rc2.svg) | 1.010x ↓<br>[📄](results/bm-20250710-3.15.0a0-61dd9fd-NOGIL/bm-20250710-macm4pro-arm64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd-vs-base.md)[📈](results/bm-20250710-3.15.0a0-61dd9fd-NOGIL/bm-20250710-macm4pro-arm64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd-vs-base.svg)[🧠](results/bm-20250710-3.15.0a0-61dd9fd-NOGIL/bm-20250710-macm4pro-arm64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd-vs-base-mem.svg) |
| [2025-07-10](results/bm-20250710-3.15.0a0-61dd9fd) | python/61dd9fdad729fe02d91c | 61dd9fd | 1.111x ↑<br>[📄](results/bm-20250710-3.15.0a0-61dd9fd/bm-20250710-macm4pro-arm64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd-vs-3.12.6.md)[📈](results/bm-20250710-3.15.0a0-61dd9fd/bm-20250710-macm4pro-arm64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd-vs-3.12.6.svg) | 1.031x ↑<br>[📄](results/bm-20250710-3.15.0a0-61dd9fd/bm-20250710-macm4pro-arm64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd-vs-3.13.0rc2.md)[📈](results/bm-20250710-3.15.0a0-61dd9fd/bm-20250710-macm4pro-arm64-python-61dd9fdad729fe02d91c-3.15.0a0-61dd9fd-vs-3.13.0rc2.svg) |  |
| [2025-07-08](results/bm-20250708-3.15.0a0-a6566e4-NOGIL) | python/a6566e49e63219b6dad6 | a6566e4 (NOGIL) | 1.100x ↑<br>[📄](results/bm-20250708-3.15.0a0-a6566e4-NOGIL/bm-20250708-macm4pro-arm64-python-a6566e49e63219b6dad6-3.15.0a0-a6566e4-vs-3.12.6.md)[📈](results/bm-20250708-3.15.0a0-a6566e4-NOGIL/bm-20250708-macm4pro-arm64-python-a6566e49e63219b6dad6-3.15.0a0-a6566e4-vs-3.12.6.svg) | 1.020x ↑<br>[📄](results/bm-20250708-3.15.0a0-a6566e4-NOGIL/bm-20250708-macm4pro-arm64-python-a6566e49e63219b6dad6-3.15.0a0-a6566e4-vs-3.13.0rc2.md)[📈](results/bm-20250708-3.15.0a0-a6566e4-NOGIL/bm-20250708-macm4pro-arm64-python-a6566e49e63219b6dad6-3.15.0a0-a6566e4-vs-3.13.0rc2.svg) | 1.010x ↓<br>[📄](results/bm-20250708-3.15.0a0-a6566e4-NOGIL/bm-20250708-macm4pro-arm64-python-a6566e49e63219b6dad6-3.15.0a0-a6566e4-vs-base.md)[📈](results/bm-20250708-3.15.0a0-a6566e4-NOGIL/bm-20250708-macm4pro-arm64-python-a6566e49e63219b6dad6-3.15.0a0-a6566e4-vs-base.svg)[🧠](results/bm-20250708-3.15.0a0-a6566e4-NOGIL/bm-20250708-macm4pro-arm64-python-a6566e49e63219b6dad6-3.15.0a0-a6566e4-vs-base-mem.svg) |
| [2025-07-08](results/bm-20250708-3.15.0a0-a6566e4) | python/a6566e49e63219b6dad6 | a6566e4 | 1.109x ↑<br>[📄](results/bm-20250708-3.15.0a0-a6566e4/bm-20250708-macm4pro-arm64-python-a6566e49e63219b6dad6-3.15.0a0-a6566e4-vs-3.12.6.md)[📈](results/bm-20250708-3.15.0a0-a6566e4/bm-20250708-macm4pro-arm64-python-a6566e49e63219b6dad6-3.15.0a0-a6566e4-vs-3.12.6.svg) | 1.028x ↑<br>[📄](results/bm-20250708-3.15.0a0-a6566e4/bm-20250708-macm4pro-arm64-python-a6566e49e63219b6dad6-3.15.0a0-a6566e4-vs-3.13.0rc2.md)[📈](results/bm-20250708-3.15.0a0-a6566e4/bm-20250708-macm4pro-arm64-python-a6566e49e63219b6dad6-3.15.0a0-a6566e4-vs-3.13.0rc2.svg) |  |


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
