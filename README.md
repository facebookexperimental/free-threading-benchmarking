# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
[Most recent pystats on main (22a4421)](results/bm-20250111-3.14.0a3%2B-22a4421-PYTHON_UOPS/bm-20250111-vultr-x86_64-python-22a442181d5f1ac496da-3.14.0a3%2B-22a4421-pystats.md)

## linux x86_64 (linux)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-01-28](results/bm-20250128-3.14.0a4%2B-1c3bb20-NOGIL) | python/1c3bb200da77f9df30af | 1c3bb20 (NOGIL) | 1.100x ↓<br>[📄](results/bm-20250128-3.14.0a4%2B-1c3bb20-NOGIL/bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4%2B-1c3bb20-vs-3.12.6.md)[📈](results/bm-20250128-3.14.0a4%2B-1c3bb20-NOGIL/bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4%2B-1c3bb20-vs-3.12.6.svg) | 1.131x ↓<br>[📄](results/bm-20250128-3.14.0a4%2B-1c3bb20-NOGIL/bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4%2B-1c3bb20-vs-3.13.0rc2.md)[📈](results/bm-20250128-3.14.0a4%2B-1c3bb20-NOGIL/bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4%2B-1c3bb20-vs-3.13.0rc2.svg) | 1.152x ↓<br>[📄](results/bm-20250128-3.14.0a4%2B-1c3bb20-NOGIL/bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4%2B-1c3bb20-vs-base.md)[📈](results/bm-20250128-3.14.0a4%2B-1c3bb20-NOGIL/bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4%2B-1c3bb20-vs-base.svg)[🧠](results/bm-20250128-3.14.0a4%2B-1c3bb20-NOGIL/bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4%2B-1c3bb20-vs-base-mem.svg) |
| [2025-01-28](results/bm-20250128-3.14.0a4%2B-1c3bb20) | python/1c3bb200da77f9df30af | 1c3bb20 | 1.074x ↑<br>[📄](results/bm-20250128-3.14.0a4%2B-1c3bb20/bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4%2B-1c3bb20-vs-3.12.6.md)[📈](results/bm-20250128-3.14.0a4%2B-1c3bb20/bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4%2B-1c3bb20-vs-3.12.6.svg) | 1.029x ↑<br>[📄](results/bm-20250128-3.14.0a4%2B-1c3bb20/bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4%2B-1c3bb20-vs-3.13.0rc2.md)[📈](results/bm-20250128-3.14.0a4%2B-1c3bb20/bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4%2B-1c3bb20-vs-3.13.0rc2.svg) |  |
| [2025-01-26](results/bm-20250126-3.14.0a4%2B-a8dc6d6-NOGIL) | python/a8dc6d6d44a141a8f839 | a8dc6d6 (NOGIL) | 1.035x ↓<br>[📄](results/bm-20250126-3.14.0a4%2B-a8dc6d6-NOGIL/bm-20250126-linux-x86_64-python-a8dc6d6d44a141a8f839-3.14.0a4%2B-a8dc6d6-vs-3.12.6.md)[📈](results/bm-20250126-3.14.0a4%2B-a8dc6d6-NOGIL/bm-20250126-linux-x86_64-python-a8dc6d6d44a141a8f839-3.14.0a4%2B-a8dc6d6-vs-3.12.6.svg) | 1.069x ↓<br>[📄](results/bm-20250126-3.14.0a4%2B-a8dc6d6-NOGIL/bm-20250126-linux-x86_64-python-a8dc6d6d44a141a8f839-3.14.0a4%2B-a8dc6d6-vs-3.13.0rc2.md)[📈](results/bm-20250126-3.14.0a4%2B-a8dc6d6-NOGIL/bm-20250126-linux-x86_64-python-a8dc6d6d44a141a8f839-3.14.0a4%2B-a8dc6d6-vs-3.13.0rc2.svg) | 1.136x ↓<br>[📄](results/bm-20250126-3.14.0a4%2B-a8dc6d6-NOGIL/bm-20250126-linux-x86_64-python-a8dc6d6d44a141a8f839-3.14.0a4%2B-a8dc6d6-vs-base.md)[📈](results/bm-20250126-3.14.0a4%2B-a8dc6d6-NOGIL/bm-20250126-linux-x86_64-python-a8dc6d6d44a141a8f839-3.14.0a4%2B-a8dc6d6-vs-base.svg)[🧠](results/bm-20250126-3.14.0a4%2B-a8dc6d6-NOGIL/bm-20250126-linux-x86_64-python-a8dc6d6d44a141a8f839-3.14.0a4%2B-a8dc6d6-vs-base-mem.svg) |
| [2025-01-26](results/bm-20250126-3.14.0a4%2B-a8dc6d6) | python/a8dc6d6d44a141a8f839 | a8dc6d6 | 1.121x ↑<br>[📄](results/bm-20250126-3.14.0a4%2B-a8dc6d6/bm-20250126-linux-x86_64-python-a8dc6d6d44a141a8f839-3.14.0a4%2B-a8dc6d6-vs-3.12.6.md)[📈](results/bm-20250126-3.14.0a4%2B-a8dc6d6/bm-20250126-linux-x86_64-python-a8dc6d6d44a141a8f839-3.14.0a4%2B-a8dc6d6-vs-3.12.6.svg) | 1.075x ↑<br>[📄](results/bm-20250126-3.14.0a4%2B-a8dc6d6/bm-20250126-linux-x86_64-python-a8dc6d6d44a141a8f839-3.14.0a4%2B-a8dc6d6-vs-3.13.0rc2.md)[📈](results/bm-20250126-3.14.0a4%2B-a8dc6d6/bm-20250126-linux-x86_64-python-a8dc6d6d44a141a8f839-3.14.0a4%2B-a8dc6d6-vs-3.13.0rc2.svg) |  |
| [2025-01-25](results/bm-20250125-3.14.0a4%2B-3f2cfd0) | python/3f2cfd0462e13368092a | 3f2cfd0 | 1.072x ↑<br>[📄](results/bm-20250125-3.14.0a4%2B-3f2cfd0/bm-20250125-linux-x86_64-python-3f2cfd0462e13368092a-3.14.0a4%2B-3f2cfd0-vs-3.12.6.md)[📈](results/bm-20250125-3.14.0a4%2B-3f2cfd0/bm-20250125-linux-x86_64-python-3f2cfd0462e13368092a-3.14.0a4%2B-3f2cfd0-vs-3.12.6.svg) | 1.030x ↑<br>[📄](results/bm-20250125-3.14.0a4%2B-3f2cfd0/bm-20250125-linux-x86_64-python-3f2cfd0462e13368092a-3.14.0a4%2B-3f2cfd0-vs-3.13.0rc2.md)[📈](results/bm-20250125-3.14.0a4%2B-3f2cfd0/bm-20250125-linux-x86_64-python-3f2cfd0462e13368092a-3.14.0a4%2B-3f2cfd0-vs-3.13.0rc2.svg) |  |
| [2025-01-25](results/bm-20250125-3.14.0a4%2B-3f2cfd0-NOGIL) | python/3f2cfd0462e13368092a | 3f2cfd0 (NOGIL) | 1.102x ↓<br>[📄](results/bm-20250125-3.14.0a4%2B-3f2cfd0-NOGIL/bm-20250125-linux-x86_64-python-3f2cfd0462e13368092a-3.14.0a4%2B-3f2cfd0-vs-3.12.6.md)[📈](results/bm-20250125-3.14.0a4%2B-3f2cfd0-NOGIL/bm-20250125-linux-x86_64-python-3f2cfd0462e13368092a-3.14.0a4%2B-3f2cfd0-vs-3.12.6.svg) | 1.135x ↓<br>[📄](results/bm-20250125-3.14.0a4%2B-3f2cfd0-NOGIL/bm-20250125-linux-x86_64-python-3f2cfd0462e13368092a-3.14.0a4%2B-3f2cfd0-vs-3.13.0rc2.md)[📈](results/bm-20250125-3.14.0a4%2B-3f2cfd0-NOGIL/bm-20250125-linux-x86_64-python-3f2cfd0462e13368092a-3.14.0a4%2B-3f2cfd0-vs-3.13.0rc2.svg) | 1.158x ↓<br>[📄](results/bm-20250125-3.14.0a4%2B-3f2cfd0-NOGIL/bm-20250125-linux-x86_64-python-3f2cfd0462e13368092a-3.14.0a4%2B-3f2cfd0-vs-base.md)[📈](results/bm-20250125-3.14.0a4%2B-3f2cfd0-NOGIL/bm-20250125-linux-x86_64-python-3f2cfd0462e13368092a-3.14.0a4%2B-3f2cfd0-vs-base.svg)[🧠](results/bm-20250125-3.14.0a4%2B-3f2cfd0-NOGIL/bm-20250125-linux-x86_64-python-3f2cfd0462e13368092a-3.14.0a4%2B-3f2cfd0-vs-base-mem.svg) |
| [2025-01-24](results/bm-20250124-3.14.0a4%2B-9abbb58) | python/9abbb58e3f023555473d | 9abbb58 | 1.066x ↑<br>[📄](results/bm-20250124-3.14.0a4%2B-9abbb58/bm-20250124-linux-x86_64-python-9abbb58e3f023555473d-3.14.0a4%2B-9abbb58-vs-3.12.6.md)[📈](results/bm-20250124-3.14.0a4%2B-9abbb58/bm-20250124-linux-x86_64-python-9abbb58e3f023555473d-3.14.0a4%2B-9abbb58-vs-3.12.6.svg) | 1.021x ↑<br>[📄](results/bm-20250124-3.14.0a4%2B-9abbb58/bm-20250124-linux-x86_64-python-9abbb58e3f023555473d-3.14.0a4%2B-9abbb58-vs-3.13.0rc2.md)[📈](results/bm-20250124-3.14.0a4%2B-9abbb58/bm-20250124-linux-x86_64-python-9abbb58e3f023555473d-3.14.0a4%2B-9abbb58-vs-3.13.0rc2.svg) |  |
| [2025-01-24](results/bm-20250124-3.14.0a4%2B-9abbb58-NOGIL) | python/9abbb58e3f023555473d | 9abbb58 (NOGIL) | 1.081x ↓<br>[📄](results/bm-20250124-3.14.0a4%2B-9abbb58-NOGIL/bm-20250124-linux-x86_64-python-9abbb58e3f023555473d-3.14.0a4%2B-9abbb58-vs-3.12.6.md)[📈](results/bm-20250124-3.14.0a4%2B-9abbb58-NOGIL/bm-20250124-linux-x86_64-python-9abbb58e3f023555473d-3.14.0a4%2B-9abbb58-vs-3.12.6.svg) | 1.114x ↓<br>[📄](results/bm-20250124-3.14.0a4%2B-9abbb58-NOGIL/bm-20250124-linux-x86_64-python-9abbb58e3f023555473d-3.14.0a4%2B-9abbb58-vs-3.13.0rc2.md)[📈](results/bm-20250124-3.14.0a4%2B-9abbb58-NOGIL/bm-20250124-linux-x86_64-python-9abbb58e3f023555473d-3.14.0a4%2B-9abbb58-vs-3.13.0rc2.svg) | 1.133x ↓<br>[📄](results/bm-20250124-3.14.0a4%2B-9abbb58-NOGIL/bm-20250124-linux-x86_64-python-9abbb58e3f023555473d-3.14.0a4%2B-9abbb58-vs-base.md)[📈](results/bm-20250124-3.14.0a4%2B-9abbb58-NOGIL/bm-20250124-linux-x86_64-python-9abbb58e3f023555473d-3.14.0a4%2B-9abbb58-vs-base.svg)[🧠](results/bm-20250124-3.14.0a4%2B-9abbb58-NOGIL/bm-20250124-linux-x86_64-python-9abbb58e3f023555473d-3.14.0a4%2B-9abbb58-vs-base-mem.svg) |

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-01-28](results/bm-20250128-3.14.0a4%2B-1c3bb20-NOGIL) | python/1c3bb200da77f9df30af | 1c3bb20 (NOGIL) | 1.077x ↓<br>[📄](results/bm-20250128-3.14.0a4%2B-1c3bb20-NOGIL/bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4%2B-1c3bb20-vs-3.12.6.md)[📈](results/bm-20250128-3.14.0a4%2B-1c3bb20-NOGIL/bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4%2B-1c3bb20-vs-3.12.6.svg) | 1.107x ↓<br>[📄](results/bm-20250128-3.14.0a4%2B-1c3bb20-NOGIL/bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4%2B-1c3bb20-vs-3.13.0rc2.md)[📈](results/bm-20250128-3.14.0a4%2B-1c3bb20-NOGIL/bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4%2B-1c3bb20-vs-3.13.0rc2.svg) | 1.153x ↓<br>[📄](results/bm-20250128-3.14.0a4%2B-1c3bb20-NOGIL/bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4%2B-1c3bb20-vs-base.md)[📈](results/bm-20250128-3.14.0a4%2B-1c3bb20-NOGIL/bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4%2B-1c3bb20-vs-base.svg)[🧠](results/bm-20250128-3.14.0a4%2B-1c3bb20-NOGIL/bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4%2B-1c3bb20-vs-base-mem.svg) |
| [2025-01-28](results/bm-20250128-3.14.0a4%2B-1c3bb20) | python/1c3bb200da77f9df30af | 1c3bb20 | 1.090x ↑<br>[📄](results/bm-20250128-3.14.0a4%2B-1c3bb20/bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4%2B-1c3bb20-vs-3.12.6.md)[📈](results/bm-20250128-3.14.0a4%2B-1c3bb20/bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4%2B-1c3bb20-vs-3.12.6.svg) | 1.051x ↑<br>[📄](results/bm-20250128-3.14.0a4%2B-1c3bb20/bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4%2B-1c3bb20-vs-3.13.0rc2.md)[📈](results/bm-20250128-3.14.0a4%2B-1c3bb20/bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4%2B-1c3bb20-vs-3.13.0rc2.svg) |  |
| [2025-01-27](results/bm-20250127-3.14.0a4%2B-c92089c-NOGIL) | Yhg1s/more_spec | c92089c (NOGIL) | 1.062x ↓<br>[📄](results/bm-20250127-3.14.0a4%2B-c92089c-NOGIL/bm-20250127-vultr-x86_64-Yhg1s-more_spec-3.14.0a4%2B-c92089c-vs-3.12.6.md)[📈](results/bm-20250127-3.14.0a4%2B-c92089c-NOGIL/bm-20250127-vultr-x86_64-Yhg1s-more_spec-3.14.0a4%2B-c92089c-vs-3.12.6.svg) | 1.092x ↓<br>[📄](results/bm-20250127-3.14.0a4%2B-c92089c-NOGIL/bm-20250127-vultr-x86_64-Yhg1s-more_spec-3.14.0a4%2B-c92089c-vs-3.13.0rc2.md)[📈](results/bm-20250127-3.14.0a4%2B-c92089c-NOGIL/bm-20250127-vultr-x86_64-Yhg1s-more_spec-3.14.0a4%2B-c92089c-vs-3.13.0rc2.svg) | 1.009x ↑<br>[📄](results/bm-20250127-3.14.0a4%2B-c92089c-NOGIL/bm-20250127-vultr-x86_64-Yhg1s-more_spec-3.14.0a4%2B-c92089c-vs-base.md)[📈](results/bm-20250127-3.14.0a4%2B-c92089c-NOGIL/bm-20250127-vultr-x86_64-Yhg1s-more_spec-3.14.0a4%2B-c92089c-vs-base.svg)[🧠](results/bm-20250127-3.14.0a4%2B-c92089c-NOGIL/bm-20250127-vultr-x86_64-Yhg1s-more_spec-3.14.0a4%2B-c92089c-vs-base-mem.svg) |
| [2025-01-27](results/bm-20250127-3.14.0a4%2B-a5075cd-NOGIL) | python/a5075cd5bd0307d9c19a | a5075cd (NOGIL) | 1.071x ↓<br>[📄](results/bm-20250127-3.14.0a4%2B-a5075cd-NOGIL/bm-20250127-vultr-x86_64-python-a5075cd5bd0307d9c19a-3.14.0a4%2B-a5075cd-vs-3.12.6.md)[📈](results/bm-20250127-3.14.0a4%2B-a5075cd-NOGIL/bm-20250127-vultr-x86_64-python-a5075cd5bd0307d9c19a-3.14.0a4%2B-a5075cd-vs-3.12.6.svg) | 1.101x ↓<br>[📄](results/bm-20250127-3.14.0a4%2B-a5075cd-NOGIL/bm-20250127-vultr-x86_64-python-a5075cd5bd0307d9c19a-3.14.0a4%2B-a5075cd-vs-3.13.0rc2.md)[📈](results/bm-20250127-3.14.0a4%2B-a5075cd-NOGIL/bm-20250127-vultr-x86_64-python-a5075cd5bd0307d9c19a-3.14.0a4%2B-a5075cd-vs-3.13.0rc2.svg) |  |
| [2025-01-26](results/bm-20250126-3.14.0a4%2B-a8dc6d6-NOGIL) | python/a8dc6d6d44a141a8f839 | a8dc6d6 (NOGIL) | 1.059x ↓<br>[📄](results/bm-20250126-3.14.0a4%2B-a8dc6d6-NOGIL/bm-20250126-vultr-x86_64-python-a8dc6d6d44a141a8f839-3.14.0a4%2B-a8dc6d6-vs-3.12.6.md)[📈](results/bm-20250126-3.14.0a4%2B-a8dc6d6-NOGIL/bm-20250126-vultr-x86_64-python-a8dc6d6d44a141a8f839-3.14.0a4%2B-a8dc6d6-vs-3.12.6.svg) | 1.089x ↓<br>[📄](results/bm-20250126-3.14.0a4%2B-a8dc6d6-NOGIL/bm-20250126-vultr-x86_64-python-a8dc6d6d44a141a8f839-3.14.0a4%2B-a8dc6d6-vs-3.13.0rc2.md)[📈](results/bm-20250126-3.14.0a4%2B-a8dc6d6-NOGIL/bm-20250126-vultr-x86_64-python-a8dc6d6d44a141a8f839-3.14.0a4%2B-a8dc6d6-vs-3.13.0rc2.svg) | 1.135x ↓<br>[📄](results/bm-20250126-3.14.0a4%2B-a8dc6d6-NOGIL/bm-20250126-vultr-x86_64-python-a8dc6d6d44a141a8f839-3.14.0a4%2B-a8dc6d6-vs-base.md)[📈](results/bm-20250126-3.14.0a4%2B-a8dc6d6-NOGIL/bm-20250126-vultr-x86_64-python-a8dc6d6d44a141a8f839-3.14.0a4%2B-a8dc6d6-vs-base.svg)[🧠](results/bm-20250126-3.14.0a4%2B-a8dc6d6-NOGIL/bm-20250126-vultr-x86_64-python-a8dc6d6d44a141a8f839-3.14.0a4%2B-a8dc6d6-vs-base-mem.svg) |
| [2025-01-26](results/bm-20250126-3.14.0a4%2B-a8dc6d6) | python/a8dc6d6d44a141a8f839 | a8dc6d6 | 1.088x ↑<br>[📄](results/bm-20250126-3.14.0a4%2B-a8dc6d6/bm-20250126-vultr-x86_64-python-a8dc6d6d44a141a8f839-3.14.0a4%2B-a8dc6d6-vs-3.12.6.md)[📈](results/bm-20250126-3.14.0a4%2B-a8dc6d6/bm-20250126-vultr-x86_64-python-a8dc6d6d44a141a8f839-3.14.0a4%2B-a8dc6d6-vs-3.12.6.svg) | 1.049x ↑<br>[📄](results/bm-20250126-3.14.0a4%2B-a8dc6d6/bm-20250126-vultr-x86_64-python-a8dc6d6d44a141a8f839-3.14.0a4%2B-a8dc6d6-vs-3.13.0rc2.md)[📈](results/bm-20250126-3.14.0a4%2B-a8dc6d6/bm-20250126-vultr-x86_64-python-a8dc6d6d44a141a8f839-3.14.0a4%2B-a8dc6d6-vs-3.13.0rc2.svg) |  |
| [2025-01-25](results/bm-20250125-3.14.0a4%2B-3f2cfd0) | python/3f2cfd0462e13368092a | 3f2cfd0 | 1.088x ↑<br>[📄](results/bm-20250125-3.14.0a4%2B-3f2cfd0/bm-20250125-vultr-x86_64-python-3f2cfd0462e13368092a-3.14.0a4%2B-3f2cfd0-vs-3.12.6.md)[📈](results/bm-20250125-3.14.0a4%2B-3f2cfd0/bm-20250125-vultr-x86_64-python-3f2cfd0462e13368092a-3.14.0a4%2B-3f2cfd0-vs-3.12.6.svg) | 1.050x ↑<br>[📄](results/bm-20250125-3.14.0a4%2B-3f2cfd0/bm-20250125-vultr-x86_64-python-3f2cfd0462e13368092a-3.14.0a4%2B-3f2cfd0-vs-3.13.0rc2.md)[📈](results/bm-20250125-3.14.0a4%2B-3f2cfd0/bm-20250125-vultr-x86_64-python-3f2cfd0462e13368092a-3.14.0a4%2B-3f2cfd0-vs-3.13.0rc2.svg) |  |
| [2025-01-25](results/bm-20250125-3.14.0a4%2B-3f2cfd0-NOGIL) | python/3f2cfd0462e13368092a | 3f2cfd0 (NOGIL) | 1.058x ↓<br>[📄](results/bm-20250125-3.14.0a4%2B-3f2cfd0-NOGIL/bm-20250125-vultr-x86_64-python-3f2cfd0462e13368092a-3.14.0a4%2B-3f2cfd0-vs-3.12.6.md)[📈](results/bm-20250125-3.14.0a4%2B-3f2cfd0-NOGIL/bm-20250125-vultr-x86_64-python-3f2cfd0462e13368092a-3.14.0a4%2B-3f2cfd0-vs-3.12.6.svg) | 1.088x ↓<br>[📄](results/bm-20250125-3.14.0a4%2B-3f2cfd0-NOGIL/bm-20250125-vultr-x86_64-python-3f2cfd0462e13368092a-3.14.0a4%2B-3f2cfd0-vs-3.13.0rc2.md)[📈](results/bm-20250125-3.14.0a4%2B-3f2cfd0-NOGIL/bm-20250125-vultr-x86_64-python-3f2cfd0462e13368092a-3.14.0a4%2B-3f2cfd0-vs-3.13.0rc2.svg) | 1.135x ↓<br>[📄](results/bm-20250125-3.14.0a4%2B-3f2cfd0-NOGIL/bm-20250125-vultr-x86_64-python-3f2cfd0462e13368092a-3.14.0a4%2B-3f2cfd0-vs-base.md)[📈](results/bm-20250125-3.14.0a4%2B-3f2cfd0-NOGIL/bm-20250125-vultr-x86_64-python-3f2cfd0462e13368092a-3.14.0a4%2B-3f2cfd0-vs-base.svg)[🧠](results/bm-20250125-3.14.0a4%2B-3f2cfd0-NOGIL/bm-20250125-vultr-x86_64-python-3f2cfd0462e13368092a-3.14.0a4%2B-3f2cfd0-vs-base-mem.svg) |
| [2025-01-24](results/bm-20250124-3.14.0a4%2B-9abbb58) | python/9abbb58e3f023555473d | 9abbb58 | 1.089x ↑<br>[📄](results/bm-20250124-3.14.0a4%2B-9abbb58/bm-20250124-vultr-x86_64-python-9abbb58e3f023555473d-3.14.0a4%2B-9abbb58-vs-3.12.6.md)[📈](results/bm-20250124-3.14.0a4%2B-9abbb58/bm-20250124-vultr-x86_64-python-9abbb58e3f023555473d-3.14.0a4%2B-9abbb58-vs-3.12.6.svg) | 1.051x ↑<br>[📄](results/bm-20250124-3.14.0a4%2B-9abbb58/bm-20250124-vultr-x86_64-python-9abbb58e3f023555473d-3.14.0a4%2B-9abbb58-vs-3.13.0rc2.md)[📈](results/bm-20250124-3.14.0a4%2B-9abbb58/bm-20250124-vultr-x86_64-python-9abbb58e3f023555473d-3.14.0a4%2B-9abbb58-vs-3.13.0rc2.svg) |  |
| [2025-01-24](results/bm-20250124-3.14.0a4%2B-9abbb58-NOGIL) | python/9abbb58e3f023555473d | 9abbb58 (NOGIL) | 1.063x ↓<br>[📄](results/bm-20250124-3.14.0a4%2B-9abbb58-NOGIL/bm-20250124-vultr-x86_64-python-9abbb58e3f023555473d-3.14.0a4%2B-9abbb58-vs-3.12.6.md)[📈](results/bm-20250124-3.14.0a4%2B-9abbb58-NOGIL/bm-20250124-vultr-x86_64-python-9abbb58e3f023555473d-3.14.0a4%2B-9abbb58-vs-3.12.6.svg) | 1.094x ↓<br>[📄](results/bm-20250124-3.14.0a4%2B-9abbb58-NOGIL/bm-20250124-vultr-x86_64-python-9abbb58e3f023555473d-3.14.0a4%2B-9abbb58-vs-3.13.0rc2.md)[📈](results/bm-20250124-3.14.0a4%2B-9abbb58-NOGIL/bm-20250124-vultr-x86_64-python-9abbb58e3f023555473d-3.14.0a4%2B-9abbb58-vs-3.13.0rc2.svg) | 1.140x ↓<br>[📄](results/bm-20250124-3.14.0a4%2B-9abbb58-NOGIL/bm-20250124-vultr-x86_64-python-9abbb58e3f023555473d-3.14.0a4%2B-9abbb58-vs-base.md)[📈](results/bm-20250124-3.14.0a4%2B-9abbb58-NOGIL/bm-20250124-vultr-x86_64-python-9abbb58e3f023555473d-3.14.0a4%2B-9abbb58-vs-base.svg)[🧠](results/bm-20250124-3.14.0a4%2B-9abbb58-NOGIL/bm-20250124-vultr-x86_64-python-9abbb58e3f023555473d-3.14.0a4%2B-9abbb58-vs-base-mem.svg) |


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
