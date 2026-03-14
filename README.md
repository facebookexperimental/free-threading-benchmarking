# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (149c465)](results/bm-20260307-3.15.0a6%2B-149c465/bm-20260307-vultr-x86_64-python-149c4657507d17f78dd0-3.15.0a6%2B-149c465-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (149c465)](results/bm-20260307-3.15.0a6%2B-149c465-PYTHON_UOPS/bm-20260307-vultr-x86_64-python-149c4657507d17f78dd0-3.15.0a6%2B-149c465-pystats.md)
- [Most recent JIT pystats on main (bedaea0)](results/bm-20251019-3.15.0a1%2B-bedaea0-JIT/bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-03-13](results/bm-20260313-3.15.0a7%2B-3c38feb-NOGIL) | python/3c38feb2a21aacdb009e | 3c38feb (NOGIL) | 1.022x ↓<br>[📄](results/bm-20260313-3.15.0a7%2B-3c38feb-NOGIL/bm-20260313-vultr-x86_64-python-3c38feb2a21aacdb009e-3.15.0a7%2B-3c38feb-vs-3.12.6.md)[📈](results/bm-20260313-3.15.0a7%2B-3c38feb-NOGIL/bm-20260313-vultr-x86_64-python-3c38feb2a21aacdb009e-3.15.0a7%2B-3c38feb-vs-3.12.6.svg) | 1.055x ↓<br>[📄](results/bm-20260313-3.15.0a7%2B-3c38feb-NOGIL/bm-20260313-vultr-x86_64-python-3c38feb2a21aacdb009e-3.15.0a7%2B-3c38feb-vs-3.13.0rc2.md)[📈](results/bm-20260313-3.15.0a7%2B-3c38feb-NOGIL/bm-20260313-vultr-x86_64-python-3c38feb2a21aacdb009e-3.15.0a7%2B-3c38feb-vs-3.13.0rc2.svg) | 1.093x ↓<br>[📄](results/bm-20260313-3.15.0a7%2B-3c38feb-NOGIL/bm-20260313-vultr-x86_64-python-3c38feb2a21aacdb009e-3.15.0a7%2B-3c38feb-vs-base.md)[📈](results/bm-20260313-3.15.0a7%2B-3c38feb-NOGIL/bm-20260313-vultr-x86_64-python-3c38feb2a21aacdb009e-3.15.0a7%2B-3c38feb-vs-base.svg)[🧠](results/bm-20260313-3.15.0a7%2B-3c38feb-NOGIL/bm-20260313-vultr-x86_64-python-3c38feb2a21aacdb009e-3.15.0a7%2B-3c38feb-vs-base-mem.svg) |
| [2026-03-13](results/bm-20260313-3.15.0a7%2B-3c38feb) | python/3c38feb2a21aacdb009e | 3c38feb | 1.073x ↑<br>[📄](results/bm-20260313-3.15.0a7%2B-3c38feb/bm-20260313-vultr-x86_64-python-3c38feb2a21aacdb009e-3.15.0a7%2B-3c38feb-vs-3.12.6.md)[📈](results/bm-20260313-3.15.0a7%2B-3c38feb/bm-20260313-vultr-x86_64-python-3c38feb2a21aacdb009e-3.15.0a7%2B-3c38feb-vs-3.12.6.svg) | 1.037x ↑<br>[📄](results/bm-20260313-3.15.0a7%2B-3c38feb/bm-20260313-vultr-x86_64-python-3c38feb2a21aacdb009e-3.15.0a7%2B-3c38feb-vs-3.13.0rc2.md)[📈](results/bm-20260313-3.15.0a7%2B-3c38feb/bm-20260313-vultr-x86_64-python-3c38feb2a21aacdb009e-3.15.0a7%2B-3c38feb-vs-3.13.0rc2.svg) |  |
| [2026-03-13](results/bm-20260313-3.15.0a7%2B-400bdcb-JIT) | Fidget-Spinner/resume_tracing | 400bdcb (JIT) | 1.137x ↑<br>[📄](results/bm-20260313-3.15.0a7%2B-400bdcb-JIT/bm-20260313-vultr-x86_64-Fidget%252dSpinner-resume_tracing-3.15.0a7%2B-400bdcb-vs-3.12.6.md)[📈](results/bm-20260313-3.15.0a7%2B-400bdcb-JIT/bm-20260313-vultr-x86_64-Fidget%252dSpinner-resume_tracing-3.15.0a7%2B-400bdcb-vs-3.12.6.svg) | 1.098x ↑<br>[📄](results/bm-20260313-3.15.0a7%2B-400bdcb-JIT/bm-20260313-vultr-x86_64-Fidget%252dSpinner-resume_tracing-3.15.0a7%2B-400bdcb-vs-3.13.0rc2.md)[📈](results/bm-20260313-3.15.0a7%2B-400bdcb-JIT/bm-20260313-vultr-x86_64-Fidget%252dSpinner-resume_tracing-3.15.0a7%2B-400bdcb-vs-3.13.0rc2.svg) | 1.000x ↑<br>[📄](results/bm-20260313-3.15.0a7%2B-400bdcb-JIT/bm-20260313-vultr-x86_64-Fidget%252dSpinner-resume_tracing-3.15.0a7%2B-400bdcb-vs-base.md)[📈](results/bm-20260313-3.15.0a7%2B-400bdcb-JIT/bm-20260313-vultr-x86_64-Fidget%252dSpinner-resume_tracing-3.15.0a7%2B-400bdcb-vs-base.svg)[🧠](results/bm-20260313-3.15.0a7%2B-400bdcb-JIT/bm-20260313-vultr-x86_64-Fidget%252dSpinner-resume_tracing-3.15.0a7%2B-400bdcb-vs-base-mem.svg) |
| [2026-03-12](results/bm-20260312-3.15.0a7%2B-08a018e-NOGIL) | python/08a018ebe0d673e9c352 | 08a018e (NOGIL) | 1.017x ↓<br>[📄](results/bm-20260312-3.15.0a7%2B-08a018e-NOGIL/bm-20260312-vultr-x86_64-python-08a018ebe0d673e9c352-3.15.0a7%2B-08a018e-vs-3.12.6.md)[📈](results/bm-20260312-3.15.0a7%2B-08a018e-NOGIL/bm-20260312-vultr-x86_64-python-08a018ebe0d673e9c352-3.15.0a7%2B-08a018e-vs-3.12.6.svg) | 1.050x ↓<br>[📄](results/bm-20260312-3.15.0a7%2B-08a018e-NOGIL/bm-20260312-vultr-x86_64-python-08a018ebe0d673e9c352-3.15.0a7%2B-08a018e-vs-3.13.0rc2.md)[📈](results/bm-20260312-3.15.0a7%2B-08a018e-NOGIL/bm-20260312-vultr-x86_64-python-08a018ebe0d673e9c352-3.15.0a7%2B-08a018e-vs-3.13.0rc2.svg) | 1.087x ↓<br>[📄](results/bm-20260312-3.15.0a7%2B-08a018e-NOGIL/bm-20260312-vultr-x86_64-python-08a018ebe0d673e9c352-3.15.0a7%2B-08a018e-vs-base.md)[📈](results/bm-20260312-3.15.0a7%2B-08a018e-NOGIL/bm-20260312-vultr-x86_64-python-08a018ebe0d673e9c352-3.15.0a7%2B-08a018e-vs-base.svg)[🧠](results/bm-20260312-3.15.0a7%2B-08a018e-NOGIL/bm-20260312-vultr-x86_64-python-08a018ebe0d673e9c352-3.15.0a7%2B-08a018e-vs-base-mem.svg) |
| [2026-03-12](results/bm-20260312-3.15.0a7%2B-08a018e) | python/08a018ebe0d673e9c352 | 08a018e | 1.071x ↑<br>[📄](results/bm-20260312-3.15.0a7%2B-08a018e/bm-20260312-vultr-x86_64-python-08a018ebe0d673e9c352-3.15.0a7%2B-08a018e-vs-3.12.6.md)[📈](results/bm-20260312-3.15.0a7%2B-08a018e/bm-20260312-vultr-x86_64-python-08a018ebe0d673e9c352-3.15.0a7%2B-08a018e-vs-3.12.6.svg) | 1.035x ↑<br>[📄](results/bm-20260312-3.15.0a7%2B-08a018e/bm-20260312-vultr-x86_64-python-08a018ebe0d673e9c352-3.15.0a7%2B-08a018e-vs-3.13.0rc2.md)[📈](results/bm-20260312-3.15.0a7%2B-08a018e/bm-20260312-vultr-x86_64-python-08a018ebe0d673e9c352-3.15.0a7%2B-08a018e-vs-3.13.0rc2.svg) |  |
| [2026-03-12](results/bm-20260312-3.15.0a7%2B-0adc728-JIT) | python/0adc7289c3ab097b5608 | 0adc728 (JIT) | 1.136x ↑<br>[📄](results/bm-20260312-3.15.0a7%2B-0adc728-JIT/bm-20260312-vultr-x86_64-python-0adc7289c3ab097b5608-3.15.0a7%2B-0adc728-vs-3.12.6.md)[📈](results/bm-20260312-3.15.0a7%2B-0adc728-JIT/bm-20260312-vultr-x86_64-python-0adc7289c3ab097b5608-3.15.0a7%2B-0adc728-vs-3.12.6.svg) | 1.098x ↑<br>[📄](results/bm-20260312-3.15.0a7%2B-0adc728-JIT/bm-20260312-vultr-x86_64-python-0adc7289c3ab097b5608-3.15.0a7%2B-0adc728-vs-3.13.0rc2.md)[📈](results/bm-20260312-3.15.0a7%2B-0adc728-JIT/bm-20260312-vultr-x86_64-python-0adc7289c3ab097b5608-3.15.0a7%2B-0adc728-vs-3.13.0rc2.svg) |  |
| [2026-03-11](results/bm-20260311-3.15.0a7%2B-d19de37-NOGIL) | python/d19de375a204c74ab5f3 | d19de37 (NOGIL) | 1.026x ↓<br>[📄](results/bm-20260311-3.15.0a7%2B-d19de37-NOGIL/bm-20260311-vultr-x86_64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-3.12.6.md)[📈](results/bm-20260311-3.15.0a7%2B-d19de37-NOGIL/bm-20260311-vultr-x86_64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-3.12.6.svg) | 1.058x ↓<br>[📄](results/bm-20260311-3.15.0a7%2B-d19de37-NOGIL/bm-20260311-vultr-x86_64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-3.13.0rc2.md)[📈](results/bm-20260311-3.15.0a7%2B-d19de37-NOGIL/bm-20260311-vultr-x86_64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-3.13.0rc2.svg) | 1.095x ↓<br>[📄](results/bm-20260311-3.15.0a7%2B-d19de37-NOGIL/bm-20260311-vultr-x86_64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-base.md)[📈](results/bm-20260311-3.15.0a7%2B-d19de37-NOGIL/bm-20260311-vultr-x86_64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-base.svg)[🧠](results/bm-20260311-3.15.0a7%2B-d19de37-NOGIL/bm-20260311-vultr-x86_64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-base-mem.svg) |
| [2026-03-11](results/bm-20260311-3.15.0a7%2B-d19de37) | python/d19de375a204c74ab5f3 | d19de37 | 1.071x ↑<br>[📄](results/bm-20260311-3.15.0a7%2B-d19de37/bm-20260311-vultr-x86_64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-3.12.6.md)[📈](results/bm-20260311-3.15.0a7%2B-d19de37/bm-20260311-vultr-x86_64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-3.12.6.svg) | 1.036x ↑<br>[📄](results/bm-20260311-3.15.0a7%2B-d19de37/bm-20260311-vultr-x86_64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-3.13.0rc2.md)[📈](results/bm-20260311-3.15.0a7%2B-d19de37/bm-20260311-vultr-x86_64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-3.13.0rc2.svg) |  |
| [2026-03-10](results/bm-20260310-3.15.0a7%2B-5197ecb-NOGIL) | python/5197ecb5e4df30ba0f67 | 5197ecb (NOGIL) | 1.027x ↓<br>[📄](results/bm-20260310-3.15.0a7%2B-5197ecb-NOGIL/bm-20260310-vultr-x86_64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-3.12.6.md)[📈](results/bm-20260310-3.15.0a7%2B-5197ecb-NOGIL/bm-20260310-vultr-x86_64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-3.12.6.svg) | 1.059x ↓<br>[📄](results/bm-20260310-3.15.0a7%2B-5197ecb-NOGIL/bm-20260310-vultr-x86_64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-3.13.0rc2.md)[📈](results/bm-20260310-3.15.0a7%2B-5197ecb-NOGIL/bm-20260310-vultr-x86_64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-3.13.0rc2.svg) | 1.092x ↓<br>[📄](results/bm-20260310-3.15.0a7%2B-5197ecb-NOGIL/bm-20260310-vultr-x86_64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-base.md)[📈](results/bm-20260310-3.15.0a7%2B-5197ecb-NOGIL/bm-20260310-vultr-x86_64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-base.svg)[🧠](results/bm-20260310-3.15.0a7%2B-5197ecb-NOGIL/bm-20260310-vultr-x86_64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-base-mem.svg) |
| [2026-03-10](results/bm-20260310-3.15.0a7%2B-5197ecb) | python/5197ecb5e4df30ba0f67 | 5197ecb | 1.068x ↑<br>[📄](results/bm-20260310-3.15.0a7%2B-5197ecb/bm-20260310-vultr-x86_64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-3.12.6.md)[📈](results/bm-20260310-3.15.0a7%2B-5197ecb/bm-20260310-vultr-x86_64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-3.12.6.svg) | 1.032x ↑<br>[📄](results/bm-20260310-3.15.0a7%2B-5197ecb/bm-20260310-vultr-x86_64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-3.13.0rc2.md)[📈](results/bm-20260310-3.15.0a7%2B-5197ecb/bm-20260310-vultr-x86_64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-03-13](results/bm-20260313-3.15.0a7%2B-3c38feb-NOGIL) | python/3c38feb2a21aacdb009e | 3c38feb (NOGIL) | 1.101x ↑<br>[📄](results/bm-20260313-3.15.0a7%2B-3c38feb-NOGIL/bm-20260313-macm4pro-arm64-python-3c38feb2a21aacdb009e-3.15.0a7%2B-3c38feb-vs-3.12.6.md)[📈](results/bm-20260313-3.15.0a7%2B-3c38feb-NOGIL/bm-20260313-macm4pro-arm64-python-3c38feb2a21aacdb009e-3.15.0a7%2B-3c38feb-vs-3.12.6.svg) | 1.022x ↑<br>[📄](results/bm-20260313-3.15.0a7%2B-3c38feb-NOGIL/bm-20260313-macm4pro-arm64-python-3c38feb2a21aacdb009e-3.15.0a7%2B-3c38feb-vs-3.13.0rc2.md)[📈](results/bm-20260313-3.15.0a7%2B-3c38feb-NOGIL/bm-20260313-macm4pro-arm64-python-3c38feb2a21aacdb009e-3.15.0a7%2B-3c38feb-vs-3.13.0rc2.svg) | 1.057x ↓<br>[📄](results/bm-20260313-3.15.0a7%2B-3c38feb-NOGIL/bm-20260313-macm4pro-arm64-python-3c38feb2a21aacdb009e-3.15.0a7%2B-3c38feb-vs-base.md)[📈](results/bm-20260313-3.15.0a7%2B-3c38feb-NOGIL/bm-20260313-macm4pro-arm64-python-3c38feb2a21aacdb009e-3.15.0a7%2B-3c38feb-vs-base.svg)[🧠](results/bm-20260313-3.15.0a7%2B-3c38feb-NOGIL/bm-20260313-macm4pro-arm64-python-3c38feb2a21aacdb009e-3.15.0a7%2B-3c38feb-vs-base-mem.svg) |
| [2026-03-13](results/bm-20260313-3.15.0a7%2B-3c38feb) | python/3c38feb2a21aacdb009e | 3c38feb | 1.168x ↑<br>[📄](results/bm-20260313-3.15.0a7%2B-3c38feb/bm-20260313-macm4pro-arm64-python-3c38feb2a21aacdb009e-3.15.0a7%2B-3c38feb-vs-3.12.6.md)[📈](results/bm-20260313-3.15.0a7%2B-3c38feb/bm-20260313-macm4pro-arm64-python-3c38feb2a21aacdb009e-3.15.0a7%2B-3c38feb-vs-3.12.6.svg) | 1.083x ↑<br>[📄](results/bm-20260313-3.15.0a7%2B-3c38feb/bm-20260313-macm4pro-arm64-python-3c38feb2a21aacdb009e-3.15.0a7%2B-3c38feb-vs-3.13.0rc2.md)[📈](results/bm-20260313-3.15.0a7%2B-3c38feb/bm-20260313-macm4pro-arm64-python-3c38feb2a21aacdb009e-3.15.0a7%2B-3c38feb-vs-3.13.0rc2.svg) |  |
| [2026-03-13](results/bm-20260313-3.15.0a7%2B-af09d44-JIT) | Fidget-Spinner/resume_tracing | af09d44 (JIT) | 1.287x ↑<br>[📄](results/bm-20260313-3.15.0a7%2B-af09d44-JIT/bm-20260313-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a7%2B-af09d44-vs-3.12.6.md)[📈](results/bm-20260313-3.15.0a7%2B-af09d44-JIT/bm-20260313-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a7%2B-af09d44-vs-3.12.6.svg) | 1.193x ↑<br>[📄](results/bm-20260313-3.15.0a7%2B-af09d44-JIT/bm-20260313-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a7%2B-af09d44-vs-3.13.0rc2.md)[📈](results/bm-20260313-3.15.0a7%2B-af09d44-JIT/bm-20260313-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a7%2B-af09d44-vs-3.13.0rc2.svg) | 1.037x ↑<br>[📄](results/bm-20260313-3.15.0a7%2B-af09d44-JIT/bm-20260313-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a7%2B-af09d44-vs-base.md)[📈](results/bm-20260313-3.15.0a7%2B-af09d44-JIT/bm-20260313-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a7%2B-af09d44-vs-base.svg)[🧠](results/bm-20260313-3.15.0a7%2B-af09d44-JIT/bm-20260313-macm4pro-arm64-Fidget%252dSpinner-resume_tracing-3.15.0a7%2B-af09d44-vs-base-mem.svg) |
| [2026-03-12](results/bm-20260312-3.15.0a7%2B-0adc728-JIT) | python/0adc7289c3ab097b5608 | 0adc728 (JIT) | 1.244x ↑<br>[📄](results/bm-20260312-3.15.0a7%2B-0adc728-JIT/bm-20260312-macm4pro-arm64-python-0adc7289c3ab097b5608-3.15.0a7%2B-0adc728-vs-3.12.6.md)[📈](results/bm-20260312-3.15.0a7%2B-0adc728-JIT/bm-20260312-macm4pro-arm64-python-0adc7289c3ab097b5608-3.15.0a7%2B-0adc728-vs-3.12.6.svg) | 1.153x ↑<br>[📄](results/bm-20260312-3.15.0a7%2B-0adc728-JIT/bm-20260312-macm4pro-arm64-python-0adc7289c3ab097b5608-3.15.0a7%2B-0adc728-vs-3.13.0rc2.md)[📈](results/bm-20260312-3.15.0a7%2B-0adc728-JIT/bm-20260312-macm4pro-arm64-python-0adc7289c3ab097b5608-3.15.0a7%2B-0adc728-vs-3.13.0rc2.svg) |  |
| [2026-03-11](results/bm-20260311-3.15.0a7%2B-d19de37-NOGIL) | python/d19de375a204c74ab5f3 | d19de37 (NOGIL) | 1.105x ↑<br>[📄](results/bm-20260311-3.15.0a7%2B-d19de37-NOGIL/bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-3.12.6.md)[📈](results/bm-20260311-3.15.0a7%2B-d19de37-NOGIL/bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-3.12.6.svg) | 1.024x ↑<br>[📄](results/bm-20260311-3.15.0a7%2B-d19de37-NOGIL/bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-3.13.0rc2.md)[📈](results/bm-20260311-3.15.0a7%2B-d19de37-NOGIL/bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-3.13.0rc2.svg) | 1.057x ↓<br>[📄](results/bm-20260311-3.15.0a7%2B-d19de37-NOGIL/bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-base.md)[📈](results/bm-20260311-3.15.0a7%2B-d19de37-NOGIL/bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-base.svg)[🧠](results/bm-20260311-3.15.0a7%2B-d19de37-NOGIL/bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-base-mem.svg) |
| [2026-03-11](results/bm-20260311-3.15.0a7%2B-d19de37) | python/d19de375a204c74ab5f3 | d19de37 | 1.169x ↑<br>[📄](results/bm-20260311-3.15.0a7%2B-d19de37/bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-3.12.6.md)[📈](results/bm-20260311-3.15.0a7%2B-d19de37/bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-3.12.6.svg) | 1.084x ↑<br>[📄](results/bm-20260311-3.15.0a7%2B-d19de37/bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-3.13.0rc2.md)[📈](results/bm-20260311-3.15.0a7%2B-d19de37/bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-3.13.0rc2.svg) |  |
| [2026-03-10](results/bm-20260310-3.15.0a7%2B-5197ecb-NOGIL) | python/5197ecb5e4df30ba0f67 | 5197ecb (NOGIL) | 1.104x ↑<br>[📄](results/bm-20260310-3.15.0a7%2B-5197ecb-NOGIL/bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-3.12.6.md)[📈](results/bm-20260310-3.15.0a7%2B-5197ecb-NOGIL/bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-3.12.6.svg) | 1.024x ↑<br>[📄](results/bm-20260310-3.15.0a7%2B-5197ecb-NOGIL/bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-3.13.0rc2.md)[📈](results/bm-20260310-3.15.0a7%2B-5197ecb-NOGIL/bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-3.13.0rc2.svg) | 1.026x ↓<br>[📄](results/bm-20260310-3.15.0a7%2B-5197ecb-NOGIL/bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-base.md)[📈](results/bm-20260310-3.15.0a7%2B-5197ecb-NOGIL/bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-base.svg)[🧠](results/bm-20260310-3.15.0a7%2B-5197ecb-NOGIL/bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-base-mem.svg) |
| [2026-03-10](results/bm-20260310-3.15.0a7%2B-5197ecb) | python/5197ecb5e4df30ba0f67 | 5197ecb | 1.134x ↑<br>[📄](results/bm-20260310-3.15.0a7%2B-5197ecb/bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-3.12.6.md)[📈](results/bm-20260310-3.15.0a7%2B-5197ecb/bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-3.12.6.svg) | 1.052x ↑<br>[📄](results/bm-20260310-3.15.0a7%2B-5197ecb/bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-3.13.0rc2.md)[📈](results/bm-20260310-3.15.0a7%2B-5197ecb/bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-3.13.0rc2.svg) |  |


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
