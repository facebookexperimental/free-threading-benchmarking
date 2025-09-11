# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (c117b03)](results/bm-20250906-3.15.0a0-c117b03/bm-20250906-vultr-x86_64-python-c117b033856ab7873972-3.15.0a0-c117b03-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (c117b03)](results/bm-20250906-3.15.0a0-c117b03-PYTHON_UOPS/bm-20250906-vultr-x86_64-python-c117b033856ab7873972-3.15.0a0-c117b03-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-09-10](results/bm-20250910-3.15.0a0-d0c9943-NOGIL) | python/d0c9943869bb143df445 | d0c9943 (NOGIL) | 1.018x ↓<br>[📄](results/bm-20250910-3.15.0a0-d0c9943-NOGIL/bm-20250910-vultr-x86_64-python-d0c9943869bb143df445-3.15.0a0-d0c9943-vs-3.12.6.md)[📈](results/bm-20250910-3.15.0a0-d0c9943-NOGIL/bm-20250910-vultr-x86_64-python-d0c9943869bb143df445-3.15.0a0-d0c9943-vs-3.12.6.svg) | 1.051x ↓<br>[📄](results/bm-20250910-3.15.0a0-d0c9943-NOGIL/bm-20250910-vultr-x86_64-python-d0c9943869bb143df445-3.15.0a0-d0c9943-vs-3.13.0rc2.md)[📈](results/bm-20250910-3.15.0a0-d0c9943-NOGIL/bm-20250910-vultr-x86_64-python-d0c9943869bb143df445-3.15.0a0-d0c9943-vs-3.13.0rc2.svg) | 1.084x ↓<br>[📄](results/bm-20250910-3.15.0a0-d0c9943-NOGIL/bm-20250910-vultr-x86_64-python-d0c9943869bb143df445-3.15.0a0-d0c9943-vs-base.md)[📈](results/bm-20250910-3.15.0a0-d0c9943-NOGIL/bm-20250910-vultr-x86_64-python-d0c9943869bb143df445-3.15.0a0-d0c9943-vs-base.svg)[🧠](results/bm-20250910-3.15.0a0-d0c9943-NOGIL/bm-20250910-vultr-x86_64-python-d0c9943869bb143df445-3.15.0a0-d0c9943-vs-base-mem.svg) |
| [2025-09-10](results/bm-20250910-3.15.0a0-d0c9943) | python/d0c9943869bb143df445 | d0c9943 | 1.064x ↑<br>[📄](results/bm-20250910-3.15.0a0-d0c9943/bm-20250910-vultr-x86_64-python-d0c9943869bb143df445-3.15.0a0-d0c9943-vs-3.12.6.md)[📈](results/bm-20250910-3.15.0a0-d0c9943/bm-20250910-vultr-x86_64-python-d0c9943869bb143df445-3.15.0a0-d0c9943-vs-3.12.6.svg) | 1.028x ↑<br>[📄](results/bm-20250910-3.15.0a0-d0c9943/bm-20250910-vultr-x86_64-python-d0c9943869bb143df445-3.15.0a0-d0c9943-vs-3.13.0rc2.md)[📈](results/bm-20250910-3.15.0a0-d0c9943/bm-20250910-vultr-x86_64-python-d0c9943869bb143df445-3.15.0a0-d0c9943-vs-3.13.0rc2.svg) |  |
| [2025-09-10](results/bm-20250910-3.15.0a0-766e7f1-NOGIL) | python/766e7f150ae93d637824 | 766e7f1 (NOGIL) | 1.026x ↓<br>[📄](results/bm-20250910-3.15.0a0-766e7f1-NOGIL/bm-20250910-vultr-x86_64-python-766e7f150ae93d637824-3.15.0a0-766e7f1-vs-3.12.6.md)[📈](results/bm-20250910-3.15.0a0-766e7f1-NOGIL/bm-20250910-vultr-x86_64-python-766e7f150ae93d637824-3.15.0a0-766e7f1-vs-3.12.6.svg) | 1.059x ↓<br>[📄](results/bm-20250910-3.15.0a0-766e7f1-NOGIL/bm-20250910-vultr-x86_64-python-766e7f150ae93d637824-3.15.0a0-766e7f1-vs-3.13.0rc2.md)[📈](results/bm-20250910-3.15.0a0-766e7f1-NOGIL/bm-20250910-vultr-x86_64-python-766e7f150ae93d637824-3.15.0a0-766e7f1-vs-3.13.0rc2.svg) | 1.092x ↓<br>[📄](results/bm-20250910-3.15.0a0-766e7f1-NOGIL/bm-20250910-vultr-x86_64-python-766e7f150ae93d637824-3.15.0a0-766e7f1-vs-base.md)[📈](results/bm-20250910-3.15.0a0-766e7f1-NOGIL/bm-20250910-vultr-x86_64-python-766e7f150ae93d637824-3.15.0a0-766e7f1-vs-base.svg)[🧠](results/bm-20250910-3.15.0a0-766e7f1-NOGIL/bm-20250910-vultr-x86_64-python-766e7f150ae93d637824-3.15.0a0-766e7f1-vs-base-mem.svg) |
| [2025-09-10](results/bm-20250910-3.15.0a0-766e7f1) | python/766e7f150ae93d637824 | 766e7f1 | 1.066x ↑<br>[📄](results/bm-20250910-3.15.0a0-766e7f1/bm-20250910-vultr-x86_64-python-766e7f150ae93d637824-3.15.0a0-766e7f1-vs-3.12.6.md)[📈](results/bm-20250910-3.15.0a0-766e7f1/bm-20250910-vultr-x86_64-python-766e7f150ae93d637824-3.15.0a0-766e7f1-vs-3.12.6.svg) | 1.030x ↑<br>[📄](results/bm-20250910-3.15.0a0-766e7f1/bm-20250910-vultr-x86_64-python-766e7f150ae93d637824-3.15.0a0-766e7f1-vs-3.13.0rc2.md)[📈](results/bm-20250910-3.15.0a0-766e7f1/bm-20250910-vultr-x86_64-python-766e7f150ae93d637824-3.15.0a0-766e7f1-vs-3.13.0rc2.svg) |  |
| [2025-09-09](results/bm-20250909-3.15.0a0-03ee060-NOGIL) | python/03ee060ec8408303cd27 | 03ee060 (NOGIL) | 1.023x ↓<br>[📄](results/bm-20250909-3.15.0a0-03ee060-NOGIL/bm-20250909-vultr-x86_64-python-03ee060ec8408303cd27-3.15.0a0-03ee060-vs-3.12.6.md)[📈](results/bm-20250909-3.15.0a0-03ee060-NOGIL/bm-20250909-vultr-x86_64-python-03ee060ec8408303cd27-3.15.0a0-03ee060-vs-3.12.6.svg) | 1.056x ↓<br>[📄](results/bm-20250909-3.15.0a0-03ee060-NOGIL/bm-20250909-vultr-x86_64-python-03ee060ec8408303cd27-3.15.0a0-03ee060-vs-3.13.0rc2.md)[📈](results/bm-20250909-3.15.0a0-03ee060-NOGIL/bm-20250909-vultr-x86_64-python-03ee060ec8408303cd27-3.15.0a0-03ee060-vs-3.13.0rc2.svg) | 1.095x ↓<br>[📄](results/bm-20250909-3.15.0a0-03ee060-NOGIL/bm-20250909-vultr-x86_64-python-03ee060ec8408303cd27-3.15.0a0-03ee060-vs-base.md)[📈](results/bm-20250909-3.15.0a0-03ee060-NOGIL/bm-20250909-vultr-x86_64-python-03ee060ec8408303cd27-3.15.0a0-03ee060-vs-base.svg)[🧠](results/bm-20250909-3.15.0a0-03ee060-NOGIL/bm-20250909-vultr-x86_64-python-03ee060ec8408303cd27-3.15.0a0-03ee060-vs-base-mem.svg) |
| [2025-09-09](results/bm-20250909-3.15.0a0-03ee060) | python/03ee060ec8408303cd27 | 03ee060 | 1.073x ↑<br>[📄](results/bm-20250909-3.15.0a0-03ee060/bm-20250909-vultr-x86_64-python-03ee060ec8408303cd27-3.15.0a0-03ee060-vs-3.12.6.md)[📈](results/bm-20250909-3.15.0a0-03ee060/bm-20250909-vultr-x86_64-python-03ee060ec8408303cd27-3.15.0a0-03ee060-vs-3.12.6.svg) | 1.038x ↑<br>[📄](results/bm-20250909-3.15.0a0-03ee060/bm-20250909-vultr-x86_64-python-03ee060ec8408303cd27-3.15.0a0-03ee060-vs-3.13.0rc2.md)[📈](results/bm-20250909-3.15.0a0-03ee060/bm-20250909-vultr-x86_64-python-03ee060ec8408303cd27-3.15.0a0-03ee060-vs-3.13.0rc2.svg) |  |
| [2025-09-08](results/bm-20250908-3.15.0a0-b0420b5-NOGIL) | python/b0420b505e6c9bbc8418 | b0420b5 (NOGIL) | 1.025x ↓<br>[📄](results/bm-20250908-3.15.0a0-b0420b5-NOGIL/bm-20250908-vultr-x86_64-python-b0420b505e6c9bbc8418-3.15.0a0-b0420b5-vs-3.12.6.md)[📈](results/bm-20250908-3.15.0a0-b0420b5-NOGIL/bm-20250908-vultr-x86_64-python-b0420b505e6c9bbc8418-3.15.0a0-b0420b5-vs-3.12.6.svg) | 1.058x ↓<br>[📄](results/bm-20250908-3.15.0a0-b0420b5-NOGIL/bm-20250908-vultr-x86_64-python-b0420b505e6c9bbc8418-3.15.0a0-b0420b5-vs-3.13.0rc2.md)[📈](results/bm-20250908-3.15.0a0-b0420b5-NOGIL/bm-20250908-vultr-x86_64-python-b0420b505e6c9bbc8418-3.15.0a0-b0420b5-vs-3.13.0rc2.svg) | 1.088x ↓<br>[📄](results/bm-20250908-3.15.0a0-b0420b5-NOGIL/bm-20250908-vultr-x86_64-python-b0420b505e6c9bbc8418-3.15.0a0-b0420b5-vs-base.md)[📈](results/bm-20250908-3.15.0a0-b0420b5-NOGIL/bm-20250908-vultr-x86_64-python-b0420b505e6c9bbc8418-3.15.0a0-b0420b5-vs-base.svg)[🧠](results/bm-20250908-3.15.0a0-b0420b5-NOGIL/bm-20250908-vultr-x86_64-python-b0420b505e6c9bbc8418-3.15.0a0-b0420b5-vs-base-mem.svg) |
| [2025-09-08](results/bm-20250908-3.15.0a0-b0420b5) | python/b0420b505e6c9bbc8418 | b0420b5 | 1.061x ↑<br>[📄](results/bm-20250908-3.15.0a0-b0420b5/bm-20250908-vultr-x86_64-python-b0420b505e6c9bbc8418-3.15.0a0-b0420b5-vs-3.12.6.md)[📈](results/bm-20250908-3.15.0a0-b0420b5/bm-20250908-vultr-x86_64-python-b0420b505e6c9bbc8418-3.15.0a0-b0420b5-vs-3.12.6.svg) | 1.026x ↑<br>[📄](results/bm-20250908-3.15.0a0-b0420b5/bm-20250908-vultr-x86_64-python-b0420b505e6c9bbc8418-3.15.0a0-b0420b5-vs-3.13.0rc2.md)[📈](results/bm-20250908-3.15.0a0-b0420b5/bm-20250908-vultr-x86_64-python-b0420b505e6c9bbc8418-3.15.0a0-b0420b5-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-09-10](results/bm-20250910-3.15.0a0-d0c9943-NOGIL) | python/d0c9943869bb143df445 | d0c9943 (NOGIL) | 1.073x ↑<br>[📄](results/bm-20250910-3.15.0a0-d0c9943-NOGIL/bm-20250910-macm4pro-arm64-python-d0c9943869bb143df445-3.15.0a0-d0c9943-vs-3.12.6.md)[📈](results/bm-20250910-3.15.0a0-d0c9943-NOGIL/bm-20250910-macm4pro-arm64-python-d0c9943869bb143df445-3.15.0a0-d0c9943-vs-3.12.6.svg) | 1.004x ↓<br>[📄](results/bm-20250910-3.15.0a0-d0c9943-NOGIL/bm-20250910-macm4pro-arm64-python-d0c9943869bb143df445-3.15.0a0-d0c9943-vs-3.13.0rc2.md)[📈](results/bm-20250910-3.15.0a0-d0c9943-NOGIL/bm-20250910-macm4pro-arm64-python-d0c9943869bb143df445-3.15.0a0-d0c9943-vs-3.13.0rc2.svg) | 1.022x ↓<br>[📄](results/bm-20250910-3.15.0a0-d0c9943-NOGIL/bm-20250910-macm4pro-arm64-python-d0c9943869bb143df445-3.15.0a0-d0c9943-vs-base.md)[📈](results/bm-20250910-3.15.0a0-d0c9943-NOGIL/bm-20250910-macm4pro-arm64-python-d0c9943869bb143df445-3.15.0a0-d0c9943-vs-base.svg)[🧠](results/bm-20250910-3.15.0a0-d0c9943-NOGIL/bm-20250910-macm4pro-arm64-python-d0c9943869bb143df445-3.15.0a0-d0c9943-vs-base-mem.svg) |
| [2025-09-10](results/bm-20250910-3.15.0a0-d0c9943) | python/d0c9943869bb143df445 | d0c9943 | 1.096x ↑<br>[📄](results/bm-20250910-3.15.0a0-d0c9943/bm-20250910-macm4pro-arm64-python-d0c9943869bb143df445-3.15.0a0-d0c9943-vs-3.12.6.md)[📈](results/bm-20250910-3.15.0a0-d0c9943/bm-20250910-macm4pro-arm64-python-d0c9943869bb143df445-3.15.0a0-d0c9943-vs-3.12.6.svg) | 1.017x ↑<br>[📄](results/bm-20250910-3.15.0a0-d0c9943/bm-20250910-macm4pro-arm64-python-d0c9943869bb143df445-3.15.0a0-d0c9943-vs-3.13.0rc2.md)[📈](results/bm-20250910-3.15.0a0-d0c9943/bm-20250910-macm4pro-arm64-python-d0c9943869bb143df445-3.15.0a0-d0c9943-vs-3.13.0rc2.svg) |  |
| [2025-09-10](results/bm-20250910-3.15.0a0-766e7f1-NOGIL) | python/766e7f150ae93d637824 | 766e7f1 (NOGIL) | 1.083x ↑<br>[📄](results/bm-20250910-3.15.0a0-766e7f1-NOGIL/bm-20250910-macm4pro-arm64-python-766e7f150ae93d637824-3.15.0a0-766e7f1-vs-3.12.6.md)[📈](results/bm-20250910-3.15.0a0-766e7f1-NOGIL/bm-20250910-macm4pro-arm64-python-766e7f150ae93d637824-3.15.0a0-766e7f1-vs-3.12.6.svg) | 1.004x ↑<br>[📄](results/bm-20250910-3.15.0a0-766e7f1-NOGIL/bm-20250910-macm4pro-arm64-python-766e7f150ae93d637824-3.15.0a0-766e7f1-vs-3.13.0rc2.md)[📈](results/bm-20250910-3.15.0a0-766e7f1-NOGIL/bm-20250910-macm4pro-arm64-python-766e7f150ae93d637824-3.15.0a0-766e7f1-vs-3.13.0rc2.svg) | 1.022x ↓<br>[📄](results/bm-20250910-3.15.0a0-766e7f1-NOGIL/bm-20250910-macm4pro-arm64-python-766e7f150ae93d637824-3.15.0a0-766e7f1-vs-base.md)[📈](results/bm-20250910-3.15.0a0-766e7f1-NOGIL/bm-20250910-macm4pro-arm64-python-766e7f150ae93d637824-3.15.0a0-766e7f1-vs-base.svg)[🧠](results/bm-20250910-3.15.0a0-766e7f1-NOGIL/bm-20250910-macm4pro-arm64-python-766e7f150ae93d637824-3.15.0a0-766e7f1-vs-base-mem.svg) |
| [2025-09-10](results/bm-20250910-3.15.0a0-766e7f1) | python/766e7f150ae93d637824 | 766e7f1 | 1.105x ↑<br>[📄](results/bm-20250910-3.15.0a0-766e7f1/bm-20250910-macm4pro-arm64-python-766e7f150ae93d637824-3.15.0a0-766e7f1-vs-3.12.6.md)[📈](results/bm-20250910-3.15.0a0-766e7f1/bm-20250910-macm4pro-arm64-python-766e7f150ae93d637824-3.15.0a0-766e7f1-vs-3.12.6.svg) | 1.025x ↑<br>[📄](results/bm-20250910-3.15.0a0-766e7f1/bm-20250910-macm4pro-arm64-python-766e7f150ae93d637824-3.15.0a0-766e7f1-vs-3.13.0rc2.md)[📈](results/bm-20250910-3.15.0a0-766e7f1/bm-20250910-macm4pro-arm64-python-766e7f150ae93d637824-3.15.0a0-766e7f1-vs-3.13.0rc2.svg) |  |
| [2025-09-09](results/bm-20250909-3.15.0a0-03ee060-NOGIL) | python/03ee060ec8408303cd27 | 03ee060 (NOGIL) | 1.081x ↑<br>[📄](results/bm-20250909-3.15.0a0-03ee060-NOGIL/bm-20250909-macm4pro-arm64-python-03ee060ec8408303cd27-3.15.0a0-03ee060-vs-3.12.6.md)[📈](results/bm-20250909-3.15.0a0-03ee060-NOGIL/bm-20250909-macm4pro-arm64-python-03ee060ec8408303cd27-3.15.0a0-03ee060-vs-3.12.6.svg) | 1.003x ↑<br>[📄](results/bm-20250909-3.15.0a0-03ee060-NOGIL/bm-20250909-macm4pro-arm64-python-03ee060ec8408303cd27-3.15.0a0-03ee060-vs-3.13.0rc2.md)[📈](results/bm-20250909-3.15.0a0-03ee060-NOGIL/bm-20250909-macm4pro-arm64-python-03ee060ec8408303cd27-3.15.0a0-03ee060-vs-3.13.0rc2.svg) | 1.024x ↓<br>[📄](results/bm-20250909-3.15.0a0-03ee060-NOGIL/bm-20250909-macm4pro-arm64-python-03ee060ec8408303cd27-3.15.0a0-03ee060-vs-base.md)[📈](results/bm-20250909-3.15.0a0-03ee060-NOGIL/bm-20250909-macm4pro-arm64-python-03ee060ec8408303cd27-3.15.0a0-03ee060-vs-base.svg)[🧠](results/bm-20250909-3.15.0a0-03ee060-NOGIL/bm-20250909-macm4pro-arm64-python-03ee060ec8408303cd27-3.15.0a0-03ee060-vs-base-mem.svg) |
| [2025-09-09](results/bm-20250909-3.15.0a0-03ee060) | python/03ee060ec8408303cd27 | 03ee060 | 1.105x ↑<br>[📄](results/bm-20250909-3.15.0a0-03ee060/bm-20250909-macm4pro-arm64-python-03ee060ec8408303cd27-3.15.0a0-03ee060-vs-3.12.6.md)[📈](results/bm-20250909-3.15.0a0-03ee060/bm-20250909-macm4pro-arm64-python-03ee060ec8408303cd27-3.15.0a0-03ee060-vs-3.12.6.svg) | 1.025x ↑<br>[📄](results/bm-20250909-3.15.0a0-03ee060/bm-20250909-macm4pro-arm64-python-03ee060ec8408303cd27-3.15.0a0-03ee060-vs-3.13.0rc2.md)[📈](results/bm-20250909-3.15.0a0-03ee060/bm-20250909-macm4pro-arm64-python-03ee060ec8408303cd27-3.15.0a0-03ee060-vs-3.13.0rc2.svg) |  |
| [2025-09-08](results/bm-20250908-3.15.0a0-b0420b5-NOGIL) | python/b0420b505e6c9bbc8418 | b0420b5 (NOGIL) | 1.076x ↑<br>[📄](results/bm-20250908-3.15.0a0-b0420b5-NOGIL/bm-20250908-macm4pro-arm64-python-b0420b505e6c9bbc8418-3.15.0a0-b0420b5-vs-3.12.6.md)[📈](results/bm-20250908-3.15.0a0-b0420b5-NOGIL/bm-20250908-macm4pro-arm64-python-b0420b505e6c9bbc8418-3.15.0a0-b0420b5-vs-3.12.6.svg) | 1.002x ↓<br>[📄](results/bm-20250908-3.15.0a0-b0420b5-NOGIL/bm-20250908-macm4pro-arm64-python-b0420b505e6c9bbc8418-3.15.0a0-b0420b5-vs-3.13.0rc2.md)[📈](results/bm-20250908-3.15.0a0-b0420b5-NOGIL/bm-20250908-macm4pro-arm64-python-b0420b505e6c9bbc8418-3.15.0a0-b0420b5-vs-3.13.0rc2.svg) | 1.010x ↓<br>[📄](results/bm-20250908-3.15.0a0-b0420b5-NOGIL/bm-20250908-macm4pro-arm64-python-b0420b505e6c9bbc8418-3.15.0a0-b0420b5-vs-base.md)[📈](results/bm-20250908-3.15.0a0-b0420b5-NOGIL/bm-20250908-macm4pro-arm64-python-b0420b505e6c9bbc8418-3.15.0a0-b0420b5-vs-base.svg)[🧠](results/bm-20250908-3.15.0a0-b0420b5-NOGIL/bm-20250908-macm4pro-arm64-python-b0420b505e6c9bbc8418-3.15.0a0-b0420b5-vs-base-mem.svg) |
| [2025-09-08](results/bm-20250908-3.15.0a0-b0420b5) | python/b0420b505e6c9bbc8418 | b0420b5 | 1.085x ↑<br>[📄](results/bm-20250908-3.15.0a0-b0420b5/bm-20250908-macm4pro-arm64-python-b0420b505e6c9bbc8418-3.15.0a0-b0420b5-vs-3.12.6.md)[📈](results/bm-20250908-3.15.0a0-b0420b5/bm-20250908-macm4pro-arm64-python-b0420b505e6c9bbc8418-3.15.0a0-b0420b5-vs-3.12.6.svg) | 1.007x ↑<br>[📄](results/bm-20250908-3.15.0a0-b0420b5/bm-20250908-macm4pro-arm64-python-b0420b505e6c9bbc8418-3.15.0a0-b0420b5-vs-3.13.0rc2.md)[📈](results/bm-20250908-3.15.0a0-b0420b5/bm-20250908-macm4pro-arm64-python-b0420b505e6c9bbc8418-3.15.0a0-b0420b5-vs-3.13.0rc2.svg) |  |


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
