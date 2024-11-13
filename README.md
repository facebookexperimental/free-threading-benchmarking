# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
[Most recent pystats on main (7d7d56d)](results/bm-20241102-3.14.0a1%2B-7d7d56d-PYTHON_UOPS/bm-20241102-vultr-x86_64-python-7d7d56d8b1147a6b85e1-3.14.0a1%2B-7d7d56d-pystats.md)

## linux x86_64 (linux)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2024-11-12](results/bm-20241112-3.14.0a1%2B-8cc6e5c) | python/8cc6e5c8751139e86b2a | 8cc6e5c | 1.00x ↑<br>[📄](results/bm-20241112-3.14.0a1%2B-8cc6e5c/bm-20241112-linux-x86_64-python-8cc6e5c8751139e86b2a-3.14.0a1%2B-8cc6e5c-vs-3.12.6.md)[📈](results/bm-20241112-3.14.0a1%2B-8cc6e5c/bm-20241112-linux-x86_64-python-8cc6e5c8751139e86b2a-3.14.0a1%2B-8cc6e5c-vs-3.12.6.svg) | 1.01x ↓<br>[📄](results/bm-20241112-3.14.0a1%2B-8cc6e5c/bm-20241112-linux-x86_64-python-8cc6e5c8751139e86b2a-3.14.0a1%2B-8cc6e5c-vs-3.13.0rc2.md)[📈](results/bm-20241112-3.14.0a1%2B-8cc6e5c/bm-20241112-linux-x86_64-python-8cc6e5c8751139e86b2a-3.14.0a1%2B-8cc6e5c-vs-3.13.0rc2.svg) |  |
| [2024-11-12](results/bm-20241112-3.14.0a1%2B-494360a) | python/494360afd00dc8f6b549 | 494360a | 1.01x ↑<br>[📄](results/bm-20241112-3.14.0a1%2B-494360a/bm-20241112-linux-x86_64-python-494360afd00dc8f6b549-3.14.0a1%2B-494360a-vs-3.12.6.md)[📈](results/bm-20241112-3.14.0a1%2B-494360a/bm-20241112-linux-x86_64-python-494360afd00dc8f6b549-3.14.0a1%2B-494360a-vs-3.12.6.svg) | 1.01x ↓<br>[📄](results/bm-20241112-3.14.0a1%2B-494360a/bm-20241112-linux-x86_64-python-494360afd00dc8f6b549-3.14.0a1%2B-494360a-vs-3.13.0rc2.md)[📈](results/bm-20241112-3.14.0a1%2B-494360a/bm-20241112-linux-x86_64-python-494360afd00dc8f6b549-3.14.0a1%2B-494360a-vs-3.13.0rc2.svg) |  |
| [2024-11-12](results/bm-20241112-3.14.0a1%2B-494360a-NOGIL) | python/494360afd00dc8f6b549 | 494360a (NOGIL) | 1.44x ↓<br>[📄](results/bm-20241112-3.14.0a1%2B-494360a-NOGIL/bm-20241112-linux-x86_64-python-494360afd00dc8f6b549-3.14.0a1%2B-494360a-vs-3.12.6.md)[📈](results/bm-20241112-3.14.0a1%2B-494360a-NOGIL/bm-20241112-linux-x86_64-python-494360afd00dc8f6b549-3.14.0a1%2B-494360a-vs-3.12.6.svg) | 1.46x ↓<br>[📄](results/bm-20241112-3.14.0a1%2B-494360a-NOGIL/bm-20241112-linux-x86_64-python-494360afd00dc8f6b549-3.14.0a1%2B-494360a-vs-3.13.0rc2.md)[📈](results/bm-20241112-3.14.0a1%2B-494360a-NOGIL/bm-20241112-linux-x86_64-python-494360afd00dc8f6b549-3.14.0a1%2B-494360a-vs-3.13.0rc2.svg) | 1.45x ↓<br>[📄](results/bm-20241112-3.14.0a1%2B-494360a-NOGIL/bm-20241112-linux-x86_64-python-494360afd00dc8f6b549-3.14.0a1%2B-494360a-vs-base.md)[📈](results/bm-20241112-3.14.0a1%2B-494360a-NOGIL/bm-20241112-linux-x86_64-python-494360afd00dc8f6b549-3.14.0a1%2B-494360a-vs-base.svg)[🧠](results/bm-20241112-3.14.0a1%2B-494360a-NOGIL/bm-20241112-linux-x86_64-python-494360afd00dc8f6b549-3.14.0a1%2B-494360a-vs-base-mem.svg) |
| [2024-11-10](results/bm-20241110-3.14.0a1%2B-f435de6-NOGIL) | python/f435de6765e032799585 | f435de6 (NOGIL) | 1.44x ↓<br>[📄](results/bm-20241110-3.14.0a1%2B-f435de6-NOGIL/bm-20241110-linux-x86_64-python-f435de6765e032799585-3.14.0a1%2B-f435de6-vs-3.12.6.md)[📈](results/bm-20241110-3.14.0a1%2B-f435de6-NOGIL/bm-20241110-linux-x86_64-python-f435de6765e032799585-3.14.0a1%2B-f435de6-vs-3.12.6.svg) | 1.46x ↓<br>[📄](results/bm-20241110-3.14.0a1%2B-f435de6-NOGIL/bm-20241110-linux-x86_64-python-f435de6765e032799585-3.14.0a1%2B-f435de6-vs-3.13.0rc2.md)[📈](results/bm-20241110-3.14.0a1%2B-f435de6-NOGIL/bm-20241110-linux-x86_64-python-f435de6765e032799585-3.14.0a1%2B-f435de6-vs-3.13.0rc2.svg) | 1.44x ↓<br>[📄](results/bm-20241110-3.14.0a1%2B-f435de6-NOGIL/bm-20241110-linux-x86_64-python-f435de6765e032799585-3.14.0a1%2B-f435de6-vs-base.md)[📈](results/bm-20241110-3.14.0a1%2B-f435de6-NOGIL/bm-20241110-linux-x86_64-python-f435de6765e032799585-3.14.0a1%2B-f435de6-vs-base.svg)[🧠](results/bm-20241110-3.14.0a1%2B-f435de6-NOGIL/bm-20241110-linux-x86_64-python-f435de6765e032799585-3.14.0a1%2B-f435de6-vs-base-mem.svg) |
| [2024-11-10](results/bm-20241110-3.14.0a1%2B-f435de6) | python/f435de6765e032799585 | f435de6 | 1.00x ↑<br>[📄](results/bm-20241110-3.14.0a1%2B-f435de6/bm-20241110-linux-x86_64-python-f435de6765e032799585-3.14.0a1%2B-f435de6-vs-3.12.6.md)[📈](results/bm-20241110-3.14.0a1%2B-f435de6/bm-20241110-linux-x86_64-python-f435de6765e032799585-3.14.0a1%2B-f435de6-vs-3.12.6.svg) | 1.01x ↓<br>[📄](results/bm-20241110-3.14.0a1%2B-f435de6/bm-20241110-linux-x86_64-python-f435de6765e032799585-3.14.0a1%2B-f435de6-vs-3.13.0rc2.md)[📈](results/bm-20241110-3.14.0a1%2B-f435de6/bm-20241110-linux-x86_64-python-f435de6765e032799585-3.14.0a1%2B-f435de6-vs-3.13.0rc2.svg) |  |
| [2024-11-09](results/bm-20241109-3.14.0a1%2B-9d08423) | python/9d08423b6e0fa89ce9cf | 9d08423 | 1.01x ↑<br>[📄](results/bm-20241109-3.14.0a1%2B-9d08423/bm-20241109-linux-x86_64-python-9d08423b6e0fa89ce9cf-3.14.0a1%2B-9d08423-vs-3.12.6.md)[📈](results/bm-20241109-3.14.0a1%2B-9d08423/bm-20241109-linux-x86_64-python-9d08423b6e0fa89ce9cf-3.14.0a1%2B-9d08423-vs-3.12.6.svg) | 1.00x ↓<br>[📄](results/bm-20241109-3.14.0a1%2B-9d08423/bm-20241109-linux-x86_64-python-9d08423b6e0fa89ce9cf-3.14.0a1%2B-9d08423-vs-3.13.0rc2.md)[📈](results/bm-20241109-3.14.0a1%2B-9d08423/bm-20241109-linux-x86_64-python-9d08423b6e0fa89ce9cf-3.14.0a1%2B-9d08423-vs-3.13.0rc2.svg) |  |
| [2024-11-09](results/bm-20241109-3.14.0a1%2B-9d08423-NOGIL) | python/9d08423b6e0fa89ce9cf | 9d08423 (NOGIL) | 1.44x ↓<br>[📄](results/bm-20241109-3.14.0a1%2B-9d08423-NOGIL/bm-20241109-linux-x86_64-python-9d08423b6e0fa89ce9cf-3.14.0a1%2B-9d08423-vs-3.12.6.md)[📈](results/bm-20241109-3.14.0a1%2B-9d08423-NOGIL/bm-20241109-linux-x86_64-python-9d08423b6e0fa89ce9cf-3.14.0a1%2B-9d08423-vs-3.12.6.svg) | 1.47x ↓<br>[📄](results/bm-20241109-3.14.0a1%2B-9d08423-NOGIL/bm-20241109-linux-x86_64-python-9d08423b6e0fa89ce9cf-3.14.0a1%2B-9d08423-vs-3.13.0rc2.md)[📈](results/bm-20241109-3.14.0a1%2B-9d08423-NOGIL/bm-20241109-linux-x86_64-python-9d08423b6e0fa89ce9cf-3.14.0a1%2B-9d08423-vs-3.13.0rc2.svg) | 1.46x ↓<br>[📄](results/bm-20241109-3.14.0a1%2B-9d08423-NOGIL/bm-20241109-linux-x86_64-python-9d08423b6e0fa89ce9cf-3.14.0a1%2B-9d08423-vs-base.md)[📈](results/bm-20241109-3.14.0a1%2B-9d08423-NOGIL/bm-20241109-linux-x86_64-python-9d08423b6e0fa89ce9cf-3.14.0a1%2B-9d08423-vs-base.svg)[🧠](results/bm-20241109-3.14.0a1%2B-9d08423-NOGIL/bm-20241109-linux-x86_64-python-9d08423b6e0fa89ce9cf-3.14.0a1%2B-9d08423-vs-base-mem.svg) |

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2024-11-13](results/bm-20241113-3.14.0a1%2B-b1f1c71) | corona10/gh_115999_bool | b1f1c71 | 1.00x ↓<br>[📄](results/bm-20241113-3.14.0a1%2B-b1f1c71/bm-20241113-vultr-x86_64-corona10-gh_115999_bool-3.14.0a1%2B-b1f1c71-vs-3.12.6.md)[📈](results/bm-20241113-3.14.0a1%2B-b1f1c71/bm-20241113-vultr-x86_64-corona10-gh_115999_bool-3.14.0a1%2B-b1f1c71-vs-3.12.6.svg) | 1.02x ↓<br>[📄](results/bm-20241113-3.14.0a1%2B-b1f1c71/bm-20241113-vultr-x86_64-corona10-gh_115999_bool-3.14.0a1%2B-b1f1c71-vs-3.13.0rc2.md)[📈](results/bm-20241113-3.14.0a1%2B-b1f1c71/bm-20241113-vultr-x86_64-corona10-gh_115999_bool-3.14.0a1%2B-b1f1c71-vs-3.13.0rc2.svg) | 1.01x ↑<br>[📄](results/bm-20241113-3.14.0a1%2B-b1f1c71/bm-20241113-vultr-x86_64-corona10-gh_115999_bool-3.14.0a1%2B-b1f1c71-vs-base.md)[📈](results/bm-20241113-3.14.0a1%2B-b1f1c71/bm-20241113-vultr-x86_64-corona10-gh_115999_bool-3.14.0a1%2B-b1f1c71-vs-base.svg)[🧠](results/bm-20241113-3.14.0a1%2B-b1f1c71/bm-20241113-vultr-x86_64-corona10-gh_115999_bool-3.14.0a1%2B-b1f1c71-vs-base-mem.svg) |
| [2024-11-12](results/bm-20241112-3.14.0a1%2B-8cc6e5c) | python/8cc6e5c8751139e86b2a | 8cc6e5c | 1.01x ↓<br>[📄](results/bm-20241112-3.14.0a1%2B-8cc6e5c/bm-20241112-vultr-x86_64-python-8cc6e5c8751139e86b2a-3.14.0a1%2B-8cc6e5c-vs-3.12.6.md)[📈](results/bm-20241112-3.14.0a1%2B-8cc6e5c/bm-20241112-vultr-x86_64-python-8cc6e5c8751139e86b2a-3.14.0a1%2B-8cc6e5c-vs-3.12.6.svg) | 1.02x ↓<br>[📄](results/bm-20241112-3.14.0a1%2B-8cc6e5c/bm-20241112-vultr-x86_64-python-8cc6e5c8751139e86b2a-3.14.0a1%2B-8cc6e5c-vs-3.13.0rc2.md)[📈](results/bm-20241112-3.14.0a1%2B-8cc6e5c/bm-20241112-vultr-x86_64-python-8cc6e5c8751139e86b2a-3.14.0a1%2B-8cc6e5c-vs-3.13.0rc2.svg) |  |
| [2024-11-12](results/bm-20241112-3.14.0a1%2B-8cc6e5c-NOGIL) | python/8cc6e5c8751139e86b2a | 8cc6e5c (NOGIL) | 1.55x ↓<br>[📄](results/bm-20241112-3.14.0a1%2B-8cc6e5c-NOGIL/bm-20241112-vultr-x86_64-python-8cc6e5c8751139e86b2a-3.14.0a1%2B-8cc6e5c-vs-3.12.6.md)[📈](results/bm-20241112-3.14.0a1%2B-8cc6e5c-NOGIL/bm-20241112-vultr-x86_64-python-8cc6e5c8751139e86b2a-3.14.0a1%2B-8cc6e5c-vs-3.12.6.svg) | 1.57x ↓<br>[📄](results/bm-20241112-3.14.0a1%2B-8cc6e5c-NOGIL/bm-20241112-vultr-x86_64-python-8cc6e5c8751139e86b2a-3.14.0a1%2B-8cc6e5c-vs-3.13.0rc2.md)[📈](results/bm-20241112-3.14.0a1%2B-8cc6e5c-NOGIL/bm-20241112-vultr-x86_64-python-8cc6e5c8751139e86b2a-3.14.0a1%2B-8cc6e5c-vs-3.13.0rc2.svg) | 1.54x ↓<br>[📄](results/bm-20241112-3.14.0a1%2B-8cc6e5c-NOGIL/bm-20241112-vultr-x86_64-python-8cc6e5c8751139e86b2a-3.14.0a1%2B-8cc6e5c-vs-base.md)[📈](results/bm-20241112-3.14.0a1%2B-8cc6e5c-NOGIL/bm-20241112-vultr-x86_64-python-8cc6e5c8751139e86b2a-3.14.0a1%2B-8cc6e5c-vs-base.svg)[🧠](results/bm-20241112-3.14.0a1%2B-8cc6e5c-NOGIL/bm-20241112-vultr-x86_64-python-8cc6e5c8751139e86b2a-3.14.0a1%2B-8cc6e5c-vs-base-mem.svg) |
| [2024-11-12](results/bm-20241112-3.14.0a1%2B-494360a) | python/494360afd00dc8f6b549 | 494360a | 1.01x ↓<br>[📄](results/bm-20241112-3.14.0a1%2B-494360a/bm-20241112-vultr-x86_64-python-494360afd00dc8f6b549-3.14.0a1%2B-494360a-vs-3.12.6.md)[📈](results/bm-20241112-3.14.0a1%2B-494360a/bm-20241112-vultr-x86_64-python-494360afd00dc8f6b549-3.14.0a1%2B-494360a-vs-3.12.6.svg) | 1.02x ↓<br>[📄](results/bm-20241112-3.14.0a1%2B-494360a/bm-20241112-vultr-x86_64-python-494360afd00dc8f6b549-3.14.0a1%2B-494360a-vs-3.13.0rc2.md)[📈](results/bm-20241112-3.14.0a1%2B-494360a/bm-20241112-vultr-x86_64-python-494360afd00dc8f6b549-3.14.0a1%2B-494360a-vs-3.13.0rc2.svg) |  |
| [2024-11-12](results/bm-20241112-3.14.0a1%2B-494360a-NOGIL) | python/494360afd00dc8f6b549 | 494360a (NOGIL) | 1.55x ↓<br>[📄](results/bm-20241112-3.14.0a1%2B-494360a-NOGIL/bm-20241112-vultr-x86_64-python-494360afd00dc8f6b549-3.14.0a1%2B-494360a-vs-3.12.6.md)[📈](results/bm-20241112-3.14.0a1%2B-494360a-NOGIL/bm-20241112-vultr-x86_64-python-494360afd00dc8f6b549-3.14.0a1%2B-494360a-vs-3.12.6.svg) | 1.57x ↓<br>[📄](results/bm-20241112-3.14.0a1%2B-494360a-NOGIL/bm-20241112-vultr-x86_64-python-494360afd00dc8f6b549-3.14.0a1%2B-494360a-vs-3.13.0rc2.md)[📈](results/bm-20241112-3.14.0a1%2B-494360a-NOGIL/bm-20241112-vultr-x86_64-python-494360afd00dc8f6b549-3.14.0a1%2B-494360a-vs-3.13.0rc2.svg) | 1.54x ↓<br>[📄](results/bm-20241112-3.14.0a1%2B-494360a-NOGIL/bm-20241112-vultr-x86_64-python-494360afd00dc8f6b549-3.14.0a1%2B-494360a-vs-base.md)[📈](results/bm-20241112-3.14.0a1%2B-494360a-NOGIL/bm-20241112-vultr-x86_64-python-494360afd00dc8f6b549-3.14.0a1%2B-494360a-vs-base.svg)[🧠](results/bm-20241112-3.14.0a1%2B-494360a-NOGIL/bm-20241112-vultr-x86_64-python-494360afd00dc8f6b549-3.14.0a1%2B-494360a-vs-base-mem.svg) |
| [2024-11-10](results/bm-20241110-3.14.0a1%2B-f435de6-NOGIL) | python/f435de6765e032799585 | f435de6 (NOGIL) | 1.55x ↓<br>[📄](results/bm-20241110-3.14.0a1%2B-f435de6-NOGIL/bm-20241110-vultr-x86_64-python-f435de6765e032799585-3.14.0a1%2B-f435de6-vs-3.12.6.md)[📈](results/bm-20241110-3.14.0a1%2B-f435de6-NOGIL/bm-20241110-vultr-x86_64-python-f435de6765e032799585-3.14.0a1%2B-f435de6-vs-3.12.6.svg) | 1.57x ↓<br>[📄](results/bm-20241110-3.14.0a1%2B-f435de6-NOGIL/bm-20241110-vultr-x86_64-python-f435de6765e032799585-3.14.0a1%2B-f435de6-vs-3.13.0rc2.md)[📈](results/bm-20241110-3.14.0a1%2B-f435de6-NOGIL/bm-20241110-vultr-x86_64-python-f435de6765e032799585-3.14.0a1%2B-f435de6-vs-3.13.0rc2.svg) | 1.54x ↓<br>[📄](results/bm-20241110-3.14.0a1%2B-f435de6-NOGIL/bm-20241110-vultr-x86_64-python-f435de6765e032799585-3.14.0a1%2B-f435de6-vs-base.md)[📈](results/bm-20241110-3.14.0a1%2B-f435de6-NOGIL/bm-20241110-vultr-x86_64-python-f435de6765e032799585-3.14.0a1%2B-f435de6-vs-base.svg)[🧠](results/bm-20241110-3.14.0a1%2B-f435de6-NOGIL/bm-20241110-vultr-x86_64-python-f435de6765e032799585-3.14.0a1%2B-f435de6-vs-base-mem.svg) |
| [2024-11-10](results/bm-20241110-3.14.0a1%2B-f435de6) | python/f435de6765e032799585 | f435de6 | 1.00x ↓<br>[📄](results/bm-20241110-3.14.0a1%2B-f435de6/bm-20241110-vultr-x86_64-python-f435de6765e032799585-3.14.0a1%2B-f435de6-vs-3.12.6.md)[📈](results/bm-20241110-3.14.0a1%2B-f435de6/bm-20241110-vultr-x86_64-python-f435de6765e032799585-3.14.0a1%2B-f435de6-vs-3.12.6.svg) | 1.02x ↓<br>[📄](results/bm-20241110-3.14.0a1%2B-f435de6/bm-20241110-vultr-x86_64-python-f435de6765e032799585-3.14.0a1%2B-f435de6-vs-3.13.0rc2.md)[📈](results/bm-20241110-3.14.0a1%2B-f435de6/bm-20241110-vultr-x86_64-python-f435de6765e032799585-3.14.0a1%2B-f435de6-vs-3.13.0rc2.svg) |  |
| [2024-11-09](results/bm-20241109-3.14.0a1%2B-9d08423) | python/9d08423b6e0fa89ce9cf | 9d08423 | 1.01x ↓<br>[📄](results/bm-20241109-3.14.0a1%2B-9d08423/bm-20241109-vultr-x86_64-python-9d08423b6e0fa89ce9cf-3.14.0a1%2B-9d08423-vs-3.12.6.md)[📈](results/bm-20241109-3.14.0a1%2B-9d08423/bm-20241109-vultr-x86_64-python-9d08423b6e0fa89ce9cf-3.14.0a1%2B-9d08423-vs-3.12.6.svg) | 1.03x ↓<br>[📄](results/bm-20241109-3.14.0a1%2B-9d08423/bm-20241109-vultr-x86_64-python-9d08423b6e0fa89ce9cf-3.14.0a1%2B-9d08423-vs-3.13.0rc2.md)[📈](results/bm-20241109-3.14.0a1%2B-9d08423/bm-20241109-vultr-x86_64-python-9d08423b6e0fa89ce9cf-3.14.0a1%2B-9d08423-vs-3.13.0rc2.svg) |  |
| [2024-11-09](results/bm-20241109-3.14.0a1%2B-9d08423-NOGIL) | python/9d08423b6e0fa89ce9cf | 9d08423 (NOGIL) | 1.56x ↓<br>[📄](results/bm-20241109-3.14.0a1%2B-9d08423-NOGIL/bm-20241109-vultr-x86_64-python-9d08423b6e0fa89ce9cf-3.14.0a1%2B-9d08423-vs-3.12.6.md)[📈](results/bm-20241109-3.14.0a1%2B-9d08423-NOGIL/bm-20241109-vultr-x86_64-python-9d08423b6e0fa89ce9cf-3.14.0a1%2B-9d08423-vs-3.12.6.svg) | 1.58x ↓<br>[📄](results/bm-20241109-3.14.0a1%2B-9d08423-NOGIL/bm-20241109-vultr-x86_64-python-9d08423b6e0fa89ce9cf-3.14.0a1%2B-9d08423-vs-3.13.0rc2.md)[📈](results/bm-20241109-3.14.0a1%2B-9d08423-NOGIL/bm-20241109-vultr-x86_64-python-9d08423b6e0fa89ce9cf-3.14.0a1%2B-9d08423-vs-3.13.0rc2.svg) | 1.54x ↓<br>[📄](results/bm-20241109-3.14.0a1%2B-9d08423-NOGIL/bm-20241109-vultr-x86_64-python-9d08423b6e0fa89ce9cf-3.14.0a1%2B-9d08423-vs-base.md)[📈](results/bm-20241109-3.14.0a1%2B-9d08423-NOGIL/bm-20241109-vultr-x86_64-python-9d08423b6e0fa89ce9cf-3.14.0a1%2B-9d08423-vs-base.svg)[🧠](results/bm-20241109-3.14.0a1%2B-9d08423-NOGIL/bm-20241109-vultr-x86_64-python-9d08423b6e0fa89ce9cf-3.14.0a1%2B-9d08423-vs-base-mem.svg) |
| [2024-11-09](results/bm-20241109-3.14.0a1%2B-6293d00) | python/6293d00e7201f3f28b1f | 6293d00 | 1.01x ↓<br>[📄](results/bm-20241109-3.14.0a1%2B-6293d00/bm-20241109-vultr-x86_64-python-6293d00e7201f3f28b1f-3.14.0a1%2B-6293d00-vs-3.12.6.md)[📈](results/bm-20241109-3.14.0a1%2B-6293d00/bm-20241109-vultr-x86_64-python-6293d00e7201f3f28b1f-3.14.0a1%2B-6293d00-vs-3.12.6.svg) | 1.02x ↓<br>[📄](results/bm-20241109-3.14.0a1%2B-6293d00/bm-20241109-vultr-x86_64-python-6293d00e7201f3f28b1f-3.14.0a1%2B-6293d00-vs-3.13.0rc2.md)[📈](results/bm-20241109-3.14.0a1%2B-6293d00/bm-20241109-vultr-x86_64-python-6293d00e7201f3f28b1f-3.14.0a1%2B-6293d00-vs-3.13.0rc2.svg) |  |
| [2024-11-08](results/bm-20241108-3.14.0a1%2B-d49e9e6) | Eclips4/ft_specialize_unpack | d49e9e6 | 1.00x ↓<br>[📄](results/bm-20241108-3.14.0a1%2B-d49e9e6/bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1%2B-d49e9e6-vs-3.12.6.md)[📈](results/bm-20241108-3.14.0a1%2B-d49e9e6/bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1%2B-d49e9e6-vs-3.12.6.svg) | 1.02x ↓<br>[📄](results/bm-20241108-3.14.0a1%2B-d49e9e6/bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1%2B-d49e9e6-vs-3.13.0rc2.md)[📈](results/bm-20241108-3.14.0a1%2B-d49e9e6/bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1%2B-d49e9e6-vs-3.13.0rc2.svg) | 1.00x ↑<br>[📄](results/bm-20241108-3.14.0a1%2B-d49e9e6/bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1%2B-d49e9e6-vs-base.md)[📈](results/bm-20241108-3.14.0a1%2B-d49e9e6/bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1%2B-d49e9e6-vs-base.svg)[🧠](results/bm-20241108-3.14.0a1%2B-d49e9e6/bm-20241108-vultr-x86_64-Eclips4-ft_specialize_unpack-3.14.0a1%2B-d49e9e6-vs-base-mem.svg) |
| [2024-11-07](results/bm-20241107-3.14.0a1%2B-85036c8) | python/85036c8d612007356d21 | 85036c8 | 1.00x ↓<br>[📄](results/bm-20241107-3.14.0a1%2B-85036c8/bm-20241107-vultr-x86_64-python-85036c8d612007356d21-3.14.0a1%2B-85036c8-vs-3.12.6.md)[📈](results/bm-20241107-3.14.0a1%2B-85036c8/bm-20241107-vultr-x86_64-python-85036c8d612007356d21-3.14.0a1%2B-85036c8-vs-3.12.6.svg) | 1.02x ↓<br>[📄](results/bm-20241107-3.14.0a1%2B-85036c8/bm-20241107-vultr-x86_64-python-85036c8d612007356d21-3.14.0a1%2B-85036c8-vs-3.13.0rc2.md)[📈](results/bm-20241107-3.14.0a1%2B-85036c8/bm-20241107-vultr-x86_64-python-85036c8d612007356d21-3.14.0a1%2B-85036c8-vs-3.13.0rc2.svg) |  |


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
