# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (235fa72)](results/bm-20260412-3.15.0a8%2B-235fa72/bm-20260412-vultr-x86_64-python-235fa7244a0474c492ae-3.15.0a8%2B-235fa72-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (235fa72)](results/bm-20260412-3.15.0a8%2B-235fa72-PYTHON_UOPS/bm-20260412-vultr-x86_64-python-235fa7244a0474c492ae-3.15.0a8%2B-235fa72-pystats.md)
- [Most recent JIT pystats on main (bedaea0)](results/bm-20251019-3.15.0a1%2B-bedaea0-JIT/bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-04-17](results/bm-20260417-3.15.0a8%2B-2a07ff9-NOGIL) | python/2a07ff980b412559f6ce | 2a07ff9 (NOGIL) | 1.011x ↓<br>[📄](results/bm-20260417-3.15.0a8%2B-2a07ff9-NOGIL/bm-20260417-vultr-x86_64-python-2a07ff980b412559f6ce-3.15.0a8%2B-2a07ff9-vs-3.12.6.md)[📈](results/bm-20260417-3.15.0a8%2B-2a07ff9-NOGIL/bm-20260417-vultr-x86_64-python-2a07ff980b412559f6ce-3.15.0a8%2B-2a07ff9-vs-3.12.6.svg) | 1.044x ↓<br>[📄](results/bm-20260417-3.15.0a8%2B-2a07ff9-NOGIL/bm-20260417-vultr-x86_64-python-2a07ff980b412559f6ce-3.15.0a8%2B-2a07ff9-vs-3.13.0rc2.md)[📈](results/bm-20260417-3.15.0a8%2B-2a07ff9-NOGIL/bm-20260417-vultr-x86_64-python-2a07ff980b412559f6ce-3.15.0a8%2B-2a07ff9-vs-3.13.0rc2.svg) | 1.091x ↓<br>[📄](results/bm-20260417-3.15.0a8%2B-2a07ff9-NOGIL/bm-20260417-vultr-x86_64-python-2a07ff980b412559f6ce-3.15.0a8%2B-2a07ff9-vs-base.md)[📈](results/bm-20260417-3.15.0a8%2B-2a07ff9-NOGIL/bm-20260417-vultr-x86_64-python-2a07ff980b412559f6ce-3.15.0a8%2B-2a07ff9-vs-base.svg)[🧠](results/bm-20260417-3.15.0a8%2B-2a07ff9-NOGIL/bm-20260417-vultr-x86_64-python-2a07ff980b412559f6ce-3.15.0a8%2B-2a07ff9-vs-base-mem.svg) |
| [2026-04-17](results/bm-20260417-3.15.0a8%2B-2a07ff9) | python/2a07ff980b412559f6ce | 2a07ff9 | 1.084x ↑<br>[📄](results/bm-20260417-3.15.0a8%2B-2a07ff9/bm-20260417-vultr-x86_64-python-2a07ff980b412559f6ce-3.15.0a8%2B-2a07ff9-vs-3.12.6.md)[📈](results/bm-20260417-3.15.0a8%2B-2a07ff9/bm-20260417-vultr-x86_64-python-2a07ff980b412559f6ce-3.15.0a8%2B-2a07ff9-vs-3.12.6.svg) | 1.047x ↑<br>[📄](results/bm-20260417-3.15.0a8%2B-2a07ff9/bm-20260417-vultr-x86_64-python-2a07ff980b412559f6ce-3.15.0a8%2B-2a07ff9-vs-3.13.0rc2.md)[📈](results/bm-20260417-3.15.0a8%2B-2a07ff9/bm-20260417-vultr-x86_64-python-2a07ff980b412559f6ce-3.15.0a8%2B-2a07ff9-vs-3.13.0rc2.svg) |  |
| [2026-04-15](results/bm-20260415-3.15.0a8%2B-54607ee-NOGIL) | python/54607eec34b42d377a12 | 54607ee (NOGIL) | 1.012x ↓<br>[📄](results/bm-20260415-3.15.0a8%2B-54607ee-NOGIL/bm-20260415-vultr-x86_64-python-54607eec34b42d377a12-3.15.0a8%2B-54607ee-vs-3.12.6.md)[📈](results/bm-20260415-3.15.0a8%2B-54607ee-NOGIL/bm-20260415-vultr-x86_64-python-54607eec34b42d377a12-3.15.0a8%2B-54607ee-vs-3.12.6.svg) | 1.045x ↓<br>[📄](results/bm-20260415-3.15.0a8%2B-54607ee-NOGIL/bm-20260415-vultr-x86_64-python-54607eec34b42d377a12-3.15.0a8%2B-54607ee-vs-3.13.0rc2.md)[📈](results/bm-20260415-3.15.0a8%2B-54607ee-NOGIL/bm-20260415-vultr-x86_64-python-54607eec34b42d377a12-3.15.0a8%2B-54607ee-vs-3.13.0rc2.svg) | 1.091x ↓<br>[📄](results/bm-20260415-3.15.0a8%2B-54607ee-NOGIL/bm-20260415-vultr-x86_64-python-54607eec34b42d377a12-3.15.0a8%2B-54607ee-vs-base.md)[📈](results/bm-20260415-3.15.0a8%2B-54607ee-NOGIL/bm-20260415-vultr-x86_64-python-54607eec34b42d377a12-3.15.0a8%2B-54607ee-vs-base.svg)[🧠](results/bm-20260415-3.15.0a8%2B-54607ee-NOGIL/bm-20260415-vultr-x86_64-python-54607eec34b42d377a12-3.15.0a8%2B-54607ee-vs-base-mem.svg) |
| [2026-04-15](results/bm-20260415-3.15.0a8%2B-54607ee) | python/54607eec34b42d377a12 | 54607ee | 1.082x ↑<br>[📄](results/bm-20260415-3.15.0a8%2B-54607ee/bm-20260415-vultr-x86_64-python-54607eec34b42d377a12-3.15.0a8%2B-54607ee-vs-3.12.6.md)[📈](results/bm-20260415-3.15.0a8%2B-54607ee/bm-20260415-vultr-x86_64-python-54607eec34b42d377a12-3.15.0a8%2B-54607ee-vs-3.12.6.svg) | 1.046x ↑<br>[📄](results/bm-20260415-3.15.0a8%2B-54607ee/bm-20260415-vultr-x86_64-python-54607eec34b42d377a12-3.15.0a8%2B-54607ee-vs-3.13.0rc2.md)[📈](results/bm-20260415-3.15.0a8%2B-54607ee/bm-20260415-vultr-x86_64-python-54607eec34b42d377a12-3.15.0a8%2B-54607ee-vs-3.13.0rc2.svg) |  |
| [2026-04-14](results/bm-20260414-3.15.0a8%2B-d0e7c6a-NOGIL) | python/d0e7c6acc936a171d05b | d0e7c6a (NOGIL) | 1.015x ↓<br>[📄](results/bm-20260414-3.15.0a8%2B-d0e7c6a-NOGIL/bm-20260414-vultr-x86_64-python-d0e7c6acc936a171d05b-3.15.0a8%2B-d0e7c6a-vs-3.12.6.md)[📈](results/bm-20260414-3.15.0a8%2B-d0e7c6a-NOGIL/bm-20260414-vultr-x86_64-python-d0e7c6acc936a171d05b-3.15.0a8%2B-d0e7c6a-vs-3.12.6.svg) | 1.048x ↓<br>[📄](results/bm-20260414-3.15.0a8%2B-d0e7c6a-NOGIL/bm-20260414-vultr-x86_64-python-d0e7c6acc936a171d05b-3.15.0a8%2B-d0e7c6a-vs-3.13.0rc2.md)[📈](results/bm-20260414-3.15.0a8%2B-d0e7c6a-NOGIL/bm-20260414-vultr-x86_64-python-d0e7c6acc936a171d05b-3.15.0a8%2B-d0e7c6a-vs-3.13.0rc2.svg) | 1.094x ↓<br>[📄](results/bm-20260414-3.15.0a8%2B-d0e7c6a-NOGIL/bm-20260414-vultr-x86_64-python-d0e7c6acc936a171d05b-3.15.0a8%2B-d0e7c6a-vs-base.md)[📈](results/bm-20260414-3.15.0a8%2B-d0e7c6a-NOGIL/bm-20260414-vultr-x86_64-python-d0e7c6acc936a171d05b-3.15.0a8%2B-d0e7c6a-vs-base.svg)[🧠](results/bm-20260414-3.15.0a8%2B-d0e7c6a-NOGIL/bm-20260414-vultr-x86_64-python-d0e7c6acc936a171d05b-3.15.0a8%2B-d0e7c6a-vs-base-mem.svg) |
| [2026-04-14](results/bm-20260414-3.15.0a8%2B-d0e7c6a) | python/d0e7c6acc936a171d05b | d0e7c6a | 1.082x ↑<br>[📄](results/bm-20260414-3.15.0a8%2B-d0e7c6a/bm-20260414-vultr-x86_64-python-d0e7c6acc936a171d05b-3.15.0a8%2B-d0e7c6a-vs-3.12.6.md)[📈](results/bm-20260414-3.15.0a8%2B-d0e7c6a/bm-20260414-vultr-x86_64-python-d0e7c6acc936a171d05b-3.15.0a8%2B-d0e7c6a-vs-3.12.6.svg) | 1.046x ↑<br>[📄](results/bm-20260414-3.15.0a8%2B-d0e7c6a/bm-20260414-vultr-x86_64-python-d0e7c6acc936a171d05b-3.15.0a8%2B-d0e7c6a-vs-3.13.0rc2.md)[📈](results/bm-20260414-3.15.0a8%2B-d0e7c6a/bm-20260414-vultr-x86_64-python-d0e7c6acc936a171d05b-3.15.0a8%2B-d0e7c6a-vs-3.13.0rc2.svg) |  |
| [2026-04-13](results/bm-20260413-3.15.0a8%2B-eb4c78d-NOGIL) | python/eb4c78df07c87237f97e | eb4c78d (NOGIL) | 1.026x ↓<br>[📄](results/bm-20260413-3.15.0a8%2B-eb4c78d-NOGIL/bm-20260413-vultr-x86_64-python-eb4c78df07c87237f97e-3.15.0a8%2B-eb4c78d-vs-3.12.6.md)[📈](results/bm-20260413-3.15.0a8%2B-eb4c78d-NOGIL/bm-20260413-vultr-x86_64-python-eb4c78df07c87237f97e-3.15.0a8%2B-eb4c78d-vs-3.12.6.svg) | 1.059x ↓<br>[📄](results/bm-20260413-3.15.0a8%2B-eb4c78d-NOGIL/bm-20260413-vultr-x86_64-python-eb4c78df07c87237f97e-3.15.0a8%2B-eb4c78d-vs-3.13.0rc2.md)[📈](results/bm-20260413-3.15.0a8%2B-eb4c78d-NOGIL/bm-20260413-vultr-x86_64-python-eb4c78df07c87237f97e-3.15.0a8%2B-eb4c78d-vs-3.13.0rc2.svg) | 1.089x ↓<br>[📄](results/bm-20260413-3.15.0a8%2B-eb4c78d-NOGIL/bm-20260413-vultr-x86_64-python-eb4c78df07c87237f97e-3.15.0a8%2B-eb4c78d-vs-base.md)[📈](results/bm-20260413-3.15.0a8%2B-eb4c78d-NOGIL/bm-20260413-vultr-x86_64-python-eb4c78df07c87237f97e-3.15.0a8%2B-eb4c78d-vs-base.svg)[🧠](results/bm-20260413-3.15.0a8%2B-eb4c78d-NOGIL/bm-20260413-vultr-x86_64-python-eb4c78df07c87237f97e-3.15.0a8%2B-eb4c78d-vs-base-mem.svg) |
| [2026-04-13](results/bm-20260413-3.15.0a8%2B-eb4c78d) | python/eb4c78df07c87237f97e | eb4c78d | 1.064x ↑<br>[📄](results/bm-20260413-3.15.0a8%2B-eb4c78d/bm-20260413-vultr-x86_64-python-eb4c78df07c87237f97e-3.15.0a8%2B-eb4c78d-vs-3.12.6.md)[📈](results/bm-20260413-3.15.0a8%2B-eb4c78d/bm-20260413-vultr-x86_64-python-eb4c78df07c87237f97e-3.15.0a8%2B-eb4c78d-vs-3.12.6.svg) | 1.028x ↑<br>[📄](results/bm-20260413-3.15.0a8%2B-eb4c78d/bm-20260413-vultr-x86_64-python-eb4c78df07c87237f97e-3.15.0a8%2B-eb4c78d-vs-3.13.0rc2.md)[📈](results/bm-20260413-3.15.0a8%2B-eb4c78d/bm-20260413-vultr-x86_64-python-eb4c78df07c87237f97e-3.15.0a8%2B-eb4c78d-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-04-17](results/bm-20260417-3.15.0a8%2B-2a07ff9-NOGIL) | python/2a07ff980b412559f6ce | 2a07ff9 (NOGIL) | 1.106x ↑<br>[📄](results/bm-20260417-3.15.0a8%2B-2a07ff9-NOGIL/bm-20260417-macm4pro-arm64-python-2a07ff980b412559f6ce-3.15.0a8%2B-2a07ff9-vs-3.12.6.md)[📈](results/bm-20260417-3.15.0a8%2B-2a07ff9-NOGIL/bm-20260417-macm4pro-arm64-python-2a07ff980b412559f6ce-3.15.0a8%2B-2a07ff9-vs-3.12.6.svg) | 1.026x ↑<br>[📄](results/bm-20260417-3.15.0a8%2B-2a07ff9-NOGIL/bm-20260417-macm4pro-arm64-python-2a07ff980b412559f6ce-3.15.0a8%2B-2a07ff9-vs-3.13.0rc2.md)[📈](results/bm-20260417-3.15.0a8%2B-2a07ff9-NOGIL/bm-20260417-macm4pro-arm64-python-2a07ff980b412559f6ce-3.15.0a8%2B-2a07ff9-vs-3.13.0rc2.svg) | 1.028x ↓<br>[📄](results/bm-20260417-3.15.0a8%2B-2a07ff9-NOGIL/bm-20260417-macm4pro-arm64-python-2a07ff980b412559f6ce-3.15.0a8%2B-2a07ff9-vs-base.md)[📈](results/bm-20260417-3.15.0a8%2B-2a07ff9-NOGIL/bm-20260417-macm4pro-arm64-python-2a07ff980b412559f6ce-3.15.0a8%2B-2a07ff9-vs-base.svg)[🧠](results/bm-20260417-3.15.0a8%2B-2a07ff9-NOGIL/bm-20260417-macm4pro-arm64-python-2a07ff980b412559f6ce-3.15.0a8%2B-2a07ff9-vs-base-mem.svg) |
| [2026-04-17](results/bm-20260417-3.15.0a8%2B-2a07ff9) | python/2a07ff980b412559f6ce | 2a07ff9 | 1.138x ↑<br>[📄](results/bm-20260417-3.15.0a8%2B-2a07ff9/bm-20260417-macm4pro-arm64-python-2a07ff980b412559f6ce-3.15.0a8%2B-2a07ff9-vs-3.12.6.md)[📈](results/bm-20260417-3.15.0a8%2B-2a07ff9/bm-20260417-macm4pro-arm64-python-2a07ff980b412559f6ce-3.15.0a8%2B-2a07ff9-vs-3.12.6.svg) | 1.055x ↑<br>[📄](results/bm-20260417-3.15.0a8%2B-2a07ff9/bm-20260417-macm4pro-arm64-python-2a07ff980b412559f6ce-3.15.0a8%2B-2a07ff9-vs-3.13.0rc2.md)[📈](results/bm-20260417-3.15.0a8%2B-2a07ff9/bm-20260417-macm4pro-arm64-python-2a07ff980b412559f6ce-3.15.0a8%2B-2a07ff9-vs-3.13.0rc2.svg) |  |
| [2026-04-15](results/bm-20260415-3.15.0a8%2B-54607ee-NOGIL) | python/54607eec34b42d377a12 | 54607ee (NOGIL) | 1.103x ↑<br>[📄](results/bm-20260415-3.15.0a8%2B-54607ee-NOGIL/bm-20260415-macm4pro-arm64-python-54607eec34b42d377a12-3.15.0a8%2B-54607ee-vs-3.12.6.md)[📈](results/bm-20260415-3.15.0a8%2B-54607ee-NOGIL/bm-20260415-macm4pro-arm64-python-54607eec34b42d377a12-3.15.0a8%2B-54607ee-vs-3.12.6.svg) | 1.023x ↑<br>[📄](results/bm-20260415-3.15.0a8%2B-54607ee-NOGIL/bm-20260415-macm4pro-arm64-python-54607eec34b42d377a12-3.15.0a8%2B-54607ee-vs-3.13.0rc2.md)[📈](results/bm-20260415-3.15.0a8%2B-54607ee-NOGIL/bm-20260415-macm4pro-arm64-python-54607eec34b42d377a12-3.15.0a8%2B-54607ee-vs-3.13.0rc2.svg) | 1.056x ↓<br>[📄](results/bm-20260415-3.15.0a8%2B-54607ee-NOGIL/bm-20260415-macm4pro-arm64-python-54607eec34b42d377a12-3.15.0a8%2B-54607ee-vs-base.md)[📈](results/bm-20260415-3.15.0a8%2B-54607ee-NOGIL/bm-20260415-macm4pro-arm64-python-54607eec34b42d377a12-3.15.0a8%2B-54607ee-vs-base.svg)[🧠](results/bm-20260415-3.15.0a8%2B-54607ee-NOGIL/bm-20260415-macm4pro-arm64-python-54607eec34b42d377a12-3.15.0a8%2B-54607ee-vs-base-mem.svg) |
| [2026-04-15](results/bm-20260415-3.15.0a8%2B-54607ee) | python/54607eec34b42d377a12 | 54607ee | 1.168x ↑<br>[📄](results/bm-20260415-3.15.0a8%2B-54607ee/bm-20260415-macm4pro-arm64-python-54607eec34b42d377a12-3.15.0a8%2B-54607ee-vs-3.12.6.md)[📈](results/bm-20260415-3.15.0a8%2B-54607ee/bm-20260415-macm4pro-arm64-python-54607eec34b42d377a12-3.15.0a8%2B-54607ee-vs-3.12.6.svg) | 1.083x ↑<br>[📄](results/bm-20260415-3.15.0a8%2B-54607ee/bm-20260415-macm4pro-arm64-python-54607eec34b42d377a12-3.15.0a8%2B-54607ee-vs-3.13.0rc2.md)[📈](results/bm-20260415-3.15.0a8%2B-54607ee/bm-20260415-macm4pro-arm64-python-54607eec34b42d377a12-3.15.0a8%2B-54607ee-vs-3.13.0rc2.svg) |  |
| [2026-04-14](results/bm-20260414-3.15.0a8%2B-d0e7c6a-NOGIL) | python/d0e7c6acc936a171d05b | d0e7c6a (NOGIL) | 1.100x ↑<br>[📄](results/bm-20260414-3.15.0a8%2B-d0e7c6a-NOGIL/bm-20260414-macm4pro-arm64-python-d0e7c6acc936a171d05b-3.15.0a8%2B-d0e7c6a-vs-3.12.6.md)[📈](results/bm-20260414-3.15.0a8%2B-d0e7c6a-NOGIL/bm-20260414-macm4pro-arm64-python-d0e7c6acc936a171d05b-3.15.0a8%2B-d0e7c6a-vs-3.12.6.svg) | 1.020x ↑<br>[📄](results/bm-20260414-3.15.0a8%2B-d0e7c6a-NOGIL/bm-20260414-macm4pro-arm64-python-d0e7c6acc936a171d05b-3.15.0a8%2B-d0e7c6a-vs-3.13.0rc2.md)[📈](results/bm-20260414-3.15.0a8%2B-d0e7c6a-NOGIL/bm-20260414-macm4pro-arm64-python-d0e7c6acc936a171d05b-3.15.0a8%2B-d0e7c6a-vs-3.13.0rc2.svg) | 1.058x ↓<br>[📄](results/bm-20260414-3.15.0a8%2B-d0e7c6a-NOGIL/bm-20260414-macm4pro-arm64-python-d0e7c6acc936a171d05b-3.15.0a8%2B-d0e7c6a-vs-base.md)[📈](results/bm-20260414-3.15.0a8%2B-d0e7c6a-NOGIL/bm-20260414-macm4pro-arm64-python-d0e7c6acc936a171d05b-3.15.0a8%2B-d0e7c6a-vs-base.svg)[🧠](results/bm-20260414-3.15.0a8%2B-d0e7c6a-NOGIL/bm-20260414-macm4pro-arm64-python-d0e7c6acc936a171d05b-3.15.0a8%2B-d0e7c6a-vs-base-mem.svg) |
| [2026-04-14](results/bm-20260414-3.15.0a8%2B-d0e7c6a) | python/d0e7c6acc936a171d05b | d0e7c6a | 1.167x ↑<br>[📄](results/bm-20260414-3.15.0a8%2B-d0e7c6a/bm-20260414-macm4pro-arm64-python-d0e7c6acc936a171d05b-3.15.0a8%2B-d0e7c6a-vs-3.12.6.md)[📈](results/bm-20260414-3.15.0a8%2B-d0e7c6a/bm-20260414-macm4pro-arm64-python-d0e7c6acc936a171d05b-3.15.0a8%2B-d0e7c6a-vs-3.12.6.svg) | 1.083x ↑<br>[📄](results/bm-20260414-3.15.0a8%2B-d0e7c6a/bm-20260414-macm4pro-arm64-python-d0e7c6acc936a171d05b-3.15.0a8%2B-d0e7c6a-vs-3.13.0rc2.md)[📈](results/bm-20260414-3.15.0a8%2B-d0e7c6a/bm-20260414-macm4pro-arm64-python-d0e7c6acc936a171d05b-3.15.0a8%2B-d0e7c6a-vs-3.13.0rc2.svg) |  |
| [2026-04-13](results/bm-20260413-3.15.0a8%2B-eb4c78d-NOGIL) | python/eb4c78df07c87237f97e | eb4c78d (NOGIL) | 1.091x ↑<br>[📄](results/bm-20260413-3.15.0a8%2B-eb4c78d-NOGIL/bm-20260413-macm4pro-arm64-python-eb4c78df07c87237f97e-3.15.0a8%2B-eb4c78d-vs-3.12.6.md)[📈](results/bm-20260413-3.15.0a8%2B-eb4c78d-NOGIL/bm-20260413-macm4pro-arm64-python-eb4c78df07c87237f97e-3.15.0a8%2B-eb4c78d-vs-3.12.6.svg) | 1.012x ↑<br>[📄](results/bm-20260413-3.15.0a8%2B-eb4c78d-NOGIL/bm-20260413-macm4pro-arm64-python-eb4c78df07c87237f97e-3.15.0a8%2B-eb4c78d-vs-3.13.0rc2.md)[📈](results/bm-20260413-3.15.0a8%2B-eb4c78d-NOGIL/bm-20260413-macm4pro-arm64-python-eb4c78df07c87237f97e-3.15.0a8%2B-eb4c78d-vs-3.13.0rc2.svg) | 1.052x ↓<br>[📄](results/bm-20260413-3.15.0a8%2B-eb4c78d-NOGIL/bm-20260413-macm4pro-arm64-python-eb4c78df07c87237f97e-3.15.0a8%2B-eb4c78d-vs-base.md)[📈](results/bm-20260413-3.15.0a8%2B-eb4c78d-NOGIL/bm-20260413-macm4pro-arm64-python-eb4c78df07c87237f97e-3.15.0a8%2B-eb4c78d-vs-base.svg)[🧠](results/bm-20260413-3.15.0a8%2B-eb4c78d-NOGIL/bm-20260413-macm4pro-arm64-python-eb4c78df07c87237f97e-3.15.0a8%2B-eb4c78d-vs-base-mem.svg) |
| [2026-04-13](results/bm-20260413-3.15.0a8%2B-eb4c78d) | python/eb4c78df07c87237f97e | eb4c78d | 1.150x ↑<br>[📄](results/bm-20260413-3.15.0a8%2B-eb4c78d/bm-20260413-macm4pro-arm64-python-eb4c78df07c87237f97e-3.15.0a8%2B-eb4c78d-vs-3.12.6.md)[📈](results/bm-20260413-3.15.0a8%2B-eb4c78d/bm-20260413-macm4pro-arm64-python-eb4c78df07c87237f97e-3.15.0a8%2B-eb4c78d-vs-3.12.6.svg) | 1.067x ↑<br>[📄](results/bm-20260413-3.15.0a8%2B-eb4c78d/bm-20260413-macm4pro-arm64-python-eb4c78df07c87237f97e-3.15.0a8%2B-eb4c78d-vs-3.13.0rc2.md)[📈](results/bm-20260413-3.15.0a8%2B-eb4c78d/bm-20260413-macm4pro-arm64-python-eb4c78df07c87237f97e-3.15.0a8%2B-eb4c78d-vs-3.13.0rc2.svg) |  |


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
