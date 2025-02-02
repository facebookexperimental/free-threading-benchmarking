# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
[Most recent pystats on main (cf4c4ec)](results/bm-20250201-3.14.0a4%2B-cf4c4ec-PYTHON_UOPS/bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4%2B-cf4c4ec-pystats.md)

## linux x86_64 (linux)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-02-02](results/bm-20250202-3.14.0a4%2B-ae47888) | python/ae4788809d674f8e27fa | ae47888 | 1.101x ↑<br>[📄](results/bm-20250202-3.14.0a4%2B-ae47888/bm-20250202-linux-x86_64-python-ae4788809d674f8e27fa-3.14.0a4%2B-ae47888-vs-3.12.6.md)[📈](results/bm-20250202-3.14.0a4%2B-ae47888/bm-20250202-linux-x86_64-python-ae4788809d674f8e27fa-3.14.0a4%2B-ae47888-vs-3.12.6.svg) | 1.057x ↑<br>[📄](results/bm-20250202-3.14.0a4%2B-ae47888/bm-20250202-linux-x86_64-python-ae4788809d674f8e27fa-3.14.0a4%2B-ae47888-vs-3.13.0rc2.md)[📈](results/bm-20250202-3.14.0a4%2B-ae47888/bm-20250202-linux-x86_64-python-ae4788809d674f8e27fa-3.14.0a4%2B-ae47888-vs-3.13.0rc2.svg) |  |
| [2025-02-02](results/bm-20250202-3.14.0a4%2B-ae47888-NOGIL) | python/ae4788809d674f8e27fa | ae47888 (NOGIL) | 1.037x ↓<br>[📄](results/bm-20250202-3.14.0a4%2B-ae47888-NOGIL/bm-20250202-linux-x86_64-python-ae4788809d674f8e27fa-3.14.0a4%2B-ae47888-vs-3.12.6.md)[📈](results/bm-20250202-3.14.0a4%2B-ae47888-NOGIL/bm-20250202-linux-x86_64-python-ae4788809d674f8e27fa-3.14.0a4%2B-ae47888-vs-3.12.6.svg) | 1.072x ↓<br>[📄](results/bm-20250202-3.14.0a4%2B-ae47888-NOGIL/bm-20250202-linux-x86_64-python-ae4788809d674f8e27fa-3.14.0a4%2B-ae47888-vs-3.13.0rc2.md)[📈](results/bm-20250202-3.14.0a4%2B-ae47888-NOGIL/bm-20250202-linux-x86_64-python-ae4788809d674f8e27fa-3.14.0a4%2B-ae47888-vs-3.13.0rc2.svg) | 1.123x ↓<br>[📄](results/bm-20250202-3.14.0a4%2B-ae47888-NOGIL/bm-20250202-linux-x86_64-python-ae4788809d674f8e27fa-3.14.0a4%2B-ae47888-vs-base.md)[📈](results/bm-20250202-3.14.0a4%2B-ae47888-NOGIL/bm-20250202-linux-x86_64-python-ae4788809d674f8e27fa-3.14.0a4%2B-ae47888-vs-base.svg)[🧠](results/bm-20250202-3.14.0a4%2B-ae47888-NOGIL/bm-20250202-linux-x86_64-python-ae4788809d674f8e27fa-3.14.0a4%2B-ae47888-vs-base-mem.svg) |
| [2025-02-01](results/bm-20250201-3.14.0a4%2B-cf4c4ec-NOGIL) | python/cf4c4ecc26c7e3b89f2e | cf4c4ec (NOGIL) | 1.056x ↓<br>[📄](results/bm-20250201-3.14.0a4%2B-cf4c4ec-NOGIL/bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4%2B-cf4c4ec-vs-3.12.6.md)[📈](results/bm-20250201-3.14.0a4%2B-cf4c4ec-NOGIL/bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4%2B-cf4c4ec-vs-3.12.6.svg) | 1.091x ↓<br>[📄](results/bm-20250201-3.14.0a4%2B-cf4c4ec-NOGIL/bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4%2B-cf4c4ec-vs-3.13.0rc2.md)[📈](results/bm-20250201-3.14.0a4%2B-cf4c4ec-NOGIL/bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4%2B-cf4c4ec-vs-3.13.0rc2.svg) | 1.133x ↓<br>[📄](results/bm-20250201-3.14.0a4%2B-cf4c4ec-NOGIL/bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4%2B-cf4c4ec-vs-base.md)[📈](results/bm-20250201-3.14.0a4%2B-cf4c4ec-NOGIL/bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4%2B-cf4c4ec-vs-base.svg)[🧠](results/bm-20250201-3.14.0a4%2B-cf4c4ec-NOGIL/bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4%2B-cf4c4ec-vs-base-mem.svg) |
| [2025-02-01](results/bm-20250201-3.14.0a4%2B-cf4c4ec) | python/cf4c4ecc26c7e3b89f2e | cf4c4ec | 1.096x ↑<br>[📄](results/bm-20250201-3.14.0a4%2B-cf4c4ec/bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4%2B-cf4c4ec-vs-3.12.6.md)[📈](results/bm-20250201-3.14.0a4%2B-cf4c4ec/bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4%2B-cf4c4ec-vs-3.12.6.svg) | 1.055x ↑<br>[📄](results/bm-20250201-3.14.0a4%2B-cf4c4ec/bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4%2B-cf4c4ec-vs-3.13.0rc2.md)[📈](results/bm-20250201-3.14.0a4%2B-cf4c4ec/bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4%2B-cf4c4ec-vs-3.13.0rc2.svg) |  |
| [2025-01-31](results/bm-20250131-3.14.0a4%2B-c3ae5c9-NOGIL) | python/c3ae5c9e4ad121f8ba60 | c3ae5c9 (NOGIL) | 1.044x ↓<br>[📄](results/bm-20250131-3.14.0a4%2B-c3ae5c9-NOGIL/bm-20250131-linux-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4%2B-c3ae5c9-vs-3.12.6.md)[📈](results/bm-20250131-3.14.0a4%2B-c3ae5c9-NOGIL/bm-20250131-linux-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4%2B-c3ae5c9-vs-3.12.6.svg) | 1.078x ↓<br>[📄](results/bm-20250131-3.14.0a4%2B-c3ae5c9-NOGIL/bm-20250131-linux-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4%2B-c3ae5c9-vs-3.13.0rc2.md)[📈](results/bm-20250131-3.14.0a4%2B-c3ae5c9-NOGIL/bm-20250131-linux-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4%2B-c3ae5c9-vs-3.13.0rc2.svg) | 1.011x ↓<br>[📄](results/bm-20250131-3.14.0a4%2B-c3ae5c9-NOGIL/bm-20250131-linux-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4%2B-c3ae5c9-vs-base.md)[📈](results/bm-20250131-3.14.0a4%2B-c3ae5c9-NOGIL/bm-20250131-linux-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4%2B-c3ae5c9-vs-base.svg)[🧠](results/bm-20250131-3.14.0a4%2B-c3ae5c9-NOGIL/bm-20250131-linux-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4%2B-c3ae5c9-vs-base-mem.svg) |
| [2025-01-31](results/bm-20250131-3.14.0a4%2B-31c82c2-NOGIL) | python/31c82c28f927b7e55c7d | 31c82c2 (NOGIL) | 1.032x ↓<br>[📄](results/bm-20250131-3.14.0a4%2B-31c82c2-NOGIL/bm-20250131-linux-x86_64-python-31c82c28f927b7e55c7d-3.14.0a4%2B-31c82c2-vs-3.12.6.md)[📈](results/bm-20250131-3.14.0a4%2B-31c82c2-NOGIL/bm-20250131-linux-x86_64-python-31c82c28f927b7e55c7d-3.14.0a4%2B-31c82c2-vs-3.12.6.svg) | 1.066x ↓<br>[📄](results/bm-20250131-3.14.0a4%2B-31c82c2-NOGIL/bm-20250131-linux-x86_64-python-31c82c28f927b7e55c7d-3.14.0a4%2B-31c82c2-vs-3.13.0rc2.md)[📈](results/bm-20250131-3.14.0a4%2B-31c82c2-NOGIL/bm-20250131-linux-x86_64-python-31c82c28f927b7e55c7d-3.14.0a4%2B-31c82c2-vs-3.13.0rc2.svg) |  |
| [2025-01-31](results/bm-20250131-3.14.0a4%2B-d89a5f6-NOGIL) | python/d89a5f6a6e65511a5f6e | d89a5f6 (NOGIL) | 1.035x ↓<br>[📄](results/bm-20250131-3.14.0a4%2B-d89a5f6-NOGIL/bm-20250131-linux-x86_64-python-d89a5f6a6e65511a5f6e-3.14.0a4%2B-d89a5f6-vs-3.12.6.md)[📈](results/bm-20250131-3.14.0a4%2B-d89a5f6-NOGIL/bm-20250131-linux-x86_64-python-d89a5f6a6e65511a5f6e-3.14.0a4%2B-d89a5f6-vs-3.12.6.svg) | 1.072x ↓<br>[📄](results/bm-20250131-3.14.0a4%2B-d89a5f6-NOGIL/bm-20250131-linux-x86_64-python-d89a5f6a6e65511a5f6e-3.14.0a4%2B-d89a5f6-vs-3.13.0rc2.md)[📈](results/bm-20250131-3.14.0a4%2B-d89a5f6-NOGIL/bm-20250131-linux-x86_64-python-d89a5f6a6e65511a5f6e-3.14.0a4%2B-d89a5f6-vs-3.13.0rc2.svg) | 1.100x ↓<br>[📄](results/bm-20250131-3.14.0a4%2B-d89a5f6-NOGIL/bm-20250131-linux-x86_64-python-d89a5f6a6e65511a5f6e-3.14.0a4%2B-d89a5f6-vs-base.md)[📈](results/bm-20250131-3.14.0a4%2B-d89a5f6-NOGIL/bm-20250131-linux-x86_64-python-d89a5f6a6e65511a5f6e-3.14.0a4%2B-d89a5f6-vs-base.svg)[🧠](results/bm-20250131-3.14.0a4%2B-d89a5f6-NOGIL/bm-20250131-linux-x86_64-python-d89a5f6a6e65511a5f6e-3.14.0a4%2B-d89a5f6-vs-base-mem.svg) |
| [2025-01-31](results/bm-20250131-3.14.0a4%2B-d89a5f6) | python/d89a5f6a6e65511a5f6e | d89a5f6 | 1.074x ↑<br>[📄](results/bm-20250131-3.14.0a4%2B-d89a5f6/bm-20250131-linux-x86_64-python-d89a5f6a6e65511a5f6e-3.14.0a4%2B-d89a5f6-vs-3.12.6.md)[📈](results/bm-20250131-3.14.0a4%2B-d89a5f6/bm-20250131-linux-x86_64-python-d89a5f6a6e65511a5f6e-3.14.0a4%2B-d89a5f6-vs-3.12.6.svg) | 1.035x ↑<br>[📄](results/bm-20250131-3.14.0a4%2B-d89a5f6/bm-20250131-linux-x86_64-python-d89a5f6a6e65511a5f6e-3.14.0a4%2B-d89a5f6-vs-3.13.0rc2.md)[📈](results/bm-20250131-3.14.0a4%2B-d89a5f6/bm-20250131-linux-x86_64-python-d89a5f6a6e65511a5f6e-3.14.0a4%2B-d89a5f6-vs-3.13.0rc2.svg) |  |
| [2025-01-30](results/bm-20250130-3.14.0a4%2B-10ee2d9) | python/10ee2d9d3bcde27c75f1 | 10ee2d9 | 1.089x ↑<br>[📄](results/bm-20250130-3.14.0a4%2B-10ee2d9/bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4%2B-10ee2d9-vs-3.12.6.md)[📈](results/bm-20250130-3.14.0a4%2B-10ee2d9/bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4%2B-10ee2d9-vs-3.12.6.svg) | 1.049x ↑<br>[📄](results/bm-20250130-3.14.0a4%2B-10ee2d9/bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4%2B-10ee2d9-vs-3.13.0rc2.md)[📈](results/bm-20250130-3.14.0a4%2B-10ee2d9/bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4%2B-10ee2d9-vs-3.13.0rc2.svg) |  |
| [2025-01-30](results/bm-20250130-3.14.0a4%2B-10ee2d9-NOGIL) | python/10ee2d9d3bcde27c75f1 | 10ee2d9 (NOGIL) | 1.051x ↓<br>[📄](results/bm-20250130-3.14.0a4%2B-10ee2d9-NOGIL/bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4%2B-10ee2d9-vs-3.12.6.md)[📈](results/bm-20250130-3.14.0a4%2B-10ee2d9-NOGIL/bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4%2B-10ee2d9-vs-3.12.6.svg) | 1.083x ↓<br>[📄](results/bm-20250130-3.14.0a4%2B-10ee2d9-NOGIL/bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4%2B-10ee2d9-vs-3.13.0rc2.md)[📈](results/bm-20250130-3.14.0a4%2B-10ee2d9-NOGIL/bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4%2B-10ee2d9-vs-3.13.0rc2.svg) | 1.127x ↓<br>[📄](results/bm-20250130-3.14.0a4%2B-10ee2d9-NOGIL/bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4%2B-10ee2d9-vs-base.md)[📈](results/bm-20250130-3.14.0a4%2B-10ee2d9-NOGIL/bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4%2B-10ee2d9-vs-base.svg)[🧠](results/bm-20250130-3.14.0a4%2B-10ee2d9-NOGIL/bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4%2B-10ee2d9-vs-base-mem.svg) |
| [2025-01-30](results/bm-20250130-3.14.0a4%2B-a549f43-NOGIL) | python/a549f439384b4509b256 | a549f43 (NOGIL) | 1.047x ↓<br>[📄](results/bm-20250130-3.14.0a4%2B-a549f43-NOGIL/bm-20250130-linux-x86_64-python-a549f439384b4509b256-3.14.0a4%2B-a549f43-vs-3.12.6.md)[📈](results/bm-20250130-3.14.0a4%2B-a549f43-NOGIL/bm-20250130-linux-x86_64-python-a549f439384b4509b256-3.14.0a4%2B-a549f43-vs-3.12.6.svg) | 1.082x ↓<br>[📄](results/bm-20250130-3.14.0a4%2B-a549f43-NOGIL/bm-20250130-linux-x86_64-python-a549f439384b4509b256-3.14.0a4%2B-a549f43-vs-3.13.0rc2.md)[📈](results/bm-20250130-3.14.0a4%2B-a549f43-NOGIL/bm-20250130-linux-x86_64-python-a549f439384b4509b256-3.14.0a4%2B-a549f43-vs-3.13.0rc2.svg) | 1.111x ↓<br>[📄](results/bm-20250130-3.14.0a4%2B-a549f43-NOGIL/bm-20250130-linux-x86_64-python-a549f439384b4509b256-3.14.0a4%2B-a549f43-vs-base.md)[📈](results/bm-20250130-3.14.0a4%2B-a549f43-NOGIL/bm-20250130-linux-x86_64-python-a549f439384b4509b256-3.14.0a4%2B-a549f43-vs-base.svg)[🧠](results/bm-20250130-3.14.0a4%2B-a549f43-NOGIL/bm-20250130-linux-x86_64-python-a549f439384b4509b256-3.14.0a4%2B-a549f43-vs-base-mem.svg) |
| [2025-01-30](results/bm-20250130-3.14.0a4%2B-a549f43) | python/a549f439384b4509b256 | a549f43 | 1.077x ↑<br>[📄](results/bm-20250130-3.14.0a4%2B-a549f43/bm-20250130-linux-x86_64-python-a549f439384b4509b256-3.14.0a4%2B-a549f43-vs-3.12.6.md)[📈](results/bm-20250130-3.14.0a4%2B-a549f43/bm-20250130-linux-x86_64-python-a549f439384b4509b256-3.14.0a4%2B-a549f43-vs-3.12.6.svg) | 1.034x ↑<br>[📄](results/bm-20250130-3.14.0a4%2B-a549f43/bm-20250130-linux-x86_64-python-a549f439384b4509b256-3.14.0a4%2B-a549f43-vs-3.13.0rc2.md)[📈](results/bm-20250130-3.14.0a4%2B-a549f43/bm-20250130-linux-x86_64-python-a549f439384b4509b256-3.14.0a4%2B-a549f43-vs-3.13.0rc2.svg) |  |

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-02-02](results/bm-20250202-3.14.0a4%2B-ae47888) | python/ae4788809d674f8e27fa | ae47888 | 1.100x ↑<br>[📄](results/bm-20250202-3.14.0a4%2B-ae47888/bm-20250202-vultr-x86_64-python-ae4788809d674f8e27fa-3.14.0a4%2B-ae47888-vs-3.12.6.md)[📈](results/bm-20250202-3.14.0a4%2B-ae47888/bm-20250202-vultr-x86_64-python-ae4788809d674f8e27fa-3.14.0a4%2B-ae47888-vs-3.12.6.svg) | 1.061x ↑<br>[📄](results/bm-20250202-3.14.0a4%2B-ae47888/bm-20250202-vultr-x86_64-python-ae4788809d674f8e27fa-3.14.0a4%2B-ae47888-vs-3.13.0rc2.md)[📈](results/bm-20250202-3.14.0a4%2B-ae47888/bm-20250202-vultr-x86_64-python-ae4788809d674f8e27fa-3.14.0a4%2B-ae47888-vs-3.13.0rc2.svg) |  |
| [2025-02-02](results/bm-20250202-3.14.0a4%2B-ae47888-NOGIL) | python/ae4788809d674f8e27fa | ae47888 (NOGIL) | 1.027x ↓<br>[📄](results/bm-20250202-3.14.0a4%2B-ae47888-NOGIL/bm-20250202-vultr-x86_64-python-ae4788809d674f8e27fa-3.14.0a4%2B-ae47888-vs-3.12.6.md)[📈](results/bm-20250202-3.14.0a4%2B-ae47888-NOGIL/bm-20250202-vultr-x86_64-python-ae4788809d674f8e27fa-3.14.0a4%2B-ae47888-vs-3.12.6.svg) | 1.059x ↓<br>[📄](results/bm-20250202-3.14.0a4%2B-ae47888-NOGIL/bm-20250202-vultr-x86_64-python-ae4788809d674f8e27fa-3.14.0a4%2B-ae47888-vs-3.13.0rc2.md)[📈](results/bm-20250202-3.14.0a4%2B-ae47888-NOGIL/bm-20250202-vultr-x86_64-python-ae4788809d674f8e27fa-3.14.0a4%2B-ae47888-vs-3.13.0rc2.svg) | 1.117x ↓<br>[📄](results/bm-20250202-3.14.0a4%2B-ae47888-NOGIL/bm-20250202-vultr-x86_64-python-ae4788809d674f8e27fa-3.14.0a4%2B-ae47888-vs-base.md)[📈](results/bm-20250202-3.14.0a4%2B-ae47888-NOGIL/bm-20250202-vultr-x86_64-python-ae4788809d674f8e27fa-3.14.0a4%2B-ae47888-vs-base.svg)[🧠](results/bm-20250202-3.14.0a4%2B-ae47888-NOGIL/bm-20250202-vultr-x86_64-python-ae4788809d674f8e27fa-3.14.0a4%2B-ae47888-vs-base-mem.svg) |
| [2025-02-01](results/bm-20250201-3.14.0a4%2B-cf4c4ec-NOGIL) | python/cf4c4ecc26c7e3b89f2e | cf4c4ec (NOGIL) | 1.024x ↓<br>[📄](results/bm-20250201-3.14.0a4%2B-cf4c4ec-NOGIL/bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4%2B-cf4c4ec-vs-3.12.6.md)[📈](results/bm-20250201-3.14.0a4%2B-cf4c4ec-NOGIL/bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4%2B-cf4c4ec-vs-3.12.6.svg) | 1.056x ↓<br>[📄](results/bm-20250201-3.14.0a4%2B-cf4c4ec-NOGIL/bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4%2B-cf4c4ec-vs-3.13.0rc2.md)[📈](results/bm-20250201-3.14.0a4%2B-cf4c4ec-NOGIL/bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4%2B-cf4c4ec-vs-3.13.0rc2.svg) | 1.117x ↓<br>[📄](results/bm-20250201-3.14.0a4%2B-cf4c4ec-NOGIL/bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4%2B-cf4c4ec-vs-base.md)[📈](results/bm-20250201-3.14.0a4%2B-cf4c4ec-NOGIL/bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4%2B-cf4c4ec-vs-base.svg)[🧠](results/bm-20250201-3.14.0a4%2B-cf4c4ec-NOGIL/bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4%2B-cf4c4ec-vs-base-mem.svg) |
| [2025-02-01](results/bm-20250201-3.14.0a4%2B-cf4c4ec) | python/cf4c4ecc26c7e3b89f2e | cf4c4ec | 1.104x ↑<br>[📄](results/bm-20250201-3.14.0a4%2B-cf4c4ec/bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4%2B-cf4c4ec-vs-3.12.6.md)[📈](results/bm-20250201-3.14.0a4%2B-cf4c4ec/bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4%2B-cf4c4ec-vs-3.12.6.svg) | 1.065x ↑<br>[📄](results/bm-20250201-3.14.0a4%2B-cf4c4ec/bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4%2B-cf4c4ec-vs-3.13.0rc2.md)[📈](results/bm-20250201-3.14.0a4%2B-cf4c4ec/bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4%2B-cf4c4ec-vs-3.13.0rc2.svg) |  |
| [2025-02-01](results/bm-20250201-3.14.0a4%2B-3edc57c-NOGIL) | mpage/revert_c3ae5c9 | 3edc57c (NOGIL) | 1.051x ↓<br>[📄](results/bm-20250201-3.14.0a4%2B-3edc57c-NOGIL/bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4%2B-3edc57c-vs-3.12.6.md)[📈](results/bm-20250201-3.14.0a4%2B-3edc57c-NOGIL/bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4%2B-3edc57c-vs-3.12.6.svg) | 1.082x ↓<br>[📄](results/bm-20250201-3.14.0a4%2B-3edc57c-NOGIL/bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4%2B-3edc57c-vs-3.13.0rc2.md)[📈](results/bm-20250201-3.14.0a4%2B-3edc57c-NOGIL/bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4%2B-3edc57c-vs-3.13.0rc2.svg) | 1.027x ↓<br>[📄](results/bm-20250201-3.14.0a4%2B-3edc57c-NOGIL/bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4%2B-3edc57c-vs-base.md)[📈](results/bm-20250201-3.14.0a4%2B-3edc57c-NOGIL/bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4%2B-3edc57c-vs-base.svg)[🧠](results/bm-20250201-3.14.0a4%2B-3edc57c-NOGIL/bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4%2B-3edc57c-vs-base-mem.svg) |
| [2025-01-31](results/bm-20250131-3.14.0a4%2B-abfc49a-NOGIL) | nascheme/gh_129201_gc_mark_pr | abfc49a (NOGIL) | 1.043x ↓<br>[📄](results/bm-20250131-3.14.0a4%2B-abfc49a-NOGIL/bm-20250131-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4%2B-abfc49a-vs-3.12.6.md)[📈](results/bm-20250131-3.14.0a4%2B-abfc49a-NOGIL/bm-20250131-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4%2B-abfc49a-vs-3.12.6.svg) | 1.074x ↓<br>[📄](results/bm-20250131-3.14.0a4%2B-abfc49a-NOGIL/bm-20250131-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4%2B-abfc49a-vs-3.13.0rc2.md)[📈](results/bm-20250131-3.14.0a4%2B-abfc49a-NOGIL/bm-20250131-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4%2B-abfc49a-vs-3.13.0rc2.svg) | 1.005x ↑<br>[📄](results/bm-20250131-3.14.0a4%2B-abfc49a-NOGIL/bm-20250131-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4%2B-abfc49a-vs-base.md)[📈](results/bm-20250131-3.14.0a4%2B-abfc49a-NOGIL/bm-20250131-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4%2B-abfc49a-vs-base.svg)[🧠](results/bm-20250131-3.14.0a4%2B-abfc49a-NOGIL/bm-20250131-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4%2B-abfc49a-vs-base-mem.svg) |
| [2025-01-31](results/bm-20250131-3.14.0a4%2B-54f74b8-NOGIL) | python/54f74b80aef8b581f2b1 | 54f74b8 (NOGIL) | 1.026x ↓<br>[📄](results/bm-20250131-3.14.0a4%2B-54f74b8-NOGIL/bm-20250131-vultr-x86_64-python-54f74b80aef8b581f2b1-3.14.0a4%2B-54f74b8-vs-3.12.6.md)[📈](results/bm-20250131-3.14.0a4%2B-54f74b8-NOGIL/bm-20250131-vultr-x86_64-python-54f74b80aef8b581f2b1-3.14.0a4%2B-54f74b8-vs-3.12.6.svg) | 1.058x ↓<br>[📄](results/bm-20250131-3.14.0a4%2B-54f74b8-NOGIL/bm-20250131-vultr-x86_64-python-54f74b80aef8b581f2b1-3.14.0a4%2B-54f74b8-vs-3.13.0rc2.md)[📈](results/bm-20250131-3.14.0a4%2B-54f74b8-NOGIL/bm-20250131-vultr-x86_64-python-54f74b80aef8b581f2b1-3.14.0a4%2B-54f74b8-vs-3.13.0rc2.svg) | 1.000x ↓<br>[📄](results/bm-20250131-3.14.0a4%2B-54f74b8-NOGIL/bm-20250131-vultr-x86_64-python-54f74b80aef8b581f2b1-3.14.0a4%2B-54f74b8-vs-base.md)[📈](results/bm-20250131-3.14.0a4%2B-54f74b8-NOGIL/bm-20250131-vultr-x86_64-python-54f74b80aef8b581f2b1-3.14.0a4%2B-54f74b8-vs-base.svg)[🧠](results/bm-20250131-3.14.0a4%2B-54f74b8-NOGIL/bm-20250131-vultr-x86_64-python-54f74b80aef8b581f2b1-3.14.0a4%2B-54f74b8-vs-base-mem.svg) |
| [2025-01-31](results/bm-20250131-3.14.0a4%2B-9ba281d-NOGIL) | python/9ba281d871c4df3a3ac4 | 9ba281d (NOGIL) | 1.025x ↓<br>[📄](results/bm-20250131-3.14.0a4%2B-9ba281d-NOGIL/bm-20250131-vultr-x86_64-python-9ba281d871c4df3a3ac4-3.14.0a4%2B-9ba281d-vs-3.12.6.md)[📈](results/bm-20250131-3.14.0a4%2B-9ba281d-NOGIL/bm-20250131-vultr-x86_64-python-9ba281d871c4df3a3ac4-3.14.0a4%2B-9ba281d-vs-3.12.6.svg) | 1.057x ↓<br>[📄](results/bm-20250131-3.14.0a4%2B-9ba281d-NOGIL/bm-20250131-vultr-x86_64-python-9ba281d871c4df3a3ac4-3.14.0a4%2B-9ba281d-vs-3.13.0rc2.md)[📈](results/bm-20250131-3.14.0a4%2B-9ba281d-NOGIL/bm-20250131-vultr-x86_64-python-9ba281d871c4df3a3ac4-3.14.0a4%2B-9ba281d-vs-3.13.0rc2.svg) |  |
| [2025-01-31](results/bm-20250131-3.14.0a4%2B-c3ae5c9-NOGIL) | python/c3ae5c9e4ad121f8ba60 | c3ae5c9 (NOGIL) | 1.029x ↓<br>[📄](results/bm-20250131-3.14.0a4%2B-c3ae5c9-NOGIL/bm-20250131-vultr-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4%2B-c3ae5c9-vs-3.12.6.md)[📈](results/bm-20250131-3.14.0a4%2B-c3ae5c9-NOGIL/bm-20250131-vultr-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4%2B-c3ae5c9-vs-3.12.6.svg) | 1.061x ↓<br>[📄](results/bm-20250131-3.14.0a4%2B-c3ae5c9-NOGIL/bm-20250131-vultr-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4%2B-c3ae5c9-vs-3.13.0rc2.md)[📈](results/bm-20250131-3.14.0a4%2B-c3ae5c9-NOGIL/bm-20250131-vultr-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4%2B-c3ae5c9-vs-3.13.0rc2.svg) | 1.029x ↑<br>[📄](results/bm-20250131-3.14.0a4%2B-c3ae5c9-NOGIL/bm-20250131-vultr-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4%2B-c3ae5c9-vs-base.md)[📈](results/bm-20250131-3.14.0a4%2B-c3ae5c9-NOGIL/bm-20250131-vultr-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4%2B-c3ae5c9-vs-base.svg)[🧠](results/bm-20250131-3.14.0a4%2B-c3ae5c9-NOGIL/bm-20250131-vultr-x86_64-python-c3ae5c9e4ad121f8ba60-3.14.0a4%2B-c3ae5c9-vs-base-mem.svg) |
| [2025-01-31](results/bm-20250131-3.14.0a4%2B-31c82c2-NOGIL) | python/31c82c28f927b7e55c7d | 31c82c2 (NOGIL) | 1.057x ↓<br>[📄](results/bm-20250131-3.14.0a4%2B-31c82c2-NOGIL/bm-20250131-vultr-x86_64-python-31c82c28f927b7e55c7d-3.14.0a4%2B-31c82c2-vs-3.12.6.md)[📈](results/bm-20250131-3.14.0a4%2B-31c82c2-NOGIL/bm-20250131-vultr-x86_64-python-31c82c28f927b7e55c7d-3.14.0a4%2B-31c82c2-vs-3.12.6.svg) | 1.087x ↓<br>[📄](results/bm-20250131-3.14.0a4%2B-31c82c2-NOGIL/bm-20250131-vultr-x86_64-python-31c82c28f927b7e55c7d-3.14.0a4%2B-31c82c2-vs-3.13.0rc2.md)[📈](results/bm-20250131-3.14.0a4%2B-31c82c2-NOGIL/bm-20250131-vultr-x86_64-python-31c82c28f927b7e55c7d-3.14.0a4%2B-31c82c2-vs-3.13.0rc2.svg) |  |
| [2025-01-31](results/bm-20250131-3.14.0a4%2B-d89a5f6-NOGIL) | python/main | d89a5f6 (NOGIL) | 1.026x ↓<br>[📄](results/bm-20250131-3.14.0a4%2B-d89a5f6-NOGIL/bm-20250131-vultr-x86_64-python-main-3.14.0a4%2B-d89a5f6-vs-3.12.6.md)[📈](results/bm-20250131-3.14.0a4%2B-d89a5f6-NOGIL/bm-20250131-vultr-x86_64-python-main-3.14.0a4%2B-d89a5f6-vs-3.12.6.svg) | 1.057x ↓<br>[📄](results/bm-20250131-3.14.0a4%2B-d89a5f6-NOGIL/bm-20250131-vultr-x86_64-python-main-3.14.0a4%2B-d89a5f6-vs-3.13.0rc2.md)[📈](results/bm-20250131-3.14.0a4%2B-d89a5f6-NOGIL/bm-20250131-vultr-x86_64-python-main-3.14.0a4%2B-d89a5f6-vs-3.13.0rc2.svg) | 1.104x ↓<br>[📄](results/bm-20250131-3.14.0a4%2B-d89a5f6-NOGIL/bm-20250131-vultr-x86_64-python-main-3.14.0a4%2B-d89a5f6-vs-base.md)[📈](results/bm-20250131-3.14.0a4%2B-d89a5f6-NOGIL/bm-20250131-vultr-x86_64-python-main-3.14.0a4%2B-d89a5f6-vs-base.svg)[🧠](results/bm-20250131-3.14.0a4%2B-d89a5f6-NOGIL/bm-20250131-vultr-x86_64-python-main-3.14.0a4%2B-d89a5f6-vs-base-mem.svg) |
| [2025-01-31](results/bm-20250131-3.14.0a4%2B-d89a5f6-NOGIL) | python/d89a5f6a6e65511a5f6e | d89a5f6 (NOGIL) | 1.027x ↓<br>[📄](results/bm-20250131-3.14.0a4%2B-d89a5f6-NOGIL/bm-20250131-vultr-x86_64-python-d89a5f6a6e65511a5f6e-3.14.0a4%2B-d89a5f6-vs-3.12.6.md)[📈](results/bm-20250131-3.14.0a4%2B-d89a5f6-NOGIL/bm-20250131-vultr-x86_64-python-d89a5f6a6e65511a5f6e-3.14.0a4%2B-d89a5f6-vs-3.12.6.svg) | 1.059x ↓<br>[📄](results/bm-20250131-3.14.0a4%2B-d89a5f6-NOGIL/bm-20250131-vultr-x86_64-python-d89a5f6a6e65511a5f6e-3.14.0a4%2B-d89a5f6-vs-3.13.0rc2.md)[📈](results/bm-20250131-3.14.0a4%2B-d89a5f6-NOGIL/bm-20250131-vultr-x86_64-python-d89a5f6a6e65511a5f6e-3.14.0a4%2B-d89a5f6-vs-3.13.0rc2.svg) | 1.106x ↓<br>[📄](results/bm-20250131-3.14.0a4%2B-d89a5f6-NOGIL/bm-20250131-vultr-x86_64-python-d89a5f6a6e65511a5f6e-3.14.0a4%2B-d89a5f6-vs-base.md)[📈](results/bm-20250131-3.14.0a4%2B-d89a5f6-NOGIL/bm-20250131-vultr-x86_64-python-d89a5f6a6e65511a5f6e-3.14.0a4%2B-d89a5f6-vs-base.svg)[🧠](results/bm-20250131-3.14.0a4%2B-d89a5f6-NOGIL/bm-20250131-vultr-x86_64-python-d89a5f6a6e65511a5f6e-3.14.0a4%2B-d89a5f6-vs-base-mem.svg) |
| [2025-01-31](results/bm-20250131-3.14.0a4%2B-d89a5f6) | python/d89a5f6a6e65511a5f6e | d89a5f6 | 1.086x ↑<br>[📄](results/bm-20250131-3.14.0a4%2B-d89a5f6/bm-20250131-vultr-x86_64-python-d89a5f6a6e65511a5f6e-3.14.0a4%2B-d89a5f6-vs-3.12.6.md)[📈](results/bm-20250131-3.14.0a4%2B-d89a5f6/bm-20250131-vultr-x86_64-python-d89a5f6a6e65511a5f6e-3.14.0a4%2B-d89a5f6-vs-3.12.6.svg) | 1.047x ↑<br>[📄](results/bm-20250131-3.14.0a4%2B-d89a5f6/bm-20250131-vultr-x86_64-python-d89a5f6a6e65511a5f6e-3.14.0a4%2B-d89a5f6-vs-3.13.0rc2.md)[📈](results/bm-20250131-3.14.0a4%2B-d89a5f6/bm-20250131-vultr-x86_64-python-d89a5f6a6e65511a5f6e-3.14.0a4%2B-d89a5f6-vs-3.13.0rc2.svg) |  |
| [2025-01-30](results/bm-20250130-3.14.0a4%2B-10ee2d9) | python/10ee2d9d3bcde27c75f1 | 10ee2d9 | 1.097x ↑<br>[📄](results/bm-20250130-3.14.0a4%2B-10ee2d9/bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4%2B-10ee2d9-vs-3.12.6.md)[📈](results/bm-20250130-3.14.0a4%2B-10ee2d9/bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4%2B-10ee2d9-vs-3.12.6.svg) | 1.058x ↑<br>[📄](results/bm-20250130-3.14.0a4%2B-10ee2d9/bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4%2B-10ee2d9-vs-3.13.0rc2.md)[📈](results/bm-20250130-3.14.0a4%2B-10ee2d9/bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4%2B-10ee2d9-vs-3.13.0rc2.svg) |  |
| [2025-01-30](results/bm-20250130-3.14.0a4%2B-10ee2d9-NOGIL) | python/10ee2d9d3bcde27c75f1 | 10ee2d9 (NOGIL) | 1.050x ↓<br>[📄](results/bm-20250130-3.14.0a4%2B-10ee2d9-NOGIL/bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4%2B-10ee2d9-vs-3.12.6.md)[📈](results/bm-20250130-3.14.0a4%2B-10ee2d9-NOGIL/bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4%2B-10ee2d9-vs-3.12.6.svg) | 1.080x ↓<br>[📄](results/bm-20250130-3.14.0a4%2B-10ee2d9-NOGIL/bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4%2B-10ee2d9-vs-3.13.0rc2.md)[📈](results/bm-20250130-3.14.0a4%2B-10ee2d9-NOGIL/bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4%2B-10ee2d9-vs-3.13.0rc2.svg) | 1.134x ↓<br>[📄](results/bm-20250130-3.14.0a4%2B-10ee2d9-NOGIL/bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4%2B-10ee2d9-vs-base.md)[📈](results/bm-20250130-3.14.0a4%2B-10ee2d9-NOGIL/bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4%2B-10ee2d9-vs-base.svg)[🧠](results/bm-20250130-3.14.0a4%2B-10ee2d9-NOGIL/bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4%2B-10ee2d9-vs-base-mem.svg) |
| [2025-01-30](results/bm-20250130-3.14.0a4%2B-e12dd2e-NOGIL) | nascheme/gh_129201_gc_mark_pr | e12dd2e (NOGIL) | 1.054x ↓<br>[📄](results/bm-20250130-3.14.0a4%2B-e12dd2e-NOGIL/bm-20250130-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4%2B-e12dd2e-vs-3.12.6.md)[📈](results/bm-20250130-3.14.0a4%2B-e12dd2e-NOGIL/bm-20250130-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4%2B-e12dd2e-vs-3.12.6.svg) | 1.085x ↓<br>[📄](results/bm-20250130-3.14.0a4%2B-e12dd2e-NOGIL/bm-20250130-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4%2B-e12dd2e-vs-3.13.0rc2.md)[📈](results/bm-20250130-3.14.0a4%2B-e12dd2e-NOGIL/bm-20250130-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4%2B-e12dd2e-vs-3.13.0rc2.svg) | 1.006x ↓<br>[📄](results/bm-20250130-3.14.0a4%2B-e12dd2e-NOGIL/bm-20250130-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4%2B-e12dd2e-vs-base.md)[📈](results/bm-20250130-3.14.0a4%2B-e12dd2e-NOGIL/bm-20250130-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4%2B-e12dd2e-vs-base.svg)[🧠](results/bm-20250130-3.14.0a4%2B-e12dd2e-NOGIL/bm-20250130-vultr-x86_64-nascheme-gh_129201_gc_mark_pr-3.14.0a4%2B-e12dd2e-vs-base-mem.svg) |
| [2025-01-30](results/bm-20250130-3.14.0a4%2B-4ca9fc0-NOGIL) | python/4ca9fc08f89bf7172d41 | 4ca9fc0 (NOGIL) | 1.048x ↓<br>[📄](results/bm-20250130-3.14.0a4%2B-4ca9fc0-NOGIL/bm-20250130-vultr-x86_64-python-4ca9fc08f89bf7172d41-3.14.0a4%2B-4ca9fc0-vs-3.12.6.md)[📈](results/bm-20250130-3.14.0a4%2B-4ca9fc0-NOGIL/bm-20250130-vultr-x86_64-python-4ca9fc08f89bf7172d41-3.14.0a4%2B-4ca9fc0-vs-3.12.6.svg) | 1.079x ↓<br>[📄](results/bm-20250130-3.14.0a4%2B-4ca9fc0-NOGIL/bm-20250130-vultr-x86_64-python-4ca9fc08f89bf7172d41-3.14.0a4%2B-4ca9fc0-vs-3.13.0rc2.md)[📈](results/bm-20250130-3.14.0a4%2B-4ca9fc0-NOGIL/bm-20250130-vultr-x86_64-python-4ca9fc08f89bf7172d41-3.14.0a4%2B-4ca9fc0-vs-3.13.0rc2.svg) |  |
| [2025-01-30](results/bm-20250130-3.14.0a4%2B-a549f43-NOGIL) | python/a549f439384b4509b256 | a549f43 (NOGIL) | 1.045x ↓<br>[📄](results/bm-20250130-3.14.0a4%2B-a549f43-NOGIL/bm-20250130-vultr-x86_64-python-a549f439384b4509b256-3.14.0a4%2B-a549f43-vs-3.12.6.md)[📈](results/bm-20250130-3.14.0a4%2B-a549f43-NOGIL/bm-20250130-vultr-x86_64-python-a549f439384b4509b256-3.14.0a4%2B-a549f43-vs-3.12.6.svg) | 1.076x ↓<br>[📄](results/bm-20250130-3.14.0a4%2B-a549f43-NOGIL/bm-20250130-vultr-x86_64-python-a549f439384b4509b256-3.14.0a4%2B-a549f43-vs-3.13.0rc2.md)[📈](results/bm-20250130-3.14.0a4%2B-a549f43-NOGIL/bm-20250130-vultr-x86_64-python-a549f439384b4509b256-3.14.0a4%2B-a549f43-vs-3.13.0rc2.svg) | 1.134x ↓<br>[📄](results/bm-20250130-3.14.0a4%2B-a549f43-NOGIL/bm-20250130-vultr-x86_64-python-a549f439384b4509b256-3.14.0a4%2B-a549f43-vs-base.md)[📈](results/bm-20250130-3.14.0a4%2B-a549f43-NOGIL/bm-20250130-vultr-x86_64-python-a549f439384b4509b256-3.14.0a4%2B-a549f43-vs-base.svg)[🧠](results/bm-20250130-3.14.0a4%2B-a549f43-NOGIL/bm-20250130-vultr-x86_64-python-a549f439384b4509b256-3.14.0a4%2B-a549f43-vs-base-mem.svg) |
| [2025-01-30](results/bm-20250130-3.14.0a4%2B-a549f43) | python/a549f439384b4509b256 | a549f43 | 1.101x ↑<br>[📄](results/bm-20250130-3.14.0a4%2B-a549f43/bm-20250130-vultr-x86_64-python-a549f439384b4509b256-3.14.0a4%2B-a549f43-vs-3.12.6.md)[📈](results/bm-20250130-3.14.0a4%2B-a549f43/bm-20250130-vultr-x86_64-python-a549f439384b4509b256-3.14.0a4%2B-a549f43-vs-3.12.6.svg) | 1.062x ↑<br>[📄](results/bm-20250130-3.14.0a4%2B-a549f43/bm-20250130-vultr-x86_64-python-a549f439384b4509b256-3.14.0a4%2B-a549f43-vs-3.13.0rc2.md)[📈](results/bm-20250130-3.14.0a4%2B-a549f43/bm-20250130-vultr-x86_64-python-a549f439384b4509b256-3.14.0a4%2B-a549f43-vs-3.13.0rc2.svg) |  |


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
