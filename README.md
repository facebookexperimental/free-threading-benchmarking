# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
[Most recent pystats on main (29f8a67)](results/bm-20250208-3.14.0a4%2B-29f8a67-PYTHON_UOPS/bm-20250208-linux-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-pystats.md)

## linux x86_64 (linux)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-02-11](results/bm-20250211-3.14.0a5%2B-06ac157) | python/06ac157c53046f4fcad3 | 06ac157 | 1.125x ↑<br>[📄](results/bm-20250211-3.14.0a5%2B-06ac157/bm-20250211-linux-x86_64-python-06ac157c53046f4fcad3-3.14.0a5%2B-06ac157-vs-3.12.6.md)[📈](results/bm-20250211-3.14.0a5%2B-06ac157/bm-20250211-linux-x86_64-python-06ac157c53046f4fcad3-3.14.0a5%2B-06ac157-vs-3.12.6.svg) | 1.083x ↑<br>[📄](results/bm-20250211-3.14.0a5%2B-06ac157/bm-20250211-linux-x86_64-python-06ac157c53046f4fcad3-3.14.0a5%2B-06ac157-vs-3.13.0rc2.md)[📈](results/bm-20250211-3.14.0a5%2B-06ac157/bm-20250211-linux-x86_64-python-06ac157c53046f4fcad3-3.14.0a5%2B-06ac157-vs-3.13.0rc2.svg) |  |
| [2025-02-11](results/bm-20250211-3.14.0a5%2B-06ac157-NOGIL) | python/06ac157c53046f4fcad3 | 06ac157 (NOGIL) | 1.009x ↓<br>[📄](results/bm-20250211-3.14.0a5%2B-06ac157-NOGIL/bm-20250211-linux-x86_64-python-06ac157c53046f4fcad3-3.14.0a5%2B-06ac157-vs-3.12.6.md)[📈](results/bm-20250211-3.14.0a5%2B-06ac157-NOGIL/bm-20250211-linux-x86_64-python-06ac157c53046f4fcad3-3.14.0a5%2B-06ac157-vs-3.12.6.svg) | 1.046x ↓<br>[📄](results/bm-20250211-3.14.0a5%2B-06ac157-NOGIL/bm-20250211-linux-x86_64-python-06ac157c53046f4fcad3-3.14.0a5%2B-06ac157-vs-3.13.0rc2.md)[📈](results/bm-20250211-3.14.0a5%2B-06ac157-NOGIL/bm-20250211-linux-x86_64-python-06ac157c53046f4fcad3-3.14.0a5%2B-06ac157-vs-3.13.0rc2.svg) | 1.119x ↓<br>[📄](results/bm-20250211-3.14.0a5%2B-06ac157-NOGIL/bm-20250211-linux-x86_64-python-06ac157c53046f4fcad3-3.14.0a5%2B-06ac157-vs-base.md)[📈](results/bm-20250211-3.14.0a5%2B-06ac157-NOGIL/bm-20250211-linux-x86_64-python-06ac157c53046f4fcad3-3.14.0a5%2B-06ac157-vs-base.svg)[🧠](results/bm-20250211-3.14.0a5%2B-06ac157-NOGIL/bm-20250211-linux-x86_64-python-06ac157c53046f4fcad3-3.14.0a5%2B-06ac157-vs-base-mem.svg) |
| [2025-02-10](results/bm-20250210-3.14.0a4%2B-1feaecc) | python/1feaecc2bc42cb96f2d7 | 1feaecc | 1.108x ↑<br>[📄](results/bm-20250210-3.14.0a4%2B-1feaecc/bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4%2B-1feaecc-vs-3.12.6.md)[📈](results/bm-20250210-3.14.0a4%2B-1feaecc/bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4%2B-1feaecc-vs-3.12.6.svg) | 1.065x ↑<br>[📄](results/bm-20250210-3.14.0a4%2B-1feaecc/bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4%2B-1feaecc-vs-3.13.0rc2.md)[📈](results/bm-20250210-3.14.0a4%2B-1feaecc/bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4%2B-1feaecc-vs-3.13.0rc2.svg) |  |
| [2025-02-10](results/bm-20250210-3.14.0a4%2B-1feaecc-NOGIL) | python/1feaecc2bc42cb96f2d7 | 1feaecc (NOGIL) | 1.034x ↓<br>[📄](results/bm-20250210-3.14.0a4%2B-1feaecc-NOGIL/bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4%2B-1feaecc-vs-3.12.6.md)[📈](results/bm-20250210-3.14.0a4%2B-1feaecc-NOGIL/bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4%2B-1feaecc-vs-3.12.6.svg) | 1.070x ↓<br>[📄](results/bm-20250210-3.14.0a4%2B-1feaecc-NOGIL/bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4%2B-1feaecc-vs-3.13.0rc2.md)[📈](results/bm-20250210-3.14.0a4%2B-1feaecc-NOGIL/bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4%2B-1feaecc-vs-3.13.0rc2.svg) | 1.127x ↓<br>[📄](results/bm-20250210-3.14.0a4%2B-1feaecc-NOGIL/bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4%2B-1feaecc-vs-base.md)[📈](results/bm-20250210-3.14.0a4%2B-1feaecc-NOGIL/bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4%2B-1feaecc-vs-base.svg)[🧠](results/bm-20250210-3.14.0a4%2B-1feaecc-NOGIL/bm-20250210-linux-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4%2B-1feaecc-vs-base-mem.svg) |
| [2025-02-10](results/bm-20250210-3.14.0a4%2B-7e6ee50) | python/7e6ee50b6b8c760bcefb | 7e6ee50 | 1.111x ↑<br>[📄](results/bm-20250210-3.14.0a4%2B-7e6ee50/bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-3.12.6.md)[📈](results/bm-20250210-3.14.0a4%2B-7e6ee50/bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-3.12.6.svg) | 1.073x ↑<br>[📄](results/bm-20250210-3.14.0a4%2B-7e6ee50/bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-3.13.0rc2.md)[📈](results/bm-20250210-3.14.0a4%2B-7e6ee50/bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-3.13.0rc2.svg) |  |
| [2025-02-10](results/bm-20250210-3.14.0a4%2B-7e6ee50-NOGIL) | python/7e6ee50b6b8c760bcefb | 7e6ee50 (NOGIL) | 1.020x ↓<br>[📄](results/bm-20250210-3.14.0a4%2B-7e6ee50-NOGIL/bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-3.12.6.md)[📈](results/bm-20250210-3.14.0a4%2B-7e6ee50-NOGIL/bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-3.12.6.svg) | 1.056x ↓<br>[📄](results/bm-20250210-3.14.0a4%2B-7e6ee50-NOGIL/bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-3.13.0rc2.md)[📈](results/bm-20250210-3.14.0a4%2B-7e6ee50-NOGIL/bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-3.13.0rc2.svg) | 1.116x ↓<br>[📄](results/bm-20250210-3.14.0a4%2B-7e6ee50-NOGIL/bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-base.md)[📈](results/bm-20250210-3.14.0a4%2B-7e6ee50-NOGIL/bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-base.svg)[🧠](results/bm-20250210-3.14.0a4%2B-7e6ee50-NOGIL/bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-base-mem.svg) |
| [2025-02-08](results/bm-20250208-3.14.0a4%2B-29f8a67) | python/29f8a67ae00081a36fdc | 29f8a67 | 1.149x ↑<br>[📄](results/bm-20250208-3.14.0a4%2B-29f8a67/bm-20250208-linux-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-3.12.6.md)[📈](results/bm-20250208-3.14.0a4%2B-29f8a67/bm-20250208-linux-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-3.12.6.svg) | 1.104x ↑<br>[📄](results/bm-20250208-3.14.0a4%2B-29f8a67/bm-20250208-linux-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-3.13.0rc2.md)[📈](results/bm-20250208-3.14.0a4%2B-29f8a67/bm-20250208-linux-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-3.13.0rc2.svg) |  |
| [2025-02-08](results/bm-20250208-3.14.0a4%2B-29f8a67-NOGIL) | python/29f8a67ae00081a36fdc | 29f8a67 (NOGIL) | 1.003x ↑<br>[📄](results/bm-20250208-3.14.0a4%2B-29f8a67-NOGIL/bm-20250208-linux-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-3.12.6.md)[📈](results/bm-20250208-3.14.0a4%2B-29f8a67-NOGIL/bm-20250208-linux-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-3.12.6.svg) | 1.034x ↓<br>[📄](results/bm-20250208-3.14.0a4%2B-29f8a67-NOGIL/bm-20250208-linux-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-3.13.0rc2.md)[📈](results/bm-20250208-3.14.0a4%2B-29f8a67-NOGIL/bm-20250208-linux-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-3.13.0rc2.svg) | 1.123x ↓<br>[📄](results/bm-20250208-3.14.0a4%2B-29f8a67-NOGIL/bm-20250208-linux-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-base.md)[📈](results/bm-20250208-3.14.0a4%2B-29f8a67-NOGIL/bm-20250208-linux-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-base.svg)[🧠](results/bm-20250208-3.14.0a4%2B-29f8a67-NOGIL/bm-20250208-linux-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-base-mem.svg) |

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-02-11](results/bm-20250211-3.14.0a5%2B-06ac157) | python/06ac157c53046f4fcad3 | 06ac157 | 1.092x ↑<br>[📄](results/bm-20250211-3.14.0a5%2B-06ac157/bm-20250211-vultr-x86_64-python-06ac157c53046f4fcad3-3.14.0a5%2B-06ac157-vs-3.12.6.md)[📈](results/bm-20250211-3.14.0a5%2B-06ac157/bm-20250211-vultr-x86_64-python-06ac157c53046f4fcad3-3.14.0a5%2B-06ac157-vs-3.12.6.svg) | 1.053x ↑<br>[📄](results/bm-20250211-3.14.0a5%2B-06ac157/bm-20250211-vultr-x86_64-python-06ac157c53046f4fcad3-3.14.0a5%2B-06ac157-vs-3.13.0rc2.md)[📈](results/bm-20250211-3.14.0a5%2B-06ac157/bm-20250211-vultr-x86_64-python-06ac157c53046f4fcad3-3.14.0a5%2B-06ac157-vs-3.13.0rc2.svg) |  |
| [2025-02-11](results/bm-20250211-3.14.0a5%2B-06ac157-NOGIL) | python/06ac157c53046f4fcad3 | 06ac157 (NOGIL) | 1.046x ↓<br>[📄](results/bm-20250211-3.14.0a5%2B-06ac157-NOGIL/bm-20250211-vultr-x86_64-python-06ac157c53046f4fcad3-3.14.0a5%2B-06ac157-vs-3.12.6.md)[📈](results/bm-20250211-3.14.0a5%2B-06ac157-NOGIL/bm-20250211-vultr-x86_64-python-06ac157c53046f4fcad3-3.14.0a5%2B-06ac157-vs-3.12.6.svg) | 1.077x ↓<br>[📄](results/bm-20250211-3.14.0a5%2B-06ac157-NOGIL/bm-20250211-vultr-x86_64-python-06ac157c53046f4fcad3-3.14.0a5%2B-06ac157-vs-3.13.0rc2.md)[📈](results/bm-20250211-3.14.0a5%2B-06ac157-NOGIL/bm-20250211-vultr-x86_64-python-06ac157c53046f4fcad3-3.14.0a5%2B-06ac157-vs-3.13.0rc2.svg) | 1.127x ↓<br>[📄](results/bm-20250211-3.14.0a5%2B-06ac157-NOGIL/bm-20250211-vultr-x86_64-python-06ac157c53046f4fcad3-3.14.0a5%2B-06ac157-vs-base.md)[📈](results/bm-20250211-3.14.0a5%2B-06ac157-NOGIL/bm-20250211-vultr-x86_64-python-06ac157c53046f4fcad3-3.14.0a5%2B-06ac157-vs-base.svg)[🧠](results/bm-20250211-3.14.0a5%2B-06ac157-NOGIL/bm-20250211-vultr-x86_64-python-06ac157c53046f4fcad3-3.14.0a5%2B-06ac157-vs-base-mem.svg) |
| [2025-02-10](results/bm-20250210-3.14.0a4%2B-1feaecc) | python/1feaecc2bc42cb96f2d7 | 1feaecc | 1.099x ↑<br>[📄](results/bm-20250210-3.14.0a4%2B-1feaecc/bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4%2B-1feaecc-vs-3.12.6.md)[📈](results/bm-20250210-3.14.0a4%2B-1feaecc/bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4%2B-1feaecc-vs-3.12.6.svg) | 1.060x ↑<br>[📄](results/bm-20250210-3.14.0a4%2B-1feaecc/bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4%2B-1feaecc-vs-3.13.0rc2.md)[📈](results/bm-20250210-3.14.0a4%2B-1feaecc/bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4%2B-1feaecc-vs-3.13.0rc2.svg) |  |
| [2025-02-10](results/bm-20250210-3.14.0a4%2B-1feaecc-NOGIL) | python/1feaecc2bc42cb96f2d7 | 1feaecc (NOGIL) | 1.050x ↓<br>[📄](results/bm-20250210-3.14.0a4%2B-1feaecc-NOGIL/bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4%2B-1feaecc-vs-3.12.6.md)[📈](results/bm-20250210-3.14.0a4%2B-1feaecc-NOGIL/bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4%2B-1feaecc-vs-3.12.6.svg) | 1.081x ↓<br>[📄](results/bm-20250210-3.14.0a4%2B-1feaecc-NOGIL/bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4%2B-1feaecc-vs-3.13.0rc2.md)[📈](results/bm-20250210-3.14.0a4%2B-1feaecc-NOGIL/bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4%2B-1feaecc-vs-3.13.0rc2.svg) | 1.136x ↓<br>[📄](results/bm-20250210-3.14.0a4%2B-1feaecc-NOGIL/bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4%2B-1feaecc-vs-base.md)[📈](results/bm-20250210-3.14.0a4%2B-1feaecc-NOGIL/bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4%2B-1feaecc-vs-base.svg)[🧠](results/bm-20250210-3.14.0a4%2B-1feaecc-NOGIL/bm-20250210-vultr-x86_64-python-1feaecc2bc42cb96f2d7-3.14.0a4%2B-1feaecc-vs-base-mem.svg) |
| [2025-02-10](results/bm-20250210-3.14.0a4%2B-8e67151-NOGIL) | DinoV/immortal_deferred | 8e67151 (NOGIL) | 1.045x ↓<br>[📄](results/bm-20250210-3.14.0a4%2B-8e67151-NOGIL/bm-20250210-vultr-x86_64-DinoV-immortal_deferred-3.14.0a4%2B-8e67151-vs-3.12.6.md)[📈](results/bm-20250210-3.14.0a4%2B-8e67151-NOGIL/bm-20250210-vultr-x86_64-DinoV-immortal_deferred-3.14.0a4%2B-8e67151-vs-3.12.6.svg) | 1.078x ↓<br>[📄](results/bm-20250210-3.14.0a4%2B-8e67151-NOGIL/bm-20250210-vultr-x86_64-DinoV-immortal_deferred-3.14.0a4%2B-8e67151-vs-3.13.0rc2.md)[📈](results/bm-20250210-3.14.0a4%2B-8e67151-NOGIL/bm-20250210-vultr-x86_64-DinoV-immortal_deferred-3.14.0a4%2B-8e67151-vs-3.13.0rc2.svg) | 1.004x ↓<br>[📄](results/bm-20250210-3.14.0a4%2B-8e67151-NOGIL/bm-20250210-vultr-x86_64-DinoV-immortal_deferred-3.14.0a4%2B-8e67151-vs-base.md)[📈](results/bm-20250210-3.14.0a4%2B-8e67151-NOGIL/bm-20250210-vultr-x86_64-DinoV-immortal_deferred-3.14.0a4%2B-8e67151-vs-base.svg)[🧠](results/bm-20250210-3.14.0a4%2B-8e67151-NOGIL/bm-20250210-vultr-x86_64-DinoV-immortal_deferred-3.14.0a4%2B-8e67151-vs-base-mem.svg) |
| [2025-02-10](results/bm-20250210-3.14.0a4%2B-7e6ee50) | python/7e6ee50b6b8c760bcefb | 7e6ee50 | 1.097x ↑<br>[📄](results/bm-20250210-3.14.0a4%2B-7e6ee50/bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-3.12.6.md)[📈](results/bm-20250210-3.14.0a4%2B-7e6ee50/bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-3.12.6.svg) | 1.058x ↑<br>[📄](results/bm-20250210-3.14.0a4%2B-7e6ee50/bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-3.13.0rc2.md)[📈](results/bm-20250210-3.14.0a4%2B-7e6ee50/bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-3.13.0rc2.svg) |  |
| [2025-02-10](results/bm-20250210-3.14.0a4%2B-7e6ee50-NOGIL) | python/7e6ee50b6b8c760bcefb | 7e6ee50 (NOGIL) | 1.044x ↓<br>[📄](results/bm-20250210-3.14.0a4%2B-7e6ee50-NOGIL/bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-3.12.6.md)[📈](results/bm-20250210-3.14.0a4%2B-7e6ee50-NOGIL/bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-3.12.6.svg) | 1.075x ↓<br>[📄](results/bm-20250210-3.14.0a4%2B-7e6ee50-NOGIL/bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-3.13.0rc2.md)[📈](results/bm-20250210-3.14.0a4%2B-7e6ee50-NOGIL/bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-3.13.0rc2.svg) | 1.129x ↓<br>[📄](results/bm-20250210-3.14.0a4%2B-7e6ee50-NOGIL/bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-base.md)[📈](results/bm-20250210-3.14.0a4%2B-7e6ee50-NOGIL/bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-base.svg)[🧠](results/bm-20250210-3.14.0a4%2B-7e6ee50-NOGIL/bm-20250210-vultr-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4%2B-7e6ee50-vs-base-mem.svg) |
| [2025-02-08](results/bm-20250208-3.14.0a4%2B-29f8a67) | python/29f8a67ae00081a36fdc | 29f8a67 | 1.096x ↑<br>[📄](results/bm-20250208-3.14.0a4%2B-29f8a67/bm-20250208-vultr-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-3.12.6.md)[📈](results/bm-20250208-3.14.0a4%2B-29f8a67/bm-20250208-vultr-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-3.12.6.svg) | 1.057x ↑<br>[📄](results/bm-20250208-3.14.0a4%2B-29f8a67/bm-20250208-vultr-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-3.13.0rc2.md)[📈](results/bm-20250208-3.14.0a4%2B-29f8a67/bm-20250208-vultr-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-3.13.0rc2.svg) |  |
| [2025-02-08](results/bm-20250208-3.14.0a4%2B-29f8a67-NOGIL) | python/29f8a67ae00081a36fdc | 29f8a67 (NOGIL) | 1.048x ↓<br>[📄](results/bm-20250208-3.14.0a4%2B-29f8a67-NOGIL/bm-20250208-vultr-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-3.12.6.md)[📈](results/bm-20250208-3.14.0a4%2B-29f8a67-NOGIL/bm-20250208-vultr-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-3.12.6.svg) | 1.079x ↓<br>[📄](results/bm-20250208-3.14.0a4%2B-29f8a67-NOGIL/bm-20250208-vultr-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-3.13.0rc2.md)[📈](results/bm-20250208-3.14.0a4%2B-29f8a67-NOGIL/bm-20250208-vultr-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-3.13.0rc2.svg) | 1.132x ↓<br>[📄](results/bm-20250208-3.14.0a4%2B-29f8a67-NOGIL/bm-20250208-vultr-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-base.md)[📈](results/bm-20250208-3.14.0a4%2B-29f8a67-NOGIL/bm-20250208-vultr-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-base.svg)[🧠](results/bm-20250208-3.14.0a4%2B-29f8a67-NOGIL/bm-20250208-vultr-x86_64-python-29f8a67ae00081a36fdc-3.14.0a4%2B-29f8a67-vs-base-mem.svg) |
| [2025-02-05](results/bm-20250205-3.14.0a4%2B-cbd6459-NOGIL) | DinoV/hash_type | cbd6459 (NOGIL) | 1.048x ↓<br>[📄](results/bm-20250205-3.14.0a4%2B-cbd6459-NOGIL/bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4%2B-cbd6459-vs-3.12.6.md)[📈](results/bm-20250205-3.14.0a4%2B-cbd6459-NOGIL/bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4%2B-cbd6459-vs-3.12.6.svg) | 1.080x ↓<br>[📄](results/bm-20250205-3.14.0a4%2B-cbd6459-NOGIL/bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4%2B-cbd6459-vs-3.13.0rc2.md)[📈](results/bm-20250205-3.14.0a4%2B-cbd6459-NOGIL/bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4%2B-cbd6459-vs-3.13.0rc2.svg) | 1.007x ↓<br>[📄](results/bm-20250205-3.14.0a4%2B-cbd6459-NOGIL/bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4%2B-cbd6459-vs-base.md)[📈](results/bm-20250205-3.14.0a4%2B-cbd6459-NOGIL/bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4%2B-cbd6459-vs-base.svg)[🧠](results/bm-20250205-3.14.0a4%2B-cbd6459-NOGIL/bm-20250205-vultr-x86_64-DinoV-hash_type-3.14.0a4%2B-cbd6459-vs-base-mem.svg) |


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
