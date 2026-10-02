# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (1e8ff18)](results/bm-20260926-3.16.0a0-1e8ff18/bm-20260926-vultr-x86_64-python-1e8ff18a1215b711136b-3.16.0a0-1e8ff18-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (1e8ff18)](results/bm-20260926-3.16.0a0-1e8ff18-PYTHON_UOPS/bm-20260926-vultr-x86_64-python-1e8ff18a1215b711136b-3.16.0a0-1e8ff18-pystats.md)
- [Most recent JIT pystats on main (bedaea0)](results/bm-20251019-3.15.0a1%2B-bedaea0-JIT/bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-10-01](results/bm-20261001-3.16.0a0-a4f28a5-NOGIL) | python/a4f28a52b4b54c34100e | a4f28a5 (NOGIL) | 1.043x ↓<br>[📄](results/bm-20261001-3.16.0a0-a4f28a5-NOGIL/bm-20261001-vultr-x86_64-python-a4f28a52b4b54c34100e-3.16.0a0-a4f28a5-vs-3.12.6.md)[📈](results/bm-20261001-3.16.0a0-a4f28a5-NOGIL/bm-20261001-vultr-x86_64-python-a4f28a52b4b54c34100e-3.16.0a0-a4f28a5-vs-3.12.6.svg) | 1.076x ↓<br>[📄](results/bm-20261001-3.16.0a0-a4f28a5-NOGIL/bm-20261001-vultr-x86_64-python-a4f28a52b4b54c34100e-3.16.0a0-a4f28a5-vs-3.13.0rc2.md)[📈](results/bm-20261001-3.16.0a0-a4f28a5-NOGIL/bm-20261001-vultr-x86_64-python-a4f28a52b4b54c34100e-3.16.0a0-a4f28a5-vs-3.13.0rc2.svg) | 1.104x ↓<br>[📄](results/bm-20261001-3.16.0a0-a4f28a5-NOGIL/bm-20261001-vultr-x86_64-python-a4f28a52b4b54c34100e-3.16.0a0-a4f28a5-vs-base.md)[📈](results/bm-20261001-3.16.0a0-a4f28a5-NOGIL/bm-20261001-vultr-x86_64-python-a4f28a52b4b54c34100e-3.16.0a0-a4f28a5-vs-base.svg)[🧠](results/bm-20261001-3.16.0a0-a4f28a5-NOGIL/bm-20261001-vultr-x86_64-python-a4f28a52b4b54c34100e-3.16.0a0-a4f28a5-vs-base-mem.svg) |
| [2026-10-01](results/bm-20261001-3.16.0a0-a4f28a5) | python/a4f28a52b4b54c34100e | a4f28a5 | 1.064x ↑<br>[📄](results/bm-20261001-3.16.0a0-a4f28a5/bm-20261001-vultr-x86_64-python-a4f28a52b4b54c34100e-3.16.0a0-a4f28a5-vs-3.12.6.md)[📈](results/bm-20261001-3.16.0a0-a4f28a5/bm-20261001-vultr-x86_64-python-a4f28a52b4b54c34100e-3.16.0a0-a4f28a5-vs-3.12.6.svg) | 1.028x ↑<br>[📄](results/bm-20261001-3.16.0a0-a4f28a5/bm-20261001-vultr-x86_64-python-a4f28a52b4b54c34100e-3.16.0a0-a4f28a5-vs-3.13.0rc2.md)[📈](results/bm-20261001-3.16.0a0-a4f28a5/bm-20261001-vultr-x86_64-python-a4f28a52b4b54c34100e-3.16.0a0-a4f28a5-vs-3.13.0rc2.svg) |  |
| [2026-10-01](results/bm-20261001-3.16.0a0-763b6ed-NOGIL) | python/763b6edb0ec959bdfb78 | 763b6ed (NOGIL) | 1.045x ↓<br>[📄](results/bm-20261001-3.16.0a0-763b6ed-NOGIL/bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed-vs-3.12.6.md)[📈](results/bm-20261001-3.16.0a0-763b6ed-NOGIL/bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed-vs-3.12.6.svg) | 1.078x ↓<br>[📄](results/bm-20261001-3.16.0a0-763b6ed-NOGIL/bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed-vs-3.13.0rc2.md)[📈](results/bm-20261001-3.16.0a0-763b6ed-NOGIL/bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed-vs-3.13.0rc2.svg) | 1.108x ↓<br>[📄](results/bm-20261001-3.16.0a0-763b6ed-NOGIL/bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed-vs-base.md)[📈](results/bm-20261001-3.16.0a0-763b6ed-NOGIL/bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed-vs-base.svg)[🧠](results/bm-20261001-3.16.0a0-763b6ed-NOGIL/bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed-vs-base-mem.svg) |
| [2026-10-01](results/bm-20261001-3.16.0a0-763b6ed) | python/763b6edb0ec959bdfb78 | 763b6ed | 1.066x ↑<br>[📄](results/bm-20261001-3.16.0a0-763b6ed/bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed-vs-3.12.6.md)[📈](results/bm-20261001-3.16.0a0-763b6ed/bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed-vs-3.12.6.svg) | 1.030x ↑<br>[📄](results/bm-20261001-3.16.0a0-763b6ed/bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed-vs-3.13.0rc2.md)[📈](results/bm-20261001-3.16.0a0-763b6ed/bm-20261001-vultr-x86_64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed-vs-3.13.0rc2.svg) |  |
| [2026-09-29](results/bm-20260929-3.16.0a0-540274c-NOGIL) | python/540274c649e29a88f56c | 540274c (NOGIL) | 1.053x ↓<br>[📄](results/bm-20260929-3.16.0a0-540274c-NOGIL/bm-20260929-vultr-x86_64-python-540274c649e29a88f56c-3.16.0a0-540274c-vs-3.12.6.md)[📈](results/bm-20260929-3.16.0a0-540274c-NOGIL/bm-20260929-vultr-x86_64-python-540274c649e29a88f56c-3.16.0a0-540274c-vs-3.12.6.svg) | 1.086x ↓<br>[📄](results/bm-20260929-3.16.0a0-540274c-NOGIL/bm-20260929-vultr-x86_64-python-540274c649e29a88f56c-3.16.0a0-540274c-vs-3.13.0rc2.md)[📈](results/bm-20260929-3.16.0a0-540274c-NOGIL/bm-20260929-vultr-x86_64-python-540274c649e29a88f56c-3.16.0a0-540274c-vs-3.13.0rc2.svg) | 1.113x ↓<br>[📄](results/bm-20260929-3.16.0a0-540274c-NOGIL/bm-20260929-vultr-x86_64-python-540274c649e29a88f56c-3.16.0a0-540274c-vs-base.md)[📈](results/bm-20260929-3.16.0a0-540274c-NOGIL/bm-20260929-vultr-x86_64-python-540274c649e29a88f56c-3.16.0a0-540274c-vs-base.svg)[🧠](results/bm-20260929-3.16.0a0-540274c-NOGIL/bm-20260929-vultr-x86_64-python-540274c649e29a88f56c-3.16.0a0-540274c-vs-base-mem.svg) |
| [2026-09-29](results/bm-20260929-3.16.0a0-540274c) | python/540274c649e29a88f56c | 540274c | 1.064x ↑<br>[📄](results/bm-20260929-3.16.0a0-540274c/bm-20260929-vultr-x86_64-python-540274c649e29a88f56c-3.16.0a0-540274c-vs-3.12.6.md)[📈](results/bm-20260929-3.16.0a0-540274c/bm-20260929-vultr-x86_64-python-540274c649e29a88f56c-3.16.0a0-540274c-vs-3.12.6.svg) | 1.028x ↑<br>[📄](results/bm-20260929-3.16.0a0-540274c/bm-20260929-vultr-x86_64-python-540274c649e29a88f56c-3.16.0a0-540274c-vs-3.13.0rc2.md)[📈](results/bm-20260929-3.16.0a0-540274c/bm-20260929-vultr-x86_64-python-540274c649e29a88f56c-3.16.0a0-540274c-vs-3.13.0rc2.svg) |  |
| [2026-09-28](results/bm-20260928-3.16.0a0-3330712-NOGIL) | python/333071231d3a46cccc32 | 3330712 (NOGIL) | 1.046x ↓<br>[📄](results/bm-20260928-3.16.0a0-3330712-NOGIL/bm-20260928-vultr-x86_64-python-333071231d3a46cccc32-3.16.0a0-3330712-vs-3.12.6.md)[📈](results/bm-20260928-3.16.0a0-3330712-NOGIL/bm-20260928-vultr-x86_64-python-333071231d3a46cccc32-3.16.0a0-3330712-vs-3.12.6.svg) | 1.079x ↓<br>[📄](results/bm-20260928-3.16.0a0-3330712-NOGIL/bm-20260928-vultr-x86_64-python-333071231d3a46cccc32-3.16.0a0-3330712-vs-3.13.0rc2.md)[📈](results/bm-20260928-3.16.0a0-3330712-NOGIL/bm-20260928-vultr-x86_64-python-333071231d3a46cccc32-3.16.0a0-3330712-vs-3.13.0rc2.svg) | 1.107x ↓<br>[📄](results/bm-20260928-3.16.0a0-3330712-NOGIL/bm-20260928-vultr-x86_64-python-333071231d3a46cccc32-3.16.0a0-3330712-vs-base.md)[📈](results/bm-20260928-3.16.0a0-3330712-NOGIL/bm-20260928-vultr-x86_64-python-333071231d3a46cccc32-3.16.0a0-3330712-vs-base.svg)[🧠](results/bm-20260928-3.16.0a0-3330712-NOGIL/bm-20260928-vultr-x86_64-python-333071231d3a46cccc32-3.16.0a0-3330712-vs-base-mem.svg) |
| [2026-09-28](results/bm-20260928-3.16.0a0-3330712) | python/333071231d3a46cccc32 | 3330712 | 1.064x ↑<br>[📄](results/bm-20260928-3.16.0a0-3330712/bm-20260928-vultr-x86_64-python-333071231d3a46cccc32-3.16.0a0-3330712-vs-3.12.6.md)[📈](results/bm-20260928-3.16.0a0-3330712/bm-20260928-vultr-x86_64-python-333071231d3a46cccc32-3.16.0a0-3330712-vs-3.12.6.svg) | 1.027x ↑<br>[📄](results/bm-20260928-3.16.0a0-3330712/bm-20260928-vultr-x86_64-python-333071231d3a46cccc32-3.16.0a0-3330712-vs-3.13.0rc2.md)[📈](results/bm-20260928-3.16.0a0-3330712/bm-20260928-vultr-x86_64-python-333071231d3a46cccc32-3.16.0a0-3330712-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-10-01](results/bm-20261001-3.16.0a0-a4f28a5-NOGIL) | python/a4f28a52b4b54c34100e | a4f28a5 (NOGIL) | 1.053x ↑<br>[📄](results/bm-20261001-3.16.0a0-a4f28a5-NOGIL/bm-20261001-macm4pro-arm64-python-a4f28a52b4b54c34100e-3.16.0a0-a4f28a5-vs-3.12.6.md)[📈](results/bm-20261001-3.16.0a0-a4f28a5-NOGIL/bm-20261001-macm4pro-arm64-python-a4f28a52b4b54c34100e-3.16.0a0-a4f28a5-vs-3.12.6.svg) | 1.025x ↓<br>[📄](results/bm-20261001-3.16.0a0-a4f28a5-NOGIL/bm-20261001-macm4pro-arm64-python-a4f28a52b4b54c34100e-3.16.0a0-a4f28a5-vs-3.13.0rc2.md)[📈](results/bm-20261001-3.16.0a0-a4f28a5-NOGIL/bm-20261001-macm4pro-arm64-python-a4f28a52b4b54c34100e-3.16.0a0-a4f28a5-vs-3.13.0rc2.svg) | 1.077x ↓<br>[📄](results/bm-20261001-3.16.0a0-a4f28a5-NOGIL/bm-20261001-macm4pro-arm64-python-a4f28a52b4b54c34100e-3.16.0a0-a4f28a5-vs-base.md)[📈](results/bm-20261001-3.16.0a0-a4f28a5-NOGIL/bm-20261001-macm4pro-arm64-python-a4f28a52b4b54c34100e-3.16.0a0-a4f28a5-vs-base.svg)[🧠](results/bm-20261001-3.16.0a0-a4f28a5-NOGIL/bm-20261001-macm4pro-arm64-python-a4f28a52b4b54c34100e-3.16.0a0-a4f28a5-vs-base-mem.svg) |
| [2026-10-01](results/bm-20261001-3.16.0a0-a4f28a5) | python/a4f28a52b4b54c34100e | a4f28a5 | 1.145x ↑<br>[📄](results/bm-20261001-3.16.0a0-a4f28a5/bm-20261001-macm4pro-arm64-python-a4f28a52b4b54c34100e-3.16.0a0-a4f28a5-vs-3.12.6.md)[📈](results/bm-20261001-3.16.0a0-a4f28a5/bm-20261001-macm4pro-arm64-python-a4f28a52b4b54c34100e-3.16.0a0-a4f28a5-vs-3.12.6.svg) | 1.058x ↑<br>[📄](results/bm-20261001-3.16.0a0-a4f28a5/bm-20261001-macm4pro-arm64-python-a4f28a52b4b54c34100e-3.16.0a0-a4f28a5-vs-3.13.0rc2.md)[📈](results/bm-20261001-3.16.0a0-a4f28a5/bm-20261001-macm4pro-arm64-python-a4f28a52b4b54c34100e-3.16.0a0-a4f28a5-vs-3.13.0rc2.svg) |  |
| [2026-10-01](results/bm-20261001-3.16.0a0-763b6ed-NOGIL) | python/763b6edb0ec959bdfb78 | 763b6ed (NOGIL) | 1.079x ↑<br>[📄](results/bm-20261001-3.16.0a0-763b6ed-NOGIL/bm-20261001-macm4pro-arm64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed-vs-3.12.6.md)[📈](results/bm-20261001-3.16.0a0-763b6ed-NOGIL/bm-20261001-macm4pro-arm64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed-vs-3.12.6.svg) | 1.001x ↓<br>[📄](results/bm-20261001-3.16.0a0-763b6ed-NOGIL/bm-20261001-macm4pro-arm64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed-vs-3.13.0rc2.md)[📈](results/bm-20261001-3.16.0a0-763b6ed-NOGIL/bm-20261001-macm4pro-arm64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed-vs-3.13.0rc2.svg) | 1.043x ↓<br>[📄](results/bm-20261001-3.16.0a0-763b6ed-NOGIL/bm-20261001-macm4pro-arm64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed-vs-base.md)[📈](results/bm-20261001-3.16.0a0-763b6ed-NOGIL/bm-20261001-macm4pro-arm64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed-vs-base.svg)[🧠](results/bm-20261001-3.16.0a0-763b6ed-NOGIL/bm-20261001-macm4pro-arm64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed-vs-base-mem.svg) |
| [2026-10-01](results/bm-20261001-3.16.0a0-763b6ed) | python/763b6edb0ec959bdfb78 | 763b6ed | 1.132x ↑<br>[📄](results/bm-20261001-3.16.0a0-763b6ed/bm-20261001-macm4pro-arm64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed-vs-3.12.6.md)[📈](results/bm-20261001-3.16.0a0-763b6ed/bm-20261001-macm4pro-arm64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed-vs-3.12.6.svg) | 1.046x ↑<br>[📄](results/bm-20261001-3.16.0a0-763b6ed/bm-20261001-macm4pro-arm64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed-vs-3.13.0rc2.md)[📈](results/bm-20261001-3.16.0a0-763b6ed/bm-20261001-macm4pro-arm64-python-763b6edb0ec959bdfb78-3.16.0a0-763b6ed-vs-3.13.0rc2.svg) |  |
| [2026-09-29](results/bm-20260929-3.16.0a0-540274c-NOGIL) | python/540274c649e29a88f56c | 540274c (NOGIL) | 1.005x ↓<br>[📄](results/bm-20260929-3.16.0a0-540274c-NOGIL/bm-20260929-macm4pro-arm64-python-540274c649e29a88f56c-3.16.0a0-540274c-vs-3.12.6.md)[📈](results/bm-20260929-3.16.0a0-540274c-NOGIL/bm-20260929-macm4pro-arm64-python-540274c649e29a88f56c-3.16.0a0-540274c-vs-3.12.6.svg) | 1.078x ↓<br>[📄](results/bm-20260929-3.16.0a0-540274c-NOGIL/bm-20260929-macm4pro-arm64-python-540274c649e29a88f56c-3.16.0a0-540274c-vs-3.13.0rc2.md)[📈](results/bm-20260929-3.16.0a0-540274c-NOGIL/bm-20260929-macm4pro-arm64-python-540274c649e29a88f56c-3.16.0a0-540274c-vs-3.13.0rc2.svg) | 1.124x ↓<br>[📄](results/bm-20260929-3.16.0a0-540274c-NOGIL/bm-20260929-macm4pro-arm64-python-540274c649e29a88f56c-3.16.0a0-540274c-vs-base.md)[📈](results/bm-20260929-3.16.0a0-540274c-NOGIL/bm-20260929-macm4pro-arm64-python-540274c649e29a88f56c-3.16.0a0-540274c-vs-base.svg)[🧠](results/bm-20260929-3.16.0a0-540274c-NOGIL/bm-20260929-macm4pro-arm64-python-540274c649e29a88f56c-3.16.0a0-540274c-vs-base-mem.svg) |
| [2026-09-29](results/bm-20260929-3.16.0a0-540274c) | python/540274c649e29a88f56c | 540274c | 1.138x ↑<br>[📄](results/bm-20260929-3.16.0a0-540274c/bm-20260929-macm4pro-arm64-python-540274c649e29a88f56c-3.16.0a0-540274c-vs-3.12.6.md)[📈](results/bm-20260929-3.16.0a0-540274c/bm-20260929-macm4pro-arm64-python-540274c649e29a88f56c-3.16.0a0-540274c-vs-3.12.6.svg) | 1.051x ↑<br>[📄](results/bm-20260929-3.16.0a0-540274c/bm-20260929-macm4pro-arm64-python-540274c649e29a88f56c-3.16.0a0-540274c-vs-3.13.0rc2.md)[📈](results/bm-20260929-3.16.0a0-540274c/bm-20260929-macm4pro-arm64-python-540274c649e29a88f56c-3.16.0a0-540274c-vs-3.13.0rc2.svg) |  |
| [2026-09-28](results/bm-20260928-3.16.0a0-3330712-NOGIL) | python/333071231d3a46cccc32 | 3330712 (NOGIL) | 1.002x ↓<br>[📄](results/bm-20260928-3.16.0a0-3330712-NOGIL/bm-20260928-macm4pro-arm64-python-333071231d3a46cccc32-3.16.0a0-3330712-vs-3.12.6.md)[📈](results/bm-20260928-3.16.0a0-3330712-NOGIL/bm-20260928-macm4pro-arm64-python-333071231d3a46cccc32-3.16.0a0-3330712-vs-3.12.6.svg) | 1.075x ↓<br>[📄](results/bm-20260928-3.16.0a0-3330712-NOGIL/bm-20260928-macm4pro-arm64-python-333071231d3a46cccc32-3.16.0a0-3330712-vs-3.13.0rc2.md)[📈](results/bm-20260928-3.16.0a0-3330712-NOGIL/bm-20260928-macm4pro-arm64-python-333071231d3a46cccc32-3.16.0a0-3330712-vs-3.13.0rc2.svg) | 1.122x ↓<br>[📄](results/bm-20260928-3.16.0a0-3330712-NOGIL/bm-20260928-macm4pro-arm64-python-333071231d3a46cccc32-3.16.0a0-3330712-vs-base.md)[📈](results/bm-20260928-3.16.0a0-3330712-NOGIL/bm-20260928-macm4pro-arm64-python-333071231d3a46cccc32-3.16.0a0-3330712-vs-base.svg)[🧠](results/bm-20260928-3.16.0a0-3330712-NOGIL/bm-20260928-macm4pro-arm64-python-333071231d3a46cccc32-3.16.0a0-3330712-vs-base-mem.svg) |
| [2026-09-28](results/bm-20260928-3.16.0a0-3330712) | python/333071231d3a46cccc32 | 3330712 | 1.138x ↑<br>[📄](results/bm-20260928-3.16.0a0-3330712/bm-20260928-macm4pro-arm64-python-333071231d3a46cccc32-3.16.0a0-3330712-vs-3.12.6.md)[📈](results/bm-20260928-3.16.0a0-3330712/bm-20260928-macm4pro-arm64-python-333071231d3a46cccc32-3.16.0a0-3330712-vs-3.12.6.svg) | 1.051x ↑<br>[📄](results/bm-20260928-3.16.0a0-3330712/bm-20260928-macm4pro-arm64-python-333071231d3a46cccc32-3.16.0a0-3330712-vs-3.13.0rc2.md)[📈](results/bm-20260928-3.16.0a0-3330712/bm-20260928-macm4pro-arm64-python-333071231d3a46cccc32-3.16.0a0-3330712-vs-3.13.0rc2.svg) |  |


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
