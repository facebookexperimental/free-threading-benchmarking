# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
[Most recent pystats on main (7d7d56d)](results/bm-20241102-3.14.0a1%2B-7d7d56d-PYTHON_UOPS/bm-20241102-vultr-x86_64-python-7d7d56d8b1147a6b85e1-3.14.0a1%2B-7d7d56d-pystats.md)

## linux x86_64 (linux)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2024-11-17](results/bm-20241117-3.14.0a1%2B-acbd5c9-NOGIL) | python/acbd5c9c6c62dac34d2e | acbd5c9 (NOGIL) | 1.41x ↓<br>[📄](results/bm-20241117-3.14.0a1%2B-acbd5c9-NOGIL/bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1%2B-acbd5c9-vs-3.12.6.md)[📈](results/bm-20241117-3.14.0a1%2B-acbd5c9-NOGIL/bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1%2B-acbd5c9-vs-3.12.6.svg) | 1.43x ↓<br>[📄](results/bm-20241117-3.14.0a1%2B-acbd5c9-NOGIL/bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1%2B-acbd5c9-vs-3.13.0rc2.md)[📈](results/bm-20241117-3.14.0a1%2B-acbd5c9-NOGIL/bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1%2B-acbd5c9-vs-3.13.0rc2.svg) | 1.42x ↓<br>[📄](results/bm-20241117-3.14.0a1%2B-acbd5c9-NOGIL/bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1%2B-acbd5c9-vs-base.md)[📈](results/bm-20241117-3.14.0a1%2B-acbd5c9-NOGIL/bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1%2B-acbd5c9-vs-base.svg)[🧠](results/bm-20241117-3.14.0a1%2B-acbd5c9-NOGIL/bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1%2B-acbd5c9-vs-base-mem.svg) |
| [2024-11-17](results/bm-20241117-3.14.0a1%2B-acbd5c9) | python/acbd5c9c6c62dac34d2e | acbd5c9 | 1.01x ↑<br>[📄](results/bm-20241117-3.14.0a1%2B-acbd5c9/bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1%2B-acbd5c9-vs-3.12.6.md)[📈](results/bm-20241117-3.14.0a1%2B-acbd5c9/bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1%2B-acbd5c9-vs-3.12.6.svg) | 1.01x ↓<br>[📄](results/bm-20241117-3.14.0a1%2B-acbd5c9/bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1%2B-acbd5c9-vs-3.13.0rc2.md)[📈](results/bm-20241117-3.14.0a1%2B-acbd5c9/bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1%2B-acbd5c9-vs-3.13.0rc2.svg) |  |
| [2024-11-15](results/bm-20241115-3.14.0a1%2B-d6bcc15) | python/d6bcc154e93a0a20ab97 | d6bcc15 | 1.01x ↑<br>[📄](results/bm-20241115-3.14.0a1%2B-d6bcc15/bm-20241115-linux-x86_64-python-d6bcc154e93a0a20ab97-3.14.0a1%2B-d6bcc15-vs-3.12.6.md)[📈](results/bm-20241115-3.14.0a1%2B-d6bcc15/bm-20241115-linux-x86_64-python-d6bcc154e93a0a20ab97-3.14.0a1%2B-d6bcc15-vs-3.12.6.svg) | 1.01x ↓<br>[📄](results/bm-20241115-3.14.0a1%2B-d6bcc15/bm-20241115-linux-x86_64-python-d6bcc154e93a0a20ab97-3.14.0a1%2B-d6bcc15-vs-3.13.0rc2.md)[📈](results/bm-20241115-3.14.0a1%2B-d6bcc15/bm-20241115-linux-x86_64-python-d6bcc154e93a0a20ab97-3.14.0a1%2B-d6bcc15-vs-3.13.0rc2.svg) |  |
| [2024-11-15](results/bm-20241115-3.14.0a1%2B-d6bcc15-NOGIL) | python/d6bcc154e93a0a20ab97 | d6bcc15 (NOGIL) | 1.47x ↓<br>[📄](results/bm-20241115-3.14.0a1%2B-d6bcc15-NOGIL/bm-20241115-linux-x86_64-python-d6bcc154e93a0a20ab97-3.14.0a1%2B-d6bcc15-vs-3.12.6.md)[📈](results/bm-20241115-3.14.0a1%2B-d6bcc15-NOGIL/bm-20241115-linux-x86_64-python-d6bcc154e93a0a20ab97-3.14.0a1%2B-d6bcc15-vs-3.12.6.svg) | 1.49x ↓<br>[📄](results/bm-20241115-3.14.0a1%2B-d6bcc15-NOGIL/bm-20241115-linux-x86_64-python-d6bcc154e93a0a20ab97-3.14.0a1%2B-d6bcc15-vs-3.13.0rc2.md)[📈](results/bm-20241115-3.14.0a1%2B-d6bcc15-NOGIL/bm-20241115-linux-x86_64-python-d6bcc154e93a0a20ab97-3.14.0a1%2B-d6bcc15-vs-3.13.0rc2.svg) | 1.48x ↓<br>[📄](results/bm-20241115-3.14.0a1%2B-d6bcc15-NOGIL/bm-20241115-linux-x86_64-python-d6bcc154e93a0a20ab97-3.14.0a1%2B-d6bcc15-vs-base.md)[📈](results/bm-20241115-3.14.0a1%2B-d6bcc15-NOGIL/bm-20241115-linux-x86_64-python-d6bcc154e93a0a20ab97-3.14.0a1%2B-d6bcc15-vs-base.svg)[🧠](results/bm-20241115-3.14.0a1%2B-d6bcc15-NOGIL/bm-20241115-linux-x86_64-python-d6bcc154e93a0a20ab97-3.14.0a1%2B-d6bcc15-vs-base-mem.svg) |
| [2024-11-15](results/bm-20241115-3.14.0a1%2B-3fecbe9) | python/3fecbe9255391be1ac3c | 3fecbe9 | 1.03x ↑<br>[📄](results/bm-20241115-3.14.0a1%2B-3fecbe9/bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1%2B-3fecbe9-vs-3.12.6.md)[📈](results/bm-20241115-3.14.0a1%2B-3fecbe9/bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1%2B-3fecbe9-vs-3.12.6.svg) | 1.01x ↑<br>[📄](results/bm-20241115-3.14.0a1%2B-3fecbe9/bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1%2B-3fecbe9-vs-3.13.0rc2.md)[📈](results/bm-20241115-3.14.0a1%2B-3fecbe9/bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1%2B-3fecbe9-vs-3.13.0rc2.svg) |  |
| [2024-11-15](results/bm-20241115-3.14.0a1%2B-3fecbe9-NOGIL) | python/3fecbe9255391be1ac3c | 3fecbe9 (NOGIL) | 1.43x ↓<br>[📄](results/bm-20241115-3.14.0a1%2B-3fecbe9-NOGIL/bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1%2B-3fecbe9-vs-3.12.6.md)[📈](results/bm-20241115-3.14.0a1%2B-3fecbe9-NOGIL/bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1%2B-3fecbe9-vs-3.12.6.svg) | 1.45x ↓<br>[📄](results/bm-20241115-3.14.0a1%2B-3fecbe9-NOGIL/bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1%2B-3fecbe9-vs-3.13.0rc2.md)[📈](results/bm-20241115-3.14.0a1%2B-3fecbe9-NOGIL/bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1%2B-3fecbe9-vs-3.13.0rc2.svg) | 1.46x ↓<br>[📄](results/bm-20241115-3.14.0a1%2B-3fecbe9-NOGIL/bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1%2B-3fecbe9-vs-base.md)[📈](results/bm-20241115-3.14.0a1%2B-3fecbe9-NOGIL/bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1%2B-3fecbe9-vs-base.svg)[🧠](results/bm-20241115-3.14.0a1%2B-3fecbe9-NOGIL/bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1%2B-3fecbe9-vs-base-mem.svg) |
| [2024-11-13](results/bm-20241113-3.14.0a1%2B-4ae5061) | python/4ae50615d2beef0f93d9 | 4ae5061 | 1.00x ↓<br>[📄](results/bm-20241113-3.14.0a1%2B-4ae5061/bm-20241113-linux-x86_64-python-4ae50615d2beef0f93d9-3.14.0a1%2B-4ae5061-vs-3.12.6.md)[📈](results/bm-20241113-3.14.0a1%2B-4ae5061/bm-20241113-linux-x86_64-python-4ae50615d2beef0f93d9-3.14.0a1%2B-4ae5061-vs-3.12.6.svg) | 1.02x ↓<br>[📄](results/bm-20241113-3.14.0a1%2B-4ae5061/bm-20241113-linux-x86_64-python-4ae50615d2beef0f93d9-3.14.0a1%2B-4ae5061-vs-3.13.0rc2.md)[📈](results/bm-20241113-3.14.0a1%2B-4ae5061/bm-20241113-linux-x86_64-python-4ae50615d2beef0f93d9-3.14.0a1%2B-4ae5061-vs-3.13.0rc2.svg) |  |
| [2024-11-13](results/bm-20241113-3.14.0a1%2B-4ae5061-NOGIL) | python/4ae50615d2beef0f93d9 | 4ae5061 (NOGIL) | 1.47x ↓<br>[📄](results/bm-20241113-3.14.0a1%2B-4ae5061-NOGIL/bm-20241113-linux-x86_64-python-4ae50615d2beef0f93d9-3.14.0a1%2B-4ae5061-vs-3.12.6.md)[📈](results/bm-20241113-3.14.0a1%2B-4ae5061-NOGIL/bm-20241113-linux-x86_64-python-4ae50615d2beef0f93d9-3.14.0a1%2B-4ae5061-vs-3.12.6.svg) | 1.49x ↓<br>[📄](results/bm-20241113-3.14.0a1%2B-4ae5061-NOGIL/bm-20241113-linux-x86_64-python-4ae50615d2beef0f93d9-3.14.0a1%2B-4ae5061-vs-3.13.0rc2.md)[📈](results/bm-20241113-3.14.0a1%2B-4ae5061-NOGIL/bm-20241113-linux-x86_64-python-4ae50615d2beef0f93d9-3.14.0a1%2B-4ae5061-vs-3.13.0rc2.svg) | 1.47x ↓<br>[📄](results/bm-20241113-3.14.0a1%2B-4ae5061-NOGIL/bm-20241113-linux-x86_64-python-4ae50615d2beef0f93d9-3.14.0a1%2B-4ae5061-vs-base.md)[📈](results/bm-20241113-3.14.0a1%2B-4ae5061-NOGIL/bm-20241113-linux-x86_64-python-4ae50615d2beef0f93d9-3.14.0a1%2B-4ae5061-vs-base.svg)[🧠](results/bm-20241113-3.14.0a1%2B-4ae5061-NOGIL/bm-20241113-linux-x86_64-python-4ae50615d2beef0f93d9-3.14.0a1%2B-4ae5061-vs-base-mem.svg) |

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2024-11-17](results/bm-20241117-3.14.0a1%2B-acbd5c9-NOGIL) | python/acbd5c9c6c62dac34d2e | acbd5c9 (NOGIL) | 1.56x ↓<br>[📄](results/bm-20241117-3.14.0a1%2B-acbd5c9-NOGIL/bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1%2B-acbd5c9-vs-3.12.6.md)[📈](results/bm-20241117-3.14.0a1%2B-acbd5c9-NOGIL/bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1%2B-acbd5c9-vs-3.12.6.svg) | 1.58x ↓<br>[📄](results/bm-20241117-3.14.0a1%2B-acbd5c9-NOGIL/bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1%2B-acbd5c9-vs-3.13.0rc2.md)[📈](results/bm-20241117-3.14.0a1%2B-acbd5c9-NOGIL/bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1%2B-acbd5c9-vs-3.13.0rc2.svg) | 1.56x ↓<br>[📄](results/bm-20241117-3.14.0a1%2B-acbd5c9-NOGIL/bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1%2B-acbd5c9-vs-base.md)[📈](results/bm-20241117-3.14.0a1%2B-acbd5c9-NOGIL/bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1%2B-acbd5c9-vs-base.svg)[🧠](results/bm-20241117-3.14.0a1%2B-acbd5c9-NOGIL/bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1%2B-acbd5c9-vs-base-mem.svg) |
| [2024-11-17](results/bm-20241117-3.14.0a1%2B-acbd5c9) | python/acbd5c9c6c62dac34d2e | acbd5c9 | 1.00x ↓<br>[📄](results/bm-20241117-3.14.0a1%2B-acbd5c9/bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1%2B-acbd5c9-vs-3.12.6.md)[📈](results/bm-20241117-3.14.0a1%2B-acbd5c9/bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1%2B-acbd5c9-vs-3.12.6.svg) | 1.02x ↓<br>[📄](results/bm-20241117-3.14.0a1%2B-acbd5c9/bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1%2B-acbd5c9-vs-3.13.0rc2.md)[📈](results/bm-20241117-3.14.0a1%2B-acbd5c9/bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1%2B-acbd5c9-vs-3.13.0rc2.svg) |  |
| [2024-11-15](results/bm-20241115-3.14.0a1%2B-d6bcc15) | python/d6bcc154e93a0a20ab97 | d6bcc15 | 1.00x ↓<br>[📄](results/bm-20241115-3.14.0a1%2B-d6bcc15/bm-20241115-vultr-x86_64-python-d6bcc154e93a0a20ab97-3.14.0a1%2B-d6bcc15-vs-3.12.6.md)[📈](results/bm-20241115-3.14.0a1%2B-d6bcc15/bm-20241115-vultr-x86_64-python-d6bcc154e93a0a20ab97-3.14.0a1%2B-d6bcc15-vs-3.12.6.svg) | 1.02x ↓<br>[📄](results/bm-20241115-3.14.0a1%2B-d6bcc15/bm-20241115-vultr-x86_64-python-d6bcc154e93a0a20ab97-3.14.0a1%2B-d6bcc15-vs-3.13.0rc2.md)[📈](results/bm-20241115-3.14.0a1%2B-d6bcc15/bm-20241115-vultr-x86_64-python-d6bcc154e93a0a20ab97-3.14.0a1%2B-d6bcc15-vs-3.13.0rc2.svg) |  |
| [2024-11-15](results/bm-20241115-3.14.0a1%2B-d6bcc15-NOGIL) | python/d6bcc154e93a0a20ab97 | d6bcc15 (NOGIL) | 1.55x ↓<br>[📄](results/bm-20241115-3.14.0a1%2B-d6bcc15-NOGIL/bm-20241115-vultr-x86_64-python-d6bcc154e93a0a20ab97-3.14.0a1%2B-d6bcc15-vs-3.12.6.md)[📈](results/bm-20241115-3.14.0a1%2B-d6bcc15-NOGIL/bm-20241115-vultr-x86_64-python-d6bcc154e93a0a20ab97-3.14.0a1%2B-d6bcc15-vs-3.12.6.svg) | 1.58x ↓<br>[📄](results/bm-20241115-3.14.0a1%2B-d6bcc15-NOGIL/bm-20241115-vultr-x86_64-python-d6bcc154e93a0a20ab97-3.14.0a1%2B-d6bcc15-vs-3.13.0rc2.md)[📈](results/bm-20241115-3.14.0a1%2B-d6bcc15-NOGIL/bm-20241115-vultr-x86_64-python-d6bcc154e93a0a20ab97-3.14.0a1%2B-d6bcc15-vs-3.13.0rc2.svg) | 1.55x ↓<br>[📄](results/bm-20241115-3.14.0a1%2B-d6bcc15-NOGIL/bm-20241115-vultr-x86_64-python-d6bcc154e93a0a20ab97-3.14.0a1%2B-d6bcc15-vs-base.md)[📈](results/bm-20241115-3.14.0a1%2B-d6bcc15-NOGIL/bm-20241115-vultr-x86_64-python-d6bcc154e93a0a20ab97-3.14.0a1%2B-d6bcc15-vs-base.svg)[🧠](results/bm-20241115-3.14.0a1%2B-d6bcc15-NOGIL/bm-20241115-vultr-x86_64-python-d6bcc154e93a0a20ab97-3.14.0a1%2B-d6bcc15-vs-base-mem.svg) |
| [2024-11-15](results/bm-20241115-3.14.0a1%2B-3fecbe9) | python/3fecbe9255391be1ac3c | 3fecbe9 | 1.00x ↓<br>[📄](results/bm-20241115-3.14.0a1%2B-3fecbe9/bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1%2B-3fecbe9-vs-3.12.6.md)[📈](results/bm-20241115-3.14.0a1%2B-3fecbe9/bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1%2B-3fecbe9-vs-3.12.6.svg) | 1.02x ↓<br>[📄](results/bm-20241115-3.14.0a1%2B-3fecbe9/bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1%2B-3fecbe9-vs-3.13.0rc2.md)[📈](results/bm-20241115-3.14.0a1%2B-3fecbe9/bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1%2B-3fecbe9-vs-3.13.0rc2.svg) |  |
| [2024-11-15](results/bm-20241115-3.14.0a1%2B-3fecbe9-NOGIL) | python/3fecbe9255391be1ac3c | 3fecbe9 (NOGIL) | 1.54x ↓<br>[📄](results/bm-20241115-3.14.0a1%2B-3fecbe9-NOGIL/bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1%2B-3fecbe9-vs-3.12.6.md)[📈](results/bm-20241115-3.14.0a1%2B-3fecbe9-NOGIL/bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1%2B-3fecbe9-vs-3.12.6.svg) | 1.57x ↓<br>[📄](results/bm-20241115-3.14.0a1%2B-3fecbe9-NOGIL/bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1%2B-3fecbe9-vs-3.13.0rc2.md)[📈](results/bm-20241115-3.14.0a1%2B-3fecbe9-NOGIL/bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1%2B-3fecbe9-vs-3.13.0rc2.svg) | 1.54x ↓<br>[📄](results/bm-20241115-3.14.0a1%2B-3fecbe9-NOGIL/bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1%2B-3fecbe9-vs-base.md)[📈](results/bm-20241115-3.14.0a1%2B-3fecbe9-NOGIL/bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1%2B-3fecbe9-vs-base.svg)[🧠](results/bm-20241115-3.14.0a1%2B-3fecbe9-NOGIL/bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1%2B-3fecbe9-vs-base-mem.svg) |
| [2024-11-13](results/bm-20241113-3.14.0a1%2B-4ae5061) | python/4ae50615d2beef0f93d9 | 4ae5061 | 1.00x ↓<br>[📄](results/bm-20241113-3.14.0a1%2B-4ae5061/bm-20241113-vultr-x86_64-python-4ae50615d2beef0f93d9-3.14.0a1%2B-4ae5061-vs-3.12.6.md)[📈](results/bm-20241113-3.14.0a1%2B-4ae5061/bm-20241113-vultr-x86_64-python-4ae50615d2beef0f93d9-3.14.0a1%2B-4ae5061-vs-3.12.6.svg) | 1.02x ↓<br>[📄](results/bm-20241113-3.14.0a1%2B-4ae5061/bm-20241113-vultr-x86_64-python-4ae50615d2beef0f93d9-3.14.0a1%2B-4ae5061-vs-3.13.0rc2.md)[📈](results/bm-20241113-3.14.0a1%2B-4ae5061/bm-20241113-vultr-x86_64-python-4ae50615d2beef0f93d9-3.14.0a1%2B-4ae5061-vs-3.13.0rc2.svg) |  |
| [2024-11-13](results/bm-20241113-3.14.0a1%2B-4ae5061-NOGIL) | python/4ae50615d2beef0f93d9 | 4ae5061 (NOGIL) | 1.55x ↓<br>[📄](results/bm-20241113-3.14.0a1%2B-4ae5061-NOGIL/bm-20241113-vultr-x86_64-python-4ae50615d2beef0f93d9-3.14.0a1%2B-4ae5061-vs-3.12.6.md)[📈](results/bm-20241113-3.14.0a1%2B-4ae5061-NOGIL/bm-20241113-vultr-x86_64-python-4ae50615d2beef0f93d9-3.14.0a1%2B-4ae5061-vs-3.12.6.svg) | 1.57x ↓<br>[📄](results/bm-20241113-3.14.0a1%2B-4ae5061-NOGIL/bm-20241113-vultr-x86_64-python-4ae50615d2beef0f93d9-3.14.0a1%2B-4ae5061-vs-3.13.0rc2.md)[📈](results/bm-20241113-3.14.0a1%2B-4ae5061-NOGIL/bm-20241113-vultr-x86_64-python-4ae50615d2beef0f93d9-3.14.0a1%2B-4ae5061-vs-3.13.0rc2.svg) | 1.54x ↓<br>[📄](results/bm-20241113-3.14.0a1%2B-4ae5061-NOGIL/bm-20241113-vultr-x86_64-python-4ae50615d2beef0f93d9-3.14.0a1%2B-4ae5061-vs-base.md)[📈](results/bm-20241113-3.14.0a1%2B-4ae5061-NOGIL/bm-20241113-vultr-x86_64-python-4ae50615d2beef0f93d9-3.14.0a1%2B-4ae5061-vs-base.svg)[🧠](results/bm-20241113-3.14.0a1%2B-4ae5061-NOGIL/bm-20241113-vultr-x86_64-python-4ae50615d2beef0f93d9-3.14.0a1%2B-4ae5061-vs-base-mem.svg) |


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
