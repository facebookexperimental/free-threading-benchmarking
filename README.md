# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (6b632ce)](results/bm-20260502-3.15.0a8%2B-6b632ce/bm-20260502-vultr-x86_64-python-6b632ce36b950c7753c5-3.15.0a8%2B-6b632ce-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (6b632ce)](results/bm-20260502-3.15.0a8%2B-6b632ce-PYTHON_UOPS/bm-20260502-vultr-x86_64-python-6b632ce36b950c7753c5-3.15.0a8%2B-6b632ce-pystats.md)
- [Most recent JIT pystats on main (bedaea0)](results/bm-20251019-3.15.0a1%2B-bedaea0-JIT/bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-05-07](results/bm-20260507-3.16.0a0-49918f5-NOGIL) | python/49918f5b0ceb1950c322 | 49918f5 (NOGIL) | 1.037x ↓<br>[📄](results/bm-20260507-3.16.0a0-49918f5-NOGIL/bm-20260507-vultr-x86_64-python-49918f5b0ceb1950c322-3.16.0a0-49918f5-vs-3.12.6.md)[📈](results/bm-20260507-3.16.0a0-49918f5-NOGIL/bm-20260507-vultr-x86_64-python-49918f5b0ceb1950c322-3.16.0a0-49918f5-vs-3.12.6.svg) | 1.072x ↓<br>[📄](results/bm-20260507-3.16.0a0-49918f5-NOGIL/bm-20260507-vultr-x86_64-python-49918f5b0ceb1950c322-3.16.0a0-49918f5-vs-3.13.0rc2.md)[📈](results/bm-20260507-3.16.0a0-49918f5-NOGIL/bm-20260507-vultr-x86_64-python-49918f5b0ceb1950c322-3.16.0a0-49918f5-vs-3.13.0rc2.svg) | 1.090x ↓<br>[📄](results/bm-20260507-3.16.0a0-49918f5-NOGIL/bm-20260507-vultr-x86_64-python-49918f5b0ceb1950c322-3.16.0a0-49918f5-vs-base.md)[📈](results/bm-20260507-3.16.0a0-49918f5-NOGIL/bm-20260507-vultr-x86_64-python-49918f5b0ceb1950c322-3.16.0a0-49918f5-vs-base.svg)[🧠](results/bm-20260507-3.16.0a0-49918f5-NOGIL/bm-20260507-vultr-x86_64-python-49918f5b0ceb1950c322-3.16.0a0-49918f5-vs-base-mem.svg) |
| [2026-05-07](results/bm-20260507-3.16.0a0-49918f5) | python/49918f5b0ceb1950c322 | 49918f5 | 1.053x ↑<br>[📄](results/bm-20260507-3.16.0a0-49918f5/bm-20260507-vultr-x86_64-python-49918f5b0ceb1950c322-3.16.0a0-49918f5-vs-3.12.6.md)[📈](results/bm-20260507-3.16.0a0-49918f5/bm-20260507-vultr-x86_64-python-49918f5b0ceb1950c322-3.16.0a0-49918f5-vs-3.12.6.svg) | 1.015x ↑<br>[📄](results/bm-20260507-3.16.0a0-49918f5/bm-20260507-vultr-x86_64-python-49918f5b0ceb1950c322-3.16.0a0-49918f5-vs-3.13.0rc2.md)[📈](results/bm-20260507-3.16.0a0-49918f5/bm-20260507-vultr-x86_64-python-49918f5b0ceb1950c322-3.16.0a0-49918f5-vs-3.13.0rc2.svg) |  |
| [2026-05-06](results/bm-20260506-3.15.0a8%2B-2b7c28a-NOGIL) | python/2b7c28a4406da1b26dd0 | 2b7c28a (NOGIL) | 1.018x ↓<br>[📄](results/bm-20260506-3.15.0a8%2B-2b7c28a-NOGIL/bm-20260506-vultr-x86_64-python-2b7c28a4406da1b26dd0-3.15.0a8%2B-2b7c28a-vs-3.12.6.md)[📈](results/bm-20260506-3.15.0a8%2B-2b7c28a-NOGIL/bm-20260506-vultr-x86_64-python-2b7c28a4406da1b26dd0-3.15.0a8%2B-2b7c28a-vs-3.12.6.svg) | 1.053x ↓<br>[📄](results/bm-20260506-3.15.0a8%2B-2b7c28a-NOGIL/bm-20260506-vultr-x86_64-python-2b7c28a4406da1b26dd0-3.15.0a8%2B-2b7c28a-vs-3.13.0rc2.md)[📈](results/bm-20260506-3.15.0a8%2B-2b7c28a-NOGIL/bm-20260506-vultr-x86_64-python-2b7c28a4406da1b26dd0-3.15.0a8%2B-2b7c28a-vs-3.13.0rc2.svg) | 1.069x ↓<br>[📄](results/bm-20260506-3.15.0a8%2B-2b7c28a-NOGIL/bm-20260506-vultr-x86_64-python-2b7c28a4406da1b26dd0-3.15.0a8%2B-2b7c28a-vs-base.md)[📈](results/bm-20260506-3.15.0a8%2B-2b7c28a-NOGIL/bm-20260506-vultr-x86_64-python-2b7c28a4406da1b26dd0-3.15.0a8%2B-2b7c28a-vs-base.svg)[🧠](results/bm-20260506-3.15.0a8%2B-2b7c28a-NOGIL/bm-20260506-vultr-x86_64-python-2b7c28a4406da1b26dd0-3.15.0a8%2B-2b7c28a-vs-base-mem.svg) |
| [2026-05-06](results/bm-20260506-3.15.0a8%2B-2b7c28a) | python/2b7c28a4406da1b26dd0 | 2b7c28a | 1.048x ↑<br>[📄](results/bm-20260506-3.15.0a8%2B-2b7c28a/bm-20260506-vultr-x86_64-python-2b7c28a4406da1b26dd0-3.15.0a8%2B-2b7c28a-vs-3.12.6.md)[📈](results/bm-20260506-3.15.0a8%2B-2b7c28a/bm-20260506-vultr-x86_64-python-2b7c28a4406da1b26dd0-3.15.0a8%2B-2b7c28a-vs-3.12.6.svg) | 1.011x ↑<br>[📄](results/bm-20260506-3.15.0a8%2B-2b7c28a/bm-20260506-vultr-x86_64-python-2b7c28a4406da1b26dd0-3.15.0a8%2B-2b7c28a-vs-3.13.0rc2.md)[📈](results/bm-20260506-3.15.0a8%2B-2b7c28a/bm-20260506-vultr-x86_64-python-2b7c28a4406da1b26dd0-3.15.0a8%2B-2b7c28a-vs-3.13.0rc2.svg) |  |
| [2026-05-05](results/bm-20260505-3.15.0a8%2B-17975f9-NOGIL) | python/17975f92edd2a6a84549 | 17975f9 (NOGIL) | 1.017x ↓<br>[📄](results/bm-20260505-3.15.0a8%2B-17975f9-NOGIL/bm-20260505-vultr-x86_64-python-17975f92edd2a6a84549-3.15.0a8%2B-17975f9-vs-3.12.6.md)[📈](results/bm-20260505-3.15.0a8%2B-17975f9-NOGIL/bm-20260505-vultr-x86_64-python-17975f92edd2a6a84549-3.15.0a8%2B-17975f9-vs-3.12.6.svg) | 1.053x ↓<br>[📄](results/bm-20260505-3.15.0a8%2B-17975f9-NOGIL/bm-20260505-vultr-x86_64-python-17975f92edd2a6a84549-3.15.0a8%2B-17975f9-vs-3.13.0rc2.md)[📈](results/bm-20260505-3.15.0a8%2B-17975f9-NOGIL/bm-20260505-vultr-x86_64-python-17975f92edd2a6a84549-3.15.0a8%2B-17975f9-vs-3.13.0rc2.svg) | 1.078x ↓<br>[📄](results/bm-20260505-3.15.0a8%2B-17975f9-NOGIL/bm-20260505-vultr-x86_64-python-17975f92edd2a6a84549-3.15.0a8%2B-17975f9-vs-base.md)[📈](results/bm-20260505-3.15.0a8%2B-17975f9-NOGIL/bm-20260505-vultr-x86_64-python-17975f92edd2a6a84549-3.15.0a8%2B-17975f9-vs-base.svg)[🧠](results/bm-20260505-3.15.0a8%2B-17975f9-NOGIL/bm-20260505-vultr-x86_64-python-17975f92edd2a6a84549-3.15.0a8%2B-17975f9-vs-base-mem.svg) |
| [2026-05-05](results/bm-20260505-3.15.0a8%2B-17975f9) | python/17975f92edd2a6a84549 | 17975f9 | 1.059x ↑<br>[📄](results/bm-20260505-3.15.0a8%2B-17975f9/bm-20260505-vultr-x86_64-python-17975f92edd2a6a84549-3.15.0a8%2B-17975f9-vs-3.12.6.md)[📈](results/bm-20260505-3.15.0a8%2B-17975f9/bm-20260505-vultr-x86_64-python-17975f92edd2a6a84549-3.15.0a8%2B-17975f9-vs-3.12.6.svg) | 1.021x ↑<br>[📄](results/bm-20260505-3.15.0a8%2B-17975f9/bm-20260505-vultr-x86_64-python-17975f92edd2a6a84549-3.15.0a8%2B-17975f9-vs-3.13.0rc2.md)[📈](results/bm-20260505-3.15.0a8%2B-17975f9/bm-20260505-vultr-x86_64-python-17975f92edd2a6a84549-3.15.0a8%2B-17975f9-vs-3.13.0rc2.svg) |  |
| [2026-05-05](results/bm-20260505-3.15.0a8%2B-24aa562-NOGIL) | python/24aa562062fced910e8b | 24aa562 (NOGIL) | 1.020x ↓<br>[📄](results/bm-20260505-3.15.0a8%2B-24aa562-NOGIL/bm-20260505-vultr-x86_64-python-24aa562062fced910e8b-3.15.0a8%2B-24aa562-vs-3.12.6.md)[📈](results/bm-20260505-3.15.0a8%2B-24aa562-NOGIL/bm-20260505-vultr-x86_64-python-24aa562062fced910e8b-3.15.0a8%2B-24aa562-vs-3.12.6.svg) | 1.055x ↓<br>[📄](results/bm-20260505-3.15.0a8%2B-24aa562-NOGIL/bm-20260505-vultr-x86_64-python-24aa562062fced910e8b-3.15.0a8%2B-24aa562-vs-3.13.0rc2.md)[📈](results/bm-20260505-3.15.0a8%2B-24aa562-NOGIL/bm-20260505-vultr-x86_64-python-24aa562062fced910e8b-3.15.0a8%2B-24aa562-vs-3.13.0rc2.svg) |  |
| [2026-05-05](results/bm-20260505-3.15.0a8%2B-67a2a66-NOGIL) | nascheme/gc_ft_adapt | 67a2a66 (NOGIL) | 1.023x ↓<br>[📄](results/bm-20260505-3.15.0a8%2B-67a2a66-NOGIL/bm-20260505-vultr-x86_64-nascheme-gc_ft_adapt-3.15.0a8%2B-67a2a66-vs-3.12.6.md)[📈](results/bm-20260505-3.15.0a8%2B-67a2a66-NOGIL/bm-20260505-vultr-x86_64-nascheme-gc_ft_adapt-3.15.0a8%2B-67a2a66-vs-3.12.6.svg) | 1.058x ↓<br>[📄](results/bm-20260505-3.15.0a8%2B-67a2a66-NOGIL/bm-20260505-vultr-x86_64-nascheme-gc_ft_adapt-3.15.0a8%2B-67a2a66-vs-3.13.0rc2.md)[📈](results/bm-20260505-3.15.0a8%2B-67a2a66-NOGIL/bm-20260505-vultr-x86_64-nascheme-gc_ft_adapt-3.15.0a8%2B-67a2a66-vs-3.13.0rc2.svg) | 1.004x ↓<br>[📄](results/bm-20260505-3.15.0a8%2B-67a2a66-NOGIL/bm-20260505-vultr-x86_64-nascheme-gc_ft_adapt-3.15.0a8%2B-67a2a66-vs-base.md)[📈](results/bm-20260505-3.15.0a8%2B-67a2a66-NOGIL/bm-20260505-vultr-x86_64-nascheme-gc_ft_adapt-3.15.0a8%2B-67a2a66-vs-base.svg)[🧠](results/bm-20260505-3.15.0a8%2B-67a2a66-NOGIL/bm-20260505-vultr-x86_64-nascheme-gc_ft_adapt-3.15.0a8%2B-67a2a66-vs-base-mem.svg) |
| [2026-05-05](results/bm-20260505-3.15.0a8%2B-04ce318-NOGIL) | python/04ce31852260b3d39e35 | 04ce318 (NOGIL) | 1.022x ↓<br>[📄](results/bm-20260505-3.15.0a8%2B-04ce318-NOGIL/bm-20260505-vultr-x86_64-python-04ce31852260b3d39e35-3.15.0a8%2B-04ce318-vs-3.12.6.md)[📈](results/bm-20260505-3.15.0a8%2B-04ce318-NOGIL/bm-20260505-vultr-x86_64-python-04ce31852260b3d39e35-3.15.0a8%2B-04ce318-vs-3.12.6.svg) | 1.057x ↓<br>[📄](results/bm-20260505-3.15.0a8%2B-04ce318-NOGIL/bm-20260505-vultr-x86_64-python-04ce31852260b3d39e35-3.15.0a8%2B-04ce318-vs-3.13.0rc2.md)[📈](results/bm-20260505-3.15.0a8%2B-04ce318-NOGIL/bm-20260505-vultr-x86_64-python-04ce31852260b3d39e35-3.15.0a8%2B-04ce318-vs-3.13.0rc2.svg) | 1.080x ↓<br>[📄](results/bm-20260505-3.15.0a8%2B-04ce318-NOGIL/bm-20260505-vultr-x86_64-python-04ce31852260b3d39e35-3.15.0a8%2B-04ce318-vs-base.md)[📈](results/bm-20260505-3.15.0a8%2B-04ce318-NOGIL/bm-20260505-vultr-x86_64-python-04ce31852260b3d39e35-3.15.0a8%2B-04ce318-vs-base.svg)[🧠](results/bm-20260505-3.15.0a8%2B-04ce318-NOGIL/bm-20260505-vultr-x86_64-python-04ce31852260b3d39e35-3.15.0a8%2B-04ce318-vs-base-mem.svg) |
| [2026-05-05](results/bm-20260505-3.15.0a8%2B-04ce318) | python/04ce31852260b3d39e35 | 04ce318 | 1.058x ↑<br>[📄](results/bm-20260505-3.15.0a8%2B-04ce318/bm-20260505-vultr-x86_64-python-04ce31852260b3d39e35-3.15.0a8%2B-04ce318-vs-3.12.6.md)[📈](results/bm-20260505-3.15.0a8%2B-04ce318/bm-20260505-vultr-x86_64-python-04ce31852260b3d39e35-3.15.0a8%2B-04ce318-vs-3.12.6.svg) | 1.020x ↑<br>[📄](results/bm-20260505-3.15.0a8%2B-04ce318/bm-20260505-vultr-x86_64-python-04ce31852260b3d39e35-3.15.0a8%2B-04ce318-vs-3.13.0rc2.md)[📈](results/bm-20260505-3.15.0a8%2B-04ce318/bm-20260505-vultr-x86_64-python-04ce31852260b3d39e35-3.15.0a8%2B-04ce318-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2026-05-07](results/bm-20260507-3.16.0a0-49918f5-NOGIL) | python/49918f5b0ceb1950c322 | 49918f5 (NOGIL) | 1.090x ↑<br>[📄](results/bm-20260507-3.16.0a0-49918f5-NOGIL/bm-20260507-macm4pro-arm64-python-49918f5b0ceb1950c322-3.16.0a0-49918f5-vs-3.12.6.md)[📈](results/bm-20260507-3.16.0a0-49918f5-NOGIL/bm-20260507-macm4pro-arm64-python-49918f5b0ceb1950c322-3.16.0a0-49918f5-vs-3.12.6.svg) | 1.006x ↑<br>[📄](results/bm-20260507-3.16.0a0-49918f5-NOGIL/bm-20260507-macm4pro-arm64-python-49918f5b0ceb1950c322-3.16.0a0-49918f5-vs-3.13.0rc2.md)[📈](results/bm-20260507-3.16.0a0-49918f5-NOGIL/bm-20260507-macm4pro-arm64-python-49918f5b0ceb1950c322-3.16.0a0-49918f5-vs-3.13.0rc2.svg) | 1.022x ↓<br>[📄](results/bm-20260507-3.16.0a0-49918f5-NOGIL/bm-20260507-macm4pro-arm64-python-49918f5b0ceb1950c322-3.16.0a0-49918f5-vs-base.md)[📈](results/bm-20260507-3.16.0a0-49918f5-NOGIL/bm-20260507-macm4pro-arm64-python-49918f5b0ceb1950c322-3.16.0a0-49918f5-vs-base.svg)[🧠](results/bm-20260507-3.16.0a0-49918f5-NOGIL/bm-20260507-macm4pro-arm64-python-49918f5b0ceb1950c322-3.16.0a0-49918f5-vs-base-mem.svg) |
| [2026-05-07](results/bm-20260507-3.16.0a0-49918f5) | python/49918f5b0ceb1950c322 | 49918f5 | 1.113x ↑<br>[📄](results/bm-20260507-3.16.0a0-49918f5/bm-20260507-macm4pro-arm64-python-49918f5b0ceb1950c322-3.16.0a0-49918f5-vs-3.12.6.md)[📈](results/bm-20260507-3.16.0a0-49918f5/bm-20260507-macm4pro-arm64-python-49918f5b0ceb1950c322-3.16.0a0-49918f5-vs-3.12.6.svg) | 1.028x ↑<br>[📄](results/bm-20260507-3.16.0a0-49918f5/bm-20260507-macm4pro-arm64-python-49918f5b0ceb1950c322-3.16.0a0-49918f5-vs-3.13.0rc2.md)[📈](results/bm-20260507-3.16.0a0-49918f5/bm-20260507-macm4pro-arm64-python-49918f5b0ceb1950c322-3.16.0a0-49918f5-vs-3.13.0rc2.svg) |  |
| [2026-05-06](results/bm-20260506-3.15.0a8%2B-2b7c28a-NOGIL) | python/2b7c28a4406da1b26dd0 | 2b7c28a (NOGIL) | 1.130x ↑<br>[📄](results/bm-20260506-3.15.0a8%2B-2b7c28a-NOGIL/bm-20260506-macm4pro-arm64-python-2b7c28a4406da1b26dd0-3.15.0a8%2B-2b7c28a-vs-3.12.6.md)[📈](results/bm-20260506-3.15.0a8%2B-2b7c28a-NOGIL/bm-20260506-macm4pro-arm64-python-2b7c28a4406da1b26dd0-3.15.0a8%2B-2b7c28a-vs-3.12.6.svg) | 1.044x ↑<br>[📄](results/bm-20260506-3.15.0a8%2B-2b7c28a-NOGIL/bm-20260506-macm4pro-arm64-python-2b7c28a4406da1b26dd0-3.15.0a8%2B-2b7c28a-vs-3.13.0rc2.md)[📈](results/bm-20260506-3.15.0a8%2B-2b7c28a-NOGIL/bm-20260506-macm4pro-arm64-python-2b7c28a4406da1b26dd0-3.15.0a8%2B-2b7c28a-vs-3.13.0rc2.svg) | 1.025x ↓<br>[📄](results/bm-20260506-3.15.0a8%2B-2b7c28a-NOGIL/bm-20260506-macm4pro-arm64-python-2b7c28a4406da1b26dd0-3.15.0a8%2B-2b7c28a-vs-base.md)[📈](results/bm-20260506-3.15.0a8%2B-2b7c28a-NOGIL/bm-20260506-macm4pro-arm64-python-2b7c28a4406da1b26dd0-3.15.0a8%2B-2b7c28a-vs-base.svg)[🧠](results/bm-20260506-3.15.0a8%2B-2b7c28a-NOGIL/bm-20260506-macm4pro-arm64-python-2b7c28a4406da1b26dd0-3.15.0a8%2B-2b7c28a-vs-base-mem.svg) |
| [2026-05-06](results/bm-20260506-3.15.0a8%2B-2b7c28a) | python/2b7c28a4406da1b26dd0 | 2b7c28a | 1.156x ↑<br>[📄](results/bm-20260506-3.15.0a8%2B-2b7c28a/bm-20260506-macm4pro-arm64-python-2b7c28a4406da1b26dd0-3.15.0a8%2B-2b7c28a-vs-3.12.6.md)[📈](results/bm-20260506-3.15.0a8%2B-2b7c28a/bm-20260506-macm4pro-arm64-python-2b7c28a4406da1b26dd0-3.15.0a8%2B-2b7c28a-vs-3.12.6.svg) | 1.068x ↑<br>[📄](results/bm-20260506-3.15.0a8%2B-2b7c28a/bm-20260506-macm4pro-arm64-python-2b7c28a4406da1b26dd0-3.15.0a8%2B-2b7c28a-vs-3.13.0rc2.md)[📈](results/bm-20260506-3.15.0a8%2B-2b7c28a/bm-20260506-macm4pro-arm64-python-2b7c28a4406da1b26dd0-3.15.0a8%2B-2b7c28a-vs-3.13.0rc2.svg) |  |
| [2026-05-05](results/bm-20260505-3.15.0a8%2B-17975f9) | python/17975f92edd2a6a84549 | 17975f9 | 1.148x ↑<br>[📄](results/bm-20260505-3.15.0a8%2B-17975f9/bm-20260505-macm4pro-arm64-python-17975f92edd2a6a84549-3.15.0a8%2B-17975f9-vs-3.12.6.md)[📈](results/bm-20260505-3.15.0a8%2B-17975f9/bm-20260505-macm4pro-arm64-python-17975f92edd2a6a84549-3.15.0a8%2B-17975f9-vs-3.12.6.svg) | 1.060x ↑<br>[📄](results/bm-20260505-3.15.0a8%2B-17975f9/bm-20260505-macm4pro-arm64-python-17975f92edd2a6a84549-3.15.0a8%2B-17975f9-vs-3.13.0rc2.md)[📈](results/bm-20260505-3.15.0a8%2B-17975f9/bm-20260505-macm4pro-arm64-python-17975f92edd2a6a84549-3.15.0a8%2B-17975f9-vs-3.13.0rc2.svg) |  |
| [2026-05-05](results/bm-20260505-3.15.0a8%2B-04ce318-NOGIL) | python/04ce31852260b3d39e35 | 04ce318 (NOGIL) | 1.113x ↑<br>[📄](results/bm-20260505-3.15.0a8%2B-04ce318-NOGIL/bm-20260505-macm4pro-arm64-python-04ce31852260b3d39e35-3.15.0a8%2B-04ce318-vs-3.12.6.md)[📈](results/bm-20260505-3.15.0a8%2B-04ce318-NOGIL/bm-20260505-macm4pro-arm64-python-04ce31852260b3d39e35-3.15.0a8%2B-04ce318-vs-3.12.6.svg) | 1.028x ↑<br>[📄](results/bm-20260505-3.15.0a8%2B-04ce318-NOGIL/bm-20260505-macm4pro-arm64-python-04ce31852260b3d39e35-3.15.0a8%2B-04ce318-vs-3.13.0rc2.md)[📈](results/bm-20260505-3.15.0a8%2B-04ce318-NOGIL/bm-20260505-macm4pro-arm64-python-04ce31852260b3d39e35-3.15.0a8%2B-04ce318-vs-3.13.0rc2.svg) | 1.027x ↓<br>[📄](results/bm-20260505-3.15.0a8%2B-04ce318-NOGIL/bm-20260505-macm4pro-arm64-python-04ce31852260b3d39e35-3.15.0a8%2B-04ce318-vs-base.md)[📈](results/bm-20260505-3.15.0a8%2B-04ce318-NOGIL/bm-20260505-macm4pro-arm64-python-04ce31852260b3d39e35-3.15.0a8%2B-04ce318-vs-base.svg)[🧠](results/bm-20260505-3.15.0a8%2B-04ce318-NOGIL/bm-20260505-macm4pro-arm64-python-04ce31852260b3d39e35-3.15.0a8%2B-04ce318-vs-base-mem.svg) |
| [2026-05-05](results/bm-20260505-3.15.0a8%2B-04ce318) | python/04ce31852260b3d39e35 | 04ce318 | 1.142x ↑<br>[📄](results/bm-20260505-3.15.0a8%2B-04ce318/bm-20260505-macm4pro-arm64-python-04ce31852260b3d39e35-3.15.0a8%2B-04ce318-vs-3.12.6.md)[📈](results/bm-20260505-3.15.0a8%2B-04ce318/bm-20260505-macm4pro-arm64-python-04ce31852260b3d39e35-3.15.0a8%2B-04ce318-vs-3.12.6.svg) | 1.054x ↑<br>[📄](results/bm-20260505-3.15.0a8%2B-04ce318/bm-20260505-macm4pro-arm64-python-04ce31852260b3d39e35-3.15.0a8%2B-04ce318-vs-3.13.0rc2.md)[📈](results/bm-20260505-3.15.0a8%2B-04ce318/bm-20260505-macm4pro-arm64-python-04ce31852260b3d39e35-3.15.0a8%2B-04ce318-vs-3.13.0rc2.svg) |  |


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
