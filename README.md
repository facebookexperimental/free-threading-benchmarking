# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
[Most recent pystats on main (5ec4bf8)](results/bm-20250222-3.14.0a5%2B-5ec4bf8-PYTHON_UOPS/bm-20250222-linux-x86_64-python-5ec4bf86b7f4455432ae-3.14.0a5%2B-5ec4bf8-pystats.md)

## linux x86_64 (linux)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-02-24](results/bm-20250224-3.14.0a5%2B-3a555f0) | python/3a555f09f387a0212e59 | 3a555f0 | 1.089x ↑<br>[📄](results/bm-20250224-3.14.0a5%2B-3a555f0/bm-20250224-linux-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-3.12.6.md)[📈](results/bm-20250224-3.14.0a5%2B-3a555f0/bm-20250224-linux-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-3.12.6.svg) | 1.048x ↑<br>[📄](results/bm-20250224-3.14.0a5%2B-3a555f0/bm-20250224-linux-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-3.13.0rc2.md)[📈](results/bm-20250224-3.14.0a5%2B-3a555f0/bm-20250224-linux-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-3.13.0rc2.svg) |  |
| [2025-02-24](results/bm-20250224-3.14.0a5%2B-3a555f0-NOGIL) | python/3a555f09f387a0212e59 | 3a555f0 (NOGIL) | 1.018x ↓<br>[📄](results/bm-20250224-3.14.0a5%2B-3a555f0-NOGIL/bm-20250224-linux-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-3.12.6.md)[📈](results/bm-20250224-3.14.0a5%2B-3a555f0-NOGIL/bm-20250224-linux-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-3.12.6.svg) | 1.054x ↓<br>[📄](results/bm-20250224-3.14.0a5%2B-3a555f0-NOGIL/bm-20250224-linux-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-3.13.0rc2.md)[📈](results/bm-20250224-3.14.0a5%2B-3a555f0-NOGIL/bm-20250224-linux-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-3.13.0rc2.svg) | 1.098x ↓<br>[📄](results/bm-20250224-3.14.0a5%2B-3a555f0-NOGIL/bm-20250224-linux-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-base.md)[📈](results/bm-20250224-3.14.0a5%2B-3a555f0-NOGIL/bm-20250224-linux-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-base.svg)[🧠](results/bm-20250224-3.14.0a5%2B-3a555f0-NOGIL/bm-20250224-linux-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-base-mem.svg) |
| [2025-02-24](results/bm-20250224-3.14.0a5%2B-cd6abe2) | python/cd6abe27a2582786da7b | cd6abe2 | 1.132x ↑<br>[📄](results/bm-20250224-3.14.0a5%2B-cd6abe2/bm-20250224-linux-x86_64-python-cd6abe27a2582786da7b-3.14.0a5%2B-cd6abe2-vs-3.12.6.md)[📈](results/bm-20250224-3.14.0a5%2B-cd6abe2/bm-20250224-linux-x86_64-python-cd6abe27a2582786da7b-3.14.0a5%2B-cd6abe2-vs-3.12.6.svg) | 1.090x ↑<br>[📄](results/bm-20250224-3.14.0a5%2B-cd6abe2/bm-20250224-linux-x86_64-python-cd6abe27a2582786da7b-3.14.0a5%2B-cd6abe2-vs-3.13.0rc2.md)[📈](results/bm-20250224-3.14.0a5%2B-cd6abe2/bm-20250224-linux-x86_64-python-cd6abe27a2582786da7b-3.14.0a5%2B-cd6abe2-vs-3.13.0rc2.svg) |  |
| [2025-02-24](results/bm-20250224-3.14.0a5%2B-cd6abe2-NOGIL) | python/cd6abe27a2582786da7b | cd6abe2 (NOGIL) | 1.003x ↑<br>[📄](results/bm-20250224-3.14.0a5%2B-cd6abe2-NOGIL/bm-20250224-linux-x86_64-python-cd6abe27a2582786da7b-3.14.0a5%2B-cd6abe2-vs-3.12.6.md)[📈](results/bm-20250224-3.14.0a5%2B-cd6abe2-NOGIL/bm-20250224-linux-x86_64-python-cd6abe27a2582786da7b-3.14.0a5%2B-cd6abe2-vs-3.12.6.svg) | 1.035x ↓<br>[📄](results/bm-20250224-3.14.0a5%2B-cd6abe2-NOGIL/bm-20250224-linux-x86_64-python-cd6abe27a2582786da7b-3.14.0a5%2B-cd6abe2-vs-3.13.0rc2.md)[📈](results/bm-20250224-3.14.0a5%2B-cd6abe2-NOGIL/bm-20250224-linux-x86_64-python-cd6abe27a2582786da7b-3.14.0a5%2B-cd6abe2-vs-3.13.0rc2.svg) | 1.113x ↓<br>[📄](results/bm-20250224-3.14.0a5%2B-cd6abe2-NOGIL/bm-20250224-linux-x86_64-python-cd6abe27a2582786da7b-3.14.0a5%2B-cd6abe2-vs-base.md)[📈](results/bm-20250224-3.14.0a5%2B-cd6abe2-NOGIL/bm-20250224-linux-x86_64-python-cd6abe27a2582786da7b-3.14.0a5%2B-cd6abe2-vs-base.svg)[🧠](results/bm-20250224-3.14.0a5%2B-cd6abe2-NOGIL/bm-20250224-linux-x86_64-python-cd6abe27a2582786da7b-3.14.0a5%2B-cd6abe2-vs-base-mem.svg) |
| [2025-02-22](results/bm-20250222-3.14.0a5%2B-5ec4bf8) | python/5ec4bf86b7f4455432ae | 5ec4bf8 | 1.139x ↑<br>[📄](results/bm-20250222-3.14.0a5%2B-5ec4bf8/bm-20250222-linux-x86_64-python-5ec4bf86b7f4455432ae-3.14.0a5%2B-5ec4bf8-vs-3.12.6.md)[📈](results/bm-20250222-3.14.0a5%2B-5ec4bf8/bm-20250222-linux-x86_64-python-5ec4bf86b7f4455432ae-3.14.0a5%2B-5ec4bf8-vs-3.12.6.svg) | 1.097x ↑<br>[📄](results/bm-20250222-3.14.0a5%2B-5ec4bf8/bm-20250222-linux-x86_64-python-5ec4bf86b7f4455432ae-3.14.0a5%2B-5ec4bf8-vs-3.13.0rc2.md)[📈](results/bm-20250222-3.14.0a5%2B-5ec4bf8/bm-20250222-linux-x86_64-python-5ec4bf86b7f4455432ae-3.14.0a5%2B-5ec4bf8-vs-3.13.0rc2.svg) |  |
| [2025-02-22](results/bm-20250222-3.14.0a5%2B-5ec4bf8-NOGIL) | python/5ec4bf86b7f4455432ae | 5ec4bf8 (NOGIL) | 1.026x ↑<br>[📄](results/bm-20250222-3.14.0a5%2B-5ec4bf8-NOGIL/bm-20250222-linux-x86_64-python-5ec4bf86b7f4455432ae-3.14.0a5%2B-5ec4bf8-vs-3.12.6.md)[📈](results/bm-20250222-3.14.0a5%2B-5ec4bf8-NOGIL/bm-20250222-linux-x86_64-python-5ec4bf86b7f4455432ae-3.14.0a5%2B-5ec4bf8-vs-3.12.6.svg) | 1.012x ↓<br>[📄](results/bm-20250222-3.14.0a5%2B-5ec4bf8-NOGIL/bm-20250222-linux-x86_64-python-5ec4bf86b7f4455432ae-3.14.0a5%2B-5ec4bf8-vs-3.13.0rc2.md)[📈](results/bm-20250222-3.14.0a5%2B-5ec4bf8-NOGIL/bm-20250222-linux-x86_64-python-5ec4bf86b7f4455432ae-3.14.0a5%2B-5ec4bf8-vs-3.13.0rc2.svg) | 1.102x ↓<br>[📄](results/bm-20250222-3.14.0a5%2B-5ec4bf8-NOGIL/bm-20250222-linux-x86_64-python-5ec4bf86b7f4455432ae-3.14.0a5%2B-5ec4bf8-vs-base.md)[📈](results/bm-20250222-3.14.0a5%2B-5ec4bf8-NOGIL/bm-20250222-linux-x86_64-python-5ec4bf86b7f4455432ae-3.14.0a5%2B-5ec4bf8-vs-base.svg)[🧠](results/bm-20250222-3.14.0a5%2B-5ec4bf8-NOGIL/bm-20250222-linux-x86_64-python-5ec4bf86b7f4455432ae-3.14.0a5%2B-5ec4bf8-vs-base-mem.svg) |
| [2025-02-21](results/bm-20250221-3.14.0a5%2B-38642bf) | python/38642bff139bde5c0118 | 38642bf | 1.064x ↑<br>[📄](results/bm-20250221-3.14.0a5%2B-38642bf/bm-20250221-linux-x86_64-python-38642bff139bde5c0118-3.14.0a5%2B-38642bf-vs-3.12.6.md)[📈](results/bm-20250221-3.14.0a5%2B-38642bf/bm-20250221-linux-x86_64-python-38642bff139bde5c0118-3.14.0a5%2B-38642bf-vs-3.12.6.svg) | 1.017x ↑<br>[📄](results/bm-20250221-3.14.0a5%2B-38642bf/bm-20250221-linux-x86_64-python-38642bff139bde5c0118-3.14.0a5%2B-38642bf-vs-3.13.0rc2.md)[📈](results/bm-20250221-3.14.0a5%2B-38642bf/bm-20250221-linux-x86_64-python-38642bff139bde5c0118-3.14.0a5%2B-38642bf-vs-3.13.0rc2.svg) |  |
| [2025-02-21](results/bm-20250221-3.14.0a5%2B-38642bf-NOGIL) | python/38642bff139bde5c0118 | 38642bf (NOGIL) | 1.056x ↓<br>[📄](results/bm-20250221-3.14.0a5%2B-38642bf-NOGIL/bm-20250221-linux-x86_64-python-38642bff139bde5c0118-3.14.0a5%2B-38642bf-vs-3.12.6.md)[📈](results/bm-20250221-3.14.0a5%2B-38642bf-NOGIL/bm-20250221-linux-x86_64-python-38642bff139bde5c0118-3.14.0a5%2B-38642bf-vs-3.12.6.svg) | 1.089x ↓<br>[📄](results/bm-20250221-3.14.0a5%2B-38642bf-NOGIL/bm-20250221-linux-x86_64-python-38642bff139bde5c0118-3.14.0a5%2B-38642bf-vs-3.13.0rc2.md)[📈](results/bm-20250221-3.14.0a5%2B-38642bf-NOGIL/bm-20250221-linux-x86_64-python-38642bff139bde5c0118-3.14.0a5%2B-38642bf-vs-3.13.0rc2.svg) | 1.103x ↓<br>[📄](results/bm-20250221-3.14.0a5%2B-38642bf-NOGIL/bm-20250221-linux-x86_64-python-38642bff139bde5c0118-3.14.0a5%2B-38642bf-vs-base.md)[📈](results/bm-20250221-3.14.0a5%2B-38642bf-NOGIL/bm-20250221-linux-x86_64-python-38642bff139bde5c0118-3.14.0a5%2B-38642bf-vs-base.svg)[🧠](results/bm-20250221-3.14.0a5%2B-38642bf-NOGIL/bm-20250221-linux-x86_64-python-38642bff139bde5c0118-3.14.0a5%2B-38642bf-vs-base-mem.svg) |

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-02-24](results/bm-20250224-3.14.0a5%2B-3a555f0) | python/3a555f09f387a0212e59 | 3a555f0 | 1.086x ↑<br>[📄](results/bm-20250224-3.14.0a5%2B-3a555f0/bm-20250224-vultr-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-3.12.6.md)[📈](results/bm-20250224-3.14.0a5%2B-3a555f0/bm-20250224-vultr-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-3.12.6.svg) | 1.046x ↑<br>[📄](results/bm-20250224-3.14.0a5%2B-3a555f0/bm-20250224-vultr-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-3.13.0rc2.md)[📈](results/bm-20250224-3.14.0a5%2B-3a555f0/bm-20250224-vultr-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-3.13.0rc2.svg) |  |
| [2025-02-24](results/bm-20250224-3.14.0a5%2B-3a555f0-NOGIL) | python/3a555f09f387a0212e59 | 3a555f0 (NOGIL) | 1.043x ↓<br>[📄](results/bm-20250224-3.14.0a5%2B-3a555f0-NOGIL/bm-20250224-vultr-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-3.12.6.md)[📈](results/bm-20250224-3.14.0a5%2B-3a555f0-NOGIL/bm-20250224-vultr-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-3.12.6.svg) | 1.075x ↓<br>[📄](results/bm-20250224-3.14.0a5%2B-3a555f0-NOGIL/bm-20250224-vultr-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-3.13.0rc2.md)[📈](results/bm-20250224-3.14.0a5%2B-3a555f0-NOGIL/bm-20250224-vultr-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-3.13.0rc2.svg) | 1.119x ↓<br>[📄](results/bm-20250224-3.14.0a5%2B-3a555f0-NOGIL/bm-20250224-vultr-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-base.md)[📈](results/bm-20250224-3.14.0a5%2B-3a555f0-NOGIL/bm-20250224-vultr-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-base.svg)[🧠](results/bm-20250224-3.14.0a5%2B-3a555f0-NOGIL/bm-20250224-vultr-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-base-mem.svg) |
| [2025-02-24](results/bm-20250224-3.14.0a5%2B-cd6abe2) | python/cd6abe27a2582786da7b | cd6abe2 | 1.088x ↑<br>[📄](results/bm-20250224-3.14.0a5%2B-cd6abe2/bm-20250224-vultr-x86_64-python-cd6abe27a2582786da7b-3.14.0a5%2B-cd6abe2-vs-3.12.6.md)[📈](results/bm-20250224-3.14.0a5%2B-cd6abe2/bm-20250224-vultr-x86_64-python-cd6abe27a2582786da7b-3.14.0a5%2B-cd6abe2-vs-3.12.6.svg) | 1.048x ↑<br>[📄](results/bm-20250224-3.14.0a5%2B-cd6abe2/bm-20250224-vultr-x86_64-python-cd6abe27a2582786da7b-3.14.0a5%2B-cd6abe2-vs-3.13.0rc2.md)[📈](results/bm-20250224-3.14.0a5%2B-cd6abe2/bm-20250224-vultr-x86_64-python-cd6abe27a2582786da7b-3.14.0a5%2B-cd6abe2-vs-3.13.0rc2.svg) |  |
| [2025-02-24](results/bm-20250224-3.14.0a5%2B-cd6abe2-NOGIL) | python/cd6abe27a2582786da7b | cd6abe2 (NOGIL) | 1.045x ↓<br>[📄](results/bm-20250224-3.14.0a5%2B-cd6abe2-NOGIL/bm-20250224-vultr-x86_64-python-cd6abe27a2582786da7b-3.14.0a5%2B-cd6abe2-vs-3.12.6.md)[📈](results/bm-20250224-3.14.0a5%2B-cd6abe2-NOGIL/bm-20250224-vultr-x86_64-python-cd6abe27a2582786da7b-3.14.0a5%2B-cd6abe2-vs-3.12.6.svg) | 1.077x ↓<br>[📄](results/bm-20250224-3.14.0a5%2B-cd6abe2-NOGIL/bm-20250224-vultr-x86_64-python-cd6abe27a2582786da7b-3.14.0a5%2B-cd6abe2-vs-3.13.0rc2.md)[📈](results/bm-20250224-3.14.0a5%2B-cd6abe2-NOGIL/bm-20250224-vultr-x86_64-python-cd6abe27a2582786da7b-3.14.0a5%2B-cd6abe2-vs-3.13.0rc2.svg) | 1.123x ↓<br>[📄](results/bm-20250224-3.14.0a5%2B-cd6abe2-NOGIL/bm-20250224-vultr-x86_64-python-cd6abe27a2582786da7b-3.14.0a5%2B-cd6abe2-vs-base.md)[📈](results/bm-20250224-3.14.0a5%2B-cd6abe2-NOGIL/bm-20250224-vultr-x86_64-python-cd6abe27a2582786da7b-3.14.0a5%2B-cd6abe2-vs-base.svg)[🧠](results/bm-20250224-3.14.0a5%2B-cd6abe2-NOGIL/bm-20250224-vultr-x86_64-python-cd6abe27a2582786da7b-3.14.0a5%2B-cd6abe2-vs-base-mem.svg) |
| [2025-02-22](results/bm-20250222-3.14.0a5%2B-5ec4bf8) | python/5ec4bf86b7f4455432ae | 5ec4bf8 | 1.090x ↑<br>[📄](results/bm-20250222-3.14.0a5%2B-5ec4bf8/bm-20250222-vultr-x86_64-python-5ec4bf86b7f4455432ae-3.14.0a5%2B-5ec4bf8-vs-3.12.6.md)[📈](results/bm-20250222-3.14.0a5%2B-5ec4bf8/bm-20250222-vultr-x86_64-python-5ec4bf86b7f4455432ae-3.14.0a5%2B-5ec4bf8-vs-3.12.6.svg) | 1.050x ↑<br>[📄](results/bm-20250222-3.14.0a5%2B-5ec4bf8/bm-20250222-vultr-x86_64-python-5ec4bf86b7f4455432ae-3.14.0a5%2B-5ec4bf8-vs-3.13.0rc2.md)[📈](results/bm-20250222-3.14.0a5%2B-5ec4bf8/bm-20250222-vultr-x86_64-python-5ec4bf86b7f4455432ae-3.14.0a5%2B-5ec4bf8-vs-3.13.0rc2.svg) |  |
| [2025-02-22](results/bm-20250222-3.14.0a5%2B-5ec4bf8-NOGIL) | python/5ec4bf86b7f4455432ae | 5ec4bf8 (NOGIL) | 1.044x ↓<br>[📄](results/bm-20250222-3.14.0a5%2B-5ec4bf8-NOGIL/bm-20250222-vultr-x86_64-python-5ec4bf86b7f4455432ae-3.14.0a5%2B-5ec4bf8-vs-3.12.6.md)[📈](results/bm-20250222-3.14.0a5%2B-5ec4bf8-NOGIL/bm-20250222-vultr-x86_64-python-5ec4bf86b7f4455432ae-3.14.0a5%2B-5ec4bf8-vs-3.12.6.svg) | 1.076x ↓<br>[📄](results/bm-20250222-3.14.0a5%2B-5ec4bf8-NOGIL/bm-20250222-vultr-x86_64-python-5ec4bf86b7f4455432ae-3.14.0a5%2B-5ec4bf8-vs-3.13.0rc2.md)[📈](results/bm-20250222-3.14.0a5%2B-5ec4bf8-NOGIL/bm-20250222-vultr-x86_64-python-5ec4bf86b7f4455432ae-3.14.0a5%2B-5ec4bf8-vs-3.13.0rc2.svg) | 1.124x ↓<br>[📄](results/bm-20250222-3.14.0a5%2B-5ec4bf8-NOGIL/bm-20250222-vultr-x86_64-python-5ec4bf86b7f4455432ae-3.14.0a5%2B-5ec4bf8-vs-base.md)[📈](results/bm-20250222-3.14.0a5%2B-5ec4bf8-NOGIL/bm-20250222-vultr-x86_64-python-5ec4bf86b7f4455432ae-3.14.0a5%2B-5ec4bf8-vs-base.svg)[🧠](results/bm-20250222-3.14.0a5%2B-5ec4bf8-NOGIL/bm-20250222-vultr-x86_64-python-5ec4bf86b7f4455432ae-3.14.0a5%2B-5ec4bf8-vs-base-mem.svg) |
| [2025-02-21](results/bm-20250221-3.14.0a5%2B-1382cfc-NOGIL) | mpage/load_fast_borrow_abs | 1382cfc (NOGIL) | 1.012x ↑<br>[📄](results/bm-20250221-3.14.0a5%2B-1382cfc-NOGIL/bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-1382cfc-vs-3.12.6.md)[📈](results/bm-20250221-3.14.0a5%2B-1382cfc-NOGIL/bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-1382cfc-vs-3.12.6.svg) | 1.021x ↓<br>[📄](results/bm-20250221-3.14.0a5%2B-1382cfc-NOGIL/bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-1382cfc-vs-3.13.0rc2.md)[📈](results/bm-20250221-3.14.0a5%2B-1382cfc-NOGIL/bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-1382cfc-vs-3.13.0rc2.svg) | 1.053x ↑<br>[📄](results/bm-20250221-3.14.0a5%2B-1382cfc-NOGIL/bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-1382cfc-vs-base.md)[📈](results/bm-20250221-3.14.0a5%2B-1382cfc-NOGIL/bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-1382cfc-vs-base.svg)[🧠](results/bm-20250221-3.14.0a5%2B-1382cfc-NOGIL/bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-1382cfc-vs-base-mem.svg) |
| [2025-02-21](results/bm-20250221-3.14.0a5%2B-38642bf) | python/38642bff139bde5c0118 | 38642bf | 1.089x ↑<br>[📄](results/bm-20250221-3.14.0a5%2B-38642bf/bm-20250221-vultr-x86_64-python-38642bff139bde5c0118-3.14.0a5%2B-38642bf-vs-3.12.6.md)[📈](results/bm-20250221-3.14.0a5%2B-38642bf/bm-20250221-vultr-x86_64-python-38642bff139bde5c0118-3.14.0a5%2B-38642bf-vs-3.12.6.svg) | 1.048x ↑<br>[📄](results/bm-20250221-3.14.0a5%2B-38642bf/bm-20250221-vultr-x86_64-python-38642bff139bde5c0118-3.14.0a5%2B-38642bf-vs-3.13.0rc2.md)[📈](results/bm-20250221-3.14.0a5%2B-38642bf/bm-20250221-vultr-x86_64-python-38642bff139bde5c0118-3.14.0a5%2B-38642bf-vs-3.13.0rc2.svg) |  |
| [2025-02-21](results/bm-20250221-3.14.0a5%2B-38642bf-NOGIL) | python/38642bff139bde5c0118 | 38642bf (NOGIL) | 1.039x ↓<br>[📄](results/bm-20250221-3.14.0a5%2B-38642bf-NOGIL/bm-20250221-vultr-x86_64-python-38642bff139bde5c0118-3.14.0a5%2B-38642bf-vs-3.12.6.md)[📈](results/bm-20250221-3.14.0a5%2B-38642bf-NOGIL/bm-20250221-vultr-x86_64-python-38642bff139bde5c0118-3.14.0a5%2B-38642bf-vs-3.12.6.svg) | 1.071x ↓<br>[📄](results/bm-20250221-3.14.0a5%2B-38642bf-NOGIL/bm-20250221-vultr-x86_64-python-38642bff139bde5c0118-3.14.0a5%2B-38642bf-vs-3.13.0rc2.md)[📈](results/bm-20250221-3.14.0a5%2B-38642bf-NOGIL/bm-20250221-vultr-x86_64-python-38642bff139bde5c0118-3.14.0a5%2B-38642bf-vs-3.13.0rc2.svg) | 1.118x ↓<br>[📄](results/bm-20250221-3.14.0a5%2B-38642bf-NOGIL/bm-20250221-vultr-x86_64-python-38642bff139bde5c0118-3.14.0a5%2B-38642bf-vs-base.md)[📈](results/bm-20250221-3.14.0a5%2B-38642bf-NOGIL/bm-20250221-vultr-x86_64-python-38642bff139bde5c0118-3.14.0a5%2B-38642bf-vs-base.svg)[🧠](results/bm-20250221-3.14.0a5%2B-38642bf-NOGIL/bm-20250221-vultr-x86_64-python-38642bff139bde5c0118-3.14.0a5%2B-38642bf-vs-base-mem.svg) |


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
