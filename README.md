# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
[Most recent pystats on main (cf4c4ec)](results/bm-20250201-3.14.0a4%2B-cf4c4ec-PYTHON_UOPS/bm-20250201-linux-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4%2B-cf4c4ec-pystats.md)

## linux x86_64 (linux)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-02-07](results/bm-20250207-3.14.0a4%2B-a191d6f) | python/a191d6f78e10268845b2 | a191d6f | 1.113x ↑<br>[📄](results/bm-20250207-3.14.0a4%2B-a191d6f/bm-20250207-linux-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-3.12.6.md)[📈](results/bm-20250207-3.14.0a4%2B-a191d6f/bm-20250207-linux-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-3.12.6.svg) | 1.070x ↑<br>[📄](results/bm-20250207-3.14.0a4%2B-a191d6f/bm-20250207-linux-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-3.13.0rc2.md)[📈](results/bm-20250207-3.14.0a4%2B-a191d6f/bm-20250207-linux-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-3.13.0rc2.svg) |  |
| [2025-02-07](results/bm-20250207-3.14.0a4%2B-a191d6f-NOGIL) | python/a191d6f78e10268845b2 | a191d6f (NOGIL) | 1.028x ↓<br>[📄](results/bm-20250207-3.14.0a4%2B-a191d6f-NOGIL/bm-20250207-linux-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-3.12.6.md)[📈](results/bm-20250207-3.14.0a4%2B-a191d6f-NOGIL/bm-20250207-linux-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-3.12.6.svg) | 1.064x ↓<br>[📄](results/bm-20250207-3.14.0a4%2B-a191d6f-NOGIL/bm-20250207-linux-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-3.13.0rc2.md)[📈](results/bm-20250207-3.14.0a4%2B-a191d6f-NOGIL/bm-20250207-linux-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-3.13.0rc2.svg) | 1.125x ↓<br>[📄](results/bm-20250207-3.14.0a4%2B-a191d6f-NOGIL/bm-20250207-linux-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-base.md)[📈](results/bm-20250207-3.14.0a4%2B-a191d6f-NOGIL/bm-20250207-linux-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-base.svg)[🧠](results/bm-20250207-3.14.0a4%2B-a191d6f-NOGIL/bm-20250207-linux-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-base-mem.svg) |
| [2025-02-05](results/bm-20250205-3.14.0a4%2B-cdcacec-NOGIL) | python/cdcacec79f7a216c3c98 | cdcacec (NOGIL) | 1.034x ↓<br>[📄](results/bm-20250205-3.14.0a4%2B-cdcacec-NOGIL/bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4%2B-cdcacec-vs-3.12.6.md)[📈](results/bm-20250205-3.14.0a4%2B-cdcacec-NOGIL/bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4%2B-cdcacec-vs-3.12.6.svg) | 1.069x ↓<br>[📄](results/bm-20250205-3.14.0a4%2B-cdcacec-NOGIL/bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4%2B-cdcacec-vs-3.13.0rc2.md)[📈](results/bm-20250205-3.14.0a4%2B-cdcacec-NOGIL/bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4%2B-cdcacec-vs-3.13.0rc2.svg) | 1.132x ↓<br>[📄](results/bm-20250205-3.14.0a4%2B-cdcacec-NOGIL/bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4%2B-cdcacec-vs-base.md)[📈](results/bm-20250205-3.14.0a4%2B-cdcacec-NOGIL/bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4%2B-cdcacec-vs-base.svg)[🧠](results/bm-20250205-3.14.0a4%2B-cdcacec-NOGIL/bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4%2B-cdcacec-vs-base-mem.svg) |
| [2025-02-05](results/bm-20250205-3.14.0a4%2B-cdcacec) | python/cdcacec79f7a216c3c98 | cdcacec | 1.115x ↑<br>[📄](results/bm-20250205-3.14.0a4%2B-cdcacec/bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4%2B-cdcacec-vs-3.12.6.md)[📈](results/bm-20250205-3.14.0a4%2B-cdcacec/bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4%2B-cdcacec-vs-3.12.6.svg) | 1.072x ↑<br>[📄](results/bm-20250205-3.14.0a4%2B-cdcacec/bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4%2B-cdcacec-vs-3.13.0rc2.md)[📈](results/bm-20250205-3.14.0a4%2B-cdcacec/bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4%2B-cdcacec-vs-3.13.0rc2.svg) |  |
| [2025-02-04](results/bm-20250204-3.14.0a4%2B-e41ec8e-NOGIL) | python/e41ec8e18b078024b02a | e41ec8e (NOGIL) | 1.035x ↓<br>[📄](results/bm-20250204-3.14.0a4%2B-e41ec8e-NOGIL/bm-20250204-linux-x86_64-python-e41ec8e18b078024b02a-3.14.0a4%2B-e41ec8e-vs-3.12.6.md)[📈](results/bm-20250204-3.14.0a4%2B-e41ec8e-NOGIL/bm-20250204-linux-x86_64-python-e41ec8e18b078024b02a-3.14.0a4%2B-e41ec8e-vs-3.12.6.svg) | 1.070x ↓<br>[📄](results/bm-20250204-3.14.0a4%2B-e41ec8e-NOGIL/bm-20250204-linux-x86_64-python-e41ec8e18b078024b02a-3.14.0a4%2B-e41ec8e-vs-3.13.0rc2.md)[📈](results/bm-20250204-3.14.0a4%2B-e41ec8e-NOGIL/bm-20250204-linux-x86_64-python-e41ec8e18b078024b02a-3.14.0a4%2B-e41ec8e-vs-3.13.0rc2.svg) | 1.114x ↓<br>[📄](results/bm-20250204-3.14.0a4%2B-e41ec8e-NOGIL/bm-20250204-linux-x86_64-python-e41ec8e18b078024b02a-3.14.0a4%2B-e41ec8e-vs-base.md)[📈](results/bm-20250204-3.14.0a4%2B-e41ec8e-NOGIL/bm-20250204-linux-x86_64-python-e41ec8e18b078024b02a-3.14.0a4%2B-e41ec8e-vs-base.svg)[🧠](results/bm-20250204-3.14.0a4%2B-e41ec8e-NOGIL/bm-20250204-linux-x86_64-python-e41ec8e18b078024b02a-3.14.0a4%2B-e41ec8e-vs-base-mem.svg) |
| [2025-02-04](results/bm-20250204-3.14.0a4%2B-e41ec8e) | python/e41ec8e18b078024b02a | e41ec8e | 1.093x ↑<br>[📄](results/bm-20250204-3.14.0a4%2B-e41ec8e/bm-20250204-linux-x86_64-python-e41ec8e18b078024b02a-3.14.0a4%2B-e41ec8e-vs-3.12.6.md)[📈](results/bm-20250204-3.14.0a4%2B-e41ec8e/bm-20250204-linux-x86_64-python-e41ec8e18b078024b02a-3.14.0a4%2B-e41ec8e-vs-3.12.6.svg) | 1.055x ↑<br>[📄](results/bm-20250204-3.14.0a4%2B-e41ec8e/bm-20250204-linux-x86_64-python-e41ec8e18b078024b02a-3.14.0a4%2B-e41ec8e-vs-3.13.0rc2.md)[📈](results/bm-20250204-3.14.0a4%2B-e41ec8e/bm-20250204-linux-x86_64-python-e41ec8e18b078024b02a-3.14.0a4%2B-e41ec8e-vs-3.13.0rc2.svg) |  |
| [2025-02-03](results/bm-20250203-3.14.0a4%2B-bb5c687) | python/bb5c6875d6e84bf2b4e1 | bb5c687 | 1.104x ↑<br>[📄](results/bm-20250203-3.14.0a4%2B-bb5c687/bm-20250203-linux-x86_64-python-bb5c6875d6e84bf2b4e1-3.14.0a4%2B-bb5c687-vs-3.12.6.md)[📈](results/bm-20250203-3.14.0a4%2B-bb5c687/bm-20250203-linux-x86_64-python-bb5c6875d6e84bf2b4e1-3.14.0a4%2B-bb5c687-vs-3.12.6.svg) | 1.059x ↑<br>[📄](results/bm-20250203-3.14.0a4%2B-bb5c687/bm-20250203-linux-x86_64-python-bb5c6875d6e84bf2b4e1-3.14.0a4%2B-bb5c687-vs-3.13.0rc2.md)[📈](results/bm-20250203-3.14.0a4%2B-bb5c687/bm-20250203-linux-x86_64-python-bb5c6875d6e84bf2b4e1-3.14.0a4%2B-bb5c687-vs-3.13.0rc2.svg) |  |
| [2025-02-03](results/bm-20250203-3.14.0a4%2B-bb5c687-NOGIL) | python/bb5c6875d6e84bf2b4e1 | bb5c687 (NOGIL) | 1.040x ↓<br>[📄](results/bm-20250203-3.14.0a4%2B-bb5c687-NOGIL/bm-20250203-linux-x86_64-python-bb5c6875d6e84bf2b4e1-3.14.0a4%2B-bb5c687-vs-3.12.6.md)[📈](results/bm-20250203-3.14.0a4%2B-bb5c687-NOGIL/bm-20250203-linux-x86_64-python-bb5c6875d6e84bf2b4e1-3.14.0a4%2B-bb5c687-vs-3.12.6.svg) | 1.073x ↓<br>[📄](results/bm-20250203-3.14.0a4%2B-bb5c687-NOGIL/bm-20250203-linux-x86_64-python-bb5c6875d6e84bf2b4e1-3.14.0a4%2B-bb5c687-vs-3.13.0rc2.md)[📈](results/bm-20250203-3.14.0a4%2B-bb5c687-NOGIL/bm-20250203-linux-x86_64-python-bb5c6875d6e84bf2b4e1-3.14.0a4%2B-bb5c687-vs-3.13.0rc2.svg) | 1.125x ↓<br>[📄](results/bm-20250203-3.14.0a4%2B-bb5c687-NOGIL/bm-20250203-linux-x86_64-python-bb5c6875d6e84bf2b4e1-3.14.0a4%2B-bb5c687-vs-base.md)[📈](results/bm-20250203-3.14.0a4%2B-bb5c687-NOGIL/bm-20250203-linux-x86_64-python-bb5c6875d6e84bf2b4e1-3.14.0a4%2B-bb5c687-vs-base.svg)[🧠](results/bm-20250203-3.14.0a4%2B-bb5c687-NOGIL/bm-20250203-linux-x86_64-python-bb5c6875d6e84bf2b4e1-3.14.0a4%2B-bb5c687-vs-base-mem.svg) |

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-02-07](results/bm-20250207-3.14.0a4%2B-a191d6f) | python/a191d6f78e10268845b2 | a191d6f | 1.087x ↑<br>[📄](results/bm-20250207-3.14.0a4%2B-a191d6f/bm-20250207-vultr-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-3.12.6.md)[📈](results/bm-20250207-3.14.0a4%2B-a191d6f/bm-20250207-vultr-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-3.12.6.svg) | 1.048x ↑<br>[📄](results/bm-20250207-3.14.0a4%2B-a191d6f/bm-20250207-vultr-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-3.13.0rc2.md)[📈](results/bm-20250207-3.14.0a4%2B-a191d6f/bm-20250207-vultr-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-3.13.0rc2.svg) |  |
| [2025-02-07](results/bm-20250207-3.14.0a4%2B-a191d6f-NOGIL) | python/a191d6f78e10268845b2 | a191d6f (NOGIL) | 1.046x ↓<br>[📄](results/bm-20250207-3.14.0a4%2B-a191d6f-NOGIL/bm-20250207-vultr-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-3.12.6.md)[📈](results/bm-20250207-3.14.0a4%2B-a191d6f-NOGIL/bm-20250207-vultr-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-3.12.6.svg) | 1.077x ↓<br>[📄](results/bm-20250207-3.14.0a4%2B-a191d6f-NOGIL/bm-20250207-vultr-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-3.13.0rc2.md)[📈](results/bm-20250207-3.14.0a4%2B-a191d6f-NOGIL/bm-20250207-vultr-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-3.13.0rc2.svg) | 1.123x ↓<br>[📄](results/bm-20250207-3.14.0a4%2B-a191d6f-NOGIL/bm-20250207-vultr-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-base.md)[📈](results/bm-20250207-3.14.0a4%2B-a191d6f-NOGIL/bm-20250207-vultr-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-base.svg)[🧠](results/bm-20250207-3.14.0a4%2B-a191d6f-NOGIL/bm-20250207-vultr-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-base-mem.svg) |
| [2025-02-06](results/bm-20250206-3.14.0a4%2B-7bd7810-NOGIL) | mpage/load_fast_borrow | 7bd7810 (NOGIL) | 1.043x ↓<br>[📄](results/bm-20250206-3.14.0a4%2B-7bd7810-NOGIL/bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4%2B-7bd7810-vs-3.12.6.md)[📈](results/bm-20250206-3.14.0a4%2B-7bd7810-NOGIL/bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4%2B-7bd7810-vs-3.12.6.svg) | 1.073x ↓<br>[📄](results/bm-20250206-3.14.0a4%2B-7bd7810-NOGIL/bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4%2B-7bd7810-vs-3.13.0rc2.md)[📈](results/bm-20250206-3.14.0a4%2B-7bd7810-NOGIL/bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4%2B-7bd7810-vs-3.13.0rc2.svg) | 1.008x ↑<br>[📄](results/bm-20250206-3.14.0a4%2B-7bd7810-NOGIL/bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4%2B-7bd7810-vs-base.md)[📈](results/bm-20250206-3.14.0a4%2B-7bd7810-NOGIL/bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4%2B-7bd7810-vs-base.svg)[🧠](results/bm-20250206-3.14.0a4%2B-7bd7810-NOGIL/bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4%2B-7bd7810-vs-base-mem.svg) |
| [2025-02-05](results/bm-20250205-3.14.0a4%2B-7d9a22f-NOGIL) | python/7d9a22f50923309955a2 | 7d9a22f (NOGIL) | 1.047x ↓<br>[📄](results/bm-20250205-3.14.0a4%2B-7d9a22f-NOGIL/bm-20250205-vultr-x86_64-python-7d9a22f50923309955a2-3.14.0a4%2B-7d9a22f-vs-3.12.6.md)[📈](results/bm-20250205-3.14.0a4%2B-7d9a22f-NOGIL/bm-20250205-vultr-x86_64-python-7d9a22f50923309955a2-3.14.0a4%2B-7d9a22f-vs-3.12.6.svg) | 1.078x ↓<br>[📄](results/bm-20250205-3.14.0a4%2B-7d9a22f-NOGIL/bm-20250205-vultr-x86_64-python-7d9a22f50923309955a2-3.14.0a4%2B-7d9a22f-vs-3.13.0rc2.md)[📈](results/bm-20250205-3.14.0a4%2B-7d9a22f-NOGIL/bm-20250205-vultr-x86_64-python-7d9a22f50923309955a2-3.14.0a4%2B-7d9a22f-vs-3.13.0rc2.svg) |  |
| [2025-02-05](results/bm-20250205-3.14.0a4%2B-43173b7-NOGIL) | DinoV/noclock_clear | 43173b7 (NOGIL) | 1.042x ↓<br>[📄](results/bm-20250205-3.14.0a4%2B-43173b7-NOGIL/bm-20250205-vultr-x86_64-DinoV-noclock_clear-3.14.0a4%2B-43173b7-vs-3.12.6.md)[📈](results/bm-20250205-3.14.0a4%2B-43173b7-NOGIL/bm-20250205-vultr-x86_64-DinoV-noclock_clear-3.14.0a4%2B-43173b7-vs-3.12.6.svg) | 1.073x ↓<br>[📄](results/bm-20250205-3.14.0a4%2B-43173b7-NOGIL/bm-20250205-vultr-x86_64-DinoV-noclock_clear-3.14.0a4%2B-43173b7-vs-3.13.0rc2.md)[📈](results/bm-20250205-3.14.0a4%2B-43173b7-NOGIL/bm-20250205-vultr-x86_64-DinoV-noclock_clear-3.14.0a4%2B-43173b7-vs-3.13.0rc2.svg) | 1.001x ↓<br>[📄](results/bm-20250205-3.14.0a4%2B-43173b7-NOGIL/bm-20250205-vultr-x86_64-DinoV-noclock_clear-3.14.0a4%2B-43173b7-vs-base.md)[📈](results/bm-20250205-3.14.0a4%2B-43173b7-NOGIL/bm-20250205-vultr-x86_64-DinoV-noclock_clear-3.14.0a4%2B-43173b7-vs-base.svg)[🧠](results/bm-20250205-3.14.0a4%2B-43173b7-NOGIL/bm-20250205-vultr-x86_64-DinoV-noclock_clear-3.14.0a4%2B-43173b7-vs-base-mem.svg) |
| [2025-02-05](results/bm-20250205-3.14.0a4%2B-ecf15ed-NOGIL) | nascheme/ft_float_consume_inp | ecf15ed (NOGIL) | 1.044x ↓<br>[📄](results/bm-20250205-3.14.0a4%2B-ecf15ed-NOGIL/bm-20250205-vultr-x86_64-nascheme-ft_float_consume_inp-3.14.0a4%2B-ecf15ed-vs-3.12.6.md)[📈](results/bm-20250205-3.14.0a4%2B-ecf15ed-NOGIL/bm-20250205-vultr-x86_64-nascheme-ft_float_consume_inp-3.14.0a4%2B-ecf15ed-vs-3.12.6.svg) | 1.075x ↓<br>[📄](results/bm-20250205-3.14.0a4%2B-ecf15ed-NOGIL/bm-20250205-vultr-x86_64-nascheme-ft_float_consume_inp-3.14.0a4%2B-ecf15ed-vs-3.13.0rc2.md)[📈](results/bm-20250205-3.14.0a4%2B-ecf15ed-NOGIL/bm-20250205-vultr-x86_64-nascheme-ft_float_consume_inp-3.14.0a4%2B-ecf15ed-vs-3.13.0rc2.svg) | 1.002x ↑<br>[📄](results/bm-20250205-3.14.0a4%2B-ecf15ed-NOGIL/bm-20250205-vultr-x86_64-nascheme-ft_float_consume_inp-3.14.0a4%2B-ecf15ed-vs-base.md)[📈](results/bm-20250205-3.14.0a4%2B-ecf15ed-NOGIL/bm-20250205-vultr-x86_64-nascheme-ft_float_consume_inp-3.14.0a4%2B-ecf15ed-vs-base.svg)[🧠](results/bm-20250205-3.14.0a4%2B-ecf15ed-NOGIL/bm-20250205-vultr-x86_64-nascheme-ft_float_consume_inp-3.14.0a4%2B-ecf15ed-vs-base-mem.svg) |
| [2025-02-05](results/bm-20250205-3.14.0a4%2B-d7cb09f-NOGIL) | wrongnull/ft_new_reference_dat | d7cb09f (NOGIL) | 1.042x ↓<br>[📄](results/bm-20250205-3.14.0a4%2B-d7cb09f-NOGIL/bm-20250205-vultr-x86_64-wrongnull-ft_new_reference_dat-3.14.0a4%2B-d7cb09f-vs-3.12.6.md)[📈](results/bm-20250205-3.14.0a4%2B-d7cb09f-NOGIL/bm-20250205-vultr-x86_64-wrongnull-ft_new_reference_dat-3.14.0a4%2B-d7cb09f-vs-3.12.6.svg) | 1.073x ↓<br>[📄](results/bm-20250205-3.14.0a4%2B-d7cb09f-NOGIL/bm-20250205-vultr-x86_64-wrongnull-ft_new_reference_dat-3.14.0a4%2B-d7cb09f-vs-3.13.0rc2.md)[📈](results/bm-20250205-3.14.0a4%2B-d7cb09f-NOGIL/bm-20250205-vultr-x86_64-wrongnull-ft_new_reference_dat-3.14.0a4%2B-d7cb09f-vs-3.13.0rc2.svg) | 1.001x ↑<br>[📄](results/bm-20250205-3.14.0a4%2B-d7cb09f-NOGIL/bm-20250205-vultr-x86_64-wrongnull-ft_new_reference_dat-3.14.0a4%2B-d7cb09f-vs-base.md)[📈](results/bm-20250205-3.14.0a4%2B-d7cb09f-NOGIL/bm-20250205-vultr-x86_64-wrongnull-ft_new_reference_dat-3.14.0a4%2B-d7cb09f-vs-base.svg)[🧠](results/bm-20250205-3.14.0a4%2B-d7cb09f-NOGIL/bm-20250205-vultr-x86_64-wrongnull-ft_new_reference_dat-3.14.0a4%2B-d7cb09f-vs-base-mem.svg) |
| [2025-02-05](results/bm-20250205-3.14.0a4%2B-cdcacec-NOGIL) | python/cdcacec79f7a216c3c98 | cdcacec (NOGIL) | 1.042x ↓<br>[📄](results/bm-20250205-3.14.0a4%2B-cdcacec-NOGIL/bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4%2B-cdcacec-vs-3.12.6.md)[📈](results/bm-20250205-3.14.0a4%2B-cdcacec-NOGIL/bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4%2B-cdcacec-vs-3.12.6.svg) | 1.073x ↓<br>[📄](results/bm-20250205-3.14.0a4%2B-cdcacec-NOGIL/bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4%2B-cdcacec-vs-3.13.0rc2.md)[📈](results/bm-20250205-3.14.0a4%2B-cdcacec-NOGIL/bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4%2B-cdcacec-vs-3.13.0rc2.svg) | 1.119x ↓<br>[📄](results/bm-20250205-3.14.0a4%2B-cdcacec-NOGIL/bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4%2B-cdcacec-vs-base.md)[📈](results/bm-20250205-3.14.0a4%2B-cdcacec-NOGIL/bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4%2B-cdcacec-vs-base.svg)[🧠](results/bm-20250205-3.14.0a4%2B-cdcacec-NOGIL/bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4%2B-cdcacec-vs-base-mem.svg) |
| [2025-02-05](results/bm-20250205-3.14.0a4%2B-cdcacec) | python/cdcacec79f7a216c3c98 | cdcacec | 1.085x ↑<br>[📄](results/bm-20250205-3.14.0a4%2B-cdcacec/bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4%2B-cdcacec-vs-3.12.6.md)[📈](results/bm-20250205-3.14.0a4%2B-cdcacec/bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4%2B-cdcacec-vs-3.12.6.svg) | 1.046x ↑<br>[📄](results/bm-20250205-3.14.0a4%2B-cdcacec/bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4%2B-cdcacec-vs-3.13.0rc2.md)[📈](results/bm-20250205-3.14.0a4%2B-cdcacec/bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4%2B-cdcacec-vs-3.13.0rc2.svg) |  |
| [2025-02-05](results/bm-20250205-3.14.0a4%2B-cbd6459-NOGIL) | DinoV/hash_type | cbd6459 (NOGIL) | 1.050x ↓<br>[📄](results/bm-20250205-3.14.0a4%2B-cbd6459-NOGIL/bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4%2B-cbd6459-vs-3.12.6.md)[📈](results/bm-20250205-3.14.0a4%2B-cbd6459-NOGIL/bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4%2B-cbd6459-vs-3.12.6.svg) | 1.080x ↓<br>[📄](results/bm-20250205-3.14.0a4%2B-cbd6459-NOGIL/bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4%2B-cbd6459-vs-3.13.0rc2.md)[📈](results/bm-20250205-3.14.0a4%2B-cbd6459-NOGIL/bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4%2B-cbd6459-vs-3.13.0rc2.svg) | 1.008x ↓<br>[📄](results/bm-20250205-3.14.0a4%2B-cbd6459-NOGIL/bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4%2B-cbd6459-vs-base.md)[📈](results/bm-20250205-3.14.0a4%2B-cbd6459-NOGIL/bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4%2B-cbd6459-vs-base.svg)[🧠](results/bm-20250205-3.14.0a4%2B-cbd6459-NOGIL/bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4%2B-cbd6459-vs-base-mem.svg) |
| [2025-02-04](results/bm-20250204-3.14.0a4%2B-e41ec8e-NOGIL) | python/e41ec8e18b078024b02a | e41ec8e (NOGIL) | 1.051x ↓<br>[📄](results/bm-20250204-3.14.0a4%2B-e41ec8e-NOGIL/bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4%2B-e41ec8e-vs-3.12.6.md)[📈](results/bm-20250204-3.14.0a4%2B-e41ec8e-NOGIL/bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4%2B-e41ec8e-vs-3.12.6.svg) | 1.081x ↓<br>[📄](results/bm-20250204-3.14.0a4%2B-e41ec8e-NOGIL/bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4%2B-e41ec8e-vs-3.13.0rc2.md)[📈](results/bm-20250204-3.14.0a4%2B-e41ec8e-NOGIL/bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4%2B-e41ec8e-vs-3.13.0rc2.svg) | 1.131x ↓<br>[📄](results/bm-20250204-3.14.0a4%2B-e41ec8e-NOGIL/bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4%2B-e41ec8e-vs-base.md)[📈](results/bm-20250204-3.14.0a4%2B-e41ec8e-NOGIL/bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4%2B-e41ec8e-vs-base.svg)[🧠](results/bm-20250204-3.14.0a4%2B-e41ec8e-NOGIL/bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4%2B-e41ec8e-vs-base-mem.svg) |
| [2025-02-04](results/bm-20250204-3.14.0a4%2B-e41ec8e) | python/e41ec8e18b078024b02a | e41ec8e | 1.092x ↑<br>[📄](results/bm-20250204-3.14.0a4%2B-e41ec8e/bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4%2B-e41ec8e-vs-3.12.6.md)[📈](results/bm-20250204-3.14.0a4%2B-e41ec8e/bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4%2B-e41ec8e-vs-3.12.6.svg) | 1.053x ↑<br>[📄](results/bm-20250204-3.14.0a4%2B-e41ec8e/bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4%2B-e41ec8e-vs-3.13.0rc2.md)[📈](results/bm-20250204-3.14.0a4%2B-e41ec8e/bm-20250204-vultr-x86_64-python-e41ec8e18b078024b02a-3.14.0a4%2B-e41ec8e-vs-3.13.0rc2.svg) |  |
| [2025-02-04](results/bm-20250204-3.14.0a4%2B-08975df-NOGIL) | DinoV/noclock_clear | 08975df (NOGIL) | 1.054x ↓<br>[📄](results/bm-20250204-3.14.0a4%2B-08975df-NOGIL/bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4%2B-08975df-vs-3.12.6.md)[📈](results/bm-20250204-3.14.0a4%2B-08975df-NOGIL/bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4%2B-08975df-vs-3.12.6.svg) | 1.079x ↓<br>[📄](results/bm-20250204-3.14.0a4%2B-08975df-NOGIL/bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4%2B-08975df-vs-3.13.0rc2.md)[📈](results/bm-20250204-3.14.0a4%2B-08975df-NOGIL/bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4%2B-08975df-vs-3.13.0rc2.svg) | 1.012x ↓<br>[📄](results/bm-20250204-3.14.0a4%2B-08975df-NOGIL/bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4%2B-08975df-vs-base.md)[📈](results/bm-20250204-3.14.0a4%2B-08975df-NOGIL/bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4%2B-08975df-vs-base.svg)[🧠](results/bm-20250204-3.14.0a4%2B-08975df-NOGIL/bm-20250204-vultr-x86_64-DinoV-noclock_clear-3.14.0a4%2B-08975df-vs-base-mem.svg) |
| [2025-02-03](results/bm-20250203-3.14.0a4%2B-bb5c687) | python/bb5c6875d6e84bf2b4e1 | bb5c687 | 1.100x ↑<br>[📄](results/bm-20250203-3.14.0a4%2B-bb5c687/bm-20250203-vultr-x86_64-python-bb5c6875d6e84bf2b4e1-3.14.0a4%2B-bb5c687-vs-3.12.6.md)[📈](results/bm-20250203-3.14.0a4%2B-bb5c687/bm-20250203-vultr-x86_64-python-bb5c6875d6e84bf2b4e1-3.14.0a4%2B-bb5c687-vs-3.12.6.svg) | 1.061x ↑<br>[📄](results/bm-20250203-3.14.0a4%2B-bb5c687/bm-20250203-vultr-x86_64-python-bb5c6875d6e84bf2b4e1-3.14.0a4%2B-bb5c687-vs-3.13.0rc2.md)[📈](results/bm-20250203-3.14.0a4%2B-bb5c687/bm-20250203-vultr-x86_64-python-bb5c6875d6e84bf2b4e1-3.14.0a4%2B-bb5c687-vs-3.13.0rc2.svg) |  |
| [2025-02-03](results/bm-20250203-3.14.0a4%2B-bb5c687-NOGIL) | python/bb5c6875d6e84bf2b4e1 | bb5c687 (NOGIL) | 1.043x ↓<br>[📄](results/bm-20250203-3.14.0a4%2B-bb5c687-NOGIL/bm-20250203-vultr-x86_64-python-bb5c6875d6e84bf2b4e1-3.14.0a4%2B-bb5c687-vs-3.12.6.md)[📈](results/bm-20250203-3.14.0a4%2B-bb5c687-NOGIL/bm-20250203-vultr-x86_64-python-bb5c6875d6e84bf2b4e1-3.14.0a4%2B-bb5c687-vs-3.12.6.svg) | 1.074x ↓<br>[📄](results/bm-20250203-3.14.0a4%2B-bb5c687-NOGIL/bm-20250203-vultr-x86_64-python-bb5c6875d6e84bf2b4e1-3.14.0a4%2B-bb5c687-vs-3.13.0rc2.md)[📈](results/bm-20250203-3.14.0a4%2B-bb5c687-NOGIL/bm-20250203-vultr-x86_64-python-bb5c6875d6e84bf2b4e1-3.14.0a4%2B-bb5c687-vs-3.13.0rc2.svg) | 1.130x ↓<br>[📄](results/bm-20250203-3.14.0a4%2B-bb5c687-NOGIL/bm-20250203-vultr-x86_64-python-bb5c6875d6e84bf2b4e1-3.14.0a4%2B-bb5c687-vs-base.md)[📈](results/bm-20250203-3.14.0a4%2B-bb5c687-NOGIL/bm-20250203-vultr-x86_64-python-bb5c6875d6e84bf2b4e1-3.14.0a4%2B-bb5c687-vs-base.svg)[🧠](results/bm-20250203-3.14.0a4%2B-bb5c687-NOGIL/bm-20250203-vultr-x86_64-python-bb5c6875d6e84bf2b4e1-3.14.0a4%2B-bb5c687-vs-base-mem.svg) |
| [2025-02-03](results/bm-20250203-3.14.0a4%2B-75b628a-NOGIL) | python/75b628adebd4594529da | 75b628a (NOGIL) | 1.043x ↓<br>[📄](results/bm-20250203-3.14.0a4%2B-75b628a-NOGIL/bm-20250203-vultr-x86_64-python-75b628adebd4594529da-3.14.0a4%2B-75b628a-vs-3.12.6.md)[📈](results/bm-20250203-3.14.0a4%2B-75b628a-NOGIL/bm-20250203-vultr-x86_64-python-75b628adebd4594529da-3.14.0a4%2B-75b628a-vs-3.12.6.svg) | 1.074x ↓<br>[📄](results/bm-20250203-3.14.0a4%2B-75b628a-NOGIL/bm-20250203-vultr-x86_64-python-75b628adebd4594529da-3.14.0a4%2B-75b628a-vs-3.13.0rc2.md)[📈](results/bm-20250203-3.14.0a4%2B-75b628a-NOGIL/bm-20250203-vultr-x86_64-python-75b628adebd4594529da-3.14.0a4%2B-75b628a-vs-3.13.0rc2.svg) | 1.016x ↓<br>[📄](results/bm-20250203-3.14.0a4%2B-75b628a-NOGIL/bm-20250203-vultr-x86_64-python-75b628adebd4594529da-3.14.0a4%2B-75b628a-vs-base.md)[📈](results/bm-20250203-3.14.0a4%2B-75b628a-NOGIL/bm-20250203-vultr-x86_64-python-75b628adebd4594529da-3.14.0a4%2B-75b628a-vs-base.svg)[🧠](results/bm-20250203-3.14.0a4%2B-75b628a-NOGIL/bm-20250203-vultr-x86_64-python-75b628adebd4594529da-3.14.0a4%2B-75b628a-vs-base-mem.svg) |
| [2025-02-03](results/bm-20250203-3.14.0a4%2B-808071b-NOGIL) | python/808071b994370886a169 | 808071b (NOGIL) | 1.027x ↓<br>[📄](results/bm-20250203-3.14.0a4%2B-808071b-NOGIL/bm-20250203-vultr-x86_64-python-808071b994370886a169-3.14.0a4%2B-808071b-vs-3.12.6.md)[📈](results/bm-20250203-3.14.0a4%2B-808071b-NOGIL/bm-20250203-vultr-x86_64-python-808071b994370886a169-3.14.0a4%2B-808071b-vs-3.12.6.svg) | 1.058x ↓<br>[📄](results/bm-20250203-3.14.0a4%2B-808071b-NOGIL/bm-20250203-vultr-x86_64-python-808071b994370886a169-3.14.0a4%2B-808071b-vs-3.13.0rc2.md)[📈](results/bm-20250203-3.14.0a4%2B-808071b-NOGIL/bm-20250203-vultr-x86_64-python-808071b994370886a169-3.14.0a4%2B-808071b-vs-3.13.0rc2.svg) |  |
| [2025-01-29](results/bm-20250129-3.14.0a4%2B-49f2465-NOGIL) | python/49f24650e45414568724 | 49f2465 (NOGIL) | 1.041x ↓<br>[📄](results/bm-20250129-3.14.0a4%2B-49f2465-NOGIL/bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4%2B-49f2465-vs-3.12.6.md)[📈](results/bm-20250129-3.14.0a4%2B-49f2465-NOGIL/bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4%2B-49f2465-vs-3.12.6.svg) | 1.073x ↓<br>[📄](results/bm-20250129-3.14.0a4%2B-49f2465-NOGIL/bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4%2B-49f2465-vs-3.13.0rc2.md)[📈](results/bm-20250129-3.14.0a4%2B-49f2465-NOGIL/bm-20250129-vultr-x86_64-python-49f24650e45414568724-3.14.0a4%2B-49f2465-vs-3.13.0rc2.svg) |  |


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
