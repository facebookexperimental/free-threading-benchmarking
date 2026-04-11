# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (1f36a51)](results/bm-20260405-3.15.0a7%2B-1f36a51/bm-20260405-vultr-x86_64-python-1f36a510a2a16e8ff155-3.15.0a7%2B-1f36a51-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (1f36a51)](results/bm-20260405-3.15.0a7%2B-1f36a51-PYTHON_UOPS/bm-20260405-vultr-x86_64-python-1f36a510a2a16e8ff155-3.15.0a7%2B-1f36a51-pystats.md)
- [Most recent JIT pystats on main (bedaea0)](results/bm-20251019-3.15.0a1%2B-bedaea0-JIT/bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-04-10](results/bm-20260410-3.15.0a8%2B-dd88e77-NOGIL) | python/dd88e77fad887aaf00ea | dd88e77 (NOGIL) | 1.027x ↓<br>[📄](results/bm-20260410-3.15.0a8%2B-dd88e77-NOGIL/bm-20260410-vultr-x86_64-python-dd88e77fad887aaf00ea-3.15.0a8%2B-dd88e77-vs-3.12.6.md)[📈](results/bm-20260410-3.15.0a8%2B-dd88e77-NOGIL/bm-20260410-vultr-x86_64-python-dd88e77fad887aaf00ea-3.15.0a8%2B-dd88e77-vs-3.12.6.svg) | 1.059x ↓<br>[📄](results/bm-20260410-3.15.0a8%2B-dd88e77-NOGIL/bm-20260410-vultr-x86_64-python-dd88e77fad887aaf00ea-3.15.0a8%2B-dd88e77-vs-3.13.0rc2.md)[📈](results/bm-20260410-3.15.0a8%2B-dd88e77-NOGIL/bm-20260410-vultr-x86_64-python-dd88e77fad887aaf00ea-3.15.0a8%2B-dd88e77-vs-3.13.0rc2.svg) | 1.090x ↓<br>[📄](results/bm-20260410-3.15.0a8%2B-dd88e77-NOGIL/bm-20260410-vultr-x86_64-python-dd88e77fad887aaf00ea-3.15.0a8%2B-dd88e77-vs-base.md)[📈](results/bm-20260410-3.15.0a8%2B-dd88e77-NOGIL/bm-20260410-vultr-x86_64-python-dd88e77fad887aaf00ea-3.15.0a8%2B-dd88e77-vs-base.svg)[🧠](results/bm-20260410-3.15.0a8%2B-dd88e77-NOGIL/bm-20260410-vultr-x86_64-python-dd88e77fad887aaf00ea-3.15.0a8%2B-dd88e77-vs-base-mem.svg) |
| [2026-04-10](results/bm-20260410-3.15.0a8%2B-dd88e77) | python/dd88e77fad887aaf00ea | dd88e77 | 1.063x ↑<br>[📄](results/bm-20260410-3.15.0a8%2B-dd88e77/bm-20260410-vultr-x86_64-python-dd88e77fad887aaf00ea-3.15.0a8%2B-dd88e77-vs-3.12.6.md)[📈](results/bm-20260410-3.15.0a8%2B-dd88e77/bm-20260410-vultr-x86_64-python-dd88e77fad887aaf00ea-3.15.0a8%2B-dd88e77-vs-3.12.6.svg) | 1.028x ↑<br>[📄](results/bm-20260410-3.15.0a8%2B-dd88e77/bm-20260410-vultr-x86_64-python-dd88e77fad887aaf00ea-3.15.0a8%2B-dd88e77-vs-3.13.0rc2.md)[📈](results/bm-20260410-3.15.0a8%2B-dd88e77/bm-20260410-vultr-x86_64-python-dd88e77fad887aaf00ea-3.15.0a8%2B-dd88e77-vs-3.13.0rc2.svg) |  |
| [2026-04-09](results/bm-20260409-3.15.0a8%2B-1a0edb1-NOGIL) | python/1a0edb1fa899c067f19b | 1a0edb1 (NOGIL) | 1.026x ↓<br>[📄](results/bm-20260409-3.15.0a8%2B-1a0edb1-NOGIL/bm-20260409-vultr-x86_64-python-1a0edb1fa899c067f19b-3.15.0a8%2B-1a0edb1-vs-3.12.6.md)[📈](results/bm-20260409-3.15.0a8%2B-1a0edb1-NOGIL/bm-20260409-vultr-x86_64-python-1a0edb1fa899c067f19b-3.15.0a8%2B-1a0edb1-vs-3.12.6.svg) | 1.059x ↓<br>[📄](results/bm-20260409-3.15.0a8%2B-1a0edb1-NOGIL/bm-20260409-vultr-x86_64-python-1a0edb1fa899c067f19b-3.15.0a8%2B-1a0edb1-vs-3.13.0rc2.md)[📈](results/bm-20260409-3.15.0a8%2B-1a0edb1-NOGIL/bm-20260409-vultr-x86_64-python-1a0edb1fa899c067f19b-3.15.0a8%2B-1a0edb1-vs-3.13.0rc2.svg) | 1.092x ↓<br>[📄](results/bm-20260409-3.15.0a8%2B-1a0edb1-NOGIL/bm-20260409-vultr-x86_64-python-1a0edb1fa899c067f19b-3.15.0a8%2B-1a0edb1-vs-base.md)[📈](results/bm-20260409-3.15.0a8%2B-1a0edb1-NOGIL/bm-20260409-vultr-x86_64-python-1a0edb1fa899c067f19b-3.15.0a8%2B-1a0edb1-vs-base.svg)[🧠](results/bm-20260409-3.15.0a8%2B-1a0edb1-NOGIL/bm-20260409-vultr-x86_64-python-1a0edb1fa899c067f19b-3.15.0a8%2B-1a0edb1-vs-base-mem.svg) |
| [2026-04-09](results/bm-20260409-3.15.0a8%2B-1a0edb1) | python/1a0edb1fa899c067f19b | 1a0edb1 | 1.069x ↑<br>[📄](results/bm-20260409-3.15.0a8%2B-1a0edb1/bm-20260409-vultr-x86_64-python-1a0edb1fa899c067f19b-3.15.0a8%2B-1a0edb1-vs-3.12.6.md)[📈](results/bm-20260409-3.15.0a8%2B-1a0edb1/bm-20260409-vultr-x86_64-python-1a0edb1fa899c067f19b-3.15.0a8%2B-1a0edb1-vs-3.12.6.svg) | 1.033x ↑<br>[📄](results/bm-20260409-3.15.0a8%2B-1a0edb1/bm-20260409-vultr-x86_64-python-1a0edb1fa899c067f19b-3.15.0a8%2B-1a0edb1-vs-3.13.0rc2.md)[📈](results/bm-20260409-3.15.0a8%2B-1a0edb1/bm-20260409-vultr-x86_64-python-1a0edb1fa899c067f19b-3.15.0a8%2B-1a0edb1-vs-3.13.0rc2.svg) |  |
| [2026-04-08](results/bm-20260408-3.15.0a8%2B-efde433-NOGIL) | python/efde4333bfcdd1e24c2a | efde433 (NOGIL) | 1.024x ↓<br>[📄](results/bm-20260408-3.15.0a8%2B-efde433-NOGIL/bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8%2B-efde433-vs-3.12.6.md)[📈](results/bm-20260408-3.15.0a8%2B-efde433-NOGIL/bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8%2B-efde433-vs-3.12.6.svg) | 1.057x ↓<br>[📄](results/bm-20260408-3.15.0a8%2B-efde433-NOGIL/bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8%2B-efde433-vs-3.13.0rc2.md)[📈](results/bm-20260408-3.15.0a8%2B-efde433-NOGIL/bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8%2B-efde433-vs-3.13.0rc2.svg) | 1.090x ↓<br>[📄](results/bm-20260408-3.15.0a8%2B-efde433-NOGIL/bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8%2B-efde433-vs-base.md)[📈](results/bm-20260408-3.15.0a8%2B-efde433-NOGIL/bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8%2B-efde433-vs-base.svg)[🧠](results/bm-20260408-3.15.0a8%2B-efde433-NOGIL/bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8%2B-efde433-vs-base-mem.svg) |
| [2026-04-08](results/bm-20260408-3.15.0a8%2B-efde433) | python/efde4333bfcdd1e24c2a | efde433 | 1.067x ↑<br>[📄](results/bm-20260408-3.15.0a8%2B-efde433/bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8%2B-efde433-vs-3.12.6.md)[📈](results/bm-20260408-3.15.0a8%2B-efde433/bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8%2B-efde433-vs-3.12.6.svg) | 1.032x ↑<br>[📄](results/bm-20260408-3.15.0a8%2B-efde433/bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8%2B-efde433-vs-3.13.0rc2.md)[📈](results/bm-20260408-3.15.0a8%2B-efde433/bm-20260408-vultr-x86_64-python-efde4333bfcdd1e24c2a-3.15.0a8%2B-efde433-vs-3.13.0rc2.svg) |  |
| [2026-04-07](results/bm-20260407-3.15.0a8%2B-0b20bff-NOGIL) | python/0b20bff386141ee0e8c6 | 0b20bff (NOGIL) | 1.021x ↓<br>[📄](results/bm-20260407-3.15.0a8%2B-0b20bff-NOGIL/bm-20260407-vultr-x86_64-python-0b20bff386141ee0e8c6-3.15.0a8%2B-0b20bff-vs-3.12.6.md)[📈](results/bm-20260407-3.15.0a8%2B-0b20bff-NOGIL/bm-20260407-vultr-x86_64-python-0b20bff386141ee0e8c6-3.15.0a8%2B-0b20bff-vs-3.12.6.svg) | 1.054x ↓<br>[📄](results/bm-20260407-3.15.0a8%2B-0b20bff-NOGIL/bm-20260407-vultr-x86_64-python-0b20bff386141ee0e8c6-3.15.0a8%2B-0b20bff-vs-3.13.0rc2.md)[📈](results/bm-20260407-3.15.0a8%2B-0b20bff-NOGIL/bm-20260407-vultr-x86_64-python-0b20bff386141ee0e8c6-3.15.0a8%2B-0b20bff-vs-3.13.0rc2.svg) | 1.087x ↓<br>[📄](results/bm-20260407-3.15.0a8%2B-0b20bff-NOGIL/bm-20260407-vultr-x86_64-python-0b20bff386141ee0e8c6-3.15.0a8%2B-0b20bff-vs-base.md)[📈](results/bm-20260407-3.15.0a8%2B-0b20bff-NOGIL/bm-20260407-vultr-x86_64-python-0b20bff386141ee0e8c6-3.15.0a8%2B-0b20bff-vs-base.svg)[🧠](results/bm-20260407-3.15.0a8%2B-0b20bff-NOGIL/bm-20260407-vultr-x86_64-python-0b20bff386141ee0e8c6-3.15.0a8%2B-0b20bff-vs-base-mem.svg) |
| [2026-04-07](results/bm-20260407-3.15.0a8%2B-0b20bff) | python/0b20bff386141ee0e8c6 | 0b20bff | 1.066x ↑<br>[📄](results/bm-20260407-3.15.0a8%2B-0b20bff/bm-20260407-vultr-x86_64-python-0b20bff386141ee0e8c6-3.15.0a8%2B-0b20bff-vs-3.12.6.md)[📈](results/bm-20260407-3.15.0a8%2B-0b20bff/bm-20260407-vultr-x86_64-python-0b20bff386141ee0e8c6-3.15.0a8%2B-0b20bff-vs-3.12.6.svg) | 1.031x ↑<br>[📄](results/bm-20260407-3.15.0a8%2B-0b20bff/bm-20260407-vultr-x86_64-python-0b20bff386141ee0e8c6-3.15.0a8%2B-0b20bff-vs-3.13.0rc2.md)[📈](results/bm-20260407-3.15.0a8%2B-0b20bff/bm-20260407-vultr-x86_64-python-0b20bff386141ee0e8c6-3.15.0a8%2B-0b20bff-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-04-10](results/bm-20260410-3.15.0a8%2B-dd88e77-NOGIL) | python/dd88e77fad887aaf00ea | dd88e77 (NOGIL) | 1.106x ↑<br>[📄](results/bm-20260410-3.15.0a8%2B-dd88e77-NOGIL/bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8%2B-dd88e77-vs-3.12.6.md)[📈](results/bm-20260410-3.15.0a8%2B-dd88e77-NOGIL/bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8%2B-dd88e77-vs-3.12.6.svg) | 1.026x ↑<br>[📄](results/bm-20260410-3.15.0a8%2B-dd88e77-NOGIL/bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8%2B-dd88e77-vs-3.13.0rc2.md)[📈](results/bm-20260410-3.15.0a8%2B-dd88e77-NOGIL/bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8%2B-dd88e77-vs-3.13.0rc2.svg) | 1.063x ↓<br>[📄](results/bm-20260410-3.15.0a8%2B-dd88e77-NOGIL/bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8%2B-dd88e77-vs-base.md)[📈](results/bm-20260410-3.15.0a8%2B-dd88e77-NOGIL/bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8%2B-dd88e77-vs-base.svg)[🧠](results/bm-20260410-3.15.0a8%2B-dd88e77-NOGIL/bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8%2B-dd88e77-vs-base-mem.svg) |
| [2026-04-10](results/bm-20260410-3.15.0a8%2B-dd88e77) | python/dd88e77fad887aaf00ea | dd88e77 | 1.181x ↑<br>[📄](results/bm-20260410-3.15.0a8%2B-dd88e77/bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8%2B-dd88e77-vs-3.12.6.md)[📈](results/bm-20260410-3.15.0a8%2B-dd88e77/bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8%2B-dd88e77-vs-3.12.6.svg) | 1.095x ↑<br>[📄](results/bm-20260410-3.15.0a8%2B-dd88e77/bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8%2B-dd88e77-vs-3.13.0rc2.md)[📈](results/bm-20260410-3.15.0a8%2B-dd88e77/bm-20260410-macm4pro-arm64-python-dd88e77fad887aaf00ea-3.15.0a8%2B-dd88e77-vs-3.13.0rc2.svg) |  |
| [2026-04-09](results/bm-20260409-3.15.0a8%2B-1a0edb1-NOGIL) | python/1a0edb1fa899c067f19b | 1a0edb1 (NOGIL) | 1.102x ↑<br>[📄](results/bm-20260409-3.15.0a8%2B-1a0edb1-NOGIL/bm-20260409-macm4pro-arm64-python-1a0edb1fa899c067f19b-3.15.0a8%2B-1a0edb1-vs-3.12.6.md)[📈](results/bm-20260409-3.15.0a8%2B-1a0edb1-NOGIL/bm-20260409-macm4pro-arm64-python-1a0edb1fa899c067f19b-3.15.0a8%2B-1a0edb1-vs-3.12.6.svg) | 1.022x ↑<br>[📄](results/bm-20260409-3.15.0a8%2B-1a0edb1-NOGIL/bm-20260409-macm4pro-arm64-python-1a0edb1fa899c067f19b-3.15.0a8%2B-1a0edb1-vs-3.13.0rc2.md)[📈](results/bm-20260409-3.15.0a8%2B-1a0edb1-NOGIL/bm-20260409-macm4pro-arm64-python-1a0edb1fa899c067f19b-3.15.0a8%2B-1a0edb1-vs-3.13.0rc2.svg) | 1.055x ↓<br>[📄](results/bm-20260409-3.15.0a8%2B-1a0edb1-NOGIL/bm-20260409-macm4pro-arm64-python-1a0edb1fa899c067f19b-3.15.0a8%2B-1a0edb1-vs-base.md)[📈](results/bm-20260409-3.15.0a8%2B-1a0edb1-NOGIL/bm-20260409-macm4pro-arm64-python-1a0edb1fa899c067f19b-3.15.0a8%2B-1a0edb1-vs-base.svg)[🧠](results/bm-20260409-3.15.0a8%2B-1a0edb1-NOGIL/bm-20260409-macm4pro-arm64-python-1a0edb1fa899c067f19b-3.15.0a8%2B-1a0edb1-vs-base-mem.svg) |
| [2026-04-09](results/bm-20260409-3.15.0a8%2B-1a0edb1) | python/1a0edb1fa899c067f19b | 1a0edb1 | 1.166x ↑<br>[📄](results/bm-20260409-3.15.0a8%2B-1a0edb1/bm-20260409-macm4pro-arm64-python-1a0edb1fa899c067f19b-3.15.0a8%2B-1a0edb1-vs-3.12.6.md)[📈](results/bm-20260409-3.15.0a8%2B-1a0edb1/bm-20260409-macm4pro-arm64-python-1a0edb1fa899c067f19b-3.15.0a8%2B-1a0edb1-vs-3.12.6.svg) | 1.082x ↑<br>[📄](results/bm-20260409-3.15.0a8%2B-1a0edb1/bm-20260409-macm4pro-arm64-python-1a0edb1fa899c067f19b-3.15.0a8%2B-1a0edb1-vs-3.13.0rc2.md)[📈](results/bm-20260409-3.15.0a8%2B-1a0edb1/bm-20260409-macm4pro-arm64-python-1a0edb1fa899c067f19b-3.15.0a8%2B-1a0edb1-vs-3.13.0rc2.svg) |  |
| [2026-04-08](results/bm-20260408-3.15.0a8%2B-efde433-NOGIL) | python/efde4333bfcdd1e24c2a | efde433 (NOGIL) | 1.104x ↑<br>[📄](results/bm-20260408-3.15.0a8%2B-efde433-NOGIL/bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8%2B-efde433-vs-3.12.6.md)[📈](results/bm-20260408-3.15.0a8%2B-efde433-NOGIL/bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8%2B-efde433-vs-3.12.6.svg) | 1.024x ↑<br>[📄](results/bm-20260408-3.15.0a8%2B-efde433-NOGIL/bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8%2B-efde433-vs-3.13.0rc2.md)[📈](results/bm-20260408-3.15.0a8%2B-efde433-NOGIL/bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8%2B-efde433-vs-3.13.0rc2.svg) | 1.052x ↓<br>[📄](results/bm-20260408-3.15.0a8%2B-efde433-NOGIL/bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8%2B-efde433-vs-base.md)[📈](results/bm-20260408-3.15.0a8%2B-efde433-NOGIL/bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8%2B-efde433-vs-base.svg)[🧠](results/bm-20260408-3.15.0a8%2B-efde433-NOGIL/bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8%2B-efde433-vs-base-mem.svg) |
| [2026-04-08](results/bm-20260408-3.15.0a8%2B-efde433) | python/efde4333bfcdd1e24c2a | efde433 | 1.164x ↑<br>[📄](results/bm-20260408-3.15.0a8%2B-efde433/bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8%2B-efde433-vs-3.12.6.md)[📈](results/bm-20260408-3.15.0a8%2B-efde433/bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8%2B-efde433-vs-3.12.6.svg) | 1.080x ↑<br>[📄](results/bm-20260408-3.15.0a8%2B-efde433/bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8%2B-efde433-vs-3.13.0rc2.md)[📈](results/bm-20260408-3.15.0a8%2B-efde433/bm-20260408-macm4pro-arm64-python-efde4333bfcdd1e24c2a-3.15.0a8%2B-efde433-vs-3.13.0rc2.svg) |  |
| [2026-04-07](results/bm-20260407-3.15.0a8%2B-0b20bff-NOGIL) | python/0b20bff386141ee0e8c6 | 0b20bff (NOGIL) | 1.099x ↑<br>[📄](results/bm-20260407-3.15.0a8%2B-0b20bff-NOGIL/bm-20260407-macm4pro-arm64-python-0b20bff386141ee0e8c6-3.15.0a8%2B-0b20bff-vs-3.12.6.md)[📈](results/bm-20260407-3.15.0a8%2B-0b20bff-NOGIL/bm-20260407-macm4pro-arm64-python-0b20bff386141ee0e8c6-3.15.0a8%2B-0b20bff-vs-3.12.6.svg) | 1.019x ↑<br>[📄](results/bm-20260407-3.15.0a8%2B-0b20bff-NOGIL/bm-20260407-macm4pro-arm64-python-0b20bff386141ee0e8c6-3.15.0a8%2B-0b20bff-vs-3.13.0rc2.md)[📈](results/bm-20260407-3.15.0a8%2B-0b20bff-NOGIL/bm-20260407-macm4pro-arm64-python-0b20bff386141ee0e8c6-3.15.0a8%2B-0b20bff-vs-3.13.0rc2.svg) | 1.063x ↓<br>[📄](results/bm-20260407-3.15.0a8%2B-0b20bff-NOGIL/bm-20260407-macm4pro-arm64-python-0b20bff386141ee0e8c6-3.15.0a8%2B-0b20bff-vs-base.md)[📈](results/bm-20260407-3.15.0a8%2B-0b20bff-NOGIL/bm-20260407-macm4pro-arm64-python-0b20bff386141ee0e8c6-3.15.0a8%2B-0b20bff-vs-base.svg)[🧠](results/bm-20260407-3.15.0a8%2B-0b20bff-NOGIL/bm-20260407-macm4pro-arm64-python-0b20bff386141ee0e8c6-3.15.0a8%2B-0b20bff-vs-base-mem.svg) |
| [2026-04-07](results/bm-20260407-3.15.0a8%2B-0b20bff) | python/0b20bff386141ee0e8c6 | 0b20bff | 1.172x ↑<br>[📄](results/bm-20260407-3.15.0a8%2B-0b20bff/bm-20260407-macm4pro-arm64-python-0b20bff386141ee0e8c6-3.15.0a8%2B-0b20bff-vs-3.12.6.md)[📈](results/bm-20260407-3.15.0a8%2B-0b20bff/bm-20260407-macm4pro-arm64-python-0b20bff386141ee0e8c6-3.15.0a8%2B-0b20bff-vs-3.12.6.svg) | 1.087x ↑<br>[📄](results/bm-20260407-3.15.0a8%2B-0b20bff/bm-20260407-macm4pro-arm64-python-0b20bff386141ee0e8c6-3.15.0a8%2B-0b20bff-vs-3.13.0rc2.md)[📈](results/bm-20260407-3.15.0a8%2B-0b20bff/bm-20260407-macm4pro-arm64-python-0b20bff386141ee0e8c6-3.15.0a8%2B-0b20bff-vs-3.13.0rc2.svg) |  |


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
