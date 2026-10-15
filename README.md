# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (c6c0608)](results/bm-20261010-3.16.0a0-c6c0608/bm-20261010-vultr-x86_64-python-c6c060843b7635b5a1f8-3.16.0a0-c6c0608-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (c6c0608)](results/bm-20261010-3.16.0a0-c6c0608-PYTHON_UOPS/bm-20261010-vultr-x86_64-python-c6c060843b7635b5a1f8-3.16.0a0-c6c0608-pystats.md)
- [Most recent JIT pystats on main (bedaea0)](results/bm-20251019-3.15.0a1%2B-bedaea0-JIT/bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-10-14](results/bm-20261014-3.16.0a1%2Bdev-a6b4aa6-NOGIL) | python/a6b4aa687cd9f8f95e3b | a6b4aa6 (NOGIL) | 1.040x ↓<br>[📄](results/bm-20261014-3.16.0a1%2Bdev-a6b4aa6-NOGIL/bm-20261014-vultr-x86_64-python-a6b4aa687cd9f8f95e3b-3.16.0a1%2Bdev-a6b4aa6-vs-3.12.6.md)[📈](results/bm-20261014-3.16.0a1%2Bdev-a6b4aa6-NOGIL/bm-20261014-vultr-x86_64-python-a6b4aa687cd9f8f95e3b-3.16.0a1%2Bdev-a6b4aa6-vs-3.12.6.svg) | 1.072x ↓<br>[📄](results/bm-20261014-3.16.0a1%2Bdev-a6b4aa6-NOGIL/bm-20261014-vultr-x86_64-python-a6b4aa687cd9f8f95e3b-3.16.0a1%2Bdev-a6b4aa6-vs-3.13.0rc2.md)[📈](results/bm-20261014-3.16.0a1%2Bdev-a6b4aa6-NOGIL/bm-20261014-vultr-x86_64-python-a6b4aa687cd9f8f95e3b-3.16.0a1%2Bdev-a6b4aa6-vs-3.13.0rc2.svg) | 1.113x ↓<br>[📄](results/bm-20261014-3.16.0a1%2Bdev-a6b4aa6-NOGIL/bm-20261014-vultr-x86_64-python-a6b4aa687cd9f8f95e3b-3.16.0a1%2Bdev-a6b4aa6-vs-base.md)[📈](results/bm-20261014-3.16.0a1%2Bdev-a6b4aa6-NOGIL/bm-20261014-vultr-x86_64-python-a6b4aa687cd9f8f95e3b-3.16.0a1%2Bdev-a6b4aa6-vs-base.svg)[🧠](results/bm-20261014-3.16.0a1%2Bdev-a6b4aa6-NOGIL/bm-20261014-vultr-x86_64-python-a6b4aa687cd9f8f95e3b-3.16.0a1%2Bdev-a6b4aa6-vs-base-mem.svg) |
| [2026-10-14](results/bm-20261014-3.16.0a1%2Bdev-a6b4aa6) | python/a6b4aa687cd9f8f95e3b | a6b4aa6 | 1.079x ↑<br>[📄](results/bm-20261014-3.16.0a1%2Bdev-a6b4aa6/bm-20261014-vultr-x86_64-python-a6b4aa687cd9f8f95e3b-3.16.0a1%2Bdev-a6b4aa6-vs-3.12.6.md)[📈](results/bm-20261014-3.16.0a1%2Bdev-a6b4aa6/bm-20261014-vultr-x86_64-python-a6b4aa687cd9f8f95e3b-3.16.0a1%2Bdev-a6b4aa6-vs-3.12.6.svg) | 1.043x ↑<br>[📄](results/bm-20261014-3.16.0a1%2Bdev-a6b4aa6/bm-20261014-vultr-x86_64-python-a6b4aa687cd9f8f95e3b-3.16.0a1%2Bdev-a6b4aa6-vs-3.13.0rc2.md)[📈](results/bm-20261014-3.16.0a1%2Bdev-a6b4aa6/bm-20261014-vultr-x86_64-python-a6b4aa687cd9f8f95e3b-3.16.0a1%2Bdev-a6b4aa6-vs-3.13.0rc2.svg) |  |
| [2026-10-13](results/bm-20261013-3.16.0a1%2Bdev-084aff8-NOGIL) | python/084aff869c4aa2f2cbdf | 084aff8 (NOGIL) | 1.044x ↓<br>[📄](results/bm-20261013-3.16.0a1%2Bdev-084aff8-NOGIL/bm-20261013-vultr-x86_64-python-084aff869c4aa2f2cbdf-3.16.0a1%2Bdev-084aff8-vs-3.12.6.md)[📈](results/bm-20261013-3.16.0a1%2Bdev-084aff8-NOGIL/bm-20261013-vultr-x86_64-python-084aff869c4aa2f2cbdf-3.16.0a1%2Bdev-084aff8-vs-3.12.6.svg) | 1.077x ↓<br>[📄](results/bm-20261013-3.16.0a1%2Bdev-084aff8-NOGIL/bm-20261013-vultr-x86_64-python-084aff869c4aa2f2cbdf-3.16.0a1%2Bdev-084aff8-vs-3.13.0rc2.md)[📈](results/bm-20261013-3.16.0a1%2Bdev-084aff8-NOGIL/bm-20261013-vultr-x86_64-python-084aff869c4aa2f2cbdf-3.16.0a1%2Bdev-084aff8-vs-3.13.0rc2.svg) | 1.119x ↓<br>[📄](results/bm-20261013-3.16.0a1%2Bdev-084aff8-NOGIL/bm-20261013-vultr-x86_64-python-084aff869c4aa2f2cbdf-3.16.0a1%2Bdev-084aff8-vs-base.md)[📈](results/bm-20261013-3.16.0a1%2Bdev-084aff8-NOGIL/bm-20261013-vultr-x86_64-python-084aff869c4aa2f2cbdf-3.16.0a1%2Bdev-084aff8-vs-base.svg)[🧠](results/bm-20261013-3.16.0a1%2Bdev-084aff8-NOGIL/bm-20261013-vultr-x86_64-python-084aff869c4aa2f2cbdf-3.16.0a1%2Bdev-084aff8-vs-base-mem.svg) |
| [2026-10-13](results/bm-20261013-3.16.0a1%2Bdev-084aff8) | python/084aff869c4aa2f2cbdf | 084aff8 | 1.082x ↑<br>[📄](results/bm-20261013-3.16.0a1%2Bdev-084aff8/bm-20261013-vultr-x86_64-python-084aff869c4aa2f2cbdf-3.16.0a1%2Bdev-084aff8-vs-3.12.6.md)[📈](results/bm-20261013-3.16.0a1%2Bdev-084aff8/bm-20261013-vultr-x86_64-python-084aff869c4aa2f2cbdf-3.16.0a1%2Bdev-084aff8-vs-3.12.6.svg) | 1.045x ↑<br>[📄](results/bm-20261013-3.16.0a1%2Bdev-084aff8/bm-20261013-vultr-x86_64-python-084aff869c4aa2f2cbdf-3.16.0a1%2Bdev-084aff8-vs-3.13.0rc2.md)[📈](results/bm-20261013-3.16.0a1%2Bdev-084aff8/bm-20261013-vultr-x86_64-python-084aff869c4aa2f2cbdf-3.16.0a1%2Bdev-084aff8-vs-3.13.0rc2.svg) |  |
| [2026-10-13](results/bm-20261013-3.16.0a0-8b9cb49-NOGIL) | corona10/gh_159111 | 8b9cb49 (NOGIL) | 1.038x ↓<br>[📄](results/bm-20261013-3.16.0a0-8b9cb49-NOGIL/bm-20261013-vultr-x86_64-corona10-gh_159111-3.16.0a0-8b9cb49-vs-3.12.6.md)[📈](results/bm-20261013-3.16.0a0-8b9cb49-NOGIL/bm-20261013-vultr-x86_64-corona10-gh_159111-3.16.0a0-8b9cb49-vs-3.12.6.svg) | 1.071x ↓<br>[📄](results/bm-20261013-3.16.0a0-8b9cb49-NOGIL/bm-20261013-vultr-x86_64-corona10-gh_159111-3.16.0a0-8b9cb49-vs-3.13.0rc2.md)[📈](results/bm-20261013-3.16.0a0-8b9cb49-NOGIL/bm-20261013-vultr-x86_64-corona10-gh_159111-3.16.0a0-8b9cb49-vs-3.13.0rc2.svg) | 1.003x ↑<br>[📄](results/bm-20261013-3.16.0a0-8b9cb49-NOGIL/bm-20261013-vultr-x86_64-corona10-gh_159111-3.16.0a0-8b9cb49-vs-base.md)[📈](results/bm-20261013-3.16.0a0-8b9cb49-NOGIL/bm-20261013-vultr-x86_64-corona10-gh_159111-3.16.0a0-8b9cb49-vs-base.svg)[🧠](results/bm-20261013-3.16.0a0-8b9cb49-NOGIL/bm-20261013-vultr-x86_64-corona10-gh_159111-3.16.0a0-8b9cb49-vs-base-mem.svg) |
| [2026-10-12](results/bm-20261012-3.16.0a0-64018ac-NOGIL) | python/64018ac45cbc3f408412 | 64018ac (NOGIL) | 1.040x ↓<br>[📄](results/bm-20261012-3.16.0a0-64018ac-NOGIL/bm-20261012-vultr-x86_64-python-64018ac45cbc3f408412-3.16.0a0-64018ac-vs-3.12.6.md)[📈](results/bm-20261012-3.16.0a0-64018ac-NOGIL/bm-20261012-vultr-x86_64-python-64018ac45cbc3f408412-3.16.0a0-64018ac-vs-3.12.6.svg) | 1.073x ↓<br>[📄](results/bm-20261012-3.16.0a0-64018ac-NOGIL/bm-20261012-vultr-x86_64-python-64018ac45cbc3f408412-3.16.0a0-64018ac-vs-3.13.0rc2.md)[📈](results/bm-20261012-3.16.0a0-64018ac-NOGIL/bm-20261012-vultr-x86_64-python-64018ac45cbc3f408412-3.16.0a0-64018ac-vs-3.13.0rc2.svg) | 1.109x ↓<br>[📄](results/bm-20261012-3.16.0a0-64018ac-NOGIL/bm-20261012-vultr-x86_64-python-64018ac45cbc3f408412-3.16.0a0-64018ac-vs-base.md)[📈](results/bm-20261012-3.16.0a0-64018ac-NOGIL/bm-20261012-vultr-x86_64-python-64018ac45cbc3f408412-3.16.0a0-64018ac-vs-base.svg)[🧠](results/bm-20261012-3.16.0a0-64018ac-NOGIL/bm-20261012-vultr-x86_64-python-64018ac45cbc3f408412-3.16.0a0-64018ac-vs-base-mem.svg) |
| [2026-10-12](results/bm-20261012-3.16.0a0-64018ac) | python/64018ac45cbc3f408412 | 64018ac | 1.074x ↑<br>[📄](results/bm-20261012-3.16.0a0-64018ac/bm-20261012-vultr-x86_64-python-64018ac45cbc3f408412-3.16.0a0-64018ac-vs-3.12.6.md)[📈](results/bm-20261012-3.16.0a0-64018ac/bm-20261012-vultr-x86_64-python-64018ac45cbc3f408412-3.16.0a0-64018ac-vs-3.12.6.svg) | 1.037x ↑<br>[📄](results/bm-20261012-3.16.0a0-64018ac/bm-20261012-vultr-x86_64-python-64018ac45cbc3f408412-3.16.0a0-64018ac-vs-3.13.0rc2.md)[📈](results/bm-20261012-3.16.0a0-64018ac/bm-20261012-vultr-x86_64-python-64018ac45cbc3f408412-3.16.0a0-64018ac-vs-3.13.0rc2.svg) |  |
| [2026-10-11](results/bm-20261011-3.16.0a0-aab474a-NOGIL) | python/aab474a35b7d47aa3404 | aab474a (NOGIL) | 1.039x ↓<br>[📄](results/bm-20261011-3.16.0a0-aab474a-NOGIL/bm-20261011-vultr-x86_64-python-aab474a35b7d47aa3404-3.16.0a0-aab474a-vs-3.12.6.md)[📈](results/bm-20261011-3.16.0a0-aab474a-NOGIL/bm-20261011-vultr-x86_64-python-aab474a35b7d47aa3404-3.16.0a0-aab474a-vs-3.12.6.svg) | 1.072x ↓<br>[📄](results/bm-20261011-3.16.0a0-aab474a-NOGIL/bm-20261011-vultr-x86_64-python-aab474a35b7d47aa3404-3.16.0a0-aab474a-vs-3.13.0rc2.md)[📈](results/bm-20261011-3.16.0a0-aab474a-NOGIL/bm-20261011-vultr-x86_64-python-aab474a35b7d47aa3404-3.16.0a0-aab474a-vs-3.13.0rc2.svg) | 1.115x ↓<br>[📄](results/bm-20261011-3.16.0a0-aab474a-NOGIL/bm-20261011-vultr-x86_64-python-aab474a35b7d47aa3404-3.16.0a0-aab474a-vs-base.md)[📈](results/bm-20261011-3.16.0a0-aab474a-NOGIL/bm-20261011-vultr-x86_64-python-aab474a35b7d47aa3404-3.16.0a0-aab474a-vs-base.svg)[🧠](results/bm-20261011-3.16.0a0-aab474a-NOGIL/bm-20261011-vultr-x86_64-python-aab474a35b7d47aa3404-3.16.0a0-aab474a-vs-base-mem.svg) |
| [2026-10-11](results/bm-20261011-3.16.0a0-aab474a) | python/aab474a35b7d47aa3404 | aab474a | 1.084x ↑<br>[📄](results/bm-20261011-3.16.0a0-aab474a/bm-20261011-vultr-x86_64-python-aab474a35b7d47aa3404-3.16.0a0-aab474a-vs-3.12.6.md)[📈](results/bm-20261011-3.16.0a0-aab474a/bm-20261011-vultr-x86_64-python-aab474a35b7d47aa3404-3.16.0a0-aab474a-vs-3.12.6.svg) | 1.047x ↑<br>[📄](results/bm-20261011-3.16.0a0-aab474a/bm-20261011-vultr-x86_64-python-aab474a35b7d47aa3404-3.16.0a0-aab474a-vs-3.13.0rc2.md)[📈](results/bm-20261011-3.16.0a0-aab474a/bm-20261011-vultr-x86_64-python-aab474a35b7d47aa3404-3.16.0a0-aab474a-vs-3.13.0rc2.svg) |  |
| [2026-10-11](results/bm-20261011-3.16.0a0-1967a87-NOGIL) | python/1967a87ad395552dbd1e | 1967a87 (NOGIL) | 1.040x ↓<br>[📄](results/bm-20261011-3.16.0a0-1967a87-NOGIL/bm-20261011-vultr-x86_64-python-1967a87ad395552dbd1e-3.16.0a0-1967a87-vs-3.12.6.md)[📈](results/bm-20261011-3.16.0a0-1967a87-NOGIL/bm-20261011-vultr-x86_64-python-1967a87ad395552dbd1e-3.16.0a0-1967a87-vs-3.12.6.svg) | 1.073x ↓<br>[📄](results/bm-20261011-3.16.0a0-1967a87-NOGIL/bm-20261011-vultr-x86_64-python-1967a87ad395552dbd1e-3.16.0a0-1967a87-vs-3.13.0rc2.md)[📈](results/bm-20261011-3.16.0a0-1967a87-NOGIL/bm-20261011-vultr-x86_64-python-1967a87ad395552dbd1e-3.16.0a0-1967a87-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-10-14](results/bm-20261014-3.16.0a1%2Bdev-a6b4aa6-NOGIL) | python/a6b4aa687cd9f8f95e3b | a6b4aa6 (NOGIL) | 1.059x ↑<br>[📄](results/bm-20261014-3.16.0a1%2Bdev-a6b4aa6-NOGIL/bm-20261014-macm4pro-arm64-python-a6b4aa687cd9f8f95e3b-3.16.0a1%2Bdev-a6b4aa6-vs-3.12.6.md)[📈](results/bm-20261014-3.16.0a1%2Bdev-a6b4aa6-NOGIL/bm-20261014-macm4pro-arm64-python-a6b4aa687cd9f8f95e3b-3.16.0a1%2Bdev-a6b4aa6-vs-3.12.6.svg) | 1.019x ↓<br>[📄](results/bm-20261014-3.16.0a1%2Bdev-a6b4aa6-NOGIL/bm-20261014-macm4pro-arm64-python-a6b4aa687cd9f8f95e3b-3.16.0a1%2Bdev-a6b4aa6-vs-3.13.0rc2.md)[📈](results/bm-20261014-3.16.0a1%2Bdev-a6b4aa6-NOGIL/bm-20261014-macm4pro-arm64-python-a6b4aa687cd9f8f95e3b-3.16.0a1%2Bdev-a6b4aa6-vs-3.13.0rc2.svg) | 1.102x ↓<br>[📄](results/bm-20261014-3.16.0a1%2Bdev-a6b4aa6-NOGIL/bm-20261014-macm4pro-arm64-python-a6b4aa687cd9f8f95e3b-3.16.0a1%2Bdev-a6b4aa6-vs-base.md)[📈](results/bm-20261014-3.16.0a1%2Bdev-a6b4aa6-NOGIL/bm-20261014-macm4pro-arm64-python-a6b4aa687cd9f8f95e3b-3.16.0a1%2Bdev-a6b4aa6-vs-base.svg)[🧠](results/bm-20261014-3.16.0a1%2Bdev-a6b4aa6-NOGIL/bm-20261014-macm4pro-arm64-python-a6b4aa687cd9f8f95e3b-3.16.0a1%2Bdev-a6b4aa6-vs-base-mem.svg) |
| [2026-10-14](results/bm-20261014-3.16.0a1%2Bdev-a6b4aa6) | python/a6b4aa687cd9f8f95e3b | a6b4aa6 | 1.185x ↑<br>[📄](results/bm-20261014-3.16.0a1%2Bdev-a6b4aa6/bm-20261014-macm4pro-arm64-python-a6b4aa687cd9f8f95e3b-3.16.0a1%2Bdev-a6b4aa6-vs-3.12.6.md)[📈](results/bm-20261014-3.16.0a1%2Bdev-a6b4aa6/bm-20261014-macm4pro-arm64-python-a6b4aa687cd9f8f95e3b-3.16.0a1%2Bdev-a6b4aa6-vs-3.12.6.svg) | 1.095x ↑<br>[📄](results/bm-20261014-3.16.0a1%2Bdev-a6b4aa6/bm-20261014-macm4pro-arm64-python-a6b4aa687cd9f8f95e3b-3.16.0a1%2Bdev-a6b4aa6-vs-3.13.0rc2.md)[📈](results/bm-20261014-3.16.0a1%2Bdev-a6b4aa6/bm-20261014-macm4pro-arm64-python-a6b4aa687cd9f8f95e3b-3.16.0a1%2Bdev-a6b4aa6-vs-3.13.0rc2.svg) |  |
| [2026-10-13](results/bm-20261013-3.16.0a1%2Bdev-084aff8-NOGIL) | python/084aff869c4aa2f2cbdf | 084aff8 (NOGIL) | 1.063x ↑<br>[📄](results/bm-20261013-3.16.0a1%2Bdev-084aff8-NOGIL/bm-20261013-macm4pro-arm64-python-084aff869c4aa2f2cbdf-3.16.0a1%2Bdev-084aff8-vs-3.12.6.md)[📈](results/bm-20261013-3.16.0a1%2Bdev-084aff8-NOGIL/bm-20261013-macm4pro-arm64-python-084aff869c4aa2f2cbdf-3.16.0a1%2Bdev-084aff8-vs-3.12.6.svg) | 1.015x ↓<br>[📄](results/bm-20261013-3.16.0a1%2Bdev-084aff8-NOGIL/bm-20261013-macm4pro-arm64-python-084aff869c4aa2f2cbdf-3.16.0a1%2Bdev-084aff8-vs-3.13.0rc2.md)[📈](results/bm-20261013-3.16.0a1%2Bdev-084aff8-NOGIL/bm-20261013-macm4pro-arm64-python-084aff869c4aa2f2cbdf-3.16.0a1%2Bdev-084aff8-vs-3.13.0rc2.svg) | 1.098x ↓<br>[📄](results/bm-20261013-3.16.0a1%2Bdev-084aff8-NOGIL/bm-20261013-macm4pro-arm64-python-084aff869c4aa2f2cbdf-3.16.0a1%2Bdev-084aff8-vs-base.md)[📈](results/bm-20261013-3.16.0a1%2Bdev-084aff8-NOGIL/bm-20261013-macm4pro-arm64-python-084aff869c4aa2f2cbdf-3.16.0a1%2Bdev-084aff8-vs-base.svg)[🧠](results/bm-20261013-3.16.0a1%2Bdev-084aff8-NOGIL/bm-20261013-macm4pro-arm64-python-084aff869c4aa2f2cbdf-3.16.0a1%2Bdev-084aff8-vs-base-mem.svg) |
| [2026-10-13](results/bm-20261013-3.16.0a1%2Bdev-084aff8) | python/084aff869c4aa2f2cbdf | 084aff8 | 1.184x ↑<br>[📄](results/bm-20261013-3.16.0a1%2Bdev-084aff8/bm-20261013-macm4pro-arm64-python-084aff869c4aa2f2cbdf-3.16.0a1%2Bdev-084aff8-vs-3.12.6.md)[📈](results/bm-20261013-3.16.0a1%2Bdev-084aff8/bm-20261013-macm4pro-arm64-python-084aff869c4aa2f2cbdf-3.16.0a1%2Bdev-084aff8-vs-3.12.6.svg) | 1.094x ↑<br>[📄](results/bm-20261013-3.16.0a1%2Bdev-084aff8/bm-20261013-macm4pro-arm64-python-084aff869c4aa2f2cbdf-3.16.0a1%2Bdev-084aff8-vs-3.13.0rc2.md)[📈](results/bm-20261013-3.16.0a1%2Bdev-084aff8/bm-20261013-macm4pro-arm64-python-084aff869c4aa2f2cbdf-3.16.0a1%2Bdev-084aff8-vs-3.13.0rc2.svg) |  |
| [2026-10-12](results/bm-20261012-3.16.0a0-64018ac) | python/64018ac45cbc3f408412 | 64018ac | 1.191x ↑<br>[📄](results/bm-20261012-3.16.0a0-64018ac/bm-20261012-macm4pro-arm64-python-64018ac45cbc3f408412-3.16.0a0-64018ac-vs-3.12.6.md)[📈](results/bm-20261012-3.16.0a0-64018ac/bm-20261012-macm4pro-arm64-python-64018ac45cbc3f408412-3.16.0a0-64018ac-vs-3.12.6.svg) | 1.101x ↑<br>[📄](results/bm-20261012-3.16.0a0-64018ac/bm-20261012-macm4pro-arm64-python-64018ac45cbc3f408412-3.16.0a0-64018ac-vs-3.13.0rc2.md)[📈](results/bm-20261012-3.16.0a0-64018ac/bm-20261012-macm4pro-arm64-python-64018ac45cbc3f408412-3.16.0a0-64018ac-vs-3.13.0rc2.svg) |  |
| [2026-10-11](results/bm-20261011-3.16.0a0-aab474a-NOGIL) | python/aab474a35b7d47aa3404 | aab474a (NOGIL) | 1.067x ↑<br>[📄](results/bm-20261011-3.16.0a0-aab474a-NOGIL/bm-20261011-macm4pro-arm64-python-aab474a35b7d47aa3404-3.16.0a0-aab474a-vs-3.12.6.md)[📈](results/bm-20261011-3.16.0a0-aab474a-NOGIL/bm-20261011-macm4pro-arm64-python-aab474a35b7d47aa3404-3.16.0a0-aab474a-vs-3.12.6.svg) | 1.012x ↓<br>[📄](results/bm-20261011-3.16.0a0-aab474a-NOGIL/bm-20261011-macm4pro-arm64-python-aab474a35b7d47aa3404-3.16.0a0-aab474a-vs-3.13.0rc2.md)[📈](results/bm-20261011-3.16.0a0-aab474a-NOGIL/bm-20261011-macm4pro-arm64-python-aab474a35b7d47aa3404-3.16.0a0-aab474a-vs-3.13.0rc2.svg) | 1.098x ↓<br>[📄](results/bm-20261011-3.16.0a0-aab474a-NOGIL/bm-20261011-macm4pro-arm64-python-aab474a35b7d47aa3404-3.16.0a0-aab474a-vs-base.md)[📈](results/bm-20261011-3.16.0a0-aab474a-NOGIL/bm-20261011-macm4pro-arm64-python-aab474a35b7d47aa3404-3.16.0a0-aab474a-vs-base.svg)[🧠](results/bm-20261011-3.16.0a0-aab474a-NOGIL/bm-20261011-macm4pro-arm64-python-aab474a35b7d47aa3404-3.16.0a0-aab474a-vs-base-mem.svg) |
| [2026-10-11](results/bm-20261011-3.16.0a0-aab474a) | python/aab474a35b7d47aa3404 | aab474a | 1.188x ↑<br>[📄](results/bm-20261011-3.16.0a0-aab474a/bm-20261011-macm4pro-arm64-python-aab474a35b7d47aa3404-3.16.0a0-aab474a-vs-3.12.6.md)[📈](results/bm-20261011-3.16.0a0-aab474a/bm-20261011-macm4pro-arm64-python-aab474a35b7d47aa3404-3.16.0a0-aab474a-vs-3.12.6.svg) | 1.097x ↑<br>[📄](results/bm-20261011-3.16.0a0-aab474a/bm-20261011-macm4pro-arm64-python-aab474a35b7d47aa3404-3.16.0a0-aab474a-vs-3.13.0rc2.md)[📈](results/bm-20261011-3.16.0a0-aab474a/bm-20261011-macm4pro-arm64-python-aab474a35b7d47aa3404-3.16.0a0-aab474a-vs-3.13.0rc2.svg) |  |


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
