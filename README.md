# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
[Most recent pystats on main (29f8a67)](results/bm-20250208-3.14.0a4%2B-29f8a67-PYTHON_UOPS/bm-20250208-linux-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-pystats.md)

## linux x86_64 (linux)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-02-10](results/bm-20250210-3.14.0a4%2B-7e6ee50) | python/7e6ee50b6b8c760bcefb | 7e6ee50 | 1.111x ↑<br>[📄](results/bm-20250210-3.14.0a4%2B-7e6ee50/bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-3.12.6.md)[📈](results/bm-20250210-3.14.0a4%2B-7e6ee50/bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-3.12.6.svg) | 1.073x ↑<br>[📄](results/bm-20250210-3.14.0a4%2B-7e6ee50/bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-3.13.0rc2.md)[📈](results/bm-20250210-3.14.0a4%2B-7e6ee50/bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-3.13.0rc2.svg) |  |
| [2025-02-10](results/bm-20250210-3.14.0a4%2B-7e6ee50-NOGIL) | python/7e6ee50b6b8c760bcefb | 7e6ee50 (NOGIL) | 1.020x ↓<br>[📄](results/bm-20250210-3.14.0a4%2B-7e6ee50-NOGIL/bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-3.12.6.md)[📈](results/bm-20250210-3.14.0a4%2B-7e6ee50-NOGIL/bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-3.12.6.svg) | 1.056x ↓<br>[📄](results/bm-20250210-3.14.0a4%2B-7e6ee50-NOGIL/bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-3.13.0rc2.md)[📈](results/bm-20250210-3.14.0a4%2B-7e6ee50-NOGIL/bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-3.13.0rc2.svg) | 1.116x ↓<br>[📄](results/bm-20250210-3.14.0a4%2B-7e6ee50-NOGIL/bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-base.md)[📈](results/bm-20250210-3.14.0a4%2B-7e6ee50-NOGIL/bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-base.svg)[🧠](results/bm-20250210-3.14.0a4%2B-7e6ee50-NOGIL/bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-base-mem.svg) |
| [2025-02-08](results/bm-20250208-3.14.0a4%2B-29f8a67) | python/29f8a67ae00081a36fdc | 29f8a67 | 1.149x ↑<br>[📄](results/bm-20250208-3.14.0a4%2B-29f8a67/bm-20250208-linux-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-3.12.6.md)[📈](results/bm-20250208-3.14.0a4%2B-29f8a67/bm-20250208-linux-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-3.12.6.svg) | 1.104x ↑<br>[📄](results/bm-20250208-3.14.0a4%2B-29f8a67/bm-20250208-linux-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-3.13.0rc2.md)[📈](results/bm-20250208-3.14.0a4%2B-29f8a67/bm-20250208-linux-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-3.13.0rc2.svg) |  |
| [2025-02-08](results/bm-20250208-3.14.0a4%2B-29f8a67-NOGIL) | python/29f8a67ae00081a36fdc | 29f8a67 (NOGIL) | 1.003x ↑<br>[📄](results/bm-20250208-3.14.0a4%2B-29f8a67-NOGIL/bm-20250208-linux-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-3.12.6.md)[📈](results/bm-20250208-3.14.0a4%2B-29f8a67-NOGIL/bm-20250208-linux-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-3.12.6.svg) | 1.034x ↓<br>[📄](results/bm-20250208-3.14.0a4%2B-29f8a67-NOGIL/bm-20250208-linux-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-3.13.0rc2.md)[📈](results/bm-20250208-3.14.0a4%2B-29f8a67-NOGIL/bm-20250208-linux-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-3.13.0rc2.svg) | 1.123x ↓<br>[📄](results/bm-20250208-3.14.0a4%2B-29f8a67-NOGIL/bm-20250208-linux-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-base.md)[📈](results/bm-20250208-3.14.0a4%2B-29f8a67-NOGIL/bm-20250208-linux-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-base.svg)[🧠](results/bm-20250208-3.14.0a4%2B-29f8a67-NOGIL/bm-20250208-linux-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-base-mem.svg) |
| [2025-02-07](results/bm-20250207-3.14.0a4%2B-a1417b2-NOGIL) | python/a1417b211f0bb9582b00 | a1417b2 (NOGIL) | 1.004x ↑<br>[📄](results/bm-20250207-3.14.0a4%2B-a1417b2-NOGIL/bm-20250207-linux-x86_64-python-a1417b211f0bb9582b00-3.14.0a4%2B-a1417b2-vs-3.12.6.md)[📈](results/bm-20250207-3.14.0a4%2B-a1417b2-NOGIL/bm-20250207-linux-x86_64-python-a1417b211f0bb9582b00-3.14.0a4%2B-a1417b2-vs-3.12.6.svg) | 1.032x ↓<br>[📄](results/bm-20250207-3.14.0a4%2B-a1417b2-NOGIL/bm-20250207-linux-x86_64-python-a1417b211f0bb9582b00-3.14.0a4%2B-a1417b2-vs-3.13.0rc2.md)[📈](results/bm-20250207-3.14.0a4%2B-a1417b2-NOGIL/bm-20250207-linux-x86_64-python-a1417b211f0bb9582b00-3.14.0a4%2B-a1417b2-vs-3.13.0rc2.svg) | 1.117x ↓<br>[📄](results/bm-20250207-3.14.0a4%2B-a1417b2-NOGIL/bm-20250207-linux-x86_64-python-a1417b211f0bb9582b00-3.14.0a4%2B-a1417b2-vs-base.md)[📈](results/bm-20250207-3.14.0a4%2B-a1417b2-NOGIL/bm-20250207-linux-x86_64-python-a1417b211f0bb9582b00-3.14.0a4%2B-a1417b2-vs-base.svg)[🧠](results/bm-20250207-3.14.0a4%2B-a1417b2-NOGIL/bm-20250207-linux-x86_64-python-a1417b211f0bb9582b00-3.14.0a4%2B-a1417b2-vs-base-mem.svg) |
| [2025-02-07](results/bm-20250207-3.14.0a4%2B-a1417b2) | python/a1417b211f0bb9582b00 | a1417b2 | 1.135x ↑<br>[📄](results/bm-20250207-3.14.0a4%2B-a1417b2/bm-20250207-linux-x86_64-python-a1417b211f0bb9582b00-3.14.0a4%2B-a1417b2-vs-3.12.6.md)[📈](results/bm-20250207-3.14.0a4%2B-a1417b2/bm-20250207-linux-x86_64-python-a1417b211f0bb9582b00-3.14.0a4%2B-a1417b2-vs-3.12.6.svg) | 1.089x ↑<br>[📄](results/bm-20250207-3.14.0a4%2B-a1417b2/bm-20250207-linux-x86_64-python-a1417b211f0bb9582b00-3.14.0a4%2B-a1417b2-vs-3.13.0rc2.md)[📈](results/bm-20250207-3.14.0a4%2B-a1417b2/bm-20250207-linux-x86_64-python-a1417b211f0bb9582b00-3.14.0a4%2B-a1417b2-vs-3.13.0rc2.svg) |  |
| [2025-02-07](results/bm-20250207-3.14.0a4%2B-a191d6f) | python/a191d6f78e10268845b2 | a191d6f | 1.113x ↑<br>[📄](results/bm-20250207-3.14.0a4%2B-a191d6f/bm-20250207-linux-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-3.12.6.md)[📈](results/bm-20250207-3.14.0a4%2B-a191d6f/bm-20250207-linux-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-3.12.6.svg) | 1.070x ↑<br>[📄](results/bm-20250207-3.14.0a4%2B-a191d6f/bm-20250207-linux-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-3.13.0rc2.md)[📈](results/bm-20250207-3.14.0a4%2B-a191d6f/bm-20250207-linux-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-3.13.0rc2.svg) |  |
| [2025-02-07](results/bm-20250207-3.14.0a4%2B-a191d6f-NOGIL) | python/a191d6f78e10268845b2 | a191d6f (NOGIL) | 1.028x ↓<br>[📄](results/bm-20250207-3.14.0a4%2B-a191d6f-NOGIL/bm-20250207-linux-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-3.12.6.md)[📈](results/bm-20250207-3.14.0a4%2B-a191d6f-NOGIL/bm-20250207-linux-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-3.12.6.svg) | 1.064x ↓<br>[📄](results/bm-20250207-3.14.0a4%2B-a191d6f-NOGIL/bm-20250207-linux-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-3.13.0rc2.md)[📈](results/bm-20250207-3.14.0a4%2B-a191d6f-NOGIL/bm-20250207-linux-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-3.13.0rc2.svg) | 1.125x ↓<br>[📄](results/bm-20250207-3.14.0a4%2B-a191d6f-NOGIL/bm-20250207-linux-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-base.md)[📈](results/bm-20250207-3.14.0a4%2B-a191d6f-NOGIL/bm-20250207-linux-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-base.svg)[🧠](results/bm-20250207-3.14.0a4%2B-a191d6f-NOGIL/bm-20250207-linux-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-base-mem.svg) |

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-02-10](results/bm-20250210-3.14.0a4%2B-7e6ee50) | python/7e6ee50b6b8c760bcefb | 7e6ee50 | 1.097x ↑<br>[📄](results/bm-20250210-3.14.0a4%2B-7e6ee50/bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-3.12.6.md)[📈](results/bm-20250210-3.14.0a4%2B-7e6ee50/bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-3.12.6.svg) | 1.058x ↑<br>[📄](results/bm-20250210-3.14.0a4%2B-7e6ee50/bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-3.13.0rc2.md)[📈](results/bm-20250210-3.14.0a4%2B-7e6ee50/bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-3.13.0rc2.svg) |  |
| [2025-02-10](results/bm-20250210-3.14.0a4%2B-7e6ee50-NOGIL) | python/7e6ee50b6b8c760bcefb | 7e6ee50 (NOGIL) | 1.044x ↓<br>[📄](results/bm-20250210-3.14.0a4%2B-7e6ee50-NOGIL/bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-3.12.6.md)[📈](results/bm-20250210-3.14.0a4%2B-7e6ee50-NOGIL/bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-3.12.6.svg) | 1.075x ↓<br>[📄](results/bm-20250210-3.14.0a4%2B-7e6ee50-NOGIL/bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-3.13.0rc2.md)[📈](results/bm-20250210-3.14.0a4%2B-7e6ee50-NOGIL/bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-3.13.0rc2.svg) | 1.129x ↓<br>[📄](results/bm-20250210-3.14.0a4%2B-7e6ee50-NOGIL/bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-base.md)[📈](results/bm-20250210-3.14.0a4%2B-7e6ee50-NOGIL/bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-base.svg)[🧠](results/bm-20250210-3.14.0a4%2B-7e6ee50-NOGIL/bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-base-mem.svg) |
| [2025-02-08](results/bm-20250208-3.14.0a4%2B-29f8a67) | python/29f8a67ae00081a36fdc | 29f8a67 | 1.096x ↑<br>[📄](results/bm-20250208-3.14.0a4%2B-29f8a67/bm-20250208-vultr-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-3.12.6.md)[📈](results/bm-20250208-3.14.0a4%2B-29f8a67/bm-20250208-vultr-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-3.12.6.svg) | 1.057x ↑<br>[📄](results/bm-20250208-3.14.0a4%2B-29f8a67/bm-20250208-vultr-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-3.13.0rc2.md)[📈](results/bm-20250208-3.14.0a4%2B-29f8a67/bm-20250208-vultr-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-3.13.0rc2.svg) |  |
| [2025-02-08](results/bm-20250208-3.14.0a4%2B-29f8a67-NOGIL) | python/29f8a67ae00081a36fdc | 29f8a67 (NOGIL) | 1.048x ↓<br>[📄](results/bm-20250208-3.14.0a4%2B-29f8a67-NOGIL/bm-20250208-vultr-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-3.12.6.md)[📈](results/bm-20250208-3.14.0a4%2B-29f8a67-NOGIL/bm-20250208-vultr-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-3.12.6.svg) | 1.079x ↓<br>[📄](results/bm-20250208-3.14.0a4%2B-29f8a67-NOGIL/bm-20250208-vultr-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-3.13.0rc2.md)[📈](results/bm-20250208-3.14.0a4%2B-29f8a67-NOGIL/bm-20250208-vultr-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-3.13.0rc2.svg) | 1.132x ↓<br>[📄](results/bm-20250208-3.14.0a4%2B-29f8a67-NOGIL/bm-20250208-vultr-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-base.md)[📈](results/bm-20250208-3.14.0a4%2B-29f8a67-NOGIL/bm-20250208-vultr-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-base.svg)[🧠](results/bm-20250208-3.14.0a4%2B-29f8a67-NOGIL/bm-20250208-vultr-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-base-mem.svg) |
| [2025-02-07](results/bm-20250207-3.14.0a4%2B-a1417b2-NOGIL) | python/a1417b211f0bb9582b00 | a1417b2 (NOGIL) | 1.049x ↓<br>[📄](results/bm-20250207-3.14.0a4%2B-a1417b2-NOGIL/bm-20250207-vultr-x86_64-python-a1417b211f0bb9582b00-3.14.0a4%2B-a1417b2-vs-3.12.6.md)[📈](results/bm-20250207-3.14.0a4%2B-a1417b2-NOGIL/bm-20250207-vultr-x86_64-python-a1417b211f0bb9582b00-3.14.0a4%2B-a1417b2-vs-3.12.6.svg) | 1.080x ↓<br>[📄](results/bm-20250207-3.14.0a4%2B-a1417b2-NOGIL/bm-20250207-vultr-x86_64-python-a1417b211f0bb9582b00-3.14.0a4%2B-a1417b2-vs-3.13.0rc2.md)[📈](results/bm-20250207-3.14.0a4%2B-a1417b2-NOGIL/bm-20250207-vultr-x86_64-python-a1417b211f0bb9582b00-3.14.0a4%2B-a1417b2-vs-3.13.0rc2.svg) | 1.138x ↓<br>[📄](results/bm-20250207-3.14.0a4%2B-a1417b2-NOGIL/bm-20250207-vultr-x86_64-python-a1417b211f0bb9582b00-3.14.0a4%2B-a1417b2-vs-base.md)[📈](results/bm-20250207-3.14.0a4%2B-a1417b2-NOGIL/bm-20250207-vultr-x86_64-python-a1417b211f0bb9582b00-3.14.0a4%2B-a1417b2-vs-base.svg)[🧠](results/bm-20250207-3.14.0a4%2B-a1417b2-NOGIL/bm-20250207-vultr-x86_64-python-a1417b211f0bb9582b00-3.14.0a4%2B-a1417b2-vs-base-mem.svg) |
| [2025-02-07](results/bm-20250207-3.14.0a4%2B-a1417b2) | python/a1417b211f0bb9582b00 | a1417b2 | 1.103x ↑<br>[📄](results/bm-20250207-3.14.0a4%2B-a1417b2/bm-20250207-vultr-x86_64-python-a1417b211f0bb9582b00-3.14.0a4%2B-a1417b2-vs-3.12.6.md)[📈](results/bm-20250207-3.14.0a4%2B-a1417b2/bm-20250207-vultr-x86_64-python-a1417b211f0bb9582b00-3.14.0a4%2B-a1417b2-vs-3.12.6.svg) | 1.064x ↑<br>[📄](results/bm-20250207-3.14.0a4%2B-a1417b2/bm-20250207-vultr-x86_64-python-a1417b211f0bb9582b00-3.14.0a4%2B-a1417b2-vs-3.13.0rc2.md)[📈](results/bm-20250207-3.14.0a4%2B-a1417b2/bm-20250207-vultr-x86_64-python-a1417b211f0bb9582b00-3.14.0a4%2B-a1417b2-vs-3.13.0rc2.svg) |  |
| [2025-02-07](results/bm-20250207-3.14.0a4%2B-a191d6f) | python/a191d6f78e10268845b2 | a191d6f | 1.087x ↑<br>[📄](results/bm-20250207-3.14.0a4%2B-a191d6f/bm-20250207-vultr-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-3.12.6.md)[📈](results/bm-20250207-3.14.0a4%2B-a191d6f/bm-20250207-vultr-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-3.12.6.svg) | 1.048x ↑<br>[📄](results/bm-20250207-3.14.0a4%2B-a191d6f/bm-20250207-vultr-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-3.13.0rc2.md)[📈](results/bm-20250207-3.14.0a4%2B-a191d6f/bm-20250207-vultr-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-3.13.0rc2.svg) |  |
| [2025-02-07](results/bm-20250207-3.14.0a4%2B-a191d6f-NOGIL) | python/a191d6f78e10268845b2 | a191d6f (NOGIL) | 1.046x ↓<br>[📄](results/bm-20250207-3.14.0a4%2B-a191d6f-NOGIL/bm-20250207-vultr-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-3.12.6.md)[📈](results/bm-20250207-3.14.0a4%2B-a191d6f-NOGIL/bm-20250207-vultr-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-3.12.6.svg) | 1.077x ↓<br>[📄](results/bm-20250207-3.14.0a4%2B-a191d6f-NOGIL/bm-20250207-vultr-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-3.13.0rc2.md)[📈](results/bm-20250207-3.14.0a4%2B-a191d6f-NOGIL/bm-20250207-vultr-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-3.13.0rc2.svg) | 1.123x ↓<br>[📄](results/bm-20250207-3.14.0a4%2B-a191d6f-NOGIL/bm-20250207-vultr-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-base.md)[📈](results/bm-20250207-3.14.0a4%2B-a191d6f-NOGIL/bm-20250207-vultr-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-base.svg)[🧠](results/bm-20250207-3.14.0a4%2B-a191d6f-NOGIL/bm-20250207-vultr-x86_64-python-a191d6f78e10268845b2-3.14.0a4%2B-a191d6f-vs-base-mem.svg) |
| [2025-02-06](results/bm-20250206-3.14.0a4%2B-b0fcd85-NOGIL) | mpage/load_fast_borrow | b0fcd85 (NOGIL) | 1.038x ↓<br>[📄](results/bm-20250206-3.14.0a4%2B-b0fcd85-NOGIL/bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4%2B-b0fcd85-vs-3.12.6.md)[📈](results/bm-20250206-3.14.0a4%2B-b0fcd85-NOGIL/bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4%2B-b0fcd85-vs-3.12.6.svg) | 1.069x ↓<br>[📄](results/bm-20250206-3.14.0a4%2B-b0fcd85-NOGIL/bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4%2B-b0fcd85-vs-3.13.0rc2.md)[📈](results/bm-20250206-3.14.0a4%2B-b0fcd85-NOGIL/bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4%2B-b0fcd85-vs-3.13.0rc2.svg) | 1.012x ↑<br>[📄](results/bm-20250206-3.14.0a4%2B-b0fcd85-NOGIL/bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4%2B-b0fcd85-vs-base.md)[📈](results/bm-20250206-3.14.0a4%2B-b0fcd85-NOGIL/bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4%2B-b0fcd85-vs-base.svg)[🧠](results/bm-20250206-3.14.0a4%2B-b0fcd85-NOGIL/bm-20250206-vultr-x86_64-mpage-load_fast_borrow-3.14.0a4%2B-b0fcd85-vs-base-mem.svg) |


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
