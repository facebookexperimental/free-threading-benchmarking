# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
[Most recent pystats on main (2a66dd3)](results/bm-20241220-3.14.0a3%2B-2a66dd3-PYTHON_UOPS/bm-20241220-vultr-x86_64-python-2a66dd33dfc0b845042d-3.14.0a3%2B-2a66dd3-pystats.md)

## linux x86_64 (linux)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2024-12-24](results/bm-20241224-3.14.0a3%2B-418114c-NOGIL) | python/418114c139666f33abff | 418114c (NOGIL) | 1.145x ↓<br>[📄](results/bm-20241224-3.14.0a3%2B-418114c-NOGIL/bm-20241224-linux-x86_64-python-418114c139666f33abff-3.14.0a3%2B-418114c-vs-3.12.6.md)[📈](results/bm-20241224-3.14.0a3%2B-418114c-NOGIL/bm-20241224-linux-x86_64-python-418114c139666f33abff-3.14.0a3%2B-418114c-vs-3.12.6.svg) | 1.174x ↓<br>[📄](results/bm-20241224-3.14.0a3%2B-418114c-NOGIL/bm-20241224-linux-x86_64-python-418114c139666f33abff-3.14.0a3%2B-418114c-vs-3.13.0rc2.md)[📈](results/bm-20241224-3.14.0a3%2B-418114c-NOGIL/bm-20241224-linux-x86_64-python-418114c139666f33abff-3.14.0a3%2B-418114c-vs-3.13.0rc2.svg) | 1.224x ↓<br>[📄](results/bm-20241224-3.14.0a3%2B-418114c-NOGIL/bm-20241224-linux-x86_64-python-418114c139666f33abff-3.14.0a3%2B-418114c-vs-base.md)[📈](results/bm-20241224-3.14.0a3%2B-418114c-NOGIL/bm-20241224-linux-x86_64-python-418114c139666f33abff-3.14.0a3%2B-418114c-vs-base.svg)[🧠](results/bm-20241224-3.14.0a3%2B-418114c-NOGIL/bm-20241224-linux-x86_64-python-418114c139666f33abff-3.14.0a3%2B-418114c-vs-base-mem.svg) |
| [2024-12-24](results/bm-20241224-3.14.0a3%2B-418114c) | python/418114c139666f33abff | 418114c | 1.112x ↑<br>[📄](results/bm-20241224-3.14.0a3%2B-418114c/bm-20241224-linux-x86_64-python-418114c139666f33abff-3.14.0a3%2B-418114c-vs-3.12.6.md)[📈](results/bm-20241224-3.14.0a3%2B-418114c/bm-20241224-linux-x86_64-python-418114c139666f33abff-3.14.0a3%2B-418114c-vs-3.12.6.svg) | 1.070x ↑<br>[📄](results/bm-20241224-3.14.0a3%2B-418114c/bm-20241224-linux-x86_64-python-418114c139666f33abff-3.14.0a3%2B-418114c-vs-3.13.0rc2.md)[📈](results/bm-20241224-3.14.0a3%2B-418114c/bm-20241224-linux-x86_64-python-418114c139666f33abff-3.14.0a3%2B-418114c-vs-3.13.0rc2.svg) |  |
| [2024-12-24](results/bm-20241224-3.14.0a3%2B-30efede-NOGIL) | python/30efede33ca1fe32debb | 30efede (NOGIL) | 1.140x ↓<br>[📄](results/bm-20241224-3.14.0a3%2B-30efede-NOGIL/bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3%2B-30efede-vs-3.12.6.md)[📈](results/bm-20241224-3.14.0a3%2B-30efede-NOGIL/bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3%2B-30efede-vs-3.12.6.svg) | 1.172x ↓<br>[📄](results/bm-20241224-3.14.0a3%2B-30efede-NOGIL/bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3%2B-30efede-vs-3.13.0rc2.md)[📈](results/bm-20241224-3.14.0a3%2B-30efede-NOGIL/bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3%2B-30efede-vs-3.13.0rc2.svg) | 1.209x ↓<br>[📄](results/bm-20241224-3.14.0a3%2B-30efede-NOGIL/bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3%2B-30efede-vs-base.md)[📈](results/bm-20241224-3.14.0a3%2B-30efede-NOGIL/bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3%2B-30efede-vs-base.svg)[🧠](results/bm-20241224-3.14.0a3%2B-30efede-NOGIL/bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3%2B-30efede-vs-base-mem.svg) |
| [2024-12-24](results/bm-20241224-3.14.0a3%2B-30efede) | python/30efede33ca1fe32debb | 30efede | 1.093x ↑<br>[📄](results/bm-20241224-3.14.0a3%2B-30efede/bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3%2B-30efede-vs-3.12.6.md)[📈](results/bm-20241224-3.14.0a3%2B-30efede/bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3%2B-30efede-vs-3.12.6.svg) | 1.051x ↑<br>[📄](results/bm-20241224-3.14.0a3%2B-30efede/bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3%2B-30efede-vs-3.13.0rc2.md)[📈](results/bm-20241224-3.14.0a3%2B-30efede/bm-20241224-linux-x86_64-python-30efede33ca1fe32debb-3.14.0a3%2B-30efede-vs-3.13.0rc2.svg) |  |
| [2024-12-22](results/bm-20241222-3.14.0a3%2B-9d3a8f4) | python/9d3a8f494985e8bbef69 | 9d3a8f4 | 1.082x ↑<br>[📄](results/bm-20241222-3.14.0a3%2B-9d3a8f4/bm-20241222-linux-x86_64-python-9d3a8f494985e8bbef69-3.14.0a3%2B-9d3a8f4-vs-3.12.6.md)[📈](results/bm-20241222-3.14.0a3%2B-9d3a8f4/bm-20241222-linux-x86_64-python-9d3a8f494985e8bbef69-3.14.0a3%2B-9d3a8f4-vs-3.12.6.svg) | 1.038x ↑<br>[📄](results/bm-20241222-3.14.0a3%2B-9d3a8f4/bm-20241222-linux-x86_64-python-9d3a8f494985e8bbef69-3.14.0a3%2B-9d3a8f4-vs-3.13.0rc2.md)[📈](results/bm-20241222-3.14.0a3%2B-9d3a8f4/bm-20241222-linux-x86_64-python-9d3a8f494985e8bbef69-3.14.0a3%2B-9d3a8f4-vs-3.13.0rc2.svg) |  |
| [2024-12-22](results/bm-20241222-3.14.0a3%2B-9d3a8f4-NOGIL) | python/9d3a8f494985e8bbef69 | 9d3a8f4 (NOGIL) | 1.137x ↓<br>[📄](results/bm-20241222-3.14.0a3%2B-9d3a8f4-NOGIL/bm-20241222-linux-x86_64-python-9d3a8f494985e8bbef69-3.14.0a3%2B-9d3a8f4-vs-3.12.6.md)[📈](results/bm-20241222-3.14.0a3%2B-9d3a8f4-NOGIL/bm-20241222-linux-x86_64-python-9d3a8f494985e8bbef69-3.14.0a3%2B-9d3a8f4-vs-3.12.6.svg) | 1.167x ↓<br>[📄](results/bm-20241222-3.14.0a3%2B-9d3a8f4-NOGIL/bm-20241222-linux-x86_64-python-9d3a8f494985e8bbef69-3.14.0a3%2B-9d3a8f4-vs-3.13.0rc2.md)[📈](results/bm-20241222-3.14.0a3%2B-9d3a8f4-NOGIL/bm-20241222-linux-x86_64-python-9d3a8f494985e8bbef69-3.14.0a3%2B-9d3a8f4-vs-3.13.0rc2.svg) | 1.196x ↓<br>[📄](results/bm-20241222-3.14.0a3%2B-9d3a8f4-NOGIL/bm-20241222-linux-x86_64-python-9d3a8f494985e8bbef69-3.14.0a3%2B-9d3a8f4-vs-base.md)[📈](results/bm-20241222-3.14.0a3%2B-9d3a8f4-NOGIL/bm-20241222-linux-x86_64-python-9d3a8f494985e8bbef69-3.14.0a3%2B-9d3a8f4-vs-base.svg)[🧠](results/bm-20241222-3.14.0a3%2B-9d3a8f4-NOGIL/bm-20241222-linux-x86_64-python-9d3a8f494985e8bbef69-3.14.0a3%2B-9d3a8f4-vs-base-mem.svg) |

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2024-12-24](results/bm-20241224-3.14.0a3%2B-418114c-NOGIL) | python/418114c139666f33abff | 418114c (NOGIL) | 1.175x ↓<br>[📄](results/bm-20241224-3.14.0a3%2B-418114c-NOGIL/bm-20241224-vultr-x86_64-python-418114c139666f33abff-3.14.0a3%2B-418114c-vs-3.12.6.md)[📈](results/bm-20241224-3.14.0a3%2B-418114c-NOGIL/bm-20241224-vultr-x86_64-python-418114c139666f33abff-3.14.0a3%2B-418114c-vs-3.12.6.svg) | 1.202x ↓<br>[📄](results/bm-20241224-3.14.0a3%2B-418114c-NOGIL/bm-20241224-vultr-x86_64-python-418114c139666f33abff-3.14.0a3%2B-418114c-vs-3.13.0rc2.md)[📈](results/bm-20241224-3.14.0a3%2B-418114c-NOGIL/bm-20241224-vultr-x86_64-python-418114c139666f33abff-3.14.0a3%2B-418114c-vs-3.13.0rc2.svg) | 1.234x ↓<br>[📄](results/bm-20241224-3.14.0a3%2B-418114c-NOGIL/bm-20241224-vultr-x86_64-python-418114c139666f33abff-3.14.0a3%2B-418114c-vs-base.md)[📈](results/bm-20241224-3.14.0a3%2B-418114c-NOGIL/bm-20241224-vultr-x86_64-python-418114c139666f33abff-3.14.0a3%2B-418114c-vs-base.svg)[🧠](results/bm-20241224-3.14.0a3%2B-418114c-NOGIL/bm-20241224-vultr-x86_64-python-418114c139666f33abff-3.14.0a3%2B-418114c-vs-base-mem.svg) |
| [2024-12-24](results/bm-20241224-3.14.0a3%2B-418114c) | python/418114c139666f33abff | 418114c | 1.084x ↑<br>[📄](results/bm-20241224-3.14.0a3%2B-418114c/bm-20241224-vultr-x86_64-python-418114c139666f33abff-3.14.0a3%2B-418114c-vs-3.12.6.md)[📈](results/bm-20241224-3.14.0a3%2B-418114c/bm-20241224-vultr-x86_64-python-418114c139666f33abff-3.14.0a3%2B-418114c-vs-3.12.6.svg) | 1.046x ↑<br>[📄](results/bm-20241224-3.14.0a3%2B-418114c/bm-20241224-vultr-x86_64-python-418114c139666f33abff-3.14.0a3%2B-418114c-vs-3.13.0rc2.md)[📈](results/bm-20241224-3.14.0a3%2B-418114c/bm-20241224-vultr-x86_64-python-418114c139666f33abff-3.14.0a3%2B-418114c-vs-3.13.0rc2.svg) |  |
| [2024-12-24](results/bm-20241224-3.14.0a3%2B-30efede-NOGIL) | python/30efede33ca1fe32debb | 30efede (NOGIL) | 1.168x ↓<br>[📄](results/bm-20241224-3.14.0a3%2B-30efede-NOGIL/bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3%2B-30efede-vs-3.12.6.md)[📈](results/bm-20241224-3.14.0a3%2B-30efede-NOGIL/bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3%2B-30efede-vs-3.12.6.svg) | 1.195x ↓<br>[📄](results/bm-20241224-3.14.0a3%2B-30efede-NOGIL/bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3%2B-30efede-vs-3.13.0rc2.md)[📈](results/bm-20241224-3.14.0a3%2B-30efede-NOGIL/bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3%2B-30efede-vs-3.13.0rc2.svg) | 1.229x ↓<br>[📄](results/bm-20241224-3.14.0a3%2B-30efede-NOGIL/bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3%2B-30efede-vs-base.md)[📈](results/bm-20241224-3.14.0a3%2B-30efede-NOGIL/bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3%2B-30efede-vs-base.svg)[🧠](results/bm-20241224-3.14.0a3%2B-30efede-NOGIL/bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3%2B-30efede-vs-base-mem.svg) |
| [2024-12-24](results/bm-20241224-3.14.0a3%2B-30efede) | python/30efede33ca1fe32debb | 30efede | 1.087x ↑<br>[📄](results/bm-20241224-3.14.0a3%2B-30efede/bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3%2B-30efede-vs-3.12.6.md)[📈](results/bm-20241224-3.14.0a3%2B-30efede/bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3%2B-30efede-vs-3.12.6.svg) | 1.049x ↑<br>[📄](results/bm-20241224-3.14.0a3%2B-30efede/bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3%2B-30efede-vs-3.13.0rc2.md)[📈](results/bm-20241224-3.14.0a3%2B-30efede/bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3%2B-30efede-vs-3.13.0rc2.svg) |  |
| [2024-12-22](results/bm-20241222-3.14.0a3%2B-f420bdd-NOGIL) | python/f420bdd29fbc1a97ad20 | f420bdd (NOGIL) | 1.187x ↓<br>[📄](results/bm-20241222-3.14.0a3%2B-f420bdd-NOGIL/bm-20241222-vultr-x86_64-python-f420bdd29fbc1a97ad20-3.14.0a3%2B-f420bdd-vs-3.12.6.md)[📈](results/bm-20241222-3.14.0a3%2B-f420bdd-NOGIL/bm-20241222-vultr-x86_64-python-f420bdd29fbc1a97ad20-3.14.0a3%2B-f420bdd-vs-3.12.6.svg) | 1.213x ↓<br>[📄](results/bm-20241222-3.14.0a3%2B-f420bdd-NOGIL/bm-20241222-vultr-x86_64-python-f420bdd29fbc1a97ad20-3.14.0a3%2B-f420bdd-vs-3.13.0rc2.md)[📈](results/bm-20241222-3.14.0a3%2B-f420bdd-NOGIL/bm-20241222-vultr-x86_64-python-f420bdd29fbc1a97ad20-3.14.0a3%2B-f420bdd-vs-3.13.0rc2.svg) |  |
| [2024-12-22](results/bm-20241222-3.14.0a3%2B-83781d1-NOGIL) | colesbury/align_32 | 83781d1 (NOGIL) | 1.177x ↓<br>[📄](results/bm-20241222-3.14.0a3%2B-83781d1-NOGIL/bm-20241222-vultr-x86_64-colesbury-align_32-3.14.0a3%2B-83781d1-vs-3.12.6.md)[📈](results/bm-20241222-3.14.0a3%2B-83781d1-NOGIL/bm-20241222-vultr-x86_64-colesbury-align_32-3.14.0a3%2B-83781d1-vs-3.12.6.svg) | 1.203x ↓<br>[📄](results/bm-20241222-3.14.0a3%2B-83781d1-NOGIL/bm-20241222-vultr-x86_64-colesbury-align_32-3.14.0a3%2B-83781d1-vs-3.13.0rc2.md)[📈](results/bm-20241222-3.14.0a3%2B-83781d1-NOGIL/bm-20241222-vultr-x86_64-colesbury-align_32-3.14.0a3%2B-83781d1-vs-3.13.0rc2.svg) | 1.012x ↑<br>[📄](results/bm-20241222-3.14.0a3%2B-83781d1-NOGIL/bm-20241222-vultr-x86_64-colesbury-align_32-3.14.0a3%2B-83781d1-vs-base.md)[📈](results/bm-20241222-3.14.0a3%2B-83781d1-NOGIL/bm-20241222-vultr-x86_64-colesbury-align_32-3.14.0a3%2B-83781d1-vs-base.svg)[🧠](results/bm-20241222-3.14.0a3%2B-83781d1-NOGIL/bm-20241222-vultr-x86_64-colesbury-align_32-3.14.0a3%2B-83781d1-vs-base-mem.svg) |
| [2024-12-22](results/bm-20241222-3.14.0a3%2B-9d3a8f4) | python/9d3a8f494985e8bbef69 | 9d3a8f4 | 1.094x ↑<br>[📄](results/bm-20241222-3.14.0a3%2B-9d3a8f4/bm-20241222-vultr-x86_64-python-9d3a8f494985e8bbef69-3.14.0a3%2B-9d3a8f4-vs-3.12.6.md)[📈](results/bm-20241222-3.14.0a3%2B-9d3a8f4/bm-20241222-vultr-x86_64-python-9d3a8f494985e8bbef69-3.14.0a3%2B-9d3a8f4-vs-3.12.6.svg) | 1.055x ↑<br>[📄](results/bm-20241222-3.14.0a3%2B-9d3a8f4/bm-20241222-vultr-x86_64-python-9d3a8f494985e8bbef69-3.14.0a3%2B-9d3a8f4-vs-3.13.0rc2.md)[📈](results/bm-20241222-3.14.0a3%2B-9d3a8f4/bm-20241222-vultr-x86_64-python-9d3a8f494985e8bbef69-3.14.0a3%2B-9d3a8f4-vs-3.13.0rc2.svg) |  |
| [2024-12-22](results/bm-20241222-3.14.0a3%2B-9d3a8f4-NOGIL) | python/9d3a8f494985e8bbef69 | 9d3a8f4 (NOGIL) | 1.188x ↓<br>[📄](results/bm-20241222-3.14.0a3%2B-9d3a8f4-NOGIL/bm-20241222-vultr-x86_64-python-9d3a8f494985e8bbef69-3.14.0a3%2B-9d3a8f4-vs-3.12.6.md)[📈](results/bm-20241222-3.14.0a3%2B-9d3a8f4-NOGIL/bm-20241222-vultr-x86_64-python-9d3a8f494985e8bbef69-3.14.0a3%2B-9d3a8f4-vs-3.12.6.svg) | 1.214x ↓<br>[📄](results/bm-20241222-3.14.0a3%2B-9d3a8f4-NOGIL/bm-20241222-vultr-x86_64-python-9d3a8f494985e8bbef69-3.14.0a3%2B-9d3a8f4-vs-3.13.0rc2.md)[📈](results/bm-20241222-3.14.0a3%2B-9d3a8f4-NOGIL/bm-20241222-vultr-x86_64-python-9d3a8f494985e8bbef69-3.14.0a3%2B-9d3a8f4-vs-3.13.0rc2.svg) | 1.000x ↓<br>[📄](results/bm-20241222-3.14.0a3%2B-9d3a8f4-NOGIL/bm-20241222-vultr-x86_64-python-9d3a8f494985e8bbef69-3.14.0a3%2B-9d3a8f4-vs-base.md)[📈](results/bm-20241222-3.14.0a3%2B-9d3a8f4-NOGIL/bm-20241222-vultr-x86_64-python-9d3a8f494985e8bbef69-3.14.0a3%2B-9d3a8f4-vs-base.svg)[🧠](results/bm-20241222-3.14.0a3%2B-9d3a8f4-NOGIL/bm-20241222-vultr-x86_64-python-9d3a8f494985e8bbef69-3.14.0a3%2B-9d3a8f4-vs-base-mem.svg) |
| [2024-12-20](results/bm-20241220-3.14.0a3%2B-4fc4237) | mpage/4fc4237a1ea09f6a31e9 | 4fc4237 | 1.091x ↑<br>[📄](results/bm-20241220-3.14.0a3%2B-4fc4237/bm-20241220-vultr-x86_64-mpage-4fc4237a1ea09f6a31e9-3.14.0a3%2B-4fc4237-vs-3.12.6.md)[📈](results/bm-20241220-3.14.0a3%2B-4fc4237/bm-20241220-vultr-x86_64-mpage-4fc4237a1ea09f6a31e9-3.14.0a3%2B-4fc4237-vs-3.12.6.svg) | 1.052x ↑<br>[📄](results/bm-20241220-3.14.0a3%2B-4fc4237/bm-20241220-vultr-x86_64-mpage-4fc4237a1ea09f6a31e9-3.14.0a3%2B-4fc4237-vs-3.13.0rc2.md)[📈](results/bm-20241220-3.14.0a3%2B-4fc4237/bm-20241220-vultr-x86_64-mpage-4fc4237a1ea09f6a31e9-3.14.0a3%2B-4fc4237-vs-3.13.0rc2.svg) | 1.002x ↑<br>[📄](results/bm-20241220-3.14.0a3%2B-4fc4237/bm-20241220-vultr-x86_64-mpage-4fc4237a1ea09f6a31e9-3.14.0a3%2B-4fc4237-vs-base.md)[📈](results/bm-20241220-3.14.0a3%2B-4fc4237/bm-20241220-vultr-x86_64-mpage-4fc4237a1ea09f6a31e9-3.14.0a3%2B-4fc4237-vs-base.svg)[🧠](results/bm-20241220-3.14.0a3%2B-4fc4237/bm-20241220-vultr-x86_64-mpage-4fc4237a1ea09f6a31e9-3.14.0a3%2B-4fc4237-vs-base-mem.svg) |
| [2024-12-20](results/bm-20241220-3.14.0a3%2B-63a53fd) | mpage/63a53fd736f57fcf80df | 63a53fd | 1.085x ↑<br>[📄](results/bm-20241220-3.14.0a3%2B-63a53fd/bm-20241220-vultr-x86_64-mpage-63a53fd736f57fcf80df-3.14.0a3%2B-63a53fd-vs-3.12.6.md)[📈](results/bm-20241220-3.14.0a3%2B-63a53fd/bm-20241220-vultr-x86_64-mpage-63a53fd736f57fcf80df-3.14.0a3%2B-63a53fd-vs-3.12.6.svg) | 1.046x ↑<br>[📄](results/bm-20241220-3.14.0a3%2B-63a53fd/bm-20241220-vultr-x86_64-mpage-63a53fd736f57fcf80df-3.14.0a3%2B-63a53fd-vs-3.13.0rc2.md)[📈](results/bm-20241220-3.14.0a3%2B-63a53fd/bm-20241220-vultr-x86_64-mpage-63a53fd736f57fcf80df-3.14.0a3%2B-63a53fd-vs-3.13.0rc2.svg) | 1.002x ↓<br>[📄](results/bm-20241220-3.14.0a3%2B-63a53fd/bm-20241220-vultr-x86_64-mpage-63a53fd736f57fcf80df-3.14.0a3%2B-63a53fd-vs-base.md)[📈](results/bm-20241220-3.14.0a3%2B-63a53fd/bm-20241220-vultr-x86_64-mpage-63a53fd736f57fcf80df-3.14.0a3%2B-63a53fd-vs-base.svg)[🧠](results/bm-20241220-3.14.0a3%2B-63a53fd/bm-20241220-vultr-x86_64-mpage-63a53fd736f57fcf80df-3.14.0a3%2B-63a53fd-vs-base-mem.svg) |
| [2024-12-20](results/bm-20241220-3.14.0a3%2B-9364aaa) | mpage/9364aaa5b628ce0b5ffb | 9364aaa | 1.090x ↑<br>[📄](results/bm-20241220-3.14.0a3%2B-9364aaa/bm-20241220-vultr-x86_64-mpage-9364aaa5b628ce0b5ffb-3.14.0a3%2B-9364aaa-vs-3.12.6.md)[📈](results/bm-20241220-3.14.0a3%2B-9364aaa/bm-20241220-vultr-x86_64-mpage-9364aaa5b628ce0b5ffb-3.14.0a3%2B-9364aaa-vs-3.12.6.svg) | 1.051x ↑<br>[📄](results/bm-20241220-3.14.0a3%2B-9364aaa/bm-20241220-vultr-x86_64-mpage-9364aaa5b628ce0b5ffb-3.14.0a3%2B-9364aaa-vs-3.13.0rc2.md)[📈](results/bm-20241220-3.14.0a3%2B-9364aaa/bm-20241220-vultr-x86_64-mpage-9364aaa5b628ce0b5ffb-3.14.0a3%2B-9364aaa-vs-3.13.0rc2.svg) | 1.001x ↑<br>[📄](results/bm-20241220-3.14.0a3%2B-9364aaa/bm-20241220-vultr-x86_64-mpage-9364aaa5b628ce0b5ffb-3.14.0a3%2B-9364aaa-vs-base.md)[📈](results/bm-20241220-3.14.0a3%2B-9364aaa/bm-20241220-vultr-x86_64-mpage-9364aaa5b628ce0b5ffb-3.14.0a3%2B-9364aaa-vs-base.svg)[🧠](results/bm-20241220-3.14.0a3%2B-9364aaa/bm-20241220-vultr-x86_64-mpage-9364aaa5b628ce0b5ffb-3.14.0a3%2B-9364aaa-vs-base-mem.svg) |


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
