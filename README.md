# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (8d2d7bb)](results/bm-20251220-3.15.0a3%2B-8d2d7bb/bm-20251220-vultr-x86_64-python-8d2d7bb2e754f8649a68-3.15.0a3%2B-8d2d7bb-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (8d2d7bb)](results/bm-20251220-3.15.0a3%2B-8d2d7bb-PYTHON_UOPS/bm-20251220-vultr-x86_64-python-8d2d7bb2e754f8649a68-3.15.0a3%2B-8d2d7bb-pystats.md)
- [Most recent JIT pystats on main (bedaea0)](results/bm-20251019-3.15.0a1%2B-bedaea0-JIT/bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-12-26](results/bm-20251226-3.15.0a3%2B-a1c6308-NOGIL) | python/a1c630834649d54ffbca | a1c6308 (NOGIL) | 1.035x ↓<br>[📄](results/bm-20251226-3.15.0a3%2B-a1c6308-NOGIL/bm-20251226-vultr-x86_64-python-a1c630834649d54ffbca-3.15.0a3%2B-a1c6308-vs-3.12.6.md)[📈](results/bm-20251226-3.15.0a3%2B-a1c6308-NOGIL/bm-20251226-vultr-x86_64-python-a1c630834649d54ffbca-3.15.0a3%2B-a1c6308-vs-3.12.6.svg) | 1.068x ↓<br>[📄](results/bm-20251226-3.15.0a3%2B-a1c6308-NOGIL/bm-20251226-vultr-x86_64-python-a1c630834649d54ffbca-3.15.0a3%2B-a1c6308-vs-3.13.0rc2.md)[📈](results/bm-20251226-3.15.0a3%2B-a1c6308-NOGIL/bm-20251226-vultr-x86_64-python-a1c630834649d54ffbca-3.15.0a3%2B-a1c6308-vs-3.13.0rc2.svg) | 1.109x ↓<br>[📄](results/bm-20251226-3.15.0a3%2B-a1c6308-NOGIL/bm-20251226-vultr-x86_64-python-a1c630834649d54ffbca-3.15.0a3%2B-a1c6308-vs-base.md)[📈](results/bm-20251226-3.15.0a3%2B-a1c6308-NOGIL/bm-20251226-vultr-x86_64-python-a1c630834649d54ffbca-3.15.0a3%2B-a1c6308-vs-base.svg)[🧠](results/bm-20251226-3.15.0a3%2B-a1c6308-NOGIL/bm-20251226-vultr-x86_64-python-a1c630834649d54ffbca-3.15.0a3%2B-a1c6308-vs-base-mem.svg) |
| [2025-12-26](results/bm-20251226-3.15.0a3%2B-a1c6308) | python/a1c630834649d54ffbca | a1c6308 | 1.079x ↑<br>[📄](results/bm-20251226-3.15.0a3%2B-a1c6308/bm-20251226-vultr-x86_64-python-a1c630834649d54ffbca-3.15.0a3%2B-a1c6308-vs-3.12.6.md)[📈](results/bm-20251226-3.15.0a3%2B-a1c6308/bm-20251226-vultr-x86_64-python-a1c630834649d54ffbca-3.15.0a3%2B-a1c6308-vs-3.12.6.svg) | 1.043x ↑<br>[📄](results/bm-20251226-3.15.0a3%2B-a1c6308/bm-20251226-vultr-x86_64-python-a1c630834649d54ffbca-3.15.0a3%2B-a1c6308-vs-3.13.0rc2.md)[📈](results/bm-20251226-3.15.0a3%2B-a1c6308/bm-20251226-vultr-x86_64-python-a1c630834649d54ffbca-3.15.0a3%2B-a1c6308-vs-3.13.0rc2.svg) |  |
| [2025-12-25](results/bm-20251225-3.15.0a3%2B-888d101-NOGIL) | python/888d101445c72c7cf239 | 888d101 (NOGIL) | 1.030x ↓<br>[📄](results/bm-20251225-3.15.0a3%2B-888d101-NOGIL/bm-20251225-vultr-x86_64-python-888d101445c72c7cf239-3.15.0a3%2B-888d101-vs-3.12.6.md)[📈](results/bm-20251225-3.15.0a3%2B-888d101-NOGIL/bm-20251225-vultr-x86_64-python-888d101445c72c7cf239-3.15.0a3%2B-888d101-vs-3.12.6.svg) | 1.063x ↓<br>[📄](results/bm-20251225-3.15.0a3%2B-888d101-NOGIL/bm-20251225-vultr-x86_64-python-888d101445c72c7cf239-3.15.0a3%2B-888d101-vs-3.13.0rc2.md)[📈](results/bm-20251225-3.15.0a3%2B-888d101-NOGIL/bm-20251225-vultr-x86_64-python-888d101445c72c7cf239-3.15.0a3%2B-888d101-vs-3.13.0rc2.svg) | 1.102x ↓<br>[📄](results/bm-20251225-3.15.0a3%2B-888d101-NOGIL/bm-20251225-vultr-x86_64-python-888d101445c72c7cf239-3.15.0a3%2B-888d101-vs-base.md)[📈](results/bm-20251225-3.15.0a3%2B-888d101-NOGIL/bm-20251225-vultr-x86_64-python-888d101445c72c7cf239-3.15.0a3%2B-888d101-vs-base.svg)[🧠](results/bm-20251225-3.15.0a3%2B-888d101-NOGIL/bm-20251225-vultr-x86_64-python-888d101445c72c7cf239-3.15.0a3%2B-888d101-vs-base-mem.svg) |
| [2025-12-25](results/bm-20251225-3.15.0a3%2B-888d101) | python/888d101445c72c7cf239 | 888d101 | 1.073x ↑<br>[📄](results/bm-20251225-3.15.0a3%2B-888d101/bm-20251225-vultr-x86_64-python-888d101445c72c7cf239-3.15.0a3%2B-888d101-vs-3.12.6.md)[📈](results/bm-20251225-3.15.0a3%2B-888d101/bm-20251225-vultr-x86_64-python-888d101445c72c7cf239-3.15.0a3%2B-888d101-vs-3.12.6.svg) | 1.038x ↑<br>[📄](results/bm-20251225-3.15.0a3%2B-888d101/bm-20251225-vultr-x86_64-python-888d101445c72c7cf239-3.15.0a3%2B-888d101-vs-3.13.0rc2.md)[📈](results/bm-20251225-3.15.0a3%2B-888d101/bm-20251225-vultr-x86_64-python-888d101445c72c7cf239-3.15.0a3%2B-888d101-vs-3.13.0rc2.svg) |  |
| [2025-12-24](results/bm-20251224-3.15.0a3%2B-cf6758f-NOGIL) | python/cf6758ff9ebd6df8ac2a | cf6758f (NOGIL) | 1.030x ↓<br>[📄](results/bm-20251224-3.15.0a3%2B-cf6758f-NOGIL/bm-20251224-vultr-x86_64-python-cf6758ff9ebd6df8ac2a-3.15.0a3%2B-cf6758f-vs-3.12.6.md)[📈](results/bm-20251224-3.15.0a3%2B-cf6758f-NOGIL/bm-20251224-vultr-x86_64-python-cf6758ff9ebd6df8ac2a-3.15.0a3%2B-cf6758f-vs-3.12.6.svg) | 1.062x ↓<br>[📄](results/bm-20251224-3.15.0a3%2B-cf6758f-NOGIL/bm-20251224-vultr-x86_64-python-cf6758ff9ebd6df8ac2a-3.15.0a3%2B-cf6758f-vs-3.13.0rc2.md)[📈](results/bm-20251224-3.15.0a3%2B-cf6758f-NOGIL/bm-20251224-vultr-x86_64-python-cf6758ff9ebd6df8ac2a-3.15.0a3%2B-cf6758f-vs-3.13.0rc2.svg) | 1.104x ↓<br>[📄](results/bm-20251224-3.15.0a3%2B-cf6758f-NOGIL/bm-20251224-vultr-x86_64-python-cf6758ff9ebd6df8ac2a-3.15.0a3%2B-cf6758f-vs-base.md)[📈](results/bm-20251224-3.15.0a3%2B-cf6758f-NOGIL/bm-20251224-vultr-x86_64-python-cf6758ff9ebd6df8ac2a-3.15.0a3%2B-cf6758f-vs-base.svg)[🧠](results/bm-20251224-3.15.0a3%2B-cf6758f-NOGIL/bm-20251224-vultr-x86_64-python-cf6758ff9ebd6df8ac2a-3.15.0a3%2B-cf6758f-vs-base-mem.svg) |
| [2025-12-24](results/bm-20251224-3.15.0a3%2B-cf6758f) | python/cf6758ff9ebd6df8ac2a | cf6758f | 1.077x ↑<br>[📄](results/bm-20251224-3.15.0a3%2B-cf6758f/bm-20251224-vultr-x86_64-python-cf6758ff9ebd6df8ac2a-3.15.0a3%2B-cf6758f-vs-3.12.6.md)[📈](results/bm-20251224-3.15.0a3%2B-cf6758f/bm-20251224-vultr-x86_64-python-cf6758ff9ebd6df8ac2a-3.15.0a3%2B-cf6758f-vs-3.12.6.svg) | 1.041x ↑<br>[📄](results/bm-20251224-3.15.0a3%2B-cf6758f/bm-20251224-vultr-x86_64-python-cf6758ff9ebd6df8ac2a-3.15.0a3%2B-cf6758f-vs-3.13.0rc2.md)[📈](results/bm-20251224-3.15.0a3%2B-cf6758f/bm-20251224-vultr-x86_64-python-cf6758ff9ebd6df8ac2a-3.15.0a3%2B-cf6758f-vs-3.13.0rc2.svg) |  |
| [2025-12-23](results/bm-20251223-3.15.0a3%2B-cc48bf0-NOGIL) | python/cc48bf0fde8025d60a57 | cc48bf0 (NOGIL) | 1.027x ↓<br>[📄](results/bm-20251223-3.15.0a3%2B-cc48bf0-NOGIL/bm-20251223-vultr-x86_64-python-cc48bf0fde8025d60a57-3.15.0a3%2B-cc48bf0-vs-3.12.6.md)[📈](results/bm-20251223-3.15.0a3%2B-cc48bf0-NOGIL/bm-20251223-vultr-x86_64-python-cc48bf0fde8025d60a57-3.15.0a3%2B-cc48bf0-vs-3.12.6.svg) | 1.060x ↓<br>[📄](results/bm-20251223-3.15.0a3%2B-cc48bf0-NOGIL/bm-20251223-vultr-x86_64-python-cc48bf0fde8025d60a57-3.15.0a3%2B-cc48bf0-vs-3.13.0rc2.md)[📈](results/bm-20251223-3.15.0a3%2B-cc48bf0-NOGIL/bm-20251223-vultr-x86_64-python-cc48bf0fde8025d60a57-3.15.0a3%2B-cc48bf0-vs-3.13.0rc2.svg) | 1.093x ↓<br>[📄](results/bm-20251223-3.15.0a3%2B-cc48bf0-NOGIL/bm-20251223-vultr-x86_64-python-cc48bf0fde8025d60a57-3.15.0a3%2B-cc48bf0-vs-base.md)[📈](results/bm-20251223-3.15.0a3%2B-cc48bf0-NOGIL/bm-20251223-vultr-x86_64-python-cc48bf0fde8025d60a57-3.15.0a3%2B-cc48bf0-vs-base.svg)[🧠](results/bm-20251223-3.15.0a3%2B-cc48bf0-NOGIL/bm-20251223-vultr-x86_64-python-cc48bf0fde8025d60a57-3.15.0a3%2B-cc48bf0-vs-base-mem.svg) |
| [2025-12-23](results/bm-20251223-3.15.0a3%2B-cc48bf0) | python/cc48bf0fde8025d60a57 | cc48bf0 | 1.067x ↑<br>[📄](results/bm-20251223-3.15.0a3%2B-cc48bf0/bm-20251223-vultr-x86_64-python-cc48bf0fde8025d60a57-3.15.0a3%2B-cc48bf0-vs-3.12.6.md)[📈](results/bm-20251223-3.15.0a3%2B-cc48bf0/bm-20251223-vultr-x86_64-python-cc48bf0fde8025d60a57-3.15.0a3%2B-cc48bf0-vs-3.12.6.svg) | 1.031x ↑<br>[📄](results/bm-20251223-3.15.0a3%2B-cc48bf0/bm-20251223-vultr-x86_64-python-cc48bf0fde8025d60a57-3.15.0a3%2B-cc48bf0-vs-3.13.0rc2.md)[📈](results/bm-20251223-3.15.0a3%2B-cc48bf0/bm-20251223-vultr-x86_64-python-cc48bf0fde8025d60a57-3.15.0a3%2B-cc48bf0-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-12-26](results/bm-20251226-3.15.0a3%2B-a1c6308-NOGIL) | python/a1c630834649d54ffbca | a1c6308 (NOGIL) | 1.095x ↑<br>[📄](results/bm-20251226-3.15.0a3%2B-a1c6308-NOGIL/bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3%2B-a1c6308-vs-3.12.6.md)[📈](results/bm-20251226-3.15.0a3%2B-a1c6308-NOGIL/bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3%2B-a1c6308-vs-3.12.6.svg) | 1.016x ↑<br>[📄](results/bm-20251226-3.15.0a3%2B-a1c6308-NOGIL/bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3%2B-a1c6308-vs-3.13.0rc2.md)[📈](results/bm-20251226-3.15.0a3%2B-a1c6308-NOGIL/bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3%2B-a1c6308-vs-3.13.0rc2.svg) | 1.062x ↓<br>[📄](results/bm-20251226-3.15.0a3%2B-a1c6308-NOGIL/bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3%2B-a1c6308-vs-base.md)[📈](results/bm-20251226-3.15.0a3%2B-a1c6308-NOGIL/bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3%2B-a1c6308-vs-base.svg)[🧠](results/bm-20251226-3.15.0a3%2B-a1c6308-NOGIL/bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3%2B-a1c6308-vs-base-mem.svg) |
| [2025-12-26](results/bm-20251226-3.15.0a3%2B-a1c6308) | python/a1c630834649d54ffbca | a1c6308 | 1.167x ↑<br>[📄](results/bm-20251226-3.15.0a3%2B-a1c6308/bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3%2B-a1c6308-vs-3.12.6.md)[📈](results/bm-20251226-3.15.0a3%2B-a1c6308/bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3%2B-a1c6308-vs-3.12.6.svg) | 1.082x ↑<br>[📄](results/bm-20251226-3.15.0a3%2B-a1c6308/bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3%2B-a1c6308-vs-3.13.0rc2.md)[📈](results/bm-20251226-3.15.0a3%2B-a1c6308/bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3%2B-a1c6308-vs-3.13.0rc2.svg) |  |
| [2025-12-25](results/bm-20251225-3.15.0a3%2B-888d101-NOGIL) | python/888d101445c72c7cf239 | 888d101 (NOGIL) | 1.130x ↑<br>[📄](results/bm-20251225-3.15.0a3%2B-888d101-NOGIL/bm-20251225-macm4pro-arm64-python-888d101445c72c7cf239-3.15.0a3%2B-888d101-vs-3.12.6.md)[📈](results/bm-20251225-3.15.0a3%2B-888d101-NOGIL/bm-20251225-macm4pro-arm64-python-888d101445c72c7cf239-3.15.0a3%2B-888d101-vs-3.12.6.svg) | 1.048x ↑<br>[📄](results/bm-20251225-3.15.0a3%2B-888d101-NOGIL/bm-20251225-macm4pro-arm64-python-888d101445c72c7cf239-3.15.0a3%2B-888d101-vs-3.13.0rc2.md)[📈](results/bm-20251225-3.15.0a3%2B-888d101-NOGIL/bm-20251225-macm4pro-arm64-python-888d101445c72c7cf239-3.15.0a3%2B-888d101-vs-3.13.0rc2.svg) | 1.060x ↓<br>[📄](results/bm-20251225-3.15.0a3%2B-888d101-NOGIL/bm-20251225-macm4pro-arm64-python-888d101445c72c7cf239-3.15.0a3%2B-888d101-vs-base.md)[📈](results/bm-20251225-3.15.0a3%2B-888d101-NOGIL/bm-20251225-macm4pro-arm64-python-888d101445c72c7cf239-3.15.0a3%2B-888d101-vs-base.svg)[🧠](results/bm-20251225-3.15.0a3%2B-888d101-NOGIL/bm-20251225-macm4pro-arm64-python-888d101445c72c7cf239-3.15.0a3%2B-888d101-vs-base-mem.svg) |
| [2025-12-25](results/bm-20251225-3.15.0a3%2B-888d101) | python/888d101445c72c7cf239 | 888d101 | 1.199x ↑<br>[📄](results/bm-20251225-3.15.0a3%2B-888d101/bm-20251225-macm4pro-arm64-python-888d101445c72c7cf239-3.15.0a3%2B-888d101-vs-3.12.6.md)[📈](results/bm-20251225-3.15.0a3%2B-888d101/bm-20251225-macm4pro-arm64-python-888d101445c72c7cf239-3.15.0a3%2B-888d101-vs-3.12.6.svg) | 1.113x ↑<br>[📄](results/bm-20251225-3.15.0a3%2B-888d101/bm-20251225-macm4pro-arm64-python-888d101445c72c7cf239-3.15.0a3%2B-888d101-vs-3.13.0rc2.md)[📈](results/bm-20251225-3.15.0a3%2B-888d101/bm-20251225-macm4pro-arm64-python-888d101445c72c7cf239-3.15.0a3%2B-888d101-vs-3.13.0rc2.svg) |  |
| [2025-12-24](results/bm-20251224-3.15.0a3%2B-cf6758f-NOGIL) | python/cf6758ff9ebd6df8ac2a | cf6758f (NOGIL) | 1.096x ↑<br>[📄](results/bm-20251224-3.15.0a3%2B-cf6758f-NOGIL/bm-20251224-macm4pro-arm64-python-cf6758ff9ebd6df8ac2a-3.15.0a3%2B-cf6758f-vs-3.12.6.md)[📈](results/bm-20251224-3.15.0a3%2B-cf6758f-NOGIL/bm-20251224-macm4pro-arm64-python-cf6758ff9ebd6df8ac2a-3.15.0a3%2B-cf6758f-vs-3.12.6.svg) | 1.015x ↑<br>[📄](results/bm-20251224-3.15.0a3%2B-cf6758f-NOGIL/bm-20251224-macm4pro-arm64-python-cf6758ff9ebd6df8ac2a-3.15.0a3%2B-cf6758f-vs-3.13.0rc2.md)[📈](results/bm-20251224-3.15.0a3%2B-cf6758f-NOGIL/bm-20251224-macm4pro-arm64-python-cf6758ff9ebd6df8ac2a-3.15.0a3%2B-cf6758f-vs-3.13.0rc2.svg) | 1.060x ↓<br>[📄](results/bm-20251224-3.15.0a3%2B-cf6758f-NOGIL/bm-20251224-macm4pro-arm64-python-cf6758ff9ebd6df8ac2a-3.15.0a3%2B-cf6758f-vs-base.md)[📈](results/bm-20251224-3.15.0a3%2B-cf6758f-NOGIL/bm-20251224-macm4pro-arm64-python-cf6758ff9ebd6df8ac2a-3.15.0a3%2B-cf6758f-vs-base.svg)[🧠](results/bm-20251224-3.15.0a3%2B-cf6758f-NOGIL/bm-20251224-macm4pro-arm64-python-cf6758ff9ebd6df8ac2a-3.15.0a3%2B-cf6758f-vs-base-mem.svg) |
| [2025-12-24](results/bm-20251224-3.15.0a3%2B-cf6758f) | python/cf6758ff9ebd6df8ac2a | cf6758f | 1.163x ↑<br>[📄](results/bm-20251224-3.15.0a3%2B-cf6758f/bm-20251224-macm4pro-arm64-python-cf6758ff9ebd6df8ac2a-3.15.0a3%2B-cf6758f-vs-3.12.6.md)[📈](results/bm-20251224-3.15.0a3%2B-cf6758f/bm-20251224-macm4pro-arm64-python-cf6758ff9ebd6df8ac2a-3.15.0a3%2B-cf6758f-vs-3.12.6.svg) | 1.078x ↑<br>[📄](results/bm-20251224-3.15.0a3%2B-cf6758f/bm-20251224-macm4pro-arm64-python-cf6758ff9ebd6df8ac2a-3.15.0a3%2B-cf6758f-vs-3.13.0rc2.md)[📈](results/bm-20251224-3.15.0a3%2B-cf6758f/bm-20251224-macm4pro-arm64-python-cf6758ff9ebd6df8ac2a-3.15.0a3%2B-cf6758f-vs-3.13.0rc2.svg) |  |
| [2025-12-23](results/bm-20251223-3.15.0a3%2B-cc48bf0-NOGIL) | python/cc48bf0fde8025d60a57 | cc48bf0 (NOGIL) | 1.093x ↑<br>[📄](results/bm-20251223-3.15.0a3%2B-cc48bf0-NOGIL/bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3%2B-cc48bf0-vs-3.12.6.md)[📈](results/bm-20251223-3.15.0a3%2B-cc48bf0-NOGIL/bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3%2B-cc48bf0-vs-3.12.6.svg) | 1.013x ↑<br>[📄](results/bm-20251223-3.15.0a3%2B-cc48bf0-NOGIL/bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3%2B-cc48bf0-vs-3.13.0rc2.md)[📈](results/bm-20251223-3.15.0a3%2B-cc48bf0-NOGIL/bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3%2B-cc48bf0-vs-3.13.0rc2.svg) | 1.045x ↓<br>[📄](results/bm-20251223-3.15.0a3%2B-cc48bf0-NOGIL/bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3%2B-cc48bf0-vs-base.md)[📈](results/bm-20251223-3.15.0a3%2B-cc48bf0-NOGIL/bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3%2B-cc48bf0-vs-base.svg)[🧠](results/bm-20251223-3.15.0a3%2B-cc48bf0-NOGIL/bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3%2B-cc48bf0-vs-base-mem.svg) |
| [2025-12-23](results/bm-20251223-3.15.0a3%2B-cc48bf0) | python/cc48bf0fde8025d60a57 | cc48bf0 | 1.144x ↑<br>[📄](results/bm-20251223-3.15.0a3%2B-cc48bf0/bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3%2B-cc48bf0-vs-3.12.6.md)[📈](results/bm-20251223-3.15.0a3%2B-cc48bf0/bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3%2B-cc48bf0-vs-3.12.6.svg) | 1.060x ↑<br>[📄](results/bm-20251223-3.15.0a3%2B-cc48bf0/bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3%2B-cc48bf0-vs-3.13.0rc2.md)[📈](results/bm-20251223-3.15.0a3%2B-cc48bf0/bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3%2B-cc48bf0-vs-3.13.0rc2.svg) |  |


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
