# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (6fcac09)](results/bm-20250823-3.15.0a0-6fcac09/bm-20250823-vultr-x86_64-python-6fcac09401e336b25833-3.15.0a0-6fcac09-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (6fcac09)](results/bm-20250823-3.15.0a0-6fcac09-PYTHON_UOPS/bm-20250823-vultr-x86_64-python-6fcac09401e336b25833-3.15.0a0-6fcac09-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-08-29](results/bm-20250829-3.15.0a0-e05182f-NOGIL) | python/e05182f98ea100b6e267 | e05182f (NOGIL) | 1.034x ↓<br>[📄](results/bm-20250829-3.15.0a0-e05182f-NOGIL/bm-20250829-vultr-x86_64-python-e05182f98ea100b6e267-3.15.0a0-e05182f-vs-3.12.6.md)[📈](results/bm-20250829-3.15.0a0-e05182f-NOGIL/bm-20250829-vultr-x86_64-python-e05182f98ea100b6e267-3.15.0a0-e05182f-vs-3.12.6.svg) | 1.066x ↓<br>[📄](results/bm-20250829-3.15.0a0-e05182f-NOGIL/bm-20250829-vultr-x86_64-python-e05182f98ea100b6e267-3.15.0a0-e05182f-vs-3.13.0rc2.md)[📈](results/bm-20250829-3.15.0a0-e05182f-NOGIL/bm-20250829-vultr-x86_64-python-e05182f98ea100b6e267-3.15.0a0-e05182f-vs-3.13.0rc2.svg) | 1.101x ↓<br>[📄](results/bm-20250829-3.15.0a0-e05182f-NOGIL/bm-20250829-vultr-x86_64-python-e05182f98ea100b6e267-3.15.0a0-e05182f-vs-base.md)[📈](results/bm-20250829-3.15.0a0-e05182f-NOGIL/bm-20250829-vultr-x86_64-python-e05182f98ea100b6e267-3.15.0a0-e05182f-vs-base.svg)[🧠](results/bm-20250829-3.15.0a0-e05182f-NOGIL/bm-20250829-vultr-x86_64-python-e05182f98ea100b6e267-3.15.0a0-e05182f-vs-base-mem.svg) |
| [2025-08-29](results/bm-20250829-3.15.0a0-e05182f) | python/e05182f98ea100b6e267 | e05182f | 1.069x ↑<br>[📄](results/bm-20250829-3.15.0a0-e05182f/bm-20250829-vultr-x86_64-python-e05182f98ea100b6e267-3.15.0a0-e05182f-vs-3.12.6.md)[📈](results/bm-20250829-3.15.0a0-e05182f/bm-20250829-vultr-x86_64-python-e05182f98ea100b6e267-3.15.0a0-e05182f-vs-3.12.6.svg) | 1.034x ↑<br>[📄](results/bm-20250829-3.15.0a0-e05182f/bm-20250829-vultr-x86_64-python-e05182f98ea100b6e267-3.15.0a0-e05182f-vs-3.13.0rc2.md)[📈](results/bm-20250829-3.15.0a0-e05182f/bm-20250829-vultr-x86_64-python-e05182f98ea100b6e267-3.15.0a0-e05182f-vs-3.13.0rc2.svg) |  |
| [2025-08-28](results/bm-20250828-3.15.0a0-c779f23-NOGIL) | python/c779f2324df06563b4ba | c779f23 (NOGIL) | 1.021x ↓<br>[📄](results/bm-20250828-3.15.0a0-c779f23-NOGIL/bm-20250828-vultr-x86_64-python-c779f2324df06563b4ba-3.15.0a0-c779f23-vs-3.12.6.md)[📈](results/bm-20250828-3.15.0a0-c779f23-NOGIL/bm-20250828-vultr-x86_64-python-c779f2324df06563b4ba-3.15.0a0-c779f23-vs-3.12.6.svg) | 1.055x ↓<br>[📄](results/bm-20250828-3.15.0a0-c779f23-NOGIL/bm-20250828-vultr-x86_64-python-c779f2324df06563b4ba-3.15.0a0-c779f23-vs-3.13.0rc2.md)[📈](results/bm-20250828-3.15.0a0-c779f23-NOGIL/bm-20250828-vultr-x86_64-python-c779f2324df06563b4ba-3.15.0a0-c779f23-vs-3.13.0rc2.svg) | 1.092x ↓<br>[📄](results/bm-20250828-3.15.0a0-c779f23-NOGIL/bm-20250828-vultr-x86_64-python-c779f2324df06563b4ba-3.15.0a0-c779f23-vs-base.md)[📈](results/bm-20250828-3.15.0a0-c779f23-NOGIL/bm-20250828-vultr-x86_64-python-c779f2324df06563b4ba-3.15.0a0-c779f23-vs-base.svg)[🧠](results/bm-20250828-3.15.0a0-c779f23-NOGIL/bm-20250828-vultr-x86_64-python-c779f2324df06563b4ba-3.15.0a0-c779f23-vs-base-mem.svg) |
| [2025-08-28](results/bm-20250828-3.15.0a0-c779f23) | python/c779f2324df06563b4ba | c779f23 | 1.071x ↑<br>[📄](results/bm-20250828-3.15.0a0-c779f23/bm-20250828-vultr-x86_64-python-c779f2324df06563b4ba-3.15.0a0-c779f23-vs-3.12.6.md)[📈](results/bm-20250828-3.15.0a0-c779f23/bm-20250828-vultr-x86_64-python-c779f2324df06563b4ba-3.15.0a0-c779f23-vs-3.12.6.svg) | 1.035x ↑<br>[📄](results/bm-20250828-3.15.0a0-c779f23/bm-20250828-vultr-x86_64-python-c779f2324df06563b4ba-3.15.0a0-c779f23-vs-3.13.0rc2.md)[📈](results/bm-20250828-3.15.0a0-c779f23/bm-20250828-vultr-x86_64-python-c779f2324df06563b4ba-3.15.0a0-c779f23-vs-3.13.0rc2.svg) |  |
| [2025-08-27](results/bm-20250827-3.15.0a0-d910b93-NOGIL) | python/d910b93f786982a11d7d | d910b93 (NOGIL) | 1.027x ↓<br>[📄](results/bm-20250827-3.15.0a0-d910b93-NOGIL/bm-20250827-vultr-x86_64-python-d910b93f786982a11d7d-3.15.0a0-d910b93-vs-3.12.6.md)[📈](results/bm-20250827-3.15.0a0-d910b93-NOGIL/bm-20250827-vultr-x86_64-python-d910b93f786982a11d7d-3.15.0a0-d910b93-vs-3.12.6.svg) | 1.059x ↓<br>[📄](results/bm-20250827-3.15.0a0-d910b93-NOGIL/bm-20250827-vultr-x86_64-python-d910b93f786982a11d7d-3.15.0a0-d910b93-vs-3.13.0rc2.md)[📈](results/bm-20250827-3.15.0a0-d910b93-NOGIL/bm-20250827-vultr-x86_64-python-d910b93f786982a11d7d-3.15.0a0-d910b93-vs-3.13.0rc2.svg) | 1.099x ↓<br>[📄](results/bm-20250827-3.15.0a0-d910b93-NOGIL/bm-20250827-vultr-x86_64-python-d910b93f786982a11d7d-3.15.0a0-d910b93-vs-base.md)[📈](results/bm-20250827-3.15.0a0-d910b93-NOGIL/bm-20250827-vultr-x86_64-python-d910b93f786982a11d7d-3.15.0a0-d910b93-vs-base.svg)[🧠](results/bm-20250827-3.15.0a0-d910b93-NOGIL/bm-20250827-vultr-x86_64-python-d910b93f786982a11d7d-3.15.0a0-d910b93-vs-base-mem.svg) |
| [2025-08-27](results/bm-20250827-3.15.0a0-d910b93) | python/d910b93f786982a11d7d | d910b93 | 1.074x ↑<br>[📄](results/bm-20250827-3.15.0a0-d910b93/bm-20250827-vultr-x86_64-python-d910b93f786982a11d7d-3.15.0a0-d910b93-vs-3.12.6.md)[📈](results/bm-20250827-3.15.0a0-d910b93/bm-20250827-vultr-x86_64-python-d910b93f786982a11d7d-3.15.0a0-d910b93-vs-3.12.6.svg) | 1.038x ↑<br>[📄](results/bm-20250827-3.15.0a0-d910b93/bm-20250827-vultr-x86_64-python-d910b93f786982a11d7d-3.15.0a0-d910b93-vs-3.13.0rc2.md)[📈](results/bm-20250827-3.15.0a0-d910b93/bm-20250827-vultr-x86_64-python-d910b93f786982a11d7d-3.15.0a0-d910b93-vs-3.13.0rc2.svg) |  |
| [2025-08-27](results/bm-20250827-3.15.0a0-ffaec6e-NOGIL) | python/ffaec6e2a11fb7b41fac | ffaec6e (NOGIL) | 1.022x ↓<br>[📄](results/bm-20250827-3.15.0a0-ffaec6e-NOGIL/bm-20250827-vultr-x86_64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e-vs-3.12.6.md)[📈](results/bm-20250827-3.15.0a0-ffaec6e-NOGIL/bm-20250827-vultr-x86_64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e-vs-3.12.6.svg) | 1.056x ↓<br>[📄](results/bm-20250827-3.15.0a0-ffaec6e-NOGIL/bm-20250827-vultr-x86_64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e-vs-3.13.0rc2.md)[📈](results/bm-20250827-3.15.0a0-ffaec6e-NOGIL/bm-20250827-vultr-x86_64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e-vs-3.13.0rc2.svg) | 1.094x ↓<br>[📄](results/bm-20250827-3.15.0a0-ffaec6e-NOGIL/bm-20250827-vultr-x86_64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e-vs-base.md)[📈](results/bm-20250827-3.15.0a0-ffaec6e-NOGIL/bm-20250827-vultr-x86_64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e-vs-base.svg)[🧠](results/bm-20250827-3.15.0a0-ffaec6e-NOGIL/bm-20250827-vultr-x86_64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e-vs-base-mem.svg) |
| [2025-08-27](results/bm-20250827-3.15.0a0-ffaec6e) | python/ffaec6e2a11fb7b41fac | ffaec6e | 1.073x ↑<br>[📄](results/bm-20250827-3.15.0a0-ffaec6e/bm-20250827-vultr-x86_64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e-vs-3.12.6.md)[📈](results/bm-20250827-3.15.0a0-ffaec6e/bm-20250827-vultr-x86_64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e-vs-3.12.6.svg) | 1.037x ↑<br>[📄](results/bm-20250827-3.15.0a0-ffaec6e/bm-20250827-vultr-x86_64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e-vs-3.13.0rc2.md)[📈](results/bm-20250827-3.15.0a0-ffaec6e/bm-20250827-vultr-x86_64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-08-29](results/bm-20250829-3.15.0a0-e05182f-NOGIL) | python/e05182f98ea100b6e267 | e05182f (NOGIL) | 1.079x ↑<br>[📄](results/bm-20250829-3.15.0a0-e05182f-NOGIL/bm-20250829-macm4pro-arm64-python-e05182f98ea100b6e267-3.15.0a0-e05182f-vs-3.12.6.md)[📈](results/bm-20250829-3.15.0a0-e05182f-NOGIL/bm-20250829-macm4pro-arm64-python-e05182f98ea100b6e267-3.15.0a0-e05182f-vs-3.12.6.svg) | 1.001x ↑<br>[📄](results/bm-20250829-3.15.0a0-e05182f-NOGIL/bm-20250829-macm4pro-arm64-python-e05182f98ea100b6e267-3.15.0a0-e05182f-vs-3.13.0rc2.md)[📈](results/bm-20250829-3.15.0a0-e05182f-NOGIL/bm-20250829-macm4pro-arm64-python-e05182f98ea100b6e267-3.15.0a0-e05182f-vs-3.13.0rc2.svg) | 1.018x ↓<br>[📄](results/bm-20250829-3.15.0a0-e05182f-NOGIL/bm-20250829-macm4pro-arm64-python-e05182f98ea100b6e267-3.15.0a0-e05182f-vs-base.md)[📈](results/bm-20250829-3.15.0a0-e05182f-NOGIL/bm-20250829-macm4pro-arm64-python-e05182f98ea100b6e267-3.15.0a0-e05182f-vs-base.svg)[🧠](results/bm-20250829-3.15.0a0-e05182f-NOGIL/bm-20250829-macm4pro-arm64-python-e05182f98ea100b6e267-3.15.0a0-e05182f-vs-base-mem.svg) |
| [2025-08-29](results/bm-20250829-3.15.0a0-e05182f) | python/e05182f98ea100b6e267 | e05182f | 1.097x ↑<br>[📄](results/bm-20250829-3.15.0a0-e05182f/bm-20250829-macm4pro-arm64-python-e05182f98ea100b6e267-3.15.0a0-e05182f-vs-3.12.6.md)[📈](results/bm-20250829-3.15.0a0-e05182f/bm-20250829-macm4pro-arm64-python-e05182f98ea100b6e267-3.15.0a0-e05182f-vs-3.12.6.svg) | 1.018x ↑<br>[📄](results/bm-20250829-3.15.0a0-e05182f/bm-20250829-macm4pro-arm64-python-e05182f98ea100b6e267-3.15.0a0-e05182f-vs-3.13.0rc2.md)[📈](results/bm-20250829-3.15.0a0-e05182f/bm-20250829-macm4pro-arm64-python-e05182f98ea100b6e267-3.15.0a0-e05182f-vs-3.13.0rc2.svg) |  |
| [2025-08-28](results/bm-20250828-3.15.0a0-c779f23-NOGIL) | python/c779f2324df06563b4ba | c779f23 (NOGIL) | 1.080x ↑<br>[📄](results/bm-20250828-3.15.0a0-c779f23-NOGIL/bm-20250828-macm4pro-arm64-python-c779f2324df06563b4ba-3.15.0a0-c779f23-vs-3.12.6.md)[📈](results/bm-20250828-3.15.0a0-c779f23-NOGIL/bm-20250828-macm4pro-arm64-python-c779f2324df06563b4ba-3.15.0a0-c779f23-vs-3.12.6.svg) | 1.002x ↑<br>[📄](results/bm-20250828-3.15.0a0-c779f23-NOGIL/bm-20250828-macm4pro-arm64-python-c779f2324df06563b4ba-3.15.0a0-c779f23-vs-3.13.0rc2.md)[📈](results/bm-20250828-3.15.0a0-c779f23-NOGIL/bm-20250828-macm4pro-arm64-python-c779f2324df06563b4ba-3.15.0a0-c779f23-vs-3.13.0rc2.svg) | 1.023x ↓<br>[📄](results/bm-20250828-3.15.0a0-c779f23-NOGIL/bm-20250828-macm4pro-arm64-python-c779f2324df06563b4ba-3.15.0a0-c779f23-vs-base.md)[📈](results/bm-20250828-3.15.0a0-c779f23-NOGIL/bm-20250828-macm4pro-arm64-python-c779f2324df06563b4ba-3.15.0a0-c779f23-vs-base.svg)[🧠](results/bm-20250828-3.15.0a0-c779f23-NOGIL/bm-20250828-macm4pro-arm64-python-c779f2324df06563b4ba-3.15.0a0-c779f23-vs-base-mem.svg) |
| [2025-08-28](results/bm-20250828-3.15.0a0-c779f23) | python/c779f2324df06563b4ba | c779f23 | 1.103x ↑<br>[📄](results/bm-20250828-3.15.0a0-c779f23/bm-20250828-macm4pro-arm64-python-c779f2324df06563b4ba-3.15.0a0-c779f23-vs-3.12.6.md)[📈](results/bm-20250828-3.15.0a0-c779f23/bm-20250828-macm4pro-arm64-python-c779f2324df06563b4ba-3.15.0a0-c779f23-vs-3.12.6.svg) | 1.023x ↑<br>[📄](results/bm-20250828-3.15.0a0-c779f23/bm-20250828-macm4pro-arm64-python-c779f2324df06563b4ba-3.15.0a0-c779f23-vs-3.13.0rc2.md)[📈](results/bm-20250828-3.15.0a0-c779f23/bm-20250828-macm4pro-arm64-python-c779f2324df06563b4ba-3.15.0a0-c779f23-vs-3.13.0rc2.svg) |  |
| [2025-08-27](results/bm-20250827-3.15.0a0-d910b93-NOGIL) | python/d910b93f786982a11d7d | d910b93 (NOGIL) | 1.072x ↑<br>[📄](results/bm-20250827-3.15.0a0-d910b93-NOGIL/bm-20250827-macm4pro-arm64-python-d910b93f786982a11d7d-3.15.0a0-d910b93-vs-3.12.6.md)[📈](results/bm-20250827-3.15.0a0-d910b93-NOGIL/bm-20250827-macm4pro-arm64-python-d910b93f786982a11d7d-3.15.0a0-d910b93-vs-3.12.6.svg) | 1.005x ↓<br>[📄](results/bm-20250827-3.15.0a0-d910b93-NOGIL/bm-20250827-macm4pro-arm64-python-d910b93f786982a11d7d-3.15.0a0-d910b93-vs-3.13.0rc2.md)[📈](results/bm-20250827-3.15.0a0-d910b93-NOGIL/bm-20250827-macm4pro-arm64-python-d910b93f786982a11d7d-3.15.0a0-d910b93-vs-3.13.0rc2.svg) | 1.031x ↓<br>[📄](results/bm-20250827-3.15.0a0-d910b93-NOGIL/bm-20250827-macm4pro-arm64-python-d910b93f786982a11d7d-3.15.0a0-d910b93-vs-base.md)[📈](results/bm-20250827-3.15.0a0-d910b93-NOGIL/bm-20250827-macm4pro-arm64-python-d910b93f786982a11d7d-3.15.0a0-d910b93-vs-base.svg)[🧠](results/bm-20250827-3.15.0a0-d910b93-NOGIL/bm-20250827-macm4pro-arm64-python-d910b93f786982a11d7d-3.15.0a0-d910b93-vs-base-mem.svg) |
| [2025-08-27](results/bm-20250827-3.15.0a0-d910b93) | python/d910b93f786982a11d7d | d910b93 | 1.105x ↑<br>[📄](results/bm-20250827-3.15.0a0-d910b93/bm-20250827-macm4pro-arm64-python-d910b93f786982a11d7d-3.15.0a0-d910b93-vs-3.12.6.md)[📈](results/bm-20250827-3.15.0a0-d910b93/bm-20250827-macm4pro-arm64-python-d910b93f786982a11d7d-3.15.0a0-d910b93-vs-3.12.6.svg) | 1.025x ↑<br>[📄](results/bm-20250827-3.15.0a0-d910b93/bm-20250827-macm4pro-arm64-python-d910b93f786982a11d7d-3.15.0a0-d910b93-vs-3.13.0rc2.md)[📈](results/bm-20250827-3.15.0a0-d910b93/bm-20250827-macm4pro-arm64-python-d910b93f786982a11d7d-3.15.0a0-d910b93-vs-3.13.0rc2.svg) |  |
| [2025-08-27](results/bm-20250827-3.15.0a0-ffaec6e-NOGIL) | python/ffaec6e2a11fb7b41fac | ffaec6e (NOGIL) | 1.077x ↑<br>[📄](results/bm-20250827-3.15.0a0-ffaec6e-NOGIL/bm-20250827-macm4pro-arm64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e-vs-3.12.6.md)[📈](results/bm-20250827-3.15.0a0-ffaec6e-NOGIL/bm-20250827-macm4pro-arm64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e-vs-3.12.6.svg) | 1.001x ↓<br>[📄](results/bm-20250827-3.15.0a0-ffaec6e-NOGIL/bm-20250827-macm4pro-arm64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e-vs-3.13.0rc2.md)[📈](results/bm-20250827-3.15.0a0-ffaec6e-NOGIL/bm-20250827-macm4pro-arm64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e-vs-3.13.0rc2.svg) | 1.024x ↓<br>[📄](results/bm-20250827-3.15.0a0-ffaec6e-NOGIL/bm-20250827-macm4pro-arm64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e-vs-base.md)[📈](results/bm-20250827-3.15.0a0-ffaec6e-NOGIL/bm-20250827-macm4pro-arm64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e-vs-base.svg)[🧠](results/bm-20250827-3.15.0a0-ffaec6e-NOGIL/bm-20250827-macm4pro-arm64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e-vs-base-mem.svg) |
| [2025-08-27](results/bm-20250827-3.15.0a0-ffaec6e) | python/ffaec6e2a11fb7b41fac | ffaec6e | 1.101x ↑<br>[📄](results/bm-20250827-3.15.0a0-ffaec6e/bm-20250827-macm4pro-arm64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e-vs-3.12.6.md)[📈](results/bm-20250827-3.15.0a0-ffaec6e/bm-20250827-macm4pro-arm64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e-vs-3.12.6.svg) | 1.022x ↑<br>[📄](results/bm-20250827-3.15.0a0-ffaec6e/bm-20250827-macm4pro-arm64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e-vs-3.13.0rc2.md)[📈](results/bm-20250827-3.15.0a0-ffaec6e/bm-20250827-macm4pro-arm64-python-ffaec6e2a11fb7b41fac-3.15.0a0-ffaec6e-vs-3.13.0rc2.svg) |  |


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
