# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (a3990df)](results/bm-20250308-3.14.0a5%2B-a3990df/bm-20250308-linux-x86_64-python-a3990df6121880e8c678-3.14.0a5%2B-a3990df-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (e82c2ca)](results/bm-20250315-3.14.0a6%2B-e82c2ca-PYTHON_UOPS/bm-20250315-linux-x86_64-python-e82c2ca2a59235bc1965-3.14.0a6%2B-e82c2ca-pystats.md)

## linux x86_64 (linux)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-03-18](results/bm-20250318-3.14.0a6%2B-49234c0) | python/49234c065cf2b1ea32c5 | 49234c0 | 1.042x ↑<br>[📄](results/bm-20250318-3.14.0a6%2B-49234c0/bm-20250318-linux-x86_64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-3.12.6.md)[📈](results/bm-20250318-3.14.0a6%2B-49234c0/bm-20250318-linux-x86_64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-3.12.6.svg) | 1.002x ↑<br>[📄](results/bm-20250318-3.14.0a6%2B-49234c0/bm-20250318-linux-x86_64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-3.13.0rc2.md)[📈](results/bm-20250318-3.14.0a6%2B-49234c0/bm-20250318-linux-x86_64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-3.13.0rc2.svg) |  |
| [2025-03-17](results/bm-20250317-3.14.0a6%2B-a936af9) | python/a936af924efc6e2fb59e | a936af9 | 1.080x ↑<br>[📄](results/bm-20250317-3.14.0a6%2B-a936af9/bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-3.12.6.md)[📈](results/bm-20250317-3.14.0a6%2B-a936af9/bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-3.12.6.svg) | 1.036x ↑<br>[📄](results/bm-20250317-3.14.0a6%2B-a936af9/bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-3.13.0rc2.md)[📈](results/bm-20250317-3.14.0a6%2B-a936af9/bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-3.13.0rc2.svg) |  |
| [2025-03-17](results/bm-20250317-3.14.0a6%2B-a936af9-NOGIL) | python/a936af924efc6e2fb59e | a936af9 (NOGIL) | 1.018x ↓<br>[📄](results/bm-20250317-3.14.0a6%2B-a936af9-NOGIL/bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-3.12.6.md)[📈](results/bm-20250317-3.14.0a6%2B-a936af9-NOGIL/bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-3.12.6.svg) | 1.055x ↓<br>[📄](results/bm-20250317-3.14.0a6%2B-a936af9-NOGIL/bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-3.13.0rc2.md)[📈](results/bm-20250317-3.14.0a6%2B-a936af9-NOGIL/bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-3.13.0rc2.svg) | 1.088x ↓<br>[📄](results/bm-20250317-3.14.0a6%2B-a936af9-NOGIL/bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-base.md)[📈](results/bm-20250317-3.14.0a6%2B-a936af9-NOGIL/bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-base.svg)[🧠](results/bm-20250317-3.14.0a6%2B-a936af9-NOGIL/bm-20250317-linux-x86_64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-base-mem.svg) |
| [2025-03-17](results/bm-20250317-3.14.0a6%2B-cf288e3-NOGIL) | python/cf288e3c250f5538aa63 | cf288e3 (NOGIL) | 1.044x ↓<br>[📄](results/bm-20250317-3.14.0a6%2B-cf288e3-NOGIL/bm-20250317-linux-x86_64-python-cf288e3c250f5538aa63-3.14.0a6%2B-cf288e3-vs-3.12.6.md)[📈](results/bm-20250317-3.14.0a6%2B-cf288e3-NOGIL/bm-20250317-linux-x86_64-python-cf288e3c250f5538aa63-3.14.0a6%2B-cf288e3-vs-3.12.6.svg) | 1.080x ↓<br>[📄](results/bm-20250317-3.14.0a6%2B-cf288e3-NOGIL/bm-20250317-linux-x86_64-python-cf288e3c250f5538aa63-3.14.0a6%2B-cf288e3-vs-3.13.0rc2.md)[📈](results/bm-20250317-3.14.0a6%2B-cf288e3-NOGIL/bm-20250317-linux-x86_64-python-cf288e3c250f5538aa63-3.14.0a6%2B-cf288e3-vs-3.13.0rc2.svg) | 1.107x ↓<br>[📄](results/bm-20250317-3.14.0a6%2B-cf288e3-NOGIL/bm-20250317-linux-x86_64-python-cf288e3c250f5538aa63-3.14.0a6%2B-cf288e3-vs-base.md)[📈](results/bm-20250317-3.14.0a6%2B-cf288e3-NOGIL/bm-20250317-linux-x86_64-python-cf288e3c250f5538aa63-3.14.0a6%2B-cf288e3-vs-base.svg)[🧠](results/bm-20250317-3.14.0a6%2B-cf288e3-NOGIL/bm-20250317-linux-x86_64-python-cf288e3c250f5538aa63-3.14.0a6%2B-cf288e3-vs-base-mem.svg) |
| [2025-03-17](results/bm-20250317-3.14.0a6%2B-cf288e3) | python/cf288e3c250f5538aa63 | cf288e3 | 1.072x ↑<br>[📄](results/bm-20250317-3.14.0a6%2B-cf288e3/bm-20250317-linux-x86_64-python-cf288e3c250f5538aa63-3.14.0a6%2B-cf288e3-vs-3.12.6.md)[📈](results/bm-20250317-3.14.0a6%2B-cf288e3/bm-20250317-linux-x86_64-python-cf288e3c250f5538aa63-3.14.0a6%2B-cf288e3-vs-3.12.6.svg) | 1.034x ↑<br>[📄](results/bm-20250317-3.14.0a6%2B-cf288e3/bm-20250317-linux-x86_64-python-cf288e3c250f5538aa63-3.14.0a6%2B-cf288e3-vs-3.13.0rc2.md)[📈](results/bm-20250317-3.14.0a6%2B-cf288e3/bm-20250317-linux-x86_64-python-cf288e3c250f5538aa63-3.14.0a6%2B-cf288e3-vs-3.13.0rc2.svg) |  |
| [2025-03-15](results/bm-20250315-3.14.0a6%2B-e82c2ca) | python/e82c2ca2a59235bc1965 | e82c2ca | 1.069x ↑<br>[📄](results/bm-20250315-3.14.0a6%2B-e82c2ca/bm-20250315-linux-x86_64-python-e82c2ca2a59235bc1965-3.14.0a6%2B-e82c2ca-vs-3.12.6.md)[📈](results/bm-20250315-3.14.0a6%2B-e82c2ca/bm-20250315-linux-x86_64-python-e82c2ca2a59235bc1965-3.14.0a6%2B-e82c2ca-vs-3.12.6.svg) | 1.029x ↑<br>[📄](results/bm-20250315-3.14.0a6%2B-e82c2ca/bm-20250315-linux-x86_64-python-e82c2ca2a59235bc1965-3.14.0a6%2B-e82c2ca-vs-3.13.0rc2.md)[📈](results/bm-20250315-3.14.0a6%2B-e82c2ca/bm-20250315-linux-x86_64-python-e82c2ca2a59235bc1965-3.14.0a6%2B-e82c2ca-vs-3.13.0rc2.svg) |  |
| [2025-03-15](results/bm-20250315-3.14.0a6%2B-e82c2ca-NOGIL) | python/e82c2ca2a59235bc1965 | e82c2ca (NOGIL) | 1.032x ↓<br>[📄](results/bm-20250315-3.14.0a6%2B-e82c2ca-NOGIL/bm-20250315-linux-x86_64-python-e82c2ca2a59235bc1965-3.14.0a6%2B-e82c2ca-vs-3.12.6.md)[📈](results/bm-20250315-3.14.0a6%2B-e82c2ca-NOGIL/bm-20250315-linux-x86_64-python-e82c2ca2a59235bc1965-3.14.0a6%2B-e82c2ca-vs-3.12.6.svg) | 1.068x ↓<br>[📄](results/bm-20250315-3.14.0a6%2B-e82c2ca-NOGIL/bm-20250315-linux-x86_64-python-e82c2ca2a59235bc1965-3.14.0a6%2B-e82c2ca-vs-3.13.0rc2.md)[📈](results/bm-20250315-3.14.0a6%2B-e82c2ca-NOGIL/bm-20250315-linux-x86_64-python-e82c2ca2a59235bc1965-3.14.0a6%2B-e82c2ca-vs-3.13.0rc2.svg) | 1.087x ↓<br>[📄](results/bm-20250315-3.14.0a6%2B-e82c2ca-NOGIL/bm-20250315-linux-x86_64-python-e82c2ca2a59235bc1965-3.14.0a6%2B-e82c2ca-vs-base.md)[📈](results/bm-20250315-3.14.0a6%2B-e82c2ca-NOGIL/bm-20250315-linux-x86_64-python-e82c2ca2a59235bc1965-3.14.0a6%2B-e82c2ca-vs-base.svg)[🧠](results/bm-20250315-3.14.0a6%2B-e82c2ca-NOGIL/bm-20250315-linux-x86_64-python-e82c2ca2a59235bc1965-3.14.0a6%2B-e82c2ca-vs-base-mem.svg) |
| [2025-03-14](results/bm-20250314-3.14.0a6%2B-55815a6-NOGIL) | python/55815a6474c59001f023 | 55815a6 (NOGIL) | 1.026x ↓<br>[📄](results/bm-20250314-3.14.0a6%2B-55815a6-NOGIL/bm-20250314-linux-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-3.12.6.md)[📈](results/bm-20250314-3.14.0a6%2B-55815a6-NOGIL/bm-20250314-linux-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-3.12.6.svg) | 1.063x ↓<br>[📄](results/bm-20250314-3.14.0a6%2B-55815a6-NOGIL/bm-20250314-linux-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-3.13.0rc2.md)[📈](results/bm-20250314-3.14.0a6%2B-55815a6-NOGIL/bm-20250314-linux-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-3.13.0rc2.svg) | 1.105x ↓<br>[📄](results/bm-20250314-3.14.0a6%2B-55815a6-NOGIL/bm-20250314-linux-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-base.md)[📈](results/bm-20250314-3.14.0a6%2B-55815a6-NOGIL/bm-20250314-linux-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-base.svg)[🧠](results/bm-20250314-3.14.0a6%2B-55815a6-NOGIL/bm-20250314-linux-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-base-mem.svg) |
| [2025-03-14](results/bm-20250314-3.14.0a6%2B-55815a6) | python/55815a6474c59001f023 | 55815a6 | 1.093x ↑<br>[📄](results/bm-20250314-3.14.0a6%2B-55815a6/bm-20250314-linux-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-3.12.6.md)[📈](results/bm-20250314-3.14.0a6%2B-55815a6/bm-20250314-linux-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-3.12.6.svg) | 1.051x ↑<br>[📄](results/bm-20250314-3.14.0a6%2B-55815a6/bm-20250314-linux-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-3.13.0rc2.md)[📈](results/bm-20250314-3.14.0a6%2B-55815a6/bm-20250314-linux-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-3.13.0rc2.svg) |  |

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-03-18](results/bm-20250318-3.14.0a6%2B-49234c0) | python/49234c065cf2b1ea32c5 | 49234c0 | 1.061x ↑<br>[📄](results/bm-20250318-3.14.0a6%2B-49234c0/bm-20250318-vultr-x86_64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-3.12.6.md)[📈](results/bm-20250318-3.14.0a6%2B-49234c0/bm-20250318-vultr-x86_64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-3.12.6.svg) | 1.022x ↑<br>[📄](results/bm-20250318-3.14.0a6%2B-49234c0/bm-20250318-vultr-x86_64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-3.13.0rc2.md)[📈](results/bm-20250318-3.14.0a6%2B-49234c0/bm-20250318-vultr-x86_64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-3.13.0rc2.svg) |  |
| [2025-03-18](results/bm-20250318-3.14.0a6%2B-49234c0-NOGIL) | python/49234c065cf2b1ea32c5 | 49234c0 (NOGIL) | 1.049x ↓<br>[📄](results/bm-20250318-3.14.0a6%2B-49234c0-NOGIL/bm-20250318-vultr-x86_64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-3.12.6.md)[📈](results/bm-20250318-3.14.0a6%2B-49234c0-NOGIL/bm-20250318-vultr-x86_64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-3.12.6.svg) | 1.081x ↓<br>[📄](results/bm-20250318-3.14.0a6%2B-49234c0-NOGIL/bm-20250318-vultr-x86_64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-3.13.0rc2.md)[📈](results/bm-20250318-3.14.0a6%2B-49234c0-NOGIL/bm-20250318-vultr-x86_64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-3.13.0rc2.svg) | 1.105x ↓<br>[📄](results/bm-20250318-3.14.0a6%2B-49234c0-NOGIL/bm-20250318-vultr-x86_64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-base.md)[📈](results/bm-20250318-3.14.0a6%2B-49234c0-NOGIL/bm-20250318-vultr-x86_64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-base.svg)[🧠](results/bm-20250318-3.14.0a6%2B-49234c0-NOGIL/bm-20250318-vultr-x86_64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-base-mem.svg) |
| [2025-03-17](results/bm-20250317-3.14.0a6%2B-a936af9) | python/a936af924efc6e2fb59e | a936af9 | 1.058x ↑<br>[📄](results/bm-20250317-3.14.0a6%2B-a936af9/bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-3.12.6.md)[📈](results/bm-20250317-3.14.0a6%2B-a936af9/bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-3.12.6.svg) | 1.020x ↑<br>[📄](results/bm-20250317-3.14.0a6%2B-a936af9/bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-3.13.0rc2.md)[📈](results/bm-20250317-3.14.0a6%2B-a936af9/bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-3.13.0rc2.svg) |  |
| [2025-03-17](results/bm-20250317-3.14.0a6%2B-a936af9-NOGIL) | python/a936af924efc6e2fb59e | a936af9 (NOGIL) | 1.060x ↓<br>[📄](results/bm-20250317-3.14.0a6%2B-a936af9-NOGIL/bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-3.12.6.md)[📈](results/bm-20250317-3.14.0a6%2B-a936af9-NOGIL/bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-3.12.6.svg) | 1.092x ↓<br>[📄](results/bm-20250317-3.14.0a6%2B-a936af9-NOGIL/bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-3.13.0rc2.md)[📈](results/bm-20250317-3.14.0a6%2B-a936af9-NOGIL/bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-3.13.0rc2.svg) | 1.113x ↓<br>[📄](results/bm-20250317-3.14.0a6%2B-a936af9-NOGIL/bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-base.md)[📈](results/bm-20250317-3.14.0a6%2B-a936af9-NOGIL/bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-base.svg)[🧠](results/bm-20250317-3.14.0a6%2B-a936af9-NOGIL/bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-base-mem.svg) |
| [2025-03-17](results/bm-20250317-3.14.0a6%2B-fd545d7-NOGIL) | python/fd545d735d5f9c048f99 | fd545d7 (NOGIL) | 1.047x ↓<br>[📄](results/bm-20250317-3.14.0a6%2B-fd545d7-NOGIL/bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6%2B-fd545d7-vs-3.12.6.md)[📈](results/bm-20250317-3.14.0a6%2B-fd545d7-NOGIL/bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6%2B-fd545d7-vs-3.12.6.svg) | 1.079x ↓<br>[📄](results/bm-20250317-3.14.0a6%2B-fd545d7-NOGIL/bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6%2B-fd545d7-vs-3.13.0rc2.md)[📈](results/bm-20250317-3.14.0a6%2B-fd545d7-NOGIL/bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6%2B-fd545d7-vs-3.13.0rc2.svg) | 1.103x ↓<br>[📄](results/bm-20250317-3.14.0a6%2B-fd545d7-NOGIL/bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6%2B-fd545d7-vs-base.md)[📈](results/bm-20250317-3.14.0a6%2B-fd545d7-NOGIL/bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6%2B-fd545d7-vs-base.svg)[🧠](results/bm-20250317-3.14.0a6%2B-fd545d7-NOGIL/bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6%2B-fd545d7-vs-base-mem.svg) |
| [2025-03-17](results/bm-20250317-3.14.0a6%2B-fd545d7) | python/fd545d735d5f9c048f99 | fd545d7 | 1.061x ↑<br>[📄](results/bm-20250317-3.14.0a6%2B-fd545d7/bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6%2B-fd545d7-vs-3.12.6.md)[📈](results/bm-20250317-3.14.0a6%2B-fd545d7/bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6%2B-fd545d7-vs-3.12.6.svg) | 1.022x ↑<br>[📄](results/bm-20250317-3.14.0a6%2B-fd545d7/bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6%2B-fd545d7-vs-3.13.0rc2.md)[📈](results/bm-20250317-3.14.0a6%2B-fd545d7/bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6%2B-fd545d7-vs-3.13.0rc2.svg) |  |
| [2025-03-17](results/bm-20250317-3.14.0a6%2B-6c2f07d-NOGIL) | mpage/load_fast_borrow_abs | 6c2f07d (NOGIL) | 1.020x ↓<br>[📄](results/bm-20250317-3.14.0a6%2B-6c2f07d-NOGIL/bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6%2B-6c2f07d-vs-3.12.6.md)[📈](results/bm-20250317-3.14.0a6%2B-6c2f07d-NOGIL/bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6%2B-6c2f07d-vs-3.12.6.svg) | 1.052x ↓<br>[📄](results/bm-20250317-3.14.0a6%2B-6c2f07d-NOGIL/bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6%2B-6c2f07d-vs-3.13.0rc2.md)[📈](results/bm-20250317-3.14.0a6%2B-6c2f07d-NOGIL/bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6%2B-6c2f07d-vs-3.13.0rc2.svg) | 1.027x ↑<br>[📄](results/bm-20250317-3.14.0a6%2B-6c2f07d-NOGIL/bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6%2B-6c2f07d-vs-base.md)[📈](results/bm-20250317-3.14.0a6%2B-6c2f07d-NOGIL/bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6%2B-6c2f07d-vs-base.svg)[🧠](results/bm-20250317-3.14.0a6%2B-6c2f07d-NOGIL/bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6%2B-6c2f07d-vs-base-mem.svg) |
| [2025-03-17](results/bm-20250317-3.14.0a6%2B-6c2f07d) | mpage/load_fast_borrow_abs | 6c2f07d | 1.096x ↑<br>[📄](results/bm-20250317-3.14.0a6%2B-6c2f07d/bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6%2B-6c2f07d-vs-3.12.6.md)[📈](results/bm-20250317-3.14.0a6%2B-6c2f07d/bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6%2B-6c2f07d-vs-3.12.6.svg) | 1.056x ↑<br>[📄](results/bm-20250317-3.14.0a6%2B-6c2f07d/bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6%2B-6c2f07d-vs-3.13.0rc2.md)[📈](results/bm-20250317-3.14.0a6%2B-6c2f07d/bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6%2B-6c2f07d-vs-3.13.0rc2.svg) | 1.032x ↑<br>[📄](results/bm-20250317-3.14.0a6%2B-6c2f07d/bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6%2B-6c2f07d-vs-base.md)[📈](results/bm-20250317-3.14.0a6%2B-6c2f07d/bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6%2B-6c2f07d-vs-base.svg)[🧠](results/bm-20250317-3.14.0a6%2B-6c2f07d/bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6%2B-6c2f07d-vs-base-mem.svg) |
| [2025-03-17](results/bm-20250317-3.14.0a6%2B-cf288e3-NOGIL) | python/cf288e3c250f5538aa63 | cf288e3 (NOGIL) | 1.046x ↓<br>[📄](results/bm-20250317-3.14.0a6%2B-cf288e3-NOGIL/bm-20250317-vultr-x86_64-python-cf288e3c250f5538aa63-3.14.0a6%2B-cf288e3-vs-3.12.6.md)[📈](results/bm-20250317-3.14.0a6%2B-cf288e3-NOGIL/bm-20250317-vultr-x86_64-python-cf288e3c250f5538aa63-3.14.0a6%2B-cf288e3-vs-3.12.6.svg) | 1.078x ↓<br>[📄](results/bm-20250317-3.14.0a6%2B-cf288e3-NOGIL/bm-20250317-vultr-x86_64-python-cf288e3c250f5538aa63-3.14.0a6%2B-cf288e3-vs-3.13.0rc2.md)[📈](results/bm-20250317-3.14.0a6%2B-cf288e3-NOGIL/bm-20250317-vultr-x86_64-python-cf288e3c250f5538aa63-3.14.0a6%2B-cf288e3-vs-3.13.0rc2.svg) | 1.098x ↓<br>[📄](results/bm-20250317-3.14.0a6%2B-cf288e3-NOGIL/bm-20250317-vultr-x86_64-python-cf288e3c250f5538aa63-3.14.0a6%2B-cf288e3-vs-base.md)[📈](results/bm-20250317-3.14.0a6%2B-cf288e3-NOGIL/bm-20250317-vultr-x86_64-python-cf288e3c250f5538aa63-3.14.0a6%2B-cf288e3-vs-base.svg)[🧠](results/bm-20250317-3.14.0a6%2B-cf288e3-NOGIL/bm-20250317-vultr-x86_64-python-cf288e3c250f5538aa63-3.14.0a6%2B-cf288e3-vs-base-mem.svg) |
| [2025-03-17](results/bm-20250317-3.14.0a6%2B-cf288e3) | python/cf288e3c250f5538aa63 | cf288e3 | 1.056x ↑<br>[📄](results/bm-20250317-3.14.0a6%2B-cf288e3/bm-20250317-vultr-x86_64-python-cf288e3c250f5538aa63-3.14.0a6%2B-cf288e3-vs-3.12.6.md)[📈](results/bm-20250317-3.14.0a6%2B-cf288e3/bm-20250317-vultr-x86_64-python-cf288e3c250f5538aa63-3.14.0a6%2B-cf288e3-vs-3.12.6.svg) | 1.017x ↑<br>[📄](results/bm-20250317-3.14.0a6%2B-cf288e3/bm-20250317-vultr-x86_64-python-cf288e3c250f5538aa63-3.14.0a6%2B-cf288e3-vs-3.13.0rc2.md)[📈](results/bm-20250317-3.14.0a6%2B-cf288e3/bm-20250317-vultr-x86_64-python-cf288e3c250f5538aa63-3.14.0a6%2B-cf288e3-vs-3.13.0rc2.svg) |  |
| [2025-03-15](results/bm-20250315-3.14.0a6%2B-e82c2ca) | python/e82c2ca2a59235bc1965 | e82c2ca | 1.060x ↑<br>[📄](results/bm-20250315-3.14.0a6%2B-e82c2ca/bm-20250315-vultr-x86_64-python-e82c2ca2a59235bc1965-3.14.0a6%2B-e82c2ca-vs-3.12.6.md)[📈](results/bm-20250315-3.14.0a6%2B-e82c2ca/bm-20250315-vultr-x86_64-python-e82c2ca2a59235bc1965-3.14.0a6%2B-e82c2ca-vs-3.12.6.svg) | 1.021x ↑<br>[📄](results/bm-20250315-3.14.0a6%2B-e82c2ca/bm-20250315-vultr-x86_64-python-e82c2ca2a59235bc1965-3.14.0a6%2B-e82c2ca-vs-3.13.0rc2.md)[📈](results/bm-20250315-3.14.0a6%2B-e82c2ca/bm-20250315-vultr-x86_64-python-e82c2ca2a59235bc1965-3.14.0a6%2B-e82c2ca-vs-3.13.0rc2.svg) |  |
| [2025-03-15](results/bm-20250315-3.14.0a6%2B-e82c2ca-NOGIL) | python/e82c2ca2a59235bc1965 | e82c2ca (NOGIL) | 1.048x ↓<br>[📄](results/bm-20250315-3.14.0a6%2B-e82c2ca-NOGIL/bm-20250315-vultr-x86_64-python-e82c2ca2a59235bc1965-3.14.0a6%2B-e82c2ca-vs-3.12.6.md)[📈](results/bm-20250315-3.14.0a6%2B-e82c2ca-NOGIL/bm-20250315-vultr-x86_64-python-e82c2ca2a59235bc1965-3.14.0a6%2B-e82c2ca-vs-3.12.6.svg) | 1.079x ↓<br>[📄](results/bm-20250315-3.14.0a6%2B-e82c2ca-NOGIL/bm-20250315-vultr-x86_64-python-e82c2ca2a59235bc1965-3.14.0a6%2B-e82c2ca-vs-3.13.0rc2.md)[📈](results/bm-20250315-3.14.0a6%2B-e82c2ca-NOGIL/bm-20250315-vultr-x86_64-python-e82c2ca2a59235bc1965-3.14.0a6%2B-e82c2ca-vs-3.13.0rc2.svg) | 1.103x ↓<br>[📄](results/bm-20250315-3.14.0a6%2B-e82c2ca-NOGIL/bm-20250315-vultr-x86_64-python-e82c2ca2a59235bc1965-3.14.0a6%2B-e82c2ca-vs-base.md)[📈](results/bm-20250315-3.14.0a6%2B-e82c2ca-NOGIL/bm-20250315-vultr-x86_64-python-e82c2ca2a59235bc1965-3.14.0a6%2B-e82c2ca-vs-base.svg)[🧠](results/bm-20250315-3.14.0a6%2B-e82c2ca-NOGIL/bm-20250315-vultr-x86_64-python-e82c2ca2a59235bc1965-3.14.0a6%2B-e82c2ca-vs-base-mem.svg) |
| [2025-03-14](results/bm-20250314-3.14.0a6%2B-55815a6-NOGIL) | python/55815a6474c59001f023 | 55815a6 (NOGIL) | 1.046x ↓<br>[📄](results/bm-20250314-3.14.0a6%2B-55815a6-NOGIL/bm-20250314-vultr-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-3.12.6.md)[📈](results/bm-20250314-3.14.0a6%2B-55815a6-NOGIL/bm-20250314-vultr-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-3.12.6.svg) | 1.078x ↓<br>[📄](results/bm-20250314-3.14.0a6%2B-55815a6-NOGIL/bm-20250314-vultr-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-3.13.0rc2.md)[📈](results/bm-20250314-3.14.0a6%2B-55815a6-NOGIL/bm-20250314-vultr-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-3.13.0rc2.svg) | 1.106x ↓<br>[📄](results/bm-20250314-3.14.0a6%2B-55815a6-NOGIL/bm-20250314-vultr-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-base.md)[📈](results/bm-20250314-3.14.0a6%2B-55815a6-NOGIL/bm-20250314-vultr-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-base.svg)[🧠](results/bm-20250314-3.14.0a6%2B-55815a6-NOGIL/bm-20250314-vultr-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-base-mem.svg) |
| [2025-03-14](results/bm-20250314-3.14.0a6%2B-55815a6) | python/55815a6474c59001f023 | 55815a6 | 1.066x ↑<br>[📄](results/bm-20250314-3.14.0a6%2B-55815a6/bm-20250314-vultr-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-3.12.6.md)[📈](results/bm-20250314-3.14.0a6%2B-55815a6/bm-20250314-vultr-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-3.12.6.svg) | 1.027x ↑<br>[📄](results/bm-20250314-3.14.0a6%2B-55815a6/bm-20250314-vultr-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-3.13.0rc2.md)[📈](results/bm-20250314-3.14.0a6%2B-55815a6/bm-20250314-vultr-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-3.13.0rc2.svg) |  |
| [2025-03-15](results/bm-20250315-3.14.0a5%2B-5264e56-NOGIL) | mpage/measure_interp_loop_ | 5264e56 (NOGIL) | 1.035x ↓<br>[📄](results/bm-20250315-3.14.0a5%2B-5264e56-NOGIL/bm-20250315-vultr-x86_64-mpage-measure_interp_loop_-3.14.0a5%2B-5264e56-vs-3.12.6.md)[📈](results/bm-20250315-3.14.0a5%2B-5264e56-NOGIL/bm-20250315-vultr-x86_64-mpage-measure_interp_loop_-3.14.0a5%2B-5264e56-vs-3.12.6.svg) | 1.067x ↓<br>[📄](results/bm-20250315-3.14.0a5%2B-5264e56-NOGIL/bm-20250315-vultr-x86_64-mpage-measure_interp_loop_-3.14.0a5%2B-5264e56-vs-3.13.0rc2.md)[📈](results/bm-20250315-3.14.0a5%2B-5264e56-NOGIL/bm-20250315-vultr-x86_64-mpage-measure_interp_loop_-3.14.0a5%2B-5264e56-vs-3.13.0rc2.svg) | 1.015x ↑<br>[📄](results/bm-20250315-3.14.0a5%2B-5264e56-NOGIL/bm-20250315-vultr-x86_64-mpage-measure_interp_loop_-3.14.0a5%2B-5264e56-vs-base.md)[📈](results/bm-20250315-3.14.0a5%2B-5264e56-NOGIL/bm-20250315-vultr-x86_64-mpage-measure_interp_loop_-3.14.0a5%2B-5264e56-vs-base.svg)[🧠](results/bm-20250315-3.14.0a5%2B-5264e56-NOGIL/bm-20250315-vultr-x86_64-mpage-measure_interp_loop_-3.14.0a5%2B-5264e56-vs-base-mem.svg) |
| [2025-03-15](results/bm-20250315-3.14.0a5%2B-94fe18c-NOGIL) | mpage/measure_bc_atomics | 94fe18c (NOGIL) | 1.042x ↓<br>[📄](results/bm-20250315-3.14.0a5%2B-94fe18c-NOGIL/bm-20250315-vultr-x86_64-mpage-measure_bc_atomics-3.14.0a5%2B-94fe18c-vs-3.12.6.md)[📈](results/bm-20250315-3.14.0a5%2B-94fe18c-NOGIL/bm-20250315-vultr-x86_64-mpage-measure_bc_atomics-3.14.0a5%2B-94fe18c-vs-3.12.6.svg) | 1.074x ↓<br>[📄](results/bm-20250315-3.14.0a5%2B-94fe18c-NOGIL/bm-20250315-vultr-x86_64-mpage-measure_bc_atomics-3.14.0a5%2B-94fe18c-vs-3.13.0rc2.md)[📈](results/bm-20250315-3.14.0a5%2B-94fe18c-NOGIL/bm-20250315-vultr-x86_64-mpage-measure_bc_atomics-3.14.0a5%2B-94fe18c-vs-3.13.0rc2.svg) | 1.008x ↑<br>[📄](results/bm-20250315-3.14.0a5%2B-94fe18c-NOGIL/bm-20250315-vultr-x86_64-mpage-measure_bc_atomics-3.14.0a5%2B-94fe18c-vs-base.md)[📈](results/bm-20250315-3.14.0a5%2B-94fe18c-NOGIL/bm-20250315-vultr-x86_64-mpage-measure_bc_atomics-3.14.0a5%2B-94fe18c-vs-base.svg)[🧠](results/bm-20250315-3.14.0a5%2B-94fe18c-NOGIL/bm-20250315-vultr-x86_64-mpage-measure_bc_atomics-3.14.0a5%2B-94fe18c-vs-base-mem.svg) |
| [2025-03-14](results/bm-20250314-3.14.0a5%2B-76fc3d1) | mpage/measure_lfb | 76fc3d1 | 1.089x ↑<br>[📄](results/bm-20250314-3.14.0a5%2B-76fc3d1/bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5%2B-76fc3d1-vs-3.12.6.md)[📈](results/bm-20250314-3.14.0a5%2B-76fc3d1/bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5%2B-76fc3d1-vs-3.12.6.svg) | 1.050x ↑<br>[📄](results/bm-20250314-3.14.0a5%2B-76fc3d1/bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5%2B-76fc3d1-vs-3.13.0rc2.md)[📈](results/bm-20250314-3.14.0a5%2B-76fc3d1/bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5%2B-76fc3d1-vs-3.13.0rc2.svg) | 1.027x ↑<br>[📄](results/bm-20250314-3.14.0a5%2B-76fc3d1/bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5%2B-76fc3d1-vs-base.md)[📈](results/bm-20250314-3.14.0a5%2B-76fc3d1/bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5%2B-76fc3d1-vs-base.svg)[🧠](results/bm-20250314-3.14.0a5%2B-76fc3d1/bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5%2B-76fc3d1-vs-base-mem.svg) |
| [2025-03-13](results/bm-20250313-3.14.0a5%2B-1a8e574) | python/1a8e5742cdcf3dba7fc5 | 1a8e574 | 1.060x ↑<br>[📄](results/bm-20250313-3.14.0a5%2B-1a8e574/bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5%2B-1a8e574-vs-3.12.6.md)[📈](results/bm-20250313-3.14.0a5%2B-1a8e574/bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5%2B-1a8e574-vs-3.12.6.svg) | 1.021x ↑<br>[📄](results/bm-20250313-3.14.0a5%2B-1a8e574/bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5%2B-1a8e574-vs-3.13.0rc2.md)[📈](results/bm-20250313-3.14.0a5%2B-1a8e574/bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5%2B-1a8e574-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-03-18](results/bm-20250318-3.14.0a6%2B-49234c0) | python/49234c065cf2b1ea32c5 | 49234c0 | 1.059x ↑<br>[📄](results/bm-20250318-3.14.0a6%2B-49234c0/bm-20250318-macm4pro-arm64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-3.12.6.md)[📈](results/bm-20250318-3.14.0a6%2B-49234c0/bm-20250318-macm4pro-arm64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-3.12.6.svg) | 1.017x ↓<br>[📄](results/bm-20250318-3.14.0a6%2B-49234c0/bm-20250318-macm4pro-arm64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-3.13.0rc2.md)[📈](results/bm-20250318-3.14.0a6%2B-49234c0/bm-20250318-macm4pro-arm64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-3.13.0rc2.svg) |  |
| [2025-03-18](results/bm-20250318-3.14.0a6%2B-49234c0-NOGIL) | python/49234c065cf2b1ea32c5 | 49234c0 (NOGIL) | 1.030x ↓<br>[📄](results/bm-20250318-3.14.0a6%2B-49234c0-NOGIL/bm-20250318-macm4pro-arm64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-3.12.6.md)[📈](results/bm-20250318-3.14.0a6%2B-49234c0-NOGIL/bm-20250318-macm4pro-arm64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-3.12.6.svg) | 1.100x ↓<br>[📄](results/bm-20250318-3.14.0a6%2B-49234c0-NOGIL/bm-20250318-macm4pro-arm64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-3.13.0rc2.md)[📈](results/bm-20250318-3.14.0a6%2B-49234c0-NOGIL/bm-20250318-macm4pro-arm64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-3.13.0rc2.svg) | 1.084x ↓<br>[📄](results/bm-20250318-3.14.0a6%2B-49234c0-NOGIL/bm-20250318-macm4pro-arm64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-base.md)[📈](results/bm-20250318-3.14.0a6%2B-49234c0-NOGIL/bm-20250318-macm4pro-arm64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-base.svg)[🧠](results/bm-20250318-3.14.0a6%2B-49234c0-NOGIL/bm-20250318-macm4pro-arm64-python-49234c065cf2b1ea32c5-3.14.0a6%2B-49234c0-vs-base-mem.svg) |
| [2025-03-17](results/bm-20250317-3.14.0a6%2B-a936af9) | python/a936af924efc6e2fb59e | a936af9 | 1.075x ↑<br>[📄](results/bm-20250317-3.14.0a6%2B-a936af9/bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-3.12.6.md)[📈](results/bm-20250317-3.14.0a6%2B-a936af9/bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-3.12.6.svg) | 1.002x ↓<br>[📄](results/bm-20250317-3.14.0a6%2B-a936af9/bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-3.13.0rc2.md)[📈](results/bm-20250317-3.14.0a6%2B-a936af9/bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-3.13.0rc2.svg) |  |
| [2025-03-17](results/bm-20250317-3.14.0a6%2B-a936af9-NOGIL) | python/a936af924efc6e2fb59e | a936af9 (NOGIL) | 1.009x ↓<br>[📄](results/bm-20250317-3.14.0a6%2B-a936af9-NOGIL/bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-3.12.6.md)[📈](results/bm-20250317-3.14.0a6%2B-a936af9-NOGIL/bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-3.12.6.svg) | 1.081x ↓<br>[📄](results/bm-20250317-3.14.0a6%2B-a936af9-NOGIL/bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-3.13.0rc2.md)[📈](results/bm-20250317-3.14.0a6%2B-a936af9-NOGIL/bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-3.13.0rc2.svg) | 1.080x ↓<br>[📄](results/bm-20250317-3.14.0a6%2B-a936af9-NOGIL/bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-base.md)[📈](results/bm-20250317-3.14.0a6%2B-a936af9-NOGIL/bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-base.svg)[🧠](results/bm-20250317-3.14.0a6%2B-a936af9-NOGIL/bm-20250317-macm4pro-arm64-python-a936af924efc6e2fb59e-3.14.0a6%2B-a936af9-vs-base-mem.svg) |
| [2025-03-14](results/bm-20250314-3.14.0a6-77b2c93) | python/v3.14.0a6 | 77b2c93 | 1.063x ↑<br>[📄](results/bm-20250314-3.14.0a6-77b2c93/bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93-vs-3.12.6.md)[📈](results/bm-20250314-3.14.0a6-77b2c93/bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93-vs-3.12.6.svg) | 1.014x ↓<br>[📄](results/bm-20250314-3.14.0a6-77b2c93/bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93-vs-3.13.0rc2.md)[📈](results/bm-20250314-3.14.0a6-77b2c93/bm-20250314-macm4pro-arm64-python-v3.14.0a6-3.14.0a6-77b2c93-vs-3.13.0rc2.svg) |  |
| [2025-02-11](results/bm-20250211-3.14.0a5-3ae9101) | python/v3.14.0a5 | 3ae9101 | 1.092x ↑<br>[📄](results/bm-20250211-3.14.0a5-3ae9101/bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101-vs-3.12.6.md)[📈](results/bm-20250211-3.14.0a5-3ae9101/bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101-vs-3.12.6.svg) | 1.014x ↑<br>[📄](results/bm-20250211-3.14.0a5-3ae9101/bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101-vs-3.13.0rc2.md)[📈](results/bm-20250211-3.14.0a5-3ae9101/bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101-vs-3.13.0rc2.svg) |  |
| [2025-02-11](results/bm-20250211-3.14.0a5-3ae9101-NOGIL) | python/v3.14.0a5 | 3ae9101 (NOGIL) | 1.010x ↓<br>[📄](results/bm-20250211-3.14.0a5-3ae9101-NOGIL/bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101-vs-3.12.6.md)[📈](results/bm-20250211-3.14.0a5-3ae9101-NOGIL/bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101-vs-3.12.6.svg) | 1.081x ↓<br>[📄](results/bm-20250211-3.14.0a5-3ae9101-NOGIL/bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101-vs-3.13.0rc2.md)[📈](results/bm-20250211-3.14.0a5-3ae9101-NOGIL/bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101-vs-3.13.0rc2.svg) | 1.094x ↓<br>[📄](results/bm-20250211-3.14.0a5-3ae9101-NOGIL/bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101-vs-base.md)[📈](results/bm-20250211-3.14.0a5-3ae9101-NOGIL/bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101-vs-base.svg)[🧠](results/bm-20250211-3.14.0a5-3ae9101-NOGIL/bm-20250211-macm4pro-arm64-python-v3.14.0a5-3.14.0a5-3ae9101-vs-base-mem.svg) |
| [2024-09-06](results/bm-20240906-3.13.0rc2-ec61006-NOGIL) | python/v3.13.0rc2 | ec61006 (NOGIL) | 1.208x ↓<br>[📄](results/bm-20240906-3.13.0rc2-ec61006-NOGIL/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006-vs-3.12.6.md)[📈](results/bm-20240906-3.13.0rc2-ec61006-NOGIL/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006-vs-3.12.6.svg) | 1.265x ↓<br>[📄](results/bm-20240906-3.13.0rc2-ec61006-NOGIL/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006-vs-3.13.0rc2.md)[📈](results/bm-20240906-3.13.0rc2-ec61006-NOGIL/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006-vs-3.13.0rc2.svg) | 1.265x ↓<br>[📄](results/bm-20240906-3.13.0rc2-ec61006-NOGIL/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006-vs-base.md)[📈](results/bm-20240906-3.13.0rc2-ec61006-NOGIL/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006-vs-base.svg)[🧠](results/bm-20240906-3.13.0rc2-ec61006-NOGIL/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006-vs-base-mem.svg) |
| [2024-09-06](results/bm-20240906-3.13.0rc2-ec61006) | python/v3.13.0rc2 | ec61006 | 1.077x ↑<br>[📄](results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006-vs-3.12.6.md)[📈](results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006-vs-3.12.6.svg) |  |  |
| [2024-09-06](results/bm-20240906-3.12.6-a4a2d2b) | python/v3.12.6 | a4a2d2b |  | 1.071x ↓<br>[📄](results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b-vs-3.13.0rc2.md)[📈](results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b-vs-3.13.0rc2.svg) |  |


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
