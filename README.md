# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (22a4421)](results/bm-20250111-3.14.0a3%2B-22a4421/bm-20250111-vultr-x86_64-python-22a442181d5f1ac496da-3.14.0a3%2B-22a4421-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (22a4421)](results/bm-20250111-3.14.0a3%2B-22a4421-PYTHON_UOPS/bm-20250111-vultr-x86_64-python-22a442181d5f1ac496da-3.14.0a3%2B-22a4421-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-06-05](results/bm-20250605-3.15.0a0-04ccde3-NOGIL) | nascheme/gh_132380_tp_getattr | 04ccde3 (NOGIL) | 1.015x ↑<br>[📄](results/bm-20250605-3.15.0a0-04ccde3-NOGIL/bm-20250605-vultr-x86_64-nascheme-gh_132380_tp_getattr-3.15.0a0-04ccde3-vs-3.12.6.md)[📈](results/bm-20250605-3.15.0a0-04ccde3-NOGIL/bm-20250605-vultr-x86_64-nascheme-gh_132380_tp_getattr-3.15.0a0-04ccde3-vs-3.12.6.svg) | 1.020x ↓<br>[📄](results/bm-20250605-3.15.0a0-04ccde3-NOGIL/bm-20250605-vultr-x86_64-nascheme-gh_132380_tp_getattr-3.15.0a0-04ccde3-vs-3.13.0rc2.md)[📈](results/bm-20250605-3.15.0a0-04ccde3-NOGIL/bm-20250605-vultr-x86_64-nascheme-gh_132380_tp_getattr-3.15.0a0-04ccde3-vs-3.13.0rc2.svg) | 1.001x ↓<br>[📄](results/bm-20250605-3.15.0a0-04ccde3-NOGIL/bm-20250605-vultr-x86_64-nascheme-gh_132380_tp_getattr-3.15.0a0-04ccde3-vs-base.md)[📈](results/bm-20250605-3.15.0a0-04ccde3-NOGIL/bm-20250605-vultr-x86_64-nascheme-gh_132380_tp_getattr-3.15.0a0-04ccde3-vs-base.svg)[🧠](results/bm-20250605-3.15.0a0-04ccde3-NOGIL/bm-20250605-vultr-x86_64-nascheme-gh_132380_tp_getattr-3.15.0a0-04ccde3-vs-base-mem.svg) |
| [2025-06-05](results/bm-20250605-3.15.0a0-b90ecea-NOGIL) | python/b90ecea9e6b33dae360e | b90ecea (NOGIL) | 1.016x ↑<br>[📄](results/bm-20250605-3.15.0a0-b90ecea-NOGIL/bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea-vs-3.12.6.md)[📈](results/bm-20250605-3.15.0a0-b90ecea-NOGIL/bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea-vs-3.12.6.svg) | 1.019x ↓<br>[📄](results/bm-20250605-3.15.0a0-b90ecea-NOGIL/bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea-vs-3.13.0rc2.md)[📈](results/bm-20250605-3.15.0a0-b90ecea-NOGIL/bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea-vs-3.13.0rc2.svg) | 1.086x ↓<br>[📄](results/bm-20250605-3.15.0a0-b90ecea-NOGIL/bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea-vs-base.md)[📈](results/bm-20250605-3.15.0a0-b90ecea-NOGIL/bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea-vs-base.svg)[🧠](results/bm-20250605-3.15.0a0-b90ecea-NOGIL/bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea-vs-base-mem.svg) |
| [2025-06-05](results/bm-20250605-3.15.0a0-b90ecea) | python/b90ecea9e6b33dae360e | b90ecea | 1.105x ↑<br>[📄](results/bm-20250605-3.15.0a0-b90ecea/bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea-vs-3.12.6.md)[📈](results/bm-20250605-3.15.0a0-b90ecea/bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea-vs-3.12.6.svg) | 1.067x ↑<br>[📄](results/bm-20250605-3.15.0a0-b90ecea/bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea-vs-3.13.0rc2.md)[📈](results/bm-20250605-3.15.0a0-b90ecea/bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea-vs-3.13.0rc2.svg) |  |
| [2025-06-04](results/bm-20250604-3.15.0a0-6b77af2-NOGIL) | python/6b77af257c25d31f1f13 | 6b77af2 (NOGIL) | 1.009x ↑<br>[📄](results/bm-20250604-3.15.0a0-6b77af2-NOGIL/bm-20250604-vultr-x86_64-python-6b77af257c25d31f1f13-3.15.0a0-6b77af2-vs-3.12.6.md)[📈](results/bm-20250604-3.15.0a0-6b77af2-NOGIL/bm-20250604-vultr-x86_64-python-6b77af257c25d31f1f13-3.15.0a0-6b77af2-vs-3.12.6.svg) | 1.026x ↓<br>[📄](results/bm-20250604-3.15.0a0-6b77af2-NOGIL/bm-20250604-vultr-x86_64-python-6b77af257c25d31f1f13-3.15.0a0-6b77af2-vs-3.13.0rc2.md)[📈](results/bm-20250604-3.15.0a0-6b77af2-NOGIL/bm-20250604-vultr-x86_64-python-6b77af257c25d31f1f13-3.15.0a0-6b77af2-vs-3.13.0rc2.svg) | 1.095x ↓<br>[📄](results/bm-20250604-3.15.0a0-6b77af2-NOGIL/bm-20250604-vultr-x86_64-python-6b77af257c25d31f1f13-3.15.0a0-6b77af2-vs-base.md)[📈](results/bm-20250604-3.15.0a0-6b77af2-NOGIL/bm-20250604-vultr-x86_64-python-6b77af257c25d31f1f13-3.15.0a0-6b77af2-vs-base.svg)[🧠](results/bm-20250604-3.15.0a0-6b77af2-NOGIL/bm-20250604-vultr-x86_64-python-6b77af257c25d31f1f13-3.15.0a0-6b77af2-vs-base-mem.svg) |
| [2025-06-04](results/bm-20250604-3.15.0a0-6b77af2) | python/6b77af257c25d31f1f13 | 6b77af2 | 1.111x ↑<br>[📄](results/bm-20250604-3.15.0a0-6b77af2/bm-20250604-vultr-x86_64-python-6b77af257c25d31f1f13-3.15.0a0-6b77af2-vs-3.12.6.md)[📈](results/bm-20250604-3.15.0a0-6b77af2/bm-20250604-vultr-x86_64-python-6b77af257c25d31f1f13-3.15.0a0-6b77af2-vs-3.12.6.svg) | 1.073x ↑<br>[📄](results/bm-20250604-3.15.0a0-6b77af2/bm-20250604-vultr-x86_64-python-6b77af257c25d31f1f13-3.15.0a0-6b77af2-vs-3.13.0rc2.md)[📈](results/bm-20250604-3.15.0a0-6b77af2/bm-20250604-vultr-x86_64-python-6b77af257c25d31f1f13-3.15.0a0-6b77af2-vs-3.13.0rc2.svg) |  |
| [2025-06-03](results/bm-20250603-3.15.0a0-1ffe913-NOGIL) | python/1ffe913c2017b44804ac | 1ffe913 (NOGIL) | 1.017x ↑<br>[📄](results/bm-20250603-3.15.0a0-1ffe913-NOGIL/bm-20250603-vultr-x86_64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913-vs-3.12.6.md)[📈](results/bm-20250603-3.15.0a0-1ffe913-NOGIL/bm-20250603-vultr-x86_64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913-vs-3.12.6.svg) | 1.019x ↓<br>[📄](results/bm-20250603-3.15.0a0-1ffe913-NOGIL/bm-20250603-vultr-x86_64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913-vs-3.13.0rc2.md)[📈](results/bm-20250603-3.15.0a0-1ffe913-NOGIL/bm-20250603-vultr-x86_64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913-vs-3.13.0rc2.svg) | 1.088x ↓<br>[📄](results/bm-20250603-3.15.0a0-1ffe913-NOGIL/bm-20250603-vultr-x86_64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913-vs-base.md)[📈](results/bm-20250603-3.15.0a0-1ffe913-NOGIL/bm-20250603-vultr-x86_64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913-vs-base.svg)[🧠](results/bm-20250603-3.15.0a0-1ffe913-NOGIL/bm-20250603-vultr-x86_64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913-vs-base-mem.svg) |
| [2025-06-03](results/bm-20250603-3.15.0a0-1ffe913) | python/1ffe913c2017b44804ac | 1ffe913 | 1.107x ↑<br>[📄](results/bm-20250603-3.15.0a0-1ffe913/bm-20250603-vultr-x86_64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913-vs-3.12.6.md)[📈](results/bm-20250603-3.15.0a0-1ffe913/bm-20250603-vultr-x86_64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913-vs-3.12.6.svg) | 1.070x ↑<br>[📄](results/bm-20250603-3.15.0a0-1ffe913/bm-20250603-vultr-x86_64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913-vs-3.13.0rc2.md)[📈](results/bm-20250603-3.15.0a0-1ffe913/bm-20250603-vultr-x86_64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913-vs-3.13.0rc2.svg) |  |
| [2025-06-03](results/bm-20250603-3.15.0a0-db6d52e-NOGIL) | nascheme/gh_132380_tp_lookup_ | db6d52e (NOGIL) | 1.015x ↑<br>[📄](results/bm-20250603-3.15.0a0-db6d52e-NOGIL/bm-20250603-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.15.0a0-db6d52e-vs-3.12.6.md)[📈](results/bm-20250603-3.15.0a0-db6d52e-NOGIL/bm-20250603-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.15.0a0-db6d52e-vs-3.12.6.svg) | 1.020x ↓<br>[📄](results/bm-20250603-3.15.0a0-db6d52e-NOGIL/bm-20250603-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.15.0a0-db6d52e-vs-3.13.0rc2.md)[📈](results/bm-20250603-3.15.0a0-db6d52e-NOGIL/bm-20250603-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.15.0a0-db6d52e-vs-3.13.0rc2.svg) | 1.001x ↓<br>[📄](results/bm-20250603-3.15.0a0-db6d52e-NOGIL/bm-20250603-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.15.0a0-db6d52e-vs-base.md)[📈](results/bm-20250603-3.15.0a0-db6d52e-NOGIL/bm-20250603-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.15.0a0-db6d52e-vs-base.svg)[🧠](results/bm-20250603-3.15.0a0-db6d52e-NOGIL/bm-20250603-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.15.0a0-db6d52e-vs-base-mem.svg) |
| [2025-06-03](results/bm-20250603-3.15.0a0-b525e31-NOGIL) | python/b525e31b7fc50e7a498f | b525e31 (NOGIL) | 1.013x ↑<br>[📄](results/bm-20250603-3.15.0a0-b525e31-NOGIL/bm-20250603-vultr-x86_64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31-vs-3.12.6.md)[📈](results/bm-20250603-3.15.0a0-b525e31-NOGIL/bm-20250603-vultr-x86_64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31-vs-3.12.6.svg) | 1.022x ↓<br>[📄](results/bm-20250603-3.15.0a0-b525e31-NOGIL/bm-20250603-vultr-x86_64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31-vs-3.13.0rc2.md)[📈](results/bm-20250603-3.15.0a0-b525e31-NOGIL/bm-20250603-vultr-x86_64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31-vs-3.13.0rc2.svg) | 1.092x ↓<br>[📄](results/bm-20250603-3.15.0a0-b525e31-NOGIL/bm-20250603-vultr-x86_64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31-vs-base.md)[📈](results/bm-20250603-3.15.0a0-b525e31-NOGIL/bm-20250603-vultr-x86_64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31-vs-base.svg)[🧠](results/bm-20250603-3.15.0a0-b525e31-NOGIL/bm-20250603-vultr-x86_64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31-vs-base-mem.svg) |
| [2025-06-03](results/bm-20250603-3.15.0a0-b525e31) | python/b525e31b7fc50e7a498f | b525e31 | 1.109x ↑<br>[📄](results/bm-20250603-3.15.0a0-b525e31/bm-20250603-vultr-x86_64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31-vs-3.12.6.md)[📈](results/bm-20250603-3.15.0a0-b525e31/bm-20250603-vultr-x86_64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31-vs-3.12.6.svg) | 1.071x ↑<br>[📄](results/bm-20250603-3.15.0a0-b525e31/bm-20250603-vultr-x86_64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31-vs-3.13.0rc2.md)[📈](results/bm-20250603-3.15.0a0-b525e31/bm-20250603-vultr-x86_64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-06-05](results/bm-20250605-3.15.0a0-b90ecea-NOGIL) | python/b90ecea9e6b33dae360e | b90ecea (NOGIL) | 1.093x ↑<br>[📄](results/bm-20250605-3.15.0a0-b90ecea-NOGIL/bm-20250605-macm4pro-arm64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea-vs-3.12.6.md)[📈](results/bm-20250605-3.15.0a0-b90ecea-NOGIL/bm-20250605-macm4pro-arm64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea-vs-3.12.6.svg) | 1.013x ↑<br>[📄](results/bm-20250605-3.15.0a0-b90ecea-NOGIL/bm-20250605-macm4pro-arm64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea-vs-3.13.0rc2.md)[📈](results/bm-20250605-3.15.0a0-b90ecea-NOGIL/bm-20250605-macm4pro-arm64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea-vs-3.13.0rc2.svg) | 1.022x ↓<br>[📄](results/bm-20250605-3.15.0a0-b90ecea-NOGIL/bm-20250605-macm4pro-arm64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea-vs-base.md)[📈](results/bm-20250605-3.15.0a0-b90ecea-NOGIL/bm-20250605-macm4pro-arm64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea-vs-base.svg)[🧠](results/bm-20250605-3.15.0a0-b90ecea-NOGIL/bm-20250605-macm4pro-arm64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea-vs-base-mem.svg) |
| [2025-06-05](results/bm-20250605-3.15.0a0-b90ecea) | python/b90ecea9e6b33dae360e | b90ecea | 1.115x ↑<br>[📄](results/bm-20250605-3.15.0a0-b90ecea/bm-20250605-macm4pro-arm64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea-vs-3.12.6.md)[📈](results/bm-20250605-3.15.0a0-b90ecea/bm-20250605-macm4pro-arm64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea-vs-3.12.6.svg) | 1.034x ↑<br>[📄](results/bm-20250605-3.15.0a0-b90ecea/bm-20250605-macm4pro-arm64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea-vs-3.13.0rc2.md)[📈](results/bm-20250605-3.15.0a0-b90ecea/bm-20250605-macm4pro-arm64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea-vs-3.13.0rc2.svg) |  |
| [2025-06-04](results/bm-20250604-3.15.0a0-6b77af2-NOGIL) | python/6b77af257c25d31f1f13 | 6b77af2 (NOGIL) | 1.100x ↑<br>[📄](results/bm-20250604-3.15.0a0-6b77af2-NOGIL/bm-20250604-macm4pro-arm64-python-6b77af257c25d31f1f13-3.15.0a0-6b77af2-vs-3.12.6.md)[📈](results/bm-20250604-3.15.0a0-6b77af2-NOGIL/bm-20250604-macm4pro-arm64-python-6b77af257c25d31f1f13-3.15.0a0-6b77af2-vs-3.12.6.svg) | 1.019x ↑<br>[📄](results/bm-20250604-3.15.0a0-6b77af2-NOGIL/bm-20250604-macm4pro-arm64-python-6b77af257c25d31f1f13-3.15.0a0-6b77af2-vs-3.13.0rc2.md)[📈](results/bm-20250604-3.15.0a0-6b77af2-NOGIL/bm-20250604-macm4pro-arm64-python-6b77af257c25d31f1f13-3.15.0a0-6b77af2-vs-3.13.0rc2.svg) | 1.026x ↓<br>[📄](results/bm-20250604-3.15.0a0-6b77af2-NOGIL/bm-20250604-macm4pro-arm64-python-6b77af257c25d31f1f13-3.15.0a0-6b77af2-vs-base.md)[📈](results/bm-20250604-3.15.0a0-6b77af2-NOGIL/bm-20250604-macm4pro-arm64-python-6b77af257c25d31f1f13-3.15.0a0-6b77af2-vs-base.svg)[🧠](results/bm-20250604-3.15.0a0-6b77af2-NOGIL/bm-20250604-macm4pro-arm64-python-6b77af257c25d31f1f13-3.15.0a0-6b77af2-vs-base-mem.svg) |
| [2025-06-04](results/bm-20250604-3.15.0a0-6b77af2) | python/6b77af257c25d31f1f13 | 6b77af2 | 1.125x ↑<br>[📄](results/bm-20250604-3.15.0a0-6b77af2/bm-20250604-macm4pro-arm64-python-6b77af257c25d31f1f13-3.15.0a0-6b77af2-vs-3.12.6.md)[📈](results/bm-20250604-3.15.0a0-6b77af2/bm-20250604-macm4pro-arm64-python-6b77af257c25d31f1f13-3.15.0a0-6b77af2-vs-3.12.6.svg) | 1.044x ↑<br>[📄](results/bm-20250604-3.15.0a0-6b77af2/bm-20250604-macm4pro-arm64-python-6b77af257c25d31f1f13-3.15.0a0-6b77af2-vs-3.13.0rc2.md)[📈](results/bm-20250604-3.15.0a0-6b77af2/bm-20250604-macm4pro-arm64-python-6b77af257c25d31f1f13-3.15.0a0-6b77af2-vs-3.13.0rc2.svg) |  |
| [2025-06-03](results/bm-20250603-3.15.0a0-1ffe913-NOGIL) | python/1ffe913c2017b44804ac | 1ffe913 (NOGIL) | 1.092x ↑<br>[📄](results/bm-20250603-3.15.0a0-1ffe913-NOGIL/bm-20250603-macm4pro-arm64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913-vs-3.12.6.md)[📈](results/bm-20250603-3.15.0a0-1ffe913-NOGIL/bm-20250603-macm4pro-arm64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913-vs-3.12.6.svg) | 1.012x ↑<br>[📄](results/bm-20250603-3.15.0a0-1ffe913-NOGIL/bm-20250603-macm4pro-arm64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913-vs-3.13.0rc2.md)[📈](results/bm-20250603-3.15.0a0-1ffe913-NOGIL/bm-20250603-macm4pro-arm64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913-vs-3.13.0rc2.svg) | 1.021x ↓<br>[📄](results/bm-20250603-3.15.0a0-1ffe913-NOGIL/bm-20250603-macm4pro-arm64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913-vs-base.md)[📈](results/bm-20250603-3.15.0a0-1ffe913-NOGIL/bm-20250603-macm4pro-arm64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913-vs-base.svg)[🧠](results/bm-20250603-3.15.0a0-1ffe913-NOGIL/bm-20250603-macm4pro-arm64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913-vs-base-mem.svg) |
| [2025-06-03](results/bm-20250603-3.15.0a0-1ffe913) | python/1ffe913c2017b44804ac | 1ffe913 | 1.112x ↑<br>[📄](results/bm-20250603-3.15.0a0-1ffe913/bm-20250603-macm4pro-arm64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913-vs-3.12.6.md)[📈](results/bm-20250603-3.15.0a0-1ffe913/bm-20250603-macm4pro-arm64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913-vs-3.12.6.svg) | 1.032x ↑<br>[📄](results/bm-20250603-3.15.0a0-1ffe913/bm-20250603-macm4pro-arm64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913-vs-3.13.0rc2.md)[📈](results/bm-20250603-3.15.0a0-1ffe913/bm-20250603-macm4pro-arm64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913-vs-3.13.0rc2.svg) |  |
| [2025-06-03](results/bm-20250603-3.15.0a0-b525e31-NOGIL) | python/b525e31b7fc50e7a498f | b525e31 (NOGIL) | 1.100x ↑<br>[📄](results/bm-20250603-3.15.0a0-b525e31-NOGIL/bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31-vs-3.12.6.md)[📈](results/bm-20250603-3.15.0a0-b525e31-NOGIL/bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31-vs-3.12.6.svg) | 1.019x ↑<br>[📄](results/bm-20250603-3.15.0a0-b525e31-NOGIL/bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31-vs-3.13.0rc2.md)[📈](results/bm-20250603-3.15.0a0-b525e31-NOGIL/bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31-vs-3.13.0rc2.svg) | 1.021x ↓<br>[📄](results/bm-20250603-3.15.0a0-b525e31-NOGIL/bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31-vs-base.md)[📈](results/bm-20250603-3.15.0a0-b525e31-NOGIL/bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31-vs-base.svg)[🧠](results/bm-20250603-3.15.0a0-b525e31-NOGIL/bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31-vs-base-mem.svg) |
| [2025-06-03](results/bm-20250603-3.15.0a0-b525e31) | python/b525e31b7fc50e7a498f | b525e31 | 1.120x ↑<br>[📄](results/bm-20250603-3.15.0a0-b525e31/bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31-vs-3.12.6.md)[📈](results/bm-20250603-3.15.0a0-b525e31/bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31-vs-3.12.6.svg) | 1.039x ↑<br>[📄](results/bm-20250603-3.15.0a0-b525e31/bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31-vs-3.13.0rc2.md)[📈](results/bm-20250603-3.15.0a0-b525e31/bm-20250603-macm4pro-arm64-python-b525e31b7fc50e7a498f-3.15.0a0-b525e31-vs-3.13.0rc2.svg) |  |


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
