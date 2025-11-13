# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (2f60b8f)](results/bm-20251101-3.15.0a1%2B-2f60b8f/bm-20251101-vultr-x86_64-python-2f60b8f02fe7cb83dd58-3.15.0a1%2B-2f60b8f-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (2f60b8f)](results/bm-20251101-3.15.0a1%2B-2f60b8f-PYTHON_UOPS/bm-20251101-vultr-x86_64-python-2f60b8f02fe7cb83dd58-3.15.0a1%2B-2f60b8f-pystats.md)
- [Most recent JIT pystats on main (bedaea0)](results/bm-20251019-3.15.0a1%2B-bedaea0-JIT/bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-11-12](results/bm-20251112-3.15.0a1%2B-26b7df2-NOGIL) | python/26b7df2430cd5a9ee772 | 26b7df2 (NOGIL) | 1.018x ↓<br>[📄](results/bm-20251112-3.15.0a1%2B-26b7df2-NOGIL/bm-20251112-vultr-x86_64-python-26b7df2430cd5a9ee772-3.15.0a1%2B-26b7df2-vs-3.12.6.md)[📈](results/bm-20251112-3.15.0a1%2B-26b7df2-NOGIL/bm-20251112-vultr-x86_64-python-26b7df2430cd5a9ee772-3.15.0a1%2B-26b7df2-vs-3.12.6.svg) | 1.051x ↓<br>[📄](results/bm-20251112-3.15.0a1%2B-26b7df2-NOGIL/bm-20251112-vultr-x86_64-python-26b7df2430cd5a9ee772-3.15.0a1%2B-26b7df2-vs-3.13.0rc2.md)[📈](results/bm-20251112-3.15.0a1%2B-26b7df2-NOGIL/bm-20251112-vultr-x86_64-python-26b7df2430cd5a9ee772-3.15.0a1%2B-26b7df2-vs-3.13.0rc2.svg) | 1.089x ↓<br>[📄](results/bm-20251112-3.15.0a1%2B-26b7df2-NOGIL/bm-20251112-vultr-x86_64-python-26b7df2430cd5a9ee772-3.15.0a1%2B-26b7df2-vs-base.md)[📈](results/bm-20251112-3.15.0a1%2B-26b7df2-NOGIL/bm-20251112-vultr-x86_64-python-26b7df2430cd5a9ee772-3.15.0a1%2B-26b7df2-vs-base.svg)[🧠](results/bm-20251112-3.15.0a1%2B-26b7df2-NOGIL/bm-20251112-vultr-x86_64-python-26b7df2430cd5a9ee772-3.15.0a1%2B-26b7df2-vs-base-mem.svg) |
| [2025-11-12](results/bm-20251112-3.15.0a1%2B-26b7df2) | python/26b7df2430cd5a9ee772 | 26b7df2 | 1.074x ↑<br>[📄](results/bm-20251112-3.15.0a1%2B-26b7df2/bm-20251112-vultr-x86_64-python-26b7df2430cd5a9ee772-3.15.0a1%2B-26b7df2-vs-3.12.6.md)[📈](results/bm-20251112-3.15.0a1%2B-26b7df2/bm-20251112-vultr-x86_64-python-26b7df2430cd5a9ee772-3.15.0a1%2B-26b7df2-vs-3.12.6.svg) | 1.038x ↑<br>[📄](results/bm-20251112-3.15.0a1%2B-26b7df2/bm-20251112-vultr-x86_64-python-26b7df2430cd5a9ee772-3.15.0a1%2B-26b7df2-vs-3.13.0rc2.md)[📈](results/bm-20251112-3.15.0a1%2B-26b7df2/bm-20251112-vultr-x86_64-python-26b7df2430cd5a9ee772-3.15.0a1%2B-26b7df2-vs-3.13.0rc2.svg) |  |
| [2025-11-12](results/bm-20251112-3.15.0a1%2B-f8a764a-JIT) | Fidget-Spinner/tracing_jit | f8a764a (JIT) | 1.096x ↑<br>[📄](results/bm-20251112-3.15.0a1%2B-f8a764a-JIT/bm-20251112-vultr-x86_64-Fidget%252dSpinner-tracing_jit-3.15.0a1%2B-f8a764a-vs-3.12.6.md)[📈](results/bm-20251112-3.15.0a1%2B-f8a764a-JIT/bm-20251112-vultr-x86_64-Fidget%252dSpinner-tracing_jit-3.15.0a1%2B-f8a764a-vs-3.12.6.svg) | 1.059x ↑<br>[📄](results/bm-20251112-3.15.0a1%2B-f8a764a-JIT/bm-20251112-vultr-x86_64-Fidget%252dSpinner-tracing_jit-3.15.0a1%2B-f8a764a-vs-3.13.0rc2.md)[📈](results/bm-20251112-3.15.0a1%2B-f8a764a-JIT/bm-20251112-vultr-x86_64-Fidget%252dSpinner-tracing_jit-3.15.0a1%2B-f8a764a-vs-3.13.0rc2.svg) | 1.007x ↑<br>[📄](results/bm-20251112-3.15.0a1%2B-f8a764a-JIT/bm-20251112-vultr-x86_64-Fidget%252dSpinner-tracing_jit-3.15.0a1%2B-f8a764a-vs-base.md)[📈](results/bm-20251112-3.15.0a1%2B-f8a764a-JIT/bm-20251112-vultr-x86_64-Fidget%252dSpinner-tracing_jit-3.15.0a1%2B-f8a764a-vs-base.svg)[🧠](results/bm-20251112-3.15.0a1%2B-f8a764a-JIT/bm-20251112-vultr-x86_64-Fidget%252dSpinner-tracing_jit-3.15.0a1%2B-f8a764a-vs-base-mem.svg) |
| [2025-11-12](results/bm-20251112-3.15.0a1%2B-0d7b48a-NOGIL) | python/0d7b48a8f5de5c1c6d57 | 0d7b48a (NOGIL) | 1.017x ↓<br>[📄](results/bm-20251112-3.15.0a1%2B-0d7b48a-NOGIL/bm-20251112-vultr-x86_64-python-0d7b48a8f5de5c1c6d57-3.15.0a1%2B-0d7b48a-vs-3.12.6.md)[📈](results/bm-20251112-3.15.0a1%2B-0d7b48a-NOGIL/bm-20251112-vultr-x86_64-python-0d7b48a8f5de5c1c6d57-3.15.0a1%2B-0d7b48a-vs-3.12.6.svg) | 1.050x ↓<br>[📄](results/bm-20251112-3.15.0a1%2B-0d7b48a-NOGIL/bm-20251112-vultr-x86_64-python-0d7b48a8f5de5c1c6d57-3.15.0a1%2B-0d7b48a-vs-3.13.0rc2.md)[📈](results/bm-20251112-3.15.0a1%2B-0d7b48a-NOGIL/bm-20251112-vultr-x86_64-python-0d7b48a8f5de5c1c6d57-3.15.0a1%2B-0d7b48a-vs-3.13.0rc2.svg) | 1.090x ↓<br>[📄](results/bm-20251112-3.15.0a1%2B-0d7b48a-NOGIL/bm-20251112-vultr-x86_64-python-0d7b48a8f5de5c1c6d57-3.15.0a1%2B-0d7b48a-vs-base.md)[📈](results/bm-20251112-3.15.0a1%2B-0d7b48a-NOGIL/bm-20251112-vultr-x86_64-python-0d7b48a8f5de5c1c6d57-3.15.0a1%2B-0d7b48a-vs-base.svg)[🧠](results/bm-20251112-3.15.0a1%2B-0d7b48a-NOGIL/bm-20251112-vultr-x86_64-python-0d7b48a8f5de5c1c6d57-3.15.0a1%2B-0d7b48a-vs-base-mem.svg) |
| [2025-11-12](results/bm-20251112-3.15.0a1%2B-0d7b48a) | python/0d7b48a8f5de5c1c6d57 | 0d7b48a | 1.076x ↑<br>[📄](results/bm-20251112-3.15.0a1%2B-0d7b48a/bm-20251112-vultr-x86_64-python-0d7b48a8f5de5c1c6d57-3.15.0a1%2B-0d7b48a-vs-3.12.6.md)[📈](results/bm-20251112-3.15.0a1%2B-0d7b48a/bm-20251112-vultr-x86_64-python-0d7b48a8f5de5c1c6d57-3.15.0a1%2B-0d7b48a-vs-3.12.6.svg) | 1.041x ↑<br>[📄](results/bm-20251112-3.15.0a1%2B-0d7b48a/bm-20251112-vultr-x86_64-python-0d7b48a8f5de5c1c6d57-3.15.0a1%2B-0d7b48a-vs-3.13.0rc2.md)[📈](results/bm-20251112-3.15.0a1%2B-0d7b48a/bm-20251112-vultr-x86_64-python-0d7b48a8f5de5c1c6d57-3.15.0a1%2B-0d7b48a-vs-3.13.0rc2.svg) |  |
| [2025-11-10](results/bm-20251110-3.15.0a1%2B-86513f6-NOGIL) | python/86513f6c2ebdd1fb692c | 86513f6 (NOGIL) | 1.021x ↓<br>[📄](results/bm-20251110-3.15.0a1%2B-86513f6-NOGIL/bm-20251110-vultr-x86_64-python-86513f6c2ebdd1fb692c-3.15.0a1%2B-86513f6-vs-3.12.6.md)[📈](results/bm-20251110-3.15.0a1%2B-86513f6-NOGIL/bm-20251110-vultr-x86_64-python-86513f6c2ebdd1fb692c-3.15.0a1%2B-86513f6-vs-3.12.6.svg) | 1.054x ↓<br>[📄](results/bm-20251110-3.15.0a1%2B-86513f6-NOGIL/bm-20251110-vultr-x86_64-python-86513f6c2ebdd1fb692c-3.15.0a1%2B-86513f6-vs-3.13.0rc2.md)[📈](results/bm-20251110-3.15.0a1%2B-86513f6-NOGIL/bm-20251110-vultr-x86_64-python-86513f6c2ebdd1fb692c-3.15.0a1%2B-86513f6-vs-3.13.0rc2.svg) | 1.094x ↓<br>[📄](results/bm-20251110-3.15.0a1%2B-86513f6-NOGIL/bm-20251110-vultr-x86_64-python-86513f6c2ebdd1fb692c-3.15.0a1%2B-86513f6-vs-base.md)[📈](results/bm-20251110-3.15.0a1%2B-86513f6-NOGIL/bm-20251110-vultr-x86_64-python-86513f6c2ebdd1fb692c-3.15.0a1%2B-86513f6-vs-base.svg)[🧠](results/bm-20251110-3.15.0a1%2B-86513f6-NOGIL/bm-20251110-vultr-x86_64-python-86513f6c2ebdd1fb692c-3.15.0a1%2B-86513f6-vs-base-mem.svg) |
| [2025-11-10](results/bm-20251110-3.15.0a1%2B-86513f6) | python/86513f6c2ebdd1fb692c | 86513f6 | 1.075x ↑<br>[📄](results/bm-20251110-3.15.0a1%2B-86513f6/bm-20251110-vultr-x86_64-python-86513f6c2ebdd1fb692c-3.15.0a1%2B-86513f6-vs-3.12.6.md)[📈](results/bm-20251110-3.15.0a1%2B-86513f6/bm-20251110-vultr-x86_64-python-86513f6c2ebdd1fb692c-3.15.0a1%2B-86513f6-vs-3.12.6.svg) | 1.040x ↑<br>[📄](results/bm-20251110-3.15.0a1%2B-86513f6/bm-20251110-vultr-x86_64-python-86513f6c2ebdd1fb692c-3.15.0a1%2B-86513f6-vs-3.13.0rc2.md)[📈](results/bm-20251110-3.15.0a1%2B-86513f6/bm-20251110-vultr-x86_64-python-86513f6c2ebdd1fb692c-3.15.0a1%2B-86513f6-vs-3.13.0rc2.svg) |  |
| [2025-11-09](results/bm-20251109-3.15.0a1%2B-b618731-NOGIL) | python/b618731781c31d4b5b75 | b618731 (NOGIL) | 1.019x ↓<br>[📄](results/bm-20251109-3.15.0a1%2B-b618731-NOGIL/bm-20251109-vultr-x86_64-python-b618731781c31d4b5b75-3.15.0a1%2B-b618731-vs-3.12.6.md)[📈](results/bm-20251109-3.15.0a1%2B-b618731-NOGIL/bm-20251109-vultr-x86_64-python-b618731781c31d4b5b75-3.15.0a1%2B-b618731-vs-3.12.6.svg) | 1.052x ↓<br>[📄](results/bm-20251109-3.15.0a1%2B-b618731-NOGIL/bm-20251109-vultr-x86_64-python-b618731781c31d4b5b75-3.15.0a1%2B-b618731-vs-3.13.0rc2.md)[📈](results/bm-20251109-3.15.0a1%2B-b618731-NOGIL/bm-20251109-vultr-x86_64-python-b618731781c31d4b5b75-3.15.0a1%2B-b618731-vs-3.13.0rc2.svg) | 1.101x ↓<br>[📄](results/bm-20251109-3.15.0a1%2B-b618731-NOGIL/bm-20251109-vultr-x86_64-python-b618731781c31d4b5b75-3.15.0a1%2B-b618731-vs-base.md)[📈](results/bm-20251109-3.15.0a1%2B-b618731-NOGIL/bm-20251109-vultr-x86_64-python-b618731781c31d4b5b75-3.15.0a1%2B-b618731-vs-base.svg)[🧠](results/bm-20251109-3.15.0a1%2B-b618731-NOGIL/bm-20251109-vultr-x86_64-python-b618731781c31d4b5b75-3.15.0a1%2B-b618731-vs-base-mem.svg) |
| [2025-11-09](results/bm-20251109-3.15.0a1%2B-b618731) | python/b618731781c31d4b5b75 | b618731 | 1.085x ↑<br>[📄](results/bm-20251109-3.15.0a1%2B-b618731/bm-20251109-vultr-x86_64-python-b618731781c31d4b5b75-3.15.0a1%2B-b618731-vs-3.12.6.md)[📈](results/bm-20251109-3.15.0a1%2B-b618731/bm-20251109-vultr-x86_64-python-b618731781c31d4b5b75-3.15.0a1%2B-b618731-vs-3.12.6.svg) | 1.049x ↑<br>[📄](results/bm-20251109-3.15.0a1%2B-b618731/bm-20251109-vultr-x86_64-python-b618731781c31d4b5b75-3.15.0a1%2B-b618731-vs-3.13.0rc2.md)[📈](results/bm-20251109-3.15.0a1%2B-b618731/bm-20251109-vultr-x86_64-python-b618731781c31d4b5b75-3.15.0a1%2B-b618731-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-11-12](results/bm-20251112-3.15.0a1%2B-26b7df2-NOGIL) | python/26b7df2430cd5a9ee772 | 26b7df2 (NOGIL) | 1.084x ↑<br>[📄](results/bm-20251112-3.15.0a1%2B-26b7df2-NOGIL/bm-20251112-macm4pro-arm64-python-26b7df2430cd5a9ee772-3.15.0a1%2B-26b7df2-vs-3.12.6.md)[📈](results/bm-20251112-3.15.0a1%2B-26b7df2-NOGIL/bm-20251112-macm4pro-arm64-python-26b7df2430cd5a9ee772-3.15.0a1%2B-26b7df2-vs-3.12.6.svg) | 1.000x ↓<br>[📄](results/bm-20251112-3.15.0a1%2B-26b7df2-NOGIL/bm-20251112-macm4pro-arm64-python-26b7df2430cd5a9ee772-3.15.0a1%2B-26b7df2-vs-3.13.0rc2.md)[📈](results/bm-20251112-3.15.0a1%2B-26b7df2-NOGIL/bm-20251112-macm4pro-arm64-python-26b7df2430cd5a9ee772-3.15.0a1%2B-26b7df2-vs-3.13.0rc2.svg) | 1.025x ↓<br>[📄](results/bm-20251112-3.15.0a1%2B-26b7df2-NOGIL/bm-20251112-macm4pro-arm64-python-26b7df2430cd5a9ee772-3.15.0a1%2B-26b7df2-vs-base.md)[📈](results/bm-20251112-3.15.0a1%2B-26b7df2-NOGIL/bm-20251112-macm4pro-arm64-python-26b7df2430cd5a9ee772-3.15.0a1%2B-26b7df2-vs-base.svg)[🧠](results/bm-20251112-3.15.0a1%2B-26b7df2-NOGIL/bm-20251112-macm4pro-arm64-python-26b7df2430cd5a9ee772-3.15.0a1%2B-26b7df2-vs-base-mem.svg) |
| [2025-11-12](results/bm-20251112-3.15.0a1%2B-26b7df2) | python/26b7df2430cd5a9ee772 | 26b7df2 | 1.111x ↑<br>[📄](results/bm-20251112-3.15.0a1%2B-26b7df2/bm-20251112-macm4pro-arm64-python-26b7df2430cd5a9ee772-3.15.0a1%2B-26b7df2-vs-3.12.6.md)[📈](results/bm-20251112-3.15.0a1%2B-26b7df2/bm-20251112-macm4pro-arm64-python-26b7df2430cd5a9ee772-3.15.0a1%2B-26b7df2-vs-3.12.6.svg) | 1.024x ↑<br>[📄](results/bm-20251112-3.15.0a1%2B-26b7df2/bm-20251112-macm4pro-arm64-python-26b7df2430cd5a9ee772-3.15.0a1%2B-26b7df2-vs-3.13.0rc2.md)[📈](results/bm-20251112-3.15.0a1%2B-26b7df2/bm-20251112-macm4pro-arm64-python-26b7df2430cd5a9ee772-3.15.0a1%2B-26b7df2-vs-3.13.0rc2.svg) |  |
| [2025-11-12](results/bm-20251112-3.15.0a1%2B-0d7b48a-NOGIL) | python/0d7b48a8f5de5c1c6d57 | 0d7b48a (NOGIL) | 1.082x ↑<br>[📄](results/bm-20251112-3.15.0a1%2B-0d7b48a-NOGIL/bm-20251112-macm4pro-arm64-python-0d7b48a8f5de5c1c6d57-3.15.0a1%2B-0d7b48a-vs-3.12.6.md)[📈](results/bm-20251112-3.15.0a1%2B-0d7b48a-NOGIL/bm-20251112-macm4pro-arm64-python-0d7b48a8f5de5c1c6d57-3.15.0a1%2B-0d7b48a-vs-3.12.6.svg) | 1.002x ↓<br>[📄](results/bm-20251112-3.15.0a1%2B-0d7b48a-NOGIL/bm-20251112-macm4pro-arm64-python-0d7b48a8f5de5c1c6d57-3.15.0a1%2B-0d7b48a-vs-3.13.0rc2.md)[📈](results/bm-20251112-3.15.0a1%2B-0d7b48a-NOGIL/bm-20251112-macm4pro-arm64-python-0d7b48a8f5de5c1c6d57-3.15.0a1%2B-0d7b48a-vs-3.13.0rc2.svg) | 1.029x ↓<br>[📄](results/bm-20251112-3.15.0a1%2B-0d7b48a-NOGIL/bm-20251112-macm4pro-arm64-python-0d7b48a8f5de5c1c6d57-3.15.0a1%2B-0d7b48a-vs-base.md)[📈](results/bm-20251112-3.15.0a1%2B-0d7b48a-NOGIL/bm-20251112-macm4pro-arm64-python-0d7b48a8f5de5c1c6d57-3.15.0a1%2B-0d7b48a-vs-base.svg)[🧠](results/bm-20251112-3.15.0a1%2B-0d7b48a-NOGIL/bm-20251112-macm4pro-arm64-python-0d7b48a8f5de5c1c6d57-3.15.0a1%2B-0d7b48a-vs-base-mem.svg) |
| [2025-11-12](results/bm-20251112-3.15.0a1%2B-0d7b48a) | python/0d7b48a8f5de5c1c6d57 | 0d7b48a | 1.114x ↑<br>[📄](results/bm-20251112-3.15.0a1%2B-0d7b48a/bm-20251112-macm4pro-arm64-python-0d7b48a8f5de5c1c6d57-3.15.0a1%2B-0d7b48a-vs-3.12.6.md)[📈](results/bm-20251112-3.15.0a1%2B-0d7b48a/bm-20251112-macm4pro-arm64-python-0d7b48a8f5de5c1c6d57-3.15.0a1%2B-0d7b48a-vs-3.12.6.svg) | 1.027x ↑<br>[📄](results/bm-20251112-3.15.0a1%2B-0d7b48a/bm-20251112-macm4pro-arm64-python-0d7b48a8f5de5c1c6d57-3.15.0a1%2B-0d7b48a-vs-3.13.0rc2.md)[📈](results/bm-20251112-3.15.0a1%2B-0d7b48a/bm-20251112-macm4pro-arm64-python-0d7b48a8f5de5c1c6d57-3.15.0a1%2B-0d7b48a-vs-3.13.0rc2.svg) |  |
| [2025-11-10](results/bm-20251110-3.15.0a1%2B-86513f6-NOGIL) | python/86513f6c2ebdd1fb692c | 86513f6 (NOGIL) | 1.069x ↑<br>[📄](results/bm-20251110-3.15.0a1%2B-86513f6-NOGIL/bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1%2B-86513f6-vs-3.12.6.md)[📈](results/bm-20251110-3.15.0a1%2B-86513f6-NOGIL/bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1%2B-86513f6-vs-3.12.6.svg) | 1.015x ↓<br>[📄](results/bm-20251110-3.15.0a1%2B-86513f6-NOGIL/bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1%2B-86513f6-vs-3.13.0rc2.md)[📈](results/bm-20251110-3.15.0a1%2B-86513f6-NOGIL/bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1%2B-86513f6-vs-3.13.0rc2.svg) | 1.041x ↓<br>[📄](results/bm-20251110-3.15.0a1%2B-86513f6-NOGIL/bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1%2B-86513f6-vs-base.md)[📈](results/bm-20251110-3.15.0a1%2B-86513f6-NOGIL/bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1%2B-86513f6-vs-base.svg)[🧠](results/bm-20251110-3.15.0a1%2B-86513f6-NOGIL/bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1%2B-86513f6-vs-base-mem.svg) |
| [2025-11-10](results/bm-20251110-3.15.0a1%2B-86513f6) | python/86513f6c2ebdd1fb692c | 86513f6 | 1.113x ↑<br>[📄](results/bm-20251110-3.15.0a1%2B-86513f6/bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1%2B-86513f6-vs-3.12.6.md)[📈](results/bm-20251110-3.15.0a1%2B-86513f6/bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1%2B-86513f6-vs-3.12.6.svg) | 1.026x ↑<br>[📄](results/bm-20251110-3.15.0a1%2B-86513f6/bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1%2B-86513f6-vs-3.13.0rc2.md)[📈](results/bm-20251110-3.15.0a1%2B-86513f6/bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1%2B-86513f6-vs-3.13.0rc2.svg) |  |
| [2025-11-09](results/bm-20251109-3.15.0a1%2B-b618731-NOGIL) | python/b618731781c31d4b5b75 | b618731 (NOGIL) | 1.085x ↑<br>[📄](results/bm-20251109-3.15.0a1%2B-b618731-NOGIL/bm-20251109-macm4pro-arm64-python-b618731781c31d4b5b75-3.15.0a1%2B-b618731-vs-3.12.6.md)[📈](results/bm-20251109-3.15.0a1%2B-b618731-NOGIL/bm-20251109-macm4pro-arm64-python-b618731781c31d4b5b75-3.15.0a1%2B-b618731-vs-3.12.6.svg) | 1.006x ↑<br>[📄](results/bm-20251109-3.15.0a1%2B-b618731-NOGIL/bm-20251109-macm4pro-arm64-python-b618731781c31d4b5b75-3.15.0a1%2B-b618731-vs-3.13.0rc2.md)[📈](results/bm-20251109-3.15.0a1%2B-b618731-NOGIL/bm-20251109-macm4pro-arm64-python-b618731781c31d4b5b75-3.15.0a1%2B-b618731-vs-3.13.0rc2.svg) | 1.021x ↓<br>[📄](results/bm-20251109-3.15.0a1%2B-b618731-NOGIL/bm-20251109-macm4pro-arm64-python-b618731781c31d4b5b75-3.15.0a1%2B-b618731-vs-base.md)[📈](results/bm-20251109-3.15.0a1%2B-b618731-NOGIL/bm-20251109-macm4pro-arm64-python-b618731781c31d4b5b75-3.15.0a1%2B-b618731-vs-base.svg)[🧠](results/bm-20251109-3.15.0a1%2B-b618731-NOGIL/bm-20251109-macm4pro-arm64-python-b618731781c31d4b5b75-3.15.0a1%2B-b618731-vs-base-mem.svg) |
| [2025-11-09](results/bm-20251109-3.15.0a1%2B-b618731) | python/b618731781c31d4b5b75 | b618731 | 1.107x ↑<br>[📄](results/bm-20251109-3.15.0a1%2B-b618731/bm-20251109-macm4pro-arm64-python-b618731781c31d4b5b75-3.15.0a1%2B-b618731-vs-3.12.6.md)[📈](results/bm-20251109-3.15.0a1%2B-b618731/bm-20251109-macm4pro-arm64-python-b618731781c31d4b5b75-3.15.0a1%2B-b618731-vs-3.12.6.svg) | 1.026x ↑<br>[📄](results/bm-20251109-3.15.0a1%2B-b618731/bm-20251109-macm4pro-arm64-python-b618731781c31d4b5b75-3.15.0a1%2B-b618731-vs-3.13.0rc2.md)[📈](results/bm-20251109-3.15.0a1%2B-b618731/bm-20251109-macm4pro-arm64-python-b618731781c31d4b5b75-3.15.0a1%2B-b618731-vs-3.13.0rc2.svg) |  |


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
