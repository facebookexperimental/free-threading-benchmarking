# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
[Most recent pystats on main (22a4421)](results/bm-20250111-3.14.0a3%2B-22a4421-PYTHON_UOPS/bm-20250111-vultr-x86_64-python-22a442181d5f1ac496da-3.14.0a3%2B-22a4421-pystats.md)

## linux x86_64 (linux)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-01-13](results/bm-20250113-3.14.0a3%2B-b70a567-NOGIL) | python/b70a567575db37846bee | b70a567 (NOGIL) | 1.185x ↓<br>[📄](results/bm-20250113-3.14.0a3%2B-b70a567-NOGIL/bm-20250113-linux-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-3.12.6.md)[📈](results/bm-20250113-3.14.0a3%2B-b70a567-NOGIL/bm-20250113-linux-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-3.12.6.svg) | 1.210x ↓<br>[📄](results/bm-20250113-3.14.0a3%2B-b70a567-NOGIL/bm-20250113-linux-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-3.13.0rc2.md)[📈](results/bm-20250113-3.14.0a3%2B-b70a567-NOGIL/bm-20250113-linux-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-3.13.0rc2.svg) |  |
| [2025-01-13](results/bm-20250113-3.14.0a3%2B-d0ecbdd-NOGIL) | python/d0ecbdd838034c1f061e | d0ecbdd (NOGIL) | 1.180x ↓<br>[📄](results/bm-20250113-3.14.0a3%2B-d0ecbdd-NOGIL/bm-20250113-linux-x86_64-python-d0ecbdd838034c1f061e-3.14.0a3%2B-d0ecbdd-vs-3.12.6.md)[📈](results/bm-20250113-3.14.0a3%2B-d0ecbdd-NOGIL/bm-20250113-linux-x86_64-python-d0ecbdd838034c1f061e-3.14.0a3%2B-d0ecbdd-vs-3.12.6.svg) | 1.211x ↓<br>[📄](results/bm-20250113-3.14.0a3%2B-d0ecbdd-NOGIL/bm-20250113-linux-x86_64-python-d0ecbdd838034c1f061e-3.14.0a3%2B-d0ecbdd-vs-3.13.0rc2.md)[📈](results/bm-20250113-3.14.0a3%2B-d0ecbdd-NOGIL/bm-20250113-linux-x86_64-python-d0ecbdd838034c1f061e-3.14.0a3%2B-d0ecbdd-vs-3.13.0rc2.svg) | 1.227x ↓<br>[📄](results/bm-20250113-3.14.0a3%2B-d0ecbdd-NOGIL/bm-20250113-linux-x86_64-python-d0ecbdd838034c1f061e-3.14.0a3%2B-d0ecbdd-vs-base.md)[📈](results/bm-20250113-3.14.0a3%2B-d0ecbdd-NOGIL/bm-20250113-linux-x86_64-python-d0ecbdd838034c1f061e-3.14.0a3%2B-d0ecbdd-vs-base.svg)[🧠](results/bm-20250113-3.14.0a3%2B-d0ecbdd-NOGIL/bm-20250113-linux-x86_64-python-d0ecbdd838034c1f061e-3.14.0a3%2B-d0ecbdd-vs-base-mem.svg) |
| [2025-01-13](results/bm-20250113-3.14.0a3%2B-d0ecbdd) | python/d0ecbdd838034c1f061e | d0ecbdd | 1.068x ↑<br>[📄](results/bm-20250113-3.14.0a3%2B-d0ecbdd/bm-20250113-linux-x86_64-python-d0ecbdd838034c1f061e-3.14.0a3%2B-d0ecbdd-vs-3.12.6.md)[📈](results/bm-20250113-3.14.0a3%2B-d0ecbdd/bm-20250113-linux-x86_64-python-d0ecbdd838034c1f061e-3.14.0a3%2B-d0ecbdd-vs-3.12.6.svg) | 1.026x ↑<br>[📄](results/bm-20250113-3.14.0a3%2B-d0ecbdd/bm-20250113-linux-x86_64-python-d0ecbdd838034c1f061e-3.14.0a3%2B-d0ecbdd-vs-3.13.0rc2.md)[📈](results/bm-20250113-3.14.0a3%2B-d0ecbdd/bm-20250113-linux-x86_64-python-d0ecbdd838034c1f061e-3.14.0a3%2B-d0ecbdd-vs-3.13.0rc2.svg) |  |
| [2025-01-13](results/bm-20250113-3.14.0a3%2B-54c551e-NOGIL) | Yhg1s/for_iter_spec | 54c551e (NOGIL) | 1.165x ↓<br>[📄](results/bm-20250113-3.14.0a3%2B-54c551e-NOGIL/bm-20250113-linux-x86_64-Yhg1s-for_iter_spec-3.14.0a3%2B-54c551e-vs-3.12.6.md)[📈](results/bm-20250113-3.14.0a3%2B-54c551e-NOGIL/bm-20250113-linux-x86_64-Yhg1s-for_iter_spec-3.14.0a3%2B-54c551e-vs-3.12.6.svg) | 1.194x ↓<br>[📄](results/bm-20250113-3.14.0a3%2B-54c551e-NOGIL/bm-20250113-linux-x86_64-Yhg1s-for_iter_spec-3.14.0a3%2B-54c551e-vs-3.13.0rc2.md)[📈](results/bm-20250113-3.14.0a3%2B-54c551e-NOGIL/bm-20250113-linux-x86_64-Yhg1s-for_iter_spec-3.14.0a3%2B-54c551e-vs-3.13.0rc2.svg) | 1.012x ↓<br>[📄](results/bm-20250113-3.14.0a3%2B-54c551e-NOGIL/bm-20250113-linux-x86_64-Yhg1s-for_iter_spec-3.14.0a3%2B-54c551e-vs-base.md)[📈](results/bm-20250113-3.14.0a3%2B-54c551e-NOGIL/bm-20250113-linux-x86_64-Yhg1s-for_iter_spec-3.14.0a3%2B-54c551e-vs-base.svg)[🧠](results/bm-20250113-3.14.0a3%2B-54c551e-NOGIL/bm-20250113-linux-x86_64-Yhg1s-for_iter_spec-3.14.0a3%2B-54c551e-vs-base-mem.svg) |
| [2025-01-11](results/bm-20250111-3.14.0a3%2B-22a4421) | python/22a442181d5f1ac496da | 22a4421 | 1.088x ↑<br>[📄](results/bm-20250111-3.14.0a3%2B-22a4421/bm-20250111-linux-x86_64-python-22a442181d5f1ac496da-3.14.0a3%2B-22a4421-vs-3.12.6.md)[📈](results/bm-20250111-3.14.0a3%2B-22a4421/bm-20250111-linux-x86_64-python-22a442181d5f1ac496da-3.14.0a3%2B-22a4421-vs-3.12.6.svg) | 1.043x ↑<br>[📄](results/bm-20250111-3.14.0a3%2B-22a4421/bm-20250111-linux-x86_64-python-22a442181d5f1ac496da-3.14.0a3%2B-22a4421-vs-3.13.0rc2.md)[📈](results/bm-20250111-3.14.0a3%2B-22a4421/bm-20250111-linux-x86_64-python-22a442181d5f1ac496da-3.14.0a3%2B-22a4421-vs-3.13.0rc2.svg) |  |
| [2025-01-11](results/bm-20250111-3.14.0a3%2B-22a4421-NOGIL) | python/22a442181d5f1ac496da | 22a4421 (NOGIL) | 1.174x ↓<br>[📄](results/bm-20250111-3.14.0a3%2B-22a4421-NOGIL/bm-20250111-linux-x86_64-python-22a442181d5f1ac496da-3.14.0a3%2B-22a4421-vs-3.12.6.md)[📈](results/bm-20250111-3.14.0a3%2B-22a4421-NOGIL/bm-20250111-linux-x86_64-python-22a442181d5f1ac496da-3.14.0a3%2B-22a4421-vs-3.12.6.svg) | 1.201x ↓<br>[📄](results/bm-20250111-3.14.0a3%2B-22a4421-NOGIL/bm-20250111-linux-x86_64-python-22a442181d5f1ac496da-3.14.0a3%2B-22a4421-vs-3.13.0rc2.md)[📈](results/bm-20250111-3.14.0a3%2B-22a4421-NOGIL/bm-20250111-linux-x86_64-python-22a442181d5f1ac496da-3.14.0a3%2B-22a4421-vs-3.13.0rc2.svg) | 1.229x ↓<br>[📄](results/bm-20250111-3.14.0a3%2B-22a4421-NOGIL/bm-20250111-linux-x86_64-python-22a442181d5f1ac496da-3.14.0a3%2B-22a4421-vs-base.md)[📈](results/bm-20250111-3.14.0a3%2B-22a4421-NOGIL/bm-20250111-linux-x86_64-python-22a442181d5f1ac496da-3.14.0a3%2B-22a4421-vs-base.svg)[🧠](results/bm-20250111-3.14.0a3%2B-22a4421-NOGIL/bm-20250111-linux-x86_64-python-22a442181d5f1ac496da-3.14.0a3%2B-22a4421-vs-base-mem.svg) |
| [2025-01-11](results/bm-20250111-3.14.0a3%2B-41ef420-NOGIL) | nascheme/nogil_gc_mark_alive | 41ef420 (NOGIL) | 1.175x ↓<br>[📄](results/bm-20250111-3.14.0a3%2B-41ef420-NOGIL/bm-20250111-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-41ef420-vs-3.12.6.md)[📈](results/bm-20250111-3.14.0a3%2B-41ef420-NOGIL/bm-20250111-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-41ef420-vs-3.12.6.svg) | 1.203x ↓<br>[📄](results/bm-20250111-3.14.0a3%2B-41ef420-NOGIL/bm-20250111-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-41ef420-vs-3.13.0rc2.md)[📈](results/bm-20250111-3.14.0a3%2B-41ef420-NOGIL/bm-20250111-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-41ef420-vs-3.13.0rc2.svg) | 1.049x ↓<br>[📄](results/bm-20250111-3.14.0a3%2B-41ef420-NOGIL/bm-20250111-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-41ef420-vs-base.md)[📈](results/bm-20250111-3.14.0a3%2B-41ef420-NOGIL/bm-20250111-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-41ef420-vs-base.svg)[🧠](results/bm-20250111-3.14.0a3%2B-41ef420-NOGIL/bm-20250111-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-41ef420-vs-base-mem.svg) |
| [2025-01-11](results/bm-20250111-3.14.0a3%2B-553cdc6-NOGIL) | python/553cdc6d6856c1b4539a | 553cdc6 (NOGIL) | 1.138x ↓<br>[📄](results/bm-20250111-3.14.0a3%2B-553cdc6-NOGIL/bm-20250111-linux-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-3.12.6.md)[📈](results/bm-20250111-3.14.0a3%2B-553cdc6-NOGIL/bm-20250111-linux-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-3.12.6.svg) | 1.168x ↓<br>[📄](results/bm-20250111-3.14.0a3%2B-553cdc6-NOGIL/bm-20250111-linux-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-3.13.0rc2.md)[📈](results/bm-20250111-3.14.0a3%2B-553cdc6-NOGIL/bm-20250111-linux-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-3.13.0rc2.svg) | 1.188x ↓<br>[📄](results/bm-20250111-3.14.0a3%2B-553cdc6-NOGIL/bm-20250111-linux-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-base.md)[📈](results/bm-20250111-3.14.0a3%2B-553cdc6-NOGIL/bm-20250111-linux-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-base.svg)[🧠](results/bm-20250111-3.14.0a3%2B-553cdc6-NOGIL/bm-20250111-linux-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-base-mem.svg) |
| [2025-01-11](results/bm-20250111-3.14.0a3%2B-553cdc6) | python/553cdc6d6856c1b4539a | 553cdc6 | 1.071x ↑<br>[📄](results/bm-20250111-3.14.0a3%2B-553cdc6/bm-20250111-linux-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-3.12.6.md)[📈](results/bm-20250111-3.14.0a3%2B-553cdc6/bm-20250111-linux-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-3.12.6.svg) | 1.034x ↑<br>[📄](results/bm-20250111-3.14.0a3%2B-553cdc6/bm-20250111-linux-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-3.13.0rc2.md)[📈](results/bm-20250111-3.14.0a3%2B-553cdc6/bm-20250111-linux-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-3.13.0rc2.svg) |  |
| [2025-01-09](results/bm-20250109-3.14.0a3%2B-7dc41ad-NOGIL) | python/7dc41ad6a7826ffc675f | 7dc41ad (NOGIL) | 1.151x ↓<br>[📄](results/bm-20250109-3.14.0a3%2B-7dc41ad-NOGIL/bm-20250109-linux-x86_64-python-7dc41ad6a7826ffc675f-3.14.0a3%2B-7dc41ad-vs-3.12.6.md)[📈](results/bm-20250109-3.14.0a3%2B-7dc41ad-NOGIL/bm-20250109-linux-x86_64-python-7dc41ad6a7826ffc675f-3.14.0a3%2B-7dc41ad-vs-3.12.6.svg) | 1.181x ↓<br>[📄](results/bm-20250109-3.14.0a3%2B-7dc41ad-NOGIL/bm-20250109-linux-x86_64-python-7dc41ad6a7826ffc675f-3.14.0a3%2B-7dc41ad-vs-3.13.0rc2.md)[📈](results/bm-20250109-3.14.0a3%2B-7dc41ad-NOGIL/bm-20250109-linux-x86_64-python-7dc41ad6a7826ffc675f-3.14.0a3%2B-7dc41ad-vs-3.13.0rc2.svg) |  |

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-01-13](results/bm-20250113-3.14.0a3%2B-b70a567-NOGIL) | python/b70a567575db37846bee | b70a567 (NOGIL) | 1.161x ↓<br>[📄](results/bm-20250113-3.14.0a3%2B-b70a567-NOGIL/bm-20250113-vultr-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-3.12.6.md)[📈](results/bm-20250113-3.14.0a3%2B-b70a567-NOGIL/bm-20250113-vultr-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-3.12.6.svg) | 1.188x ↓<br>[📄](results/bm-20250113-3.14.0a3%2B-b70a567-NOGIL/bm-20250113-vultr-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-3.13.0rc2.md)[📈](results/bm-20250113-3.14.0a3%2B-b70a567-NOGIL/bm-20250113-vultr-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-3.13.0rc2.svg) | 1.231x ↓<br>[📄](results/bm-20250113-3.14.0a3%2B-b70a567-NOGIL/bm-20250113-vultr-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-base.md)[📈](results/bm-20250113-3.14.0a3%2B-b70a567-NOGIL/bm-20250113-vultr-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-base.svg)[🧠](results/bm-20250113-3.14.0a3%2B-b70a567-NOGIL/bm-20250113-vultr-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-base-mem.svg) |
| [2025-01-13](results/bm-20250113-3.14.0a3%2B-b70a567) | python/b70a567575db37846bee | b70a567 | 1.098x ↑<br>[📄](results/bm-20250113-3.14.0a3%2B-b70a567/bm-20250113-vultr-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-3.12.6.md)[📈](results/bm-20250113-3.14.0a3%2B-b70a567/bm-20250113-vultr-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-3.12.6.svg) | 1.060x ↑<br>[📄](results/bm-20250113-3.14.0a3%2B-b70a567/bm-20250113-vultr-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-3.13.0rc2.md)[📈](results/bm-20250113-3.14.0a3%2B-b70a567/bm-20250113-vultr-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-3.13.0rc2.svg) |  |
| [2025-01-13](results/bm-20250113-3.14.0a3%2B-0c173c9-NOGIL) | nascheme/nogil_gc_mark_alive | 0c173c9 (NOGIL) | 1.160x ↓<br>[📄](results/bm-20250113-3.14.0a3%2B-0c173c9-NOGIL/bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-0c173c9-vs-3.12.6.md)[📈](results/bm-20250113-3.14.0a3%2B-0c173c9-NOGIL/bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-0c173c9-vs-3.12.6.svg) | 1.187x ↓<br>[📄](results/bm-20250113-3.14.0a3%2B-0c173c9-NOGIL/bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-0c173c9-vs-3.13.0rc2.md)[📈](results/bm-20250113-3.14.0a3%2B-0c173c9-NOGIL/bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-0c173c9-vs-3.13.0rc2.svg) | 1.000x ↑<br>[📄](results/bm-20250113-3.14.0a3%2B-0c173c9-NOGIL/bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-0c173c9-vs-base.md)[📈](results/bm-20250113-3.14.0a3%2B-0c173c9-NOGIL/bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-0c173c9-vs-base.svg)[🧠](results/bm-20250113-3.14.0a3%2B-0c173c9-NOGIL/bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-0c173c9-vs-base-mem.svg) |
| [2025-01-13](results/bm-20250113-3.14.0a3%2B-1433cd3-NOGIL) | Yhg1s/for_iter_spec | 1433cd3 (NOGIL) | 1.161x ↓<br>[📄](results/bm-20250113-3.14.0a3%2B-1433cd3-NOGIL/bm-20250113-vultr-x86_64-Yhg1s-for_iter_spec-3.14.0a3%2B-1433cd3-vs-3.12.6.md)[📈](results/bm-20250113-3.14.0a3%2B-1433cd3-NOGIL/bm-20250113-vultr-x86_64-Yhg1s-for_iter_spec-3.14.0a3%2B-1433cd3-vs-3.12.6.svg) | 1.188x ↓<br>[📄](results/bm-20250113-3.14.0a3%2B-1433cd3-NOGIL/bm-20250113-vultr-x86_64-Yhg1s-for_iter_spec-3.14.0a3%2B-1433cd3-vs-3.13.0rc2.md)[📈](results/bm-20250113-3.14.0a3%2B-1433cd3-NOGIL/bm-20250113-vultr-x86_64-Yhg1s-for_iter_spec-3.14.0a3%2B-1433cd3-vs-3.13.0rc2.svg) | 1.004x ↑<br>[📄](results/bm-20250113-3.14.0a3%2B-1433cd3-NOGIL/bm-20250113-vultr-x86_64-Yhg1s-for_iter_spec-3.14.0a3%2B-1433cd3-vs-base.md)[📈](results/bm-20250113-3.14.0a3%2B-1433cd3-NOGIL/bm-20250113-vultr-x86_64-Yhg1s-for_iter_spec-3.14.0a3%2B-1433cd3-vs-base.svg)[🧠](results/bm-20250113-3.14.0a3%2B-1433cd3-NOGIL/bm-20250113-vultr-x86_64-Yhg1s-for_iter_spec-3.14.0a3%2B-1433cd3-vs-base-mem.svg) |
| [2025-01-13](results/bm-20250113-3.14.0a3%2B-d0ecbdd-NOGIL) | python/d0ecbdd838034c1f061e | d0ecbdd (NOGIL) | 1.162x ↓<br>[📄](results/bm-20250113-3.14.0a3%2B-d0ecbdd-NOGIL/bm-20250113-vultr-x86_64-python-d0ecbdd838034c1f061e-3.14.0a3%2B-d0ecbdd-vs-3.12.6.md)[📈](results/bm-20250113-3.14.0a3%2B-d0ecbdd-NOGIL/bm-20250113-vultr-x86_64-python-d0ecbdd838034c1f061e-3.14.0a3%2B-d0ecbdd-vs-3.12.6.svg) | 1.189x ↓<br>[📄](results/bm-20250113-3.14.0a3%2B-d0ecbdd-NOGIL/bm-20250113-vultr-x86_64-python-d0ecbdd838034c1f061e-3.14.0a3%2B-d0ecbdd-vs-3.13.0rc2.md)[📈](results/bm-20250113-3.14.0a3%2B-d0ecbdd-NOGIL/bm-20250113-vultr-x86_64-python-d0ecbdd838034c1f061e-3.14.0a3%2B-d0ecbdd-vs-3.13.0rc2.svg) | 1.233x ↓<br>[📄](results/bm-20250113-3.14.0a3%2B-d0ecbdd-NOGIL/bm-20250113-vultr-x86_64-python-d0ecbdd838034c1f061e-3.14.0a3%2B-d0ecbdd-vs-base.md)[📈](results/bm-20250113-3.14.0a3%2B-d0ecbdd-NOGIL/bm-20250113-vultr-x86_64-python-d0ecbdd838034c1f061e-3.14.0a3%2B-d0ecbdd-vs-base.svg)[🧠](results/bm-20250113-3.14.0a3%2B-d0ecbdd-NOGIL/bm-20250113-vultr-x86_64-python-d0ecbdd838034c1f061e-3.14.0a3%2B-d0ecbdd-vs-base-mem.svg) |
| [2025-01-13](results/bm-20250113-3.14.0a3%2B-d0ecbdd) | python/d0ecbdd838034c1f061e | d0ecbdd | 1.100x ↑<br>[📄](results/bm-20250113-3.14.0a3%2B-d0ecbdd/bm-20250113-vultr-x86_64-python-d0ecbdd838034c1f061e-3.14.0a3%2B-d0ecbdd-vs-3.12.6.md)[📈](results/bm-20250113-3.14.0a3%2B-d0ecbdd/bm-20250113-vultr-x86_64-python-d0ecbdd838034c1f061e-3.14.0a3%2B-d0ecbdd-vs-3.12.6.svg) | 1.061x ↑<br>[📄](results/bm-20250113-3.14.0a3%2B-d0ecbdd/bm-20250113-vultr-x86_64-python-d0ecbdd838034c1f061e-3.14.0a3%2B-d0ecbdd-vs-3.13.0rc2.md)[📈](results/bm-20250113-3.14.0a3%2B-d0ecbdd/bm-20250113-vultr-x86_64-python-d0ecbdd838034c1f061e-3.14.0a3%2B-d0ecbdd-vs-3.13.0rc2.svg) |  |
| [2025-01-11](results/bm-20250111-3.14.0a3%2B-22a4421) | python/22a442181d5f1ac496da | 22a4421 | 1.099x ↑<br>[📄](results/bm-20250111-3.14.0a3%2B-22a4421/bm-20250111-vultr-x86_64-python-22a442181d5f1ac496da-3.14.0a3%2B-22a4421-vs-3.12.6.md)[📈](results/bm-20250111-3.14.0a3%2B-22a4421/bm-20250111-vultr-x86_64-python-22a442181d5f1ac496da-3.14.0a3%2B-22a4421-vs-3.12.6.svg) | 1.060x ↑<br>[📄](results/bm-20250111-3.14.0a3%2B-22a4421/bm-20250111-vultr-x86_64-python-22a442181d5f1ac496da-3.14.0a3%2B-22a4421-vs-3.13.0rc2.md)[📈](results/bm-20250111-3.14.0a3%2B-22a4421/bm-20250111-vultr-x86_64-python-22a442181d5f1ac496da-3.14.0a3%2B-22a4421-vs-3.13.0rc2.svg) |  |
| [2025-01-11](results/bm-20250111-3.14.0a3%2B-22a4421-NOGIL) | python/22a442181d5f1ac496da | 22a4421 (NOGIL) | 1.157x ↓<br>[📄](results/bm-20250111-3.14.0a3%2B-22a4421-NOGIL/bm-20250111-vultr-x86_64-python-22a442181d5f1ac496da-3.14.0a3%2B-22a4421-vs-3.12.6.md)[📈](results/bm-20250111-3.14.0a3%2B-22a4421-NOGIL/bm-20250111-vultr-x86_64-python-22a442181d5f1ac496da-3.14.0a3%2B-22a4421-vs-3.12.6.svg) | 1.184x ↓<br>[📄](results/bm-20250111-3.14.0a3%2B-22a4421-NOGIL/bm-20250111-vultr-x86_64-python-22a442181d5f1ac496da-3.14.0a3%2B-22a4421-vs-3.13.0rc2.md)[📈](results/bm-20250111-3.14.0a3%2B-22a4421-NOGIL/bm-20250111-vultr-x86_64-python-22a442181d5f1ac496da-3.14.0a3%2B-22a4421-vs-3.13.0rc2.svg) | 1.228x ↓<br>[📄](results/bm-20250111-3.14.0a3%2B-22a4421-NOGIL/bm-20250111-vultr-x86_64-python-22a442181d5f1ac496da-3.14.0a3%2B-22a4421-vs-base.md)[📈](results/bm-20250111-3.14.0a3%2B-22a4421-NOGIL/bm-20250111-vultr-x86_64-python-22a442181d5f1ac496da-3.14.0a3%2B-22a4421-vs-base.svg)[🧠](results/bm-20250111-3.14.0a3%2B-22a4421-NOGIL/bm-20250111-vultr-x86_64-python-22a442181d5f1ac496da-3.14.0a3%2B-22a4421-vs-base-mem.svg) |
| [2025-01-11](results/bm-20250111-3.14.0a3%2B-41ef420-NOGIL) | nascheme/nogil_gc_mark_alive | 41ef420 (NOGIL) | 1.151x ↓<br>[📄](results/bm-20250111-3.14.0a3%2B-41ef420-NOGIL/bm-20250111-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-41ef420-vs-3.12.6.md)[📈](results/bm-20250111-3.14.0a3%2B-41ef420-NOGIL/bm-20250111-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-41ef420-vs-3.12.6.svg) | 1.178x ↓<br>[📄](results/bm-20250111-3.14.0a3%2B-41ef420-NOGIL/bm-20250111-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-41ef420-vs-3.13.0rc2.md)[📈](results/bm-20250111-3.14.0a3%2B-41ef420-NOGIL/bm-20250111-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-41ef420-vs-3.13.0rc2.svg) | 1.009x ↑<br>[📄](results/bm-20250111-3.14.0a3%2B-41ef420-NOGIL/bm-20250111-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-41ef420-vs-base.md)[📈](results/bm-20250111-3.14.0a3%2B-41ef420-NOGIL/bm-20250111-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-41ef420-vs-base.svg)[🧠](results/bm-20250111-3.14.0a3%2B-41ef420-NOGIL/bm-20250111-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-41ef420-vs-base-mem.svg) |
| [2025-01-11](results/bm-20250111-3.14.0a3%2B-553cdc6-NOGIL) | python/553cdc6d6856c1b4539a | 553cdc6 (NOGIL) | 1.162x ↓<br>[📄](results/bm-20250111-3.14.0a3%2B-553cdc6-NOGIL/bm-20250111-vultr-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-3.12.6.md)[📈](results/bm-20250111-3.14.0a3%2B-553cdc6-NOGIL/bm-20250111-vultr-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-3.12.6.svg) | 1.189x ↓<br>[📄](results/bm-20250111-3.14.0a3%2B-553cdc6-NOGIL/bm-20250111-vultr-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-3.13.0rc2.md)[📈](results/bm-20250111-3.14.0a3%2B-553cdc6-NOGIL/bm-20250111-vultr-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-3.13.0rc2.svg) | 1.003x ↓<br>[📄](results/bm-20250111-3.14.0a3%2B-553cdc6-NOGIL/bm-20250111-vultr-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-base.md)[📈](results/bm-20250111-3.14.0a3%2B-553cdc6-NOGIL/bm-20250111-vultr-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-base.svg)[🧠](results/bm-20250111-3.14.0a3%2B-553cdc6-NOGIL/bm-20250111-vultr-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-base-mem.svg) |
| [2025-01-11](results/bm-20250111-3.14.0a3%2B-553cdc6) | python/553cdc6d6856c1b4539a | 553cdc6 | 1.101x ↑<br>[📄](results/bm-20250111-3.14.0a3%2B-553cdc6/bm-20250111-vultr-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-3.12.6.md)[📈](results/bm-20250111-3.14.0a3%2B-553cdc6/bm-20250111-vultr-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-3.12.6.svg) | 1.062x ↑<br>[📄](results/bm-20250111-3.14.0a3%2B-553cdc6/bm-20250111-vultr-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-3.13.0rc2.md)[📈](results/bm-20250111-3.14.0a3%2B-553cdc6/bm-20250111-vultr-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-3.13.0rc2.svg) | 1.001x ↑<br>[📄](results/bm-20250111-3.14.0a3%2B-553cdc6/bm-20250111-vultr-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-base.md)[📈](results/bm-20250111-3.14.0a3%2B-553cdc6/bm-20250111-vultr-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-base.svg)[🧠](results/bm-20250111-3.14.0a3%2B-553cdc6/bm-20250111-vultr-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-base-mem.svg) |
| [2025-01-10](results/bm-20250110-3.14.0a3%2B-7ab3ec6) | mpage/gh_115999_load_attr_ | 7ab3ec6 | 1.101x ↑<br>[📄](results/bm-20250110-3.14.0a3%2B-7ab3ec6/bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3%2B-7ab3ec6-vs-3.12.6.md)[📈](results/bm-20250110-3.14.0a3%2B-7ab3ec6/bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3%2B-7ab3ec6-vs-3.12.6.svg) | 1.062x ↑<br>[📄](results/bm-20250110-3.14.0a3%2B-7ab3ec6/bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3%2B-7ab3ec6-vs-3.13.0rc2.md)[📈](results/bm-20250110-3.14.0a3%2B-7ab3ec6/bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3%2B-7ab3ec6-vs-3.13.0rc2.svg) | 1.000x ↑<br>[📄](results/bm-20250110-3.14.0a3%2B-7ab3ec6/bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3%2B-7ab3ec6-vs-base.md)[📈](results/bm-20250110-3.14.0a3%2B-7ab3ec6/bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3%2B-7ab3ec6-vs-base.svg)[🧠](results/bm-20250110-3.14.0a3%2B-7ab3ec6/bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3%2B-7ab3ec6-vs-base-mem.svg) |
| [2025-01-10](results/bm-20250110-3.14.0a3%2B-1b39b50) | python/1b39b502d33c68f52fd7 | 1b39b50 | 1.100x ↑<br>[📄](results/bm-20250110-3.14.0a3%2B-1b39b50/bm-20250110-vultr-x86_64-python-1b39b502d33c68f52fd7-3.14.0a3%2B-1b39b50-vs-3.12.6.md)[📈](results/bm-20250110-3.14.0a3%2B-1b39b50/bm-20250110-vultr-x86_64-python-1b39b502d33c68f52fd7-3.14.0a3%2B-1b39b50-vs-3.12.6.svg) | 1.061x ↑<br>[📄](results/bm-20250110-3.14.0a3%2B-1b39b50/bm-20250110-vultr-x86_64-python-1b39b502d33c68f52fd7-3.14.0a3%2B-1b39b50-vs-3.13.0rc2.md)[📈](results/bm-20250110-3.14.0a3%2B-1b39b50/bm-20250110-vultr-x86_64-python-1b39b502d33c68f52fd7-3.14.0a3%2B-1b39b50-vs-3.13.0rc2.svg) |  |
| [2025-01-09](results/bm-20250109-3.14.0a3%2B-7dc41ad-NOGIL) | python/7dc41ad6a7826ffc675f | 7dc41ad (NOGIL) | 1.165x ↓<br>[📄](results/bm-20250109-3.14.0a3%2B-7dc41ad-NOGIL/bm-20250109-vultr-x86_64-python-7dc41ad6a7826ffc675f-3.14.0a3%2B-7dc41ad-vs-3.12.6.md)[📈](results/bm-20250109-3.14.0a3%2B-7dc41ad-NOGIL/bm-20250109-vultr-x86_64-python-7dc41ad6a7826ffc675f-3.14.0a3%2B-7dc41ad-vs-3.12.6.svg) | 1.192x ↓<br>[📄](results/bm-20250109-3.14.0a3%2B-7dc41ad-NOGIL/bm-20250109-vultr-x86_64-python-7dc41ad6a7826ffc675f-3.14.0a3%2B-7dc41ad-vs-3.13.0rc2.md)[📈](results/bm-20250109-3.14.0a3%2B-7dc41ad-NOGIL/bm-20250109-vultr-x86_64-python-7dc41ad6a7826ffc675f-3.14.0a3%2B-7dc41ad-vs-3.13.0rc2.svg) | 1.000x ↓<br>[📄](results/bm-20250109-3.14.0a3%2B-7dc41ad-NOGIL/bm-20250109-vultr-x86_64-python-7dc41ad6a7826ffc675f-3.14.0a3%2B-7dc41ad-vs-base.md)[📈](results/bm-20250109-3.14.0a3%2B-7dc41ad-NOGIL/bm-20250109-vultr-x86_64-python-7dc41ad6a7826ffc675f-3.14.0a3%2B-7dc41ad-vs-base.svg)[🧠](results/bm-20250109-3.14.0a3%2B-7dc41ad-NOGIL/bm-20250109-vultr-x86_64-python-7dc41ad6a7826ffc675f-3.14.0a3%2B-7dc41ad-vs-base-mem.svg) |
| [2025-01-09](results/bm-20250109-3.14.0a3%2B-f509a13-NOGIL) | nascheme/nogil_gc_mark_alive | f509a13 (NOGIL) | 1.157x ↓<br>[📄](results/bm-20250109-3.14.0a3%2B-f509a13-NOGIL/bm-20250109-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-f509a13-vs-3.12.6.md)[📈](results/bm-20250109-3.14.0a3%2B-f509a13-NOGIL/bm-20250109-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-f509a13-vs-3.12.6.svg) | 1.184x ↓<br>[📄](results/bm-20250109-3.14.0a3%2B-f509a13-NOGIL/bm-20250109-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-f509a13-vs-3.13.0rc2.md)[📈](results/bm-20250109-3.14.0a3%2B-f509a13-NOGIL/bm-20250109-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-f509a13-vs-3.13.0rc2.svg) | 1.002x ↑<br>[📄](results/bm-20250109-3.14.0a3%2B-f509a13-NOGIL/bm-20250109-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-f509a13-vs-base.md)[📈](results/bm-20250109-3.14.0a3%2B-f509a13-NOGIL/bm-20250109-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-f509a13-vs-base.svg)[🧠](results/bm-20250109-3.14.0a3%2B-f509a13-NOGIL/bm-20250109-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-f509a13-vs-base-mem.svg) |


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
