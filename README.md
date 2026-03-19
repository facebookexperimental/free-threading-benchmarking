# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (788c329)](results/bm-20260314-3.15.0a7%2B-788c329/bm-20260314-vultr-x86_64-python-788c3291172b55efa7cf-3.15.0a7%2B-788c329-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (788c329)](results/bm-20260314-3.15.0a7%2B-788c329-PYTHON_UOPS/bm-20260314-vultr-x86_64-python-788c3291172b55efa7cf-3.15.0a7%2B-788c329-pystats.md)
- [Most recent JIT pystats on main (bedaea0)](results/bm-20251019-3.15.0a1%2B-bedaea0-JIT/bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-03-19](results/bm-20260319-3.15.0a7%2B-b9d4318-NOGIL) | python/b9d43188e93967c3695e | b9d4318 (NOGIL) | 1.017x ↓<br>[📄](results/bm-20260319-3.15.0a7%2B-b9d4318-NOGIL/bm-20260319-vultr-x86_64-python-b9d43188e93967c3695e-3.15.0a7%2B-b9d4318-vs-3.12.6.md)[📈](results/bm-20260319-3.15.0a7%2B-b9d4318-NOGIL/bm-20260319-vultr-x86_64-python-b9d43188e93967c3695e-3.15.0a7%2B-b9d4318-vs-3.12.6.svg) | 1.050x ↓<br>[📄](results/bm-20260319-3.15.0a7%2B-b9d4318-NOGIL/bm-20260319-vultr-x86_64-python-b9d43188e93967c3695e-3.15.0a7%2B-b9d4318-vs-3.13.0rc2.md)[📈](results/bm-20260319-3.15.0a7%2B-b9d4318-NOGIL/bm-20260319-vultr-x86_64-python-b9d43188e93967c3695e-3.15.0a7%2B-b9d4318-vs-3.13.0rc2.svg) | 1.084x ↓<br>[📄](results/bm-20260319-3.15.0a7%2B-b9d4318-NOGIL/bm-20260319-vultr-x86_64-python-b9d43188e93967c3695e-3.15.0a7%2B-b9d4318-vs-base.md)[📈](results/bm-20260319-3.15.0a7%2B-b9d4318-NOGIL/bm-20260319-vultr-x86_64-python-b9d43188e93967c3695e-3.15.0a7%2B-b9d4318-vs-base.svg)[🧠](results/bm-20260319-3.15.0a7%2B-b9d4318-NOGIL/bm-20260319-vultr-x86_64-python-b9d43188e93967c3695e-3.15.0a7%2B-b9d4318-vs-base-mem.svg) |
| [2026-03-19](results/bm-20260319-3.15.0a7%2B-b9d4318) | python/b9d43188e93967c3695e | b9d4318 | 1.067x ↑<br>[📄](results/bm-20260319-3.15.0a7%2B-b9d4318/bm-20260319-vultr-x86_64-python-b9d43188e93967c3695e-3.15.0a7%2B-b9d4318-vs-3.12.6.md)[📈](results/bm-20260319-3.15.0a7%2B-b9d4318/bm-20260319-vultr-x86_64-python-b9d43188e93967c3695e-3.15.0a7%2B-b9d4318-vs-3.12.6.svg) | 1.031x ↑<br>[📄](results/bm-20260319-3.15.0a7%2B-b9d4318/bm-20260319-vultr-x86_64-python-b9d43188e93967c3695e-3.15.0a7%2B-b9d4318-vs-3.13.0rc2.md)[📈](results/bm-20260319-3.15.0a7%2B-b9d4318/bm-20260319-vultr-x86_64-python-b9d43188e93967c3695e-3.15.0a7%2B-b9d4318-vs-3.13.0rc2.svg) |  |
| [2026-03-17](results/bm-20260317-3.15.0a7%2B-e0f7c10-NOGIL) | python/e0f7c1097e19b6f5c239 | e0f7c10 (NOGIL) | 1.026x ↓<br>[📄](results/bm-20260317-3.15.0a7%2B-e0f7c10-NOGIL/bm-20260317-vultr-x86_64-python-e0f7c1097e19b6f5c239-3.15.0a7%2B-e0f7c10-vs-3.12.6.md)[📈](results/bm-20260317-3.15.0a7%2B-e0f7c10-NOGIL/bm-20260317-vultr-x86_64-python-e0f7c1097e19b6f5c239-3.15.0a7%2B-e0f7c10-vs-3.12.6.svg) | 1.058x ↓<br>[📄](results/bm-20260317-3.15.0a7%2B-e0f7c10-NOGIL/bm-20260317-vultr-x86_64-python-e0f7c1097e19b6f5c239-3.15.0a7%2B-e0f7c10-vs-3.13.0rc2.md)[📈](results/bm-20260317-3.15.0a7%2B-e0f7c10-NOGIL/bm-20260317-vultr-x86_64-python-e0f7c1097e19b6f5c239-3.15.0a7%2B-e0f7c10-vs-3.13.0rc2.svg) | 1.092x ↓<br>[📄](results/bm-20260317-3.15.0a7%2B-e0f7c10-NOGIL/bm-20260317-vultr-x86_64-python-e0f7c1097e19b6f5c239-3.15.0a7%2B-e0f7c10-vs-base.md)[📈](results/bm-20260317-3.15.0a7%2B-e0f7c10-NOGIL/bm-20260317-vultr-x86_64-python-e0f7c1097e19b6f5c239-3.15.0a7%2B-e0f7c10-vs-base.svg)[🧠](results/bm-20260317-3.15.0a7%2B-e0f7c10-NOGIL/bm-20260317-vultr-x86_64-python-e0f7c1097e19b6f5c239-3.15.0a7%2B-e0f7c10-vs-base-mem.svg) |
| [2026-03-17](results/bm-20260317-3.15.0a7%2B-e0f7c10) | python/e0f7c1097e19b6f5c239 | e0f7c10 | 1.068x ↑<br>[📄](results/bm-20260317-3.15.0a7%2B-e0f7c10/bm-20260317-vultr-x86_64-python-e0f7c1097e19b6f5c239-3.15.0a7%2B-e0f7c10-vs-3.12.6.md)[📈](results/bm-20260317-3.15.0a7%2B-e0f7c10/bm-20260317-vultr-x86_64-python-e0f7c1097e19b6f5c239-3.15.0a7%2B-e0f7c10-vs-3.12.6.svg) | 1.032x ↑<br>[📄](results/bm-20260317-3.15.0a7%2B-e0f7c10/bm-20260317-vultr-x86_64-python-e0f7c1097e19b6f5c239-3.15.0a7%2B-e0f7c10-vs-3.13.0rc2.md)[📈](results/bm-20260317-3.15.0a7%2B-e0f7c10/bm-20260317-vultr-x86_64-python-e0f7c1097e19b6f5c239-3.15.0a7%2B-e0f7c10-vs-3.13.0rc2.svg) |  |
| [2026-03-16](results/bm-20260316-3.15.0a7%2B-104cae0-NOGIL) | python/104cae039ac428709c7b | 104cae0 (NOGIL) | 1.026x ↓<br>[📄](results/bm-20260316-3.15.0a7%2B-104cae0-NOGIL/bm-20260316-vultr-x86_64-python-104cae039ac428709c7b-3.15.0a7%2B-104cae0-vs-3.12.6.md)[📈](results/bm-20260316-3.15.0a7%2B-104cae0-NOGIL/bm-20260316-vultr-x86_64-python-104cae039ac428709c7b-3.15.0a7%2B-104cae0-vs-3.12.6.svg) | 1.058x ↓<br>[📄](results/bm-20260316-3.15.0a7%2B-104cae0-NOGIL/bm-20260316-vultr-x86_64-python-104cae039ac428709c7b-3.15.0a7%2B-104cae0-vs-3.13.0rc2.md)[📈](results/bm-20260316-3.15.0a7%2B-104cae0-NOGIL/bm-20260316-vultr-x86_64-python-104cae039ac428709c7b-3.15.0a7%2B-104cae0-vs-3.13.0rc2.svg) | 1.090x ↓<br>[📄](results/bm-20260316-3.15.0a7%2B-104cae0-NOGIL/bm-20260316-vultr-x86_64-python-104cae039ac428709c7b-3.15.0a7%2B-104cae0-vs-base.md)[📈](results/bm-20260316-3.15.0a7%2B-104cae0-NOGIL/bm-20260316-vultr-x86_64-python-104cae039ac428709c7b-3.15.0a7%2B-104cae0-vs-base.svg)[🧠](results/bm-20260316-3.15.0a7%2B-104cae0-NOGIL/bm-20260316-vultr-x86_64-python-104cae039ac428709c7b-3.15.0a7%2B-104cae0-vs-base-mem.svg) |
| [2026-03-16](results/bm-20260316-3.15.0a7%2B-104cae0) | python/104cae039ac428709c7b | 104cae0 | 1.065x ↑<br>[📄](results/bm-20260316-3.15.0a7%2B-104cae0/bm-20260316-vultr-x86_64-python-104cae039ac428709c7b-3.15.0a7%2B-104cae0-vs-3.12.6.md)[📈](results/bm-20260316-3.15.0a7%2B-104cae0/bm-20260316-vultr-x86_64-python-104cae039ac428709c7b-3.15.0a7%2B-104cae0-vs-3.12.6.svg) | 1.029x ↑<br>[📄](results/bm-20260316-3.15.0a7%2B-104cae0/bm-20260316-vultr-x86_64-python-104cae039ac428709c7b-3.15.0a7%2B-104cae0-vs-3.13.0rc2.md)[📈](results/bm-20260316-3.15.0a7%2B-104cae0/bm-20260316-vultr-x86_64-python-104cae039ac428709c7b-3.15.0a7%2B-104cae0-vs-3.13.0rc2.svg) |  |
| [2026-03-15](results/bm-20260315-3.15.0a7%2B-40095d5-NOGIL) | python/40095d526bd8ddbabee0 | 40095d5 (NOGIL) | 1.025x ↓<br>[📄](results/bm-20260315-3.15.0a7%2B-40095d5-NOGIL/bm-20260315-vultr-x86_64-python-40095d526bd8ddbabee0-3.15.0a7%2B-40095d5-vs-3.12.6.md)[📈](results/bm-20260315-3.15.0a7%2B-40095d5-NOGIL/bm-20260315-vultr-x86_64-python-40095d526bd8ddbabee0-3.15.0a7%2B-40095d5-vs-3.12.6.svg) | 1.058x ↓<br>[📄](results/bm-20260315-3.15.0a7%2B-40095d5-NOGIL/bm-20260315-vultr-x86_64-python-40095d526bd8ddbabee0-3.15.0a7%2B-40095d5-vs-3.13.0rc2.md)[📈](results/bm-20260315-3.15.0a7%2B-40095d5-NOGIL/bm-20260315-vultr-x86_64-python-40095d526bd8ddbabee0-3.15.0a7%2B-40095d5-vs-3.13.0rc2.svg) | 1.094x ↓<br>[📄](results/bm-20260315-3.15.0a7%2B-40095d5-NOGIL/bm-20260315-vultr-x86_64-python-40095d526bd8ddbabee0-3.15.0a7%2B-40095d5-vs-base.md)[📈](results/bm-20260315-3.15.0a7%2B-40095d5-NOGIL/bm-20260315-vultr-x86_64-python-40095d526bd8ddbabee0-3.15.0a7%2B-40095d5-vs-base.svg)[🧠](results/bm-20260315-3.15.0a7%2B-40095d5-NOGIL/bm-20260315-vultr-x86_64-python-40095d526bd8ddbabee0-3.15.0a7%2B-40095d5-vs-base-mem.svg) |
| [2026-03-15](results/bm-20260315-3.15.0a7%2B-40095d5) | python/40095d526bd8ddbabee0 | 40095d5 | 1.071x ↑<br>[📄](results/bm-20260315-3.15.0a7%2B-40095d5/bm-20260315-vultr-x86_64-python-40095d526bd8ddbabee0-3.15.0a7%2B-40095d5-vs-3.12.6.md)[📈](results/bm-20260315-3.15.0a7%2B-40095d5/bm-20260315-vultr-x86_64-python-40095d526bd8ddbabee0-3.15.0a7%2B-40095d5-vs-3.12.6.svg) | 1.035x ↑<br>[📄](results/bm-20260315-3.15.0a7%2B-40095d5/bm-20260315-vultr-x86_64-python-40095d526bd8ddbabee0-3.15.0a7%2B-40095d5-vs-3.13.0rc2.md)[📈](results/bm-20260315-3.15.0a7%2B-40095d5/bm-20260315-vultr-x86_64-python-40095d526bd8ddbabee0-3.15.0a7%2B-40095d5-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-03-19](results/bm-20260319-3.15.0a7%2B-b9d4318-NOGIL) | python/b9d43188e93967c3695e | b9d4318 (NOGIL) | 1.105x ↑<br>[📄](results/bm-20260319-3.15.0a7%2B-b9d4318-NOGIL/bm-20260319-macm4pro-arm64-python-b9d43188e93967c3695e-3.15.0a7%2B-b9d4318-vs-3.12.6.md)[📈](results/bm-20260319-3.15.0a7%2B-b9d4318-NOGIL/bm-20260319-macm4pro-arm64-python-b9d43188e93967c3695e-3.15.0a7%2B-b9d4318-vs-3.12.6.svg) | 1.025x ↑<br>[📄](results/bm-20260319-3.15.0a7%2B-b9d4318-NOGIL/bm-20260319-macm4pro-arm64-python-b9d43188e93967c3695e-3.15.0a7%2B-b9d4318-vs-3.13.0rc2.md)[📈](results/bm-20260319-3.15.0a7%2B-b9d4318-NOGIL/bm-20260319-macm4pro-arm64-python-b9d43188e93967c3695e-3.15.0a7%2B-b9d4318-vs-3.13.0rc2.svg) | 1.047x ↓<br>[📄](results/bm-20260319-3.15.0a7%2B-b9d4318-NOGIL/bm-20260319-macm4pro-arm64-python-b9d43188e93967c3695e-3.15.0a7%2B-b9d4318-vs-base.md)[📈](results/bm-20260319-3.15.0a7%2B-b9d4318-NOGIL/bm-20260319-macm4pro-arm64-python-b9d43188e93967c3695e-3.15.0a7%2B-b9d4318-vs-base.svg)[🧠](results/bm-20260319-3.15.0a7%2B-b9d4318-NOGIL/bm-20260319-macm4pro-arm64-python-b9d43188e93967c3695e-3.15.0a7%2B-b9d4318-vs-base-mem.svg) |
| [2026-03-19](results/bm-20260319-3.15.0a7%2B-b9d4318) | python/b9d43188e93967c3695e | b9d4318 | 1.160x ↑<br>[📄](results/bm-20260319-3.15.0a7%2B-b9d4318/bm-20260319-macm4pro-arm64-python-b9d43188e93967c3695e-3.15.0a7%2B-b9d4318-vs-3.12.6.md)[📈](results/bm-20260319-3.15.0a7%2B-b9d4318/bm-20260319-macm4pro-arm64-python-b9d43188e93967c3695e-3.15.0a7%2B-b9d4318-vs-3.12.6.svg) | 1.076x ↑<br>[📄](results/bm-20260319-3.15.0a7%2B-b9d4318/bm-20260319-macm4pro-arm64-python-b9d43188e93967c3695e-3.15.0a7%2B-b9d4318-vs-3.13.0rc2.md)[📈](results/bm-20260319-3.15.0a7%2B-b9d4318/bm-20260319-macm4pro-arm64-python-b9d43188e93967c3695e-3.15.0a7%2B-b9d4318-vs-3.13.0rc2.svg) |  |
| [2026-03-17](results/bm-20260317-3.15.0a7%2B-e0f7c10-NOGIL) | python/e0f7c1097e19b6f5c239 | e0f7c10 (NOGIL) | 1.102x ↑<br>[📄](results/bm-20260317-3.15.0a7%2B-e0f7c10-NOGIL/bm-20260317-macm4pro-arm64-python-e0f7c1097e19b6f5c239-3.15.0a7%2B-e0f7c10-vs-3.12.6.md)[📈](results/bm-20260317-3.15.0a7%2B-e0f7c10-NOGIL/bm-20260317-macm4pro-arm64-python-e0f7c1097e19b6f5c239-3.15.0a7%2B-e0f7c10-vs-3.12.6.svg) | 1.023x ↑<br>[📄](results/bm-20260317-3.15.0a7%2B-e0f7c10-NOGIL/bm-20260317-macm4pro-arm64-python-e0f7c1097e19b6f5c239-3.15.0a7%2B-e0f7c10-vs-3.13.0rc2.md)[📈](results/bm-20260317-3.15.0a7%2B-e0f7c10-NOGIL/bm-20260317-macm4pro-arm64-python-e0f7c1097e19b6f5c239-3.15.0a7%2B-e0f7c10-vs-3.13.0rc2.svg) | 1.049x ↓<br>[📄](results/bm-20260317-3.15.0a7%2B-e0f7c10-NOGIL/bm-20260317-macm4pro-arm64-python-e0f7c1097e19b6f5c239-3.15.0a7%2B-e0f7c10-vs-base.md)[📈](results/bm-20260317-3.15.0a7%2B-e0f7c10-NOGIL/bm-20260317-macm4pro-arm64-python-e0f7c1097e19b6f5c239-3.15.0a7%2B-e0f7c10-vs-base.svg)[🧠](results/bm-20260317-3.15.0a7%2B-e0f7c10-NOGIL/bm-20260317-macm4pro-arm64-python-e0f7c1097e19b6f5c239-3.15.0a7%2B-e0f7c10-vs-base-mem.svg) |
| [2026-03-17](results/bm-20260317-3.15.0a7%2B-e0f7c10) | python/e0f7c1097e19b6f5c239 | e0f7c10 | 1.159x ↑<br>[📄](results/bm-20260317-3.15.0a7%2B-e0f7c10/bm-20260317-macm4pro-arm64-python-e0f7c1097e19b6f5c239-3.15.0a7%2B-e0f7c10-vs-3.12.6.md)[📈](results/bm-20260317-3.15.0a7%2B-e0f7c10/bm-20260317-macm4pro-arm64-python-e0f7c1097e19b6f5c239-3.15.0a7%2B-e0f7c10-vs-3.12.6.svg) | 1.075x ↑<br>[📄](results/bm-20260317-3.15.0a7%2B-e0f7c10/bm-20260317-macm4pro-arm64-python-e0f7c1097e19b6f5c239-3.15.0a7%2B-e0f7c10-vs-3.13.0rc2.md)[📈](results/bm-20260317-3.15.0a7%2B-e0f7c10/bm-20260317-macm4pro-arm64-python-e0f7c1097e19b6f5c239-3.15.0a7%2B-e0f7c10-vs-3.13.0rc2.svg) |  |
| [2026-03-16](results/bm-20260316-3.15.0a7%2B-104cae0-NOGIL) | python/104cae039ac428709c7b | 104cae0 (NOGIL) | 1.096x ↑<br>[📄](results/bm-20260316-3.15.0a7%2B-104cae0-NOGIL/bm-20260316-macm4pro-arm64-python-104cae039ac428709c7b-3.15.0a7%2B-104cae0-vs-3.12.6.md)[📈](results/bm-20260316-3.15.0a7%2B-104cae0-NOGIL/bm-20260316-macm4pro-arm64-python-104cae039ac428709c7b-3.15.0a7%2B-104cae0-vs-3.12.6.svg) | 1.017x ↑<br>[📄](results/bm-20260316-3.15.0a7%2B-104cae0-NOGIL/bm-20260316-macm4pro-arm64-python-104cae039ac428709c7b-3.15.0a7%2B-104cae0-vs-3.13.0rc2.md)[📈](results/bm-20260316-3.15.0a7%2B-104cae0-NOGIL/bm-20260316-macm4pro-arm64-python-104cae039ac428709c7b-3.15.0a7%2B-104cae0-vs-3.13.0rc2.svg) | 1.056x ↓<br>[📄](results/bm-20260316-3.15.0a7%2B-104cae0-NOGIL/bm-20260316-macm4pro-arm64-python-104cae039ac428709c7b-3.15.0a7%2B-104cae0-vs-base.md)[📈](results/bm-20260316-3.15.0a7%2B-104cae0-NOGIL/bm-20260316-macm4pro-arm64-python-104cae039ac428709c7b-3.15.0a7%2B-104cae0-vs-base.svg)[🧠](results/bm-20260316-3.15.0a7%2B-104cae0-NOGIL/bm-20260316-macm4pro-arm64-python-104cae039ac428709c7b-3.15.0a7%2B-104cae0-vs-base-mem.svg) |
| [2026-03-16](results/bm-20260316-3.15.0a7%2B-104cae0) | python/104cae039ac428709c7b | 104cae0 | 1.160x ↑<br>[📄](results/bm-20260316-3.15.0a7%2B-104cae0/bm-20260316-macm4pro-arm64-python-104cae039ac428709c7b-3.15.0a7%2B-104cae0-vs-3.12.6.md)[📈](results/bm-20260316-3.15.0a7%2B-104cae0/bm-20260316-macm4pro-arm64-python-104cae039ac428709c7b-3.15.0a7%2B-104cae0-vs-3.12.6.svg) | 1.076x ↑<br>[📄](results/bm-20260316-3.15.0a7%2B-104cae0/bm-20260316-macm4pro-arm64-python-104cae039ac428709c7b-3.15.0a7%2B-104cae0-vs-3.13.0rc2.md)[📈](results/bm-20260316-3.15.0a7%2B-104cae0/bm-20260316-macm4pro-arm64-python-104cae039ac428709c7b-3.15.0a7%2B-104cae0-vs-3.13.0rc2.svg) |  |
| [2026-03-15](results/bm-20260315-3.15.0a7%2B-40095d5-NOGIL) | python/40095d526bd8ddbabee0 | 40095d5 (NOGIL) | 1.096x ↑<br>[📄](results/bm-20260315-3.15.0a7%2B-40095d5-NOGIL/bm-20260315-macm4pro-arm64-python-40095d526bd8ddbabee0-3.15.0a7%2B-40095d5-vs-3.12.6.md)[📈](results/bm-20260315-3.15.0a7%2B-40095d5-NOGIL/bm-20260315-macm4pro-arm64-python-40095d526bd8ddbabee0-3.15.0a7%2B-40095d5-vs-3.12.6.svg) | 1.017x ↑<br>[📄](results/bm-20260315-3.15.0a7%2B-40095d5-NOGIL/bm-20260315-macm4pro-arm64-python-40095d526bd8ddbabee0-3.15.0a7%2B-40095d5-vs-3.13.0rc2.md)[📈](results/bm-20260315-3.15.0a7%2B-40095d5-NOGIL/bm-20260315-macm4pro-arm64-python-40095d526bd8ddbabee0-3.15.0a7%2B-40095d5-vs-3.13.0rc2.svg) | 1.057x ↓<br>[📄](results/bm-20260315-3.15.0a7%2B-40095d5-NOGIL/bm-20260315-macm4pro-arm64-python-40095d526bd8ddbabee0-3.15.0a7%2B-40095d5-vs-base.md)[📈](results/bm-20260315-3.15.0a7%2B-40095d5-NOGIL/bm-20260315-macm4pro-arm64-python-40095d526bd8ddbabee0-3.15.0a7%2B-40095d5-vs-base.svg)[🧠](results/bm-20260315-3.15.0a7%2B-40095d5-NOGIL/bm-20260315-macm4pro-arm64-python-40095d526bd8ddbabee0-3.15.0a7%2B-40095d5-vs-base-mem.svg) |
| [2026-03-15](results/bm-20260315-3.15.0a7%2B-40095d5) | python/40095d526bd8ddbabee0 | 40095d5 | 1.163x ↑<br>[📄](results/bm-20260315-3.15.0a7%2B-40095d5/bm-20260315-macm4pro-arm64-python-40095d526bd8ddbabee0-3.15.0a7%2B-40095d5-vs-3.12.6.md)[📈](results/bm-20260315-3.15.0a7%2B-40095d5/bm-20260315-macm4pro-arm64-python-40095d526bd8ddbabee0-3.15.0a7%2B-40095d5-vs-3.12.6.svg) | 1.079x ↑<br>[📄](results/bm-20260315-3.15.0a7%2B-40095d5/bm-20260315-macm4pro-arm64-python-40095d526bd8ddbabee0-3.15.0a7%2B-40095d5-vs-3.13.0rc2.md)[📈](results/bm-20260315-3.15.0a7%2B-40095d5/bm-20260315-macm4pro-arm64-python-40095d526bd8ddbabee0-3.15.0a7%2B-40095d5-vs-3.13.0rc2.svg) |  |


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
