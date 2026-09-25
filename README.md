# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (c1df684)](results/bm-20260919-3.16.0a0-c1df684/bm-20260919-vultr-x86_64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (c1df684)](results/bm-20260919-3.16.0a0-c1df684-PYTHON_UOPS/bm-20260919-vultr-x86_64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684-pystats.md)
- [Most recent JIT pystats on main (bedaea0)](results/bm-20251019-3.15.0a1%2B-bedaea0-JIT/bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-09-25](results/bm-20260925-3.16.0a0-80f9aa0-NOGIL) | python/80f9aa0b18d96509eec3 | 80f9aa0 (NOGIL) | 1.048x ↓<br>[📄](results/bm-20260925-3.16.0a0-80f9aa0-NOGIL/bm-20260925-vultr-x86_64-python-80f9aa0b18d96509eec3-3.16.0a0-80f9aa0-vs-3.12.6.md)[📈](results/bm-20260925-3.16.0a0-80f9aa0-NOGIL/bm-20260925-vultr-x86_64-python-80f9aa0b18d96509eec3-3.16.0a0-80f9aa0-vs-3.12.6.svg) | 1.081x ↓<br>[📄](results/bm-20260925-3.16.0a0-80f9aa0-NOGIL/bm-20260925-vultr-x86_64-python-80f9aa0b18d96509eec3-3.16.0a0-80f9aa0-vs-3.13.0rc2.md)[📈](results/bm-20260925-3.16.0a0-80f9aa0-NOGIL/bm-20260925-vultr-x86_64-python-80f9aa0b18d96509eec3-3.16.0a0-80f9aa0-vs-3.13.0rc2.svg) | 1.104x ↓<br>[📄](results/bm-20260925-3.16.0a0-80f9aa0-NOGIL/bm-20260925-vultr-x86_64-python-80f9aa0b18d96509eec3-3.16.0a0-80f9aa0-vs-base.md)[📈](results/bm-20260925-3.16.0a0-80f9aa0-NOGIL/bm-20260925-vultr-x86_64-python-80f9aa0b18d96509eec3-3.16.0a0-80f9aa0-vs-base.svg)[🧠](results/bm-20260925-3.16.0a0-80f9aa0-NOGIL/bm-20260925-vultr-x86_64-python-80f9aa0b18d96509eec3-3.16.0a0-80f9aa0-vs-base-mem.svg) |
| [2026-09-25](results/bm-20260925-3.16.0a0-80f9aa0) | python/80f9aa0b18d96509eec3 | 80f9aa0 | 1.057x ↑<br>[📄](results/bm-20260925-3.16.0a0-80f9aa0/bm-20260925-vultr-x86_64-python-80f9aa0b18d96509eec3-3.16.0a0-80f9aa0-vs-3.12.6.md)[📈](results/bm-20260925-3.16.0a0-80f9aa0/bm-20260925-vultr-x86_64-python-80f9aa0b18d96509eec3-3.16.0a0-80f9aa0-vs-3.12.6.svg) | 1.021x ↑<br>[📄](results/bm-20260925-3.16.0a0-80f9aa0/bm-20260925-vultr-x86_64-python-80f9aa0b18d96509eec3-3.16.0a0-80f9aa0-vs-3.13.0rc2.md)[📈](results/bm-20260925-3.16.0a0-80f9aa0/bm-20260925-vultr-x86_64-python-80f9aa0b18d96509eec3-3.16.0a0-80f9aa0-vs-3.13.0rc2.svg) |  |
| [2026-09-24](results/bm-20260924-3.16.0a0-1cdd590-NOGIL) | python/1cdd590cb547597ab64b | 1cdd590 (NOGIL) | 1.044x ↓<br>[📄](results/bm-20260924-3.16.0a0-1cdd590-NOGIL/bm-20260924-vultr-x86_64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590-vs-3.12.6.md)[📈](results/bm-20260924-3.16.0a0-1cdd590-NOGIL/bm-20260924-vultr-x86_64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590-vs-3.12.6.svg) | 1.076x ↓<br>[📄](results/bm-20260924-3.16.0a0-1cdd590-NOGIL/bm-20260924-vultr-x86_64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590-vs-3.13.0rc2.md)[📈](results/bm-20260924-3.16.0a0-1cdd590-NOGIL/bm-20260924-vultr-x86_64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590-vs-3.13.0rc2.svg) | 1.104x ↓<br>[📄](results/bm-20260924-3.16.0a0-1cdd590-NOGIL/bm-20260924-vultr-x86_64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590-vs-base.md)[📈](results/bm-20260924-3.16.0a0-1cdd590-NOGIL/bm-20260924-vultr-x86_64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590-vs-base.svg)[🧠](results/bm-20260924-3.16.0a0-1cdd590-NOGIL/bm-20260924-vultr-x86_64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590-vs-base-mem.svg) |
| [2026-09-24](results/bm-20260924-3.16.0a0-1cdd590) | python/1cdd590cb547597ab64b | 1cdd590 | 1.061x ↑<br>[📄](results/bm-20260924-3.16.0a0-1cdd590/bm-20260924-vultr-x86_64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590-vs-3.12.6.md)[📈](results/bm-20260924-3.16.0a0-1cdd590/bm-20260924-vultr-x86_64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590-vs-3.12.6.svg) | 1.026x ↑<br>[📄](results/bm-20260924-3.16.0a0-1cdd590/bm-20260924-vultr-x86_64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590-vs-3.13.0rc2.md)[📈](results/bm-20260924-3.16.0a0-1cdd590/bm-20260924-vultr-x86_64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590-vs-3.13.0rc2.svg) |  |
| [2026-09-22](results/bm-20260922-3.16.0a0-6757482-NOGIL) | python/6757482c25d4fa308d3f | 6757482 (NOGIL) | 1.047x ↓<br>[📄](results/bm-20260922-3.16.0a0-6757482-NOGIL/bm-20260922-vultr-x86_64-python-6757482c25d4fa308d3f-3.16.0a0-6757482-vs-3.12.6.md)[📈](results/bm-20260922-3.16.0a0-6757482-NOGIL/bm-20260922-vultr-x86_64-python-6757482c25d4fa308d3f-3.16.0a0-6757482-vs-3.12.6.svg) | 1.079x ↓<br>[📄](results/bm-20260922-3.16.0a0-6757482-NOGIL/bm-20260922-vultr-x86_64-python-6757482c25d4fa308d3f-3.16.0a0-6757482-vs-3.13.0rc2.md)[📈](results/bm-20260922-3.16.0a0-6757482-NOGIL/bm-20260922-vultr-x86_64-python-6757482c25d4fa308d3f-3.16.0a0-6757482-vs-3.13.0rc2.svg) | 1.108x ↓<br>[📄](results/bm-20260922-3.16.0a0-6757482-NOGIL/bm-20260922-vultr-x86_64-python-6757482c25d4fa308d3f-3.16.0a0-6757482-vs-base.md)[📈](results/bm-20260922-3.16.0a0-6757482-NOGIL/bm-20260922-vultr-x86_64-python-6757482c25d4fa308d3f-3.16.0a0-6757482-vs-base.svg)[🧠](results/bm-20260922-3.16.0a0-6757482-NOGIL/bm-20260922-vultr-x86_64-python-6757482c25d4fa308d3f-3.16.0a0-6757482-vs-base-mem.svg) |
| [2026-09-22](results/bm-20260922-3.16.0a0-6757482) | python/6757482c25d4fa308d3f | 6757482 | 1.063x ↑<br>[📄](results/bm-20260922-3.16.0a0-6757482/bm-20260922-vultr-x86_64-python-6757482c25d4fa308d3f-3.16.0a0-6757482-vs-3.12.6.md)[📈](results/bm-20260922-3.16.0a0-6757482/bm-20260922-vultr-x86_64-python-6757482c25d4fa308d3f-3.16.0a0-6757482-vs-3.12.6.svg) | 1.028x ↑<br>[📄](results/bm-20260922-3.16.0a0-6757482/bm-20260922-vultr-x86_64-python-6757482c25d4fa308d3f-3.16.0a0-6757482-vs-3.13.0rc2.md)[📈](results/bm-20260922-3.16.0a0-6757482/bm-20260922-vultr-x86_64-python-6757482c25d4fa308d3f-3.16.0a0-6757482-vs-3.13.0rc2.svg) |  |
| [2026-09-21](results/bm-20260921-3.16.0a0-212e603-NOGIL) | python/212e6035133957a66f1a | 212e603 (NOGIL) | 1.046x ↓<br>[📄](results/bm-20260921-3.16.0a0-212e603-NOGIL/bm-20260921-vultr-x86_64-python-212e6035133957a66f1a-3.16.0a0-212e603-vs-3.12.6.md)[📈](results/bm-20260921-3.16.0a0-212e603-NOGIL/bm-20260921-vultr-x86_64-python-212e6035133957a66f1a-3.16.0a0-212e603-vs-3.12.6.svg) | 1.077x ↓<br>[📄](results/bm-20260921-3.16.0a0-212e603-NOGIL/bm-20260921-vultr-x86_64-python-212e6035133957a66f1a-3.16.0a0-212e603-vs-3.13.0rc2.md)[📈](results/bm-20260921-3.16.0a0-212e603-NOGIL/bm-20260921-vultr-x86_64-python-212e6035133957a66f1a-3.16.0a0-212e603-vs-3.13.0rc2.svg) | 1.107x ↓<br>[📄](results/bm-20260921-3.16.0a0-212e603-NOGIL/bm-20260921-vultr-x86_64-python-212e6035133957a66f1a-3.16.0a0-212e603-vs-base.md)[📈](results/bm-20260921-3.16.0a0-212e603-NOGIL/bm-20260921-vultr-x86_64-python-212e6035133957a66f1a-3.16.0a0-212e603-vs-base.svg)[🧠](results/bm-20260921-3.16.0a0-212e603-NOGIL/bm-20260921-vultr-x86_64-python-212e6035133957a66f1a-3.16.0a0-212e603-vs-base-mem.svg) |
| [2026-09-21](results/bm-20260921-3.16.0a0-212e603) | python/212e6035133957a66f1a | 212e603 | 1.064x ↑<br>[📄](results/bm-20260921-3.16.0a0-212e603/bm-20260921-vultr-x86_64-python-212e6035133957a66f1a-3.16.0a0-212e603-vs-3.12.6.md)[📈](results/bm-20260921-3.16.0a0-212e603/bm-20260921-vultr-x86_64-python-212e6035133957a66f1a-3.16.0a0-212e603-vs-3.12.6.svg) | 1.029x ↑<br>[📄](results/bm-20260921-3.16.0a0-212e603/bm-20260921-vultr-x86_64-python-212e6035133957a66f1a-3.16.0a0-212e603-vs-3.13.0rc2.md)[📈](results/bm-20260921-3.16.0a0-212e603/bm-20260921-vultr-x86_64-python-212e6035133957a66f1a-3.16.0a0-212e603-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-09-25](results/bm-20260925-3.16.0a0-80f9aa0-NOGIL) | python/80f9aa0b18d96509eec3 | 80f9aa0 (NOGIL) | 1.003x ↑<br>[📄](results/bm-20260925-3.16.0a0-80f9aa0-NOGIL/bm-20260925-macm4pro-arm64-python-80f9aa0b18d96509eec3-3.16.0a0-80f9aa0-vs-3.12.6.md)[📈](results/bm-20260925-3.16.0a0-80f9aa0-NOGIL/bm-20260925-macm4pro-arm64-python-80f9aa0b18d96509eec3-3.16.0a0-80f9aa0-vs-3.12.6.svg) | 1.071x ↓<br>[📄](results/bm-20260925-3.16.0a0-80f9aa0-NOGIL/bm-20260925-macm4pro-arm64-python-80f9aa0b18d96509eec3-3.16.0a0-80f9aa0-vs-3.13.0rc2.md)[📈](results/bm-20260925-3.16.0a0-80f9aa0-NOGIL/bm-20260925-macm4pro-arm64-python-80f9aa0b18d96509eec3-3.16.0a0-80f9aa0-vs-3.13.0rc2.svg) | 1.114x ↓<br>[📄](results/bm-20260925-3.16.0a0-80f9aa0-NOGIL/bm-20260925-macm4pro-arm64-python-80f9aa0b18d96509eec3-3.16.0a0-80f9aa0-vs-base.md)[📈](results/bm-20260925-3.16.0a0-80f9aa0-NOGIL/bm-20260925-macm4pro-arm64-python-80f9aa0b18d96509eec3-3.16.0a0-80f9aa0-vs-base.svg)[🧠](results/bm-20260925-3.16.0a0-80f9aa0-NOGIL/bm-20260925-macm4pro-arm64-python-80f9aa0b18d96509eec3-3.16.0a0-80f9aa0-vs-base-mem.svg) |
| [2026-09-25](results/bm-20260925-3.16.0a0-80f9aa0) | python/80f9aa0b18d96509eec3 | 80f9aa0 | 1.134x ↑<br>[📄](results/bm-20260925-3.16.0a0-80f9aa0/bm-20260925-macm4pro-arm64-python-80f9aa0b18d96509eec3-3.16.0a0-80f9aa0-vs-3.12.6.md)[📈](results/bm-20260925-3.16.0a0-80f9aa0/bm-20260925-macm4pro-arm64-python-80f9aa0b18d96509eec3-3.16.0a0-80f9aa0-vs-3.12.6.svg) | 1.048x ↑<br>[📄](results/bm-20260925-3.16.0a0-80f9aa0/bm-20260925-macm4pro-arm64-python-80f9aa0b18d96509eec3-3.16.0a0-80f9aa0-vs-3.13.0rc2.md)[📈](results/bm-20260925-3.16.0a0-80f9aa0/bm-20260925-macm4pro-arm64-python-80f9aa0b18d96509eec3-3.16.0a0-80f9aa0-vs-3.13.0rc2.svg) |  |
| [2026-09-24](results/bm-20260924-3.16.0a0-1cdd590-NOGIL) | python/1cdd590cb547597ab64b | 1cdd590 (NOGIL) | 1.082x ↑<br>[📄](results/bm-20260924-3.16.0a0-1cdd590-NOGIL/bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590-vs-3.12.6.md)[📈](results/bm-20260924-3.16.0a0-1cdd590-NOGIL/bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590-vs-3.12.6.svg) | 1.002x ↑<br>[📄](results/bm-20260924-3.16.0a0-1cdd590-NOGIL/bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590-vs-3.13.0rc2.md)[📈](results/bm-20260924-3.16.0a0-1cdd590-NOGIL/bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590-vs-3.13.0rc2.svg) | 1.042x ↓<br>[📄](results/bm-20260924-3.16.0a0-1cdd590-NOGIL/bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590-vs-base.md)[📈](results/bm-20260924-3.16.0a0-1cdd590-NOGIL/bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590-vs-base.svg)[🧠](results/bm-20260924-3.16.0a0-1cdd590-NOGIL/bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590-vs-base-mem.svg) |
| [2026-09-24](results/bm-20260924-3.16.0a0-1cdd590) | python/1cdd590cb547597ab64b | 1cdd590 | 1.134x ↑<br>[📄](results/bm-20260924-3.16.0a0-1cdd590/bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590-vs-3.12.6.md)[📈](results/bm-20260924-3.16.0a0-1cdd590/bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590-vs-3.12.6.svg) | 1.047x ↑<br>[📄](results/bm-20260924-3.16.0a0-1cdd590/bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590-vs-3.13.0rc2.md)[📈](results/bm-20260924-3.16.0a0-1cdd590/bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590-vs-3.13.0rc2.svg) |  |
| [2026-09-22](results/bm-20260922-3.16.0a0-6757482-NOGIL) | python/6757482c25d4fa308d3f | 6757482 (NOGIL) | 1.002x ↑<br>[📄](results/bm-20260922-3.16.0a0-6757482-NOGIL/bm-20260922-macm4pro-arm64-python-6757482c25d4fa308d3f-3.16.0a0-6757482-vs-3.12.6.md)[📈](results/bm-20260922-3.16.0a0-6757482-NOGIL/bm-20260922-macm4pro-arm64-python-6757482c25d4fa308d3f-3.16.0a0-6757482-vs-3.12.6.svg) | 1.072x ↓<br>[📄](results/bm-20260922-3.16.0a0-6757482-NOGIL/bm-20260922-macm4pro-arm64-python-6757482c25d4fa308d3f-3.16.0a0-6757482-vs-3.13.0rc2.md)[📈](results/bm-20260922-3.16.0a0-6757482-NOGIL/bm-20260922-macm4pro-arm64-python-6757482c25d4fa308d3f-3.16.0a0-6757482-vs-3.13.0rc2.svg) | 1.123x ↓<br>[📄](results/bm-20260922-3.16.0a0-6757482-NOGIL/bm-20260922-macm4pro-arm64-python-6757482c25d4fa308d3f-3.16.0a0-6757482-vs-base.md)[📈](results/bm-20260922-3.16.0a0-6757482-NOGIL/bm-20260922-macm4pro-arm64-python-6757482c25d4fa308d3f-3.16.0a0-6757482-vs-base.svg)[🧠](results/bm-20260922-3.16.0a0-6757482-NOGIL/bm-20260922-macm4pro-arm64-python-6757482c25d4fa308d3f-3.16.0a0-6757482-vs-base-mem.svg) |
| [2026-09-22](results/bm-20260922-3.16.0a0-6757482) | python/6757482c25d4fa308d3f | 6757482 | 1.144x ↑<br>[📄](results/bm-20260922-3.16.0a0-6757482/bm-20260922-macm4pro-arm64-python-6757482c25d4fa308d3f-3.16.0a0-6757482-vs-3.12.6.md)[📈](results/bm-20260922-3.16.0a0-6757482/bm-20260922-macm4pro-arm64-python-6757482c25d4fa308d3f-3.16.0a0-6757482-vs-3.12.6.svg) | 1.056x ↑<br>[📄](results/bm-20260922-3.16.0a0-6757482/bm-20260922-macm4pro-arm64-python-6757482c25d4fa308d3f-3.16.0a0-6757482-vs-3.13.0rc2.md)[📈](results/bm-20260922-3.16.0a0-6757482/bm-20260922-macm4pro-arm64-python-6757482c25d4fa308d3f-3.16.0a0-6757482-vs-3.13.0rc2.svg) |  |
| [2026-09-21](results/bm-20260921-3.16.0a0-212e603-NOGIL) | python/212e6035133957a66f1a | 212e603 (NOGIL) | 1.002x ↑<br>[📄](results/bm-20260921-3.16.0a0-212e603-NOGIL/bm-20260921-macm4pro-arm64-python-212e6035133957a66f1a-3.16.0a0-212e603-vs-3.12.6.md)[📈](results/bm-20260921-3.16.0a0-212e603-NOGIL/bm-20260921-macm4pro-arm64-python-212e6035133957a66f1a-3.16.0a0-212e603-vs-3.12.6.svg) | 1.073x ↓<br>[📄](results/bm-20260921-3.16.0a0-212e603-NOGIL/bm-20260921-macm4pro-arm64-python-212e6035133957a66f1a-3.16.0a0-212e603-vs-3.13.0rc2.md)[📈](results/bm-20260921-3.16.0a0-212e603-NOGIL/bm-20260921-macm4pro-arm64-python-212e6035133957a66f1a-3.16.0a0-212e603-vs-3.13.0rc2.svg) | 1.119x ↓<br>[📄](results/bm-20260921-3.16.0a0-212e603-NOGIL/bm-20260921-macm4pro-arm64-python-212e6035133957a66f1a-3.16.0a0-212e603-vs-base.md)[📈](results/bm-20260921-3.16.0a0-212e603-NOGIL/bm-20260921-macm4pro-arm64-python-212e6035133957a66f1a-3.16.0a0-212e603-vs-base.svg)[🧠](results/bm-20260921-3.16.0a0-212e603-NOGIL/bm-20260921-macm4pro-arm64-python-212e6035133957a66f1a-3.16.0a0-212e603-vs-base-mem.svg) |
| [2026-09-21](results/bm-20260921-3.16.0a0-212e603) | python/212e6035133957a66f1a | 212e603 | 1.139x ↑<br>[📄](results/bm-20260921-3.16.0a0-212e603/bm-20260921-macm4pro-arm64-python-212e6035133957a66f1a-3.16.0a0-212e603-vs-3.12.6.md)[📈](results/bm-20260921-3.16.0a0-212e603/bm-20260921-macm4pro-arm64-python-212e6035133957a66f1a-3.16.0a0-212e603-vs-3.12.6.svg) | 1.052x ↑<br>[📄](results/bm-20260921-3.16.0a0-212e603/bm-20260921-macm4pro-arm64-python-212e6035133957a66f1a-3.16.0a0-212e603-vs-3.13.0rc2.md)[📈](results/bm-20260921-3.16.0a0-212e603/bm-20260921-macm4pro-arm64-python-212e6035133957a66f1a-3.16.0a0-212e603-vs-3.13.0rc2.svg) |  |


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
