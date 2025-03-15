# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (a3990df)](results/bm-20250308-3.14.0a5%2B-a3990df/bm-20250308-linux-x86_64-python-a3990df6121880e8c678-3.14.0a5%2B-a3990df-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (c9932a9)](results/bm-20250301-3.14.0a5%2B-c9932a9-PYTHON_UOPS/bm-20250301-linux-x86_64-python-c9932a9ec8a3077933a8-3.14.0a5%2B-c9932a9-pystats.md)

## linux x86_64 (linux)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-03-14](results/bm-20250314-3.14.0a6%2B-55815a6-NOGIL) | python/55815a6474c59001f023 | 55815a6 (NOGIL) | 1.026x ↓<br>[📄](results/bm-20250314-3.14.0a6%2B-55815a6-NOGIL/bm-20250314-linux-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-3.12.6.md)[📈](results/bm-20250314-3.14.0a6%2B-55815a6-NOGIL/bm-20250314-linux-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-3.12.6.svg) | 1.063x ↓<br>[📄](results/bm-20250314-3.14.0a6%2B-55815a6-NOGIL/bm-20250314-linux-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-3.13.0rc2.md)[📈](results/bm-20250314-3.14.0a6%2B-55815a6-NOGIL/bm-20250314-linux-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-3.13.0rc2.svg) | 1.105x ↓<br>[📄](results/bm-20250314-3.14.0a6%2B-55815a6-NOGIL/bm-20250314-linux-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-base.md)[📈](results/bm-20250314-3.14.0a6%2B-55815a6-NOGIL/bm-20250314-linux-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-base.svg)[🧠](results/bm-20250314-3.14.0a6%2B-55815a6-NOGIL/bm-20250314-linux-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-base-mem.svg) |
| [2025-03-14](results/bm-20250314-3.14.0a6%2B-55815a6) | python/55815a6474c59001f023 | 55815a6 | 1.093x ↑<br>[📄](results/bm-20250314-3.14.0a6%2B-55815a6/bm-20250314-linux-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-3.12.6.md)[📈](results/bm-20250314-3.14.0a6%2B-55815a6/bm-20250314-linux-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-3.12.6.svg) | 1.051x ↑<br>[📄](results/bm-20250314-3.14.0a6%2B-55815a6/bm-20250314-linux-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-3.13.0rc2.md)[📈](results/bm-20250314-3.14.0a6%2B-55815a6/bm-20250314-linux-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-3.13.0rc2.svg) |  |
| [2025-03-14](results/bm-20250314-3.14.0a5%2B-f3e275f-NOGIL) | python/f3e275f1a92c0f668b13 | f3e275f (NOGIL) | 1.045x ↓<br>[📄](results/bm-20250314-3.14.0a5%2B-f3e275f-NOGIL/bm-20250314-linux-x86_64-python-f3e275f1a92c0f668b13-3.14.0a5%2B-f3e275f-vs-3.12.6.md)[📈](results/bm-20250314-3.14.0a5%2B-f3e275f-NOGIL/bm-20250314-linux-x86_64-python-f3e275f1a92c0f668b13-3.14.0a5%2B-f3e275f-vs-3.12.6.svg) | 1.078x ↓<br>[📄](results/bm-20250314-3.14.0a5%2B-f3e275f-NOGIL/bm-20250314-linux-x86_64-python-f3e275f1a92c0f668b13-3.14.0a5%2B-f3e275f-vs-3.13.0rc2.md)[📈](results/bm-20250314-3.14.0a5%2B-f3e275f-NOGIL/bm-20250314-linux-x86_64-python-f3e275f1a92c0f668b13-3.14.0a5%2B-f3e275f-vs-3.13.0rc2.svg) | 1.099x ↓<br>[📄](results/bm-20250314-3.14.0a5%2B-f3e275f-NOGIL/bm-20250314-linux-x86_64-python-f3e275f1a92c0f668b13-3.14.0a5%2B-f3e275f-vs-base.md)[📈](results/bm-20250314-3.14.0a5%2B-f3e275f-NOGIL/bm-20250314-linux-x86_64-python-f3e275f1a92c0f668b13-3.14.0a5%2B-f3e275f-vs-base.svg)[🧠](results/bm-20250314-3.14.0a5%2B-f3e275f-NOGIL/bm-20250314-linux-x86_64-python-f3e275f1a92c0f668b13-3.14.0a5%2B-f3e275f-vs-base-mem.svg) |
| [2025-03-14](results/bm-20250314-3.14.0a5%2B-f3e275f) | python/f3e275f1a92c0f668b13 | f3e275f | 1.062x ↑<br>[📄](results/bm-20250314-3.14.0a5%2B-f3e275f/bm-20250314-linux-x86_64-python-f3e275f1a92c0f668b13-3.14.0a5%2B-f3e275f-vs-3.12.6.md)[📈](results/bm-20250314-3.14.0a5%2B-f3e275f/bm-20250314-linux-x86_64-python-f3e275f1a92c0f668b13-3.14.0a5%2B-f3e275f-vs-3.12.6.svg) | 1.022x ↑<br>[📄](results/bm-20250314-3.14.0a5%2B-f3e275f/bm-20250314-linux-x86_64-python-f3e275f1a92c0f668b13-3.14.0a5%2B-f3e275f-vs-3.13.0rc2.md)[📈](results/bm-20250314-3.14.0a5%2B-f3e275f/bm-20250314-linux-x86_64-python-f3e275f1a92c0f668b13-3.14.0a5%2B-f3e275f-vs-3.13.0rc2.svg) |  |
| [2025-03-12](results/bm-20250312-3.14.0a5%2B-3618240-NOGIL) | python/3618240624d98de2a68a | 3618240 (NOGIL) | 1.050x ↓<br>[📄](results/bm-20250312-3.14.0a5%2B-3618240-NOGIL/bm-20250312-linux-x86_64-python-3618240624d98de2a68a-3.14.0a5%2B-3618240-vs-3.12.6.md)[📈](results/bm-20250312-3.14.0a5%2B-3618240-NOGIL/bm-20250312-linux-x86_64-python-3618240624d98de2a68a-3.14.0a5%2B-3618240-vs-3.12.6.svg) | 1.085x ↓<br>[📄](results/bm-20250312-3.14.0a5%2B-3618240-NOGIL/bm-20250312-linux-x86_64-python-3618240624d98de2a68a-3.14.0a5%2B-3618240-vs-3.13.0rc2.md)[📈](results/bm-20250312-3.14.0a5%2B-3618240-NOGIL/bm-20250312-linux-x86_64-python-3618240624d98de2a68a-3.14.0a5%2B-3618240-vs-3.13.0rc2.svg) | 1.103x ↓<br>[📄](results/bm-20250312-3.14.0a5%2B-3618240-NOGIL/bm-20250312-linux-x86_64-python-3618240624d98de2a68a-3.14.0a5%2B-3618240-vs-base.md)[📈](results/bm-20250312-3.14.0a5%2B-3618240-NOGIL/bm-20250312-linux-x86_64-python-3618240624d98de2a68a-3.14.0a5%2B-3618240-vs-base.svg)[🧠](results/bm-20250312-3.14.0a5%2B-3618240-NOGIL/bm-20250312-linux-x86_64-python-3618240624d98de2a68a-3.14.0a5%2B-3618240-vs-base-mem.svg) |
| [2025-03-12](results/bm-20250312-3.14.0a5%2B-3618240) | python/3618240624d98de2a68a | 3618240 | 1.060x ↑<br>[📄](results/bm-20250312-3.14.0a5%2B-3618240/bm-20250312-linux-x86_64-python-3618240624d98de2a68a-3.14.0a5%2B-3618240-vs-3.12.6.md)[📈](results/bm-20250312-3.14.0a5%2B-3618240/bm-20250312-linux-x86_64-python-3618240624d98de2a68a-3.14.0a5%2B-3618240-vs-3.12.6.svg) | 1.023x ↑<br>[📄](results/bm-20250312-3.14.0a5%2B-3618240/bm-20250312-linux-x86_64-python-3618240624d98de2a68a-3.14.0a5%2B-3618240-vs-3.13.0rc2.md)[📈](results/bm-20250312-3.14.0a5%2B-3618240/bm-20250312-linux-x86_64-python-3618240624d98de2a68a-3.14.0a5%2B-3618240-vs-3.13.0rc2.svg) |  |
| [2025-03-11](results/bm-20250311-3.14.0a5%2B-ebc24d5-NOGIL) | python/ebc24d54bcf554403e9b | ebc24d5 (NOGIL) | 1.037x ↓<br>[📄](results/bm-20250311-3.14.0a5%2B-ebc24d5-NOGIL/bm-20250311-linux-x86_64-python-ebc24d54bcf554403e9b-3.14.0a5%2B-ebc24d5-vs-3.12.6.md)[📈](results/bm-20250311-3.14.0a5%2B-ebc24d5-NOGIL/bm-20250311-linux-x86_64-python-ebc24d54bcf554403e9b-3.14.0a5%2B-ebc24d5-vs-3.12.6.svg) | 1.072x ↓<br>[📄](results/bm-20250311-3.14.0a5%2B-ebc24d5-NOGIL/bm-20250311-linux-x86_64-python-ebc24d54bcf554403e9b-3.14.0a5%2B-ebc24d5-vs-3.13.0rc2.md)[📈](results/bm-20250311-3.14.0a5%2B-ebc24d5-NOGIL/bm-20250311-linux-x86_64-python-ebc24d54bcf554403e9b-3.14.0a5%2B-ebc24d5-vs-3.13.0rc2.svg) | 1.112x ↓<br>[📄](results/bm-20250311-3.14.0a5%2B-ebc24d5-NOGIL/bm-20250311-linux-x86_64-python-ebc24d54bcf554403e9b-3.14.0a5%2B-ebc24d5-vs-base.md)[📈](results/bm-20250311-3.14.0a5%2B-ebc24d5-NOGIL/bm-20250311-linux-x86_64-python-ebc24d54bcf554403e9b-3.14.0a5%2B-ebc24d5-vs-base.svg)[🧠](results/bm-20250311-3.14.0a5%2B-ebc24d5-NOGIL/bm-20250311-linux-x86_64-python-ebc24d54bcf554403e9b-3.14.0a5%2B-ebc24d5-vs-base-mem.svg) |
| [2025-03-11](results/bm-20250311-3.14.0a5%2B-ebc24d5) | python/ebc24d54bcf554403e9b | ebc24d5 | 1.090x ↑<br>[📄](results/bm-20250311-3.14.0a5%2B-ebc24d5/bm-20250311-linux-x86_64-python-ebc24d54bcf554403e9b-3.14.0a5%2B-ebc24d5-vs-3.12.6.md)[📈](results/bm-20250311-3.14.0a5%2B-ebc24d5/bm-20250311-linux-x86_64-python-ebc24d54bcf554403e9b-3.14.0a5%2B-ebc24d5-vs-3.12.6.svg) | 1.048x ↑<br>[📄](results/bm-20250311-3.14.0a5%2B-ebc24d5/bm-20250311-linux-x86_64-python-ebc24d54bcf554403e9b-3.14.0a5%2B-ebc24d5-vs-3.13.0rc2.md)[📈](results/bm-20250311-3.14.0a5%2B-ebc24d5/bm-20250311-linux-x86_64-python-ebc24d54bcf554403e9b-3.14.0a5%2B-ebc24d5-vs-3.13.0rc2.svg) |  |

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-03-14](results/bm-20250314-3.14.0a6%2B-55815a6-NOGIL) | python/55815a6474c59001f023 | 55815a6 (NOGIL) | 1.046x ↓<br>[📄](results/bm-20250314-3.14.0a6%2B-55815a6-NOGIL/bm-20250314-vultr-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-3.12.6.md)[📈](results/bm-20250314-3.14.0a6%2B-55815a6-NOGIL/bm-20250314-vultr-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-3.12.6.svg) | 1.078x ↓<br>[📄](results/bm-20250314-3.14.0a6%2B-55815a6-NOGIL/bm-20250314-vultr-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-3.13.0rc2.md)[📈](results/bm-20250314-3.14.0a6%2B-55815a6-NOGIL/bm-20250314-vultr-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-3.13.0rc2.svg) | 1.106x ↓<br>[📄](results/bm-20250314-3.14.0a6%2B-55815a6-NOGIL/bm-20250314-vultr-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-base.md)[📈](results/bm-20250314-3.14.0a6%2B-55815a6-NOGIL/bm-20250314-vultr-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-base.svg)[🧠](results/bm-20250314-3.14.0a6%2B-55815a6-NOGIL/bm-20250314-vultr-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-base-mem.svg) |
| [2025-03-14](results/bm-20250314-3.14.0a6%2B-55815a6) | python/55815a6474c59001f023 | 55815a6 | 1.066x ↑<br>[📄](results/bm-20250314-3.14.0a6%2B-55815a6/bm-20250314-vultr-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-3.12.6.md)[📈](results/bm-20250314-3.14.0a6%2B-55815a6/bm-20250314-vultr-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-3.12.6.svg) | 1.027x ↑<br>[📄](results/bm-20250314-3.14.0a6%2B-55815a6/bm-20250314-vultr-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-3.13.0rc2.md)[📈](results/bm-20250314-3.14.0a6%2B-55815a6/bm-20250314-vultr-x86_64-python-55815a6474c59001f023-3.14.0a6%2B-55815a6-vs-3.13.0rc2.svg) |  |
| [2025-03-15](results/bm-20250315-3.14.0a5%2B-5264e56-NOGIL) | mpage/measure_interp_loop_ | 5264e56 (NOGIL) | 1.035x ↓<br>[📄](results/bm-20250315-3.14.0a5%2B-5264e56-NOGIL/bm-20250315-vultr-x86_64-mpage-measure_interp_loop_-3.14.0a5%2B-5264e56-vs-3.12.6.md)[📈](results/bm-20250315-3.14.0a5%2B-5264e56-NOGIL/bm-20250315-vultr-x86_64-mpage-measure_interp_loop_-3.14.0a5%2B-5264e56-vs-3.12.6.svg) | 1.067x ↓<br>[📄](results/bm-20250315-3.14.0a5%2B-5264e56-NOGIL/bm-20250315-vultr-x86_64-mpage-measure_interp_loop_-3.14.0a5%2B-5264e56-vs-3.13.0rc2.md)[📈](results/bm-20250315-3.14.0a5%2B-5264e56-NOGIL/bm-20250315-vultr-x86_64-mpage-measure_interp_loop_-3.14.0a5%2B-5264e56-vs-3.13.0rc2.svg) | 1.015x ↑<br>[📄](results/bm-20250315-3.14.0a5%2B-5264e56-NOGIL/bm-20250315-vultr-x86_64-mpage-measure_interp_loop_-3.14.0a5%2B-5264e56-vs-base.md)[📈](results/bm-20250315-3.14.0a5%2B-5264e56-NOGIL/bm-20250315-vultr-x86_64-mpage-measure_interp_loop_-3.14.0a5%2B-5264e56-vs-base.svg)[🧠](results/bm-20250315-3.14.0a5%2B-5264e56-NOGIL/bm-20250315-vultr-x86_64-mpage-measure_interp_loop_-3.14.0a5%2B-5264e56-vs-base-mem.svg) |
| [2025-03-15](results/bm-20250315-3.14.0a5%2B-94fe18c-NOGIL) | mpage/measure_bc_atomics | 94fe18c (NOGIL) | 1.042x ↓<br>[📄](results/bm-20250315-3.14.0a5%2B-94fe18c-NOGIL/bm-20250315-vultr-x86_64-mpage-measure_bc_atomics-3.14.0a5%2B-94fe18c-vs-3.12.6.md)[📈](results/bm-20250315-3.14.0a5%2B-94fe18c-NOGIL/bm-20250315-vultr-x86_64-mpage-measure_bc_atomics-3.14.0a5%2B-94fe18c-vs-3.12.6.svg) | 1.074x ↓<br>[📄](results/bm-20250315-3.14.0a5%2B-94fe18c-NOGIL/bm-20250315-vultr-x86_64-mpage-measure_bc_atomics-3.14.0a5%2B-94fe18c-vs-3.13.0rc2.md)[📈](results/bm-20250315-3.14.0a5%2B-94fe18c-NOGIL/bm-20250315-vultr-x86_64-mpage-measure_bc_atomics-3.14.0a5%2B-94fe18c-vs-3.13.0rc2.svg) | 1.008x ↑<br>[📄](results/bm-20250315-3.14.0a5%2B-94fe18c-NOGIL/bm-20250315-vultr-x86_64-mpage-measure_bc_atomics-3.14.0a5%2B-94fe18c-vs-base.md)[📈](results/bm-20250315-3.14.0a5%2B-94fe18c-NOGIL/bm-20250315-vultr-x86_64-mpage-measure_bc_atomics-3.14.0a5%2B-94fe18c-vs-base.svg)[🧠](results/bm-20250315-3.14.0a5%2B-94fe18c-NOGIL/bm-20250315-vultr-x86_64-mpage-measure_bc_atomics-3.14.0a5%2B-94fe18c-vs-base-mem.svg) |
| [2025-03-14](results/bm-20250314-3.14.0a5%2B-76fc3d1) | mpage/measure_lfb | 76fc3d1 | 1.089x ↑<br>[📄](results/bm-20250314-3.14.0a5%2B-76fc3d1/bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5%2B-76fc3d1-vs-3.12.6.md)[📈](results/bm-20250314-3.14.0a5%2B-76fc3d1/bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5%2B-76fc3d1-vs-3.12.6.svg) | 1.050x ↑<br>[📄](results/bm-20250314-3.14.0a5%2B-76fc3d1/bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5%2B-76fc3d1-vs-3.13.0rc2.md)[📈](results/bm-20250314-3.14.0a5%2B-76fc3d1/bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5%2B-76fc3d1-vs-3.13.0rc2.svg) | 1.027x ↑<br>[📄](results/bm-20250314-3.14.0a5%2B-76fc3d1/bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5%2B-76fc3d1-vs-base.md)[📈](results/bm-20250314-3.14.0a5%2B-76fc3d1/bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5%2B-76fc3d1-vs-base.svg)[🧠](results/bm-20250314-3.14.0a5%2B-76fc3d1/bm-20250314-vultr-x86_64-mpage-measure_lfb-3.14.0a5%2B-76fc3d1-vs-base-mem.svg) |
| [2025-03-14](results/bm-20250314-3.14.0a5%2B-f3e275f-NOGIL) | python/f3e275f1a92c0f668b13 | f3e275f (NOGIL) | 1.043x ↓<br>[📄](results/bm-20250314-3.14.0a5%2B-f3e275f-NOGIL/bm-20250314-vultr-x86_64-python-f3e275f1a92c0f668b13-3.14.0a5%2B-f3e275f-vs-3.12.6.md)[📈](results/bm-20250314-3.14.0a5%2B-f3e275f-NOGIL/bm-20250314-vultr-x86_64-python-f3e275f1a92c0f668b13-3.14.0a5%2B-f3e275f-vs-3.12.6.svg) | 1.075x ↓<br>[📄](results/bm-20250314-3.14.0a5%2B-f3e275f-NOGIL/bm-20250314-vultr-x86_64-python-f3e275f1a92c0f668b13-3.14.0a5%2B-f3e275f-vs-3.13.0rc2.md)[📈](results/bm-20250314-3.14.0a5%2B-f3e275f-NOGIL/bm-20250314-vultr-x86_64-python-f3e275f1a92c0f668b13-3.14.0a5%2B-f3e275f-vs-3.13.0rc2.svg) | 1.102x ↓<br>[📄](results/bm-20250314-3.14.0a5%2B-f3e275f-NOGIL/bm-20250314-vultr-x86_64-python-f3e275f1a92c0f668b13-3.14.0a5%2B-f3e275f-vs-base.md)[📈](results/bm-20250314-3.14.0a5%2B-f3e275f-NOGIL/bm-20250314-vultr-x86_64-python-f3e275f1a92c0f668b13-3.14.0a5%2B-f3e275f-vs-base.svg)[🧠](results/bm-20250314-3.14.0a5%2B-f3e275f-NOGIL/bm-20250314-vultr-x86_64-python-f3e275f1a92c0f668b13-3.14.0a5%2B-f3e275f-vs-base-mem.svg) |
| [2025-03-14](results/bm-20250314-3.14.0a5%2B-f3e275f) | python/f3e275f1a92c0f668b13 | f3e275f | 1.065x ↑<br>[📄](results/bm-20250314-3.14.0a5%2B-f3e275f/bm-20250314-vultr-x86_64-python-f3e275f1a92c0f668b13-3.14.0a5%2B-f3e275f-vs-3.12.6.md)[📈](results/bm-20250314-3.14.0a5%2B-f3e275f/bm-20250314-vultr-x86_64-python-f3e275f1a92c0f668b13-3.14.0a5%2B-f3e275f-vs-3.12.6.svg) | 1.026x ↑<br>[📄](results/bm-20250314-3.14.0a5%2B-f3e275f/bm-20250314-vultr-x86_64-python-f3e275f1a92c0f668b13-3.14.0a5%2B-f3e275f-vs-3.13.0rc2.md)[📈](results/bm-20250314-3.14.0a5%2B-f3e275f/bm-20250314-vultr-x86_64-python-f3e275f1a92c0f668b13-3.14.0a5%2B-f3e275f-vs-3.13.0rc2.svg) |  |
| [2025-03-13](results/bm-20250313-3.14.0a5%2B-1a8e574) | python/1a8e5742cdcf3dba7fc5 | 1a8e574 | 1.060x ↑<br>[📄](results/bm-20250313-3.14.0a5%2B-1a8e574/bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5%2B-1a8e574-vs-3.12.6.md)[📈](results/bm-20250313-3.14.0a5%2B-1a8e574/bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5%2B-1a8e574-vs-3.12.6.svg) | 1.021x ↑<br>[📄](results/bm-20250313-3.14.0a5%2B-1a8e574/bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5%2B-1a8e574-vs-3.13.0rc2.md)[📈](results/bm-20250313-3.14.0a5%2B-1a8e574/bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5%2B-1a8e574-vs-3.13.0rc2.svg) |  |
| [2025-03-13](results/bm-20250313-3.14.0a5%2B-1a8e574-NOGIL) | python/1a8e5742cdcf3dba7fc5 | 1a8e574 (NOGIL) | 1.050x ↓<br>[📄](results/bm-20250313-3.14.0a5%2B-1a8e574-NOGIL/bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5%2B-1a8e574-vs-3.12.6.md)[📈](results/bm-20250313-3.14.0a5%2B-1a8e574-NOGIL/bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5%2B-1a8e574-vs-3.12.6.svg) | 1.082x ↓<br>[📄](results/bm-20250313-3.14.0a5%2B-1a8e574-NOGIL/bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5%2B-1a8e574-vs-3.13.0rc2.md)[📈](results/bm-20250313-3.14.0a5%2B-1a8e574-NOGIL/bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5%2B-1a8e574-vs-3.13.0rc2.svg) | 1.105x ↓<br>[📄](results/bm-20250313-3.14.0a5%2B-1a8e574-NOGIL/bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5%2B-1a8e574-vs-base.md)[📈](results/bm-20250313-3.14.0a5%2B-1a8e574-NOGIL/bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5%2B-1a8e574-vs-base.svg)[🧠](results/bm-20250313-3.14.0a5%2B-1a8e574-NOGIL/bm-20250313-vultr-x86_64-python-1a8e5742cdcf3dba7fc5-3.14.0a5%2B-1a8e574-vs-base-mem.svg) |
| [2025-03-13](results/bm-20250313-3.14.0a5%2B-b67dc73-NOGIL) | colesbury/gh_120321_gen_send | b67dc73 (NOGIL) | 1.052x ↓<br>[📄](results/bm-20250313-3.14.0a5%2B-b67dc73-NOGIL/bm-20250313-vultr-x86_64-colesbury-gh_120321_gen_send-3.14.0a5%2B-b67dc73-vs-3.12.6.md)[📈](results/bm-20250313-3.14.0a5%2B-b67dc73-NOGIL/bm-20250313-vultr-x86_64-colesbury-gh_120321_gen_send-3.14.0a5%2B-b67dc73-vs-3.12.6.svg) | 1.083x ↓<br>[📄](results/bm-20250313-3.14.0a5%2B-b67dc73-NOGIL/bm-20250313-vultr-x86_64-colesbury-gh_120321_gen_send-3.14.0a5%2B-b67dc73-vs-3.13.0rc2.md)[📈](results/bm-20250313-3.14.0a5%2B-b67dc73-NOGIL/bm-20250313-vultr-x86_64-colesbury-gh_120321_gen_send-3.14.0a5%2B-b67dc73-vs-3.13.0rc2.svg) | 1.004x ↓<br>[📄](results/bm-20250313-3.14.0a5%2B-b67dc73-NOGIL/bm-20250313-vultr-x86_64-colesbury-gh_120321_gen_send-3.14.0a5%2B-b67dc73-vs-base.md)[📈](results/bm-20250313-3.14.0a5%2B-b67dc73-NOGIL/bm-20250313-vultr-x86_64-colesbury-gh_120321_gen_send-3.14.0a5%2B-b67dc73-vs-base.svg)[🧠](results/bm-20250313-3.14.0a5%2B-b67dc73-NOGIL/bm-20250313-vultr-x86_64-colesbury-gh_120321_gen_send-3.14.0a5%2B-b67dc73-vs-base-mem.svg) |
| [2025-03-13](results/bm-20250313-3.14.0a5%2B-d4ce112-NOGIL) | nascheme/gh_127266_type_slots | d4ce112 (NOGIL) | 1.044x ↓<br>[📄](results/bm-20250313-3.14.0a5%2B-d4ce112-NOGIL/bm-20250313-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a5%2B-d4ce112-vs-3.12.6.md)[📈](results/bm-20250313-3.14.0a5%2B-d4ce112-NOGIL/bm-20250313-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a5%2B-d4ce112-vs-3.12.6.svg) | 1.075x ↓<br>[📄](results/bm-20250313-3.14.0a5%2B-d4ce112-NOGIL/bm-20250313-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a5%2B-d4ce112-vs-3.13.0rc2.md)[📈](results/bm-20250313-3.14.0a5%2B-d4ce112-NOGIL/bm-20250313-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a5%2B-d4ce112-vs-3.13.0rc2.svg) | 1.009x ↑<br>[📄](results/bm-20250313-3.14.0a5%2B-d4ce112-NOGIL/bm-20250313-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a5%2B-d4ce112-vs-base.md)[📈](results/bm-20250313-3.14.0a5%2B-d4ce112-NOGIL/bm-20250313-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a5%2B-d4ce112-vs-base.svg)[🧠](results/bm-20250313-3.14.0a5%2B-d4ce112-NOGIL/bm-20250313-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a5%2B-d4ce112-vs-base-mem.svg) |
| [2025-03-13](results/bm-20250313-3.14.0a5%2B-8ea82b5-NOGIL) | mpage/measure_lfb | 8ea82b5 (NOGIL) | 1.025x ↓<br>[📄](results/bm-20250313-3.14.0a5%2B-8ea82b5-NOGIL/bm-20250313-vultr-x86_64-mpage-measure_lfb-3.14.0a5%2B-8ea82b5-vs-3.12.6.md)[📈](results/bm-20250313-3.14.0a5%2B-8ea82b5-NOGIL/bm-20250313-vultr-x86_64-mpage-measure_lfb-3.14.0a5%2B-8ea82b5-vs-3.12.6.svg) | 1.057x ↓<br>[📄](results/bm-20250313-3.14.0a5%2B-8ea82b5-NOGIL/bm-20250313-vultr-x86_64-mpage-measure_lfb-3.14.0a5%2B-8ea82b5-vs-3.13.0rc2.md)[📈](results/bm-20250313-3.14.0a5%2B-8ea82b5-NOGIL/bm-20250313-vultr-x86_64-mpage-measure_lfb-3.14.0a5%2B-8ea82b5-vs-3.13.0rc2.svg) | 1.027x ↑<br>[📄](results/bm-20250313-3.14.0a5%2B-8ea82b5-NOGIL/bm-20250313-vultr-x86_64-mpage-measure_lfb-3.14.0a5%2B-8ea82b5-vs-base.md)[📈](results/bm-20250313-3.14.0a5%2B-8ea82b5-NOGIL/bm-20250313-vultr-x86_64-mpage-measure_lfb-3.14.0a5%2B-8ea82b5-vs-base.svg)[🧠](results/bm-20250313-3.14.0a5%2B-8ea82b5-NOGIL/bm-20250313-vultr-x86_64-mpage-measure_lfb-3.14.0a5%2B-8ea82b5-vs-base-mem.svg) |
| [2025-03-13](results/bm-20250313-3.14.0a5%2B-c5abded-NOGIL) | python/c5abded09995f208b21e | c5abded (NOGIL) | 1.048x ↓<br>[📄](results/bm-20250313-3.14.0a5%2B-c5abded-NOGIL/bm-20250313-vultr-x86_64-python-c5abded09995f208b21e-3.14.0a5%2B-c5abded-vs-3.12.6.md)[📈](results/bm-20250313-3.14.0a5%2B-c5abded-NOGIL/bm-20250313-vultr-x86_64-python-c5abded09995f208b21e-3.14.0a5%2B-c5abded-vs-3.12.6.svg) | 1.080x ↓<br>[📄](results/bm-20250313-3.14.0a5%2B-c5abded-NOGIL/bm-20250313-vultr-x86_64-python-c5abded09995f208b21e-3.14.0a5%2B-c5abded-vs-3.13.0rc2.md)[📈](results/bm-20250313-3.14.0a5%2B-c5abded-NOGIL/bm-20250313-vultr-x86_64-python-c5abded09995f208b21e-3.14.0a5%2B-c5abded-vs-3.13.0rc2.svg) |  |
| [2025-03-13](results/bm-20250313-3.14.0a5%2B-db1e582-NOGIL) | python/db1e5827c45ad737bf83 | db1e582 (NOGIL) | 1.052x ↓<br>[📄](results/bm-20250313-3.14.0a5%2B-db1e582-NOGIL/bm-20250313-vultr-x86_64-python-db1e5827c45ad737bf83-3.14.0a5%2B-db1e582-vs-3.12.6.md)[📈](results/bm-20250313-3.14.0a5%2B-db1e582-NOGIL/bm-20250313-vultr-x86_64-python-db1e5827c45ad737bf83-3.14.0a5%2B-db1e582-vs-3.12.6.svg) | 1.084x ↓<br>[📄](results/bm-20250313-3.14.0a5%2B-db1e582-NOGIL/bm-20250313-vultr-x86_64-python-db1e5827c45ad737bf83-3.14.0a5%2B-db1e582-vs-3.13.0rc2.md)[📈](results/bm-20250313-3.14.0a5%2B-db1e582-NOGIL/bm-20250313-vultr-x86_64-python-db1e5827c45ad737bf83-3.14.0a5%2B-db1e582-vs-3.13.0rc2.svg) | 1.005x ↓<br>[📄](results/bm-20250313-3.14.0a5%2B-db1e582-NOGIL/bm-20250313-vultr-x86_64-python-db1e5827c45ad737bf83-3.14.0a5%2B-db1e582-vs-base.md)[📈](results/bm-20250313-3.14.0a5%2B-db1e582-NOGIL/bm-20250313-vultr-x86_64-python-db1e5827c45ad737bf83-3.14.0a5%2B-db1e582-vs-base.svg)[🧠](results/bm-20250313-3.14.0a5%2B-db1e582-NOGIL/bm-20250313-vultr-x86_64-python-db1e5827c45ad737bf83-3.14.0a5%2B-db1e582-vs-base-mem.svg) |
| [2025-03-12](results/bm-20250312-3.14.0a5%2B-3618240-NOGIL) | python/3618240624d98de2a68a | 3618240 (NOGIL) | 1.047x ↓<br>[📄](results/bm-20250312-3.14.0a5%2B-3618240-NOGIL/bm-20250312-vultr-x86_64-python-3618240624d98de2a68a-3.14.0a5%2B-3618240-vs-3.12.6.md)[📈](results/bm-20250312-3.14.0a5%2B-3618240-NOGIL/bm-20250312-vultr-x86_64-python-3618240624d98de2a68a-3.14.0a5%2B-3618240-vs-3.12.6.svg) | 1.079x ↓<br>[📄](results/bm-20250312-3.14.0a5%2B-3618240-NOGIL/bm-20250312-vultr-x86_64-python-3618240624d98de2a68a-3.14.0a5%2B-3618240-vs-3.13.0rc2.md)[📈](results/bm-20250312-3.14.0a5%2B-3618240-NOGIL/bm-20250312-vultr-x86_64-python-3618240624d98de2a68a-3.14.0a5%2B-3618240-vs-3.13.0rc2.svg) | 1.101x ↓<br>[📄](results/bm-20250312-3.14.0a5%2B-3618240-NOGIL/bm-20250312-vultr-x86_64-python-3618240624d98de2a68a-3.14.0a5%2B-3618240-vs-base.md)[📈](results/bm-20250312-3.14.0a5%2B-3618240-NOGIL/bm-20250312-vultr-x86_64-python-3618240624d98de2a68a-3.14.0a5%2B-3618240-vs-base.svg)[🧠](results/bm-20250312-3.14.0a5%2B-3618240-NOGIL/bm-20250312-vultr-x86_64-python-3618240624d98de2a68a-3.14.0a5%2B-3618240-vs-base-mem.svg) |
| [2025-03-12](results/bm-20250312-3.14.0a5%2B-3618240) | python/3618240624d98de2a68a | 3618240 | 1.058x ↑<br>[📄](results/bm-20250312-3.14.0a5%2B-3618240/bm-20250312-vultr-x86_64-python-3618240624d98de2a68a-3.14.0a5%2B-3618240-vs-3.12.6.md)[📈](results/bm-20250312-3.14.0a5%2B-3618240/bm-20250312-vultr-x86_64-python-3618240624d98de2a68a-3.14.0a5%2B-3618240-vs-3.12.6.svg) | 1.019x ↑<br>[📄](results/bm-20250312-3.14.0a5%2B-3618240/bm-20250312-vultr-x86_64-python-3618240624d98de2a68a-3.14.0a5%2B-3618240-vs-3.13.0rc2.md)[📈](results/bm-20250312-3.14.0a5%2B-3618240/bm-20250312-vultr-x86_64-python-3618240624d98de2a68a-3.14.0a5%2B-3618240-vs-3.13.0rc2.svg) |  |
| [2025-03-11](results/bm-20250311-3.14.0a5%2B-ebc24d5-NOGIL) | python/ebc24d54bcf554403e9b | ebc24d5 (NOGIL) | 1.042x ↓<br>[📄](results/bm-20250311-3.14.0a5%2B-ebc24d5-NOGIL/bm-20250311-vultr-x86_64-python-ebc24d54bcf554403e9b-3.14.0a5%2B-ebc24d5-vs-3.12.6.md)[📈](results/bm-20250311-3.14.0a5%2B-ebc24d5-NOGIL/bm-20250311-vultr-x86_64-python-ebc24d54bcf554403e9b-3.14.0a5%2B-ebc24d5-vs-3.12.6.svg) | 1.075x ↓<br>[📄](results/bm-20250311-3.14.0a5%2B-ebc24d5-NOGIL/bm-20250311-vultr-x86_64-python-ebc24d54bcf554403e9b-3.14.0a5%2B-ebc24d5-vs-3.13.0rc2.md)[📈](results/bm-20250311-3.14.0a5%2B-ebc24d5-NOGIL/bm-20250311-vultr-x86_64-python-ebc24d54bcf554403e9b-3.14.0a5%2B-ebc24d5-vs-3.13.0rc2.svg) | 1.091x ↓<br>[📄](results/bm-20250311-3.14.0a5%2B-ebc24d5-NOGIL/bm-20250311-vultr-x86_64-python-ebc24d54bcf554403e9b-3.14.0a5%2B-ebc24d5-vs-base.md)[📈](results/bm-20250311-3.14.0a5%2B-ebc24d5-NOGIL/bm-20250311-vultr-x86_64-python-ebc24d54bcf554403e9b-3.14.0a5%2B-ebc24d5-vs-base.svg)[🧠](results/bm-20250311-3.14.0a5%2B-ebc24d5-NOGIL/bm-20250311-vultr-x86_64-python-ebc24d54bcf554403e9b-3.14.0a5%2B-ebc24d5-vs-base-mem.svg) |
| [2025-03-11](results/bm-20250311-3.14.0a5%2B-ebc24d5) | python/ebc24d54bcf554403e9b | ebc24d5 | 1.053x ↑<br>[📄](results/bm-20250311-3.14.0a5%2B-ebc24d5/bm-20250311-vultr-x86_64-python-ebc24d54bcf554403e9b-3.14.0a5%2B-ebc24d5-vs-3.12.6.md)[📈](results/bm-20250311-3.14.0a5%2B-ebc24d5/bm-20250311-vultr-x86_64-python-ebc24d54bcf554403e9b-3.14.0a5%2B-ebc24d5-vs-3.12.6.svg) | 1.014x ↑<br>[📄](results/bm-20250311-3.14.0a5%2B-ebc24d5/bm-20250311-vultr-x86_64-python-ebc24d54bcf554403e9b-3.14.0a5%2B-ebc24d5-vs-3.13.0rc2.md)[📈](results/bm-20250311-3.14.0a5%2B-ebc24d5/bm-20250311-vultr-x86_64-python-ebc24d54bcf554403e9b-3.14.0a5%2B-ebc24d5-vs-3.13.0rc2.svg) |  |


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
