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
| [2026-03-11](results/bm-20260311-3.15.0a7%2B-d19de37-NOGIL) | python/d19de375a204c74ab5f3 | d19de37 (NOGIL) | 1.026x ↓<br>[📄](results/bm-20260311-3.15.0a7%2B-d19de37-NOGIL/bm-20260311-vultr-x86_64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-3.12.6.md)[📈](results/bm-20260311-3.15.0a7%2B-d19de37-NOGIL/bm-20260311-vultr-x86_64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-3.12.6.svg) | 1.058x ↓<br>[📄](results/bm-20260311-3.15.0a7%2B-d19de37-NOGIL/bm-20260311-vultr-x86_64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-3.13.0rc2.md)[📈](results/bm-20260311-3.15.0a7%2B-d19de37-NOGIL/bm-20260311-vultr-x86_64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-3.13.0rc2.svg) | 1.095x ↓<br>[📄](results/bm-20260311-3.15.0a7%2B-d19de37-NOGIL/bm-20260311-vultr-x86_64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-base.md)[📈](results/bm-20260311-3.15.0a7%2B-d19de37-NOGIL/bm-20260311-vultr-x86_64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-base.svg)[🧠](results/bm-20260311-3.15.0a7%2B-d19de37-NOGIL/bm-20260311-vultr-x86_64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-base-mem.svg) |
| [2026-03-11](results/bm-20260311-3.15.0a7%2B-d19de37) | python/d19de375a204c74ab5f3 | d19de37 | 1.071x ↑<br>[📄](results/bm-20260311-3.15.0a7%2B-d19de37/bm-20260311-vultr-x86_64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-3.12.6.md)[📈](results/bm-20260311-3.15.0a7%2B-d19de37/bm-20260311-vultr-x86_64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-3.12.6.svg) | 1.036x ↑<br>[📄](results/bm-20260311-3.15.0a7%2B-d19de37/bm-20260311-vultr-x86_64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-3.13.0rc2.md)[📈](results/bm-20260311-3.15.0a7%2B-d19de37/bm-20260311-vultr-x86_64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-3.13.0rc2.svg) |  |
| [2026-03-10](results/bm-20260310-3.15.0a7%2B-5197ecb-NOGIL) | python/5197ecb5e4df30ba0f67 | 5197ecb (NOGIL) | 1.027x ↓<br>[📄](results/bm-20260310-3.15.0a7%2B-5197ecb-NOGIL/bm-20260310-vultr-x86_64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-3.12.6.md)[📈](results/bm-20260310-3.15.0a7%2B-5197ecb-NOGIL/bm-20260310-vultr-x86_64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-3.12.6.svg) | 1.059x ↓<br>[📄](results/bm-20260310-3.15.0a7%2B-5197ecb-NOGIL/bm-20260310-vultr-x86_64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-3.13.0rc2.md)[📈](results/bm-20260310-3.15.0a7%2B-5197ecb-NOGIL/bm-20260310-vultr-x86_64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-3.13.0rc2.svg) | 1.092x ↓<br>[📄](results/bm-20260310-3.15.0a7%2B-5197ecb-NOGIL/bm-20260310-vultr-x86_64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-base.md)[📈](results/bm-20260310-3.15.0a7%2B-5197ecb-NOGIL/bm-20260310-vultr-x86_64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-base.svg)[🧠](results/bm-20260310-3.15.0a7%2B-5197ecb-NOGIL/bm-20260310-vultr-x86_64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-base-mem.svg) |
| [2026-03-10](results/bm-20260310-3.15.0a7%2B-5197ecb) | python/5197ecb5e4df30ba0f67 | 5197ecb | 1.068x ↑<br>[📄](results/bm-20260310-3.15.0a7%2B-5197ecb/bm-20260310-vultr-x86_64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-3.12.6.md)[📈](results/bm-20260310-3.15.0a7%2B-5197ecb/bm-20260310-vultr-x86_64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-3.12.6.svg) | 1.032x ↑<br>[📄](results/bm-20260310-3.15.0a7%2B-5197ecb/bm-20260310-vultr-x86_64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-3.13.0rc2.md)[📈](results/bm-20260310-3.15.0a7%2B-5197ecb/bm-20260310-vultr-x86_64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-3.13.0rc2.svg) |  |
| [2026-03-09](results/bm-20260309-3.15.0a6%2B-099943b-NOGIL) | python/099943b122cda2548ad7 | 099943b (NOGIL) | 1.029x ↓<br>[📄](results/bm-20260309-3.15.0a6%2B-099943b-NOGIL/bm-20260309-vultr-x86_64-python-099943b122cda2548ad7-3.15.0a6%2B-099943b-vs-3.12.6.md)[📈](results/bm-20260309-3.15.0a6%2B-099943b-NOGIL/bm-20260309-vultr-x86_64-python-099943b122cda2548ad7-3.15.0a6%2B-099943b-vs-3.12.6.svg) | 1.061x ↓<br>[📄](results/bm-20260309-3.15.0a6%2B-099943b-NOGIL/bm-20260309-vultr-x86_64-python-099943b122cda2548ad7-3.15.0a6%2B-099943b-vs-3.13.0rc2.md)[📈](results/bm-20260309-3.15.0a6%2B-099943b-NOGIL/bm-20260309-vultr-x86_64-python-099943b122cda2548ad7-3.15.0a6%2B-099943b-vs-3.13.0rc2.svg) | 1.101x ↓<br>[📄](results/bm-20260309-3.15.0a6%2B-099943b-NOGIL/bm-20260309-vultr-x86_64-python-099943b122cda2548ad7-3.15.0a6%2B-099943b-vs-base.md)[📈](results/bm-20260309-3.15.0a6%2B-099943b-NOGIL/bm-20260309-vultr-x86_64-python-099943b122cda2548ad7-3.15.0a6%2B-099943b-vs-base.svg)[🧠](results/bm-20260309-3.15.0a6%2B-099943b-NOGIL/bm-20260309-vultr-x86_64-python-099943b122cda2548ad7-3.15.0a6%2B-099943b-vs-base-mem.svg) |
| [2026-03-09](results/bm-20260309-3.15.0a6%2B-099943b) | python/099943b122cda2548ad7 | 099943b | 1.075x ↑<br>[📄](results/bm-20260309-3.15.0a6%2B-099943b/bm-20260309-vultr-x86_64-python-099943b122cda2548ad7-3.15.0a6%2B-099943b-vs-3.12.6.md)[📈](results/bm-20260309-3.15.0a6%2B-099943b/bm-20260309-vultr-x86_64-python-099943b122cda2548ad7-3.15.0a6%2B-099943b-vs-3.12.6.svg) | 1.040x ↑<br>[📄](results/bm-20260309-3.15.0a6%2B-099943b/bm-20260309-vultr-x86_64-python-099943b122cda2548ad7-3.15.0a6%2B-099943b-vs-3.13.0rc2.md)[📈](results/bm-20260309-3.15.0a6%2B-099943b/bm-20260309-vultr-x86_64-python-099943b122cda2548ad7-3.15.0a6%2B-099943b-vs-3.13.0rc2.svg) |  |
| [2026-03-08](results/bm-20260308-3.15.0a6%2B-5a15a52-NOGIL) | python/5a15a52dd1dee37af4f2 | 5a15a52 (NOGIL) | 1.027x ↓<br>[📄](results/bm-20260308-3.15.0a6%2B-5a15a52-NOGIL/bm-20260308-vultr-x86_64-python-5a15a52dd1dee37af4f2-3.15.0a6%2B-5a15a52-vs-3.12.6.md)[📈](results/bm-20260308-3.15.0a6%2B-5a15a52-NOGIL/bm-20260308-vultr-x86_64-python-5a15a52dd1dee37af4f2-3.15.0a6%2B-5a15a52-vs-3.12.6.svg) | 1.059x ↓<br>[📄](results/bm-20260308-3.15.0a6%2B-5a15a52-NOGIL/bm-20260308-vultr-x86_64-python-5a15a52dd1dee37af4f2-3.15.0a6%2B-5a15a52-vs-3.13.0rc2.md)[📈](results/bm-20260308-3.15.0a6%2B-5a15a52-NOGIL/bm-20260308-vultr-x86_64-python-5a15a52dd1dee37af4f2-3.15.0a6%2B-5a15a52-vs-3.13.0rc2.svg) | 1.004x ↓<br>[📄](results/bm-20260308-3.15.0a6%2B-5a15a52-NOGIL/bm-20260308-vultr-x86_64-python-5a15a52dd1dee37af4f2-3.15.0a6%2B-5a15a52-vs-base.md)[📈](results/bm-20260308-3.15.0a6%2B-5a15a52-NOGIL/bm-20260308-vultr-x86_64-python-5a15a52dd1dee37af4f2-3.15.0a6%2B-5a15a52-vs-base.svg)[🧠](results/bm-20260308-3.15.0a6%2B-5a15a52-NOGIL/bm-20260308-vultr-x86_64-python-5a15a52dd1dee37af4f2-3.15.0a6%2B-5a15a52-vs-base-mem.svg) |
| [2026-03-08](results/bm-20260308-3.15.0a6%2B-5a15a52) | python/5a15a52dd1dee37af4f2 | 5a15a52 | 1.075x ↑<br>[📄](results/bm-20260308-3.15.0a6%2B-5a15a52/bm-20260308-vultr-x86_64-python-5a15a52dd1dee37af4f2-3.15.0a6%2B-5a15a52-vs-3.12.6.md)[📈](results/bm-20260308-3.15.0a6%2B-5a15a52/bm-20260308-vultr-x86_64-python-5a15a52dd1dee37af4f2-3.15.0a6%2B-5a15a52-vs-3.12.6.svg) | 1.039x ↑<br>[📄](results/bm-20260308-3.15.0a6%2B-5a15a52/bm-20260308-vultr-x86_64-python-5a15a52dd1dee37af4f2-3.15.0a6%2B-5a15a52-vs-3.13.0rc2.md)[📈](results/bm-20260308-3.15.0a6%2B-5a15a52/bm-20260308-vultr-x86_64-python-5a15a52dd1dee37af4f2-3.15.0a6%2B-5a15a52-vs-3.13.0rc2.svg) | 1.002x ↑<br>[📄](results/bm-20260308-3.15.0a6%2B-5a15a52/bm-20260308-vultr-x86_64-python-5a15a52dd1dee37af4f2-3.15.0a6%2B-5a15a52-vs-base.md)[📈](results/bm-20260308-3.15.0a6%2B-5a15a52/bm-20260308-vultr-x86_64-python-5a15a52dd1dee37af4f2-3.15.0a6%2B-5a15a52-vs-base.svg)[🧠](results/bm-20260308-3.15.0a6%2B-5a15a52/bm-20260308-vultr-x86_64-python-5a15a52dd1dee37af4f2-3.15.0a6%2B-5a15a52-vs-base-mem.svg) |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-03-11](results/bm-20260311-3.15.0a7%2B-d19de37-NOGIL) | python/d19de375a204c74ab5f3 | d19de37 (NOGIL) | 1.105x ↑<br>[📄](results/bm-20260311-3.15.0a7%2B-d19de37-NOGIL/bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-3.12.6.md)[📈](results/bm-20260311-3.15.0a7%2B-d19de37-NOGIL/bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-3.12.6.svg) | 1.024x ↑<br>[📄](results/bm-20260311-3.15.0a7%2B-d19de37-NOGIL/bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-3.13.0rc2.md)[📈](results/bm-20260311-3.15.0a7%2B-d19de37-NOGIL/bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-3.13.0rc2.svg) | 1.057x ↓<br>[📄](results/bm-20260311-3.15.0a7%2B-d19de37-NOGIL/bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-base.md)[📈](results/bm-20260311-3.15.0a7%2B-d19de37-NOGIL/bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-base.svg)[🧠](results/bm-20260311-3.15.0a7%2B-d19de37-NOGIL/bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-base-mem.svg) |
| [2026-03-11](results/bm-20260311-3.15.0a7%2B-d19de37) | python/d19de375a204c74ab5f3 | d19de37 | 1.169x ↑<br>[📄](results/bm-20260311-3.15.0a7%2B-d19de37/bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-3.12.6.md)[📈](results/bm-20260311-3.15.0a7%2B-d19de37/bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-3.12.6.svg) | 1.084x ↑<br>[📄](results/bm-20260311-3.15.0a7%2B-d19de37/bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-3.13.0rc2.md)[📈](results/bm-20260311-3.15.0a7%2B-d19de37/bm-20260311-macm4pro-arm64-python-d19de375a204c74ab5f3-3.15.0a7%2B-d19de37-vs-3.13.0rc2.svg) |  |
| [2026-03-10](results/bm-20260310-3.15.0a7%2B-5197ecb-NOGIL) | python/5197ecb5e4df30ba0f67 | 5197ecb (NOGIL) | 1.104x ↑<br>[📄](results/bm-20260310-3.15.0a7%2B-5197ecb-NOGIL/bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-3.12.6.md)[📈](results/bm-20260310-3.15.0a7%2B-5197ecb-NOGIL/bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-3.12.6.svg) | 1.024x ↑<br>[📄](results/bm-20260310-3.15.0a7%2B-5197ecb-NOGIL/bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-3.13.0rc2.md)[📈](results/bm-20260310-3.15.0a7%2B-5197ecb-NOGIL/bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-3.13.0rc2.svg) | 1.026x ↓<br>[📄](results/bm-20260310-3.15.0a7%2B-5197ecb-NOGIL/bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-base.md)[📈](results/bm-20260310-3.15.0a7%2B-5197ecb-NOGIL/bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-base.svg)[🧠](results/bm-20260310-3.15.0a7%2B-5197ecb-NOGIL/bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-base-mem.svg) |
| [2026-03-10](results/bm-20260310-3.15.0a7%2B-5197ecb) | python/5197ecb5e4df30ba0f67 | 5197ecb | 1.134x ↑<br>[📄](results/bm-20260310-3.15.0a7%2B-5197ecb/bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-3.12.6.md)[📈](results/bm-20260310-3.15.0a7%2B-5197ecb/bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-3.12.6.svg) | 1.052x ↑<br>[📄](results/bm-20260310-3.15.0a7%2B-5197ecb/bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-3.13.0rc2.md)[📈](results/bm-20260310-3.15.0a7%2B-5197ecb/bm-20260310-macm4pro-arm64-python-5197ecb5e4df30ba0f67-3.15.0a7%2B-5197ecb-vs-3.13.0rc2.svg) |  |
| [2026-03-09](results/bm-20260309-3.15.0a6%2B-099943b-NOGIL) | python/099943b122cda2548ad7 | 099943b (NOGIL) | 1.091x ↑<br>[📄](results/bm-20260309-3.15.0a6%2B-099943b-NOGIL/bm-20260309-macm4pro-arm64-python-099943b122cda2548ad7-3.15.0a6%2B-099943b-vs-3.12.6.md)[📈](results/bm-20260309-3.15.0a6%2B-099943b-NOGIL/bm-20260309-macm4pro-arm64-python-099943b122cda2548ad7-3.15.0a6%2B-099943b-vs-3.12.6.svg) | 1.012x ↑<br>[📄](results/bm-20260309-3.15.0a6%2B-099943b-NOGIL/bm-20260309-macm4pro-arm64-python-099943b122cda2548ad7-3.15.0a6%2B-099943b-vs-3.13.0rc2.md)[📈](results/bm-20260309-3.15.0a6%2B-099943b-NOGIL/bm-20260309-macm4pro-arm64-python-099943b122cda2548ad7-3.15.0a6%2B-099943b-vs-3.13.0rc2.svg) | 1.039x ↓<br>[📄](results/bm-20260309-3.15.0a6%2B-099943b-NOGIL/bm-20260309-macm4pro-arm64-python-099943b122cda2548ad7-3.15.0a6%2B-099943b-vs-base.md)[📈](results/bm-20260309-3.15.0a6%2B-099943b-NOGIL/bm-20260309-macm4pro-arm64-python-099943b122cda2548ad7-3.15.0a6%2B-099943b-vs-base.svg)[🧠](results/bm-20260309-3.15.0a6%2B-099943b-NOGIL/bm-20260309-macm4pro-arm64-python-099943b122cda2548ad7-3.15.0a6%2B-099943b-vs-base-mem.svg) |
| [2026-03-09](results/bm-20260309-3.15.0a6%2B-099943b) | python/099943b122cda2548ad7 | 099943b | 1.135x ↑<br>[📄](results/bm-20260309-3.15.0a6%2B-099943b/bm-20260309-macm4pro-arm64-python-099943b122cda2548ad7-3.15.0a6%2B-099943b-vs-3.12.6.md)[📈](results/bm-20260309-3.15.0a6%2B-099943b/bm-20260309-macm4pro-arm64-python-099943b122cda2548ad7-3.15.0a6%2B-099943b-vs-3.12.6.svg) | 1.053x ↑<br>[📄](results/bm-20260309-3.15.0a6%2B-099943b/bm-20260309-macm4pro-arm64-python-099943b122cda2548ad7-3.15.0a6%2B-099943b-vs-3.13.0rc2.md)[📈](results/bm-20260309-3.15.0a6%2B-099943b/bm-20260309-macm4pro-arm64-python-099943b122cda2548ad7-3.15.0a6%2B-099943b-vs-3.13.0rc2.svg) |  |
| [2026-03-08](results/bm-20260308-3.15.0a6%2B-5a15a52-NOGIL) | python/5a15a52dd1dee37af4f2 | 5a15a52 (NOGIL) | 1.090x ↑<br>[📄](results/bm-20260308-3.15.0a6%2B-5a15a52-NOGIL/bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6%2B-5a15a52-vs-3.12.6.md)[📈](results/bm-20260308-3.15.0a6%2B-5a15a52-NOGIL/bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6%2B-5a15a52-vs-3.12.6.svg) | 1.011x ↑<br>[📄](results/bm-20260308-3.15.0a6%2B-5a15a52-NOGIL/bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6%2B-5a15a52-vs-3.13.0rc2.md)[📈](results/bm-20260308-3.15.0a6%2B-5a15a52-NOGIL/bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6%2B-5a15a52-vs-3.13.0rc2.svg) | 1.008x ↓<br>[📄](results/bm-20260308-3.15.0a6%2B-5a15a52-NOGIL/bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6%2B-5a15a52-vs-base.md)[📈](results/bm-20260308-3.15.0a6%2B-5a15a52-NOGIL/bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6%2B-5a15a52-vs-base.svg)[🧠](results/bm-20260308-3.15.0a6%2B-5a15a52-NOGIL/bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6%2B-5a15a52-vs-base-mem.svg) |
| [2026-03-08](results/bm-20260308-3.15.0a6%2B-5a15a52) | python/5a15a52dd1dee37af4f2 | 5a15a52 | 1.129x ↑<br>[📄](results/bm-20260308-3.15.0a6%2B-5a15a52/bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6%2B-5a15a52-vs-3.12.6.md)[📈](results/bm-20260308-3.15.0a6%2B-5a15a52/bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6%2B-5a15a52-vs-3.12.6.svg) | 1.046x ↑<br>[📄](results/bm-20260308-3.15.0a6%2B-5a15a52/bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6%2B-5a15a52-vs-3.13.0rc2.md)[📈](results/bm-20260308-3.15.0a6%2B-5a15a52/bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6%2B-5a15a52-vs-3.13.0rc2.svg) | 1.014x ↓<br>[📄](results/bm-20260308-3.15.0a6%2B-5a15a52/bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6%2B-5a15a52-vs-base.md)[📈](results/bm-20260308-3.15.0a6%2B-5a15a52/bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6%2B-5a15a52-vs-base.svg)[🧠](results/bm-20260308-3.15.0a6%2B-5a15a52/bm-20260308-macm4pro-arm64-python-5a15a52dd1dee37af4f2-3.15.0a6%2B-5a15a52-vs-base-mem.svg) |


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
