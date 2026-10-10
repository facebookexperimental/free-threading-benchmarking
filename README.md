# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (9d22a53)](results/bm-20261003-3.16.0a0-9d22a53/bm-20261003-vultr-x86_64-python-9d22a5334bd5273962ad-3.16.0a0-9d22a53-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (9d22a53)](results/bm-20261003-3.16.0a0-9d22a53-PYTHON_UOPS/bm-20261003-vultr-x86_64-python-9d22a5334bd5273962ad-3.16.0a0-9d22a53-pystats.md)
- [Most recent JIT pystats on main (bedaea0)](results/bm-20251019-3.15.0a1%2B-bedaea0-JIT/bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-10-09](results/bm-20261009-3.16.0a0-0ec3aee-NOGIL) | python/0ec3aee262b03276a18a | 0ec3aee (NOGIL) | 1.043x ↓<br>[📄](results/bm-20261009-3.16.0a0-0ec3aee-NOGIL/bm-20261009-vultr-x86_64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee-vs-3.12.6.md)[📈](results/bm-20261009-3.16.0a0-0ec3aee-NOGIL/bm-20261009-vultr-x86_64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee-vs-3.12.6.svg) | 1.075x ↓<br>[📄](results/bm-20261009-3.16.0a0-0ec3aee-NOGIL/bm-20261009-vultr-x86_64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee-vs-3.13.0rc2.md)[📈](results/bm-20261009-3.16.0a0-0ec3aee-NOGIL/bm-20261009-vultr-x86_64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee-vs-3.13.0rc2.svg) |  |
| [2026-10-08](results/bm-20261008-3.16.0a0-bc12b72-NOGIL) | python/bc12b7285f87f3ca9118 | bc12b72 (NOGIL) | 1.038x ↓<br>[📄](results/bm-20261008-3.16.0a0-bc12b72-NOGIL/bm-20261008-vultr-x86_64-python-bc12b7285f87f3ca9118-3.16.0a0-bc12b72-vs-3.12.6.md)[📈](results/bm-20261008-3.16.0a0-bc12b72-NOGIL/bm-20261008-vultr-x86_64-python-bc12b7285f87f3ca9118-3.16.0a0-bc12b72-vs-3.12.6.svg) | 1.071x ↓<br>[📄](results/bm-20261008-3.16.0a0-bc12b72-NOGIL/bm-20261008-vultr-x86_64-python-bc12b7285f87f3ca9118-3.16.0a0-bc12b72-vs-3.13.0rc2.md)[📈](results/bm-20261008-3.16.0a0-bc12b72-NOGIL/bm-20261008-vultr-x86_64-python-bc12b7285f87f3ca9118-3.16.0a0-bc12b72-vs-3.13.0rc2.svg) | 1.101x ↓<br>[📄](results/bm-20261008-3.16.0a0-bc12b72-NOGIL/bm-20261008-vultr-x86_64-python-bc12b7285f87f3ca9118-3.16.0a0-bc12b72-vs-base.md)[📈](results/bm-20261008-3.16.0a0-bc12b72-NOGIL/bm-20261008-vultr-x86_64-python-bc12b7285f87f3ca9118-3.16.0a0-bc12b72-vs-base.svg)[🧠](results/bm-20261008-3.16.0a0-bc12b72-NOGIL/bm-20261008-vultr-x86_64-python-bc12b7285f87f3ca9118-3.16.0a0-bc12b72-vs-base-mem.svg) |
| [2026-10-08](results/bm-20261008-3.16.0a0-bc12b72) | python/bc12b7285f87f3ca9118 | bc12b72 | 1.066x ↑<br>[📄](results/bm-20261008-3.16.0a0-bc12b72/bm-20261008-vultr-x86_64-python-bc12b7285f87f3ca9118-3.16.0a0-bc12b72-vs-3.12.6.md)[📈](results/bm-20261008-3.16.0a0-bc12b72/bm-20261008-vultr-x86_64-python-bc12b7285f87f3ca9118-3.16.0a0-bc12b72-vs-3.12.6.svg) | 1.030x ↑<br>[📄](results/bm-20261008-3.16.0a0-bc12b72/bm-20261008-vultr-x86_64-python-bc12b7285f87f3ca9118-3.16.0a0-bc12b72-vs-3.13.0rc2.md)[📈](results/bm-20261008-3.16.0a0-bc12b72/bm-20261008-vultr-x86_64-python-bc12b7285f87f3ca9118-3.16.0a0-bc12b72-vs-3.13.0rc2.svg) |  |
| [2026-10-08](results/bm-20261008-3.16.0a0-cdfdf7b-NOGIL) | python/cdfdf7bb73a5751ecec7 | cdfdf7b (NOGIL) | 1.042x ↓<br>[📄](results/bm-20261008-3.16.0a0-cdfdf7b-NOGIL/bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b-vs-3.12.6.md)[📈](results/bm-20261008-3.16.0a0-cdfdf7b-NOGIL/bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b-vs-3.12.6.svg) | 1.074x ↓<br>[📄](results/bm-20261008-3.16.0a0-cdfdf7b-NOGIL/bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b-vs-3.13.0rc2.md)[📈](results/bm-20261008-3.16.0a0-cdfdf7b-NOGIL/bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b-vs-3.13.0rc2.svg) | 1.107x ↓<br>[📄](results/bm-20261008-3.16.0a0-cdfdf7b-NOGIL/bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b-vs-base.md)[📈](results/bm-20261008-3.16.0a0-cdfdf7b-NOGIL/bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b-vs-base.svg)[🧠](results/bm-20261008-3.16.0a0-cdfdf7b-NOGIL/bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b-vs-base-mem.svg) |
| [2026-10-08](results/bm-20261008-3.16.0a0-cdfdf7b) | python/cdfdf7bb73a5751ecec7 | cdfdf7b | 1.069x ↑<br>[📄](results/bm-20261008-3.16.0a0-cdfdf7b/bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b-vs-3.12.6.md)[📈](results/bm-20261008-3.16.0a0-cdfdf7b/bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b-vs-3.12.6.svg) | 1.032x ↑<br>[📄](results/bm-20261008-3.16.0a0-cdfdf7b/bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b-vs-3.13.0rc2.md)[📈](results/bm-20261008-3.16.0a0-cdfdf7b/bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b-vs-3.13.0rc2.svg) |  |
| [2026-10-06](results/bm-20261006-3.16.0a0-1818fba-NOGIL) | python/1818fba7e737320b4241 | 1818fba (NOGIL) | 1.041x ↓<br>[📄](results/bm-20261006-3.16.0a0-1818fba-NOGIL/bm-20261006-vultr-x86_64-python-1818fba7e737320b4241-3.16.0a0-1818fba-vs-3.12.6.md)[📈](results/bm-20261006-3.16.0a0-1818fba-NOGIL/bm-20261006-vultr-x86_64-python-1818fba7e737320b4241-3.16.0a0-1818fba-vs-3.12.6.svg) | 1.074x ↓<br>[📄](results/bm-20261006-3.16.0a0-1818fba-NOGIL/bm-20261006-vultr-x86_64-python-1818fba7e737320b4241-3.16.0a0-1818fba-vs-3.13.0rc2.md)[📈](results/bm-20261006-3.16.0a0-1818fba-NOGIL/bm-20261006-vultr-x86_64-python-1818fba7e737320b4241-3.16.0a0-1818fba-vs-3.13.0rc2.svg) | 1.104x ↓<br>[📄](results/bm-20261006-3.16.0a0-1818fba-NOGIL/bm-20261006-vultr-x86_64-python-1818fba7e737320b4241-3.16.0a0-1818fba-vs-base.md)[📈](results/bm-20261006-3.16.0a0-1818fba-NOGIL/bm-20261006-vultr-x86_64-python-1818fba7e737320b4241-3.16.0a0-1818fba-vs-base.svg)[🧠](results/bm-20261006-3.16.0a0-1818fba-NOGIL/bm-20261006-vultr-x86_64-python-1818fba7e737320b4241-3.16.0a0-1818fba-vs-base-mem.svg) |
| [2026-10-06](results/bm-20261006-3.16.0a0-1818fba) | python/1818fba7e737320b4241 | 1818fba | 1.066x ↑<br>[📄](results/bm-20261006-3.16.0a0-1818fba/bm-20261006-vultr-x86_64-python-1818fba7e737320b4241-3.16.0a0-1818fba-vs-3.12.6.md)[📈](results/bm-20261006-3.16.0a0-1818fba/bm-20261006-vultr-x86_64-python-1818fba7e737320b4241-3.16.0a0-1818fba-vs-3.12.6.svg) | 1.029x ↑<br>[📄](results/bm-20261006-3.16.0a0-1818fba/bm-20261006-vultr-x86_64-python-1818fba7e737320b4241-3.16.0a0-1818fba-vs-3.13.0rc2.md)[📈](results/bm-20261006-3.16.0a0-1818fba/bm-20261006-vultr-x86_64-python-1818fba7e737320b4241-3.16.0a0-1818fba-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-10-09](results/bm-20261009-3.16.0a0-0ec3aee-NOGIL) | python/0ec3aee262b03276a18a | 0ec3aee (NOGIL) | 1.060x ↑<br>[📄](results/bm-20261009-3.16.0a0-0ec3aee-NOGIL/bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee-vs-3.12.6.md)[📈](results/bm-20261009-3.16.0a0-0ec3aee-NOGIL/bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee-vs-3.12.6.svg) | 1.019x ↓<br>[📄](results/bm-20261009-3.16.0a0-0ec3aee-NOGIL/bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee-vs-3.13.0rc2.md)[📈](results/bm-20261009-3.16.0a0-0ec3aee-NOGIL/bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee-vs-3.13.0rc2.svg) | 1.083x ↓<br>[📄](results/bm-20261009-3.16.0a0-0ec3aee-NOGIL/bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee-vs-base.md)[📈](results/bm-20261009-3.16.0a0-0ec3aee-NOGIL/bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee-vs-base.svg)[🧠](results/bm-20261009-3.16.0a0-0ec3aee-NOGIL/bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee-vs-base-mem.svg) |
| [2026-10-09](results/bm-20261009-3.16.0a0-0ec3aee) | python/0ec3aee262b03276a18a | 0ec3aee | 1.161x ↑<br>[📄](results/bm-20261009-3.16.0a0-0ec3aee/bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee-vs-3.12.6.md)[📈](results/bm-20261009-3.16.0a0-0ec3aee/bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee-vs-3.12.6.svg) | 1.072x ↑<br>[📄](results/bm-20261009-3.16.0a0-0ec3aee/bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee-vs-3.13.0rc2.md)[📈](results/bm-20261009-3.16.0a0-0ec3aee/bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee-vs-3.13.0rc2.svg) |  |
| [2026-10-08](results/bm-20261008-3.16.0a0-bc12b72-NOGIL) | python/bc12b7285f87f3ca9118 | bc12b72 (NOGIL) | 1.057x ↑<br>[📄](results/bm-20261008-3.16.0a0-bc12b72-NOGIL/bm-20261008-macm4pro-arm64-python-bc12b7285f87f3ca9118-3.16.0a0-bc12b72-vs-3.12.6.md)[📈](results/bm-20261008-3.16.0a0-bc12b72-NOGIL/bm-20261008-macm4pro-arm64-python-bc12b7285f87f3ca9118-3.16.0a0-bc12b72-vs-3.12.6.svg) | 1.021x ↓<br>[📄](results/bm-20261008-3.16.0a0-bc12b72-NOGIL/bm-20261008-macm4pro-arm64-python-bc12b7285f87f3ca9118-3.16.0a0-bc12b72-vs-3.13.0rc2.md)[📈](results/bm-20261008-3.16.0a0-bc12b72-NOGIL/bm-20261008-macm4pro-arm64-python-bc12b7285f87f3ca9118-3.16.0a0-bc12b72-vs-3.13.0rc2.svg) | 1.083x ↓<br>[📄](results/bm-20261008-3.16.0a0-bc12b72-NOGIL/bm-20261008-macm4pro-arm64-python-bc12b7285f87f3ca9118-3.16.0a0-bc12b72-vs-base.md)[📈](results/bm-20261008-3.16.0a0-bc12b72-NOGIL/bm-20261008-macm4pro-arm64-python-bc12b7285f87f3ca9118-3.16.0a0-bc12b72-vs-base.svg)[🧠](results/bm-20261008-3.16.0a0-bc12b72-NOGIL/bm-20261008-macm4pro-arm64-python-bc12b7285f87f3ca9118-3.16.0a0-bc12b72-vs-base-mem.svg) |
| [2026-10-08](results/bm-20261008-3.16.0a0-bc12b72) | python/bc12b7285f87f3ca9118 | bc12b72 | 1.158x ↑<br>[📄](results/bm-20261008-3.16.0a0-bc12b72/bm-20261008-macm4pro-arm64-python-bc12b7285f87f3ca9118-3.16.0a0-bc12b72-vs-3.12.6.md)[📈](results/bm-20261008-3.16.0a0-bc12b72/bm-20261008-macm4pro-arm64-python-bc12b7285f87f3ca9118-3.16.0a0-bc12b72-vs-3.12.6.svg) | 1.069x ↑<br>[📄](results/bm-20261008-3.16.0a0-bc12b72/bm-20261008-macm4pro-arm64-python-bc12b7285f87f3ca9118-3.16.0a0-bc12b72-vs-3.13.0rc2.md)[📈](results/bm-20261008-3.16.0a0-bc12b72/bm-20261008-macm4pro-arm64-python-bc12b7285f87f3ca9118-3.16.0a0-bc12b72-vs-3.13.0rc2.svg) |  |
| [2026-10-08](results/bm-20261008-3.16.0a0-cdfdf7b-NOGIL) | python/cdfdf7bb73a5751ecec7 | cdfdf7b (NOGIL) | 1.056x ↑<br>[📄](results/bm-20261008-3.16.0a0-cdfdf7b-NOGIL/bm-20261008-macm4pro-arm64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b-vs-3.12.6.md)[📈](results/bm-20261008-3.16.0a0-cdfdf7b-NOGIL/bm-20261008-macm4pro-arm64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b-vs-3.12.6.svg) | 1.022x ↓<br>[📄](results/bm-20261008-3.16.0a0-cdfdf7b-NOGIL/bm-20261008-macm4pro-arm64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b-vs-3.13.0rc2.md)[📈](results/bm-20261008-3.16.0a0-cdfdf7b-NOGIL/bm-20261008-macm4pro-arm64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b-vs-3.13.0rc2.svg) | 1.084x ↓<br>[📄](results/bm-20261008-3.16.0a0-cdfdf7b-NOGIL/bm-20261008-macm4pro-arm64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b-vs-base.md)[📈](results/bm-20261008-3.16.0a0-cdfdf7b-NOGIL/bm-20261008-macm4pro-arm64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b-vs-base.svg)[🧠](results/bm-20261008-3.16.0a0-cdfdf7b-NOGIL/bm-20261008-macm4pro-arm64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b-vs-base-mem.svg) |
| [2026-10-08](results/bm-20261008-3.16.0a0-cdfdf7b) | python/cdfdf7bb73a5751ecec7 | cdfdf7b | 1.157x ↑<br>[📄](results/bm-20261008-3.16.0a0-cdfdf7b/bm-20261008-macm4pro-arm64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b-vs-3.12.6.md)[📈](results/bm-20261008-3.16.0a0-cdfdf7b/bm-20261008-macm4pro-arm64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b-vs-3.12.6.svg) | 1.069x ↑<br>[📄](results/bm-20261008-3.16.0a0-cdfdf7b/bm-20261008-macm4pro-arm64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b-vs-3.13.0rc2.md)[📈](results/bm-20261008-3.16.0a0-cdfdf7b/bm-20261008-macm4pro-arm64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b-vs-3.13.0rc2.svg) |  |
| [2026-10-06](results/bm-20261006-3.16.0a0-1818fba-NOGIL) | python/1818fba7e737320b4241 | 1818fba (NOGIL) | 1.055x ↑<br>[📄](results/bm-20261006-3.16.0a0-1818fba-NOGIL/bm-20261006-macm4pro-arm64-python-1818fba7e737320b4241-3.16.0a0-1818fba-vs-3.12.6.md)[📈](results/bm-20261006-3.16.0a0-1818fba-NOGIL/bm-20261006-macm4pro-arm64-python-1818fba7e737320b4241-3.16.0a0-1818fba-vs-3.12.6.svg) | 1.023x ↓<br>[📄](results/bm-20261006-3.16.0a0-1818fba-NOGIL/bm-20261006-macm4pro-arm64-python-1818fba7e737320b4241-3.16.0a0-1818fba-vs-3.13.0rc2.md)[📈](results/bm-20261006-3.16.0a0-1818fba-NOGIL/bm-20261006-macm4pro-arm64-python-1818fba7e737320b4241-3.16.0a0-1818fba-vs-3.13.0rc2.svg) | 1.083x ↓<br>[📄](results/bm-20261006-3.16.0a0-1818fba-NOGIL/bm-20261006-macm4pro-arm64-python-1818fba7e737320b4241-3.16.0a0-1818fba-vs-base.md)[📈](results/bm-20261006-3.16.0a0-1818fba-NOGIL/bm-20261006-macm4pro-arm64-python-1818fba7e737320b4241-3.16.0a0-1818fba-vs-base.svg)[🧠](results/bm-20261006-3.16.0a0-1818fba-NOGIL/bm-20261006-macm4pro-arm64-python-1818fba7e737320b4241-3.16.0a0-1818fba-vs-base-mem.svg) |
| [2026-10-06](results/bm-20261006-3.16.0a0-1818fba) | python/1818fba7e737320b4241 | 1818fba | 1.155x ↑<br>[📄](results/bm-20261006-3.16.0a0-1818fba/bm-20261006-macm4pro-arm64-python-1818fba7e737320b4241-3.16.0a0-1818fba-vs-3.12.6.md)[📈](results/bm-20261006-3.16.0a0-1818fba/bm-20261006-macm4pro-arm64-python-1818fba7e737320b4241-3.16.0a0-1818fba-vs-3.12.6.svg) | 1.067x ↑<br>[📄](results/bm-20261006-3.16.0a0-1818fba/bm-20261006-macm4pro-arm64-python-1818fba7e737320b4241-3.16.0a0-1818fba-vs-3.13.0rc2.md)[📈](results/bm-20261006-3.16.0a0-1818fba/bm-20261006-macm4pro-arm64-python-1818fba7e737320b4241-3.16.0a0-1818fba-vs-3.13.0rc2.svg) |  |


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
