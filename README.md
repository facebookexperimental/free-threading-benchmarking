# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (edd6f76)](results/bm-20261114-3.16.0a2%2Bdev-edd6f76/bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2%2Bdev-edd6f76-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (edd6f76)](results/bm-20261114-3.16.0a2%2Bdev-edd6f76-PYTHON_UOPS/bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2%2Bdev-edd6f76-pystats.md)
- [Most recent JIT pystats on main (bedaea0)](results/bm-20251019-3.15.0a1%2B-bedaea0-JIT/bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-11-19](results/bm-20261119-3.16.0a2%2Bdev-94250a7-NOGIL) | python/94250a7c0f6cbf51ff6b | 94250a7 (NOGIL) | 1.030x ↓<br>[📄](results/bm-20261119-3.16.0a2%2Bdev-94250a7-NOGIL/bm-20261119-vultr-x86_64-python-94250a7c0f6cbf51ff6b-3.16.0a2%2Bdev-94250a7-vs-3.12.6.md)[📈](results/bm-20261119-3.16.0a2%2Bdev-94250a7-NOGIL/bm-20261119-vultr-x86_64-python-94250a7c0f6cbf51ff6b-3.16.0a2%2Bdev-94250a7-vs-3.12.6.svg) | 1.064x ↓<br>[📄](results/bm-20261119-3.16.0a2%2Bdev-94250a7-NOGIL/bm-20261119-vultr-x86_64-python-94250a7c0f6cbf51ff6b-3.16.0a2%2Bdev-94250a7-vs-3.13.0rc2.md)[📈](results/bm-20261119-3.16.0a2%2Bdev-94250a7-NOGIL/bm-20261119-vultr-x86_64-python-94250a7c0f6cbf51ff6b-3.16.0a2%2Bdev-94250a7-vs-3.13.0rc2.svg) | 1.117x ↓<br>[📄](results/bm-20261119-3.16.0a2%2Bdev-94250a7-NOGIL/bm-20261119-vultr-x86_64-python-94250a7c0f6cbf51ff6b-3.16.0a2%2Bdev-94250a7-vs-base.md)[📈](results/bm-20261119-3.16.0a2%2Bdev-94250a7-NOGIL/bm-20261119-vultr-x86_64-python-94250a7c0f6cbf51ff6b-3.16.0a2%2Bdev-94250a7-vs-base.svg)[🧠](results/bm-20261119-3.16.0a2%2Bdev-94250a7-NOGIL/bm-20261119-vultr-x86_64-python-94250a7c0f6cbf51ff6b-3.16.0a2%2Bdev-94250a7-vs-base-mem.svg) |
| [2026-11-19](results/bm-20261119-3.16.0a2%2Bdev-94250a7) | python/94250a7c0f6cbf51ff6b | 94250a7 | 1.093x ↑<br>[📄](results/bm-20261119-3.16.0a2%2Bdev-94250a7/bm-20261119-vultr-x86_64-python-94250a7c0f6cbf51ff6b-3.16.0a2%2Bdev-94250a7-vs-3.12.6.md)[📈](results/bm-20261119-3.16.0a2%2Bdev-94250a7/bm-20261119-vultr-x86_64-python-94250a7c0f6cbf51ff6b-3.16.0a2%2Bdev-94250a7-vs-3.12.6.svg) | 1.056x ↑<br>[📄](results/bm-20261119-3.16.0a2%2Bdev-94250a7/bm-20261119-vultr-x86_64-python-94250a7c0f6cbf51ff6b-3.16.0a2%2Bdev-94250a7-vs-3.13.0rc2.md)[📈](results/bm-20261119-3.16.0a2%2Bdev-94250a7/bm-20261119-vultr-x86_64-python-94250a7c0f6cbf51ff6b-3.16.0a2%2Bdev-94250a7-vs-3.13.0rc2.svg) |  |
| [2026-11-18](results/bm-20261118-3.16.0a2%2Bdev-3ad9316-NOGIL) | python/3ad9316217ba4e2788ab | 3ad9316 (NOGIL) | 1.031x ↓<br>[📄](results/bm-20261118-3.16.0a2%2Bdev-3ad9316-NOGIL/bm-20261118-vultr-x86_64-python-3ad9316217ba4e2788ab-3.16.0a2%2Bdev-3ad9316-vs-3.12.6.md)[📈](results/bm-20261118-3.16.0a2%2Bdev-3ad9316-NOGIL/bm-20261118-vultr-x86_64-python-3ad9316217ba4e2788ab-3.16.0a2%2Bdev-3ad9316-vs-3.12.6.svg) | 1.064x ↓<br>[📄](results/bm-20261118-3.16.0a2%2Bdev-3ad9316-NOGIL/bm-20261118-vultr-x86_64-python-3ad9316217ba4e2788ab-3.16.0a2%2Bdev-3ad9316-vs-3.13.0rc2.md)[📈](results/bm-20261118-3.16.0a2%2Bdev-3ad9316-NOGIL/bm-20261118-vultr-x86_64-python-3ad9316217ba4e2788ab-3.16.0a2%2Bdev-3ad9316-vs-3.13.0rc2.svg) | 1.115x ↓<br>[📄](results/bm-20261118-3.16.0a2%2Bdev-3ad9316-NOGIL/bm-20261118-vultr-x86_64-python-3ad9316217ba4e2788ab-3.16.0a2%2Bdev-3ad9316-vs-base.md)[📈](results/bm-20261118-3.16.0a2%2Bdev-3ad9316-NOGIL/bm-20261118-vultr-x86_64-python-3ad9316217ba4e2788ab-3.16.0a2%2Bdev-3ad9316-vs-base.svg)[🧠](results/bm-20261118-3.16.0a2%2Bdev-3ad9316-NOGIL/bm-20261118-vultr-x86_64-python-3ad9316217ba4e2788ab-3.16.0a2%2Bdev-3ad9316-vs-base-mem.svg) |
| [2026-11-18](results/bm-20261118-3.16.0a2%2Bdev-3ad9316) | python/3ad9316217ba4e2788ab | 3ad9316 | 1.091x ↑<br>[📄](results/bm-20261118-3.16.0a2%2Bdev-3ad9316/bm-20261118-vultr-x86_64-python-3ad9316217ba4e2788ab-3.16.0a2%2Bdev-3ad9316-vs-3.12.6.md)[📈](results/bm-20261118-3.16.0a2%2Bdev-3ad9316/bm-20261118-vultr-x86_64-python-3ad9316217ba4e2788ab-3.16.0a2%2Bdev-3ad9316-vs-3.12.6.svg) | 1.054x ↑<br>[📄](results/bm-20261118-3.16.0a2%2Bdev-3ad9316/bm-20261118-vultr-x86_64-python-3ad9316217ba4e2788ab-3.16.0a2%2Bdev-3ad9316-vs-3.13.0rc2.md)[📈](results/bm-20261118-3.16.0a2%2Bdev-3ad9316/bm-20261118-vultr-x86_64-python-3ad9316217ba4e2788ab-3.16.0a2%2Bdev-3ad9316-vs-3.13.0rc2.svg) |  |
| [2026-11-16](results/bm-20261116-3.16.0a2%2Bdev-910a92b-NOGIL) | python/910a92babf40b7b34baa | 910a92b (NOGIL) | 1.026x ↓<br>[📄](results/bm-20261116-3.16.0a2%2Bdev-910a92b-NOGIL/bm-20261116-vultr-x86_64-python-910a92babf40b7b34baa-3.16.0a2%2Bdev-910a92b-vs-3.12.6.md)[📈](results/bm-20261116-3.16.0a2%2Bdev-910a92b-NOGIL/bm-20261116-vultr-x86_64-python-910a92babf40b7b34baa-3.16.0a2%2Bdev-910a92b-vs-3.12.6.svg) | 1.059x ↓<br>[📄](results/bm-20261116-3.16.0a2%2Bdev-910a92b-NOGIL/bm-20261116-vultr-x86_64-python-910a92babf40b7b34baa-3.16.0a2%2Bdev-910a92b-vs-3.13.0rc2.md)[📈](results/bm-20261116-3.16.0a2%2Bdev-910a92b-NOGIL/bm-20261116-vultr-x86_64-python-910a92babf40b7b34baa-3.16.0a2%2Bdev-910a92b-vs-3.13.0rc2.svg) | 1.112x ↓<br>[📄](results/bm-20261116-3.16.0a2%2Bdev-910a92b-NOGIL/bm-20261116-vultr-x86_64-python-910a92babf40b7b34baa-3.16.0a2%2Bdev-910a92b-vs-base.md)[📈](results/bm-20261116-3.16.0a2%2Bdev-910a92b-NOGIL/bm-20261116-vultr-x86_64-python-910a92babf40b7b34baa-3.16.0a2%2Bdev-910a92b-vs-base.svg)[🧠](results/bm-20261116-3.16.0a2%2Bdev-910a92b-NOGIL/bm-20261116-vultr-x86_64-python-910a92babf40b7b34baa-3.16.0a2%2Bdev-910a92b-vs-base-mem.svg) |
| [2026-11-16](results/bm-20261116-3.16.0a2%2Bdev-910a92b) | python/910a92babf40b7b34baa | 910a92b | 1.092x ↑<br>[📄](results/bm-20261116-3.16.0a2%2Bdev-910a92b/bm-20261116-vultr-x86_64-python-910a92babf40b7b34baa-3.16.0a2%2Bdev-910a92b-vs-3.12.6.md)[📈](results/bm-20261116-3.16.0a2%2Bdev-910a92b/bm-20261116-vultr-x86_64-python-910a92babf40b7b34baa-3.16.0a2%2Bdev-910a92b-vs-3.12.6.svg) | 1.055x ↑<br>[📄](results/bm-20261116-3.16.0a2%2Bdev-910a92b/bm-20261116-vultr-x86_64-python-910a92babf40b7b34baa-3.16.0a2%2Bdev-910a92b-vs-3.13.0rc2.md)[📈](results/bm-20261116-3.16.0a2%2Bdev-910a92b/bm-20261116-vultr-x86_64-python-910a92babf40b7b34baa-3.16.0a2%2Bdev-910a92b-vs-3.13.0rc2.svg) |  |
| [2026-11-15](results/bm-20261115-3.16.0a2%2Bdev-d8bc666-NOGIL) | python/d8bc6669c7f4bcf1a725 | d8bc666 (NOGIL) | 1.024x ↓<br>[📄](results/bm-20261115-3.16.0a2%2Bdev-d8bc666-NOGIL/bm-20261115-vultr-x86_64-python-d8bc6669c7f4bcf1a725-3.16.0a2%2Bdev-d8bc666-vs-3.12.6.md)[📈](results/bm-20261115-3.16.0a2%2Bdev-d8bc666-NOGIL/bm-20261115-vultr-x86_64-python-d8bc6669c7f4bcf1a725-3.16.0a2%2Bdev-d8bc666-vs-3.12.6.svg) | 1.057x ↓<br>[📄](results/bm-20261115-3.16.0a2%2Bdev-d8bc666-NOGIL/bm-20261115-vultr-x86_64-python-d8bc6669c7f4bcf1a725-3.16.0a2%2Bdev-d8bc666-vs-3.13.0rc2.md)[📈](results/bm-20261115-3.16.0a2%2Bdev-d8bc666-NOGIL/bm-20261115-vultr-x86_64-python-d8bc6669c7f4bcf1a725-3.16.0a2%2Bdev-d8bc666-vs-3.13.0rc2.svg) | 1.109x ↓<br>[📄](results/bm-20261115-3.16.0a2%2Bdev-d8bc666-NOGIL/bm-20261115-vultr-x86_64-python-d8bc6669c7f4bcf1a725-3.16.0a2%2Bdev-d8bc666-vs-base.md)[📈](results/bm-20261115-3.16.0a2%2Bdev-d8bc666-NOGIL/bm-20261115-vultr-x86_64-python-d8bc6669c7f4bcf1a725-3.16.0a2%2Bdev-d8bc666-vs-base.svg)[🧠](results/bm-20261115-3.16.0a2%2Bdev-d8bc666-NOGIL/bm-20261115-vultr-x86_64-python-d8bc6669c7f4bcf1a725-3.16.0a2%2Bdev-d8bc666-vs-base-mem.svg) |
| [2026-11-15](results/bm-20261115-3.16.0a2%2Bdev-d8bc666) | python/d8bc6669c7f4bcf1a725 | d8bc666 | 1.091x ↑<br>[📄](results/bm-20261115-3.16.0a2%2Bdev-d8bc666/bm-20261115-vultr-x86_64-python-d8bc6669c7f4bcf1a725-3.16.0a2%2Bdev-d8bc666-vs-3.12.6.md)[📈](results/bm-20261115-3.16.0a2%2Bdev-d8bc666/bm-20261115-vultr-x86_64-python-d8bc6669c7f4bcf1a725-3.16.0a2%2Bdev-d8bc666-vs-3.12.6.svg) | 1.054x ↑<br>[📄](results/bm-20261115-3.16.0a2%2Bdev-d8bc666/bm-20261115-vultr-x86_64-python-d8bc6669c7f4bcf1a725-3.16.0a2%2Bdev-d8bc666-vs-3.13.0rc2.md)[📈](results/bm-20261115-3.16.0a2%2Bdev-d8bc666/bm-20261115-vultr-x86_64-python-d8bc6669c7f4bcf1a725-3.16.0a2%2Bdev-d8bc666-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-11-19](results/bm-20261119-3.16.0a2%2Bdev-94250a7-NOGIL) | python/94250a7c0f6cbf51ff6b | 94250a7 (NOGIL) | 1.065x ↑<br>[📄](results/bm-20261119-3.16.0a2%2Bdev-94250a7-NOGIL/bm-20261119-macm4pro-arm64-python-94250a7c0f6cbf51ff6b-3.16.0a2%2Bdev-94250a7-vs-3.12.6.md)[📈](results/bm-20261119-3.16.0a2%2Bdev-94250a7-NOGIL/bm-20261119-macm4pro-arm64-python-94250a7c0f6cbf51ff6b-3.16.0a2%2Bdev-94250a7-vs-3.12.6.svg) | 1.013x ↓<br>[📄](results/bm-20261119-3.16.0a2%2Bdev-94250a7-NOGIL/bm-20261119-macm4pro-arm64-python-94250a7c0f6cbf51ff6b-3.16.0a2%2Bdev-94250a7-vs-3.13.0rc2.md)[📈](results/bm-20261119-3.16.0a2%2Bdev-94250a7-NOGIL/bm-20261119-macm4pro-arm64-python-94250a7c0f6cbf51ff6b-3.16.0a2%2Bdev-94250a7-vs-3.13.0rc2.svg) | 1.104x ↓<br>[📄](results/bm-20261119-3.16.0a2%2Bdev-94250a7-NOGIL/bm-20261119-macm4pro-arm64-python-94250a7c0f6cbf51ff6b-3.16.0a2%2Bdev-94250a7-vs-base.md)[📈](results/bm-20261119-3.16.0a2%2Bdev-94250a7-NOGIL/bm-20261119-macm4pro-arm64-python-94250a7c0f6cbf51ff6b-3.16.0a2%2Bdev-94250a7-vs-base.svg)[🧠](results/bm-20261119-3.16.0a2%2Bdev-94250a7-NOGIL/bm-20261119-macm4pro-arm64-python-94250a7c0f6cbf51ff6b-3.16.0a2%2Bdev-94250a7-vs-base-mem.svg) |
| [2026-11-19](results/bm-20261119-3.16.0a2%2Bdev-94250a7) | python/94250a7c0f6cbf51ff6b | 94250a7 | 1.194x ↑<br>[📄](results/bm-20261119-3.16.0a2%2Bdev-94250a7/bm-20261119-macm4pro-arm64-python-94250a7c0f6cbf51ff6b-3.16.0a2%2Bdev-94250a7-vs-3.12.6.md)[📈](results/bm-20261119-3.16.0a2%2Bdev-94250a7/bm-20261119-macm4pro-arm64-python-94250a7c0f6cbf51ff6b-3.16.0a2%2Bdev-94250a7-vs-3.12.6.svg) | 1.103x ↑<br>[📄](results/bm-20261119-3.16.0a2%2Bdev-94250a7/bm-20261119-macm4pro-arm64-python-94250a7c0f6cbf51ff6b-3.16.0a2%2Bdev-94250a7-vs-3.13.0rc2.md)[📈](results/bm-20261119-3.16.0a2%2Bdev-94250a7/bm-20261119-macm4pro-arm64-python-94250a7c0f6cbf51ff6b-3.16.0a2%2Bdev-94250a7-vs-3.13.0rc2.svg) |  |
| [2026-11-18](results/bm-20261118-3.16.0a2%2Bdev-3ad9316-NOGIL) | python/3ad9316217ba4e2788ab | 3ad9316 (NOGIL) | 1.058x ↑<br>[📄](results/bm-20261118-3.16.0a2%2Bdev-3ad9316-NOGIL/bm-20261118-macm4pro-arm64-python-3ad9316217ba4e2788ab-3.16.0a2%2Bdev-3ad9316-vs-3.12.6.md)[📈](results/bm-20261118-3.16.0a2%2Bdev-3ad9316-NOGIL/bm-20261118-macm4pro-arm64-python-3ad9316217ba4e2788ab-3.16.0a2%2Bdev-3ad9316-vs-3.12.6.svg) | 1.020x ↓<br>[📄](results/bm-20261118-3.16.0a2%2Bdev-3ad9316-NOGIL/bm-20261118-macm4pro-arm64-python-3ad9316217ba4e2788ab-3.16.0a2%2Bdev-3ad9316-vs-3.13.0rc2.md)[📈](results/bm-20261118-3.16.0a2%2Bdev-3ad9316-NOGIL/bm-20261118-macm4pro-arm64-python-3ad9316217ba4e2788ab-3.16.0a2%2Bdev-3ad9316-vs-3.13.0rc2.svg) | 1.102x ↓<br>[📄](results/bm-20261118-3.16.0a2%2Bdev-3ad9316-NOGIL/bm-20261118-macm4pro-arm64-python-3ad9316217ba4e2788ab-3.16.0a2%2Bdev-3ad9316-vs-base.md)[📈](results/bm-20261118-3.16.0a2%2Bdev-3ad9316-NOGIL/bm-20261118-macm4pro-arm64-python-3ad9316217ba4e2788ab-3.16.0a2%2Bdev-3ad9316-vs-base.svg)[🧠](results/bm-20261118-3.16.0a2%2Bdev-3ad9316-NOGIL/bm-20261118-macm4pro-arm64-python-3ad9316217ba4e2788ab-3.16.0a2%2Bdev-3ad9316-vs-base-mem.svg) |
| [2026-11-18](results/bm-20261118-3.16.0a2%2Bdev-3ad9316) | python/3ad9316217ba4e2788ab | 3ad9316 | 1.183x ↑<br>[📄](results/bm-20261118-3.16.0a2%2Bdev-3ad9316/bm-20261118-macm4pro-arm64-python-3ad9316217ba4e2788ab-3.16.0a2%2Bdev-3ad9316-vs-3.12.6.md)[📈](results/bm-20261118-3.16.0a2%2Bdev-3ad9316/bm-20261118-macm4pro-arm64-python-3ad9316217ba4e2788ab-3.16.0a2%2Bdev-3ad9316-vs-3.12.6.svg) | 1.093x ↑<br>[📄](results/bm-20261118-3.16.0a2%2Bdev-3ad9316/bm-20261118-macm4pro-arm64-python-3ad9316217ba4e2788ab-3.16.0a2%2Bdev-3ad9316-vs-3.13.0rc2.md)[📈](results/bm-20261118-3.16.0a2%2Bdev-3ad9316/bm-20261118-macm4pro-arm64-python-3ad9316217ba4e2788ab-3.16.0a2%2Bdev-3ad9316-vs-3.13.0rc2.svg) |  |
| [2026-11-16](results/bm-20261116-3.16.0a2%2Bdev-910a92b-NOGIL) | python/910a92babf40b7b34baa | 910a92b (NOGIL) | 1.075x ↑<br>[📄](results/bm-20261116-3.16.0a2%2Bdev-910a92b-NOGIL/bm-20261116-macm4pro-arm64-python-910a92babf40b7b34baa-3.16.0a2%2Bdev-910a92b-vs-3.12.6.md)[📈](results/bm-20261116-3.16.0a2%2Bdev-910a92b-NOGIL/bm-20261116-macm4pro-arm64-python-910a92babf40b7b34baa-3.16.0a2%2Bdev-910a92b-vs-3.12.6.svg) | 1.005x ↓<br>[📄](results/bm-20261116-3.16.0a2%2Bdev-910a92b-NOGIL/bm-20261116-macm4pro-arm64-python-910a92babf40b7b34baa-3.16.0a2%2Bdev-910a92b-vs-3.13.0rc2.md)[📈](results/bm-20261116-3.16.0a2%2Bdev-910a92b-NOGIL/bm-20261116-macm4pro-arm64-python-910a92babf40b7b34baa-3.16.0a2%2Bdev-910a92b-vs-3.13.0rc2.svg) | 1.102x ↓<br>[📄](results/bm-20261116-3.16.0a2%2Bdev-910a92b-NOGIL/bm-20261116-macm4pro-arm64-python-910a92babf40b7b34baa-3.16.0a2%2Bdev-910a92b-vs-base.md)[📈](results/bm-20261116-3.16.0a2%2Bdev-910a92b-NOGIL/bm-20261116-macm4pro-arm64-python-910a92babf40b7b34baa-3.16.0a2%2Bdev-910a92b-vs-base.svg)[🧠](results/bm-20261116-3.16.0a2%2Bdev-910a92b-NOGIL/bm-20261116-macm4pro-arm64-python-910a92babf40b7b34baa-3.16.0a2%2Bdev-910a92b-vs-base-mem.svg) |
| [2026-11-16](results/bm-20261116-3.16.0a2%2Bdev-910a92b) | python/910a92babf40b7b34baa | 910a92b | 1.202x ↑<br>[📄](results/bm-20261116-3.16.0a2%2Bdev-910a92b/bm-20261116-macm4pro-arm64-python-910a92babf40b7b34baa-3.16.0a2%2Bdev-910a92b-vs-3.12.6.md)[📈](results/bm-20261116-3.16.0a2%2Bdev-910a92b/bm-20261116-macm4pro-arm64-python-910a92babf40b7b34baa-3.16.0a2%2Bdev-910a92b-vs-3.12.6.svg) | 1.110x ↑<br>[📄](results/bm-20261116-3.16.0a2%2Bdev-910a92b/bm-20261116-macm4pro-arm64-python-910a92babf40b7b34baa-3.16.0a2%2Bdev-910a92b-vs-3.13.0rc2.md)[📈](results/bm-20261116-3.16.0a2%2Bdev-910a92b/bm-20261116-macm4pro-arm64-python-910a92babf40b7b34baa-3.16.0a2%2Bdev-910a92b-vs-3.13.0rc2.svg) |  |
| [2026-11-15](results/bm-20261115-3.16.0a2%2Bdev-d8bc666-NOGIL) | python/d8bc6669c7f4bcf1a725 | d8bc666 (NOGIL) | 1.068x ↑<br>[📄](results/bm-20261115-3.16.0a2%2Bdev-d8bc666-NOGIL/bm-20261115-macm4pro-arm64-python-d8bc6669c7f4bcf1a725-3.16.0a2%2Bdev-d8bc666-vs-3.12.6.md)[📈](results/bm-20261115-3.16.0a2%2Bdev-d8bc666-NOGIL/bm-20261115-macm4pro-arm64-python-d8bc6669c7f4bcf1a725-3.16.0a2%2Bdev-d8bc666-vs-3.12.6.svg) | 1.011x ↓<br>[📄](results/bm-20261115-3.16.0a2%2Bdev-d8bc666-NOGIL/bm-20261115-macm4pro-arm64-python-d8bc6669c7f4bcf1a725-3.16.0a2%2Bdev-d8bc666-vs-3.13.0rc2.md)[📈](results/bm-20261115-3.16.0a2%2Bdev-d8bc666-NOGIL/bm-20261115-macm4pro-arm64-python-d8bc6669c7f4bcf1a725-3.16.0a2%2Bdev-d8bc666-vs-3.13.0rc2.svg) | 1.097x ↓<br>[📄](results/bm-20261115-3.16.0a2%2Bdev-d8bc666-NOGIL/bm-20261115-macm4pro-arm64-python-d8bc6669c7f4bcf1a725-3.16.0a2%2Bdev-d8bc666-vs-base.md)[📈](results/bm-20261115-3.16.0a2%2Bdev-d8bc666-NOGIL/bm-20261115-macm4pro-arm64-python-d8bc6669c7f4bcf1a725-3.16.0a2%2Bdev-d8bc666-vs-base.svg)[🧠](results/bm-20261115-3.16.0a2%2Bdev-d8bc666-NOGIL/bm-20261115-macm4pro-arm64-python-d8bc6669c7f4bcf1a725-3.16.0a2%2Bdev-d8bc666-vs-base-mem.svg) |
| [2026-11-15](results/bm-20261115-3.16.0a2%2Bdev-d8bc666) | python/d8bc6669c7f4bcf1a725 | d8bc666 | 1.187x ↑<br>[📄](results/bm-20261115-3.16.0a2%2Bdev-d8bc666/bm-20261115-macm4pro-arm64-python-d8bc6669c7f4bcf1a725-3.16.0a2%2Bdev-d8bc666-vs-3.12.6.md)[📈](results/bm-20261115-3.16.0a2%2Bdev-d8bc666/bm-20261115-macm4pro-arm64-python-d8bc6669c7f4bcf1a725-3.16.0a2%2Bdev-d8bc666-vs-3.12.6.svg) | 1.097x ↑<br>[📄](results/bm-20261115-3.16.0a2%2Bdev-d8bc666/bm-20261115-macm4pro-arm64-python-d8bc6669c7f4bcf1a725-3.16.0a2%2Bdev-d8bc666-vs-3.13.0rc2.md)[📈](results/bm-20261115-3.16.0a2%2Bdev-d8bc666/bm-20261115-macm4pro-arm64-python-d8bc6669c7f4bcf1a725-3.16.0a2%2Bdev-d8bc666-vs-3.13.0rc2.svg) |  |


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
