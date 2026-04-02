# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (1fd66ea)](results/bm-20260328-3.15.0a7%2B-1fd66ea/bm-20260328-vultr-x86_64-python-1fd66eadd258223a0e34-3.15.0a7%2B-1fd66ea-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (1fd66ea)](results/bm-20260328-3.15.0a7%2B-1fd66ea-PYTHON_UOPS/bm-20260328-vultr-x86_64-python-1fd66eadd258223a0e34-3.15.0a7%2B-1fd66ea-pystats.md)
- [Most recent JIT pystats on main (bedaea0)](results/bm-20251019-3.15.0a1%2B-bedaea0-JIT/bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-04-01](results/bm-20260401-3.15.0a7%2B-c32e264-NOGIL) | python/c32e264227b1fee3a643 | c32e264 (NOGIL) | 1.026x ↓<br>[📄](results/bm-20260401-3.15.0a7%2B-c32e264-NOGIL/bm-20260401-vultr-x86_64-python-c32e264227b1fee3a643-3.15.0a7%2B-c32e264-vs-3.12.6.md)[📈](results/bm-20260401-3.15.0a7%2B-c32e264-NOGIL/bm-20260401-vultr-x86_64-python-c32e264227b1fee3a643-3.15.0a7%2B-c32e264-vs-3.12.6.svg) | 1.058x ↓<br>[📄](results/bm-20260401-3.15.0a7%2B-c32e264-NOGIL/bm-20260401-vultr-x86_64-python-c32e264227b1fee3a643-3.15.0a7%2B-c32e264-vs-3.13.0rc2.md)[📈](results/bm-20260401-3.15.0a7%2B-c32e264-NOGIL/bm-20260401-vultr-x86_64-python-c32e264227b1fee3a643-3.15.0a7%2B-c32e264-vs-3.13.0rc2.svg) | 1.106x ↓<br>[📄](results/bm-20260401-3.15.0a7%2B-c32e264-NOGIL/bm-20260401-vultr-x86_64-python-c32e264227b1fee3a643-3.15.0a7%2B-c32e264-vs-base.md)[📈](results/bm-20260401-3.15.0a7%2B-c32e264-NOGIL/bm-20260401-vultr-x86_64-python-c32e264227b1fee3a643-3.15.0a7%2B-c32e264-vs-base.svg)[🧠](results/bm-20260401-3.15.0a7%2B-c32e264-NOGIL/bm-20260401-vultr-x86_64-python-c32e264227b1fee3a643-3.15.0a7%2B-c32e264-vs-base-mem.svg) |
| [2026-04-01](results/bm-20260401-3.15.0a7%2B-c32e264) | python/c32e264227b1fee3a643 | c32e264 | 1.085x ↑<br>[📄](results/bm-20260401-3.15.0a7%2B-c32e264/bm-20260401-vultr-x86_64-python-c32e264227b1fee3a643-3.15.0a7%2B-c32e264-vs-3.12.6.md)[📈](results/bm-20260401-3.15.0a7%2B-c32e264/bm-20260401-vultr-x86_64-python-c32e264227b1fee3a643-3.15.0a7%2B-c32e264-vs-3.12.6.svg) | 1.049x ↑<br>[📄](results/bm-20260401-3.15.0a7%2B-c32e264/bm-20260401-vultr-x86_64-python-c32e264227b1fee3a643-3.15.0a7%2B-c32e264-vs-3.13.0rc2.md)[📈](results/bm-20260401-3.15.0a7%2B-c32e264/bm-20260401-vultr-x86_64-python-c32e264227b1fee3a643-3.15.0a7%2B-c32e264-vs-3.13.0rc2.svg) |  |
| [2026-03-31](results/bm-20260331-3.15.0a7%2B-9e1f164-NOGIL) | python/9e1f1644cd7b7661f074 | 9e1f164 (NOGIL) | 1.022x ↓<br>[📄](results/bm-20260331-3.15.0a7%2B-9e1f164-NOGIL/bm-20260331-vultr-x86_64-python-9e1f1644cd7b7661f074-3.15.0a7%2B-9e1f164-vs-3.12.6.md)[📈](results/bm-20260331-3.15.0a7%2B-9e1f164-NOGIL/bm-20260331-vultr-x86_64-python-9e1f1644cd7b7661f074-3.15.0a7%2B-9e1f164-vs-3.12.6.svg) | 1.054x ↓<br>[📄](results/bm-20260331-3.15.0a7%2B-9e1f164-NOGIL/bm-20260331-vultr-x86_64-python-9e1f1644cd7b7661f074-3.15.0a7%2B-9e1f164-vs-3.13.0rc2.md)[📈](results/bm-20260331-3.15.0a7%2B-9e1f164-NOGIL/bm-20260331-vultr-x86_64-python-9e1f1644cd7b7661f074-3.15.0a7%2B-9e1f164-vs-3.13.0rc2.svg) | 1.094x ↓<br>[📄](results/bm-20260331-3.15.0a7%2B-9e1f164-NOGIL/bm-20260331-vultr-x86_64-python-9e1f1644cd7b7661f074-3.15.0a7%2B-9e1f164-vs-base.md)[📈](results/bm-20260331-3.15.0a7%2B-9e1f164-NOGIL/bm-20260331-vultr-x86_64-python-9e1f1644cd7b7661f074-3.15.0a7%2B-9e1f164-vs-base.svg)[🧠](results/bm-20260331-3.15.0a7%2B-9e1f164-NOGIL/bm-20260331-vultr-x86_64-python-9e1f1644cd7b7661f074-3.15.0a7%2B-9e1f164-vs-base-mem.svg) |
| [2026-03-31](results/bm-20260331-3.15.0a7%2B-9e1f164) | python/9e1f1644cd7b7661f074 | 9e1f164 | 1.075x ↑<br>[📄](results/bm-20260331-3.15.0a7%2B-9e1f164/bm-20260331-vultr-x86_64-python-9e1f1644cd7b7661f074-3.15.0a7%2B-9e1f164-vs-3.12.6.md)[📈](results/bm-20260331-3.15.0a7%2B-9e1f164/bm-20260331-vultr-x86_64-python-9e1f1644cd7b7661f074-3.15.0a7%2B-9e1f164-vs-3.12.6.svg) | 1.039x ↑<br>[📄](results/bm-20260331-3.15.0a7%2B-9e1f164/bm-20260331-vultr-x86_64-python-9e1f1644cd7b7661f074-3.15.0a7%2B-9e1f164-vs-3.13.0rc2.md)[📈](results/bm-20260331-3.15.0a7%2B-9e1f164/bm-20260331-vultr-x86_64-python-9e1f1644cd7b7661f074-3.15.0a7%2B-9e1f164-vs-3.13.0rc2.svg) |  |
| [2026-03-30](results/bm-20260330-3.15.0a7%2B-70d1b08-NOGIL) | python/70d1b08a4bb52652094c | 70d1b08 (NOGIL) | 1.024x ↓<br>[📄](results/bm-20260330-3.15.0a7%2B-70d1b08-NOGIL/bm-20260330-vultr-x86_64-python-70d1b08a4bb52652094c-3.15.0a7%2B-70d1b08-vs-3.12.6.md)[📈](results/bm-20260330-3.15.0a7%2B-70d1b08-NOGIL/bm-20260330-vultr-x86_64-python-70d1b08a4bb52652094c-3.15.0a7%2B-70d1b08-vs-3.12.6.svg) | 1.057x ↓<br>[📄](results/bm-20260330-3.15.0a7%2B-70d1b08-NOGIL/bm-20260330-vultr-x86_64-python-70d1b08a4bb52652094c-3.15.0a7%2B-70d1b08-vs-3.13.0rc2.md)[📈](results/bm-20260330-3.15.0a7%2B-70d1b08-NOGIL/bm-20260330-vultr-x86_64-python-70d1b08a4bb52652094c-3.15.0a7%2B-70d1b08-vs-3.13.0rc2.svg) | 1.095x ↓<br>[📄](results/bm-20260330-3.15.0a7%2B-70d1b08-NOGIL/bm-20260330-vultr-x86_64-python-70d1b08a4bb52652094c-3.15.0a7%2B-70d1b08-vs-base.md)[📈](results/bm-20260330-3.15.0a7%2B-70d1b08-NOGIL/bm-20260330-vultr-x86_64-python-70d1b08a4bb52652094c-3.15.0a7%2B-70d1b08-vs-base.svg)[🧠](results/bm-20260330-3.15.0a7%2B-70d1b08-NOGIL/bm-20260330-vultr-x86_64-python-70d1b08a4bb52652094c-3.15.0a7%2B-70d1b08-vs-base-mem.svg) |
| [2026-03-30](results/bm-20260330-3.15.0a7%2B-70d1b08) | python/70d1b08a4bb52652094c | 70d1b08 | 1.072x ↑<br>[📄](results/bm-20260330-3.15.0a7%2B-70d1b08/bm-20260330-vultr-x86_64-python-70d1b08a4bb52652094c-3.15.0a7%2B-70d1b08-vs-3.12.6.md)[📈](results/bm-20260330-3.15.0a7%2B-70d1b08/bm-20260330-vultr-x86_64-python-70d1b08a4bb52652094c-3.15.0a7%2B-70d1b08-vs-3.12.6.svg) | 1.036x ↑<br>[📄](results/bm-20260330-3.15.0a7%2B-70d1b08/bm-20260330-vultr-x86_64-python-70d1b08a4bb52652094c-3.15.0a7%2B-70d1b08-vs-3.13.0rc2.md)[📈](results/bm-20260330-3.15.0a7%2B-70d1b08/bm-20260330-vultr-x86_64-python-70d1b08a4bb52652094c-3.15.0a7%2B-70d1b08-vs-3.13.0rc2.svg) |  |
| [2026-03-29](results/bm-20260329-3.15.0a7%2B-4d0e8ee-NOGIL) | python/4d0e8ee649ceff96b130 | 4d0e8ee (NOGIL) | 1.029x ↓<br>[📄](results/bm-20260329-3.15.0a7%2B-4d0e8ee-NOGIL/bm-20260329-vultr-x86_64-python-4d0e8ee649ceff96b130-3.15.0a7%2B-4d0e8ee-vs-3.12.6.md)[📈](results/bm-20260329-3.15.0a7%2B-4d0e8ee-NOGIL/bm-20260329-vultr-x86_64-python-4d0e8ee649ceff96b130-3.15.0a7%2B-4d0e8ee-vs-3.12.6.svg) | 1.062x ↓<br>[📄](results/bm-20260329-3.15.0a7%2B-4d0e8ee-NOGIL/bm-20260329-vultr-x86_64-python-4d0e8ee649ceff96b130-3.15.0a7%2B-4d0e8ee-vs-3.13.0rc2.md)[📈](results/bm-20260329-3.15.0a7%2B-4d0e8ee-NOGIL/bm-20260329-vultr-x86_64-python-4d0e8ee649ceff96b130-3.15.0a7%2B-4d0e8ee-vs-3.13.0rc2.svg) | 1.104x ↓<br>[📄](results/bm-20260329-3.15.0a7%2B-4d0e8ee-NOGIL/bm-20260329-vultr-x86_64-python-4d0e8ee649ceff96b130-3.15.0a7%2B-4d0e8ee-vs-base.md)[📈](results/bm-20260329-3.15.0a7%2B-4d0e8ee-NOGIL/bm-20260329-vultr-x86_64-python-4d0e8ee649ceff96b130-3.15.0a7%2B-4d0e8ee-vs-base.svg)[🧠](results/bm-20260329-3.15.0a7%2B-4d0e8ee-NOGIL/bm-20260329-vultr-x86_64-python-4d0e8ee649ceff96b130-3.15.0a7%2B-4d0e8ee-vs-base-mem.svg) |
| [2026-03-29](results/bm-20260329-3.15.0a7%2B-4d0e8ee) | python/4d0e8ee649ceff96b130 | 4d0e8ee | 1.078x ↑<br>[📄](results/bm-20260329-3.15.0a7%2B-4d0e8ee/bm-20260329-vultr-x86_64-python-4d0e8ee649ceff96b130-3.15.0a7%2B-4d0e8ee-vs-3.12.6.md)[📈](results/bm-20260329-3.15.0a7%2B-4d0e8ee/bm-20260329-vultr-x86_64-python-4d0e8ee649ceff96b130-3.15.0a7%2B-4d0e8ee-vs-3.12.6.svg) | 1.042x ↑<br>[📄](results/bm-20260329-3.15.0a7%2B-4d0e8ee/bm-20260329-vultr-x86_64-python-4d0e8ee649ceff96b130-3.15.0a7%2B-4d0e8ee-vs-3.13.0rc2.md)[📈](results/bm-20260329-3.15.0a7%2B-4d0e8ee/bm-20260329-vultr-x86_64-python-4d0e8ee649ceff96b130-3.15.0a7%2B-4d0e8ee-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-04-01](results/bm-20260401-3.15.0a7%2B-c32e264-NOGIL) | python/c32e264227b1fee3a643 | c32e264 (NOGIL) | 1.097x ↑<br>[📄](results/bm-20260401-3.15.0a7%2B-c32e264-NOGIL/bm-20260401-macm4pro-arm64-python-c32e264227b1fee3a643-3.15.0a7%2B-c32e264-vs-3.12.6.md)[📈](results/bm-20260401-3.15.0a7%2B-c32e264-NOGIL/bm-20260401-macm4pro-arm64-python-c32e264227b1fee3a643-3.15.0a7%2B-c32e264-vs-3.12.6.svg) | 1.018x ↑<br>[📄](results/bm-20260401-3.15.0a7%2B-c32e264-NOGIL/bm-20260401-macm4pro-arm64-python-c32e264227b1fee3a643-3.15.0a7%2B-c32e264-vs-3.13.0rc2.md)[📈](results/bm-20260401-3.15.0a7%2B-c32e264-NOGIL/bm-20260401-macm4pro-arm64-python-c32e264227b1fee3a643-3.15.0a7%2B-c32e264-vs-3.13.0rc2.svg) | 1.051x ↓<br>[📄](results/bm-20260401-3.15.0a7%2B-c32e264-NOGIL/bm-20260401-macm4pro-arm64-python-c32e264227b1fee3a643-3.15.0a7%2B-c32e264-vs-base.md)[📈](results/bm-20260401-3.15.0a7%2B-c32e264-NOGIL/bm-20260401-macm4pro-arm64-python-c32e264227b1fee3a643-3.15.0a7%2B-c32e264-vs-base.svg)[🧠](results/bm-20260401-3.15.0a7%2B-c32e264-NOGIL/bm-20260401-macm4pro-arm64-python-c32e264227b1fee3a643-3.15.0a7%2B-c32e264-vs-base-mem.svg) |
| [2026-04-01](results/bm-20260401-3.15.0a7%2B-c32e264) | python/c32e264227b1fee3a643 | c32e264 | 1.156x ↑<br>[📄](results/bm-20260401-3.15.0a7%2B-c32e264/bm-20260401-macm4pro-arm64-python-c32e264227b1fee3a643-3.15.0a7%2B-c32e264-vs-3.12.6.md)[📈](results/bm-20260401-3.15.0a7%2B-c32e264/bm-20260401-macm4pro-arm64-python-c32e264227b1fee3a643-3.15.0a7%2B-c32e264-vs-3.12.6.svg) | 1.073x ↑<br>[📄](results/bm-20260401-3.15.0a7%2B-c32e264/bm-20260401-macm4pro-arm64-python-c32e264227b1fee3a643-3.15.0a7%2B-c32e264-vs-3.13.0rc2.md)[📈](results/bm-20260401-3.15.0a7%2B-c32e264/bm-20260401-macm4pro-arm64-python-c32e264227b1fee3a643-3.15.0a7%2B-c32e264-vs-3.13.0rc2.svg) |  |
| [2026-03-31](results/bm-20260331-3.15.0a7%2B-9e1f164-NOGIL) | python/9e1f1644cd7b7661f074 | 9e1f164 (NOGIL) | 1.103x ↑<br>[📄](results/bm-20260331-3.15.0a7%2B-9e1f164-NOGIL/bm-20260331-macm4pro-arm64-python-9e1f1644cd7b7661f074-3.15.0a7%2B-9e1f164-vs-3.12.6.md)[📈](results/bm-20260331-3.15.0a7%2B-9e1f164-NOGIL/bm-20260331-macm4pro-arm64-python-9e1f1644cd7b7661f074-3.15.0a7%2B-9e1f164-vs-3.12.6.svg) | 1.023x ↑<br>[📄](results/bm-20260331-3.15.0a7%2B-9e1f164-NOGIL/bm-20260331-macm4pro-arm64-python-9e1f1644cd7b7661f074-3.15.0a7%2B-9e1f164-vs-3.13.0rc2.md)[📈](results/bm-20260331-3.15.0a7%2B-9e1f164-NOGIL/bm-20260331-macm4pro-arm64-python-9e1f1644cd7b7661f074-3.15.0a7%2B-9e1f164-vs-3.13.0rc2.svg) | 1.051x ↓<br>[📄](results/bm-20260331-3.15.0a7%2B-9e1f164-NOGIL/bm-20260331-macm4pro-arm64-python-9e1f1644cd7b7661f074-3.15.0a7%2B-9e1f164-vs-base.md)[📈](results/bm-20260331-3.15.0a7%2B-9e1f164-NOGIL/bm-20260331-macm4pro-arm64-python-9e1f1644cd7b7661f074-3.15.0a7%2B-9e1f164-vs-base.svg)[🧠](results/bm-20260331-3.15.0a7%2B-9e1f164-NOGIL/bm-20260331-macm4pro-arm64-python-9e1f1644cd7b7661f074-3.15.0a7%2B-9e1f164-vs-base-mem.svg) |
| [2026-03-31](results/bm-20260331-3.15.0a7%2B-9e1f164) | python/9e1f1644cd7b7661f074 | 9e1f164 | 1.162x ↑<br>[📄](results/bm-20260331-3.15.0a7%2B-9e1f164/bm-20260331-macm4pro-arm64-python-9e1f1644cd7b7661f074-3.15.0a7%2B-9e1f164-vs-3.12.6.md)[📈](results/bm-20260331-3.15.0a7%2B-9e1f164/bm-20260331-macm4pro-arm64-python-9e1f1644cd7b7661f074-3.15.0a7%2B-9e1f164-vs-3.12.6.svg) | 1.078x ↑<br>[📄](results/bm-20260331-3.15.0a7%2B-9e1f164/bm-20260331-macm4pro-arm64-python-9e1f1644cd7b7661f074-3.15.0a7%2B-9e1f164-vs-3.13.0rc2.md)[📈](results/bm-20260331-3.15.0a7%2B-9e1f164/bm-20260331-macm4pro-arm64-python-9e1f1644cd7b7661f074-3.15.0a7%2B-9e1f164-vs-3.13.0rc2.svg) |  |
| [2026-03-30](results/bm-20260330-3.15.0a7%2B-70d1b08-NOGIL) | python/70d1b08a4bb52652094c | 70d1b08 (NOGIL) | 1.094x ↑<br>[📄](results/bm-20260330-3.15.0a7%2B-70d1b08-NOGIL/bm-20260330-macm4pro-arm64-python-70d1b08a4bb52652094c-3.15.0a7%2B-70d1b08-vs-3.12.6.md)[📈](results/bm-20260330-3.15.0a7%2B-70d1b08-NOGIL/bm-20260330-macm4pro-arm64-python-70d1b08a4bb52652094c-3.15.0a7%2B-70d1b08-vs-3.12.6.svg) | 1.015x ↑<br>[📄](results/bm-20260330-3.15.0a7%2B-70d1b08-NOGIL/bm-20260330-macm4pro-arm64-python-70d1b08a4bb52652094c-3.15.0a7%2B-70d1b08-vs-3.13.0rc2.md)[📈](results/bm-20260330-3.15.0a7%2B-70d1b08-NOGIL/bm-20260330-macm4pro-arm64-python-70d1b08a4bb52652094c-3.15.0a7%2B-70d1b08-vs-3.13.0rc2.svg) | 1.054x ↓<br>[📄](results/bm-20260330-3.15.0a7%2B-70d1b08-NOGIL/bm-20260330-macm4pro-arm64-python-70d1b08a4bb52652094c-3.15.0a7%2B-70d1b08-vs-base.md)[📈](results/bm-20260330-3.15.0a7%2B-70d1b08-NOGIL/bm-20260330-macm4pro-arm64-python-70d1b08a4bb52652094c-3.15.0a7%2B-70d1b08-vs-base.svg)[🧠](results/bm-20260330-3.15.0a7%2B-70d1b08-NOGIL/bm-20260330-macm4pro-arm64-python-70d1b08a4bb52652094c-3.15.0a7%2B-70d1b08-vs-base-mem.svg) |
| [2026-03-30](results/bm-20260330-3.15.0a7%2B-70d1b08) | python/70d1b08a4bb52652094c | 70d1b08 | 1.156x ↑<br>[📄](results/bm-20260330-3.15.0a7%2B-70d1b08/bm-20260330-macm4pro-arm64-python-70d1b08a4bb52652094c-3.15.0a7%2B-70d1b08-vs-3.12.6.md)[📈](results/bm-20260330-3.15.0a7%2B-70d1b08/bm-20260330-macm4pro-arm64-python-70d1b08a4bb52652094c-3.15.0a7%2B-70d1b08-vs-3.12.6.svg) | 1.073x ↑<br>[📄](results/bm-20260330-3.15.0a7%2B-70d1b08/bm-20260330-macm4pro-arm64-python-70d1b08a4bb52652094c-3.15.0a7%2B-70d1b08-vs-3.13.0rc2.md)[📈](results/bm-20260330-3.15.0a7%2B-70d1b08/bm-20260330-macm4pro-arm64-python-70d1b08a4bb52652094c-3.15.0a7%2B-70d1b08-vs-3.13.0rc2.svg) |  |
| [2026-03-29](results/bm-20260329-3.15.0a7%2B-4d0e8ee-NOGIL) | python/4d0e8ee649ceff96b130 | 4d0e8ee (NOGIL) | 1.108x ↑<br>[📄](results/bm-20260329-3.15.0a7%2B-4d0e8ee-NOGIL/bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7%2B-4d0e8ee-vs-3.12.6.md)[📈](results/bm-20260329-3.15.0a7%2B-4d0e8ee-NOGIL/bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7%2B-4d0e8ee-vs-3.12.6.svg) | 1.028x ↑<br>[📄](results/bm-20260329-3.15.0a7%2B-4d0e8ee-NOGIL/bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7%2B-4d0e8ee-vs-3.13.0rc2.md)[📈](results/bm-20260329-3.15.0a7%2B-4d0e8ee-NOGIL/bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7%2B-4d0e8ee-vs-3.13.0rc2.svg) | 1.045x ↓<br>[📄](results/bm-20260329-3.15.0a7%2B-4d0e8ee-NOGIL/bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7%2B-4d0e8ee-vs-base.md)[📈](results/bm-20260329-3.15.0a7%2B-4d0e8ee-NOGIL/bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7%2B-4d0e8ee-vs-base.svg)[🧠](results/bm-20260329-3.15.0a7%2B-4d0e8ee-NOGIL/bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7%2B-4d0e8ee-vs-base-mem.svg) |
| [2026-03-29](results/bm-20260329-3.15.0a7%2B-4d0e8ee) | python/4d0e8ee649ceff96b130 | 4d0e8ee | 1.160x ↑<br>[📄](results/bm-20260329-3.15.0a7%2B-4d0e8ee/bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7%2B-4d0e8ee-vs-3.12.6.md)[📈](results/bm-20260329-3.15.0a7%2B-4d0e8ee/bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7%2B-4d0e8ee-vs-3.12.6.svg) | 1.076x ↑<br>[📄](results/bm-20260329-3.15.0a7%2B-4d0e8ee/bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7%2B-4d0e8ee-vs-3.13.0rc2.md)[📈](results/bm-20260329-3.15.0a7%2B-4d0e8ee/bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7%2B-4d0e8ee-vs-3.13.0rc2.svg) |  |


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
