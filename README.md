# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
[Most recent pystats on main (359c7dd)](results/bm-20250216-3.14.0a5%2B-359c7dd-PYTHON_UOPS/bm-20250216-linux-x86_64-python-359c7dde3bb074e02968-3.14.0a5%2B-359c7dd-pystats.md)

## linux x86_64 (linux)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-02-17](results/bm-20250217-3.14.0a5%2B-99d9656-NOGIL) | python/99d965635ae2ac4bffdc | 99d9656 (NOGIL) | 1.014x ↓<br>[📄](results/bm-20250217-3.14.0a5%2B-99d9656-NOGIL/bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5%2B-99d9656-vs-3.12.6.md)[📈](results/bm-20250217-3.14.0a5%2B-99d9656-NOGIL/bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5%2B-99d9656-vs-3.12.6.svg) | 1.051x ↓<br>[📄](results/bm-20250217-3.14.0a5%2B-99d9656-NOGIL/bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5%2B-99d9656-vs-3.13.0rc2.md)[📈](results/bm-20250217-3.14.0a5%2B-99d9656-NOGIL/bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5%2B-99d9656-vs-3.13.0rc2.svg) | 1.109x ↓<br>[📄](results/bm-20250217-3.14.0a5%2B-99d9656-NOGIL/bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5%2B-99d9656-vs-base.md)[📈](results/bm-20250217-3.14.0a5%2B-99d9656-NOGIL/bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5%2B-99d9656-vs-base.svg)[🧠](results/bm-20250217-3.14.0a5%2B-99d9656-NOGIL/bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5%2B-99d9656-vs-base-mem.svg) |
| [2025-02-17](results/bm-20250217-3.14.0a5%2B-99d9656) | python/99d965635ae2ac4bffdc | 99d9656 | 1.104x ↑<br>[📄](results/bm-20250217-3.14.0a5%2B-99d9656/bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5%2B-99d9656-vs-3.12.6.md)[📈](results/bm-20250217-3.14.0a5%2B-99d9656/bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5%2B-99d9656-vs-3.12.6.svg) | 1.062x ↑<br>[📄](results/bm-20250217-3.14.0a5%2B-99d9656/bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5%2B-99d9656-vs-3.13.0rc2.md)[📈](results/bm-20250217-3.14.0a5%2B-99d9656/bm-20250217-linux-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5%2B-99d9656-vs-3.13.0rc2.svg) |  |
| [2025-02-17](results/bm-20250217-3.14.0a5%2B-cfe4103) | python/cfe41037eb5293a05184 | cfe4103 | 1.138x ↑<br>[📄](results/bm-20250217-3.14.0a5%2B-cfe4103/bm-20250217-linux-x86_64-python-cfe41037eb5293a05184-3.14.0a5%2B-cfe4103-vs-3.12.6.md)[📈](results/bm-20250217-3.14.0a5%2B-cfe4103/bm-20250217-linux-x86_64-python-cfe41037eb5293a05184-3.14.0a5%2B-cfe4103-vs-3.12.6.svg) | 1.093x ↑<br>[📄](results/bm-20250217-3.14.0a5%2B-cfe4103/bm-20250217-linux-x86_64-python-cfe41037eb5293a05184-3.14.0a5%2B-cfe4103-vs-3.13.0rc2.md)[📈](results/bm-20250217-3.14.0a5%2B-cfe4103/bm-20250217-linux-x86_64-python-cfe41037eb5293a05184-3.14.0a5%2B-cfe4103-vs-3.13.0rc2.svg) |  |
| [2025-02-17](results/bm-20250217-3.14.0a5%2B-cfe4103-NOGIL) | python/cfe41037eb5293a05184 | cfe4103 (NOGIL) | 1.021x ↓<br>[📄](results/bm-20250217-3.14.0a5%2B-cfe4103-NOGIL/bm-20250217-linux-x86_64-python-cfe41037eb5293a05184-3.14.0a5%2B-cfe4103-vs-3.12.6.md)[📈](results/bm-20250217-3.14.0a5%2B-cfe4103-NOGIL/bm-20250217-linux-x86_64-python-cfe41037eb5293a05184-3.14.0a5%2B-cfe4103-vs-3.12.6.svg) | 1.058x ↓<br>[📄](results/bm-20250217-3.14.0a5%2B-cfe4103-NOGIL/bm-20250217-linux-x86_64-python-cfe41037eb5293a05184-3.14.0a5%2B-cfe4103-vs-3.13.0rc2.md)[📈](results/bm-20250217-3.14.0a5%2B-cfe4103-NOGIL/bm-20250217-linux-x86_64-python-cfe41037eb5293a05184-3.14.0a5%2B-cfe4103-vs-3.13.0rc2.svg) | 1.137x ↓<br>[📄](results/bm-20250217-3.14.0a5%2B-cfe4103-NOGIL/bm-20250217-linux-x86_64-python-cfe41037eb5293a05184-3.14.0a5%2B-cfe4103-vs-base.md)[📈](results/bm-20250217-3.14.0a5%2B-cfe4103-NOGIL/bm-20250217-linux-x86_64-python-cfe41037eb5293a05184-3.14.0a5%2B-cfe4103-vs-base.svg)[🧠](results/bm-20250217-3.14.0a5%2B-cfe4103-NOGIL/bm-20250217-linux-x86_64-python-cfe41037eb5293a05184-3.14.0a5%2B-cfe4103-vs-base-mem.svg) |
| [2025-02-16](results/bm-20250216-3.14.0a5%2B-359c7dd) | python/359c7dde3bb074e02968 | 359c7dd | 1.131x ↑<br>[📄](results/bm-20250216-3.14.0a5%2B-359c7dd/bm-20250216-linux-x86_64-python-359c7dde3bb074e02968-3.14.0a5%2B-359c7dd-vs-3.12.6.md)[📈](results/bm-20250216-3.14.0a5%2B-359c7dd/bm-20250216-linux-x86_64-python-359c7dde3bb074e02968-3.14.0a5%2B-359c7dd-vs-3.12.6.svg) | 1.088x ↑<br>[📄](results/bm-20250216-3.14.0a5%2B-359c7dd/bm-20250216-linux-x86_64-python-359c7dde3bb074e02968-3.14.0a5%2B-359c7dd-vs-3.13.0rc2.md)[📈](results/bm-20250216-3.14.0a5%2B-359c7dd/bm-20250216-linux-x86_64-python-359c7dde3bb074e02968-3.14.0a5%2B-359c7dd-vs-3.13.0rc2.svg) |  |
| [2025-02-16](results/bm-20250216-3.14.0a5%2B-359c7dd-NOGIL) | python/359c7dde3bb074e02968 | 359c7dd (NOGIL) | 1.016x ↓<br>[📄](results/bm-20250216-3.14.0a5%2B-359c7dd-NOGIL/bm-20250216-linux-x86_64-python-359c7dde3bb074e02968-3.14.0a5%2B-359c7dd-vs-3.12.6.md)[📈](results/bm-20250216-3.14.0a5%2B-359c7dd-NOGIL/bm-20250216-linux-x86_64-python-359c7dde3bb074e02968-3.14.0a5%2B-359c7dd-vs-3.12.6.svg) | 1.053x ↓<br>[📄](results/bm-20250216-3.14.0a5%2B-359c7dd-NOGIL/bm-20250216-linux-x86_64-python-359c7dde3bb074e02968-3.14.0a5%2B-359c7dd-vs-3.13.0rc2.md)[📈](results/bm-20250216-3.14.0a5%2B-359c7dd-NOGIL/bm-20250216-linux-x86_64-python-359c7dde3bb074e02968-3.14.0a5%2B-359c7dd-vs-3.13.0rc2.svg) | 1.133x ↓<br>[📄](results/bm-20250216-3.14.0a5%2B-359c7dd-NOGIL/bm-20250216-linux-x86_64-python-359c7dde3bb074e02968-3.14.0a5%2B-359c7dd-vs-base.md)[📈](results/bm-20250216-3.14.0a5%2B-359c7dd-NOGIL/bm-20250216-linux-x86_64-python-359c7dde3bb074e02968-3.14.0a5%2B-359c7dd-vs-base.svg)[🧠](results/bm-20250216-3.14.0a5%2B-359c7dd-NOGIL/bm-20250216-linux-x86_64-python-359c7dde3bb074e02968-3.14.0a5%2B-359c7dd-vs-base-mem.svg) |
| [2025-02-14](results/bm-20250214-3.14.0a5%2B-39cd972) | python/39cd9728a6770d8fe793 | 39cd972 | 1.074x ↑<br>[📄](results/bm-20250214-3.14.0a5%2B-39cd972/bm-20250214-linux-x86_64-python-39cd9728a6770d8fe793-3.14.0a5%2B-39cd972-vs-3.12.6.md)[📈](results/bm-20250214-3.14.0a5%2B-39cd972/bm-20250214-linux-x86_64-python-39cd9728a6770d8fe793-3.14.0a5%2B-39cd972-vs-3.12.6.svg) | 1.029x ↑<br>[📄](results/bm-20250214-3.14.0a5%2B-39cd972/bm-20250214-linux-x86_64-python-39cd9728a6770d8fe793-3.14.0a5%2B-39cd972-vs-3.13.0rc2.md)[📈](results/bm-20250214-3.14.0a5%2B-39cd972/bm-20250214-linux-x86_64-python-39cd9728a6770d8fe793-3.14.0a5%2B-39cd972-vs-3.13.0rc2.svg) |  |
| [2025-02-14](results/bm-20250214-3.14.0a5%2B-39cd972-NOGIL) | python/39cd9728a6770d8fe793 | 39cd972 (NOGIL) | 1.020x ↓<br>[📄](results/bm-20250214-3.14.0a5%2B-39cd972-NOGIL/bm-20250214-linux-x86_64-python-39cd9728a6770d8fe793-3.14.0a5%2B-39cd972-vs-3.12.6.md)[📈](results/bm-20250214-3.14.0a5%2B-39cd972-NOGIL/bm-20250214-linux-x86_64-python-39cd9728a6770d8fe793-3.14.0a5%2B-39cd972-vs-3.12.6.svg) | 1.055x ↓<br>[📄](results/bm-20250214-3.14.0a5%2B-39cd972-NOGIL/bm-20250214-linux-x86_64-python-39cd9728a6770d8fe793-3.14.0a5%2B-39cd972-vs-3.13.0rc2.md)[📈](results/bm-20250214-3.14.0a5%2B-39cd972-NOGIL/bm-20250214-linux-x86_64-python-39cd9728a6770d8fe793-3.14.0a5%2B-39cd972-vs-3.13.0rc2.svg) | 1.080x ↓<br>[📄](results/bm-20250214-3.14.0a5%2B-39cd972-NOGIL/bm-20250214-linux-x86_64-python-39cd9728a6770d8fe793-3.14.0a5%2B-39cd972-vs-base.md)[📈](results/bm-20250214-3.14.0a5%2B-39cd972-NOGIL/bm-20250214-linux-x86_64-python-39cd9728a6770d8fe793-3.14.0a5%2B-39cd972-vs-base.svg)[🧠](results/bm-20250214-3.14.0a5%2B-39cd972-NOGIL/bm-20250214-linux-x86_64-python-39cd9728a6770d8fe793-3.14.0a5%2B-39cd972-vs-base-mem.svg) |

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-02-17](results/bm-20250217-3.14.0a5%2B-99d9656-NOGIL) | python/99d965635ae2ac4bffdc | 99d9656 (NOGIL) | 1.048x ↓<br>[📄](results/bm-20250217-3.14.0a5%2B-99d9656-NOGIL/bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5%2B-99d9656-vs-3.12.6.md)[📈](results/bm-20250217-3.14.0a5%2B-99d9656-NOGIL/bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5%2B-99d9656-vs-3.12.6.svg) | 1.080x ↓<br>[📄](results/bm-20250217-3.14.0a5%2B-99d9656-NOGIL/bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5%2B-99d9656-vs-3.13.0rc2.md)[📈](results/bm-20250217-3.14.0a5%2B-99d9656-NOGIL/bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5%2B-99d9656-vs-3.13.0rc2.svg) | 1.126x ↓<br>[📄](results/bm-20250217-3.14.0a5%2B-99d9656-NOGIL/bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5%2B-99d9656-vs-base.md)[📈](results/bm-20250217-3.14.0a5%2B-99d9656-NOGIL/bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5%2B-99d9656-vs-base.svg)[🧠](results/bm-20250217-3.14.0a5%2B-99d9656-NOGIL/bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5%2B-99d9656-vs-base-mem.svg) |
| [2025-02-17](results/bm-20250217-3.14.0a5%2B-99d9656) | python/99d965635ae2ac4bffdc | 99d9656 | 1.088x ↑<br>[📄](results/bm-20250217-3.14.0a5%2B-99d9656/bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5%2B-99d9656-vs-3.12.6.md)[📈](results/bm-20250217-3.14.0a5%2B-99d9656/bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5%2B-99d9656-vs-3.12.6.svg) | 1.048x ↑<br>[📄](results/bm-20250217-3.14.0a5%2B-99d9656/bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5%2B-99d9656-vs-3.13.0rc2.md)[📈](results/bm-20250217-3.14.0a5%2B-99d9656/bm-20250217-vultr-x86_64-python-99d965635ae2ac4bffdc-3.14.0a5%2B-99d9656-vs-3.13.0rc2.svg) |  |
| [2025-02-17](results/bm-20250217-3.14.0a5%2B-cfe4103) | python/cfe41037eb5293a05184 | cfe4103 | 1.092x ↑<br>[📄](results/bm-20250217-3.14.0a5%2B-cfe4103/bm-20250217-vultr-x86_64-python-cfe41037eb5293a05184-3.14.0a5%2B-cfe4103-vs-3.12.6.md)[📈](results/bm-20250217-3.14.0a5%2B-cfe4103/bm-20250217-vultr-x86_64-python-cfe41037eb5293a05184-3.14.0a5%2B-cfe4103-vs-3.12.6.svg) | 1.052x ↑<br>[📄](results/bm-20250217-3.14.0a5%2B-cfe4103/bm-20250217-vultr-x86_64-python-cfe41037eb5293a05184-3.14.0a5%2B-cfe4103-vs-3.13.0rc2.md)[📈](results/bm-20250217-3.14.0a5%2B-cfe4103/bm-20250217-vultr-x86_64-python-cfe41037eb5293a05184-3.14.0a5%2B-cfe4103-vs-3.13.0rc2.svg) |  |
| [2025-02-17](results/bm-20250217-3.14.0a5%2B-cfe4103-NOGIL) | python/cfe41037eb5293a05184 | cfe4103 (NOGIL) | 1.047x ↓<br>[📄](results/bm-20250217-3.14.0a5%2B-cfe4103-NOGIL/bm-20250217-vultr-x86_64-python-cfe41037eb5293a05184-3.14.0a5%2B-cfe4103-vs-3.12.6.md)[📈](results/bm-20250217-3.14.0a5%2B-cfe4103-NOGIL/bm-20250217-vultr-x86_64-python-cfe41037eb5293a05184-3.14.0a5%2B-cfe4103-vs-3.12.6.svg) | 1.079x ↓<br>[📄](results/bm-20250217-3.14.0a5%2B-cfe4103-NOGIL/bm-20250217-vultr-x86_64-python-cfe41037eb5293a05184-3.14.0a5%2B-cfe4103-vs-3.13.0rc2.md)[📈](results/bm-20250217-3.14.0a5%2B-cfe4103-NOGIL/bm-20250217-vultr-x86_64-python-cfe41037eb5293a05184-3.14.0a5%2B-cfe4103-vs-3.13.0rc2.svg) | 1.128x ↓<br>[📄](results/bm-20250217-3.14.0a5%2B-cfe4103-NOGIL/bm-20250217-vultr-x86_64-python-cfe41037eb5293a05184-3.14.0a5%2B-cfe4103-vs-base.md)[📈](results/bm-20250217-3.14.0a5%2B-cfe4103-NOGIL/bm-20250217-vultr-x86_64-python-cfe41037eb5293a05184-3.14.0a5%2B-cfe4103-vs-base.svg)[🧠](results/bm-20250217-3.14.0a5%2B-cfe4103-NOGIL/bm-20250217-vultr-x86_64-python-cfe41037eb5293a05184-3.14.0a5%2B-cfe4103-vs-base-mem.svg) |
| [2025-02-16](results/bm-20250216-3.14.0a5%2B-359c7dd) | python/359c7dde3bb074e02968 | 359c7dd | 1.094x ↑<br>[📄](results/bm-20250216-3.14.0a5%2B-359c7dd/bm-20250216-vultr-x86_64-python-359c7dde3bb074e02968-3.14.0a5%2B-359c7dd-vs-3.12.6.md)[📈](results/bm-20250216-3.14.0a5%2B-359c7dd/bm-20250216-vultr-x86_64-python-359c7dde3bb074e02968-3.14.0a5%2B-359c7dd-vs-3.12.6.svg) | 1.054x ↑<br>[📄](results/bm-20250216-3.14.0a5%2B-359c7dd/bm-20250216-vultr-x86_64-python-359c7dde3bb074e02968-3.14.0a5%2B-359c7dd-vs-3.13.0rc2.md)[📈](results/bm-20250216-3.14.0a5%2B-359c7dd/bm-20250216-vultr-x86_64-python-359c7dde3bb074e02968-3.14.0a5%2B-359c7dd-vs-3.13.0rc2.svg) |  |
| [2025-02-16](results/bm-20250216-3.14.0a5%2B-359c7dd-NOGIL) | python/359c7dde3bb074e02968 | 359c7dd (NOGIL) | 1.048x ↓<br>[📄](results/bm-20250216-3.14.0a5%2B-359c7dd-NOGIL/bm-20250216-vultr-x86_64-python-359c7dde3bb074e02968-3.14.0a5%2B-359c7dd-vs-3.12.6.md)[📈](results/bm-20250216-3.14.0a5%2B-359c7dd-NOGIL/bm-20250216-vultr-x86_64-python-359c7dde3bb074e02968-3.14.0a5%2B-359c7dd-vs-3.12.6.svg) | 1.080x ↓<br>[📄](results/bm-20250216-3.14.0a5%2B-359c7dd-NOGIL/bm-20250216-vultr-x86_64-python-359c7dde3bb074e02968-3.14.0a5%2B-359c7dd-vs-3.13.0rc2.md)[📈](results/bm-20250216-3.14.0a5%2B-359c7dd-NOGIL/bm-20250216-vultr-x86_64-python-359c7dde3bb074e02968-3.14.0a5%2B-359c7dd-vs-3.13.0rc2.svg) | 1.130x ↓<br>[📄](results/bm-20250216-3.14.0a5%2B-359c7dd-NOGIL/bm-20250216-vultr-x86_64-python-359c7dde3bb074e02968-3.14.0a5%2B-359c7dd-vs-base.md)[📈](results/bm-20250216-3.14.0a5%2B-359c7dd-NOGIL/bm-20250216-vultr-x86_64-python-359c7dde3bb074e02968-3.14.0a5%2B-359c7dd-vs-base.svg)[🧠](results/bm-20250216-3.14.0a5%2B-359c7dd-NOGIL/bm-20250216-vultr-x86_64-python-359c7dde3bb074e02968-3.14.0a5%2B-359c7dd-vs-base-mem.svg) |
| [2025-02-14](results/bm-20250214-3.14.0a5%2B-39cd972) | python/39cd9728a6770d8fe793 | 39cd972 | 1.088x ↑<br>[📄](results/bm-20250214-3.14.0a5%2B-39cd972/bm-20250214-vultr-x86_64-python-39cd9728a6770d8fe793-3.14.0a5%2B-39cd972-vs-3.12.6.md)[📈](results/bm-20250214-3.14.0a5%2B-39cd972/bm-20250214-vultr-x86_64-python-39cd9728a6770d8fe793-3.14.0a5%2B-39cd972-vs-3.12.6.svg) | 1.048x ↑<br>[📄](results/bm-20250214-3.14.0a5%2B-39cd972/bm-20250214-vultr-x86_64-python-39cd9728a6770d8fe793-3.14.0a5%2B-39cd972-vs-3.13.0rc2.md)[📈](results/bm-20250214-3.14.0a5%2B-39cd972/bm-20250214-vultr-x86_64-python-39cd9728a6770d8fe793-3.14.0a5%2B-39cd972-vs-3.13.0rc2.svg) |  |
| [2025-02-14](results/bm-20250214-3.14.0a5%2B-39cd972-NOGIL) | python/39cd9728a6770d8fe793 | 39cd972 (NOGIL) | 1.048x ↓<br>[📄](results/bm-20250214-3.14.0a5%2B-39cd972-NOGIL/bm-20250214-vultr-x86_64-python-39cd9728a6770d8fe793-3.14.0a5%2B-39cd972-vs-3.12.6.md)[📈](results/bm-20250214-3.14.0a5%2B-39cd972-NOGIL/bm-20250214-vultr-x86_64-python-39cd9728a6770d8fe793-3.14.0a5%2B-39cd972-vs-3.12.6.svg) | 1.080x ↓<br>[📄](results/bm-20250214-3.14.0a5%2B-39cd972-NOGIL/bm-20250214-vultr-x86_64-python-39cd9728a6770d8fe793-3.14.0a5%2B-39cd972-vs-3.13.0rc2.md)[📈](results/bm-20250214-3.14.0a5%2B-39cd972-NOGIL/bm-20250214-vultr-x86_64-python-39cd9728a6770d8fe793-3.14.0a5%2B-39cd972-vs-3.13.0rc2.svg) | 1.126x ↓<br>[📄](results/bm-20250214-3.14.0a5%2B-39cd972-NOGIL/bm-20250214-vultr-x86_64-python-39cd9728a6770d8fe793-3.14.0a5%2B-39cd972-vs-base.md)[📈](results/bm-20250214-3.14.0a5%2B-39cd972-NOGIL/bm-20250214-vultr-x86_64-python-39cd9728a6770d8fe793-3.14.0a5%2B-39cd972-vs-base.svg)[🧠](results/bm-20250214-3.14.0a5%2B-39cd972-NOGIL/bm-20250214-vultr-x86_64-python-39cd9728a6770d8fe793-3.14.0a5%2B-39cd972-vs-base-mem.svg) |
| [2025-02-14](results/bm-20250214-3.14.0a5%2B-c00cd86-NOGIL) | DinoV/noclock_clear | c00cd86 (NOGIL) | 1.047x ↓<br>[📄](results/bm-20250214-3.14.0a5%2B-c00cd86-NOGIL/bm-20250214-vultr-x86_64-DinoV-noclock_clear-3.14.0a5%2B-c00cd86-vs-3.12.6.md)[📈](results/bm-20250214-3.14.0a5%2B-c00cd86-NOGIL/bm-20250214-vultr-x86_64-DinoV-noclock_clear-3.14.0a5%2B-c00cd86-vs-3.12.6.svg) | 1.079x ↓<br>[📄](results/bm-20250214-3.14.0a5%2B-c00cd86-NOGIL/bm-20250214-vultr-x86_64-DinoV-noclock_clear-3.14.0a5%2B-c00cd86-vs-3.13.0rc2.md)[📈](results/bm-20250214-3.14.0a5%2B-c00cd86-NOGIL/bm-20250214-vultr-x86_64-DinoV-noclock_clear-3.14.0a5%2B-c00cd86-vs-3.13.0rc2.svg) | 1.000x ↑<br>[📄](results/bm-20250214-3.14.0a5%2B-c00cd86-NOGIL/bm-20250214-vultr-x86_64-DinoV-noclock_clear-3.14.0a5%2B-c00cd86-vs-base.md)[📈](results/bm-20250214-3.14.0a5%2B-c00cd86-NOGIL/bm-20250214-vultr-x86_64-DinoV-noclock_clear-3.14.0a5%2B-c00cd86-vs-base.svg)[🧠](results/bm-20250214-3.14.0a5%2B-c00cd86-NOGIL/bm-20250214-vultr-x86_64-DinoV-noclock_clear-3.14.0a5%2B-c00cd86-vs-base-mem.svg) |


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
