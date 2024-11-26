# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
[Most recent pystats on main (dbd2379)](results/bm-20241123-3.14.0a2%2B-dbd2379-PYTHON_UOPS/bm-20241123-vultr-x86_64-python-dbd23790dbd662169905-3.14.0a2%2B-dbd2379-pystats.md)

## linux x86_64 (linux)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2024-11-25](results/bm-20241125-3.14.0a2%2B-26ff32b) | python/26ff32b30553e1f7b0cc | 26ff32b | 1.083x ↑<br>[📄](results/bm-20241125-3.14.0a2%2B-26ff32b/bm-20241125-linux-x86_64-python-26ff32b30553e1f7b0cc-3.14.0a2%2B-26ff32b-vs-3.12.6.md)[📈](results/bm-20241125-3.14.0a2%2B-26ff32b/bm-20241125-linux-x86_64-python-26ff32b30553e1f7b0cc-3.14.0a2%2B-26ff32b-vs-3.12.6.svg) | 1.039x ↑<br>[📄](results/bm-20241125-3.14.0a2%2B-26ff32b/bm-20241125-linux-x86_64-python-26ff32b30553e1f7b0cc-3.14.0a2%2B-26ff32b-vs-3.13.0rc2.md)[📈](results/bm-20241125-3.14.0a2%2B-26ff32b/bm-20241125-linux-x86_64-python-26ff32b30553e1f7b0cc-3.14.0a2%2B-26ff32b-vs-3.13.0rc2.svg) |  |
| [2024-11-24](results/bm-20241124-3.14.0a2%2B-17c16ae) | python/17c16aea66b606d66f71 | 17c16ae | 1.091x ↑<br>[📄](results/bm-20241124-3.14.0a2%2B-17c16ae/bm-20241124-linux-x86_64-python-17c16aea66b606d66f71-3.14.0a2%2B-17c16ae-vs-3.12.6.md)[📈](results/bm-20241124-3.14.0a2%2B-17c16ae/bm-20241124-linux-x86_64-python-17c16aea66b606d66f71-3.14.0a2%2B-17c16ae-vs-3.12.6.svg) | 1.047x ↑<br>[📄](results/bm-20241124-3.14.0a2%2B-17c16ae/bm-20241124-linux-x86_64-python-17c16aea66b606d66f71-3.14.0a2%2B-17c16ae-vs-3.13.0rc2.md)[📈](results/bm-20241124-3.14.0a2%2B-17c16ae/bm-20241124-linux-x86_64-python-17c16aea66b606d66f71-3.14.0a2%2B-17c16ae-vs-3.13.0rc2.svg) |  |
| [2024-11-24](results/bm-20241124-3.14.0a2%2B-17c16ae-NOGIL) | python/17c16aea66b606d66f71 | 17c16ae (NOGIL) | 1.204x ↓<br>[📄](results/bm-20241124-3.14.0a2%2B-17c16ae-NOGIL/bm-20241124-linux-x86_64-python-17c16aea66b606d66f71-3.14.0a2%2B-17c16ae-vs-3.12.6.md)[📈](results/bm-20241124-3.14.0a2%2B-17c16ae-NOGIL/bm-20241124-linux-x86_64-python-17c16aea66b606d66f71-3.14.0a2%2B-17c16ae-vs-3.12.6.svg) | 1.234x ↓<br>[📄](results/bm-20241124-3.14.0a2%2B-17c16ae-NOGIL/bm-20241124-linux-x86_64-python-17c16aea66b606d66f71-3.14.0a2%2B-17c16ae-vs-3.13.0rc2.md)[📈](results/bm-20241124-3.14.0a2%2B-17c16ae-NOGIL/bm-20241124-linux-x86_64-python-17c16aea66b606d66f71-3.14.0a2%2B-17c16ae-vs-3.13.0rc2.svg) | 1.261x ↓<br>[📄](results/bm-20241124-3.14.0a2%2B-17c16ae-NOGIL/bm-20241124-linux-x86_64-python-17c16aea66b606d66f71-3.14.0a2%2B-17c16ae-vs-base.md)[📈](results/bm-20241124-3.14.0a2%2B-17c16ae-NOGIL/bm-20241124-linux-x86_64-python-17c16aea66b606d66f71-3.14.0a2%2B-17c16ae-vs-base.svg)[🧠](results/bm-20241124-3.14.0a2%2B-17c16ae-NOGIL/bm-20241124-linux-x86_64-python-17c16aea66b606d66f71-3.14.0a2%2B-17c16ae-vs-base-mem.svg) |
| [2024-11-23](results/bm-20241123-3.14.0a2%2B-dbd2379-NOGIL) | python/dbd23790dbd662169905 | dbd2379 (NOGIL) | 1.210x ↓<br>[📄](results/bm-20241123-3.14.0a2%2B-dbd2379-NOGIL/bm-20241123-linux-x86_64-python-dbd23790dbd662169905-3.14.0a2%2B-dbd2379-vs-3.12.6.md)[📈](results/bm-20241123-3.14.0a2%2B-dbd2379-NOGIL/bm-20241123-linux-x86_64-python-dbd23790dbd662169905-3.14.0a2%2B-dbd2379-vs-3.12.6.svg) | 1.241x ↓<br>[📄](results/bm-20241123-3.14.0a2%2B-dbd2379-NOGIL/bm-20241123-linux-x86_64-python-dbd23790dbd662169905-3.14.0a2%2B-dbd2379-vs-3.13.0rc2.md)[📈](results/bm-20241123-3.14.0a2%2B-dbd2379-NOGIL/bm-20241123-linux-x86_64-python-dbd23790dbd662169905-3.14.0a2%2B-dbd2379-vs-3.13.0rc2.svg) | 1.259x ↓<br>[📄](results/bm-20241123-3.14.0a2%2B-dbd2379-NOGIL/bm-20241123-linux-x86_64-python-dbd23790dbd662169905-3.14.0a2%2B-dbd2379-vs-base.md)[📈](results/bm-20241123-3.14.0a2%2B-dbd2379-NOGIL/bm-20241123-linux-x86_64-python-dbd23790dbd662169905-3.14.0a2%2B-dbd2379-vs-base.svg)[🧠](results/bm-20241123-3.14.0a2%2B-dbd2379-NOGIL/bm-20241123-linux-x86_64-python-dbd23790dbd662169905-3.14.0a2%2B-dbd2379-vs-base-mem.svg) |
| [2024-11-23](results/bm-20241123-3.14.0a2%2B-dbd2379) | python/dbd23790dbd662169905 | dbd2379 | 1.077x ↑<br>[📄](results/bm-20241123-3.14.0a2%2B-dbd2379/bm-20241123-linux-x86_64-python-dbd23790dbd662169905-3.14.0a2%2B-dbd2379-vs-3.12.6.md)[📈](results/bm-20241123-3.14.0a2%2B-dbd2379/bm-20241123-linux-x86_64-python-dbd23790dbd662169905-3.14.0a2%2B-dbd2379-vs-3.12.6.svg) | 1.034x ↑<br>[📄](results/bm-20241123-3.14.0a2%2B-dbd2379/bm-20241123-linux-x86_64-python-dbd23790dbd662169905-3.14.0a2%2B-dbd2379-vs-3.13.0rc2.md)[📈](results/bm-20241123-3.14.0a2%2B-dbd2379/bm-20241123-linux-x86_64-python-dbd23790dbd662169905-3.14.0a2%2B-dbd2379-vs-3.13.0rc2.svg) |  |
| [2024-11-22](results/bm-20241122-3.14.0a2%2B-39e60ae-NOGIL) | python/39e60aeb3837f1f23d8b | 39e60ae (NOGIL) | 1.197x ↓<br>[📄](results/bm-20241122-3.14.0a2%2B-39e60ae-NOGIL/bm-20241122-linux-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-3.12.6.md)[📈](results/bm-20241122-3.14.0a2%2B-39e60ae-NOGIL/bm-20241122-linux-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-3.12.6.svg) | 1.227x ↓<br>[📄](results/bm-20241122-3.14.0a2%2B-39e60ae-NOGIL/bm-20241122-linux-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-3.13.0rc2.md)[📈](results/bm-20241122-3.14.0a2%2B-39e60ae-NOGIL/bm-20241122-linux-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-3.13.0rc2.svg) | 1.260x ↓<br>[📄](results/bm-20241122-3.14.0a2%2B-39e60ae-NOGIL/bm-20241122-linux-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-base.md)[📈](results/bm-20241122-3.14.0a2%2B-39e60ae-NOGIL/bm-20241122-linux-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-base.svg)[🧠](results/bm-20241122-3.14.0a2%2B-39e60ae-NOGIL/bm-20241122-linux-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-base-mem.svg) |
| [2024-11-22](results/bm-20241122-3.14.0a2%2B-39e60ae) | python/39e60aeb3837f1f23d8b | 39e60ae | 1.100x ↑<br>[📄](results/bm-20241122-3.14.0a2%2B-39e60ae/bm-20241122-linux-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-3.12.6.md)[📈](results/bm-20241122-3.14.0a2%2B-39e60ae/bm-20241122-linux-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-3.12.6.svg) | 1.053x ↑<br>[📄](results/bm-20241122-3.14.0a2%2B-39e60ae/bm-20241122-linux-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-3.13.0rc2.md)[📈](results/bm-20241122-3.14.0a2%2B-39e60ae/bm-20241122-linux-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-3.13.0rc2.svg) |  |

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2024-11-25](results/bm-20241125-3.14.0a2%2B-a515a0d-NOGIL) | nascheme/gh_115999_load_super | a515a0d (NOGIL) | 1.411x ↓<br>[📄](results/bm-20241125-3.14.0a2%2B-a515a0d-NOGIL/bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2%2B-a515a0d-vs-3.12.6.md)[📈](results/bm-20241125-3.14.0a2%2B-a515a0d-NOGIL/bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2%2B-a515a0d-vs-3.12.6.svg) | 1.431x ↓<br>[📄](results/bm-20241125-3.14.0a2%2B-a515a0d-NOGIL/bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2%2B-a515a0d-vs-3.13.0rc2.md)[📈](results/bm-20241125-3.14.0a2%2B-a515a0d-NOGIL/bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2%2B-a515a0d-vs-3.13.0rc2.svg) | 1.175x ↓<br>[📄](results/bm-20241125-3.14.0a2%2B-a515a0d-NOGIL/bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2%2B-a515a0d-vs-base.md)[📈](results/bm-20241125-3.14.0a2%2B-a515a0d-NOGIL/bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2%2B-a515a0d-vs-base.svg)[🧠](results/bm-20241125-3.14.0a2%2B-a515a0d-NOGIL/bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2%2B-a515a0d-vs-base-mem.svg) |
| [2024-11-24](results/bm-20241124-3.14.0a2%2B-17c16ae) | python/17c16aea66b606d66f71 | 17c16ae | 1.032x ↑<br>[📄](results/bm-20241124-3.14.0a2%2B-17c16ae/bm-20241124-vultr-x86_64-python-17c16aea66b606d66f71-3.14.0a2%2B-17c16ae-vs-3.12.6.md)[📈](results/bm-20241124-3.14.0a2%2B-17c16ae/bm-20241124-vultr-x86_64-python-17c16aea66b606d66f71-3.14.0a2%2B-17c16ae-vs-3.12.6.svg) | 1.005x ↓<br>[📄](results/bm-20241124-3.14.0a2%2B-17c16ae/bm-20241124-vultr-x86_64-python-17c16aea66b606d66f71-3.14.0a2%2B-17c16ae-vs-3.13.0rc2.md)[📈](results/bm-20241124-3.14.0a2%2B-17c16ae/bm-20241124-vultr-x86_64-python-17c16aea66b606d66f71-3.14.0a2%2B-17c16ae-vs-3.13.0rc2.svg) |  |
| [2024-11-24](results/bm-20241124-3.14.0a2%2B-17c16ae-NOGIL) | python/17c16aea66b606d66f71 | 17c16ae (NOGIL) | 1.258x ↓<br>[📄](results/bm-20241124-3.14.0a2%2B-17c16ae-NOGIL/bm-20241124-vultr-x86_64-python-17c16aea66b606d66f71-3.14.0a2%2B-17c16ae-vs-3.12.6.md)[📈](results/bm-20241124-3.14.0a2%2B-17c16ae-NOGIL/bm-20241124-vultr-x86_64-python-17c16aea66b606d66f71-3.14.0a2%2B-17c16ae-vs-3.12.6.svg) | 1.283x ↓<br>[📄](results/bm-20241124-3.14.0a2%2B-17c16ae-NOGIL/bm-20241124-vultr-x86_64-python-17c16aea66b606d66f71-3.14.0a2%2B-17c16ae-vs-3.13.0rc2.md)[📈](results/bm-20241124-3.14.0a2%2B-17c16ae-NOGIL/bm-20241124-vultr-x86_64-python-17c16aea66b606d66f71-3.14.0a2%2B-17c16ae-vs-3.13.0rc2.svg) | 1.273x ↓<br>[📄](results/bm-20241124-3.14.0a2%2B-17c16ae-NOGIL/bm-20241124-vultr-x86_64-python-17c16aea66b606d66f71-3.14.0a2%2B-17c16ae-vs-base.md)[📈](results/bm-20241124-3.14.0a2%2B-17c16ae-NOGIL/bm-20241124-vultr-x86_64-python-17c16aea66b606d66f71-3.14.0a2%2B-17c16ae-vs-base.svg)[🧠](results/bm-20241124-3.14.0a2%2B-17c16ae-NOGIL/bm-20241124-vultr-x86_64-python-17c16aea66b606d66f71-3.14.0a2%2B-17c16ae-vs-base-mem.svg) |
| [2024-11-23](results/bm-20241123-3.14.0a2%2B-dbd2379-NOGIL) | python/dbd23790dbd662169905 | dbd2379 (NOGIL) | 1.264x ↓<br>[📄](results/bm-20241123-3.14.0a2%2B-dbd2379-NOGIL/bm-20241123-vultr-x86_64-python-dbd23790dbd662169905-3.14.0a2%2B-dbd2379-vs-3.12.6.md)[📈](results/bm-20241123-3.14.0a2%2B-dbd2379-NOGIL/bm-20241123-vultr-x86_64-python-dbd23790dbd662169905-3.14.0a2%2B-dbd2379-vs-3.12.6.svg) | 1.289x ↓<br>[📄](results/bm-20241123-3.14.0a2%2B-dbd2379-NOGIL/bm-20241123-vultr-x86_64-python-dbd23790dbd662169905-3.14.0a2%2B-dbd2379-vs-3.13.0rc2.md)[📈](results/bm-20241123-3.14.0a2%2B-dbd2379-NOGIL/bm-20241123-vultr-x86_64-python-dbd23790dbd662169905-3.14.0a2%2B-dbd2379-vs-3.13.0rc2.svg) | 1.280x ↓<br>[📄](results/bm-20241123-3.14.0a2%2B-dbd2379-NOGIL/bm-20241123-vultr-x86_64-python-dbd23790dbd662169905-3.14.0a2%2B-dbd2379-vs-base.md)[📈](results/bm-20241123-3.14.0a2%2B-dbd2379-NOGIL/bm-20241123-vultr-x86_64-python-dbd23790dbd662169905-3.14.0a2%2B-dbd2379-vs-base.svg)[🧠](results/bm-20241123-3.14.0a2%2B-dbd2379-NOGIL/bm-20241123-vultr-x86_64-python-dbd23790dbd662169905-3.14.0a2%2B-dbd2379-vs-base-mem.svg) |
| [2024-11-23](results/bm-20241123-3.14.0a2%2B-dbd2379) | python/dbd23790dbd662169905 | dbd2379 | 1.034x ↑<br>[📄](results/bm-20241123-3.14.0a2%2B-dbd2379/bm-20241123-vultr-x86_64-python-dbd23790dbd662169905-3.14.0a2%2B-dbd2379-vs-3.12.6.md)[📈](results/bm-20241123-3.14.0a2%2B-dbd2379/bm-20241123-vultr-x86_64-python-dbd23790dbd662169905-3.14.0a2%2B-dbd2379-vs-3.12.6.svg) | 1.003x ↓<br>[📄](results/bm-20241123-3.14.0a2%2B-dbd2379/bm-20241123-vultr-x86_64-python-dbd23790dbd662169905-3.14.0a2%2B-dbd2379-vs-3.13.0rc2.md)[📈](results/bm-20241123-3.14.0a2%2B-dbd2379/bm-20241123-vultr-x86_64-python-dbd23790dbd662169905-3.14.0a2%2B-dbd2379-vs-3.13.0rc2.svg) |  |
| [2024-11-22](results/bm-20241122-3.14.0a2%2B-2b63929-NOGIL) | colesbury/gh_115999_store_subs | 2b63929 (NOGIL) | 1.258x ↓<br>[📄](results/bm-20241122-3.14.0a2%2B-2b63929-NOGIL/bm-20241122-vultr-x86_64-colesbury-gh_115999_store_subs-3.14.0a2%2B-2b63929-vs-3.12.6.md)[📈](results/bm-20241122-3.14.0a2%2B-2b63929-NOGIL/bm-20241122-vultr-x86_64-colesbury-gh_115999_store_subs-3.14.0a2%2B-2b63929-vs-3.12.6.svg) | 1.283x ↓<br>[📄](results/bm-20241122-3.14.0a2%2B-2b63929-NOGIL/bm-20241122-vultr-x86_64-colesbury-gh_115999_store_subs-3.14.0a2%2B-2b63929-vs-3.13.0rc2.md)[📈](results/bm-20241122-3.14.0a2%2B-2b63929-NOGIL/bm-20241122-vultr-x86_64-colesbury-gh_115999_store_subs-3.14.0a2%2B-2b63929-vs-3.13.0rc2.svg) | 1.004x ↑<br>[📄](results/bm-20241122-3.14.0a2%2B-2b63929-NOGIL/bm-20241122-vultr-x86_64-colesbury-gh_115999_store_subs-3.14.0a2%2B-2b63929-vs-base.md)[📈](results/bm-20241122-3.14.0a2%2B-2b63929-NOGIL/bm-20241122-vultr-x86_64-colesbury-gh_115999_store_subs-3.14.0a2%2B-2b63929-vs-base.svg)[🧠](results/bm-20241122-3.14.0a2%2B-2b63929-NOGIL/bm-20241122-vultr-x86_64-colesbury-gh_115999_store_subs-3.14.0a2%2B-2b63929-vs-base-mem.svg) |
| [2024-11-22](results/bm-20241122-3.14.0a2%2B-a264637-NOGIL) | python/a264637654f9d3ac3c14 | a264637 (NOGIL) | 1.261x ↓<br>[📄](results/bm-20241122-3.14.0a2%2B-a264637-NOGIL/bm-20241122-vultr-x86_64-python-a264637654f9d3ac3c14-3.14.0a2%2B-a264637-vs-3.12.6.md)[📈](results/bm-20241122-3.14.0a2%2B-a264637-NOGIL/bm-20241122-vultr-x86_64-python-a264637654f9d3ac3c14-3.14.0a2%2B-a264637-vs-3.12.6.svg) | 1.286x ↓<br>[📄](results/bm-20241122-3.14.0a2%2B-a264637-NOGIL/bm-20241122-vultr-x86_64-python-a264637654f9d3ac3c14-3.14.0a2%2B-a264637-vs-3.13.0rc2.md)[📈](results/bm-20241122-3.14.0a2%2B-a264637-NOGIL/bm-20241122-vultr-x86_64-python-a264637654f9d3ac3c14-3.14.0a2%2B-a264637-vs-3.13.0rc2.svg) | 1.008x ↓<br>[📄](results/bm-20241122-3.14.0a2%2B-a264637-NOGIL/bm-20241122-vultr-x86_64-python-a264637654f9d3ac3c14-3.14.0a2%2B-a264637-vs-base.md)[📈](results/bm-20241122-3.14.0a2%2B-a264637-NOGIL/bm-20241122-vultr-x86_64-python-a264637654f9d3ac3c14-3.14.0a2%2B-a264637-vs-base.svg)[🧠](results/bm-20241122-3.14.0a2%2B-a264637-NOGIL/bm-20241122-vultr-x86_64-python-a264637654f9d3ac3c14-3.14.0a2%2B-a264637-vs-base-mem.svg) |
| [2024-11-22](results/bm-20241122-3.14.0a2%2B-39e60ae-NOGIL) | python/39e60aeb3837f1f23d8b | 39e60ae (NOGIL) | 1.261x ↓<br>[📄](results/bm-20241122-3.14.0a2%2B-39e60ae-NOGIL/bm-20241122-vultr-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-3.12.6.md)[📈](results/bm-20241122-3.14.0a2%2B-39e60ae-NOGIL/bm-20241122-vultr-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-3.12.6.svg) | 1.286x ↓<br>[📄](results/bm-20241122-3.14.0a2%2B-39e60ae-NOGIL/bm-20241122-vultr-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-3.13.0rc2.md)[📈](results/bm-20241122-3.14.0a2%2B-39e60ae-NOGIL/bm-20241122-vultr-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-3.13.0rc2.svg) | 1.002x ↑<br>[📄](results/bm-20241122-3.14.0a2%2B-39e60ae-NOGIL/bm-20241122-vultr-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-base.md)[📈](results/bm-20241122-3.14.0a2%2B-39e60ae-NOGIL/bm-20241122-vultr-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-base.svg)[🧠](results/bm-20241122-3.14.0a2%2B-39e60ae-NOGIL/bm-20241122-vultr-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-base-mem.svg) |
| [2024-11-22](results/bm-20241122-3.14.0a2%2B-39e60ae) | python/39e60aeb3837f1f23d8b | 39e60ae | 1.032x ↑<br>[📄](results/bm-20241122-3.14.0a2%2B-39e60ae/bm-20241122-vultr-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-3.12.6.md)[📈](results/bm-20241122-3.14.0a2%2B-39e60ae/bm-20241122-vultr-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-3.12.6.svg) | 1.004x ↓<br>[📄](results/bm-20241122-3.14.0a2%2B-39e60ae/bm-20241122-vultr-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-3.13.0rc2.md)[📈](results/bm-20241122-3.14.0a2%2B-39e60ae/bm-20241122-vultr-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-3.13.0rc2.svg) | 1.004x ↓<br>[📄](results/bm-20241122-3.14.0a2%2B-39e60ae/bm-20241122-vultr-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-base.md)[📈](results/bm-20241122-3.14.0a2%2B-39e60ae/bm-20241122-vultr-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-base.svg)[🧠](results/bm-20241122-3.14.0a2%2B-39e60ae/bm-20241122-vultr-x86_64-python-39e60aeb3837f1f23d8b-3.14.0a2%2B-39e60ae-vs-base-mem.svg) |
| [2024-11-22](results/bm-20241122-3.14.0a2%2B-26bfc21) | mpage/gh_115999_tlbc_call_ | 26bfc21 | 1.038x ↑<br>[📄](results/bm-20241122-3.14.0a2%2B-26bfc21/bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2%2B-26bfc21-vs-3.12.6.md)[📈](results/bm-20241122-3.14.0a2%2B-26bfc21/bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2%2B-26bfc21-vs-3.12.6.svg) | 1.001x ↑<br>[📄](results/bm-20241122-3.14.0a2%2B-26bfc21/bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2%2B-26bfc21-vs-3.13.0rc2.md)[📈](results/bm-20241122-3.14.0a2%2B-26bfc21/bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2%2B-26bfc21-vs-3.13.0rc2.svg) | 1.001x ↑<br>[📄](results/bm-20241122-3.14.0a2%2B-26bfc21/bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2%2B-26bfc21-vs-base.md)[📈](results/bm-20241122-3.14.0a2%2B-26bfc21/bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2%2B-26bfc21-vs-base.svg)[🧠](results/bm-20241122-3.14.0a2%2B-26bfc21/bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2%2B-26bfc21-vs-base-mem.svg) |
| [2024-11-22](results/bm-20241122-3.14.0a2%2B-26bfc21-NOGIL) | mpage/gh_115999_tlbc_call_ | 26bfc21 (NOGIL) | 1.263x ↓<br>[📄](results/bm-20241122-3.14.0a2%2B-26bfc21-NOGIL/bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2%2B-26bfc21-vs-3.12.6.md)[📈](results/bm-20241122-3.14.0a2%2B-26bfc21-NOGIL/bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2%2B-26bfc21-vs-3.12.6.svg) | 1.288x ↓<br>[📄](results/bm-20241122-3.14.0a2%2B-26bfc21-NOGIL/bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2%2B-26bfc21-vs-3.13.0rc2.md)[📈](results/bm-20241122-3.14.0a2%2B-26bfc21-NOGIL/bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2%2B-26bfc21-vs-3.13.0rc2.svg) | 1.001x ↓<br>[📄](results/bm-20241122-3.14.0a2%2B-26bfc21-NOGIL/bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2%2B-26bfc21-vs-base.md)[📈](results/bm-20241122-3.14.0a2%2B-26bfc21-NOGIL/bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2%2B-26bfc21-vs-base.svg)[🧠](results/bm-20241122-3.14.0a2%2B-26bfc21-NOGIL/bm-20241122-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2%2B-26bfc21-vs-base-mem.svg) |
| [2024-11-22](results/bm-20241122-3.14.0a2%2B-d24a22e-NOGIL) | python/d24a22e9b6377797c3b6 | d24a22e (NOGIL) | 1.263x ↓<br>[📄](results/bm-20241122-3.14.0a2%2B-d24a22e-NOGIL/bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2%2B-d24a22e-vs-3.12.6.md)[📈](results/bm-20241122-3.14.0a2%2B-d24a22e-NOGIL/bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2%2B-d24a22e-vs-3.12.6.svg) | 1.287x ↓<br>[📄](results/bm-20241122-3.14.0a2%2B-d24a22e-NOGIL/bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2%2B-d24a22e-vs-3.13.0rc2.md)[📈](results/bm-20241122-3.14.0a2%2B-d24a22e-NOGIL/bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2%2B-d24a22e-vs-3.13.0rc2.svg) | 1.282x ↓<br>[📄](results/bm-20241122-3.14.0a2%2B-d24a22e-NOGIL/bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2%2B-d24a22e-vs-base.md)[📈](results/bm-20241122-3.14.0a2%2B-d24a22e-NOGIL/bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2%2B-d24a22e-vs-base.svg)[🧠](results/bm-20241122-3.14.0a2%2B-d24a22e-NOGIL/bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2%2B-d24a22e-vs-base-mem.svg) |
| [2024-11-22](results/bm-20241122-3.14.0a2%2B-d24a22e) | python/d24a22e9b6377797c3b6 | d24a22e | 1.037x ↑<br>[📄](results/bm-20241122-3.14.0a2%2B-d24a22e/bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2%2B-d24a22e-vs-3.12.6.md)[📈](results/bm-20241122-3.14.0a2%2B-d24a22e/bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2%2B-d24a22e-vs-3.12.6.svg) | 1.000x ↑<br>[📄](results/bm-20241122-3.14.0a2%2B-d24a22e/bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2%2B-d24a22e-vs-3.13.0rc2.md)[📈](results/bm-20241122-3.14.0a2%2B-d24a22e/bm-20241122-vultr-x86_64-python-d24a22e9b6377797c3b6-3.14.0a2%2B-d24a22e-vs-3.13.0rc2.svg) |  |
| [2024-11-21](results/bm-20241121-3.14.0a2%2B-4c7837f-NOGIL) | mpage/gh_115999_tlbc_call | 4c7837f (NOGIL) | 1.302x ↓<br>[📄](results/bm-20241121-3.14.0a2%2B-4c7837f-NOGIL/bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2%2B-4c7837f-vs-3.12.6.md)[📈](results/bm-20241121-3.14.0a2%2B-4c7837f-NOGIL/bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2%2B-4c7837f-vs-3.12.6.svg) | 1.325x ↓<br>[📄](results/bm-20241121-3.14.0a2%2B-4c7837f-NOGIL/bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2%2B-4c7837f-vs-3.13.0rc2.md)[📈](results/bm-20241121-3.14.0a2%2B-4c7837f-NOGIL/bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2%2B-4c7837f-vs-3.13.0rc2.svg) | 1.031x ↑<br>[📄](results/bm-20241121-3.14.0a2%2B-4c7837f-NOGIL/bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2%2B-4c7837f-vs-base.md)[📈](results/bm-20241121-3.14.0a2%2B-4c7837f-NOGIL/bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2%2B-4c7837f-vs-base.svg)[🧠](results/bm-20241121-3.14.0a2%2B-4c7837f-NOGIL/bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2%2B-4c7837f-vs-base-mem.svg) |
| [2024-11-21](results/bm-20241121-3.14.0a2%2B-09c240f-NOGIL) | python/09c240f20c47db126ad7 | 09c240f (NOGIL) | 1.292x ↓<br>[📄](results/bm-20241121-3.14.0a2%2B-09c240f-NOGIL/bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2%2B-09c240f-vs-3.12.6.md)[📈](results/bm-20241121-3.14.0a2%2B-09c240f-NOGIL/bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2%2B-09c240f-vs-3.12.6.svg) | 1.316x ↓<br>[📄](results/bm-20241121-3.14.0a2%2B-09c240f-NOGIL/bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2%2B-09c240f-vs-3.13.0rc2.md)[📈](results/bm-20241121-3.14.0a2%2B-09c240f-NOGIL/bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2%2B-09c240f-vs-3.13.0rc2.svg) |  |
| [2024-11-20](results/bm-20241120-3.14.0a2%2B-32428cf-NOGIL) | python/32428cf9ea03bce6d64c | 32428cf (NOGIL) | 1.323x ↓<br>[📄](results/bm-20241120-3.14.0a2%2B-32428cf-NOGIL/bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2%2B-32428cf-vs-3.12.6.md)[📈](results/bm-20241120-3.14.0a2%2B-32428cf-NOGIL/bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2%2B-32428cf-vs-3.12.6.svg) | 1.346x ↓<br>[📄](results/bm-20241120-3.14.0a2%2B-32428cf-NOGIL/bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2%2B-32428cf-vs-3.13.0rc2.md)[📈](results/bm-20241120-3.14.0a2%2B-32428cf-NOGIL/bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2%2B-32428cf-vs-3.13.0rc2.svg) | 1.370x ↓<br>[📄](results/bm-20241120-3.14.0a2%2B-32428cf-NOGIL/bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2%2B-32428cf-vs-base.md)[📈](results/bm-20241120-3.14.0a2%2B-32428cf-NOGIL/bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2%2B-32428cf-vs-base.svg)[🧠](results/bm-20241120-3.14.0a2%2B-32428cf-NOGIL/bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2%2B-32428cf-vs-base-mem.svg) |


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
