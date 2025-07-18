# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (47b01da)](results/bm-20250712-3.15.0a0-47b01da/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (47b01da)](results/bm-20250712-3.15.0a0-47b01da-PYTHON_UOPS/bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-07-18](results/bm-20250718-3.15.0a0-03017a8-NOGIL) | python/03017a8cc2242d881a30 | 03017a8 (NOGIL) | 1.016x ↓<br>[📄](results/bm-20250718-3.15.0a0-03017a8-NOGIL/bm-20250718-vultr-x86_64-python-03017a8cc2242d881a30-3.15.0a0-03017a8-vs-3.12.6.md)[📈](results/bm-20250718-3.15.0a0-03017a8-NOGIL/bm-20250718-vultr-x86_64-python-03017a8cc2242d881a30-3.15.0a0-03017a8-vs-3.12.6.svg) | 1.049x ↓<br>[📄](results/bm-20250718-3.15.0a0-03017a8-NOGIL/bm-20250718-vultr-x86_64-python-03017a8cc2242d881a30-3.15.0a0-03017a8-vs-3.13.0rc2.md)[📈](results/bm-20250718-3.15.0a0-03017a8-NOGIL/bm-20250718-vultr-x86_64-python-03017a8cc2242d881a30-3.15.0a0-03017a8-vs-3.13.0rc2.svg) | 1.004x ↑<br>[📄](results/bm-20250718-3.15.0a0-03017a8-NOGIL/bm-20250718-vultr-x86_64-python-03017a8cc2242d881a30-3.15.0a0-03017a8-vs-base.md)[📈](results/bm-20250718-3.15.0a0-03017a8-NOGIL/bm-20250718-vultr-x86_64-python-03017a8cc2242d881a30-3.15.0a0-03017a8-vs-base.svg)[🧠](results/bm-20250718-3.15.0a0-03017a8-NOGIL/bm-20250718-vultr-x86_64-python-03017a8cc2242d881a30-3.15.0a0-03017a8-vs-base-mem.svg) |
| [2025-07-18](results/bm-20250718-3.15.0a0-03017a8) | python/03017a8cc2242d881a30 | 03017a8 | 1.068x ↑<br>[📄](results/bm-20250718-3.15.0a0-03017a8/bm-20250718-vultr-x86_64-python-03017a8cc2242d881a30-3.15.0a0-03017a8-vs-3.12.6.md)[📈](results/bm-20250718-3.15.0a0-03017a8/bm-20250718-vultr-x86_64-python-03017a8cc2242d881a30-3.15.0a0-03017a8-vs-3.12.6.svg) | 1.032x ↑<br>[📄](results/bm-20250718-3.15.0a0-03017a8/bm-20250718-vultr-x86_64-python-03017a8cc2242d881a30-3.15.0a0-03017a8-vs-3.13.0rc2.md)[📈](results/bm-20250718-3.15.0a0-03017a8/bm-20250718-vultr-x86_64-python-03017a8cc2242d881a30-3.15.0a0-03017a8-vs-3.13.0rc2.svg) | 1.001x ↓<br>[📄](results/bm-20250718-3.15.0a0-03017a8/bm-20250718-vultr-x86_64-python-03017a8cc2242d881a30-3.15.0a0-03017a8-vs-base.md)[📈](results/bm-20250718-3.15.0a0-03017a8/bm-20250718-vultr-x86_64-python-03017a8cc2242d881a30-3.15.0a0-03017a8-vs-base.svg)[🧠](results/bm-20250718-3.15.0a0-03017a8/bm-20250718-vultr-x86_64-python-03017a8cc2242d881a30-3.15.0a0-03017a8-vs-base-mem.svg) |
| [2025-07-17](results/bm-20250717-3.15.0a0-28937d3-NOGIL) | python/28937d3a21cf8168c853 | 28937d3 (NOGIL) | 1.020x ↓<br>[📄](results/bm-20250717-3.15.0a0-28937d3-NOGIL/bm-20250717-vultr-x86_64-python-28937d3a21cf8168c853-3.15.0a0-28937d3-vs-3.12.6.md)[📈](results/bm-20250717-3.15.0a0-28937d3-NOGIL/bm-20250717-vultr-x86_64-python-28937d3a21cf8168c853-3.15.0a0-28937d3-vs-3.12.6.svg) | 1.053x ↓<br>[📄](results/bm-20250717-3.15.0a0-28937d3-NOGIL/bm-20250717-vultr-x86_64-python-28937d3a21cf8168c853-3.15.0a0-28937d3-vs-3.13.0rc2.md)[📈](results/bm-20250717-3.15.0a0-28937d3-NOGIL/bm-20250717-vultr-x86_64-python-28937d3a21cf8168c853-3.15.0a0-28937d3-vs-3.13.0rc2.svg) | 1.089x ↓<br>[📄](results/bm-20250717-3.15.0a0-28937d3-NOGIL/bm-20250717-vultr-x86_64-python-28937d3a21cf8168c853-3.15.0a0-28937d3-vs-base.md)[📈](results/bm-20250717-3.15.0a0-28937d3-NOGIL/bm-20250717-vultr-x86_64-python-28937d3a21cf8168c853-3.15.0a0-28937d3-vs-base.svg)[🧠](results/bm-20250717-3.15.0a0-28937d3-NOGIL/bm-20250717-vultr-x86_64-python-28937d3a21cf8168c853-3.15.0a0-28937d3-vs-base-mem.svg) |
| [2025-07-17](results/bm-20250717-3.15.0a0-28937d3) | python/28937d3a21cf8168c853 | 28937d3 | 1.068x ↑<br>[📄](results/bm-20250717-3.15.0a0-28937d3/bm-20250717-vultr-x86_64-python-28937d3a21cf8168c853-3.15.0a0-28937d3-vs-3.12.6.md)[📈](results/bm-20250717-3.15.0a0-28937d3/bm-20250717-vultr-x86_64-python-28937d3a21cf8168c853-3.15.0a0-28937d3-vs-3.12.6.svg) | 1.033x ↑<br>[📄](results/bm-20250717-3.15.0a0-28937d3/bm-20250717-vultr-x86_64-python-28937d3a21cf8168c853-3.15.0a0-28937d3-vs-3.13.0rc2.md)[📈](results/bm-20250717-3.15.0a0-28937d3/bm-20250717-vultr-x86_64-python-28937d3a21cf8168c853-3.15.0a0-28937d3-vs-3.13.0rc2.svg) |  |
| [2025-07-16](results/bm-20250716-3.15.0a0-180b3eb-NOGIL) | python/180b3eb697bf5bb0088f | 180b3eb (NOGIL) | 1.021x ↓<br>[📄](results/bm-20250716-3.15.0a0-180b3eb-NOGIL/bm-20250716-vultr-x86_64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb-vs-3.12.6.md)[📈](results/bm-20250716-3.15.0a0-180b3eb-NOGIL/bm-20250716-vultr-x86_64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb-vs-3.12.6.svg) | 1.054x ↓<br>[📄](results/bm-20250716-3.15.0a0-180b3eb-NOGIL/bm-20250716-vultr-x86_64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb-vs-3.13.0rc2.md)[📈](results/bm-20250716-3.15.0a0-180b3eb-NOGIL/bm-20250716-vultr-x86_64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb-vs-3.13.0rc2.svg) | 1.093x ↓<br>[📄](results/bm-20250716-3.15.0a0-180b3eb-NOGIL/bm-20250716-vultr-x86_64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb-vs-base.md)[📈](results/bm-20250716-3.15.0a0-180b3eb-NOGIL/bm-20250716-vultr-x86_64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb-vs-base.svg)[🧠](results/bm-20250716-3.15.0a0-180b3eb-NOGIL/bm-20250716-vultr-x86_64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb-vs-base-mem.svg) |
| [2025-07-16](results/bm-20250716-3.15.0a0-180b3eb) | python/180b3eb697bf5bb0088f | 180b3eb | 1.072x ↑<br>[📄](results/bm-20250716-3.15.0a0-180b3eb/bm-20250716-vultr-x86_64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb-vs-3.12.6.md)[📈](results/bm-20250716-3.15.0a0-180b3eb/bm-20250716-vultr-x86_64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb-vs-3.12.6.svg) | 1.036x ↑<br>[📄](results/bm-20250716-3.15.0a0-180b3eb/bm-20250716-vultr-x86_64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb-vs-3.13.0rc2.md)[📈](results/bm-20250716-3.15.0a0-180b3eb/bm-20250716-vultr-x86_64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb-vs-3.13.0rc2.svg) |  |
| [2025-07-15](results/bm-20250715-3.15.0a0-cb59eae-NOGIL) | python/cb59eaefeda5ff44ac0c | cb59eae (NOGIL) | 1.024x ↓<br>[📄](results/bm-20250715-3.15.0a0-cb59eae-NOGIL/bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae-vs-3.12.6.md)[📈](results/bm-20250715-3.15.0a0-cb59eae-NOGIL/bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae-vs-3.12.6.svg) | 1.057x ↓<br>[📄](results/bm-20250715-3.15.0a0-cb59eae-NOGIL/bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae-vs-3.13.0rc2.md)[📈](results/bm-20250715-3.15.0a0-cb59eae-NOGIL/bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae-vs-3.13.0rc2.svg) | 1.093x ↓<br>[📄](results/bm-20250715-3.15.0a0-cb59eae-NOGIL/bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae-vs-base.md)[📈](results/bm-20250715-3.15.0a0-cb59eae-NOGIL/bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae-vs-base.svg)[🧠](results/bm-20250715-3.15.0a0-cb59eae-NOGIL/bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae-vs-base-mem.svg) |
| [2025-07-15](results/bm-20250715-3.15.0a0-cb59eae) | python/cb59eaefeda5ff44ac0c | cb59eae | 1.070x ↑<br>[📄](results/bm-20250715-3.15.0a0-cb59eae/bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae-vs-3.12.6.md)[📈](results/bm-20250715-3.15.0a0-cb59eae/bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae-vs-3.12.6.svg) | 1.034x ↑<br>[📄](results/bm-20250715-3.15.0a0-cb59eae/bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae-vs-3.13.0rc2.md)[📈](results/bm-20250715-3.15.0a0-cb59eae/bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-07-18](results/bm-20250718-3.15.0a0-03017a8-NOGIL) | python/03017a8cc2242d881a30 | 03017a8 (NOGIL) | 1.092x ↑<br>[📄](results/bm-20250718-3.15.0a0-03017a8-NOGIL/bm-20250718-macm4pro-arm64-python-03017a8cc2242d881a30-3.15.0a0-03017a8-vs-3.12.6.md)[📈](results/bm-20250718-3.15.0a0-03017a8-NOGIL/bm-20250718-macm4pro-arm64-python-03017a8cc2242d881a30-3.15.0a0-03017a8-vs-3.12.6.svg) | 1.013x ↑<br>[📄](results/bm-20250718-3.15.0a0-03017a8-NOGIL/bm-20250718-macm4pro-arm64-python-03017a8cc2242d881a30-3.15.0a0-03017a8-vs-3.13.0rc2.md)[📈](results/bm-20250718-3.15.0a0-03017a8-NOGIL/bm-20250718-macm4pro-arm64-python-03017a8cc2242d881a30-3.15.0a0-03017a8-vs-3.13.0rc2.svg) | 1.012x ↓<br>[📄](results/bm-20250718-3.15.0a0-03017a8-NOGIL/bm-20250718-macm4pro-arm64-python-03017a8cc2242d881a30-3.15.0a0-03017a8-vs-base.md)[📈](results/bm-20250718-3.15.0a0-03017a8-NOGIL/bm-20250718-macm4pro-arm64-python-03017a8cc2242d881a30-3.15.0a0-03017a8-vs-base.svg)[🧠](results/bm-20250718-3.15.0a0-03017a8-NOGIL/bm-20250718-macm4pro-arm64-python-03017a8cc2242d881a30-3.15.0a0-03017a8-vs-base-mem.svg) |
| [2025-07-18](results/bm-20250718-3.15.0a0-03017a8) | python/03017a8cc2242d881a30 | 03017a8 | 1.107x ↑<br>[📄](results/bm-20250718-3.15.0a0-03017a8/bm-20250718-macm4pro-arm64-python-03017a8cc2242d881a30-3.15.0a0-03017a8-vs-3.12.6.md)[📈](results/bm-20250718-3.15.0a0-03017a8/bm-20250718-macm4pro-arm64-python-03017a8cc2242d881a30-3.15.0a0-03017a8-vs-3.12.6.svg) | 1.027x ↑<br>[📄](results/bm-20250718-3.15.0a0-03017a8/bm-20250718-macm4pro-arm64-python-03017a8cc2242d881a30-3.15.0a0-03017a8-vs-3.13.0rc2.md)[📈](results/bm-20250718-3.15.0a0-03017a8/bm-20250718-macm4pro-arm64-python-03017a8cc2242d881a30-3.15.0a0-03017a8-vs-3.13.0rc2.svg) | 1.004x ↓<br>[📄](results/bm-20250718-3.15.0a0-03017a8/bm-20250718-macm4pro-arm64-python-03017a8cc2242d881a30-3.15.0a0-03017a8-vs-base.md)[📈](results/bm-20250718-3.15.0a0-03017a8/bm-20250718-macm4pro-arm64-python-03017a8cc2242d881a30-3.15.0a0-03017a8-vs-base.svg)[🧠](results/bm-20250718-3.15.0a0-03017a8/bm-20250718-macm4pro-arm64-python-03017a8cc2242d881a30-3.15.0a0-03017a8-vs-base-mem.svg) |
| [2025-07-17](results/bm-20250717-3.15.0a0-28937d3-NOGIL) | python/28937d3a21cf8168c853 | 28937d3 (NOGIL) | 1.106x ↑<br>[📄](results/bm-20250717-3.15.0a0-28937d3-NOGIL/bm-20250717-macm4pro-arm64-python-28937d3a21cf8168c853-3.15.0a0-28937d3-vs-3.12.6.md)[📈](results/bm-20250717-3.15.0a0-28937d3-NOGIL/bm-20250717-macm4pro-arm64-python-28937d3a21cf8168c853-3.15.0a0-28937d3-vs-3.12.6.svg) | 1.026x ↑<br>[📄](results/bm-20250717-3.15.0a0-28937d3-NOGIL/bm-20250717-macm4pro-arm64-python-28937d3a21cf8168c853-3.15.0a0-28937d3-vs-3.13.0rc2.md)[📈](results/bm-20250717-3.15.0a0-28937d3-NOGIL/bm-20250717-macm4pro-arm64-python-28937d3a21cf8168c853-3.15.0a0-28937d3-vs-3.13.0rc2.svg) | 1.006x ↓<br>[📄](results/bm-20250717-3.15.0a0-28937d3-NOGIL/bm-20250717-macm4pro-arm64-python-28937d3a21cf8168c853-3.15.0a0-28937d3-vs-base.md)[📈](results/bm-20250717-3.15.0a0-28937d3-NOGIL/bm-20250717-macm4pro-arm64-python-28937d3a21cf8168c853-3.15.0a0-28937d3-vs-base.svg)[🧠](results/bm-20250717-3.15.0a0-28937d3-NOGIL/bm-20250717-macm4pro-arm64-python-28937d3a21cf8168c853-3.15.0a0-28937d3-vs-base-mem.svg) |
| [2025-07-17](results/bm-20250717-3.15.0a0-28937d3) | python/28937d3a21cf8168c853 | 28937d3 | 1.111x ↑<br>[📄](results/bm-20250717-3.15.0a0-28937d3/bm-20250717-macm4pro-arm64-python-28937d3a21cf8168c853-3.15.0a0-28937d3-vs-3.12.6.md)[📈](results/bm-20250717-3.15.0a0-28937d3/bm-20250717-macm4pro-arm64-python-28937d3a21cf8168c853-3.15.0a0-28937d3-vs-3.12.6.svg) | 1.031x ↑<br>[📄](results/bm-20250717-3.15.0a0-28937d3/bm-20250717-macm4pro-arm64-python-28937d3a21cf8168c853-3.15.0a0-28937d3-vs-3.13.0rc2.md)[📈](results/bm-20250717-3.15.0a0-28937d3/bm-20250717-macm4pro-arm64-python-28937d3a21cf8168c853-3.15.0a0-28937d3-vs-3.13.0rc2.svg) |  |
| [2025-07-16](results/bm-20250716-3.15.0a0-180b3eb-NOGIL) | python/180b3eb697bf5bb0088f | 180b3eb (NOGIL) | 1.100x ↑<br>[📄](results/bm-20250716-3.15.0a0-180b3eb-NOGIL/bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb-vs-3.12.6.md)[📈](results/bm-20250716-3.15.0a0-180b3eb-NOGIL/bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb-vs-3.12.6.svg) | 1.021x ↑<br>[📄](results/bm-20250716-3.15.0a0-180b3eb-NOGIL/bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb-vs-3.13.0rc2.md)[📈](results/bm-20250716-3.15.0a0-180b3eb-NOGIL/bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb-vs-3.13.0rc2.svg) | 1.003x ↓<br>[📄](results/bm-20250716-3.15.0a0-180b3eb-NOGIL/bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb-vs-base.md)[📈](results/bm-20250716-3.15.0a0-180b3eb-NOGIL/bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb-vs-base.svg)[🧠](results/bm-20250716-3.15.0a0-180b3eb-NOGIL/bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb-vs-base-mem.svg) |
| [2025-07-16](results/bm-20250716-3.15.0a0-180b3eb) | python/180b3eb697bf5bb0088f | 180b3eb | 1.102x ↑<br>[📄](results/bm-20250716-3.15.0a0-180b3eb/bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb-vs-3.12.6.md)[📈](results/bm-20250716-3.15.0a0-180b3eb/bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb-vs-3.12.6.svg) | 1.022x ↑<br>[📄](results/bm-20250716-3.15.0a0-180b3eb/bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb-vs-3.13.0rc2.md)[📈](results/bm-20250716-3.15.0a0-180b3eb/bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb-vs-3.13.0rc2.svg) |  |
| [2025-07-15](results/bm-20250715-3.15.0a0-cb59eae-NOGIL) | python/cb59eaefeda5ff44ac0c | cb59eae (NOGIL) | 1.112x ↑<br>[📄](results/bm-20250715-3.15.0a0-cb59eae-NOGIL/bm-20250715-macm4pro-arm64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae-vs-3.12.6.md)[📈](results/bm-20250715-3.15.0a0-cb59eae-NOGIL/bm-20250715-macm4pro-arm64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae-vs-3.12.6.svg) | 1.031x ↑<br>[📄](results/bm-20250715-3.15.0a0-cb59eae-NOGIL/bm-20250715-macm4pro-arm64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae-vs-3.13.0rc2.md)[📈](results/bm-20250715-3.15.0a0-cb59eae-NOGIL/bm-20250715-macm4pro-arm64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae-vs-3.13.0rc2.svg) | 1.009x ↑<br>[📄](results/bm-20250715-3.15.0a0-cb59eae-NOGIL/bm-20250715-macm4pro-arm64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae-vs-base.md)[📈](results/bm-20250715-3.15.0a0-cb59eae-NOGIL/bm-20250715-macm4pro-arm64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae-vs-base.svg)[🧠](results/bm-20250715-3.15.0a0-cb59eae-NOGIL/bm-20250715-macm4pro-arm64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae-vs-base-mem.svg) |
| [2025-07-15](results/bm-20250715-3.15.0a0-cb59eae) | python/cb59eaefeda5ff44ac0c | cb59eae | 1.100x ↑<br>[📄](results/bm-20250715-3.15.0a0-cb59eae/bm-20250715-macm4pro-arm64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae-vs-3.12.6.md)[📈](results/bm-20250715-3.15.0a0-cb59eae/bm-20250715-macm4pro-arm64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae-vs-3.12.6.svg) | 1.021x ↑<br>[📄](results/bm-20250715-3.15.0a0-cb59eae/bm-20250715-macm4pro-arm64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae-vs-3.13.0rc2.md)[📈](results/bm-20250715-3.15.0a0-cb59eae/bm-20250715-macm4pro-arm64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae-vs-3.13.0rc2.svg) |  |


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
