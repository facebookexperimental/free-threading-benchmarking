# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
[Most recent pystats on main (5ec4bf8)](results/bm-20250222-3.14.0a5%2B-5ec4bf8-PYTHON_UOPS/bm-20250222-linux-x86_64-python-5ec4bf86b7f4455432ae-3.14.0a5%2B-5ec4bf8-pystats.md)

## linux x86_64 (linux)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-02-28](results/bm-20250228-3.14.0a5%2B-9211b3d) | python/9211b3dabeacb92713ac | 9211b3d | 1.126x ↑<br>[📄](results/bm-20250228-3.14.0a5%2B-9211b3d/bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5%2B-9211b3d-vs-3.12.6.md)[📈](results/bm-20250228-3.14.0a5%2B-9211b3d/bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5%2B-9211b3d-vs-3.12.6.svg) | 1.076x ↑<br>[📄](results/bm-20250228-3.14.0a5%2B-9211b3d/bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5%2B-9211b3d-vs-3.13.0rc2.md)[📈](results/bm-20250228-3.14.0a5%2B-9211b3d/bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5%2B-9211b3d-vs-3.13.0rc2.svg) |  |
| [2025-02-28](results/bm-20250228-3.14.0a5%2B-9211b3d-NOGIL) | python/9211b3dabeacb92713ac | 9211b3d (NOGIL) | 1.005x ↓<br>[📄](results/bm-20250228-3.14.0a5%2B-9211b3d-NOGIL/bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5%2B-9211b3d-vs-3.12.6.md)[📈](results/bm-20250228-3.14.0a5%2B-9211b3d-NOGIL/bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5%2B-9211b3d-vs-3.12.6.svg) | 1.043x ↓<br>[📄](results/bm-20250228-3.14.0a5%2B-9211b3d-NOGIL/bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5%2B-9211b3d-vs-3.13.0rc2.md)[📈](results/bm-20250228-3.14.0a5%2B-9211b3d-NOGIL/bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5%2B-9211b3d-vs-3.13.0rc2.svg) | 1.117x ↓<br>[📄](results/bm-20250228-3.14.0a5%2B-9211b3d-NOGIL/bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5%2B-9211b3d-vs-base.md)[📈](results/bm-20250228-3.14.0a5%2B-9211b3d-NOGIL/bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5%2B-9211b3d-vs-base.svg)[🧠](results/bm-20250228-3.14.0a5%2B-9211b3d-NOGIL/bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5%2B-9211b3d-vs-base-mem.svg) |
| [2025-02-26](results/bm-20250226-3.14.0a5%2B-fda056e) | python/fda056e64bdfcac3dd3d | fda056e | 1.116x ↑<br>[📄](results/bm-20250226-3.14.0a5%2B-fda056e/bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5%2B-fda056e-vs-3.12.6.md)[📈](results/bm-20250226-3.14.0a5%2B-fda056e/bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5%2B-fda056e-vs-3.12.6.svg) | 1.073x ↑<br>[📄](results/bm-20250226-3.14.0a5%2B-fda056e/bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5%2B-fda056e-vs-3.13.0rc2.md)[📈](results/bm-20250226-3.14.0a5%2B-fda056e/bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5%2B-fda056e-vs-3.13.0rc2.svg) |  |
| [2025-02-26](results/bm-20250226-3.14.0a5%2B-fda056e-NOGIL) | python/fda056e64bdfcac3dd3d | fda056e (NOGIL) | 1.004x ↑<br>[📄](results/bm-20250226-3.14.0a5%2B-fda056e-NOGIL/bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5%2B-fda056e-vs-3.12.6.md)[📈](results/bm-20250226-3.14.0a5%2B-fda056e-NOGIL/bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5%2B-fda056e-vs-3.12.6.svg) | 1.033x ↓<br>[📄](results/bm-20250226-3.14.0a5%2B-fda056e-NOGIL/bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5%2B-fda056e-vs-3.13.0rc2.md)[📈](results/bm-20250226-3.14.0a5%2B-fda056e-NOGIL/bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5%2B-fda056e-vs-3.13.0rc2.svg) | 1.101x ↓<br>[📄](results/bm-20250226-3.14.0a5%2B-fda056e-NOGIL/bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5%2B-fda056e-vs-base.md)[📈](results/bm-20250226-3.14.0a5%2B-fda056e-NOGIL/bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5%2B-fda056e-vs-base.svg)[🧠](results/bm-20250226-3.14.0a5%2B-fda056e-NOGIL/bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5%2B-fda056e-vs-base-mem.svg) |
| [2025-02-25](results/bm-20250225-3.14.0a5%2B-0ef4ffe-NOGIL) | python/0ef4ffeefd1737c18dc9 | 0ef4ffe (NOGIL) | 1.012x ↓<br>[📄](results/bm-20250225-3.14.0a5%2B-0ef4ffe-NOGIL/bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5%2B-0ef4ffe-vs-3.12.6.md)[📈](results/bm-20250225-3.14.0a5%2B-0ef4ffe-NOGIL/bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5%2B-0ef4ffe-vs-3.12.6.svg) | 1.048x ↓<br>[📄](results/bm-20250225-3.14.0a5%2B-0ef4ffe-NOGIL/bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5%2B-0ef4ffe-vs-3.13.0rc2.md)[📈](results/bm-20250225-3.14.0a5%2B-0ef4ffe-NOGIL/bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5%2B-0ef4ffe-vs-3.13.0rc2.svg) | 1.105x ↓<br>[📄](results/bm-20250225-3.14.0a5%2B-0ef4ffe-NOGIL/bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5%2B-0ef4ffe-vs-base.md)[📈](results/bm-20250225-3.14.0a5%2B-0ef4ffe-NOGIL/bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5%2B-0ef4ffe-vs-base.svg)[🧠](results/bm-20250225-3.14.0a5%2B-0ef4ffe-NOGIL/bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5%2B-0ef4ffe-vs-base-mem.svg) |
| [2025-02-25](results/bm-20250225-3.14.0a5%2B-0ef4ffe) | python/0ef4ffeefd1737c18dc9 | 0ef4ffe | 1.105x ↑<br>[📄](results/bm-20250225-3.14.0a5%2B-0ef4ffe/bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5%2B-0ef4ffe-vs-3.12.6.md)[📈](results/bm-20250225-3.14.0a5%2B-0ef4ffe/bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5%2B-0ef4ffe-vs-3.12.6.svg) | 1.063x ↑<br>[📄](results/bm-20250225-3.14.0a5%2B-0ef4ffe/bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5%2B-0ef4ffe-vs-3.13.0rc2.md)[📈](results/bm-20250225-3.14.0a5%2B-0ef4ffe/bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5%2B-0ef4ffe-vs-3.13.0rc2.svg) |  |
| [2025-02-24](results/bm-20250224-3.14.0a5%2B-3a555f0-NOGIL) | python/3a555f09f387a0212e59 | 3a555f0 (NOGIL) | 1.018x ↓<br>[📄](results/bm-20250224-3.14.0a5%2B-3a555f0-NOGIL/bm-20250224-linux-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-3.12.6.md)[📈](results/bm-20250224-3.14.0a5%2B-3a555f0-NOGIL/bm-20250224-linux-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-3.12.6.svg) | 1.054x ↓<br>[📄](results/bm-20250224-3.14.0a5%2B-3a555f0-NOGIL/bm-20250224-linux-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-3.13.0rc2.md)[📈](results/bm-20250224-3.14.0a5%2B-3a555f0-NOGIL/bm-20250224-linux-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-3.13.0rc2.svg) | 1.098x ↓<br>[📄](results/bm-20250224-3.14.0a5%2B-3a555f0-NOGIL/bm-20250224-linux-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-base.md)[📈](results/bm-20250224-3.14.0a5%2B-3a555f0-NOGIL/bm-20250224-linux-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-base.svg)[🧠](results/bm-20250224-3.14.0a5%2B-3a555f0-NOGIL/bm-20250224-linux-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-base-mem.svg) |
| [2025-02-24](results/bm-20250224-3.14.0a5%2B-3a555f0) | python/3a555f09f387a0212e59 | 3a555f0 | 1.089x ↑<br>[📄](results/bm-20250224-3.14.0a5%2B-3a555f0/bm-20250224-linux-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-3.12.6.md)[📈](results/bm-20250224-3.14.0a5%2B-3a555f0/bm-20250224-linux-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-3.12.6.svg) | 1.048x ↑<br>[📄](results/bm-20250224-3.14.0a5%2B-3a555f0/bm-20250224-linux-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-3.13.0rc2.md)[📈](results/bm-20250224-3.14.0a5%2B-3a555f0/bm-20250224-linux-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-3.13.0rc2.svg) |  |

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-02-28](results/bm-20250228-3.14.0a5%2B-9211b3d) | python/9211b3dabeacb92713ac | 9211b3d | 1.109x ↑<br>[📄](results/bm-20250228-3.14.0a5%2B-9211b3d/bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5%2B-9211b3d-vs-3.12.6.md)[📈](results/bm-20250228-3.14.0a5%2B-9211b3d/bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5%2B-9211b3d-vs-3.12.6.svg) | 1.069x ↑<br>[📄](results/bm-20250228-3.14.0a5%2B-9211b3d/bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5%2B-9211b3d-vs-3.13.0rc2.md)[📈](results/bm-20250228-3.14.0a5%2B-9211b3d/bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5%2B-9211b3d-vs-3.13.0rc2.svg) |  |
| [2025-02-28](results/bm-20250228-3.14.0a5%2B-9211b3d-NOGIL) | python/9211b3dabeacb92713ac | 9211b3d (NOGIL) | 1.057x ↓<br>[📄](results/bm-20250228-3.14.0a5%2B-9211b3d-NOGIL/bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5%2B-9211b3d-vs-3.12.6.md)[📈](results/bm-20250228-3.14.0a5%2B-9211b3d-NOGIL/bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5%2B-9211b3d-vs-3.12.6.svg) | 1.089x ↓<br>[📄](results/bm-20250228-3.14.0a5%2B-9211b3d-NOGIL/bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5%2B-9211b3d-vs-3.13.0rc2.md)[📈](results/bm-20250228-3.14.0a5%2B-9211b3d-NOGIL/bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5%2B-9211b3d-vs-3.13.0rc2.svg) | 1.150x ↓<br>[📄](results/bm-20250228-3.14.0a5%2B-9211b3d-NOGIL/bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5%2B-9211b3d-vs-base.md)[📈](results/bm-20250228-3.14.0a5%2B-9211b3d-NOGIL/bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5%2B-9211b3d-vs-base.svg)[🧠](results/bm-20250228-3.14.0a5%2B-9211b3d-NOGIL/bm-20250228-vultr-x86_64-python-9211b3dabeacb92713ac-3.14.0a5%2B-9211b3d-vs-base-mem.svg) |
| [2025-02-27](results/bm-20250227-3.14.0a5%2B-aae2849-NOGIL) | nascheme/pgo_benchmark_task | aae2849 (NOGIL) | 1.067x ↓<br>[📄](results/bm-20250227-3.14.0a5%2B-aae2849-NOGIL/bm-20250227-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5%2B-aae2849-vs-3.12.6.md)[📈](results/bm-20250227-3.14.0a5%2B-aae2849-NOGIL/bm-20250227-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5%2B-aae2849-vs-3.12.6.svg) | 1.099x ↓<br>[📄](results/bm-20250227-3.14.0a5%2B-aae2849-NOGIL/bm-20250227-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5%2B-aae2849-vs-3.13.0rc2.md)[📈](results/bm-20250227-3.14.0a5%2B-aae2849-NOGIL/bm-20250227-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5%2B-aae2849-vs-3.13.0rc2.svg) | 1.023x ↓<br>[📄](results/bm-20250227-3.14.0a5%2B-aae2849-NOGIL/bm-20250227-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5%2B-aae2849-vs-base.md)[📈](results/bm-20250227-3.14.0a5%2B-aae2849-NOGIL/bm-20250227-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5%2B-aae2849-vs-base.svg)[🧠](results/bm-20250227-3.14.0a5%2B-aae2849-NOGIL/bm-20250227-vultr-x86_64-nascheme-pgo_benchmark_task-3.14.0a5%2B-aae2849-vs-base-mem.svg) |
| [2025-02-27](results/bm-20250227-3.14.0a5%2B-9ad230b-NOGIL) | mpage/all_blocks | 9ad230b (NOGIL) | 1.029x ↓<br>[📄](results/bm-20250227-3.14.0a5%2B-9ad230b-NOGIL/bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5%2B-9ad230b-vs-3.12.6.md)[📈](results/bm-20250227-3.14.0a5%2B-9ad230b-NOGIL/bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5%2B-9ad230b-vs-3.12.6.svg) | 1.061x ↓<br>[📄](results/bm-20250227-3.14.0a5%2B-9ad230b-NOGIL/bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5%2B-9ad230b-vs-3.13.0rc2.md)[📈](results/bm-20250227-3.14.0a5%2B-9ad230b-NOGIL/bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5%2B-9ad230b-vs-3.13.0rc2.svg) | 1.028x ↑<br>[📄](results/bm-20250227-3.14.0a5%2B-9ad230b-NOGIL/bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5%2B-9ad230b-vs-base.md)[📈](results/bm-20250227-3.14.0a5%2B-9ad230b-NOGIL/bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5%2B-9ad230b-vs-base.svg)[🧠](results/bm-20250227-3.14.0a5%2B-9ad230b-NOGIL/bm-20250227-vultr-x86_64-mpage-all_blocks-3.14.0a5%2B-9ad230b-vs-base-mem.svg) |
| [2025-02-27](results/bm-20250227-3.14.0a5%2B-0d98b60-NOGIL) | mpage/load_fast_borrow_abs | 0d98b60 (NOGIL) | 1.024x ↓<br>[📄](results/bm-20250227-3.14.0a5%2B-0d98b60-NOGIL/bm-20250227-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-0d98b60-vs-3.12.6.md)[📈](results/bm-20250227-3.14.0a5%2B-0d98b60-NOGIL/bm-20250227-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-0d98b60-vs-3.12.6.svg) | 1.056x ↓<br>[📄](results/bm-20250227-3.14.0a5%2B-0d98b60-NOGIL/bm-20250227-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-0d98b60-vs-3.13.0rc2.md)[📈](results/bm-20250227-3.14.0a5%2B-0d98b60-NOGIL/bm-20250227-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-0d98b60-vs-3.13.0rc2.svg) | 1.034x ↑<br>[📄](results/bm-20250227-3.14.0a5%2B-0d98b60-NOGIL/bm-20250227-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-0d98b60-vs-base.md)[📈](results/bm-20250227-3.14.0a5%2B-0d98b60-NOGIL/bm-20250227-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-0d98b60-vs-base.svg)[🧠](results/bm-20250227-3.14.0a5%2B-0d98b60-NOGIL/bm-20250227-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-0d98b60-vs-base-mem.svg) |
| [2025-02-27](results/bm-20250227-3.14.0a5%2B-8ba0d7b-NOGIL) | python/8ba0d7bbc295781bf279 | 8ba0d7b (NOGIL) | 1.052x ↓<br>[📄](results/bm-20250227-3.14.0a5%2B-8ba0d7b-NOGIL/bm-20250227-vultr-x86_64-python-8ba0d7bbc295781bf279-3.14.0a5%2B-8ba0d7b-vs-3.12.6.md)[📈](results/bm-20250227-3.14.0a5%2B-8ba0d7b-NOGIL/bm-20250227-vultr-x86_64-python-8ba0d7bbc295781bf279-3.14.0a5%2B-8ba0d7b-vs-3.12.6.svg) | 1.084x ↓<br>[📄](results/bm-20250227-3.14.0a5%2B-8ba0d7b-NOGIL/bm-20250227-vultr-x86_64-python-8ba0d7bbc295781bf279-3.14.0a5%2B-8ba0d7b-vs-3.13.0rc2.md)[📈](results/bm-20250227-3.14.0a5%2B-8ba0d7b-NOGIL/bm-20250227-vultr-x86_64-python-8ba0d7bbc295781bf279-3.14.0a5%2B-8ba0d7b-vs-3.13.0rc2.svg) | 1.008x ↓<br>[📄](results/bm-20250227-3.14.0a5%2B-8ba0d7b-NOGIL/bm-20250227-vultr-x86_64-python-8ba0d7bbc295781bf279-3.14.0a5%2B-8ba0d7b-vs-base.md)[📈](results/bm-20250227-3.14.0a5%2B-8ba0d7b-NOGIL/bm-20250227-vultr-x86_64-python-8ba0d7bbc295781bf279-3.14.0a5%2B-8ba0d7b-vs-base.svg)[🧠](results/bm-20250227-3.14.0a5%2B-8ba0d7b-NOGIL/bm-20250227-vultr-x86_64-python-8ba0d7bbc295781bf279-3.14.0a5%2B-8ba0d7b-vs-base-mem.svg) |
| [2025-02-27](results/bm-20250227-3.14.0a5%2B-d027787-NOGIL) | python/d027787c8d89f59a9f0b | d027787 (NOGIL) | 1.044x ↓<br>[📄](results/bm-20250227-3.14.0a5%2B-d027787-NOGIL/bm-20250227-vultr-x86_64-python-d027787c8d89f59a9f0b-3.14.0a5%2B-d027787-vs-3.12.6.md)[📈](results/bm-20250227-3.14.0a5%2B-d027787-NOGIL/bm-20250227-vultr-x86_64-python-d027787c8d89f59a9f0b-3.14.0a5%2B-d027787-vs-3.12.6.svg) | 1.076x ↓<br>[📄](results/bm-20250227-3.14.0a5%2B-d027787-NOGIL/bm-20250227-vultr-x86_64-python-d027787c8d89f59a9f0b-3.14.0a5%2B-d027787-vs-3.13.0rc2.md)[📈](results/bm-20250227-3.14.0a5%2B-d027787-NOGIL/bm-20250227-vultr-x86_64-python-d027787c8d89f59a9f0b-3.14.0a5%2B-d027787-vs-3.13.0rc2.svg) |  |
| [2025-02-27](results/bm-20250227-3.14.0a5%2B-2a18e80-NOGIL) | python/2a18e80695ac1f05c95e | 2a18e80 (NOGIL) | 1.043x ↓<br>[📄](results/bm-20250227-3.14.0a5%2B-2a18e80-NOGIL/bm-20250227-vultr-x86_64-python-2a18e80695ac1f05c95e-3.14.0a5%2B-2a18e80-vs-3.12.6.md)[📈](results/bm-20250227-3.14.0a5%2B-2a18e80-NOGIL/bm-20250227-vultr-x86_64-python-2a18e80695ac1f05c95e-3.14.0a5%2B-2a18e80-vs-3.12.6.svg) | 1.075x ↓<br>[📄](results/bm-20250227-3.14.0a5%2B-2a18e80-NOGIL/bm-20250227-vultr-x86_64-python-2a18e80695ac1f05c95e-3.14.0a5%2B-2a18e80-vs-3.13.0rc2.md)[📈](results/bm-20250227-3.14.0a5%2B-2a18e80-NOGIL/bm-20250227-vultr-x86_64-python-2a18e80695ac1f05c95e-3.14.0a5%2B-2a18e80-vs-3.13.0rc2.svg) | 1.002x ↓<br>[📄](results/bm-20250227-3.14.0a5%2B-2a18e80-NOGIL/bm-20250227-vultr-x86_64-python-2a18e80695ac1f05c95e-3.14.0a5%2B-2a18e80-vs-base.md)[📈](results/bm-20250227-3.14.0a5%2B-2a18e80-NOGIL/bm-20250227-vultr-x86_64-python-2a18e80695ac1f05c95e-3.14.0a5%2B-2a18e80-vs-base.svg)[🧠](results/bm-20250227-3.14.0a5%2B-2a18e80-NOGIL/bm-20250227-vultr-x86_64-python-2a18e80695ac1f05c95e-3.14.0a5%2B-2a18e80-vs-base-mem.svg) |
| [2025-02-26](results/bm-20250226-3.14.0a5%2B-fda056e) | python/fda056e64bdfcac3dd3d | fda056e | 1.099x ↑<br>[📄](results/bm-20250226-3.14.0a5%2B-fda056e/bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5%2B-fda056e-vs-3.12.6.md)[📈](results/bm-20250226-3.14.0a5%2B-fda056e/bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5%2B-fda056e-vs-3.12.6.svg) | 1.059x ↑<br>[📄](results/bm-20250226-3.14.0a5%2B-fda056e/bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5%2B-fda056e-vs-3.13.0rc2.md)[📈](results/bm-20250226-3.14.0a5%2B-fda056e/bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5%2B-fda056e-vs-3.13.0rc2.svg) |  |
| [2025-02-26](results/bm-20250226-3.14.0a5%2B-fda056e-NOGIL) | python/fda056e64bdfcac3dd3d | fda056e (NOGIL) | 1.042x ↓<br>[📄](results/bm-20250226-3.14.0a5%2B-fda056e-NOGIL/bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5%2B-fda056e-vs-3.12.6.md)[📈](results/bm-20250226-3.14.0a5%2B-fda056e-NOGIL/bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5%2B-fda056e-vs-3.12.6.svg) | 1.074x ↓<br>[📄](results/bm-20250226-3.14.0a5%2B-fda056e-NOGIL/bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5%2B-fda056e-vs-3.13.0rc2.md)[📈](results/bm-20250226-3.14.0a5%2B-fda056e-NOGIL/bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5%2B-fda056e-vs-3.13.0rc2.svg) | 1.130x ↓<br>[📄](results/bm-20250226-3.14.0a5%2B-fda056e-NOGIL/bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5%2B-fda056e-vs-base.md)[📈](results/bm-20250226-3.14.0a5%2B-fda056e-NOGIL/bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5%2B-fda056e-vs-base.svg)[🧠](results/bm-20250226-3.14.0a5%2B-fda056e-NOGIL/bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5%2B-fda056e-vs-base-mem.svg) |
| [2025-02-26](results/bm-20250226-3.14.0a5%2B-9e474a9) | python/9e474a98af4184615540 | 9e474a9 | 1.094x ↑<br>[📄](results/bm-20250226-3.14.0a5%2B-9e474a9/bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5%2B-9e474a9-vs-3.12.6.md)[📈](results/bm-20250226-3.14.0a5%2B-9e474a9/bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5%2B-9e474a9-vs-3.12.6.svg) | 1.054x ↑<br>[📄](results/bm-20250226-3.14.0a5%2B-9e474a9/bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5%2B-9e474a9-vs-3.13.0rc2.md)[📈](results/bm-20250226-3.14.0a5%2B-9e474a9/bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5%2B-9e474a9-vs-3.13.0rc2.svg) |  |
| [2025-02-26](results/bm-20250226-3.14.0a5%2B-9e474a9-NOGIL) | python/9e474a98af4184615540 | 9e474a9 (NOGIL) | 1.048x ↓<br>[📄](results/bm-20250226-3.14.0a5%2B-9e474a9-NOGIL/bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5%2B-9e474a9-vs-3.12.6.md)[📈](results/bm-20250226-3.14.0a5%2B-9e474a9-NOGIL/bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5%2B-9e474a9-vs-3.12.6.svg) | 1.079x ↓<br>[📄](results/bm-20250226-3.14.0a5%2B-9e474a9-NOGIL/bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5%2B-9e474a9-vs-3.13.0rc2.md)[📈](results/bm-20250226-3.14.0a5%2B-9e474a9-NOGIL/bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5%2B-9e474a9-vs-3.13.0rc2.svg) | 1.131x ↓<br>[📄](results/bm-20250226-3.14.0a5%2B-9e474a9-NOGIL/bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5%2B-9e474a9-vs-base.md)[📈](results/bm-20250226-3.14.0a5%2B-9e474a9-NOGIL/bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5%2B-9e474a9-vs-base.svg)[🧠](results/bm-20250226-3.14.0a5%2B-9e474a9-NOGIL/bm-20250226-vultr-x86_64-python-9e474a98af4184615540-3.14.0a5%2B-9e474a9-vs-base-mem.svg) |
| [2025-02-26](results/bm-20250226-3.14.0a5%2B-b10c3be) | mpage/load_fast_borrow_abs | b10c3be | 1.101x ↑<br>[📄](results/bm-20250226-3.14.0a5%2B-b10c3be/bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-b10c3be-vs-3.12.6.md)[📈](results/bm-20250226-3.14.0a5%2B-b10c3be/bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-b10c3be-vs-3.12.6.svg) | 1.061x ↑<br>[📄](results/bm-20250226-3.14.0a5%2B-b10c3be/bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-b10c3be-vs-3.13.0rc2.md)[📈](results/bm-20250226-3.14.0a5%2B-b10c3be/bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-b10c3be-vs-3.13.0rc2.svg) | 1.006x ↑<br>[📄](results/bm-20250226-3.14.0a5%2B-b10c3be/bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-b10c3be-vs-base.md)[📈](results/bm-20250226-3.14.0a5%2B-b10c3be/bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-b10c3be-vs-base.svg)[🧠](results/bm-20250226-3.14.0a5%2B-b10c3be/bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-b10c3be-vs-base-mem.svg) |
| [2025-02-26](results/bm-20250226-3.14.0a5%2B-b10c3be-NOGIL) | mpage/load_fast_borrow_abs | b10c3be (NOGIL) | 1.023x ↓<br>[📄](results/bm-20250226-3.14.0a5%2B-b10c3be-NOGIL/bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-b10c3be-vs-3.12.6.md)[📈](results/bm-20250226-3.14.0a5%2B-b10c3be-NOGIL/bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-b10c3be-vs-3.12.6.svg) | 1.055x ↓<br>[📄](results/bm-20250226-3.14.0a5%2B-b10c3be-NOGIL/bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-b10c3be-vs-3.13.0rc2.md)[📈](results/bm-20250226-3.14.0a5%2B-b10c3be-NOGIL/bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-b10c3be-vs-3.13.0rc2.svg) | 1.025x ↑<br>[📄](results/bm-20250226-3.14.0a5%2B-b10c3be-NOGIL/bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-b10c3be-vs-base.md)[📈](results/bm-20250226-3.14.0a5%2B-b10c3be-NOGIL/bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-b10c3be-vs-base.svg)[🧠](results/bm-20250226-3.14.0a5%2B-b10c3be-NOGIL/bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-b10c3be-vs-base-mem.svg) |
| [2025-02-25](results/bm-20250225-3.14.0a5%2B-48e2f9e-NOGIL) | mpage/load_fast_borrow_abs | 48e2f9e (NOGIL) | 1.020x ↓<br>[📄](results/bm-20250225-3.14.0a5%2B-48e2f9e-NOGIL/bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-48e2f9e-vs-3.12.6.md)[📈](results/bm-20250225-3.14.0a5%2B-48e2f9e-NOGIL/bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-48e2f9e-vs-3.12.6.svg) | 1.053x ↓<br>[📄](results/bm-20250225-3.14.0a5%2B-48e2f9e-NOGIL/bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-48e2f9e-vs-3.13.0rc2.md)[📈](results/bm-20250225-3.14.0a5%2B-48e2f9e-NOGIL/bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-48e2f9e-vs-3.13.0rc2.svg) | 1.026x ↑<br>[📄](results/bm-20250225-3.14.0a5%2B-48e2f9e-NOGIL/bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-48e2f9e-vs-base.md)[📈](results/bm-20250225-3.14.0a5%2B-48e2f9e-NOGIL/bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-48e2f9e-vs-base.svg)[🧠](results/bm-20250225-3.14.0a5%2B-48e2f9e-NOGIL/bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-48e2f9e-vs-base-mem.svg) |
| [2025-02-25](results/bm-20250225-3.14.0a5%2B-48e2f9e) | mpage/load_fast_borrow_abs | 48e2f9e | 1.112x ↑<br>[📄](results/bm-20250225-3.14.0a5%2B-48e2f9e/bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-48e2f9e-vs-3.12.6.md)[📈](results/bm-20250225-3.14.0a5%2B-48e2f9e/bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-48e2f9e-vs-3.12.6.svg) | 1.071x ↑<br>[📄](results/bm-20250225-3.14.0a5%2B-48e2f9e/bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-48e2f9e-vs-3.13.0rc2.md)[📈](results/bm-20250225-3.14.0a5%2B-48e2f9e/bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-48e2f9e-vs-3.13.0rc2.svg) | 1.012x ↑<br>[📄](results/bm-20250225-3.14.0a5%2B-48e2f9e/bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-48e2f9e-vs-base.md)[📈](results/bm-20250225-3.14.0a5%2B-48e2f9e/bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-48e2f9e-vs-base.svg)[🧠](results/bm-20250225-3.14.0a5%2B-48e2f9e/bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-48e2f9e-vs-base-mem.svg) |
| [2025-02-25](results/bm-20250225-3.14.0a5%2B-0ef4ffe-NOGIL) | python/0ef4ffeefd1737c18dc9 | 0ef4ffe (NOGIL) | 1.046x ↓<br>[📄](results/bm-20250225-3.14.0a5%2B-0ef4ffe-NOGIL/bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5%2B-0ef4ffe-vs-3.12.6.md)[📈](results/bm-20250225-3.14.0a5%2B-0ef4ffe-NOGIL/bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5%2B-0ef4ffe-vs-3.12.6.svg) | 1.079x ↓<br>[📄](results/bm-20250225-3.14.0a5%2B-0ef4ffe-NOGIL/bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5%2B-0ef4ffe-vs-3.13.0rc2.md)[📈](results/bm-20250225-3.14.0a5%2B-0ef4ffe-NOGIL/bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5%2B-0ef4ffe-vs-3.13.0rc2.svg) | 1.132x ↓<br>[📄](results/bm-20250225-3.14.0a5%2B-0ef4ffe-NOGIL/bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5%2B-0ef4ffe-vs-base.md)[📈](results/bm-20250225-3.14.0a5%2B-0ef4ffe-NOGIL/bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5%2B-0ef4ffe-vs-base.svg)[🧠](results/bm-20250225-3.14.0a5%2B-0ef4ffe-NOGIL/bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5%2B-0ef4ffe-vs-base-mem.svg) |
| [2025-02-25](results/bm-20250225-3.14.0a5%2B-0ef4ffe) | python/0ef4ffeefd1737c18dc9 | 0ef4ffe | 1.097x ↑<br>[📄](results/bm-20250225-3.14.0a5%2B-0ef4ffe/bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5%2B-0ef4ffe-vs-3.12.6.md)[📈](results/bm-20250225-3.14.0a5%2B-0ef4ffe/bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5%2B-0ef4ffe-vs-3.12.6.svg) | 1.057x ↑<br>[📄](results/bm-20250225-3.14.0a5%2B-0ef4ffe/bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5%2B-0ef4ffe-vs-3.13.0rc2.md)[📈](results/bm-20250225-3.14.0a5%2B-0ef4ffe/bm-20250225-vultr-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5%2B-0ef4ffe-vs-3.13.0rc2.svg) |  |
| [2025-02-25](results/bm-20250225-3.14.0a5%2B-5e593ac-NOGIL) | mpage/load_fast_borrow_abs | 5e593ac (NOGIL) | 1.015x ↓<br>[📄](results/bm-20250225-3.14.0a5%2B-5e593ac-NOGIL/bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-5e593ac-vs-3.12.6.md)[📈](results/bm-20250225-3.14.0a5%2B-5e593ac-NOGIL/bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-5e593ac-vs-3.12.6.svg) | 1.048x ↓<br>[📄](results/bm-20250225-3.14.0a5%2B-5e593ac-NOGIL/bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-5e593ac-vs-3.13.0rc2.md)[📈](results/bm-20250225-3.14.0a5%2B-5e593ac-NOGIL/bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-5e593ac-vs-3.13.0rc2.svg) | 1.031x ↑<br>[📄](results/bm-20250225-3.14.0a5%2B-5e593ac-NOGIL/bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-5e593ac-vs-base.md)[📈](results/bm-20250225-3.14.0a5%2B-5e593ac-NOGIL/bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-5e593ac-vs-base.svg)[🧠](results/bm-20250225-3.14.0a5%2B-5e593ac-NOGIL/bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-5e593ac-vs-base-mem.svg) |
| [2025-02-24](results/bm-20250224-3.14.0a5%2B-3a555f0-NOGIL) | python/3a555f09f387a0212e59 | 3a555f0 (NOGIL) | 1.043x ↓<br>[📄](results/bm-20250224-3.14.0a5%2B-3a555f0-NOGIL/bm-20250224-vultr-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-3.12.6.md)[📈](results/bm-20250224-3.14.0a5%2B-3a555f0-NOGIL/bm-20250224-vultr-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-3.12.6.svg) | 1.075x ↓<br>[📄](results/bm-20250224-3.14.0a5%2B-3a555f0-NOGIL/bm-20250224-vultr-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-3.13.0rc2.md)[📈](results/bm-20250224-3.14.0a5%2B-3a555f0-NOGIL/bm-20250224-vultr-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-3.13.0rc2.svg) | 1.119x ↓<br>[📄](results/bm-20250224-3.14.0a5%2B-3a555f0-NOGIL/bm-20250224-vultr-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-base.md)[📈](results/bm-20250224-3.14.0a5%2B-3a555f0-NOGIL/bm-20250224-vultr-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-base.svg)[🧠](results/bm-20250224-3.14.0a5%2B-3a555f0-NOGIL/bm-20250224-vultr-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-base-mem.svg) |
| [2025-02-24](results/bm-20250224-3.14.0a5%2B-3a555f0) | python/3a555f09f387a0212e59 | 3a555f0 | 1.086x ↑<br>[📄](results/bm-20250224-3.14.0a5%2B-3a555f0/bm-20250224-vultr-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-3.12.6.md)[📈](results/bm-20250224-3.14.0a5%2B-3a555f0/bm-20250224-vultr-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-3.12.6.svg) | 1.046x ↑<br>[📄](results/bm-20250224-3.14.0a5%2B-3a555f0/bm-20250224-vultr-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-3.13.0rc2.md)[📈](results/bm-20250224-3.14.0a5%2B-3a555f0/bm-20250224-vultr-x86_64-python-3a555f09f387a0212e59-3.14.0a5%2B-3a555f0-vs-3.13.0rc2.svg) |  |
| [2025-02-21](results/bm-20250221-3.14.0a5%2B-1382cfc-NOGIL) | mpage/1382cfc5765730e523f5 | 1382cfc (NOGIL) | 1.015x ↑<br>[📄](results/bm-20250221-3.14.0a5%2B-1382cfc-NOGIL/bm-20250221-vultr-x86_64-mpage-1382cfc5765730e523f5-3.14.0a5%2B-1382cfc-vs-3.12.6.md)[📈](results/bm-20250221-3.14.0a5%2B-1382cfc-NOGIL/bm-20250221-vultr-x86_64-mpage-1382cfc5765730e523f5-3.14.0a5%2B-1382cfc-vs-3.12.6.svg) | 1.018x ↓<br>[📄](results/bm-20250221-3.14.0a5%2B-1382cfc-NOGIL/bm-20250221-vultr-x86_64-mpage-1382cfc5765730e523f5-3.14.0a5%2B-1382cfc-vs-3.13.0rc2.md)[📈](results/bm-20250221-3.14.0a5%2B-1382cfc-NOGIL/bm-20250221-vultr-x86_64-mpage-1382cfc5765730e523f5-3.14.0a5%2B-1382cfc-vs-3.13.0rc2.svg) | 1.056x ↑<br>[📄](results/bm-20250221-3.14.0a5%2B-1382cfc-NOGIL/bm-20250221-vultr-x86_64-mpage-1382cfc5765730e523f5-3.14.0a5%2B-1382cfc-vs-base.md)[📈](results/bm-20250221-3.14.0a5%2B-1382cfc-NOGIL/bm-20250221-vultr-x86_64-mpage-1382cfc5765730e523f5-3.14.0a5%2B-1382cfc-vs-base.svg)[🧠](results/bm-20250221-3.14.0a5%2B-1382cfc-NOGIL/bm-20250221-vultr-x86_64-mpage-1382cfc5765730e523f5-3.14.0a5%2B-1382cfc-vs-base-mem.svg) |


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
