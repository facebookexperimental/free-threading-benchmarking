# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (b14986c)](results/bm-20250621-3.15.0a0-b14986c/bm-20250621-vultr-x86_64-python-b14986c91464b06e9016-3.15.0a0-b14986c-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (b14986c)](results/bm-20250621-3.15.0a0-b14986c-PYTHON_UOPS/bm-20250621-vultr-x86_64-python-b14986c91464b06e9016-3.15.0a0-b14986c-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-06-28](results/bm-20250628-3.15.0a0-c419af9-NOGIL) | python/c419af9e277bea7dd78f | c419af9 (NOGIL) | 1.023x ↑<br>[📄](results/bm-20250628-3.15.0a0-c419af9-NOGIL/bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9-vs-3.12.6.md)[📈](results/bm-20250628-3.15.0a0-c419af9-NOGIL/bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9-vs-3.12.6.svg) | 1.012x ↓<br>[📄](results/bm-20250628-3.15.0a0-c419af9-NOGIL/bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9-vs-3.13.0rc2.md)[📈](results/bm-20250628-3.15.0a0-c419af9-NOGIL/bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9-vs-3.13.0rc2.svg) | 1.086x ↓<br>[📄](results/bm-20250628-3.15.0a0-c419af9-NOGIL/bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9-vs-base.md)[📈](results/bm-20250628-3.15.0a0-c419af9-NOGIL/bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9-vs-base.svg)[🧠](results/bm-20250628-3.15.0a0-c419af9-NOGIL/bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9-vs-base-mem.svg) |
| [2025-06-28](results/bm-20250628-3.15.0a0-c419af9) | python/c419af9e277bea7dd78f | c419af9 | 1.112x ↑<br>[📄](results/bm-20250628-3.15.0a0-c419af9/bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9-vs-3.12.6.md)[📈](results/bm-20250628-3.15.0a0-c419af9/bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9-vs-3.12.6.svg) | 1.075x ↑<br>[📄](results/bm-20250628-3.15.0a0-c419af9/bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9-vs-3.13.0rc2.md)[📈](results/bm-20250628-3.15.0a0-c419af9/bm-20250628-vultr-x86_64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9-vs-3.13.0rc2.svg) |  |
| [2025-06-26](results/bm-20250626-3.15.0a0-34ce192-NOGIL) | python/34ce1920ca33c11ca2c3 | 34ce192 (NOGIL) | 1.019x ↑<br>[📄](results/bm-20250626-3.15.0a0-34ce192-NOGIL/bm-20250626-vultr-x86_64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192-vs-3.12.6.md)[📈](results/bm-20250626-3.15.0a0-34ce192-NOGIL/bm-20250626-vultr-x86_64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192-vs-3.12.6.svg) | 1.015x ↓<br>[📄](results/bm-20250626-3.15.0a0-34ce192-NOGIL/bm-20250626-vultr-x86_64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192-vs-3.13.0rc2.md)[📈](results/bm-20250626-3.15.0a0-34ce192-NOGIL/bm-20250626-vultr-x86_64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192-vs-3.13.0rc2.svg) | 1.083x ↓<br>[📄](results/bm-20250626-3.15.0a0-34ce192-NOGIL/bm-20250626-vultr-x86_64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192-vs-base.md)[📈](results/bm-20250626-3.15.0a0-34ce192-NOGIL/bm-20250626-vultr-x86_64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192-vs-base.svg)[🧠](results/bm-20250626-3.15.0a0-34ce192-NOGIL/bm-20250626-vultr-x86_64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192-vs-base-mem.svg) |
| [2025-06-26](results/bm-20250626-3.15.0a0-34ce192) | python/34ce1920ca33c11ca2c3 | 34ce192 | 1.104x ↑<br>[📄](results/bm-20250626-3.15.0a0-34ce192/bm-20250626-vultr-x86_64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192-vs-3.12.6.md)[📈](results/bm-20250626-3.15.0a0-34ce192/bm-20250626-vultr-x86_64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192-vs-3.12.6.svg) | 1.067x ↑<br>[📄](results/bm-20250626-3.15.0a0-34ce192/bm-20250626-vultr-x86_64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192-vs-3.13.0rc2.md)[📈](results/bm-20250626-3.15.0a0-34ce192/bm-20250626-vultr-x86_64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192-vs-3.13.0rc2.svg) |  |
| [2025-06-25](results/bm-20250625-3.15.0a0-6227662-NOGIL) | python/6227662ff3bf838d31e9 | 6227662 (NOGIL) | 1.013x ↑<br>[📄](results/bm-20250625-3.15.0a0-6227662-NOGIL/bm-20250625-vultr-x86_64-python-6227662ff3bf838d31e9-3.15.0a0-6227662-vs-3.12.6.md)[📈](results/bm-20250625-3.15.0a0-6227662-NOGIL/bm-20250625-vultr-x86_64-python-6227662ff3bf838d31e9-3.15.0a0-6227662-vs-3.12.6.svg) | 1.021x ↓<br>[📄](results/bm-20250625-3.15.0a0-6227662-NOGIL/bm-20250625-vultr-x86_64-python-6227662ff3bf838d31e9-3.15.0a0-6227662-vs-3.13.0rc2.md)[📈](results/bm-20250625-3.15.0a0-6227662-NOGIL/bm-20250625-vultr-x86_64-python-6227662ff3bf838d31e9-3.15.0a0-6227662-vs-3.13.0rc2.svg) | 1.095x ↓<br>[📄](results/bm-20250625-3.15.0a0-6227662-NOGIL/bm-20250625-vultr-x86_64-python-6227662ff3bf838d31e9-3.15.0a0-6227662-vs-base.md)[📈](results/bm-20250625-3.15.0a0-6227662-NOGIL/bm-20250625-vultr-x86_64-python-6227662ff3bf838d31e9-3.15.0a0-6227662-vs-base.svg)[🧠](results/bm-20250625-3.15.0a0-6227662-NOGIL/bm-20250625-vultr-x86_64-python-6227662ff3bf838d31e9-3.15.0a0-6227662-vs-base-mem.svg) |
| [2025-06-25](results/bm-20250625-3.15.0a0-6227662) | python/6227662ff3bf838d31e9 | 6227662 | 1.114x ↑<br>[📄](results/bm-20250625-3.15.0a0-6227662/bm-20250625-vultr-x86_64-python-6227662ff3bf838d31e9-3.15.0a0-6227662-vs-3.12.6.md)[📈](results/bm-20250625-3.15.0a0-6227662/bm-20250625-vultr-x86_64-python-6227662ff3bf838d31e9-3.15.0a0-6227662-vs-3.12.6.svg) | 1.077x ↑<br>[📄](results/bm-20250625-3.15.0a0-6227662/bm-20250625-vultr-x86_64-python-6227662ff3bf838d31e9-3.15.0a0-6227662-vs-3.13.0rc2.md)[📈](results/bm-20250625-3.15.0a0-6227662/bm-20250625-vultr-x86_64-python-6227662ff3bf838d31e9-3.15.0a0-6227662-vs-3.13.0rc2.svg) |  |
| [2025-06-24](results/bm-20250624-3.15.0a0-ee0e22c-NOGIL) | python/ee0e22c088ce5483d4ba | ee0e22c (NOGIL) | 1.015x ↑<br>[📄](results/bm-20250624-3.15.0a0-ee0e22c-NOGIL/bm-20250624-vultr-x86_64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c-vs-3.12.6.md)[📈](results/bm-20250624-3.15.0a0-ee0e22c-NOGIL/bm-20250624-vultr-x86_64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c-vs-3.12.6.svg) | 1.020x ↓<br>[📄](results/bm-20250624-3.15.0a0-ee0e22c-NOGIL/bm-20250624-vultr-x86_64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c-vs-3.13.0rc2.md)[📈](results/bm-20250624-3.15.0a0-ee0e22c-NOGIL/bm-20250624-vultr-x86_64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c-vs-3.13.0rc2.svg) | 1.085x ↓<br>[📄](results/bm-20250624-3.15.0a0-ee0e22c-NOGIL/bm-20250624-vultr-x86_64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c-vs-base.md)[📈](results/bm-20250624-3.15.0a0-ee0e22c-NOGIL/bm-20250624-vultr-x86_64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c-vs-base.svg)[🧠](results/bm-20250624-3.15.0a0-ee0e22c-NOGIL/bm-20250624-vultr-x86_64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c-vs-base-mem.svg) |
| [2025-06-24](results/bm-20250624-3.15.0a0-ee0e22c) | python/ee0e22c088ce5483d4ba | ee0e22c | 1.102x ↑<br>[📄](results/bm-20250624-3.15.0a0-ee0e22c/bm-20250624-vultr-x86_64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c-vs-3.12.6.md)[📈](results/bm-20250624-3.15.0a0-ee0e22c/bm-20250624-vultr-x86_64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c-vs-3.12.6.svg) | 1.065x ↑<br>[📄](results/bm-20250624-3.15.0a0-ee0e22c/bm-20250624-vultr-x86_64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c-vs-3.13.0rc2.md)[📈](results/bm-20250624-3.15.0a0-ee0e22c/bm-20250624-vultr-x86_64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-06-28](results/bm-20250628-3.15.0a0-c419af9-NOGIL) | python/c419af9e277bea7dd78f | c419af9 (NOGIL) | 1.096x ↑<br>[📄](results/bm-20250628-3.15.0a0-c419af9-NOGIL/bm-20250628-macm4pro-arm64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9-vs-3.12.6.md)[📈](results/bm-20250628-3.15.0a0-c419af9-NOGIL/bm-20250628-macm4pro-arm64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9-vs-3.12.6.svg) | 1.017x ↑<br>[📄](results/bm-20250628-3.15.0a0-c419af9-NOGIL/bm-20250628-macm4pro-arm64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9-vs-3.13.0rc2.md)[📈](results/bm-20250628-3.15.0a0-c419af9-NOGIL/bm-20250628-macm4pro-arm64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9-vs-3.13.0rc2.svg) | 1.004x ↑<br>[📄](results/bm-20250628-3.15.0a0-c419af9-NOGIL/bm-20250628-macm4pro-arm64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9-vs-base.md)[📈](results/bm-20250628-3.15.0a0-c419af9-NOGIL/bm-20250628-macm4pro-arm64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9-vs-base.svg)[🧠](results/bm-20250628-3.15.0a0-c419af9-NOGIL/bm-20250628-macm4pro-arm64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9-vs-base-mem.svg) |
| [2025-06-28](results/bm-20250628-3.15.0a0-c419af9) | python/c419af9e277bea7dd78f | c419af9 | 1.091x ↑<br>[📄](results/bm-20250628-3.15.0a0-c419af9/bm-20250628-macm4pro-arm64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9-vs-3.12.6.md)[📈](results/bm-20250628-3.15.0a0-c419af9/bm-20250628-macm4pro-arm64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9-vs-3.12.6.svg) | 1.012x ↑<br>[📄](results/bm-20250628-3.15.0a0-c419af9/bm-20250628-macm4pro-arm64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9-vs-3.13.0rc2.md)[📈](results/bm-20250628-3.15.0a0-c419af9/bm-20250628-macm4pro-arm64-python-c419af9e277bea7dd78f-3.15.0a0-c419af9-vs-3.13.0rc2.svg) |  |
| [2025-06-26](results/bm-20250626-3.15.0a0-34ce192-NOGIL) | python/34ce1920ca33c11ca2c3 | 34ce192 (NOGIL) | 1.100x ↑<br>[📄](results/bm-20250626-3.15.0a0-34ce192-NOGIL/bm-20250626-macm4pro-arm64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192-vs-3.12.6.md)[📈](results/bm-20250626-3.15.0a0-34ce192-NOGIL/bm-20250626-macm4pro-arm64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192-vs-3.12.6.svg) | 1.021x ↑<br>[📄](results/bm-20250626-3.15.0a0-34ce192-NOGIL/bm-20250626-macm4pro-arm64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192-vs-3.13.0rc2.md)[📈](results/bm-20250626-3.15.0a0-34ce192-NOGIL/bm-20250626-macm4pro-arm64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192-vs-3.13.0rc2.svg) | 1.003x ↑<br>[📄](results/bm-20250626-3.15.0a0-34ce192-NOGIL/bm-20250626-macm4pro-arm64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192-vs-base.md)[📈](results/bm-20250626-3.15.0a0-34ce192-NOGIL/bm-20250626-macm4pro-arm64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192-vs-base.svg)[🧠](results/bm-20250626-3.15.0a0-34ce192-NOGIL/bm-20250626-macm4pro-arm64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192-vs-base-mem.svg) |
| [2025-06-26](results/bm-20250626-3.15.0a0-34ce192) | python/34ce1920ca33c11ca2c3 | 34ce192 | 1.096x ↑<br>[📄](results/bm-20250626-3.15.0a0-34ce192/bm-20250626-macm4pro-arm64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192-vs-3.12.6.md)[📈](results/bm-20250626-3.15.0a0-34ce192/bm-20250626-macm4pro-arm64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192-vs-3.12.6.svg) | 1.017x ↑<br>[📄](results/bm-20250626-3.15.0a0-34ce192/bm-20250626-macm4pro-arm64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192-vs-3.13.0rc2.md)[📈](results/bm-20250626-3.15.0a0-34ce192/bm-20250626-macm4pro-arm64-python-34ce1920ca33c11ca2c3-3.15.0a0-34ce192-vs-3.13.0rc2.svg) |  |
| [2025-06-25](results/bm-20250625-3.15.0a0-6227662-NOGIL) | python/6227662ff3bf838d31e9 | 6227662 (NOGIL) | 1.094x ↑<br>[📄](results/bm-20250625-3.15.0a0-6227662-NOGIL/bm-20250625-macm4pro-arm64-python-6227662ff3bf838d31e9-3.15.0a0-6227662-vs-3.12.6.md)[📈](results/bm-20250625-3.15.0a0-6227662-NOGIL/bm-20250625-macm4pro-arm64-python-6227662ff3bf838d31e9-3.15.0a0-6227662-vs-3.12.6.svg) | 1.014x ↑<br>[📄](results/bm-20250625-3.15.0a0-6227662-NOGIL/bm-20250625-macm4pro-arm64-python-6227662ff3bf838d31e9-3.15.0a0-6227662-vs-3.13.0rc2.md)[📈](results/bm-20250625-3.15.0a0-6227662-NOGIL/bm-20250625-macm4pro-arm64-python-6227662ff3bf838d31e9-3.15.0a0-6227662-vs-3.13.0rc2.svg) | 1.007x ↑<br>[📄](results/bm-20250625-3.15.0a0-6227662-NOGIL/bm-20250625-macm4pro-arm64-python-6227662ff3bf838d31e9-3.15.0a0-6227662-vs-base.md)[📈](results/bm-20250625-3.15.0a0-6227662-NOGIL/bm-20250625-macm4pro-arm64-python-6227662ff3bf838d31e9-3.15.0a0-6227662-vs-base.svg)[🧠](results/bm-20250625-3.15.0a0-6227662-NOGIL/bm-20250625-macm4pro-arm64-python-6227662ff3bf838d31e9-3.15.0a0-6227662-vs-base-mem.svg) |
| [2025-06-25](results/bm-20250625-3.15.0a0-6227662) | python/6227662ff3bf838d31e9 | 6227662 | 1.085x ↑<br>[📄](results/bm-20250625-3.15.0a0-6227662/bm-20250625-macm4pro-arm64-python-6227662ff3bf838d31e9-3.15.0a0-6227662-vs-3.12.6.md)[📈](results/bm-20250625-3.15.0a0-6227662/bm-20250625-macm4pro-arm64-python-6227662ff3bf838d31e9-3.15.0a0-6227662-vs-3.12.6.svg) | 1.007x ↑<br>[📄](results/bm-20250625-3.15.0a0-6227662/bm-20250625-macm4pro-arm64-python-6227662ff3bf838d31e9-3.15.0a0-6227662-vs-3.13.0rc2.md)[📈](results/bm-20250625-3.15.0a0-6227662/bm-20250625-macm4pro-arm64-python-6227662ff3bf838d31e9-3.15.0a0-6227662-vs-3.13.0rc2.svg) |  |
| [2025-06-24](results/bm-20250624-3.15.0a0-ee0e22c-NOGIL) | python/ee0e22c088ce5483d4ba | ee0e22c (NOGIL) | 1.100x ↑<br>[📄](results/bm-20250624-3.15.0a0-ee0e22c-NOGIL/bm-20250624-macm4pro-arm64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c-vs-3.12.6.md)[📈](results/bm-20250624-3.15.0a0-ee0e22c-NOGIL/bm-20250624-macm4pro-arm64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c-vs-3.12.6.svg) | 1.020x ↑<br>[📄](results/bm-20250624-3.15.0a0-ee0e22c-NOGIL/bm-20250624-macm4pro-arm64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c-vs-3.13.0rc2.md)[📈](results/bm-20250624-3.15.0a0-ee0e22c-NOGIL/bm-20250624-macm4pro-arm64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c-vs-3.13.0rc2.svg) | 1.001x ↑<br>[📄](results/bm-20250624-3.15.0a0-ee0e22c-NOGIL/bm-20250624-macm4pro-arm64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c-vs-base.md)[📈](results/bm-20250624-3.15.0a0-ee0e22c-NOGIL/bm-20250624-macm4pro-arm64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c-vs-base.svg)[🧠](results/bm-20250624-3.15.0a0-ee0e22c-NOGIL/bm-20250624-macm4pro-arm64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c-vs-base-mem.svg) |
| [2025-06-24](results/bm-20250624-3.15.0a0-ee0e22c) | python/ee0e22c088ce5483d4ba | ee0e22c | 1.098x ↑<br>[📄](results/bm-20250624-3.15.0a0-ee0e22c/bm-20250624-macm4pro-arm64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c-vs-3.12.6.md)[📈](results/bm-20250624-3.15.0a0-ee0e22c/bm-20250624-macm4pro-arm64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c-vs-3.12.6.svg) | 1.019x ↑<br>[📄](results/bm-20250624-3.15.0a0-ee0e22c/bm-20250624-macm4pro-arm64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c-vs-3.13.0rc2.md)[📈](results/bm-20250624-3.15.0a0-ee0e22c/bm-20250624-macm4pro-arm64-python-ee0e22c088ce5483d4ba-3.15.0a0-ee0e22c-vs-3.13.0rc2.svg) |  |


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
