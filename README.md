# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (e3287f6)](results/bm-20260815-3.16.0a0-e3287f6/bm-20260815-vultr-x86_64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (e3287f6)](results/bm-20260815-3.16.0a0-e3287f6-PYTHON_UOPS/bm-20260815-vultr-x86_64-python-e3287f631f3c88ed8019-3.16.0a0-e3287f6-pystats.md)
- [Most recent JIT pystats on main (bedaea0)](results/bm-20251019-3.15.0a1%2B-bedaea0-JIT/bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-08-20](results/bm-20260820-3.16.0a0-04242c0-NOGIL) | python/04242c027feeff726acb | 04242c0 (NOGIL) | 1.035x ↓<br>[📄](results/bm-20260820-3.16.0a0-04242c0-NOGIL/bm-20260820-vultr-x86_64-python-04242c027feeff726acb-3.16.0a0-04242c0-vs-3.12.6.md)[📈](results/bm-20260820-3.16.0a0-04242c0-NOGIL/bm-20260820-vultr-x86_64-python-04242c027feeff726acb-3.16.0a0-04242c0-vs-3.12.6.svg) | 1.067x ↓<br>[📄](results/bm-20260820-3.16.0a0-04242c0-NOGIL/bm-20260820-vultr-x86_64-python-04242c027feeff726acb-3.16.0a0-04242c0-vs-3.13.0rc2.md)[📈](results/bm-20260820-3.16.0a0-04242c0-NOGIL/bm-20260820-vultr-x86_64-python-04242c027feeff726acb-3.16.0a0-04242c0-vs-3.13.0rc2.svg) | 1.104x ↓<br>[📄](results/bm-20260820-3.16.0a0-04242c0-NOGIL/bm-20260820-vultr-x86_64-python-04242c027feeff726acb-3.16.0a0-04242c0-vs-base.md)[📈](results/bm-20260820-3.16.0a0-04242c0-NOGIL/bm-20260820-vultr-x86_64-python-04242c027feeff726acb-3.16.0a0-04242c0-vs-base.svg)[🧠](results/bm-20260820-3.16.0a0-04242c0-NOGIL/bm-20260820-vultr-x86_64-python-04242c027feeff726acb-3.16.0a0-04242c0-vs-base-mem.svg) |
| [2026-08-20](results/bm-20260820-3.16.0a0-04242c0) | python/04242c027feeff726acb | 04242c0 | 1.073x ↑<br>[📄](results/bm-20260820-3.16.0a0-04242c0/bm-20260820-vultr-x86_64-python-04242c027feeff726acb-3.16.0a0-04242c0-vs-3.12.6.md)[📈](results/bm-20260820-3.16.0a0-04242c0/bm-20260820-vultr-x86_64-python-04242c027feeff726acb-3.16.0a0-04242c0-vs-3.12.6.svg) | 1.038x ↑<br>[📄](results/bm-20260820-3.16.0a0-04242c0/bm-20260820-vultr-x86_64-python-04242c027feeff726acb-3.16.0a0-04242c0-vs-3.13.0rc2.md)[📈](results/bm-20260820-3.16.0a0-04242c0/bm-20260820-vultr-x86_64-python-04242c027feeff726acb-3.16.0a0-04242c0-vs-3.13.0rc2.svg) |  |
| [2026-08-19](results/bm-20260819-3.16.0a0-bf95881-NOGIL) | python/bf95881b84662d3dcd35 | bf95881 (NOGIL) | 1.035x ↓<br>[📄](results/bm-20260819-3.16.0a0-bf95881-NOGIL/bm-20260819-vultr-x86_64-python-bf95881b84662d3dcd35-3.16.0a0-bf95881-vs-3.12.6.md)[📈](results/bm-20260819-3.16.0a0-bf95881-NOGIL/bm-20260819-vultr-x86_64-python-bf95881b84662d3dcd35-3.16.0a0-bf95881-vs-3.12.6.svg) | 1.067x ↓<br>[📄](results/bm-20260819-3.16.0a0-bf95881-NOGIL/bm-20260819-vultr-x86_64-python-bf95881b84662d3dcd35-3.16.0a0-bf95881-vs-3.13.0rc2.md)[📈](results/bm-20260819-3.16.0a0-bf95881-NOGIL/bm-20260819-vultr-x86_64-python-bf95881b84662d3dcd35-3.16.0a0-bf95881-vs-3.13.0rc2.svg) | 1.099x ↓<br>[📄](results/bm-20260819-3.16.0a0-bf95881-NOGIL/bm-20260819-vultr-x86_64-python-bf95881b84662d3dcd35-3.16.0a0-bf95881-vs-base.md)[📈](results/bm-20260819-3.16.0a0-bf95881-NOGIL/bm-20260819-vultr-x86_64-python-bf95881b84662d3dcd35-3.16.0a0-bf95881-vs-base.svg)[🧠](results/bm-20260819-3.16.0a0-bf95881-NOGIL/bm-20260819-vultr-x86_64-python-bf95881b84662d3dcd35-3.16.0a0-bf95881-vs-base-mem.svg) |
| [2026-08-19](results/bm-20260819-3.16.0a0-bf95881) | python/bf95881b84662d3dcd35 | bf95881 | 1.066x ↑<br>[📄](results/bm-20260819-3.16.0a0-bf95881/bm-20260819-vultr-x86_64-python-bf95881b84662d3dcd35-3.16.0a0-bf95881-vs-3.12.6.md)[📈](results/bm-20260819-3.16.0a0-bf95881/bm-20260819-vultr-x86_64-python-bf95881b84662d3dcd35-3.16.0a0-bf95881-vs-3.12.6.svg) | 1.030x ↑<br>[📄](results/bm-20260819-3.16.0a0-bf95881/bm-20260819-vultr-x86_64-python-bf95881b84662d3dcd35-3.16.0a0-bf95881-vs-3.13.0rc2.md)[📈](results/bm-20260819-3.16.0a0-bf95881/bm-20260819-vultr-x86_64-python-bf95881b84662d3dcd35-3.16.0a0-bf95881-vs-3.13.0rc2.svg) |  |
| [2026-08-18](results/bm-20260818-3.16.0a0-af49df9-NOGIL) | python/af49df919dafc3767ae9 | af49df9 (NOGIL) | 1.036x ↓<br>[📄](results/bm-20260818-3.16.0a0-af49df9-NOGIL/bm-20260818-vultr-x86_64-python-af49df919dafc3767ae9-3.16.0a0-af49df9-vs-3.12.6.md)[📈](results/bm-20260818-3.16.0a0-af49df9-NOGIL/bm-20260818-vultr-x86_64-python-af49df919dafc3767ae9-3.16.0a0-af49df9-vs-3.12.6.svg) | 1.068x ↓<br>[📄](results/bm-20260818-3.16.0a0-af49df9-NOGIL/bm-20260818-vultr-x86_64-python-af49df919dafc3767ae9-3.16.0a0-af49df9-vs-3.13.0rc2.md)[📈](results/bm-20260818-3.16.0a0-af49df9-NOGIL/bm-20260818-vultr-x86_64-python-af49df919dafc3767ae9-3.16.0a0-af49df9-vs-3.13.0rc2.svg) | 1.105x ↓<br>[📄](results/bm-20260818-3.16.0a0-af49df9-NOGIL/bm-20260818-vultr-x86_64-python-af49df919dafc3767ae9-3.16.0a0-af49df9-vs-base.md)[📈](results/bm-20260818-3.16.0a0-af49df9-NOGIL/bm-20260818-vultr-x86_64-python-af49df919dafc3767ae9-3.16.0a0-af49df9-vs-base.svg)[🧠](results/bm-20260818-3.16.0a0-af49df9-NOGIL/bm-20260818-vultr-x86_64-python-af49df919dafc3767ae9-3.16.0a0-af49df9-vs-base-mem.svg) |
| [2026-08-18](results/bm-20260818-3.16.0a0-af49df9) | python/af49df919dafc3767ae9 | af49df9 | 1.072x ↑<br>[📄](results/bm-20260818-3.16.0a0-af49df9/bm-20260818-vultr-x86_64-python-af49df919dafc3767ae9-3.16.0a0-af49df9-vs-3.12.6.md)[📈](results/bm-20260818-3.16.0a0-af49df9/bm-20260818-vultr-x86_64-python-af49df919dafc3767ae9-3.16.0a0-af49df9-vs-3.12.6.svg) | 1.037x ↑<br>[📄](results/bm-20260818-3.16.0a0-af49df9/bm-20260818-vultr-x86_64-python-af49df919dafc3767ae9-3.16.0a0-af49df9-vs-3.13.0rc2.md)[📈](results/bm-20260818-3.16.0a0-af49df9/bm-20260818-vultr-x86_64-python-af49df919dafc3767ae9-3.16.0a0-af49df9-vs-3.13.0rc2.svg) |  |
| [2026-08-17](results/bm-20260817-3.16.0a0-a7bb524-NOGIL) | python/a7bb524fef61f77ede01 | a7bb524 (NOGIL) | 1.046x ↓<br>[📄](results/bm-20260817-3.16.0a0-a7bb524-NOGIL/bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524-vs-3.12.6.md)[📈](results/bm-20260817-3.16.0a0-a7bb524-NOGIL/bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524-vs-3.12.6.svg) | 1.077x ↓<br>[📄](results/bm-20260817-3.16.0a0-a7bb524-NOGIL/bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524-vs-3.13.0rc2.md)[📈](results/bm-20260817-3.16.0a0-a7bb524-NOGIL/bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524-vs-3.13.0rc2.svg) | 1.110x ↓<br>[📄](results/bm-20260817-3.16.0a0-a7bb524-NOGIL/bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524-vs-base.md)[📈](results/bm-20260817-3.16.0a0-a7bb524-NOGIL/bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524-vs-base.svg)[🧠](results/bm-20260817-3.16.0a0-a7bb524-NOGIL/bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524-vs-base-mem.svg) |
| [2026-08-17](results/bm-20260817-3.16.0a0-a7bb524) | python/a7bb524fef61f77ede01 | a7bb524 | 1.069x ↑<br>[📄](results/bm-20260817-3.16.0a0-a7bb524/bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524-vs-3.12.6.md)[📈](results/bm-20260817-3.16.0a0-a7bb524/bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524-vs-3.12.6.svg) | 1.033x ↑<br>[📄](results/bm-20260817-3.16.0a0-a7bb524/bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524-vs-3.13.0rc2.md)[📈](results/bm-20260817-3.16.0a0-a7bb524/bm-20260817-vultr-x86_64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-08-20](results/bm-20260820-3.16.0a0-04242c0-NOGIL) | python/04242c027feeff726acb | 04242c0 (NOGIL) | 1.010x ↑<br>[📄](results/bm-20260820-3.16.0a0-04242c0-NOGIL/bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0-vs-3.12.6.md)[📈](results/bm-20260820-3.16.0a0-04242c0-NOGIL/bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0-vs-3.12.6.svg) | 1.064x ↓<br>[📄](results/bm-20260820-3.16.0a0-04242c0-NOGIL/bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0-vs-3.13.0rc2.md)[📈](results/bm-20260820-3.16.0a0-04242c0-NOGIL/bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0-vs-3.13.0rc2.svg) | 1.106x ↓<br>[📄](results/bm-20260820-3.16.0a0-04242c0-NOGIL/bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0-vs-base.md)[📈](results/bm-20260820-3.16.0a0-04242c0-NOGIL/bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0-vs-base.svg)[🧠](results/bm-20260820-3.16.0a0-04242c0-NOGIL/bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0-vs-base-mem.svg) |
| [2026-08-20](results/bm-20260820-3.16.0a0-04242c0) | python/04242c027feeff726acb | 04242c0 | 1.132x ↑<br>[📄](results/bm-20260820-3.16.0a0-04242c0/bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0-vs-3.12.6.md)[📈](results/bm-20260820-3.16.0a0-04242c0/bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0-vs-3.12.6.svg) | 1.044x ↑<br>[📄](results/bm-20260820-3.16.0a0-04242c0/bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0-vs-3.13.0rc2.md)[📈](results/bm-20260820-3.16.0a0-04242c0/bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0-vs-3.13.0rc2.svg) |  |
| [2026-08-19](results/bm-20260819-3.16.0a0-bf95881-NOGIL) | python/bf95881b84662d3dcd35 | bf95881 (NOGIL) | 1.012x ↑<br>[📄](results/bm-20260819-3.16.0a0-bf95881-NOGIL/bm-20260819-macm4pro-arm64-python-bf95881b84662d3dcd35-3.16.0a0-bf95881-vs-3.12.6.md)[📈](results/bm-20260819-3.16.0a0-bf95881-NOGIL/bm-20260819-macm4pro-arm64-python-bf95881b84662d3dcd35-3.16.0a0-bf95881-vs-3.12.6.svg) | 1.063x ↓<br>[📄](results/bm-20260819-3.16.0a0-bf95881-NOGIL/bm-20260819-macm4pro-arm64-python-bf95881b84662d3dcd35-3.16.0a0-bf95881-vs-3.13.0rc2.md)[📈](results/bm-20260819-3.16.0a0-bf95881-NOGIL/bm-20260819-macm4pro-arm64-python-bf95881b84662d3dcd35-3.16.0a0-bf95881-vs-3.13.0rc2.svg) | 1.104x ↓<br>[📄](results/bm-20260819-3.16.0a0-bf95881-NOGIL/bm-20260819-macm4pro-arm64-python-bf95881b84662d3dcd35-3.16.0a0-bf95881-vs-base.md)[📈](results/bm-20260819-3.16.0a0-bf95881-NOGIL/bm-20260819-macm4pro-arm64-python-bf95881b84662d3dcd35-3.16.0a0-bf95881-vs-base.svg)[🧠](results/bm-20260819-3.16.0a0-bf95881-NOGIL/bm-20260819-macm4pro-arm64-python-bf95881b84662d3dcd35-3.16.0a0-bf95881-vs-base-mem.svg) |
| [2026-08-19](results/bm-20260819-3.16.0a0-bf95881) | python/bf95881b84662d3dcd35 | bf95881 | 1.132x ↑<br>[📄](results/bm-20260819-3.16.0a0-bf95881/bm-20260819-macm4pro-arm64-python-bf95881b84662d3dcd35-3.16.0a0-bf95881-vs-3.12.6.md)[📈](results/bm-20260819-3.16.0a0-bf95881/bm-20260819-macm4pro-arm64-python-bf95881b84662d3dcd35-3.16.0a0-bf95881-vs-3.12.6.svg) | 1.046x ↑<br>[📄](results/bm-20260819-3.16.0a0-bf95881/bm-20260819-macm4pro-arm64-python-bf95881b84662d3dcd35-3.16.0a0-bf95881-vs-3.13.0rc2.md)[📈](results/bm-20260819-3.16.0a0-bf95881/bm-20260819-macm4pro-arm64-python-bf95881b84662d3dcd35-3.16.0a0-bf95881-vs-3.13.0rc2.svg) |  |
| [2026-08-18](results/bm-20260818-3.16.0a0-af49df9-NOGIL) | python/af49df919dafc3767ae9 | af49df9 (NOGIL) | 1.013x ↑<br>[📄](results/bm-20260818-3.16.0a0-af49df9-NOGIL/bm-20260818-macm4pro-arm64-python-af49df919dafc3767ae9-3.16.0a0-af49df9-vs-3.12.6.md)[📈](results/bm-20260818-3.16.0a0-af49df9-NOGIL/bm-20260818-macm4pro-arm64-python-af49df919dafc3767ae9-3.16.0a0-af49df9-vs-3.12.6.svg) | 1.061x ↓<br>[📄](results/bm-20260818-3.16.0a0-af49df9-NOGIL/bm-20260818-macm4pro-arm64-python-af49df919dafc3767ae9-3.16.0a0-af49df9-vs-3.13.0rc2.md)[📈](results/bm-20260818-3.16.0a0-af49df9-NOGIL/bm-20260818-macm4pro-arm64-python-af49df919dafc3767ae9-3.16.0a0-af49df9-vs-3.13.0rc2.svg) | 1.103x ↓<br>[📄](results/bm-20260818-3.16.0a0-af49df9-NOGIL/bm-20260818-macm4pro-arm64-python-af49df919dafc3767ae9-3.16.0a0-af49df9-vs-base.md)[📈](results/bm-20260818-3.16.0a0-af49df9-NOGIL/bm-20260818-macm4pro-arm64-python-af49df919dafc3767ae9-3.16.0a0-af49df9-vs-base.svg)[🧠](results/bm-20260818-3.16.0a0-af49df9-NOGIL/bm-20260818-macm4pro-arm64-python-af49df919dafc3767ae9-3.16.0a0-af49df9-vs-base-mem.svg) |
| [2026-08-18](results/bm-20260818-3.16.0a0-af49df9) | python/af49df919dafc3767ae9 | af49df9 | 1.131x ↑<br>[📄](results/bm-20260818-3.16.0a0-af49df9/bm-20260818-macm4pro-arm64-python-af49df919dafc3767ae9-3.16.0a0-af49df9-vs-3.12.6.md)[📈](results/bm-20260818-3.16.0a0-af49df9/bm-20260818-macm4pro-arm64-python-af49df919dafc3767ae9-3.16.0a0-af49df9-vs-3.12.6.svg) | 1.044x ↑<br>[📄](results/bm-20260818-3.16.0a0-af49df9/bm-20260818-macm4pro-arm64-python-af49df919dafc3767ae9-3.16.0a0-af49df9-vs-3.13.0rc2.md)[📈](results/bm-20260818-3.16.0a0-af49df9/bm-20260818-macm4pro-arm64-python-af49df919dafc3767ae9-3.16.0a0-af49df9-vs-3.13.0rc2.svg) |  |
| [2026-08-17](results/bm-20260817-3.16.0a0-a7bb524-NOGIL) | python/a7bb524fef61f77ede01 | a7bb524 (NOGIL) | 1.015x ↑<br>[📄](results/bm-20260817-3.16.0a0-a7bb524-NOGIL/bm-20260817-macm4pro-arm64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524-vs-3.12.6.md)[📈](results/bm-20260817-3.16.0a0-a7bb524-NOGIL/bm-20260817-macm4pro-arm64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524-vs-3.12.6.svg) | 1.060x ↓<br>[📄](results/bm-20260817-3.16.0a0-a7bb524-NOGIL/bm-20260817-macm4pro-arm64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524-vs-3.13.0rc2.md)[📈](results/bm-20260817-3.16.0a0-a7bb524-NOGIL/bm-20260817-macm4pro-arm64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524-vs-3.13.0rc2.svg) | 1.098x ↓<br>[📄](results/bm-20260817-3.16.0a0-a7bb524-NOGIL/bm-20260817-macm4pro-arm64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524-vs-base.md)[📈](results/bm-20260817-3.16.0a0-a7bb524-NOGIL/bm-20260817-macm4pro-arm64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524-vs-base.svg)[🧠](results/bm-20260817-3.16.0a0-a7bb524-NOGIL/bm-20260817-macm4pro-arm64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524-vs-base-mem.svg) |
| [2026-08-17](results/bm-20260817-3.16.0a0-a7bb524) | python/a7bb524fef61f77ede01 | a7bb524 | 1.127x ↑<br>[📄](results/bm-20260817-3.16.0a0-a7bb524/bm-20260817-macm4pro-arm64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524-vs-3.12.6.md)[📈](results/bm-20260817-3.16.0a0-a7bb524/bm-20260817-macm4pro-arm64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524-vs-3.12.6.svg) | 1.041x ↑<br>[📄](results/bm-20260817-3.16.0a0-a7bb524/bm-20260817-macm4pro-arm64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524-vs-3.13.0rc2.md)[📈](results/bm-20260817-3.16.0a0-a7bb524/bm-20260817-macm4pro-arm64-python-a7bb524fef61f77ede01-3.16.0a0-a7bb524-vs-3.13.0rc2.svg) |  |


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
