# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (801cf3f)](results/bm-20250802-3.15.0a0-801cf3f/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (801cf3f)](results/bm-20250802-3.15.0a0-801cf3f-PYTHON_UOPS/bm-20250802-vultr-x86_64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-08-06](results/bm-20250806-3.15.0a0-3000594-NOGIL) | python/3000594e929aea768fe0 | 3000594 (NOGIL) | 1.026x ↓<br>[📄](results/bm-20250806-3.15.0a0-3000594-NOGIL/bm-20250806-vultr-x86_64-python-3000594e929aea768fe0-3.15.0a0-3000594-vs-3.12.6.md)[📈](results/bm-20250806-3.15.0a0-3000594-NOGIL/bm-20250806-vultr-x86_64-python-3000594e929aea768fe0-3.15.0a0-3000594-vs-3.12.6.svg) | 1.059x ↓<br>[📄](results/bm-20250806-3.15.0a0-3000594-NOGIL/bm-20250806-vultr-x86_64-python-3000594e929aea768fe0-3.15.0a0-3000594-vs-3.13.0rc2.md)[📈](results/bm-20250806-3.15.0a0-3000594-NOGIL/bm-20250806-vultr-x86_64-python-3000594e929aea768fe0-3.15.0a0-3000594-vs-3.13.0rc2.svg) | 1.092x ↓<br>[📄](results/bm-20250806-3.15.0a0-3000594-NOGIL/bm-20250806-vultr-x86_64-python-3000594e929aea768fe0-3.15.0a0-3000594-vs-base.md)[📈](results/bm-20250806-3.15.0a0-3000594-NOGIL/bm-20250806-vultr-x86_64-python-3000594e929aea768fe0-3.15.0a0-3000594-vs-base.svg)[🧠](results/bm-20250806-3.15.0a0-3000594-NOGIL/bm-20250806-vultr-x86_64-python-3000594e929aea768fe0-3.15.0a0-3000594-vs-base-mem.svg) |
| [2025-08-06](results/bm-20250806-3.15.0a0-3000594) | python/3000594e929aea768fe0 | 3000594 | 1.065x ↑<br>[📄](results/bm-20250806-3.15.0a0-3000594/bm-20250806-vultr-x86_64-python-3000594e929aea768fe0-3.15.0a0-3000594-vs-3.12.6.md)[📈](results/bm-20250806-3.15.0a0-3000594/bm-20250806-vultr-x86_64-python-3000594e929aea768fe0-3.15.0a0-3000594-vs-3.12.6.svg) | 1.030x ↑<br>[📄](results/bm-20250806-3.15.0a0-3000594/bm-20250806-vultr-x86_64-python-3000594e929aea768fe0-3.15.0a0-3000594-vs-3.13.0rc2.md)[📈](results/bm-20250806-3.15.0a0-3000594/bm-20250806-vultr-x86_64-python-3000594e929aea768fe0-3.15.0a0-3000594-vs-3.13.0rc2.svg) |  |
| [2025-08-05](results/bm-20250805-3.15.0a0-c2428ca-NOGIL) | python/c2428ca9ea0c4eac9c7f | c2428ca (NOGIL) | 1.028x ↓<br>[📄](results/bm-20250805-3.15.0a0-c2428ca-NOGIL/bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca-vs-3.12.6.md)[📈](results/bm-20250805-3.15.0a0-c2428ca-NOGIL/bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca-vs-3.12.6.svg) | 1.061x ↓<br>[📄](results/bm-20250805-3.15.0a0-c2428ca-NOGIL/bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca-vs-3.13.0rc2.md)[📈](results/bm-20250805-3.15.0a0-c2428ca-NOGIL/bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca-vs-3.13.0rc2.svg) | 1.093x ↓<br>[📄](results/bm-20250805-3.15.0a0-c2428ca-NOGIL/bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca-vs-base.md)[📈](results/bm-20250805-3.15.0a0-c2428ca-NOGIL/bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca-vs-base.svg)[🧠](results/bm-20250805-3.15.0a0-c2428ca-NOGIL/bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca-vs-base-mem.svg) |
| [2025-08-05](results/bm-20250805-3.15.0a0-c2428ca) | python/c2428ca9ea0c4eac9c7f | c2428ca | 1.065x ↑<br>[📄](results/bm-20250805-3.15.0a0-c2428ca/bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca-vs-3.12.6.md)[📈](results/bm-20250805-3.15.0a0-c2428ca/bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca-vs-3.12.6.svg) | 1.029x ↑<br>[📄](results/bm-20250805-3.15.0a0-c2428ca/bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca-vs-3.13.0rc2.md)[📈](results/bm-20250805-3.15.0a0-c2428ca/bm-20250805-vultr-x86_64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca-vs-3.13.0rc2.svg) |  |
| [2025-08-04](results/bm-20250804-3.15.0a0-001461a-NOGIL) | python/001461a29235216eb9c8 | 001461a (NOGIL) | 1.025x ↓<br>[📄](results/bm-20250804-3.15.0a0-001461a-NOGIL/bm-20250804-vultr-x86_64-python-001461a29235216eb9c8-3.15.0a0-001461a-vs-3.12.6.md)[📈](results/bm-20250804-3.15.0a0-001461a-NOGIL/bm-20250804-vultr-x86_64-python-001461a29235216eb9c8-3.15.0a0-001461a-vs-3.12.6.svg) | 1.058x ↓<br>[📄](results/bm-20250804-3.15.0a0-001461a-NOGIL/bm-20250804-vultr-x86_64-python-001461a29235216eb9c8-3.15.0a0-001461a-vs-3.13.0rc2.md)[📈](results/bm-20250804-3.15.0a0-001461a-NOGIL/bm-20250804-vultr-x86_64-python-001461a29235216eb9c8-3.15.0a0-001461a-vs-3.13.0rc2.svg) | 1.086x ↓<br>[📄](results/bm-20250804-3.15.0a0-001461a-NOGIL/bm-20250804-vultr-x86_64-python-001461a29235216eb9c8-3.15.0a0-001461a-vs-base.md)[📈](results/bm-20250804-3.15.0a0-001461a-NOGIL/bm-20250804-vultr-x86_64-python-001461a29235216eb9c8-3.15.0a0-001461a-vs-base.svg)[🧠](results/bm-20250804-3.15.0a0-001461a-NOGIL/bm-20250804-vultr-x86_64-python-001461a29235216eb9c8-3.15.0a0-001461a-vs-base-mem.svg) |
| [2025-08-04](results/bm-20250804-3.15.0a0-001461a) | python/001461a29235216eb9c8 | 001461a | 1.059x ↑<br>[📄](results/bm-20250804-3.15.0a0-001461a/bm-20250804-vultr-x86_64-python-001461a29235216eb9c8-3.15.0a0-001461a-vs-3.12.6.md)[📈](results/bm-20250804-3.15.0a0-001461a/bm-20250804-vultr-x86_64-python-001461a29235216eb9c8-3.15.0a0-001461a-vs-3.12.6.svg) | 1.024x ↑<br>[📄](results/bm-20250804-3.15.0a0-001461a/bm-20250804-vultr-x86_64-python-001461a29235216eb9c8-3.15.0a0-001461a-vs-3.13.0rc2.md)[📈](results/bm-20250804-3.15.0a0-001461a/bm-20250804-vultr-x86_64-python-001461a29235216eb9c8-3.15.0a0-001461a-vs-3.13.0rc2.svg) |  |
| [2025-08-03](results/bm-20250803-3.15.0a0-406dc71-NOGIL) | python/406dc714f6b4dbc18d4e | 406dc71 (NOGIL) | 1.022x ↓<br>[📄](results/bm-20250803-3.15.0a0-406dc71-NOGIL/bm-20250803-vultr-x86_64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71-vs-3.12.6.md)[📈](results/bm-20250803-3.15.0a0-406dc71-NOGIL/bm-20250803-vultr-x86_64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71-vs-3.12.6.svg) | 1.055x ↓<br>[📄](results/bm-20250803-3.15.0a0-406dc71-NOGIL/bm-20250803-vultr-x86_64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71-vs-3.13.0rc2.md)[📈](results/bm-20250803-3.15.0a0-406dc71-NOGIL/bm-20250803-vultr-x86_64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71-vs-3.13.0rc2.svg) | 1.091x ↓<br>[📄](results/bm-20250803-3.15.0a0-406dc71-NOGIL/bm-20250803-vultr-x86_64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71-vs-base.md)[📈](results/bm-20250803-3.15.0a0-406dc71-NOGIL/bm-20250803-vultr-x86_64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71-vs-base.svg)[🧠](results/bm-20250803-3.15.0a0-406dc71-NOGIL/bm-20250803-vultr-x86_64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71-vs-base-mem.svg) |
| [2025-08-03](results/bm-20250803-3.15.0a0-406dc71) | python/406dc714f6b4dbc18d4e | 406dc71 | 1.069x ↑<br>[📄](results/bm-20250803-3.15.0a0-406dc71/bm-20250803-vultr-x86_64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71-vs-3.12.6.md)[📈](results/bm-20250803-3.15.0a0-406dc71/bm-20250803-vultr-x86_64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71-vs-3.12.6.svg) | 1.033x ↑<br>[📄](results/bm-20250803-3.15.0a0-406dc71/bm-20250803-vultr-x86_64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71-vs-3.13.0rc2.md)[📈](results/bm-20250803-3.15.0a0-406dc71/bm-20250803-vultr-x86_64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-08-06](results/bm-20250806-3.15.0a0-3000594-NOGIL) | python/3000594e929aea768fe0 | 3000594 (NOGIL) | 1.073x ↑<br>[📄](results/bm-20250806-3.15.0a0-3000594-NOGIL/bm-20250806-macm4pro-arm64-python-3000594e929aea768fe0-3.15.0a0-3000594-vs-3.12.6.md)[📈](results/bm-20250806-3.15.0a0-3000594-NOGIL/bm-20250806-macm4pro-arm64-python-3000594e929aea768fe0-3.15.0a0-3000594-vs-3.12.6.svg) | 1.005x ↓<br>[📄](results/bm-20250806-3.15.0a0-3000594-NOGIL/bm-20250806-macm4pro-arm64-python-3000594e929aea768fe0-3.15.0a0-3000594-vs-3.13.0rc2.md)[📈](results/bm-20250806-3.15.0a0-3000594-NOGIL/bm-20250806-macm4pro-arm64-python-3000594e929aea768fe0-3.15.0a0-3000594-vs-3.13.0rc2.svg) | 1.027x ↓<br>[📄](results/bm-20250806-3.15.0a0-3000594-NOGIL/bm-20250806-macm4pro-arm64-python-3000594e929aea768fe0-3.15.0a0-3000594-vs-base.md)[📈](results/bm-20250806-3.15.0a0-3000594-NOGIL/bm-20250806-macm4pro-arm64-python-3000594e929aea768fe0-3.15.0a0-3000594-vs-base.svg)[🧠](results/bm-20250806-3.15.0a0-3000594-NOGIL/bm-20250806-macm4pro-arm64-python-3000594e929aea768fe0-3.15.0a0-3000594-vs-base-mem.svg) |
| [2025-08-06](results/bm-20250806-3.15.0a0-3000594) | python/3000594e929aea768fe0 | 3000594 | 1.100x ↑<br>[📄](results/bm-20250806-3.15.0a0-3000594/bm-20250806-macm4pro-arm64-python-3000594e929aea768fe0-3.15.0a0-3000594-vs-3.12.6.md)[📈](results/bm-20250806-3.15.0a0-3000594/bm-20250806-macm4pro-arm64-python-3000594e929aea768fe0-3.15.0a0-3000594-vs-3.12.6.svg) | 1.020x ↑<br>[📄](results/bm-20250806-3.15.0a0-3000594/bm-20250806-macm4pro-arm64-python-3000594e929aea768fe0-3.15.0a0-3000594-vs-3.13.0rc2.md)[📈](results/bm-20250806-3.15.0a0-3000594/bm-20250806-macm4pro-arm64-python-3000594e929aea768fe0-3.15.0a0-3000594-vs-3.13.0rc2.svg) |  |
| [2025-08-05](results/bm-20250805-3.15.0a0-c2428ca-NOGIL) | python/c2428ca9ea0c4eac9c7f | c2428ca (NOGIL) | 1.082x ↑<br>[📄](results/bm-20250805-3.15.0a0-c2428ca-NOGIL/bm-20250805-macm4pro-arm64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca-vs-3.12.6.md)[📈](results/bm-20250805-3.15.0a0-c2428ca-NOGIL/bm-20250805-macm4pro-arm64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca-vs-3.12.6.svg) | 1.004x ↑<br>[📄](results/bm-20250805-3.15.0a0-c2428ca-NOGIL/bm-20250805-macm4pro-arm64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca-vs-3.13.0rc2.md)[📈](results/bm-20250805-3.15.0a0-c2428ca-NOGIL/bm-20250805-macm4pro-arm64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca-vs-3.13.0rc2.svg) | 1.015x ↓<br>[📄](results/bm-20250805-3.15.0a0-c2428ca-NOGIL/bm-20250805-macm4pro-arm64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca-vs-base.md)[📈](results/bm-20250805-3.15.0a0-c2428ca-NOGIL/bm-20250805-macm4pro-arm64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca-vs-base.svg)[🧠](results/bm-20250805-3.15.0a0-c2428ca-NOGIL/bm-20250805-macm4pro-arm64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca-vs-base-mem.svg) |
| [2025-08-05](results/bm-20250805-3.15.0a0-c2428ca) | python/c2428ca9ea0c4eac9c7f | c2428ca | 1.097x ↑<br>[📄](results/bm-20250805-3.15.0a0-c2428ca/bm-20250805-macm4pro-arm64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca-vs-3.12.6.md)[📈](results/bm-20250805-3.15.0a0-c2428ca/bm-20250805-macm4pro-arm64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca-vs-3.12.6.svg) | 1.018x ↑<br>[📄](results/bm-20250805-3.15.0a0-c2428ca/bm-20250805-macm4pro-arm64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca-vs-3.13.0rc2.md)[📈](results/bm-20250805-3.15.0a0-c2428ca/bm-20250805-macm4pro-arm64-python-c2428ca9ea0c4eac9c7f-3.15.0a0-c2428ca-vs-3.13.0rc2.svg) |  |
| [2025-08-04](results/bm-20250804-3.15.0a0-001461a-NOGIL) | python/001461a29235216eb9c8 | 001461a (NOGIL) | 1.094x ↑<br>[📄](results/bm-20250804-3.15.0a0-001461a-NOGIL/bm-20250804-macm4pro-arm64-python-001461a29235216eb9c8-3.15.0a0-001461a-vs-3.12.6.md)[📈](results/bm-20250804-3.15.0a0-001461a-NOGIL/bm-20250804-macm4pro-arm64-python-001461a29235216eb9c8-3.15.0a0-001461a-vs-3.12.6.svg) | 1.015x ↑<br>[📄](results/bm-20250804-3.15.0a0-001461a-NOGIL/bm-20250804-macm4pro-arm64-python-001461a29235216eb9c8-3.15.0a0-001461a-vs-3.13.0rc2.md)[📈](results/bm-20250804-3.15.0a0-001461a-NOGIL/bm-20250804-macm4pro-arm64-python-001461a29235216eb9c8-3.15.0a0-001461a-vs-3.13.0rc2.svg) |  |
| [2025-08-03](results/bm-20250803-3.15.0a0-406dc71-NOGIL) | python/406dc714f6b4dbc18d4e | 406dc71 (NOGIL) | 1.087x ↑<br>[📄](results/bm-20250803-3.15.0a0-406dc71-NOGIL/bm-20250803-macm4pro-arm64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71-vs-3.12.6.md)[📈](results/bm-20250803-3.15.0a0-406dc71-NOGIL/bm-20250803-macm4pro-arm64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71-vs-3.12.6.svg) | 1.008x ↑<br>[📄](results/bm-20250803-3.15.0a0-406dc71-NOGIL/bm-20250803-macm4pro-arm64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71-vs-3.13.0rc2.md)[📈](results/bm-20250803-3.15.0a0-406dc71-NOGIL/bm-20250803-macm4pro-arm64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71-vs-3.13.0rc2.svg) | 1.017x ↓<br>[📄](results/bm-20250803-3.15.0a0-406dc71-NOGIL/bm-20250803-macm4pro-arm64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71-vs-base.md)[📈](results/bm-20250803-3.15.0a0-406dc71-NOGIL/bm-20250803-macm4pro-arm64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71-vs-base.svg)[🧠](results/bm-20250803-3.15.0a0-406dc71-NOGIL/bm-20250803-macm4pro-arm64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71-vs-base-mem.svg) |
| [2025-08-03](results/bm-20250803-3.15.0a0-406dc71) | python/406dc714f6b4dbc18d4e | 406dc71 | 1.103x ↑<br>[📄](results/bm-20250803-3.15.0a0-406dc71/bm-20250803-macm4pro-arm64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71-vs-3.12.6.md)[📈](results/bm-20250803-3.15.0a0-406dc71/bm-20250803-macm4pro-arm64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71-vs-3.12.6.svg) | 1.024x ↑<br>[📄](results/bm-20250803-3.15.0a0-406dc71/bm-20250803-macm4pro-arm64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71-vs-3.13.0rc2.md)[📈](results/bm-20250803-3.15.0a0-406dc71/bm-20250803-macm4pro-arm64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71-vs-3.13.0rc2.svg) |  |


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
