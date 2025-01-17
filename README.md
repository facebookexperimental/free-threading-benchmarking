# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
[Most recent pystats on main (22a4421)](results/bm-20250111-3.14.0a3%2B-22a4421-PYTHON_UOPS/bm-20250111-vultr-x86_64-python-22a442181d5f1ac496da-3.14.0a3%2B-22a4421-pystats.md)

## linux x86_64 (linux)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-01-16](results/bm-20250116-3.14.0a4%2B-b44ff6d-NOGIL) | python/b44ff6d0df9ec2d60be6 | b44ff6d (NOGIL) | 1.062x ↓<br>[📄](results/bm-20250116-3.14.0a4%2B-b44ff6d-NOGIL/bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4%2B-b44ff6d-vs-3.12.6.md)[📈](results/bm-20250116-3.14.0a4%2B-b44ff6d-NOGIL/bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4%2B-b44ff6d-vs-3.12.6.svg) | 1.096x ↓<br>[📄](results/bm-20250116-3.14.0a4%2B-b44ff6d-NOGIL/bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4%2B-b44ff6d-vs-3.13.0rc2.md)[📈](results/bm-20250116-3.14.0a4%2B-b44ff6d-NOGIL/bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4%2B-b44ff6d-vs-3.13.0rc2.svg) | 1.132x ↓<br>[📄](results/bm-20250116-3.14.0a4%2B-b44ff6d-NOGIL/bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4%2B-b44ff6d-vs-base.md)[📈](results/bm-20250116-3.14.0a4%2B-b44ff6d-NOGIL/bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4%2B-b44ff6d-vs-base.svg)[🧠](results/bm-20250116-3.14.0a4%2B-b44ff6d-NOGIL/bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4%2B-b44ff6d-vs-base-mem.svg) |
| [2025-01-16](results/bm-20250116-3.14.0a4%2B-b44ff6d) | python/b44ff6d0df9ec2d60be6 | b44ff6d | 1.081x ↑<br>[📄](results/bm-20250116-3.14.0a4%2B-b44ff6d/bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4%2B-b44ff6d-vs-3.12.6.md)[📈](results/bm-20250116-3.14.0a4%2B-b44ff6d/bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4%2B-b44ff6d-vs-3.12.6.svg) | 1.038x ↑<br>[📄](results/bm-20250116-3.14.0a4%2B-b44ff6d/bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4%2B-b44ff6d-vs-3.13.0rc2.md)[📈](results/bm-20250116-3.14.0a4%2B-b44ff6d/bm-20250116-linux-x86_64-python-b44ff6d0df9ec2d60be6-3.14.0a4%2B-b44ff6d-vs-3.13.0rc2.svg) |  |
| [2025-01-15](results/bm-20250115-3.14.0a4%2B-d05140f-NOGIL) | python/d05140f9f77d7dfc753d | d05140f (NOGIL) | 1.073x ↓<br>[📄](results/bm-20250115-3.14.0a4%2B-d05140f-NOGIL/bm-20250115-linux-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4%2B-d05140f-vs-3.12.6.md)[📈](results/bm-20250115-3.14.0a4%2B-d05140f-NOGIL/bm-20250115-linux-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4%2B-d05140f-vs-3.12.6.svg) | 1.103x ↓<br>[📄](results/bm-20250115-3.14.0a4%2B-d05140f-NOGIL/bm-20250115-linux-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4%2B-d05140f-vs-3.13.0rc2.md)[📈](results/bm-20250115-3.14.0a4%2B-d05140f-NOGIL/bm-20250115-linux-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4%2B-d05140f-vs-3.13.0rc2.svg) | 1.129x ↓<br>[📄](results/bm-20250115-3.14.0a4%2B-d05140f-NOGIL/bm-20250115-linux-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4%2B-d05140f-vs-base.md)[📈](results/bm-20250115-3.14.0a4%2B-d05140f-NOGIL/bm-20250115-linux-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4%2B-d05140f-vs-base.svg)[🧠](results/bm-20250115-3.14.0a4%2B-d05140f-NOGIL/bm-20250115-linux-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4%2B-d05140f-vs-base-mem.svg) |
| [2025-01-15](results/bm-20250115-3.14.0a4%2B-d05140f) | python/d05140f9f77d7dfc753d | d05140f | 1.074x ↑<br>[📄](results/bm-20250115-3.14.0a4%2B-d05140f/bm-20250115-linux-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4%2B-d05140f-vs-3.12.6.md)[📈](results/bm-20250115-3.14.0a4%2B-d05140f/bm-20250115-linux-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4%2B-d05140f-vs-3.12.6.svg) | 1.034x ↑<br>[📄](results/bm-20250115-3.14.0a4%2B-d05140f/bm-20250115-linux-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4%2B-d05140f-vs-3.13.0rc2.md)[📈](results/bm-20250115-3.14.0a4%2B-d05140f/bm-20250115-linux-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4%2B-d05140f-vs-3.13.0rc2.svg) |  |
| [2025-01-15](results/bm-20250115-3.14.0a4%2B-6e4f641) | python/6e4f64109b0eb6c9f1b5 | 6e4f641 | 1.067x ↑<br>[📄](results/bm-20250115-3.14.0a4%2B-6e4f641/bm-20250115-linux-x86_64-python-6e4f64109b0eb6c9f1b5-3.14.0a4%2B-6e4f641-vs-3.12.6.md)[📈](results/bm-20250115-3.14.0a4%2B-6e4f641/bm-20250115-linux-x86_64-python-6e4f64109b0eb6c9f1b5-3.14.0a4%2B-6e4f641-vs-3.12.6.svg) | 1.023x ↑<br>[📄](results/bm-20250115-3.14.0a4%2B-6e4f641/bm-20250115-linux-x86_64-python-6e4f64109b0eb6c9f1b5-3.14.0a4%2B-6e4f641-vs-3.13.0rc2.md)[📈](results/bm-20250115-3.14.0a4%2B-6e4f641/bm-20250115-linux-x86_64-python-6e4f64109b0eb6c9f1b5-3.14.0a4%2B-6e4f641-vs-3.13.0rc2.svg) |  |
| [2025-01-15](results/bm-20250115-3.14.0a4%2B-6e4f641-NOGIL) | python/6e4f64109b0eb6c9f1b5 | 6e4f641 (NOGIL) | 1.097x ↓<br>[📄](results/bm-20250115-3.14.0a4%2B-6e4f641-NOGIL/bm-20250115-linux-x86_64-python-6e4f64109b0eb6c9f1b5-3.14.0a4%2B-6e4f641-vs-3.12.6.md)[📈](results/bm-20250115-3.14.0a4%2B-6e4f641-NOGIL/bm-20250115-linux-x86_64-python-6e4f64109b0eb6c9f1b5-3.14.0a4%2B-6e4f641-vs-3.12.6.svg) | 1.128x ↓<br>[📄](results/bm-20250115-3.14.0a4%2B-6e4f641-NOGIL/bm-20250115-linux-x86_64-python-6e4f64109b0eb6c9f1b5-3.14.0a4%2B-6e4f641-vs-3.13.0rc2.md)[📈](results/bm-20250115-3.14.0a4%2B-6e4f641-NOGIL/bm-20250115-linux-x86_64-python-6e4f64109b0eb6c9f1b5-3.14.0a4%2B-6e4f641-vs-3.13.0rc2.svg) | 1.148x ↓<br>[📄](results/bm-20250115-3.14.0a4%2B-6e4f641-NOGIL/bm-20250115-linux-x86_64-python-6e4f64109b0eb6c9f1b5-3.14.0a4%2B-6e4f641-vs-base.md)[📈](results/bm-20250115-3.14.0a4%2B-6e4f641-NOGIL/bm-20250115-linux-x86_64-python-6e4f64109b0eb6c9f1b5-3.14.0a4%2B-6e4f641-vs-base.svg)[🧠](results/bm-20250115-3.14.0a4%2B-6e4f641-NOGIL/bm-20250115-linux-x86_64-python-6e4f64109b0eb6c9f1b5-3.14.0a4%2B-6e4f641-vs-base-mem.svg) |
| [2025-01-15](results/bm-20250115-3.14.0a4%2B-b52de22) | python/b52de22ac345ad8583bc | b52de22 | 1.051x ↑<br>[📄](results/bm-20250115-3.14.0a4%2B-b52de22/bm-20250115-linux-x86_64-python-b52de22ac345ad8583bc-3.14.0a4%2B-b52de22-vs-3.12.6.md)[📈](results/bm-20250115-3.14.0a4%2B-b52de22/bm-20250115-linux-x86_64-python-b52de22ac345ad8583bc-3.14.0a4%2B-b52de22-vs-3.12.6.svg) | 1.010x ↑<br>[📄](results/bm-20250115-3.14.0a4%2B-b52de22/bm-20250115-linux-x86_64-python-b52de22ac345ad8583bc-3.14.0a4%2B-b52de22-vs-3.13.0rc2.md)[📈](results/bm-20250115-3.14.0a4%2B-b52de22/bm-20250115-linux-x86_64-python-b52de22ac345ad8583bc-3.14.0a4%2B-b52de22-vs-3.13.0rc2.svg) |  |
| [2025-01-15](results/bm-20250115-3.14.0a4%2B-b52de22-NOGIL) | python/b52de22ac345ad8583bc | b52de22 (NOGIL) | 1.102x ↓<br>[📄](results/bm-20250115-3.14.0a4%2B-b52de22-NOGIL/bm-20250115-linux-x86_64-python-b52de22ac345ad8583bc-3.14.0a4%2B-b52de22-vs-3.12.6.md)[📈](results/bm-20250115-3.14.0a4%2B-b52de22-NOGIL/bm-20250115-linux-x86_64-python-b52de22ac345ad8583bc-3.14.0a4%2B-b52de22-vs-3.12.6.svg) | 1.134x ↓<br>[📄](results/bm-20250115-3.14.0a4%2B-b52de22-NOGIL/bm-20250115-linux-x86_64-python-b52de22ac345ad8583bc-3.14.0a4%2B-b52de22-vs-3.13.0rc2.md)[📈](results/bm-20250115-3.14.0a4%2B-b52de22-NOGIL/bm-20250115-linux-x86_64-python-b52de22ac345ad8583bc-3.14.0a4%2B-b52de22-vs-3.13.0rc2.svg) | 1.142x ↓<br>[📄](results/bm-20250115-3.14.0a4%2B-b52de22-NOGIL/bm-20250115-linux-x86_64-python-b52de22ac345ad8583bc-3.14.0a4%2B-b52de22-vs-base.md)[📈](results/bm-20250115-3.14.0a4%2B-b52de22-NOGIL/bm-20250115-linux-x86_64-python-b52de22ac345ad8583bc-3.14.0a4%2B-b52de22-vs-base.svg)[🧠](results/bm-20250115-3.14.0a4%2B-b52de22-NOGIL/bm-20250115-linux-x86_64-python-b52de22ac345ad8583bc-3.14.0a4%2B-b52de22-vs-base-mem.svg) |
| [2025-01-13](results/bm-20250113-3.14.0a3%2B-b70a567) | python/b70a567575db37846bee | b70a567 | 1.062x ↑<br>[📄](results/bm-20250113-3.14.0a3%2B-b70a567/bm-20250113-linux-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-3.12.6.md)[📈](results/bm-20250113-3.14.0a3%2B-b70a567/bm-20250113-linux-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-3.12.6.svg) | 1.023x ↑<br>[📄](results/bm-20250113-3.14.0a3%2B-b70a567/bm-20250113-linux-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-3.13.0rc2.md)[📈](results/bm-20250113-3.14.0a3%2B-b70a567/bm-20250113-linux-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-3.13.0rc2.svg) |  |
| [2025-01-13](results/bm-20250113-3.14.0a3%2B-b70a567-NOGIL) | python/b70a567575db37846bee | b70a567 (NOGIL) | 1.185x ↓<br>[📄](results/bm-20250113-3.14.0a3%2B-b70a567-NOGIL/bm-20250113-linux-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-3.12.6.md)[📈](results/bm-20250113-3.14.0a3%2B-b70a567-NOGIL/bm-20250113-linux-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-3.12.6.svg) | 1.210x ↓<br>[📄](results/bm-20250113-3.14.0a3%2B-b70a567-NOGIL/bm-20250113-linux-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-3.13.0rc2.md)[📈](results/bm-20250113-3.14.0a3%2B-b70a567-NOGIL/bm-20250113-linux-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-3.13.0rc2.svg) | 1.221x ↓<br>[📄](results/bm-20250113-3.14.0a3%2B-b70a567-NOGIL/bm-20250113-linux-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-base.md)[📈](results/bm-20250113-3.14.0a3%2B-b70a567-NOGIL/bm-20250113-linux-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-base.svg)[🧠](results/bm-20250113-3.14.0a3%2B-b70a567-NOGIL/bm-20250113-linux-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-base-mem.svg) |

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-01-16](results/bm-20250116-3.14.0a4%2B-211f413) | python/211f41316b7f205d18eb | 211f413 | 1.088x ↑<br>[📄](results/bm-20250116-3.14.0a4%2B-211f413/bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4%2B-211f413-vs-3.12.6.md)[📈](results/bm-20250116-3.14.0a4%2B-211f413/bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4%2B-211f413-vs-3.12.6.svg) | 1.050x ↑<br>[📄](results/bm-20250116-3.14.0a4%2B-211f413/bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4%2B-211f413-vs-3.13.0rc2.md)[📈](results/bm-20250116-3.14.0a4%2B-211f413/bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4%2B-211f413-vs-3.13.0rc2.svg) | 1.003x ↓<br>[📄](results/bm-20250116-3.14.0a4%2B-211f413/bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4%2B-211f413-vs-base.md)[📈](results/bm-20250116-3.14.0a4%2B-211f413/bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4%2B-211f413-vs-base.svg)[🧠](results/bm-20250116-3.14.0a4%2B-211f413/bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4%2B-211f413-vs-base-mem.svg) |
| [2025-01-16](results/bm-20250116-3.14.0a4%2B-211f413-NOGIL) | python/211f41316b7f205d18eb | 211f413 (NOGIL) | 1.046x ↓<br>[📄](results/bm-20250116-3.14.0a4%2B-211f413-NOGIL/bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4%2B-211f413-vs-3.12.6.md)[📈](results/bm-20250116-3.14.0a4%2B-211f413-NOGIL/bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4%2B-211f413-vs-3.12.6.svg) | 1.076x ↓<br>[📄](results/bm-20250116-3.14.0a4%2B-211f413-NOGIL/bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4%2B-211f413-vs-3.13.0rc2.md)[📈](results/bm-20250116-3.14.0a4%2B-211f413-NOGIL/bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4%2B-211f413-vs-3.13.0rc2.svg) |  |
| [2025-01-16](results/bm-20250116-3.14.0a4%2B-f48702d) | python/f48702dade921beed3e2 | f48702d | 1.091x ↑<br>[📄](results/bm-20250116-3.14.0a4%2B-f48702d/bm-20250116-vultr-x86_64-python-f48702dade921beed3e2-3.14.0a4%2B-f48702d-vs-3.12.6.md)[📈](results/bm-20250116-3.14.0a4%2B-f48702d/bm-20250116-vultr-x86_64-python-f48702dade921beed3e2-3.14.0a4%2B-f48702d-vs-3.12.6.svg) | 1.053x ↑<br>[📄](results/bm-20250116-3.14.0a4%2B-f48702d/bm-20250116-vultr-x86_64-python-f48702dade921beed3e2-3.14.0a4%2B-f48702d-vs-3.13.0rc2.md)[📈](results/bm-20250116-3.14.0a4%2B-f48702d/bm-20250116-vultr-x86_64-python-f48702dade921beed3e2-3.14.0a4%2B-f48702d-vs-3.13.0rc2.svg) | 1.007x ↓<br>[📄](results/bm-20250116-3.14.0a4%2B-f48702d/bm-20250116-vultr-x86_64-python-f48702dade921beed3e2-3.14.0a4%2B-f48702d-vs-base.md)[📈](results/bm-20250116-3.14.0a4%2B-f48702d/bm-20250116-vultr-x86_64-python-f48702dade921beed3e2-3.14.0a4%2B-f48702d-vs-base.svg)[🧠](results/bm-20250116-3.14.0a4%2B-f48702d/bm-20250116-vultr-x86_64-python-f48702dade921beed3e2-3.14.0a4%2B-f48702d-vs-base-mem.svg) |
| [2025-01-16](results/bm-20250116-3.14.0a4%2B-3893a92) | python/3893a92d956363fa2443 | 3893a92 | 1.099x ↑<br>[📄](results/bm-20250116-3.14.0a4%2B-3893a92/bm-20250116-vultr-x86_64-python-3893a92d956363fa2443-3.14.0a4%2B-3893a92-vs-3.12.6.md)[📈](results/bm-20250116-3.14.0a4%2B-3893a92/bm-20250116-vultr-x86_64-python-3893a92d956363fa2443-3.14.0a4%2B-3893a92-vs-3.12.6.svg) | 1.060x ↑<br>[📄](results/bm-20250116-3.14.0a4%2B-3893a92/bm-20250116-vultr-x86_64-python-3893a92d956363fa2443-3.14.0a4%2B-3893a92-vs-3.13.0rc2.md)[📈](results/bm-20250116-3.14.0a4%2B-3893a92/bm-20250116-vultr-x86_64-python-3893a92d956363fa2443-3.14.0a4%2B-3893a92-vs-3.13.0rc2.svg) |  |
| [2025-01-16](results/bm-20250116-3.14.0a4%2B-f1b75b3) | mpage/aa_test_2 | f1b75b3 | 1.084x ↑<br>[📄](results/bm-20250116-3.14.0a4%2B-f1b75b3/bm-20250116-vultr-x86_64-mpage-aa_test_2-3.14.0a4%2B-f1b75b3-vs-3.12.6.md)[📈](results/bm-20250116-3.14.0a4%2B-f1b75b3/bm-20250116-vultr-x86_64-mpage-aa_test_2-3.14.0a4%2B-f1b75b3-vs-3.12.6.svg) | 1.046x ↑<br>[📄](results/bm-20250116-3.14.0a4%2B-f1b75b3/bm-20250116-vultr-x86_64-mpage-aa_test_2-3.14.0a4%2B-f1b75b3-vs-3.13.0rc2.md)[📈](results/bm-20250116-3.14.0a4%2B-f1b75b3/bm-20250116-vultr-x86_64-mpage-aa_test_2-3.14.0a4%2B-f1b75b3-vs-3.13.0rc2.svg) | 1.013x ↓<br>[📄](results/bm-20250116-3.14.0a4%2B-f1b75b3/bm-20250116-vultr-x86_64-mpage-aa_test_2-3.14.0a4%2B-f1b75b3-vs-base.md)[📈](results/bm-20250116-3.14.0a4%2B-f1b75b3/bm-20250116-vultr-x86_64-mpage-aa_test_2-3.14.0a4%2B-f1b75b3-vs-base.svg)[🧠](results/bm-20250116-3.14.0a4%2B-f1b75b3/bm-20250116-vultr-x86_64-mpage-aa_test_2-3.14.0a4%2B-f1b75b3-vs-base-mem.svg) |
| [2025-01-16](results/bm-20250116-3.14.0a4%2B-de82556) | mpage/aa_test_1 | de82556 | 1.092x ↑<br>[📄](results/bm-20250116-3.14.0a4%2B-de82556/bm-20250116-vultr-x86_64-mpage-aa_test_1-3.14.0a4%2B-de82556-vs-3.12.6.md)[📈](results/bm-20250116-3.14.0a4%2B-de82556/bm-20250116-vultr-x86_64-mpage-aa_test_1-3.14.0a4%2B-de82556-vs-3.12.6.svg) | 1.054x ↑<br>[📄](results/bm-20250116-3.14.0a4%2B-de82556/bm-20250116-vultr-x86_64-mpage-aa_test_1-3.14.0a4%2B-de82556-vs-3.13.0rc2.md)[📈](results/bm-20250116-3.14.0a4%2B-de82556/bm-20250116-vultr-x86_64-mpage-aa_test_1-3.14.0a4%2B-de82556-vs-3.13.0rc2.svg) | 1.000x ↑<br>[📄](results/bm-20250116-3.14.0a4%2B-de82556/bm-20250116-vultr-x86_64-mpage-aa_test_1-3.14.0a4%2B-de82556-vs-base.md)[📈](results/bm-20250116-3.14.0a4%2B-de82556/bm-20250116-vultr-x86_64-mpage-aa_test_1-3.14.0a4%2B-de82556-vs-base.svg)[🧠](results/bm-20250116-3.14.0a4%2B-de82556/bm-20250116-vultr-x86_64-mpage-aa_test_1-3.14.0a4%2B-de82556-vs-base-mem.svg) |
| [2025-01-16](results/bm-20250116-3.14.0a4%2B-54bb905) | mpage/aa_test_0 | 54bb905 | 1.080x ↑<br>[📄](results/bm-20250116-3.14.0a4%2B-54bb905/bm-20250116-vultr-x86_64-mpage-aa_test_0-3.14.0a4%2B-54bb905-vs-3.12.6.md)[📈](results/bm-20250116-3.14.0a4%2B-54bb905/bm-20250116-vultr-x86_64-mpage-aa_test_0-3.14.0a4%2B-54bb905-vs-3.12.6.svg) | 1.042x ↑<br>[📄](results/bm-20250116-3.14.0a4%2B-54bb905/bm-20250116-vultr-x86_64-mpage-aa_test_0-3.14.0a4%2B-54bb905-vs-3.13.0rc2.md)[📈](results/bm-20250116-3.14.0a4%2B-54bb905/bm-20250116-vultr-x86_64-mpage-aa_test_0-3.14.0a4%2B-54bb905-vs-3.13.0rc2.svg) | 1.007x ↓<br>[📄](results/bm-20250116-3.14.0a4%2B-54bb905/bm-20250116-vultr-x86_64-mpage-aa_test_0-3.14.0a4%2B-54bb905-vs-base.md)[📈](results/bm-20250116-3.14.0a4%2B-54bb905/bm-20250116-vultr-x86_64-mpage-aa_test_0-3.14.0a4%2B-54bb905-vs-base.svg)[🧠](results/bm-20250116-3.14.0a4%2B-54bb905/bm-20250116-vultr-x86_64-mpage-aa_test_0-3.14.0a4%2B-54bb905-vs-base-mem.svg) |
| [2025-01-16](results/bm-20250116-3.14.0a4%2B-65a6ad3) | mpage/gh_115999_specialize | 65a6ad3 | 1.088x ↑<br>[📄](results/bm-20250116-3.14.0a4%2B-65a6ad3/bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-65a6ad3-vs-3.12.6.md)[📈](results/bm-20250116-3.14.0a4%2B-65a6ad3/bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-65a6ad3-vs-3.12.6.svg) | 1.050x ↑<br>[📄](results/bm-20250116-3.14.0a4%2B-65a6ad3/bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-65a6ad3-vs-3.13.0rc2.md)[📈](results/bm-20250116-3.14.0a4%2B-65a6ad3/bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-65a6ad3-vs-3.13.0rc2.svg) | 1.001x ↓<br>[📄](results/bm-20250116-3.14.0a4%2B-65a6ad3/bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-65a6ad3-vs-base.md)[📈](results/bm-20250116-3.14.0a4%2B-65a6ad3/bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-65a6ad3-vs-base.svg)[🧠](results/bm-20250116-3.14.0a4%2B-65a6ad3/bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-65a6ad3-vs-base-mem.svg) |
| [2025-01-16](results/bm-20250116-3.14.0a4%2B-65a6ad3-NOGIL) | mpage/gh_115999_specialize | 65a6ad3 (NOGIL) | 1.059x ↓<br>[📄](results/bm-20250116-3.14.0a4%2B-65a6ad3-NOGIL/bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-65a6ad3-vs-3.12.6.md)[📈](results/bm-20250116-3.14.0a4%2B-65a6ad3-NOGIL/bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-65a6ad3-vs-3.12.6.svg) | 1.090x ↓<br>[📄](results/bm-20250116-3.14.0a4%2B-65a6ad3-NOGIL/bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-65a6ad3-vs-3.13.0rc2.md)[📈](results/bm-20250116-3.14.0a4%2B-65a6ad3-NOGIL/bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-65a6ad3-vs-3.13.0rc2.svg) | 1.013x ↓<br>[📄](results/bm-20250116-3.14.0a4%2B-65a6ad3-NOGIL/bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-65a6ad3-vs-base.md)[📈](results/bm-20250116-3.14.0a4%2B-65a6ad3-NOGIL/bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-65a6ad3-vs-base.svg)[🧠](results/bm-20250116-3.14.0a4%2B-65a6ad3-NOGIL/bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-65a6ad3-vs-base-mem.svg) |
| [2025-01-15](results/bm-20250115-3.14.0a4%2B-d05140f-NOGIL) | python/d05140f9f77d7dfc753d | d05140f (NOGIL) | 1.053x ↓<br>[📄](results/bm-20250115-3.14.0a4%2B-d05140f-NOGIL/bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4%2B-d05140f-vs-3.12.6.md)[📈](results/bm-20250115-3.14.0a4%2B-d05140f-NOGIL/bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4%2B-d05140f-vs-3.12.6.svg) | 1.084x ↓<br>[📄](results/bm-20250115-3.14.0a4%2B-d05140f-NOGIL/bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4%2B-d05140f-vs-3.13.0rc2.md)[📈](results/bm-20250115-3.14.0a4%2B-d05140f-NOGIL/bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4%2B-d05140f-vs-3.13.0rc2.svg) | 1.127x ↓<br>[📄](results/bm-20250115-3.14.0a4%2B-d05140f-NOGIL/bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4%2B-d05140f-vs-base.md)[📈](results/bm-20250115-3.14.0a4%2B-d05140f-NOGIL/bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4%2B-d05140f-vs-base.svg)[🧠](results/bm-20250115-3.14.0a4%2B-d05140f-NOGIL/bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4%2B-d05140f-vs-base-mem.svg) |
| [2025-01-15](results/bm-20250115-3.14.0a4%2B-d05140f) | python/d05140f9f77d7dfc753d | d05140f | 1.083x ↑<br>[📄](results/bm-20250115-3.14.0a4%2B-d05140f/bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4%2B-d05140f-vs-3.12.6.md)[📈](results/bm-20250115-3.14.0a4%2B-d05140f/bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4%2B-d05140f-vs-3.12.6.svg) | 1.045x ↑<br>[📄](results/bm-20250115-3.14.0a4%2B-d05140f/bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4%2B-d05140f-vs-3.13.0rc2.md)[📈](results/bm-20250115-3.14.0a4%2B-d05140f/bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4%2B-d05140f-vs-3.13.0rc2.svg) |  |
| [2025-01-15](results/bm-20250115-3.14.0a4%2B-73aa5a2) | mpage/gh_115999_specialize | 73aa5a2 | 1.107x ↑<br>[📄](results/bm-20250115-3.14.0a4%2B-73aa5a2/bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-73aa5a2-vs-3.12.6.md)[📈](results/bm-20250115-3.14.0a4%2B-73aa5a2/bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-73aa5a2-vs-3.12.6.svg) | 1.068x ↑<br>[📄](results/bm-20250115-3.14.0a4%2B-73aa5a2/bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-73aa5a2-vs-3.13.0rc2.md)[📈](results/bm-20250115-3.14.0a4%2B-73aa5a2/bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-73aa5a2-vs-3.13.0rc2.svg) | 1.021x ↑<br>[📄](results/bm-20250115-3.14.0a4%2B-73aa5a2/bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-73aa5a2-vs-base.md)[📈](results/bm-20250115-3.14.0a4%2B-73aa5a2/bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-73aa5a2-vs-base.svg)[🧠](results/bm-20250115-3.14.0a4%2B-73aa5a2/bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-73aa5a2-vs-base-mem.svg) |
| [2025-01-15](results/bm-20250115-3.14.0a4%2B-73aa5a2-NOGIL) | mpage/gh_115999_specialize | 73aa5a2 (NOGIL) | 1.058x ↓<br>[📄](results/bm-20250115-3.14.0a4%2B-73aa5a2-NOGIL/bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-73aa5a2-vs-3.12.6.md)[📈](results/bm-20250115-3.14.0a4%2B-73aa5a2-NOGIL/bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-73aa5a2-vs-3.12.6.svg) | 1.088x ↓<br>[📄](results/bm-20250115-3.14.0a4%2B-73aa5a2-NOGIL/bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-73aa5a2-vs-3.13.0rc2.md)[📈](results/bm-20250115-3.14.0a4%2B-73aa5a2-NOGIL/bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-73aa5a2-vs-3.13.0rc2.svg) | 1.004x ↓<br>[📄](results/bm-20250115-3.14.0a4%2B-73aa5a2-NOGIL/bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-73aa5a2-vs-base.md)[📈](results/bm-20250115-3.14.0a4%2B-73aa5a2-NOGIL/bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-73aa5a2-vs-base.svg)[🧠](results/bm-20250115-3.14.0a4%2B-73aa5a2-NOGIL/bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-73aa5a2-vs-base-mem.svg) |
| [2025-01-15](results/bm-20250115-3.14.0a4%2B-3cedaed-NOGIL) | mpage/gh_115999_specialize | 3cedaed (NOGIL) | 1.053x ↓<br>[📄](results/bm-20250115-3.14.0a4%2B-3cedaed-NOGIL/bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-3cedaed-vs-3.12.6.md)[📈](results/bm-20250115-3.14.0a4%2B-3cedaed-NOGIL/bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-3cedaed-vs-3.12.6.svg) | 1.084x ↓<br>[📄](results/bm-20250115-3.14.0a4%2B-3cedaed-NOGIL/bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-3cedaed-vs-3.13.0rc2.md)[📈](results/bm-20250115-3.14.0a4%2B-3cedaed-NOGIL/bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-3cedaed-vs-3.13.0rc2.svg) | 1.000x ↑<br>[📄](results/bm-20250115-3.14.0a4%2B-3cedaed-NOGIL/bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-3cedaed-vs-base.md)[📈](results/bm-20250115-3.14.0a4%2B-3cedaed-NOGIL/bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-3cedaed-vs-base.svg)[🧠](results/bm-20250115-3.14.0a4%2B-3cedaed-NOGIL/bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-3cedaed-vs-base-mem.svg) |
| [2025-01-15](results/bm-20250115-3.14.0a4%2B-3cedaed) | mpage/gh_115999_specialize | 3cedaed | 1.102x ↑<br>[📄](results/bm-20250115-3.14.0a4%2B-3cedaed/bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-3cedaed-vs-3.12.6.md)[📈](results/bm-20250115-3.14.0a4%2B-3cedaed/bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-3cedaed-vs-3.12.6.svg) | 1.063x ↑<br>[📄](results/bm-20250115-3.14.0a4%2B-3cedaed/bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-3cedaed-vs-3.13.0rc2.md)[📈](results/bm-20250115-3.14.0a4%2B-3cedaed/bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-3cedaed-vs-3.13.0rc2.svg) | 1.016x ↑<br>[📄](results/bm-20250115-3.14.0a4%2B-3cedaed/bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-3cedaed-vs-base.md)[📈](results/bm-20250115-3.14.0a4%2B-3cedaed/bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-3cedaed-vs-base.svg)[🧠](results/bm-20250115-3.14.0a4%2B-3cedaed/bm-20250115-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4%2B-3cedaed-vs-base-mem.svg) |
| [2025-01-15](results/bm-20250115-3.14.0a4%2B-6e4f641) | python/6e4f64109b0eb6c9f1b5 | 6e4f641 | 1.110x ↑<br>[📄](results/bm-20250115-3.14.0a4%2B-6e4f641/bm-20250115-vultr-x86_64-python-6e4f64109b0eb6c9f1b5-3.14.0a4%2B-6e4f641-vs-3.12.6.md)[📈](results/bm-20250115-3.14.0a4%2B-6e4f641/bm-20250115-vultr-x86_64-python-6e4f64109b0eb6c9f1b5-3.14.0a4%2B-6e4f641-vs-3.12.6.svg) | 1.071x ↑<br>[📄](results/bm-20250115-3.14.0a4%2B-6e4f641/bm-20250115-vultr-x86_64-python-6e4f64109b0eb6c9f1b5-3.14.0a4%2B-6e4f641-vs-3.13.0rc2.md)[📈](results/bm-20250115-3.14.0a4%2B-6e4f641/bm-20250115-vultr-x86_64-python-6e4f64109b0eb6c9f1b5-3.14.0a4%2B-6e4f641-vs-3.13.0rc2.svg) |  |
| [2025-01-15](results/bm-20250115-3.14.0a4%2B-6e4f641-NOGIL) | python/6e4f64109b0eb6c9f1b5 | 6e4f641 (NOGIL) | 1.059x ↓<br>[📄](results/bm-20250115-3.14.0a4%2B-6e4f641-NOGIL/bm-20250115-vultr-x86_64-python-6e4f64109b0eb6c9f1b5-3.14.0a4%2B-6e4f641-vs-3.12.6.md)[📈](results/bm-20250115-3.14.0a4%2B-6e4f641-NOGIL/bm-20250115-vultr-x86_64-python-6e4f64109b0eb6c9f1b5-3.14.0a4%2B-6e4f641-vs-3.12.6.svg) | 1.089x ↓<br>[📄](results/bm-20250115-3.14.0a4%2B-6e4f641-NOGIL/bm-20250115-vultr-x86_64-python-6e4f64109b0eb6c9f1b5-3.14.0a4%2B-6e4f641-vs-3.13.0rc2.md)[📈](results/bm-20250115-3.14.0a4%2B-6e4f641-NOGIL/bm-20250115-vultr-x86_64-python-6e4f64109b0eb6c9f1b5-3.14.0a4%2B-6e4f641-vs-3.13.0rc2.svg) | 1.153x ↓<br>[📄](results/bm-20250115-3.14.0a4%2B-6e4f641-NOGIL/bm-20250115-vultr-x86_64-python-6e4f64109b0eb6c9f1b5-3.14.0a4%2B-6e4f641-vs-base.md)[📈](results/bm-20250115-3.14.0a4%2B-6e4f641-NOGIL/bm-20250115-vultr-x86_64-python-6e4f64109b0eb6c9f1b5-3.14.0a4%2B-6e4f641-vs-base.svg)[🧠](results/bm-20250115-3.14.0a4%2B-6e4f641-NOGIL/bm-20250115-vultr-x86_64-python-6e4f64109b0eb6c9f1b5-3.14.0a4%2B-6e4f641-vs-base-mem.svg) |
| [2025-01-15](results/bm-20250115-3.14.0a4%2B-b52de22) | python/b52de22ac345ad8583bc | b52de22 | 1.107x ↑<br>[📄](results/bm-20250115-3.14.0a4%2B-b52de22/bm-20250115-vultr-x86_64-python-b52de22ac345ad8583bc-3.14.0a4%2B-b52de22-vs-3.12.6.md)[📈](results/bm-20250115-3.14.0a4%2B-b52de22/bm-20250115-vultr-x86_64-python-b52de22ac345ad8583bc-3.14.0a4%2B-b52de22-vs-3.12.6.svg) | 1.068x ↑<br>[📄](results/bm-20250115-3.14.0a4%2B-b52de22/bm-20250115-vultr-x86_64-python-b52de22ac345ad8583bc-3.14.0a4%2B-b52de22-vs-3.13.0rc2.md)[📈](results/bm-20250115-3.14.0a4%2B-b52de22/bm-20250115-vultr-x86_64-python-b52de22ac345ad8583bc-3.14.0a4%2B-b52de22-vs-3.13.0rc2.svg) |  |
| [2025-01-15](results/bm-20250115-3.14.0a4%2B-b52de22-NOGIL) | python/b52de22ac345ad8583bc | b52de22 (NOGIL) | 1.066x ↓<br>[📄](results/bm-20250115-3.14.0a4%2B-b52de22-NOGIL/bm-20250115-vultr-x86_64-python-b52de22ac345ad8583bc-3.14.0a4%2B-b52de22-vs-3.12.6.md)[📈](results/bm-20250115-3.14.0a4%2B-b52de22-NOGIL/bm-20250115-vultr-x86_64-python-b52de22ac345ad8583bc-3.14.0a4%2B-b52de22-vs-3.12.6.svg) | 1.096x ↓<br>[📄](results/bm-20250115-3.14.0a4%2B-b52de22-NOGIL/bm-20250115-vultr-x86_64-python-b52de22ac345ad8583bc-3.14.0a4%2B-b52de22-vs-3.13.0rc2.md)[📈](results/bm-20250115-3.14.0a4%2B-b52de22-NOGIL/bm-20250115-vultr-x86_64-python-b52de22ac345ad8583bc-3.14.0a4%2B-b52de22-vs-3.13.0rc2.svg) | 1.156x ↓<br>[📄](results/bm-20250115-3.14.0a4%2B-b52de22-NOGIL/bm-20250115-vultr-x86_64-python-b52de22ac345ad8583bc-3.14.0a4%2B-b52de22-vs-base.md)[📈](results/bm-20250115-3.14.0a4%2B-b52de22-NOGIL/bm-20250115-vultr-x86_64-python-b52de22ac345ad8583bc-3.14.0a4%2B-b52de22-vs-base.svg)[🧠](results/bm-20250115-3.14.0a4%2B-b52de22-NOGIL/bm-20250115-vultr-x86_64-python-b52de22ac345ad8583bc-3.14.0a4%2B-b52de22-vs-base-mem.svg) |
| [2025-01-13](results/bm-20250113-3.14.0a3%2B-b70a567) | python/b70a567575db37846bee | b70a567 | 1.098x ↑<br>[📄](results/bm-20250113-3.14.0a3%2B-b70a567/bm-20250113-vultr-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-3.12.6.md)[📈](results/bm-20250113-3.14.0a3%2B-b70a567/bm-20250113-vultr-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-3.12.6.svg) | 1.060x ↑<br>[📄](results/bm-20250113-3.14.0a3%2B-b70a567/bm-20250113-vultr-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-3.13.0rc2.md)[📈](results/bm-20250113-3.14.0a3%2B-b70a567/bm-20250113-vultr-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-3.13.0rc2.svg) |  |
| [2025-01-13](results/bm-20250113-3.14.0a3%2B-b70a567-NOGIL) | python/b70a567575db37846bee | b70a567 (NOGIL) | 1.161x ↓<br>[📄](results/bm-20250113-3.14.0a3%2B-b70a567-NOGIL/bm-20250113-vultr-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-3.12.6.md)[📈](results/bm-20250113-3.14.0a3%2B-b70a567-NOGIL/bm-20250113-vultr-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-3.12.6.svg) | 1.188x ↓<br>[📄](results/bm-20250113-3.14.0a3%2B-b70a567-NOGIL/bm-20250113-vultr-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-3.13.0rc2.md)[📈](results/bm-20250113-3.14.0a3%2B-b70a567-NOGIL/bm-20250113-vultr-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-3.13.0rc2.svg) | 1.231x ↓<br>[📄](results/bm-20250113-3.14.0a3%2B-b70a567-NOGIL/bm-20250113-vultr-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-base.md)[📈](results/bm-20250113-3.14.0a3%2B-b70a567-NOGIL/bm-20250113-vultr-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-base.svg)[🧠](results/bm-20250113-3.14.0a3%2B-b70a567-NOGIL/bm-20250113-vultr-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-base-mem.svg) |
| [2025-01-13](results/bm-20250113-3.14.0a3%2B-0c173c9-NOGIL) | nascheme/nogil_gc_mark_alive | 0c173c9 (NOGIL) | 1.160x ↓<br>[📄](results/bm-20250113-3.14.0a3%2B-0c173c9-NOGIL/bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-0c173c9-vs-3.12.6.md)[📈](results/bm-20250113-3.14.0a3%2B-0c173c9-NOGIL/bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-0c173c9-vs-3.12.6.svg) | 1.187x ↓<br>[📄](results/bm-20250113-3.14.0a3%2B-0c173c9-NOGIL/bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-0c173c9-vs-3.13.0rc2.md)[📈](results/bm-20250113-3.14.0a3%2B-0c173c9-NOGIL/bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-0c173c9-vs-3.13.0rc2.svg) | 1.000x ↑<br>[📄](results/bm-20250113-3.14.0a3%2B-0c173c9-NOGIL/bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-0c173c9-vs-base.md)[📈](results/bm-20250113-3.14.0a3%2B-0c173c9-NOGIL/bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-0c173c9-vs-base.svg)[🧠](results/bm-20250113-3.14.0a3%2B-0c173c9-NOGIL/bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-0c173c9-vs-base-mem.svg) |
| [2025-01-11](results/bm-20250111-3.14.0a3%2B-553cdc6-NOGIL) | python/553cdc6d6856c1b4539a | 553cdc6 (NOGIL) | 1.160x ↓<br>[📄](results/bm-20250111-3.14.0a3%2B-553cdc6-NOGIL/bm-20250111-vultr-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-3.12.6.md)[📈](results/bm-20250111-3.14.0a3%2B-553cdc6-NOGIL/bm-20250111-vultr-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-3.12.6.svg) | 1.187x ↓<br>[📄](results/bm-20250111-3.14.0a3%2B-553cdc6-NOGIL/bm-20250111-vultr-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-3.13.0rc2.md)[📈](results/bm-20250111-3.14.0a3%2B-553cdc6-NOGIL/bm-20250111-vultr-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-3.13.0rc2.svg) | 1.002x ↓<br>[📄](results/bm-20250111-3.14.0a3%2B-553cdc6-NOGIL/bm-20250111-vultr-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-base.md)[📈](results/bm-20250111-3.14.0a3%2B-553cdc6-NOGIL/bm-20250111-vultr-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-base.svg)[🧠](results/bm-20250111-3.14.0a3%2B-553cdc6-NOGIL/bm-20250111-vultr-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-base-mem.svg) |


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
