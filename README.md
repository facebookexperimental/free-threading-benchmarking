# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (ccbe41e)](results/bm-20260130-3.15.0a5%2B-ccbe41e/bm-20260130-vultr-x86_64-python-ccbe41e27cdb44103318-3.15.0a5%2B-ccbe41e-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (ccbe41e)](results/bm-20260130-3.15.0a5%2B-ccbe41e-PYTHON_UOPS/bm-20260130-vultr-x86_64-python-ccbe41e27cdb44103318-3.15.0a5%2B-ccbe41e-pystats.md)
- [Most recent JIT pystats on main (bedaea0)](results/bm-20251019-3.15.0a1%2B-bedaea0-JIT/bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-02-06](results/bm-20260206-3.15.0a5%2B-74db440-NOGIL) | python/74db4404eaa9b4448b50 | 74db440 (NOGIL) | 1.023x ↓<br>[📄](results/bm-20260206-3.15.0a5%2B-74db440-NOGIL/bm-20260206-vultr-x86_64-python-74db4404eaa9b4448b50-3.15.0a5%2B-74db440-vs-3.12.6.md)[📈](results/bm-20260206-3.15.0a5%2B-74db440-NOGIL/bm-20260206-vultr-x86_64-python-74db4404eaa9b4448b50-3.15.0a5%2B-74db440-vs-3.12.6.svg) | 1.056x ↓<br>[📄](results/bm-20260206-3.15.0a5%2B-74db440-NOGIL/bm-20260206-vultr-x86_64-python-74db4404eaa9b4448b50-3.15.0a5%2B-74db440-vs-3.13.0rc2.md)[📈](results/bm-20260206-3.15.0a5%2B-74db440-NOGIL/bm-20260206-vultr-x86_64-python-74db4404eaa9b4448b50-3.15.0a5%2B-74db440-vs-3.13.0rc2.svg) | 1.096x ↓<br>[📄](results/bm-20260206-3.15.0a5%2B-74db440-NOGIL/bm-20260206-vultr-x86_64-python-74db4404eaa9b4448b50-3.15.0a5%2B-74db440-vs-base.md)[📈](results/bm-20260206-3.15.0a5%2B-74db440-NOGIL/bm-20260206-vultr-x86_64-python-74db4404eaa9b4448b50-3.15.0a5%2B-74db440-vs-base.svg)[🧠](results/bm-20260206-3.15.0a5%2B-74db440-NOGIL/bm-20260206-vultr-x86_64-python-74db4404eaa9b4448b50-3.15.0a5%2B-74db440-vs-base-mem.svg) |
| [2026-02-06](results/bm-20260206-3.15.0a5%2B-74db440) | python/74db4404eaa9b4448b50 | 74db440 | 1.076x ↑<br>[📄](results/bm-20260206-3.15.0a5%2B-74db440/bm-20260206-vultr-x86_64-python-74db4404eaa9b4448b50-3.15.0a5%2B-74db440-vs-3.12.6.md)[📈](results/bm-20260206-3.15.0a5%2B-74db440/bm-20260206-vultr-x86_64-python-74db4404eaa9b4448b50-3.15.0a5%2B-74db440-vs-3.12.6.svg) | 1.040x ↑<br>[📄](results/bm-20260206-3.15.0a5%2B-74db440/bm-20260206-vultr-x86_64-python-74db4404eaa9b4448b50-3.15.0a5%2B-74db440-vs-3.13.0rc2.md)[📈](results/bm-20260206-3.15.0a5%2B-74db440/bm-20260206-vultr-x86_64-python-74db4404eaa9b4448b50-3.15.0a5%2B-74db440-vs-3.13.0rc2.svg) |  |
| [2026-02-05](results/bm-20260205-3.15.0a5%2B-957f9fe-NOGIL) | python/957f9fe162398fceeaa9 | 957f9fe (NOGIL) | 1.029x ↓<br>[📄](results/bm-20260205-3.15.0a5%2B-957f9fe-NOGIL/bm-20260205-vultr-x86_64-python-957f9fe162398fceeaa9-3.15.0a5%2B-957f9fe-vs-3.12.6.md)[📈](results/bm-20260205-3.15.0a5%2B-957f9fe-NOGIL/bm-20260205-vultr-x86_64-python-957f9fe162398fceeaa9-3.15.0a5%2B-957f9fe-vs-3.12.6.svg) | 1.062x ↓<br>[📄](results/bm-20260205-3.15.0a5%2B-957f9fe-NOGIL/bm-20260205-vultr-x86_64-python-957f9fe162398fceeaa9-3.15.0a5%2B-957f9fe-vs-3.13.0rc2.md)[📈](results/bm-20260205-3.15.0a5%2B-957f9fe-NOGIL/bm-20260205-vultr-x86_64-python-957f9fe162398fceeaa9-3.15.0a5%2B-957f9fe-vs-3.13.0rc2.svg) | 1.103x ↓<br>[📄](results/bm-20260205-3.15.0a5%2B-957f9fe-NOGIL/bm-20260205-vultr-x86_64-python-957f9fe162398fceeaa9-3.15.0a5%2B-957f9fe-vs-base.md)[📈](results/bm-20260205-3.15.0a5%2B-957f9fe-NOGIL/bm-20260205-vultr-x86_64-python-957f9fe162398fceeaa9-3.15.0a5%2B-957f9fe-vs-base.svg)[🧠](results/bm-20260205-3.15.0a5%2B-957f9fe-NOGIL/bm-20260205-vultr-x86_64-python-957f9fe162398fceeaa9-3.15.0a5%2B-957f9fe-vs-base-mem.svg) |
| [2026-02-05](results/bm-20260205-3.15.0a5%2B-957f9fe) | python/957f9fe162398fceeaa9 | 957f9fe | 1.077x ↑<br>[📄](results/bm-20260205-3.15.0a5%2B-957f9fe/bm-20260205-vultr-x86_64-python-957f9fe162398fceeaa9-3.15.0a5%2B-957f9fe-vs-3.12.6.md)[📈](results/bm-20260205-3.15.0a5%2B-957f9fe/bm-20260205-vultr-x86_64-python-957f9fe162398fceeaa9-3.15.0a5%2B-957f9fe-vs-3.12.6.svg) | 1.041x ↑<br>[📄](results/bm-20260205-3.15.0a5%2B-957f9fe/bm-20260205-vultr-x86_64-python-957f9fe162398fceeaa9-3.15.0a5%2B-957f9fe-vs-3.13.0rc2.md)[📈](results/bm-20260205-3.15.0a5%2B-957f9fe/bm-20260205-vultr-x86_64-python-957f9fe162398fceeaa9-3.15.0a5%2B-957f9fe-vs-3.13.0rc2.svg) |  |
| [2026-02-04](results/bm-20260204-3.15.0a5%2B-b6d8aa4-NOGIL) | python/b6d8aa436b0108fcc90c | b6d8aa4 (NOGIL) | 1.029x ↓<br>[📄](results/bm-20260204-3.15.0a5%2B-b6d8aa4-NOGIL/bm-20260204-vultr-x86_64-python-b6d8aa436b0108fcc90c-3.15.0a5%2B-b6d8aa4-vs-3.12.6.md)[📈](results/bm-20260204-3.15.0a5%2B-b6d8aa4-NOGIL/bm-20260204-vultr-x86_64-python-b6d8aa436b0108fcc90c-3.15.0a5%2B-b6d8aa4-vs-3.12.6.svg) | 1.062x ↓<br>[📄](results/bm-20260204-3.15.0a5%2B-b6d8aa4-NOGIL/bm-20260204-vultr-x86_64-python-b6d8aa436b0108fcc90c-3.15.0a5%2B-b6d8aa4-vs-3.13.0rc2.md)[📈](results/bm-20260204-3.15.0a5%2B-b6d8aa4-NOGIL/bm-20260204-vultr-x86_64-python-b6d8aa436b0108fcc90c-3.15.0a5%2B-b6d8aa4-vs-3.13.0rc2.svg) | 1.107x ↓<br>[📄](results/bm-20260204-3.15.0a5%2B-b6d8aa4-NOGIL/bm-20260204-vultr-x86_64-python-b6d8aa436b0108fcc90c-3.15.0a5%2B-b6d8aa4-vs-base.md)[📈](results/bm-20260204-3.15.0a5%2B-b6d8aa4-NOGIL/bm-20260204-vultr-x86_64-python-b6d8aa436b0108fcc90c-3.15.0a5%2B-b6d8aa4-vs-base.svg)[🧠](results/bm-20260204-3.15.0a5%2B-b6d8aa4-NOGIL/bm-20260204-vultr-x86_64-python-b6d8aa436b0108fcc90c-3.15.0a5%2B-b6d8aa4-vs-base-mem.svg) |
| [2026-02-04](results/bm-20260204-3.15.0a5%2B-b6d8aa4) | python/b6d8aa436b0108fcc90c | b6d8aa4 | 1.083x ↑<br>[📄](results/bm-20260204-3.15.0a5%2B-b6d8aa4/bm-20260204-vultr-x86_64-python-b6d8aa436b0108fcc90c-3.15.0a5%2B-b6d8aa4-vs-3.12.6.md)[📈](results/bm-20260204-3.15.0a5%2B-b6d8aa4/bm-20260204-vultr-x86_64-python-b6d8aa436b0108fcc90c-3.15.0a5%2B-b6d8aa4-vs-3.12.6.svg) | 1.047x ↑<br>[📄](results/bm-20260204-3.15.0a5%2B-b6d8aa4/bm-20260204-vultr-x86_64-python-b6d8aa436b0108fcc90c-3.15.0a5%2B-b6d8aa4-vs-3.13.0rc2.md)[📈](results/bm-20260204-3.15.0a5%2B-b6d8aa4/bm-20260204-vultr-x86_64-python-b6d8aa436b0108fcc90c-3.15.0a5%2B-b6d8aa4-vs-3.13.0rc2.svg) |  |
| [2026-02-03](results/bm-20260203-3.15.0a5%2B-9d0c743-NOGIL) | python/9d0c7432ea40ab3f73af | 9d0c743 (NOGIL) | 1.026x ↓<br>[📄](results/bm-20260203-3.15.0a5%2B-9d0c743-NOGIL/bm-20260203-vultr-x86_64-python-9d0c7432ea40ab3f73af-3.15.0a5%2B-9d0c743-vs-3.12.6.md)[📈](results/bm-20260203-3.15.0a5%2B-9d0c743-NOGIL/bm-20260203-vultr-x86_64-python-9d0c7432ea40ab3f73af-3.15.0a5%2B-9d0c743-vs-3.12.6.svg) | 1.059x ↓<br>[📄](results/bm-20260203-3.15.0a5%2B-9d0c743-NOGIL/bm-20260203-vultr-x86_64-python-9d0c7432ea40ab3f73af-3.15.0a5%2B-9d0c743-vs-3.13.0rc2.md)[📈](results/bm-20260203-3.15.0a5%2B-9d0c743-NOGIL/bm-20260203-vultr-x86_64-python-9d0c7432ea40ab3f73af-3.15.0a5%2B-9d0c743-vs-3.13.0rc2.svg) | 1.105x ↓<br>[📄](results/bm-20260203-3.15.0a5%2B-9d0c743-NOGIL/bm-20260203-vultr-x86_64-python-9d0c7432ea40ab3f73af-3.15.0a5%2B-9d0c743-vs-base.md)[📈](results/bm-20260203-3.15.0a5%2B-9d0c743-NOGIL/bm-20260203-vultr-x86_64-python-9d0c7432ea40ab3f73af-3.15.0a5%2B-9d0c743-vs-base.svg)[🧠](results/bm-20260203-3.15.0a5%2B-9d0c743-NOGIL/bm-20260203-vultr-x86_64-python-9d0c7432ea40ab3f73af-3.15.0a5%2B-9d0c743-vs-base-mem.svg) |
| [2026-02-03](results/bm-20260203-3.15.0a5%2B-9d0c743) | python/9d0c7432ea40ab3f73af | 9d0c743 | 1.083x ↑<br>[📄](results/bm-20260203-3.15.0a5%2B-9d0c743/bm-20260203-vultr-x86_64-python-9d0c7432ea40ab3f73af-3.15.0a5%2B-9d0c743-vs-3.12.6.md)[📈](results/bm-20260203-3.15.0a5%2B-9d0c743/bm-20260203-vultr-x86_64-python-9d0c7432ea40ab3f73af-3.15.0a5%2B-9d0c743-vs-3.12.6.svg) | 1.046x ↑<br>[📄](results/bm-20260203-3.15.0a5%2B-9d0c743/bm-20260203-vultr-x86_64-python-9d0c7432ea40ab3f73af-3.15.0a5%2B-9d0c743-vs-3.13.0rc2.md)[📈](results/bm-20260203-3.15.0a5%2B-9d0c743/bm-20260203-vultr-x86_64-python-9d0c7432ea40ab3f73af-3.15.0a5%2B-9d0c743-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-02-06](results/bm-20260206-3.15.0a5%2B-74db440-NOGIL) | python/74db4404eaa9b4448b50 | 74db440 (NOGIL) | 1.114x ↑<br>[📄](results/bm-20260206-3.15.0a5%2B-74db440-NOGIL/bm-20260206-macm4pro-arm64-python-74db4404eaa9b4448b50-3.15.0a5%2B-74db440-vs-3.12.6.md)[📈](results/bm-20260206-3.15.0a5%2B-74db440-NOGIL/bm-20260206-macm4pro-arm64-python-74db4404eaa9b4448b50-3.15.0a5%2B-74db440-vs-3.12.6.svg) | 1.034x ↑<br>[📄](results/bm-20260206-3.15.0a5%2B-74db440-NOGIL/bm-20260206-macm4pro-arm64-python-74db4404eaa9b4448b50-3.15.0a5%2B-74db440-vs-3.13.0rc2.md)[📈](results/bm-20260206-3.15.0a5%2B-74db440-NOGIL/bm-20260206-macm4pro-arm64-python-74db4404eaa9b4448b50-3.15.0a5%2B-74db440-vs-3.13.0rc2.svg) | 1.068x ↓<br>[📄](results/bm-20260206-3.15.0a5%2B-74db440-NOGIL/bm-20260206-macm4pro-arm64-python-74db4404eaa9b4448b50-3.15.0a5%2B-74db440-vs-base.md)[📈](results/bm-20260206-3.15.0a5%2B-74db440-NOGIL/bm-20260206-macm4pro-arm64-python-74db4404eaa9b4448b50-3.15.0a5%2B-74db440-vs-base.svg)[🧠](results/bm-20260206-3.15.0a5%2B-74db440-NOGIL/bm-20260206-macm4pro-arm64-python-74db4404eaa9b4448b50-3.15.0a5%2B-74db440-vs-base-mem.svg) |
| [2026-02-06](results/bm-20260206-3.15.0a5%2B-74db440) | python/74db4404eaa9b4448b50 | 74db440 | 1.195x ↑<br>[📄](results/bm-20260206-3.15.0a5%2B-74db440/bm-20260206-macm4pro-arm64-python-74db4404eaa9b4448b50-3.15.0a5%2B-74db440-vs-3.12.6.md)[📈](results/bm-20260206-3.15.0a5%2B-74db440/bm-20260206-macm4pro-arm64-python-74db4404eaa9b4448b50-3.15.0a5%2B-74db440-vs-3.12.6.svg) | 1.109x ↑<br>[📄](results/bm-20260206-3.15.0a5%2B-74db440/bm-20260206-macm4pro-arm64-python-74db4404eaa9b4448b50-3.15.0a5%2B-74db440-vs-3.13.0rc2.md)[📈](results/bm-20260206-3.15.0a5%2B-74db440/bm-20260206-macm4pro-arm64-python-74db4404eaa9b4448b50-3.15.0a5%2B-74db440-vs-3.13.0rc2.svg) |  |
| [2026-02-05](results/bm-20260205-3.15.0a5%2B-957f9fe-NOGIL) | python/957f9fe162398fceeaa9 | 957f9fe (NOGIL) | 1.121x ↑<br>[📄](results/bm-20260205-3.15.0a5%2B-957f9fe-NOGIL/bm-20260205-macm4pro-arm64-python-957f9fe162398fceeaa9-3.15.0a5%2B-957f9fe-vs-3.12.6.md)[📈](results/bm-20260205-3.15.0a5%2B-957f9fe-NOGIL/bm-20260205-macm4pro-arm64-python-957f9fe162398fceeaa9-3.15.0a5%2B-957f9fe-vs-3.12.6.svg) | 1.040x ↑<br>[📄](results/bm-20260205-3.15.0a5%2B-957f9fe-NOGIL/bm-20260205-macm4pro-arm64-python-957f9fe162398fceeaa9-3.15.0a5%2B-957f9fe-vs-3.13.0rc2.md)[📈](results/bm-20260205-3.15.0a5%2B-957f9fe-NOGIL/bm-20260205-macm4pro-arm64-python-957f9fe162398fceeaa9-3.15.0a5%2B-957f9fe-vs-3.13.0rc2.svg) | 1.058x ↓<br>[📄](results/bm-20260205-3.15.0a5%2B-957f9fe-NOGIL/bm-20260205-macm4pro-arm64-python-957f9fe162398fceeaa9-3.15.0a5%2B-957f9fe-vs-base.md)[📈](results/bm-20260205-3.15.0a5%2B-957f9fe-NOGIL/bm-20260205-macm4pro-arm64-python-957f9fe162398fceeaa9-3.15.0a5%2B-957f9fe-vs-base.svg)[🧠](results/bm-20260205-3.15.0a5%2B-957f9fe-NOGIL/bm-20260205-macm4pro-arm64-python-957f9fe162398fceeaa9-3.15.0a5%2B-957f9fe-vs-base-mem.svg) |
| [2026-02-05](results/bm-20260205-3.15.0a5%2B-957f9fe) | python/957f9fe162398fceeaa9 | 957f9fe | 1.189x ↑<br>[📄](results/bm-20260205-3.15.0a5%2B-957f9fe/bm-20260205-macm4pro-arm64-python-957f9fe162398fceeaa9-3.15.0a5%2B-957f9fe-vs-3.12.6.md)[📈](results/bm-20260205-3.15.0a5%2B-957f9fe/bm-20260205-macm4pro-arm64-python-957f9fe162398fceeaa9-3.15.0a5%2B-957f9fe-vs-3.12.6.svg) | 1.103x ↑<br>[📄](results/bm-20260205-3.15.0a5%2B-957f9fe/bm-20260205-macm4pro-arm64-python-957f9fe162398fceeaa9-3.15.0a5%2B-957f9fe-vs-3.13.0rc2.md)[📈](results/bm-20260205-3.15.0a5%2B-957f9fe/bm-20260205-macm4pro-arm64-python-957f9fe162398fceeaa9-3.15.0a5%2B-957f9fe-vs-3.13.0rc2.svg) |  |
| [2026-02-04](results/bm-20260204-3.15.0a5%2B-b6d8aa4-NOGIL) | python/b6d8aa436b0108fcc90c | b6d8aa4 (NOGIL) | 1.120x ↑<br>[📄](results/bm-20260204-3.15.0a5%2B-b6d8aa4-NOGIL/bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5%2B-b6d8aa4-vs-3.12.6.md)[📈](results/bm-20260204-3.15.0a5%2B-b6d8aa4-NOGIL/bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5%2B-b6d8aa4-vs-3.12.6.svg) | 1.039x ↑<br>[📄](results/bm-20260204-3.15.0a5%2B-b6d8aa4-NOGIL/bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5%2B-b6d8aa4-vs-3.13.0rc2.md)[📈](results/bm-20260204-3.15.0a5%2B-b6d8aa4-NOGIL/bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5%2B-b6d8aa4-vs-3.13.0rc2.svg) | 1.064x ↓<br>[📄](results/bm-20260204-3.15.0a5%2B-b6d8aa4-NOGIL/bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5%2B-b6d8aa4-vs-base.md)[📈](results/bm-20260204-3.15.0a5%2B-b6d8aa4-NOGIL/bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5%2B-b6d8aa4-vs-base.svg)[🧠](results/bm-20260204-3.15.0a5%2B-b6d8aa4-NOGIL/bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5%2B-b6d8aa4-vs-base-mem.svg) |
| [2026-02-04](results/bm-20260204-3.15.0a5%2B-b6d8aa4) | python/b6d8aa436b0108fcc90c | b6d8aa4 | 1.196x ↑<br>[📄](results/bm-20260204-3.15.0a5%2B-b6d8aa4/bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5%2B-b6d8aa4-vs-3.12.6.md)[📈](results/bm-20260204-3.15.0a5%2B-b6d8aa4/bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5%2B-b6d8aa4-vs-3.12.6.svg) | 1.110x ↑<br>[📄](results/bm-20260204-3.15.0a5%2B-b6d8aa4/bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5%2B-b6d8aa4-vs-3.13.0rc2.md)[📈](results/bm-20260204-3.15.0a5%2B-b6d8aa4/bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5%2B-b6d8aa4-vs-3.13.0rc2.svg) |  |
| [2026-02-03](results/bm-20260203-3.15.0a5%2B-9d0c743-NOGIL) | python/9d0c7432ea40ab3f73af | 9d0c743 (NOGIL) | 1.132x ↑<br>[📄](results/bm-20260203-3.15.0a5%2B-9d0c743-NOGIL/bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5%2B-9d0c743-vs-3.12.6.md)[📈](results/bm-20260203-3.15.0a5%2B-9d0c743-NOGIL/bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5%2B-9d0c743-vs-3.12.6.svg) | 1.050x ↑<br>[📄](results/bm-20260203-3.15.0a5%2B-9d0c743-NOGIL/bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5%2B-9d0c743-vs-3.13.0rc2.md)[📈](results/bm-20260203-3.15.0a5%2B-9d0c743-NOGIL/bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5%2B-9d0c743-vs-3.13.0rc2.svg) | 1.048x ↓<br>[📄](results/bm-20260203-3.15.0a5%2B-9d0c743-NOGIL/bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5%2B-9d0c743-vs-base.md)[📈](results/bm-20260203-3.15.0a5%2B-9d0c743-NOGIL/bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5%2B-9d0c743-vs-base.svg)[🧠](results/bm-20260203-3.15.0a5%2B-9d0c743-NOGIL/bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5%2B-9d0c743-vs-base-mem.svg) |
| [2026-02-03](results/bm-20260203-3.15.0a5%2B-9d0c743) | python/9d0c7432ea40ab3f73af | 9d0c743 | 1.189x ↑<br>[📄](results/bm-20260203-3.15.0a5%2B-9d0c743/bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5%2B-9d0c743-vs-3.12.6.md)[📈](results/bm-20260203-3.15.0a5%2B-9d0c743/bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5%2B-9d0c743-vs-3.12.6.svg) | 1.103x ↑<br>[📄](results/bm-20260203-3.15.0a5%2B-9d0c743/bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5%2B-9d0c743-vs-3.13.0rc2.md)[📈](results/bm-20260203-3.15.0a5%2B-9d0c743/bm-20260203-macm4pro-arm64-python-9d0c7432ea40ab3f73af-3.15.0a5%2B-9d0c743-vs-3.13.0rc2.svg) |  |


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
