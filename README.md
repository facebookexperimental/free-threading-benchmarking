# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
[Most recent pystats on main (0cafa97)](results/bm-20250104-3.14.0a3%2B-0cafa97-PYTHON_UOPS/bm-20250104-vultr-x86_64-python-0cafa97932c6574734bb-3.14.0a3%2B-0cafa97-pystats.md)

## linux x86_64 (linux)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-01-09](results/bm-20250109-3.14.0a3%2B-7263d1e-NOGIL) | Yhg1s/list_realloc | 7263d1e (NOGIL) | 1.179x ↓<br>[📄](results/bm-20250109-3.14.0a3%2B-7263d1e-NOGIL/bm-20250109-linux-x86_64-Yhg1s-list_realloc-3.14.0a3%2B-7263d1e-vs-3.12.6.md)[📈](results/bm-20250109-3.14.0a3%2B-7263d1e-NOGIL/bm-20250109-linux-x86_64-Yhg1s-list_realloc-3.14.0a3%2B-7263d1e-vs-3.12.6.svg) | 1.206x ↓<br>[📄](results/bm-20250109-3.14.0a3%2B-7263d1e-NOGIL/bm-20250109-linux-x86_64-Yhg1s-list_realloc-3.14.0a3%2B-7263d1e-vs-3.13.0rc2.md)[📈](results/bm-20250109-3.14.0a3%2B-7263d1e-NOGIL/bm-20250109-linux-x86_64-Yhg1s-list_realloc-3.14.0a3%2B-7263d1e-vs-3.13.0rc2.svg) |  |
| [2025-01-08](results/bm-20250108-3.14.0a3%2B-a1284e9) | python/a1284e97979ff73ad72a | a1284e9 | 1.098x ↑<br>[📄](results/bm-20250108-3.14.0a3%2B-a1284e9/bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3%2B-a1284e9-vs-3.12.6.md)[📈](results/bm-20250108-3.14.0a3%2B-a1284e9/bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3%2B-a1284e9-vs-3.12.6.svg) | 1.055x ↑<br>[📄](results/bm-20250108-3.14.0a3%2B-a1284e9/bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3%2B-a1284e9-vs-3.13.0rc2.md)[📈](results/bm-20250108-3.14.0a3%2B-a1284e9/bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3%2B-a1284e9-vs-3.13.0rc2.svg) |  |
| [2025-01-08](results/bm-20250108-3.14.0a3%2B-a1284e9-NOGIL) | python/a1284e97979ff73ad72a | a1284e9 (NOGIL) | 1.130x ↓<br>[📄](results/bm-20250108-3.14.0a3%2B-a1284e9-NOGIL/bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3%2B-a1284e9-vs-3.12.6.md)[📈](results/bm-20250108-3.14.0a3%2B-a1284e9-NOGIL/bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3%2B-a1284e9-vs-3.12.6.svg) | 1.160x ↓<br>[📄](results/bm-20250108-3.14.0a3%2B-a1284e9-NOGIL/bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3%2B-a1284e9-vs-3.13.0rc2.md)[📈](results/bm-20250108-3.14.0a3%2B-a1284e9-NOGIL/bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3%2B-a1284e9-vs-3.13.0rc2.svg) | 1.202x ↓<br>[📄](results/bm-20250108-3.14.0a3%2B-a1284e9-NOGIL/bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3%2B-a1284e9-vs-base.md)[📈](results/bm-20250108-3.14.0a3%2B-a1284e9-NOGIL/bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3%2B-a1284e9-vs-base.svg)[🧠](results/bm-20250108-3.14.0a3%2B-a1284e9-NOGIL/bm-20250108-linux-x86_64-python-a1284e97979ff73ad72a-3.14.0a3%2B-a1284e9-vs-base-mem.svg) |
| [2025-01-08](results/bm-20250108-3.14.0a3%2B-a111bff-NOGIL) | nascheme/nogil_gc_mark_alive | a111bff (NOGIL) | 1.120x ↓<br>[📄](results/bm-20250108-3.14.0a3%2B-a111bff-NOGIL/bm-20250108-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-a111bff-vs-3.12.6.md)[📈](results/bm-20250108-3.14.0a3%2B-a111bff-NOGIL/bm-20250108-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-a111bff-vs-3.12.6.svg) | 1.150x ↓<br>[📄](results/bm-20250108-3.14.0a3%2B-a111bff-NOGIL/bm-20250108-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-a111bff-vs-3.13.0rc2.md)[📈](results/bm-20250108-3.14.0a3%2B-a111bff-NOGIL/bm-20250108-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-a111bff-vs-3.13.0rc2.svg) | 1.017x ↑<br>[📄](results/bm-20250108-3.14.0a3%2B-a111bff-NOGIL/bm-20250108-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-a111bff-vs-base.md)[📈](results/bm-20250108-3.14.0a3%2B-a111bff-NOGIL/bm-20250108-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-a111bff-vs-base.svg)[🧠](results/bm-20250108-3.14.0a3%2B-a111bff-NOGIL/bm-20250108-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-a111bff-vs-base-mem.svg) |
| [2025-01-07](results/bm-20250107-3.14.0a3%2B-e08b282) | python/e08b28235a863323ca3a | e08b282 | 1.101x ↑<br>[📄](results/bm-20250107-3.14.0a3%2B-e08b282/bm-20250107-linux-x86_64-python-e08b28235a863323ca3a-3.14.0a3%2B-e08b282-vs-3.12.6.md)[📈](results/bm-20250107-3.14.0a3%2B-e08b282/bm-20250107-linux-x86_64-python-e08b28235a863323ca3a-3.14.0a3%2B-e08b282-vs-3.12.6.svg) | 1.059x ↑<br>[📄](results/bm-20250107-3.14.0a3%2B-e08b282/bm-20250107-linux-x86_64-python-e08b28235a863323ca3a-3.14.0a3%2B-e08b282-vs-3.13.0rc2.md)[📈](results/bm-20250107-3.14.0a3%2B-e08b282/bm-20250107-linux-x86_64-python-e08b28235a863323ca3a-3.14.0a3%2B-e08b282-vs-3.13.0rc2.svg) |  |
| [2025-01-07](results/bm-20250107-3.14.0a3%2B-e08b282-NOGIL) | python/e08b28235a863323ca3a | e08b282 (NOGIL) | 1.124x ↓<br>[📄](results/bm-20250107-3.14.0a3%2B-e08b282-NOGIL/bm-20250107-linux-x86_64-python-e08b28235a863323ca3a-3.14.0a3%2B-e08b282-vs-3.12.6.md)[📈](results/bm-20250107-3.14.0a3%2B-e08b282-NOGIL/bm-20250107-linux-x86_64-python-e08b28235a863323ca3a-3.14.0a3%2B-e08b282-vs-3.12.6.svg) | 1.155x ↓<br>[📄](results/bm-20250107-3.14.0a3%2B-e08b282-NOGIL/bm-20250107-linux-x86_64-python-e08b28235a863323ca3a-3.14.0a3%2B-e08b282-vs-3.13.0rc2.md)[📈](results/bm-20250107-3.14.0a3%2B-e08b282-NOGIL/bm-20250107-linux-x86_64-python-e08b28235a863323ca3a-3.14.0a3%2B-e08b282-vs-3.13.0rc2.svg) | 1.200x ↓<br>[📄](results/bm-20250107-3.14.0a3%2B-e08b282-NOGIL/bm-20250107-linux-x86_64-python-e08b28235a863323ca3a-3.14.0a3%2B-e08b282-vs-base.md)[📈](results/bm-20250107-3.14.0a3%2B-e08b282-NOGIL/bm-20250107-linux-x86_64-python-e08b28235a863323ca3a-3.14.0a3%2B-e08b282-vs-base.svg)[🧠](results/bm-20250107-3.14.0a3%2B-e08b282-NOGIL/bm-20250107-linux-x86_64-python-e08b28235a863323ca3a-3.14.0a3%2B-e08b282-vs-base-mem.svg) |
| [2025-01-07](results/bm-20250107-3.14.0a3%2B-953b49e-NOGIL) | python/953b49e5468d02afadda | 953b49e (NOGIL) | 1.109x ↓<br>[📄](results/bm-20250107-3.14.0a3%2B-953b49e-NOGIL/bm-20250107-linux-x86_64-python-953b49e5468d02afadda-3.14.0a3%2B-953b49e-vs-3.12.6.md)[📈](results/bm-20250107-3.14.0a3%2B-953b49e-NOGIL/bm-20250107-linux-x86_64-python-953b49e5468d02afadda-3.14.0a3%2B-953b49e-vs-3.12.6.svg) | 1.140x ↓<br>[📄](results/bm-20250107-3.14.0a3%2B-953b49e-NOGIL/bm-20250107-linux-x86_64-python-953b49e5468d02afadda-3.14.0a3%2B-953b49e-vs-3.13.0rc2.md)[📈](results/bm-20250107-3.14.0a3%2B-953b49e-NOGIL/bm-20250107-linux-x86_64-python-953b49e5468d02afadda-3.14.0a3%2B-953b49e-vs-3.13.0rc2.svg) | 1.208x ↓<br>[📄](results/bm-20250107-3.14.0a3%2B-953b49e-NOGIL/bm-20250107-linux-x86_64-python-953b49e5468d02afadda-3.14.0a3%2B-953b49e-vs-base.md)[📈](results/bm-20250107-3.14.0a3%2B-953b49e-NOGIL/bm-20250107-linux-x86_64-python-953b49e5468d02afadda-3.14.0a3%2B-953b49e-vs-base.svg)[🧠](results/bm-20250107-3.14.0a3%2B-953b49e-NOGIL/bm-20250107-linux-x86_64-python-953b49e5468d02afadda-3.14.0a3%2B-953b49e-vs-base-mem.svg) |
| [2025-01-07](results/bm-20250107-3.14.0a3%2B-953b49e) | python/953b49e5468d02afadda | 953b49e | 1.131x ↑<br>[📄](results/bm-20250107-3.14.0a3%2B-953b49e/bm-20250107-linux-x86_64-python-953b49e5468d02afadda-3.14.0a3%2B-953b49e-vs-3.12.6.md)[📈](results/bm-20250107-3.14.0a3%2B-953b49e/bm-20250107-linux-x86_64-python-953b49e5468d02afadda-3.14.0a3%2B-953b49e-vs-3.12.6.svg) | 1.087x ↑<br>[📄](results/bm-20250107-3.14.0a3%2B-953b49e/bm-20250107-linux-x86_64-python-953b49e5468d02afadda-3.14.0a3%2B-953b49e-vs-3.13.0rc2.md)[📈](results/bm-20250107-3.14.0a3%2B-953b49e/bm-20250107-linux-x86_64-python-953b49e5468d02afadda-3.14.0a3%2B-953b49e-vs-3.13.0rc2.svg) |  |
| [2025-01-05](results/bm-20250105-3.14.0a3%2B-3b231be) | python/3b231be8f000ae59faa0 | 3b231be | 1.125x ↑<br>[📄](results/bm-20250105-3.14.0a3%2B-3b231be/bm-20250105-linux-x86_64-python-3b231be8f000ae59faa0-3.14.0a3%2B-3b231be-vs-3.12.6.md)[📈](results/bm-20250105-3.14.0a3%2B-3b231be/bm-20250105-linux-x86_64-python-3b231be8f000ae59faa0-3.14.0a3%2B-3b231be-vs-3.12.6.svg) | 1.083x ↑<br>[📄](results/bm-20250105-3.14.0a3%2B-3b231be/bm-20250105-linux-x86_64-python-3b231be8f000ae59faa0-3.14.0a3%2B-3b231be-vs-3.13.0rc2.md)[📈](results/bm-20250105-3.14.0a3%2B-3b231be/bm-20250105-linux-x86_64-python-3b231be8f000ae59faa0-3.14.0a3%2B-3b231be-vs-3.13.0rc2.svg) |  |
| [2025-01-05](results/bm-20250105-3.14.0a3%2B-3b231be-NOGIL) | python/3b231be8f000ae59faa0 | 3b231be (NOGIL) | 1.123x ↓<br>[📄](results/bm-20250105-3.14.0a3%2B-3b231be-NOGIL/bm-20250105-linux-x86_64-python-3b231be8f000ae59faa0-3.14.0a3%2B-3b231be-vs-3.12.6.md)[📈](results/bm-20250105-3.14.0a3%2B-3b231be-NOGIL/bm-20250105-linux-x86_64-python-3b231be8f000ae59faa0-3.14.0a3%2B-3b231be-vs-3.12.6.svg) | 1.153x ↓<br>[📄](results/bm-20250105-3.14.0a3%2B-3b231be-NOGIL/bm-20250105-linux-x86_64-python-3b231be8f000ae59faa0-3.14.0a3%2B-3b231be-vs-3.13.0rc2.md)[📈](results/bm-20250105-3.14.0a3%2B-3b231be-NOGIL/bm-20250105-linux-x86_64-python-3b231be8f000ae59faa0-3.14.0a3%2B-3b231be-vs-3.13.0rc2.svg) | 1.214x ↓<br>[📄](results/bm-20250105-3.14.0a3%2B-3b231be-NOGIL/bm-20250105-linux-x86_64-python-3b231be8f000ae59faa0-3.14.0a3%2B-3b231be-vs-base.md)[📈](results/bm-20250105-3.14.0a3%2B-3b231be-NOGIL/bm-20250105-linux-x86_64-python-3b231be8f000ae59faa0-3.14.0a3%2B-3b231be-vs-base.svg)[🧠](results/bm-20250105-3.14.0a3%2B-3b231be-NOGIL/bm-20250105-linux-x86_64-python-3b231be8f000ae59faa0-3.14.0a3%2B-3b231be-vs-base-mem.svg) |

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-01-08](results/bm-20250108-3.14.0a3%2B-a1284e9-NOGIL) | python/a1284e97979ff73ad72a | a1284e9 (NOGIL) | 1.159x ↓<br>[📄](results/bm-20250108-3.14.0a3%2B-a1284e9-NOGIL/bm-20250108-vultr-x86_64-python-a1284e97979ff73ad72a-3.14.0a3%2B-a1284e9-vs-3.12.6.md)[📈](results/bm-20250108-3.14.0a3%2B-a1284e9-NOGIL/bm-20250108-vultr-x86_64-python-a1284e97979ff73ad72a-3.14.0a3%2B-a1284e9-vs-3.12.6.svg) | 1.186x ↓<br>[📄](results/bm-20250108-3.14.0a3%2B-a1284e9-NOGIL/bm-20250108-vultr-x86_64-python-a1284e97979ff73ad72a-3.14.0a3%2B-a1284e9-vs-3.13.0rc2.md)[📈](results/bm-20250108-3.14.0a3%2B-a1284e9-NOGIL/bm-20250108-vultr-x86_64-python-a1284e97979ff73ad72a-3.14.0a3%2B-a1284e9-vs-3.13.0rc2.svg) |  |
| [2025-01-08](results/bm-20250108-3.14.0a3%2B-a111bff-NOGIL) | nascheme/nogil_gc_mark_alive | a111bff (NOGIL) | 1.161x ↓<br>[📄](results/bm-20250108-3.14.0a3%2B-a111bff-NOGIL/bm-20250108-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-a111bff-vs-3.12.6.md)[📈](results/bm-20250108-3.14.0a3%2B-a111bff-NOGIL/bm-20250108-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-a111bff-vs-3.12.6.svg) | 1.188x ↓<br>[📄](results/bm-20250108-3.14.0a3%2B-a111bff-NOGIL/bm-20250108-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-a111bff-vs-3.13.0rc2.md)[📈](results/bm-20250108-3.14.0a3%2B-a111bff-NOGIL/bm-20250108-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-a111bff-vs-3.13.0rc2.svg) | 1.002x ↓<br>[📄](results/bm-20250108-3.14.0a3%2B-a111bff-NOGIL/bm-20250108-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-a111bff-vs-base.md)[📈](results/bm-20250108-3.14.0a3%2B-a111bff-NOGIL/bm-20250108-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-a111bff-vs-base.svg)[🧠](results/bm-20250108-3.14.0a3%2B-a111bff-NOGIL/bm-20250108-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-a111bff-vs-base-mem.svg) |
| [2025-01-07](results/bm-20250107-3.14.0a3%2B-e08b282) | python/e08b28235a863323ca3a | e08b282 | 1.102x ↑<br>[📄](results/bm-20250107-3.14.0a3%2B-e08b282/bm-20250107-vultr-x86_64-python-e08b28235a863323ca3a-3.14.0a3%2B-e08b282-vs-3.12.6.md)[📈](results/bm-20250107-3.14.0a3%2B-e08b282/bm-20250107-vultr-x86_64-python-e08b28235a863323ca3a-3.14.0a3%2B-e08b282-vs-3.12.6.svg) | 1.063x ↑<br>[📄](results/bm-20250107-3.14.0a3%2B-e08b282/bm-20250107-vultr-x86_64-python-e08b28235a863323ca3a-3.14.0a3%2B-e08b282-vs-3.13.0rc2.md)[📈](results/bm-20250107-3.14.0a3%2B-e08b282/bm-20250107-vultr-x86_64-python-e08b28235a863323ca3a-3.14.0a3%2B-e08b282-vs-3.13.0rc2.svg) |  |
| [2025-01-07](results/bm-20250107-3.14.0a3%2B-e08b282-NOGIL) | python/e08b28235a863323ca3a | e08b282 (NOGIL) | 1.159x ↓<br>[📄](results/bm-20250107-3.14.0a3%2B-e08b282-NOGIL/bm-20250107-vultr-x86_64-python-e08b28235a863323ca3a-3.14.0a3%2B-e08b282-vs-3.12.6.md)[📈](results/bm-20250107-3.14.0a3%2B-e08b282-NOGIL/bm-20250107-vultr-x86_64-python-e08b28235a863323ca3a-3.14.0a3%2B-e08b282-vs-3.12.6.svg) | 1.186x ↓<br>[📄](results/bm-20250107-3.14.0a3%2B-e08b282-NOGIL/bm-20250107-vultr-x86_64-python-e08b28235a863323ca3a-3.14.0a3%2B-e08b282-vs-3.13.0rc2.md)[📈](results/bm-20250107-3.14.0a3%2B-e08b282-NOGIL/bm-20250107-vultr-x86_64-python-e08b28235a863323ca3a-3.14.0a3%2B-e08b282-vs-3.13.0rc2.svg) | 1.232x ↓<br>[📄](results/bm-20250107-3.14.0a3%2B-e08b282-NOGIL/bm-20250107-vultr-x86_64-python-e08b28235a863323ca3a-3.14.0a3%2B-e08b282-vs-base.md)[📈](results/bm-20250107-3.14.0a3%2B-e08b282-NOGIL/bm-20250107-vultr-x86_64-python-e08b28235a863323ca3a-3.14.0a3%2B-e08b282-vs-base.svg)[🧠](results/bm-20250107-3.14.0a3%2B-e08b282-NOGIL/bm-20250107-vultr-x86_64-python-e08b28235a863323ca3a-3.14.0a3%2B-e08b282-vs-base-mem.svg) |
| [2025-01-07](results/bm-20250107-3.14.0a3%2B-953b49e-NOGIL) | python/953b49e5468d02afadda | 953b49e (NOGIL) | 1.168x ↓<br>[📄](results/bm-20250107-3.14.0a3%2B-953b49e-NOGIL/bm-20250107-vultr-x86_64-python-953b49e5468d02afadda-3.14.0a3%2B-953b49e-vs-3.12.6.md)[📈](results/bm-20250107-3.14.0a3%2B-953b49e-NOGIL/bm-20250107-vultr-x86_64-python-953b49e5468d02afadda-3.14.0a3%2B-953b49e-vs-3.12.6.svg) | 1.195x ↓<br>[📄](results/bm-20250107-3.14.0a3%2B-953b49e-NOGIL/bm-20250107-vultr-x86_64-python-953b49e5468d02afadda-3.14.0a3%2B-953b49e-vs-3.13.0rc2.md)[📈](results/bm-20250107-3.14.0a3%2B-953b49e-NOGIL/bm-20250107-vultr-x86_64-python-953b49e5468d02afadda-3.14.0a3%2B-953b49e-vs-3.13.0rc2.svg) | 1.240x ↓<br>[📄](results/bm-20250107-3.14.0a3%2B-953b49e-NOGIL/bm-20250107-vultr-x86_64-python-953b49e5468d02afadda-3.14.0a3%2B-953b49e-vs-base.md)[📈](results/bm-20250107-3.14.0a3%2B-953b49e-NOGIL/bm-20250107-vultr-x86_64-python-953b49e5468d02afadda-3.14.0a3%2B-953b49e-vs-base.svg)[🧠](results/bm-20250107-3.14.0a3%2B-953b49e-NOGIL/bm-20250107-vultr-x86_64-python-953b49e5468d02afadda-3.14.0a3%2B-953b49e-vs-base-mem.svg) |
| [2025-01-07](results/bm-20250107-3.14.0a3%2B-953b49e) | python/953b49e5468d02afadda | 953b49e | 1.102x ↑<br>[📄](results/bm-20250107-3.14.0a3%2B-953b49e/bm-20250107-vultr-x86_64-python-953b49e5468d02afadda-3.14.0a3%2B-953b49e-vs-3.12.6.md)[📈](results/bm-20250107-3.14.0a3%2B-953b49e/bm-20250107-vultr-x86_64-python-953b49e5468d02afadda-3.14.0a3%2B-953b49e-vs-3.12.6.svg) | 1.063x ↑<br>[📄](results/bm-20250107-3.14.0a3%2B-953b49e/bm-20250107-vultr-x86_64-python-953b49e5468d02afadda-3.14.0a3%2B-953b49e-vs-3.13.0rc2.md)[📈](results/bm-20250107-3.14.0a3%2B-953b49e/bm-20250107-vultr-x86_64-python-953b49e5468d02afadda-3.14.0a3%2B-953b49e-vs-3.13.0rc2.svg) |  |
| [2025-01-05](results/bm-20250105-3.14.0a3%2B-3b231be) | python/3b231be8f000ae59faa0 | 3b231be | 1.100x ↑<br>[📄](results/bm-20250105-3.14.0a3%2B-3b231be/bm-20250105-vultr-x86_64-python-3b231be8f000ae59faa0-3.14.0a3%2B-3b231be-vs-3.12.6.md)[📈](results/bm-20250105-3.14.0a3%2B-3b231be/bm-20250105-vultr-x86_64-python-3b231be8f000ae59faa0-3.14.0a3%2B-3b231be-vs-3.12.6.svg) | 1.061x ↑<br>[📄](results/bm-20250105-3.14.0a3%2B-3b231be/bm-20250105-vultr-x86_64-python-3b231be8f000ae59faa0-3.14.0a3%2B-3b231be-vs-3.13.0rc2.md)[📈](results/bm-20250105-3.14.0a3%2B-3b231be/bm-20250105-vultr-x86_64-python-3b231be8f000ae59faa0-3.14.0a3%2B-3b231be-vs-3.13.0rc2.svg) |  |
| [2025-01-05](results/bm-20250105-3.14.0a3%2B-3b231be-NOGIL) | python/3b231be8f000ae59faa0 | 3b231be (NOGIL) | 1.173x ↓<br>[📄](results/bm-20250105-3.14.0a3%2B-3b231be-NOGIL/bm-20250105-vultr-x86_64-python-3b231be8f000ae59faa0-3.14.0a3%2B-3b231be-vs-3.12.6.md)[📈](results/bm-20250105-3.14.0a3%2B-3b231be-NOGIL/bm-20250105-vultr-x86_64-python-3b231be8f000ae59faa0-3.14.0a3%2B-3b231be-vs-3.12.6.svg) | 1.199x ↓<br>[📄](results/bm-20250105-3.14.0a3%2B-3b231be-NOGIL/bm-20250105-vultr-x86_64-python-3b231be8f000ae59faa0-3.14.0a3%2B-3b231be-vs-3.13.0rc2.md)[📈](results/bm-20250105-3.14.0a3%2B-3b231be-NOGIL/bm-20250105-vultr-x86_64-python-3b231be8f000ae59faa0-3.14.0a3%2B-3b231be-vs-3.13.0rc2.svg) | 1.243x ↓<br>[📄](results/bm-20250105-3.14.0a3%2B-3b231be-NOGIL/bm-20250105-vultr-x86_64-python-3b231be8f000ae59faa0-3.14.0a3%2B-3b231be-vs-base.md)[📈](results/bm-20250105-3.14.0a3%2B-3b231be-NOGIL/bm-20250105-vultr-x86_64-python-3b231be8f000ae59faa0-3.14.0a3%2B-3b231be-vs-base.svg)[🧠](results/bm-20250105-3.14.0a3%2B-3b231be-NOGIL/bm-20250105-vultr-x86_64-python-3b231be8f000ae59faa0-3.14.0a3%2B-3b231be-vs-base-mem.svg) |


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
