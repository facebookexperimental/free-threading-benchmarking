# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (a1ec746)](results/bm-20260228-3.15.0a6%2B-a1ec746/bm-20260228-vultr-x86_64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (a1ec746)](results/bm-20260228-3.15.0a6%2B-a1ec746-PYTHON_UOPS/bm-20260228-vultr-x86_64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-pystats.md)
- [Most recent JIT pystats on main (bedaea0)](results/bm-20251019-3.15.0a1%2B-bedaea0-JIT/bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-03-01](results/bm-20260301-3.15.0a6%2B-c9a5d9a-NOGIL) | python/c9a5d9aae48a9faa553a | c9a5d9a (NOGIL) | 1.032x ↓<br>[📄](results/bm-20260301-3.15.0a6%2B-c9a5d9a-NOGIL/bm-20260301-vultr-x86_64-python-c9a5d9aae48a9faa553a-3.15.0a6%2B-c9a5d9a-vs-3.12.6.md)[📈](results/bm-20260301-3.15.0a6%2B-c9a5d9a-NOGIL/bm-20260301-vultr-x86_64-python-c9a5d9aae48a9faa553a-3.15.0a6%2B-c9a5d9a-vs-3.12.6.svg) | 1.064x ↓<br>[📄](results/bm-20260301-3.15.0a6%2B-c9a5d9a-NOGIL/bm-20260301-vultr-x86_64-python-c9a5d9aae48a9faa553a-3.15.0a6%2B-c9a5d9a-vs-3.13.0rc2.md)[📈](results/bm-20260301-3.15.0a6%2B-c9a5d9a-NOGIL/bm-20260301-vultr-x86_64-python-c9a5d9aae48a9faa553a-3.15.0a6%2B-c9a5d9a-vs-3.13.0rc2.svg) | 1.100x ↓<br>[📄](results/bm-20260301-3.15.0a6%2B-c9a5d9a-NOGIL/bm-20260301-vultr-x86_64-python-c9a5d9aae48a9faa553a-3.15.0a6%2B-c9a5d9a-vs-base.md)[📈](results/bm-20260301-3.15.0a6%2B-c9a5d9a-NOGIL/bm-20260301-vultr-x86_64-python-c9a5d9aae48a9faa553a-3.15.0a6%2B-c9a5d9a-vs-base.svg)[🧠](results/bm-20260301-3.15.0a6%2B-c9a5d9a-NOGIL/bm-20260301-vultr-x86_64-python-c9a5d9aae48a9faa553a-3.15.0a6%2B-c9a5d9a-vs-base-mem.svg) |
| [2026-03-01](results/bm-20260301-3.15.0a6%2B-c9a5d9a) | python/c9a5d9aae48a9faa553a | c9a5d9a | 1.072x ↑<br>[📄](results/bm-20260301-3.15.0a6%2B-c9a5d9a/bm-20260301-vultr-x86_64-python-c9a5d9aae48a9faa553a-3.15.0a6%2B-c9a5d9a-vs-3.12.6.md)[📈](results/bm-20260301-3.15.0a6%2B-c9a5d9a/bm-20260301-vultr-x86_64-python-c9a5d9aae48a9faa553a-3.15.0a6%2B-c9a5d9a-vs-3.12.6.svg) | 1.036x ↑<br>[📄](results/bm-20260301-3.15.0a6%2B-c9a5d9a/bm-20260301-vultr-x86_64-python-c9a5d9aae48a9faa553a-3.15.0a6%2B-c9a5d9a-vs-3.13.0rc2.md)[📈](results/bm-20260301-3.15.0a6%2B-c9a5d9a/bm-20260301-vultr-x86_64-python-c9a5d9aae48a9faa553a-3.15.0a6%2B-c9a5d9a-vs-3.13.0rc2.svg) |  |
| [2026-02-28](results/bm-20260228-3.15.0a6%2B-a1ec746-NOGIL) | python/a1ec7467874207957519 | a1ec746 (NOGIL) | 1.030x ↓<br>[📄](results/bm-20260228-3.15.0a6%2B-a1ec746-NOGIL/bm-20260228-vultr-x86_64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-3.12.6.md)[📈](results/bm-20260228-3.15.0a6%2B-a1ec746-NOGIL/bm-20260228-vultr-x86_64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-3.12.6.svg) | 1.062x ↓<br>[📄](results/bm-20260228-3.15.0a6%2B-a1ec746-NOGIL/bm-20260228-vultr-x86_64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-3.13.0rc2.md)[📈](results/bm-20260228-3.15.0a6%2B-a1ec746-NOGIL/bm-20260228-vultr-x86_64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-3.13.0rc2.svg) | 1.103x ↓<br>[📄](results/bm-20260228-3.15.0a6%2B-a1ec746-NOGIL/bm-20260228-vultr-x86_64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-base.md)[📈](results/bm-20260228-3.15.0a6%2B-a1ec746-NOGIL/bm-20260228-vultr-x86_64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-base.svg)[🧠](results/bm-20260228-3.15.0a6%2B-a1ec746-NOGIL/bm-20260228-vultr-x86_64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-base-mem.svg) |
| [2026-02-28](results/bm-20260228-3.15.0a6%2B-a1ec746-JIT) | python/a1ec7467874207957519 | a1ec746 (JIT) | 1.135x ↑<br>[📄](results/bm-20260228-3.15.0a6%2B-a1ec746-JIT/bm-20260228-vultr-x86_64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-3.12.6.md)[📈](results/bm-20260228-3.15.0a6%2B-a1ec746-JIT/bm-20260228-vultr-x86_64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-3.12.6.svg) | 1.098x ↑<br>[📄](results/bm-20260228-3.15.0a6%2B-a1ec746-JIT/bm-20260228-vultr-x86_64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-3.13.0rc2.md)[📈](results/bm-20260228-3.15.0a6%2B-a1ec746-JIT/bm-20260228-vultr-x86_64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-3.13.0rc2.svg) | 1.048x ↑<br>[📄](results/bm-20260228-3.15.0a6%2B-a1ec746-JIT/bm-20260228-vultr-x86_64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-base.md)[📈](results/bm-20260228-3.15.0a6%2B-a1ec746-JIT/bm-20260228-vultr-x86_64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-base.svg)[🧠](results/bm-20260228-3.15.0a6%2B-a1ec746-JIT/bm-20260228-vultr-x86_64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-base-mem.svg) |
| [2026-02-28](results/bm-20260228-3.15.0a6%2B-a1ec746-CLANG) | python/a1ec7467874207957519 | a1ec746 (CLANG) | 1.133x ↑<br>[📄](results/bm-20260228-3.15.0a6%2B-a1ec746-CLANG/bm-20260228-vultr-x86_64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-3.12.6.md)[📈](results/bm-20260228-3.15.0a6%2B-a1ec746-CLANG/bm-20260228-vultr-x86_64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-3.12.6.svg) | 1.096x ↑<br>[📄](results/bm-20260228-3.15.0a6%2B-a1ec746-CLANG/bm-20260228-vultr-x86_64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-3.13.0rc2.md)[📈](results/bm-20260228-3.15.0a6%2B-a1ec746-CLANG/bm-20260228-vultr-x86_64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-3.13.0rc2.svg) | 1.051x ↑<br>[📄](results/bm-20260228-3.15.0a6%2B-a1ec746-CLANG/bm-20260228-vultr-x86_64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-base.md)[📈](results/bm-20260228-3.15.0a6%2B-a1ec746-CLANG/bm-20260228-vultr-x86_64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-base.svg)[🧠](results/bm-20260228-3.15.0a6%2B-a1ec746-CLANG/bm-20260228-vultr-x86_64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-base-mem.svg) |
| [2026-02-28](results/bm-20260228-3.15.0a6%2B-a1ec746) | python/a1ec7467874207957519 | a1ec746 | 1.076x ↑<br>[📄](results/bm-20260228-3.15.0a6%2B-a1ec746/bm-20260228-vultr-x86_64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-3.12.6.md)[📈](results/bm-20260228-3.15.0a6%2B-a1ec746/bm-20260228-vultr-x86_64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-3.12.6.svg) | 1.040x ↑<br>[📄](results/bm-20260228-3.15.0a6%2B-a1ec746/bm-20260228-vultr-x86_64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-3.13.0rc2.md)[📈](results/bm-20260228-3.15.0a6%2B-a1ec746/bm-20260228-vultr-x86_64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-3.13.0rc2.svg) |  |
| [2026-02-28](results/bm-20260228-3.15.0a6%2B-180d58c-NOGIL) | python/180d58cbcc0f7f34d6ba | 180d58c (NOGIL) | 1.031x ↓<br>[📄](results/bm-20260228-3.15.0a6%2B-180d58c-NOGIL/bm-20260228-vultr-x86_64-python-180d58cbcc0f7f34d6ba-3.15.0a6%2B-180d58c-vs-3.12.6.md)[📈](results/bm-20260228-3.15.0a6%2B-180d58c-NOGIL/bm-20260228-vultr-x86_64-python-180d58cbcc0f7f34d6ba-3.15.0a6%2B-180d58c-vs-3.12.6.svg) | 1.063x ↓<br>[📄](results/bm-20260228-3.15.0a6%2B-180d58c-NOGIL/bm-20260228-vultr-x86_64-python-180d58cbcc0f7f34d6ba-3.15.0a6%2B-180d58c-vs-3.13.0rc2.md)[📈](results/bm-20260228-3.15.0a6%2B-180d58c-NOGIL/bm-20260228-vultr-x86_64-python-180d58cbcc0f7f34d6ba-3.15.0a6%2B-180d58c-vs-3.13.0rc2.svg) | 1.099x ↓<br>[📄](results/bm-20260228-3.15.0a6%2B-180d58c-NOGIL/bm-20260228-vultr-x86_64-python-180d58cbcc0f7f34d6ba-3.15.0a6%2B-180d58c-vs-base.md)[📈](results/bm-20260228-3.15.0a6%2B-180d58c-NOGIL/bm-20260228-vultr-x86_64-python-180d58cbcc0f7f34d6ba-3.15.0a6%2B-180d58c-vs-base.svg)[🧠](results/bm-20260228-3.15.0a6%2B-180d58c-NOGIL/bm-20260228-vultr-x86_64-python-180d58cbcc0f7f34d6ba-3.15.0a6%2B-180d58c-vs-base-mem.svg) |
| [2026-02-28](results/bm-20260228-3.15.0a6%2B-180d58c) | python/180d58cbcc0f7f34d6ba | 180d58c | 1.070x ↑<br>[📄](results/bm-20260228-3.15.0a6%2B-180d58c/bm-20260228-vultr-x86_64-python-180d58cbcc0f7f34d6ba-3.15.0a6%2B-180d58c-vs-3.12.6.md)[📈](results/bm-20260228-3.15.0a6%2B-180d58c/bm-20260228-vultr-x86_64-python-180d58cbcc0f7f34d6ba-3.15.0a6%2B-180d58c-vs-3.12.6.svg) | 1.034x ↑<br>[📄](results/bm-20260228-3.15.0a6%2B-180d58c/bm-20260228-vultr-x86_64-python-180d58cbcc0f7f34d6ba-3.15.0a6%2B-180d58c-vs-3.13.0rc2.md)[📈](results/bm-20260228-3.15.0a6%2B-180d58c/bm-20260228-vultr-x86_64-python-180d58cbcc0f7f34d6ba-3.15.0a6%2B-180d58c-vs-3.13.0rc2.svg) |  |
| [2026-02-26](results/bm-20260226-3.15.0a6%2B-06b0920-NOGIL) | python/06b0920f1292690a22ab | 06b0920 (NOGIL) | 1.035x ↓<br>[📄](results/bm-20260226-3.15.0a6%2B-06b0920-NOGIL/bm-20260226-vultr-x86_64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-3.12.6.md)[📈](results/bm-20260226-3.15.0a6%2B-06b0920-NOGIL/bm-20260226-vultr-x86_64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-3.12.6.svg) | 1.068x ↓<br>[📄](results/bm-20260226-3.15.0a6%2B-06b0920-NOGIL/bm-20260226-vultr-x86_64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-3.13.0rc2.md)[📈](results/bm-20260226-3.15.0a6%2B-06b0920-NOGIL/bm-20260226-vultr-x86_64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-3.13.0rc2.svg) | 1.106x ↓<br>[📄](results/bm-20260226-3.15.0a6%2B-06b0920-NOGIL/bm-20260226-vultr-x86_64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-base.md)[📈](results/bm-20260226-3.15.0a6%2B-06b0920-NOGIL/bm-20260226-vultr-x86_64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-base.svg)[🧠](results/bm-20260226-3.15.0a6%2B-06b0920-NOGIL/bm-20260226-vultr-x86_64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-base-mem.svg) |
| [2026-02-26](results/bm-20260226-3.15.0a6%2B-06b0920) | python/06b0920f1292690a22ab | 06b0920 | 1.074x ↑<br>[📄](results/bm-20260226-3.15.0a6%2B-06b0920/bm-20260226-vultr-x86_64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-3.12.6.md)[📈](results/bm-20260226-3.15.0a6%2B-06b0920/bm-20260226-vultr-x86_64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-3.12.6.svg) | 1.038x ↑<br>[📄](results/bm-20260226-3.15.0a6%2B-06b0920/bm-20260226-vultr-x86_64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-3.13.0rc2.md)[📈](results/bm-20260226-3.15.0a6%2B-06b0920/bm-20260226-vultr-x86_64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-03-01](results/bm-20260301-3.15.0a6%2B-c9a5d9a-NOGIL) | python/c9a5d9aae48a9faa553a | c9a5d9a (NOGIL) | 1.101x ↑<br>[📄](results/bm-20260301-3.15.0a6%2B-c9a5d9a-NOGIL/bm-20260301-macm4pro-arm64-python-c9a5d9aae48a9faa553a-3.15.0a6%2B-c9a5d9a-vs-3.12.6.md)[📈](results/bm-20260301-3.15.0a6%2B-c9a5d9a-NOGIL/bm-20260301-macm4pro-arm64-python-c9a5d9aae48a9faa553a-3.15.0a6%2B-c9a5d9a-vs-3.12.6.svg) | 1.022x ↑<br>[📄](results/bm-20260301-3.15.0a6%2B-c9a5d9a-NOGIL/bm-20260301-macm4pro-arm64-python-c9a5d9aae48a9faa553a-3.15.0a6%2B-c9a5d9a-vs-3.13.0rc2.md)[📈](results/bm-20260301-3.15.0a6%2B-c9a5d9a-NOGIL/bm-20260301-macm4pro-arm64-python-c9a5d9aae48a9faa553a-3.15.0a6%2B-c9a5d9a-vs-3.13.0rc2.svg) | 1.059x ↓<br>[📄](results/bm-20260301-3.15.0a6%2B-c9a5d9a-NOGIL/bm-20260301-macm4pro-arm64-python-c9a5d9aae48a9faa553a-3.15.0a6%2B-c9a5d9a-vs-base.md)[📈](results/bm-20260301-3.15.0a6%2B-c9a5d9a-NOGIL/bm-20260301-macm4pro-arm64-python-c9a5d9aae48a9faa553a-3.15.0a6%2B-c9a5d9a-vs-base.svg)[🧠](results/bm-20260301-3.15.0a6%2B-c9a5d9a-NOGIL/bm-20260301-macm4pro-arm64-python-c9a5d9aae48a9faa553a-3.15.0a6%2B-c9a5d9a-vs-base-mem.svg) |
| [2026-03-01](results/bm-20260301-3.15.0a6%2B-c9a5d9a) | python/c9a5d9aae48a9faa553a | c9a5d9a | 1.169x ↑<br>[📄](results/bm-20260301-3.15.0a6%2B-c9a5d9a/bm-20260301-macm4pro-arm64-python-c9a5d9aae48a9faa553a-3.15.0a6%2B-c9a5d9a-vs-3.12.6.md)[📈](results/bm-20260301-3.15.0a6%2B-c9a5d9a/bm-20260301-macm4pro-arm64-python-c9a5d9aae48a9faa553a-3.15.0a6%2B-c9a5d9a-vs-3.12.6.svg) | 1.085x ↑<br>[📄](results/bm-20260301-3.15.0a6%2B-c9a5d9a/bm-20260301-macm4pro-arm64-python-c9a5d9aae48a9faa553a-3.15.0a6%2B-c9a5d9a-vs-3.13.0rc2.md)[📈](results/bm-20260301-3.15.0a6%2B-c9a5d9a/bm-20260301-macm4pro-arm64-python-c9a5d9aae48a9faa553a-3.15.0a6%2B-c9a5d9a-vs-3.13.0rc2.svg) |  |
| [2026-02-28](results/bm-20260228-3.15.0a6%2B-a1ec746-NOGIL) | python/a1ec7467874207957519 | a1ec746 (NOGIL) | 1.103x ↑<br>[📄](results/bm-20260228-3.15.0a6%2B-a1ec746-NOGIL/bm-20260228-macm4pro-arm64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-3.12.6.md)[📈](results/bm-20260228-3.15.0a6%2B-a1ec746-NOGIL/bm-20260228-macm4pro-arm64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-3.12.6.svg) | 1.023x ↑<br>[📄](results/bm-20260228-3.15.0a6%2B-a1ec746-NOGIL/bm-20260228-macm4pro-arm64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-3.13.0rc2.md)[📈](results/bm-20260228-3.15.0a6%2B-a1ec746-NOGIL/bm-20260228-macm4pro-arm64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-3.13.0rc2.svg) | 1.042x ↓<br>[📄](results/bm-20260228-3.15.0a6%2B-a1ec746-NOGIL/bm-20260228-macm4pro-arm64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-base.md)[📈](results/bm-20260228-3.15.0a6%2B-a1ec746-NOGIL/bm-20260228-macm4pro-arm64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-base.svg)[🧠](results/bm-20260228-3.15.0a6%2B-a1ec746-NOGIL/bm-20260228-macm4pro-arm64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-base-mem.svg) |
| [2026-02-28](results/bm-20260228-3.15.0a6%2B-a1ec746-CLANG) | python/a1ec7467874207957519 | a1ec746 (CLANG) | 1.179x ↑<br>[📄](results/bm-20260228-3.15.0a6%2B-a1ec746-CLANG/bm-20260228-macm4pro-arm64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-3.12.6.md)[📈](results/bm-20260228-3.15.0a6%2B-a1ec746-CLANG/bm-20260228-macm4pro-arm64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-3.12.6.svg) | 1.094x ↑<br>[📄](results/bm-20260228-3.15.0a6%2B-a1ec746-CLANG/bm-20260228-macm4pro-arm64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-3.13.0rc2.md)[📈](results/bm-20260228-3.15.0a6%2B-a1ec746-CLANG/bm-20260228-macm4pro-arm64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-3.13.0rc2.svg) | 1.026x ↑<br>[📄](results/bm-20260228-3.15.0a6%2B-a1ec746-CLANG/bm-20260228-macm4pro-arm64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-base.md)[📈](results/bm-20260228-3.15.0a6%2B-a1ec746-CLANG/bm-20260228-macm4pro-arm64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-base.svg)[🧠](results/bm-20260228-3.15.0a6%2B-a1ec746-CLANG/bm-20260228-macm4pro-arm64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-base-mem.svg) |
| [2026-02-28](results/bm-20260228-3.15.0a6%2B-a1ec746) | python/a1ec7467874207957519 | a1ec746 | 1.151x ↑<br>[📄](results/bm-20260228-3.15.0a6%2B-a1ec746/bm-20260228-macm4pro-arm64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-3.12.6.md)[📈](results/bm-20260228-3.15.0a6%2B-a1ec746/bm-20260228-macm4pro-arm64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-3.12.6.svg) | 1.068x ↑<br>[📄](results/bm-20260228-3.15.0a6%2B-a1ec746/bm-20260228-macm4pro-arm64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-3.13.0rc2.md)[📈](results/bm-20260228-3.15.0a6%2B-a1ec746/bm-20260228-macm4pro-arm64-python-a1ec7467874207957519-3.15.0a6%2B-a1ec746-vs-3.13.0rc2.svg) |  |
| [2026-02-28](results/bm-20260228-3.15.0a6%2B-180d58c-NOGIL) | python/180d58cbcc0f7f34d6ba | 180d58c (NOGIL) | 1.090x ↑<br>[📄](results/bm-20260228-3.15.0a6%2B-180d58c-NOGIL/bm-20260228-macm4pro-arm64-python-180d58cbcc0f7f34d6ba-3.15.0a6%2B-180d58c-vs-3.12.6.md)[📈](results/bm-20260228-3.15.0a6%2B-180d58c-NOGIL/bm-20260228-macm4pro-arm64-python-180d58cbcc0f7f34d6ba-3.15.0a6%2B-180d58c-vs-3.12.6.svg) | 1.011x ↑<br>[📄](results/bm-20260228-3.15.0a6%2B-180d58c-NOGIL/bm-20260228-macm4pro-arm64-python-180d58cbcc0f7f34d6ba-3.15.0a6%2B-180d58c-vs-3.13.0rc2.md)[📈](results/bm-20260228-3.15.0a6%2B-180d58c-NOGIL/bm-20260228-macm4pro-arm64-python-180d58cbcc0f7f34d6ba-3.15.0a6%2B-180d58c-vs-3.13.0rc2.svg) |  |
| [2026-02-26](results/bm-20260226-3.15.0a6%2B-06b0920-NOGIL) | python/06b0920f1292690a22ab | 06b0920 (NOGIL) | 1.087x ↑<br>[📄](results/bm-20260226-3.15.0a6%2B-06b0920-NOGIL/bm-20260226-macm4pro-arm64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-3.12.6.md)[📈](results/bm-20260226-3.15.0a6%2B-06b0920-NOGIL/bm-20260226-macm4pro-arm64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-3.12.6.svg) | 1.009x ↑<br>[📄](results/bm-20260226-3.15.0a6%2B-06b0920-NOGIL/bm-20260226-macm4pro-arm64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-3.13.0rc2.md)[📈](results/bm-20260226-3.15.0a6%2B-06b0920-NOGIL/bm-20260226-macm4pro-arm64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-3.13.0rc2.svg) | 1.059x ↓<br>[📄](results/bm-20260226-3.15.0a6%2B-06b0920-NOGIL/bm-20260226-macm4pro-arm64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-base.md)[📈](results/bm-20260226-3.15.0a6%2B-06b0920-NOGIL/bm-20260226-macm4pro-arm64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-base.svg)[🧠](results/bm-20260226-3.15.0a6%2B-06b0920-NOGIL/bm-20260226-macm4pro-arm64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-base-mem.svg) |
| [2026-02-26](results/bm-20260226-3.15.0a6%2B-06b0920) | python/06b0920f1292690a22ab | 06b0920 | 1.154x ↑<br>[📄](results/bm-20260226-3.15.0a6%2B-06b0920/bm-20260226-macm4pro-arm64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-3.12.6.md)[📈](results/bm-20260226-3.15.0a6%2B-06b0920/bm-20260226-macm4pro-arm64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-3.12.6.svg) | 1.070x ↑<br>[📄](results/bm-20260226-3.15.0a6%2B-06b0920/bm-20260226-macm4pro-arm64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-3.13.0rc2.md)[📈](results/bm-20260226-3.15.0a6%2B-06b0920/bm-20260226-macm4pro-arm64-python-06b0920f1292690a22ab-3.15.0a6%2B-06b0920-vs-3.13.0rc2.svg) |  |


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
