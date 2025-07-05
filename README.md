# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (5334732)](results/bm-20250628-3.15.0a0-5334732/bm-20250628-vultr-x86_64-python-5334732f9c8a44722e4b-3.15.0a0-5334732-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (5334732)](results/bm-20250628-3.15.0a0-5334732-PYTHON_UOPS/bm-20250628-vultr-x86_64-python-5334732f9c8a44722e4b-3.15.0a0-5334732-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-07-04](results/bm-20250704-3.15.0a0-d1d5dce-NOGIL) | python/d1d5dce14f90d777608e | d1d5dce (NOGIL) | 1.022x ↓<br>[📄](results/bm-20250704-3.15.0a0-d1d5dce-NOGIL/bm-20250704-vultr-x86_64-python-d1d5dce14f90d777608e-3.15.0a0-d1d5dce-vs-3.12.6.md)[📈](results/bm-20250704-3.15.0a0-d1d5dce-NOGIL/bm-20250704-vultr-x86_64-python-d1d5dce14f90d777608e-3.15.0a0-d1d5dce-vs-3.12.6.svg) | 1.054x ↓<br>[📄](results/bm-20250704-3.15.0a0-d1d5dce-NOGIL/bm-20250704-vultr-x86_64-python-d1d5dce14f90d777608e-3.15.0a0-d1d5dce-vs-3.13.0rc2.md)[📈](results/bm-20250704-3.15.0a0-d1d5dce-NOGIL/bm-20250704-vultr-x86_64-python-d1d5dce14f90d777608e-3.15.0a0-d1d5dce-vs-3.13.0rc2.svg) | 1.090x ↓<br>[📄](results/bm-20250704-3.15.0a0-d1d5dce-NOGIL/bm-20250704-vultr-x86_64-python-d1d5dce14f90d777608e-3.15.0a0-d1d5dce-vs-base.md)[📈](results/bm-20250704-3.15.0a0-d1d5dce-NOGIL/bm-20250704-vultr-x86_64-python-d1d5dce14f90d777608e-3.15.0a0-d1d5dce-vs-base.svg)[🧠](results/bm-20250704-3.15.0a0-d1d5dce-NOGIL/bm-20250704-vultr-x86_64-python-d1d5dce14f90d777608e-3.15.0a0-d1d5dce-vs-base-mem.svg) |
| [2025-07-04](results/bm-20250704-3.15.0a0-d1d5dce) | python/d1d5dce14f90d777608e | d1d5dce | 1.069x ↑<br>[📄](results/bm-20250704-3.15.0a0-d1d5dce/bm-20250704-vultr-x86_64-python-d1d5dce14f90d777608e-3.15.0a0-d1d5dce-vs-3.12.6.md)[📈](results/bm-20250704-3.15.0a0-d1d5dce/bm-20250704-vultr-x86_64-python-d1d5dce14f90d777608e-3.15.0a0-d1d5dce-vs-3.12.6.svg) | 1.033x ↑<br>[📄](results/bm-20250704-3.15.0a0-d1d5dce/bm-20250704-vultr-x86_64-python-d1d5dce14f90d777608e-3.15.0a0-d1d5dce-vs-3.13.0rc2.md)[📈](results/bm-20250704-3.15.0a0-d1d5dce/bm-20250704-vultr-x86_64-python-d1d5dce14f90d777608e-3.15.0a0-d1d5dce-vs-3.13.0rc2.svg) |  |
| [2025-07-03](results/bm-20250703-3.15.0a0-b499105-NOGIL) | python/b4991056f4f44acb50ae | b499105 (NOGIL) | 1.023x ↓<br>[📄](results/bm-20250703-3.15.0a0-b499105-NOGIL/bm-20250703-vultr-x86_64-python-b4991056f4f44acb50ae-3.15.0a0-b499105-vs-3.12.6.md)[📈](results/bm-20250703-3.15.0a0-b499105-NOGIL/bm-20250703-vultr-x86_64-python-b4991056f4f44acb50ae-3.15.0a0-b499105-vs-3.12.6.svg) | 1.055x ↓<br>[📄](results/bm-20250703-3.15.0a0-b499105-NOGIL/bm-20250703-vultr-x86_64-python-b4991056f4f44acb50ae-3.15.0a0-b499105-vs-3.13.0rc2.md)[📈](results/bm-20250703-3.15.0a0-b499105-NOGIL/bm-20250703-vultr-x86_64-python-b4991056f4f44acb50ae-3.15.0a0-b499105-vs-3.13.0rc2.svg) | 1.092x ↓<br>[📄](results/bm-20250703-3.15.0a0-b499105-NOGIL/bm-20250703-vultr-x86_64-python-b4991056f4f44acb50ae-3.15.0a0-b499105-vs-base.md)[📈](results/bm-20250703-3.15.0a0-b499105-NOGIL/bm-20250703-vultr-x86_64-python-b4991056f4f44acb50ae-3.15.0a0-b499105-vs-base.svg)[🧠](results/bm-20250703-3.15.0a0-b499105-NOGIL/bm-20250703-vultr-x86_64-python-b4991056f4f44acb50ae-3.15.0a0-b499105-vs-base-mem.svg) |
| [2025-07-03](results/bm-20250703-3.15.0a0-b499105) | python/b4991056f4f44acb50ae | b499105 | 1.070x ↑<br>[📄](results/bm-20250703-3.15.0a0-b499105/bm-20250703-vultr-x86_64-python-b4991056f4f44acb50ae-3.15.0a0-b499105-vs-3.12.6.md)[📈](results/bm-20250703-3.15.0a0-b499105/bm-20250703-vultr-x86_64-python-b4991056f4f44acb50ae-3.15.0a0-b499105-vs-3.12.6.svg) | 1.035x ↑<br>[📄](results/bm-20250703-3.15.0a0-b499105/bm-20250703-vultr-x86_64-python-b4991056f4f44acb50ae-3.15.0a0-b499105-vs-3.13.0rc2.md)[📈](results/bm-20250703-3.15.0a0-b499105/bm-20250703-vultr-x86_64-python-b4991056f4f44acb50ae-3.15.0a0-b499105-vs-3.13.0rc2.svg) |  |
| [2025-07-02](results/bm-20250702-3.15.0a0-7afe1ad-NOGIL) | python/7afe1adb0089d0f2df2a | 7afe1ad (NOGIL) | 1.021x ↓<br>[📄](results/bm-20250702-3.15.0a0-7afe1ad-NOGIL/bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad-vs-3.12.6.md)[📈](results/bm-20250702-3.15.0a0-7afe1ad-NOGIL/bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad-vs-3.12.6.svg) | 1.054x ↓<br>[📄](results/bm-20250702-3.15.0a0-7afe1ad-NOGIL/bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad-vs-3.13.0rc2.md)[📈](results/bm-20250702-3.15.0a0-7afe1ad-NOGIL/bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad-vs-3.13.0rc2.svg) | 1.092x ↓<br>[📄](results/bm-20250702-3.15.0a0-7afe1ad-NOGIL/bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad-vs-base.md)[📈](results/bm-20250702-3.15.0a0-7afe1ad-NOGIL/bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad-vs-base.svg)[🧠](results/bm-20250702-3.15.0a0-7afe1ad-NOGIL/bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad-vs-base-mem.svg) |
| [2025-07-02](results/bm-20250702-3.15.0a0-7afe1ad) | python/7afe1adb0089d0f2df2a | 7afe1ad | 1.071x ↑<br>[📄](results/bm-20250702-3.15.0a0-7afe1ad/bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad-vs-3.12.6.md)[📈](results/bm-20250702-3.15.0a0-7afe1ad/bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad-vs-3.12.6.svg) | 1.036x ↑<br>[📄](results/bm-20250702-3.15.0a0-7afe1ad/bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad-vs-3.13.0rc2.md)[📈](results/bm-20250702-3.15.0a0-7afe1ad/bm-20250702-vultr-x86_64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad-vs-3.13.0rc2.svg) |  |
| [2025-07-01](results/bm-20250701-3.15.0a0-f41e9c7-NOGIL) | python/f41e9c750e6971c165e0 | f41e9c7 (NOGIL) | 1.028x ↓<br>[📄](results/bm-20250701-3.15.0a0-f41e9c7-NOGIL/bm-20250701-vultr-x86_64-python-f41e9c750e6971c165e0-3.15.0a0-f41e9c7-vs-3.12.6.md)[📈](results/bm-20250701-3.15.0a0-f41e9c7-NOGIL/bm-20250701-vultr-x86_64-python-f41e9c750e6971c165e0-3.15.0a0-f41e9c7-vs-3.12.6.svg) | 1.060x ↓<br>[📄](results/bm-20250701-3.15.0a0-f41e9c7-NOGIL/bm-20250701-vultr-x86_64-python-f41e9c750e6971c165e0-3.15.0a0-f41e9c7-vs-3.13.0rc2.md)[📈](results/bm-20250701-3.15.0a0-f41e9c7-NOGIL/bm-20250701-vultr-x86_64-python-f41e9c750e6971c165e0-3.15.0a0-f41e9c7-vs-3.13.0rc2.svg) | 1.096x ↓<br>[📄](results/bm-20250701-3.15.0a0-f41e9c7-NOGIL/bm-20250701-vultr-x86_64-python-f41e9c750e6971c165e0-3.15.0a0-f41e9c7-vs-base.md)[📈](results/bm-20250701-3.15.0a0-f41e9c7-NOGIL/bm-20250701-vultr-x86_64-python-f41e9c750e6971c165e0-3.15.0a0-f41e9c7-vs-base.svg)[🧠](results/bm-20250701-3.15.0a0-f41e9c7-NOGIL/bm-20250701-vultr-x86_64-python-f41e9c750e6971c165e0-3.15.0a0-f41e9c7-vs-base-mem.svg) |
| [2025-07-01](results/bm-20250701-3.15.0a0-f41e9c7) | python/f41e9c750e6971c165e0 | f41e9c7 | 1.069x ↑<br>[📄](results/bm-20250701-3.15.0a0-f41e9c7/bm-20250701-vultr-x86_64-python-f41e9c750e6971c165e0-3.15.0a0-f41e9c7-vs-3.12.6.md)[📈](results/bm-20250701-3.15.0a0-f41e9c7/bm-20250701-vultr-x86_64-python-f41e9c750e6971c165e0-3.15.0a0-f41e9c7-vs-3.12.6.svg) | 1.034x ↑<br>[📄](results/bm-20250701-3.15.0a0-f41e9c7/bm-20250701-vultr-x86_64-python-f41e9c750e6971c165e0-3.15.0a0-f41e9c7-vs-3.13.0rc2.md)[📈](results/bm-20250701-3.15.0a0-f41e9c7/bm-20250701-vultr-x86_64-python-f41e9c750e6971c165e0-3.15.0a0-f41e9c7-vs-3.13.0rc2.svg) |  |
| [2025-06-25](results/bm-20250625-3.15.0a0-992ac08-JIT) | Fidget-Spinner/tos_caching_rebased_ | 992ac08 (JIT) | 1.116x ↑<br>[📄](results/bm-20250625-3.15.0a0-992ac08-JIT/bm-20250625-vultr-x86_64-Fidget%252dSpinner-tos_caching_rebased_-3.15.0a0-992ac08-vs-3.12.6.md)[📈](results/bm-20250625-3.15.0a0-992ac08-JIT/bm-20250625-vultr-x86_64-Fidget%252dSpinner-tos_caching_rebased_-3.15.0a0-992ac08-vs-3.12.6.svg) | 1.079x ↑<br>[📄](results/bm-20250625-3.15.0a0-992ac08-JIT/bm-20250625-vultr-x86_64-Fidget%252dSpinner-tos_caching_rebased_-3.15.0a0-992ac08-vs-3.13.0rc2.md)[📈](results/bm-20250625-3.15.0a0-992ac08-JIT/bm-20250625-vultr-x86_64-Fidget%252dSpinner-tos_caching_rebased_-3.15.0a0-992ac08-vs-3.13.0rc2.svg) | 1.003x ↑<br>[📄](results/bm-20250625-3.15.0a0-992ac08-JIT/bm-20250625-vultr-x86_64-Fidget%252dSpinner-tos_caching_rebased_-3.15.0a0-992ac08-vs-base.md)[📈](results/bm-20250625-3.15.0a0-992ac08-JIT/bm-20250625-vultr-x86_64-Fidget%252dSpinner-tos_caching_rebased_-3.15.0a0-992ac08-vs-base.svg)[🧠](results/bm-20250625-3.15.0a0-992ac08-JIT/bm-20250625-vultr-x86_64-Fidget%252dSpinner-tos_caching_rebased_-3.15.0a0-992ac08-vs-base-mem.svg) |
| [2025-06-24](results/bm-20250624-3.15.0a0-50081dc-JIT) | Fidget-Spinner/tos_caching_rebased | 50081dc (JIT) | 1.119x ↑<br>[📄](results/bm-20250624-3.15.0a0-50081dc-JIT/bm-20250624-vultr-x86_64-Fidget%252dSpinner-tos_caching_rebased-3.15.0a0-50081dc-vs-3.12.6.md)[📈](results/bm-20250624-3.15.0a0-50081dc-JIT/bm-20250624-vultr-x86_64-Fidget%252dSpinner-tos_caching_rebased-3.15.0a0-50081dc-vs-3.12.6.svg) | 1.082x ↑<br>[📄](results/bm-20250624-3.15.0a0-50081dc-JIT/bm-20250624-vultr-x86_64-Fidget%252dSpinner-tos_caching_rebased-3.15.0a0-50081dc-vs-3.13.0rc2.md)[📈](results/bm-20250624-3.15.0a0-50081dc-JIT/bm-20250624-vultr-x86_64-Fidget%252dSpinner-tos_caching_rebased-3.15.0a0-50081dc-vs-3.13.0rc2.svg) | 1.005x ↑<br>[📄](results/bm-20250624-3.15.0a0-50081dc-JIT/bm-20250624-vultr-x86_64-Fidget%252dSpinner-tos_caching_rebased-3.15.0a0-50081dc-vs-base.md)[📈](results/bm-20250624-3.15.0a0-50081dc-JIT/bm-20250624-vultr-x86_64-Fidget%252dSpinner-tos_caching_rebased-3.15.0a0-50081dc-vs-base.svg)[🧠](results/bm-20250624-3.15.0a0-50081dc-JIT/bm-20250624-vultr-x86_64-Fidget%252dSpinner-tos_caching_rebased-3.15.0a0-50081dc-vs-base-mem.svg) |
| [2025-06-24](results/bm-20250624-3.15.0a0-bda1218-JIT) | python/bda121862e7d7f4684d9 | bda1218 (JIT) | 1.113x ↑<br>[📄](results/bm-20250624-3.15.0a0-bda1218-JIT/bm-20250624-vultr-x86_64-python-bda121862e7d7f4684d9-3.15.0a0-bda1218-vs-3.12.6.md)[📈](results/bm-20250624-3.15.0a0-bda1218-JIT/bm-20250624-vultr-x86_64-python-bda121862e7d7f4684d9-3.15.0a0-bda1218-vs-3.12.6.svg) | 1.076x ↑<br>[📄](results/bm-20250624-3.15.0a0-bda1218-JIT/bm-20250624-vultr-x86_64-python-bda121862e7d7f4684d9-3.15.0a0-bda1218-vs-3.13.0rc2.md)[📈](results/bm-20250624-3.15.0a0-bda1218-JIT/bm-20250624-vultr-x86_64-python-bda121862e7d7f4684d9-3.15.0a0-bda1218-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-07-04](results/bm-20250704-3.15.0a0-d1d5dce-NOGIL) | python/d1d5dce14f90d777608e | d1d5dce (NOGIL) | 1.097x ↑<br>[📄](results/bm-20250704-3.15.0a0-d1d5dce-NOGIL/bm-20250704-macm4pro-arm64-python-d1d5dce14f90d777608e-3.15.0a0-d1d5dce-vs-3.12.6.md)[📈](results/bm-20250704-3.15.0a0-d1d5dce-NOGIL/bm-20250704-macm4pro-arm64-python-d1d5dce14f90d777608e-3.15.0a0-d1d5dce-vs-3.12.6.svg) | 1.018x ↑<br>[📄](results/bm-20250704-3.15.0a0-d1d5dce-NOGIL/bm-20250704-macm4pro-arm64-python-d1d5dce14f90d777608e-3.15.0a0-d1d5dce-vs-3.13.0rc2.md)[📈](results/bm-20250704-3.15.0a0-d1d5dce-NOGIL/bm-20250704-macm4pro-arm64-python-d1d5dce14f90d777608e-3.15.0a0-d1d5dce-vs-3.13.0rc2.svg) | 1.006x ↑<br>[📄](results/bm-20250704-3.15.0a0-d1d5dce-NOGIL/bm-20250704-macm4pro-arm64-python-d1d5dce14f90d777608e-3.15.0a0-d1d5dce-vs-base.md)[📈](results/bm-20250704-3.15.0a0-d1d5dce-NOGIL/bm-20250704-macm4pro-arm64-python-d1d5dce14f90d777608e-3.15.0a0-d1d5dce-vs-base.svg)[🧠](results/bm-20250704-3.15.0a0-d1d5dce-NOGIL/bm-20250704-macm4pro-arm64-python-d1d5dce14f90d777608e-3.15.0a0-d1d5dce-vs-base-mem.svg) |
| [2025-07-04](results/bm-20250704-3.15.0a0-d1d5dce) | python/d1d5dce14f90d777608e | d1d5dce | 1.089x ↑<br>[📄](results/bm-20250704-3.15.0a0-d1d5dce/bm-20250704-macm4pro-arm64-python-d1d5dce14f90d777608e-3.15.0a0-d1d5dce-vs-3.12.6.md)[📈](results/bm-20250704-3.15.0a0-d1d5dce/bm-20250704-macm4pro-arm64-python-d1d5dce14f90d777608e-3.15.0a0-d1d5dce-vs-3.12.6.svg) | 1.011x ↑<br>[📄](results/bm-20250704-3.15.0a0-d1d5dce/bm-20250704-macm4pro-arm64-python-d1d5dce14f90d777608e-3.15.0a0-d1d5dce-vs-3.13.0rc2.md)[📈](results/bm-20250704-3.15.0a0-d1d5dce/bm-20250704-macm4pro-arm64-python-d1d5dce14f90d777608e-3.15.0a0-d1d5dce-vs-3.13.0rc2.svg) |  |
| [2025-07-03](results/bm-20250703-3.15.0a0-b499105-NOGIL) | python/b4991056f4f44acb50ae | b499105 (NOGIL) | 1.098x ↑<br>[📄](results/bm-20250703-3.15.0a0-b499105-NOGIL/bm-20250703-macm4pro-arm64-python-b4991056f4f44acb50ae-3.15.0a0-b499105-vs-3.12.6.md)[📈](results/bm-20250703-3.15.0a0-b499105-NOGIL/bm-20250703-macm4pro-arm64-python-b4991056f4f44acb50ae-3.15.0a0-b499105-vs-3.12.6.svg) | 1.019x ↑<br>[📄](results/bm-20250703-3.15.0a0-b499105-NOGIL/bm-20250703-macm4pro-arm64-python-b4991056f4f44acb50ae-3.15.0a0-b499105-vs-3.13.0rc2.md)[📈](results/bm-20250703-3.15.0a0-b499105-NOGIL/bm-20250703-macm4pro-arm64-python-b4991056f4f44acb50ae-3.15.0a0-b499105-vs-3.13.0rc2.svg) | 1.009x ↑<br>[📄](results/bm-20250703-3.15.0a0-b499105-NOGIL/bm-20250703-macm4pro-arm64-python-b4991056f4f44acb50ae-3.15.0a0-b499105-vs-base.md)[📈](results/bm-20250703-3.15.0a0-b499105-NOGIL/bm-20250703-macm4pro-arm64-python-b4991056f4f44acb50ae-3.15.0a0-b499105-vs-base.svg)[🧠](results/bm-20250703-3.15.0a0-b499105-NOGIL/bm-20250703-macm4pro-arm64-python-b4991056f4f44acb50ae-3.15.0a0-b499105-vs-base-mem.svg) |
| [2025-07-03](results/bm-20250703-3.15.0a0-b499105) | python/b4991056f4f44acb50ae | b499105 | 1.087x ↑<br>[📄](results/bm-20250703-3.15.0a0-b499105/bm-20250703-macm4pro-arm64-python-b4991056f4f44acb50ae-3.15.0a0-b499105-vs-3.12.6.md)[📈](results/bm-20250703-3.15.0a0-b499105/bm-20250703-macm4pro-arm64-python-b4991056f4f44acb50ae-3.15.0a0-b499105-vs-3.12.6.svg) | 1.008x ↑<br>[📄](results/bm-20250703-3.15.0a0-b499105/bm-20250703-macm4pro-arm64-python-b4991056f4f44acb50ae-3.15.0a0-b499105-vs-3.13.0rc2.md)[📈](results/bm-20250703-3.15.0a0-b499105/bm-20250703-macm4pro-arm64-python-b4991056f4f44acb50ae-3.15.0a0-b499105-vs-3.13.0rc2.svg) |  |
| [2025-07-02](results/bm-20250702-3.15.0a0-7afe1ad-NOGIL) | python/7afe1adb0089d0f2df2a | 7afe1ad (NOGIL) | 1.087x ↑<br>[📄](results/bm-20250702-3.15.0a0-7afe1ad-NOGIL/bm-20250702-macm4pro-arm64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad-vs-3.12.6.md)[📈](results/bm-20250702-3.15.0a0-7afe1ad-NOGIL/bm-20250702-macm4pro-arm64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad-vs-3.12.6.svg) | 1.008x ↑<br>[📄](results/bm-20250702-3.15.0a0-7afe1ad-NOGIL/bm-20250702-macm4pro-arm64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad-vs-3.13.0rc2.md)[📈](results/bm-20250702-3.15.0a0-7afe1ad-NOGIL/bm-20250702-macm4pro-arm64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad-vs-3.13.0rc2.svg) | 1.014x ↓<br>[📄](results/bm-20250702-3.15.0a0-7afe1ad-NOGIL/bm-20250702-macm4pro-arm64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad-vs-base.md)[📈](results/bm-20250702-3.15.0a0-7afe1ad-NOGIL/bm-20250702-macm4pro-arm64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad-vs-base.svg)[🧠](results/bm-20250702-3.15.0a0-7afe1ad-NOGIL/bm-20250702-macm4pro-arm64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad-vs-base-mem.svg) |
| [2025-07-02](results/bm-20250702-3.15.0a0-7afe1ad) | python/7afe1adb0089d0f2df2a | 7afe1ad | 1.100x ↑<br>[📄](results/bm-20250702-3.15.0a0-7afe1ad/bm-20250702-macm4pro-arm64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad-vs-3.12.6.md)[📈](results/bm-20250702-3.15.0a0-7afe1ad/bm-20250702-macm4pro-arm64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad-vs-3.12.6.svg) | 1.020x ↑<br>[📄](results/bm-20250702-3.15.0a0-7afe1ad/bm-20250702-macm4pro-arm64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad-vs-3.13.0rc2.md)[📈](results/bm-20250702-3.15.0a0-7afe1ad/bm-20250702-macm4pro-arm64-python-7afe1adb0089d0f2df2a-3.15.0a0-7afe1ad-vs-3.13.0rc2.svg) |  |
| [2025-07-01](results/bm-20250701-3.15.0a0-f41e9c7-NOGIL) | python/f41e9c750e6971c165e0 | f41e9c7 (NOGIL) | 1.091x ↑<br>[📄](results/bm-20250701-3.15.0a0-f41e9c7-NOGIL/bm-20250701-macm4pro-arm64-python-f41e9c750e6971c165e0-3.15.0a0-f41e9c7-vs-3.12.6.md)[📈](results/bm-20250701-3.15.0a0-f41e9c7-NOGIL/bm-20250701-macm4pro-arm64-python-f41e9c750e6971c165e0-3.15.0a0-f41e9c7-vs-3.12.6.svg) | 1.012x ↑<br>[📄](results/bm-20250701-3.15.0a0-f41e9c7-NOGIL/bm-20250701-macm4pro-arm64-python-f41e9c750e6971c165e0-3.15.0a0-f41e9c7-vs-3.13.0rc2.md)[📈](results/bm-20250701-3.15.0a0-f41e9c7-NOGIL/bm-20250701-macm4pro-arm64-python-f41e9c750e6971c165e0-3.15.0a0-f41e9c7-vs-3.13.0rc2.svg) | 1.005x ↑<br>[📄](results/bm-20250701-3.15.0a0-f41e9c7-NOGIL/bm-20250701-macm4pro-arm64-python-f41e9c750e6971c165e0-3.15.0a0-f41e9c7-vs-base.md)[📈](results/bm-20250701-3.15.0a0-f41e9c7-NOGIL/bm-20250701-macm4pro-arm64-python-f41e9c750e6971c165e0-3.15.0a0-f41e9c7-vs-base.svg)[🧠](results/bm-20250701-3.15.0a0-f41e9c7-NOGIL/bm-20250701-macm4pro-arm64-python-f41e9c750e6971c165e0-3.15.0a0-f41e9c7-vs-base-mem.svg) |
| [2025-07-01](results/bm-20250701-3.15.0a0-f41e9c7) | python/f41e9c750e6971c165e0 | f41e9c7 | 1.084x ↑<br>[📄](results/bm-20250701-3.15.0a0-f41e9c7/bm-20250701-macm4pro-arm64-python-f41e9c750e6971c165e0-3.15.0a0-f41e9c7-vs-3.12.6.md)[📈](results/bm-20250701-3.15.0a0-f41e9c7/bm-20250701-macm4pro-arm64-python-f41e9c750e6971c165e0-3.15.0a0-f41e9c7-vs-3.12.6.svg) | 1.006x ↑<br>[📄](results/bm-20250701-3.15.0a0-f41e9c7/bm-20250701-macm4pro-arm64-python-f41e9c750e6971c165e0-3.15.0a0-f41e9c7-vs-3.13.0rc2.md)[📈](results/bm-20250701-3.15.0a0-f41e9c7/bm-20250701-macm4pro-arm64-python-f41e9c750e6971c165e0-3.15.0a0-f41e9c7-vs-3.13.0rc2.svg) |  |


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
