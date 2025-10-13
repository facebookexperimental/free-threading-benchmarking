# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (d6dd64a)](results/bm-20251012-3.15.0a0-d6dd64a/bm-20251012-vultr-x86_64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (d6dd64a)](results/bm-20251012-3.15.0a0-d6dd64a-PYTHON_UOPS/bm-20251012-vultr-x86_64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a-pystats.md)

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-10-12](results/bm-20251012-3.15.0a0-bb85af3-NOGIL) | python/bb85af343f331b104e3b | bb85af3 (NOGIL) | 1.017x ↓<br>[📄](results/bm-20251012-3.15.0a0-bb85af3-NOGIL/bm-20251012-vultr-x86_64-python-bb85af343f331b104e3b-3.15.0a0-bb85af3-vs-3.12.6.md)[📈](results/bm-20251012-3.15.0a0-bb85af3-NOGIL/bm-20251012-vultr-x86_64-python-bb85af343f331b104e3b-3.15.0a0-bb85af3-vs-3.12.6.svg) | 1.051x ↓<br>[📄](results/bm-20251012-3.15.0a0-bb85af3-NOGIL/bm-20251012-vultr-x86_64-python-bb85af343f331b104e3b-3.15.0a0-bb85af3-vs-3.13.0rc2.md)[📈](results/bm-20251012-3.15.0a0-bb85af3-NOGIL/bm-20251012-vultr-x86_64-python-bb85af343f331b104e3b-3.15.0a0-bb85af3-vs-3.13.0rc2.svg) | 1.091x ↓<br>[📄](results/bm-20251012-3.15.0a0-bb85af3-NOGIL/bm-20251012-vultr-x86_64-python-bb85af343f331b104e3b-3.15.0a0-bb85af3-vs-base.md)[📈](results/bm-20251012-3.15.0a0-bb85af3-NOGIL/bm-20251012-vultr-x86_64-python-bb85af343f331b104e3b-3.15.0a0-bb85af3-vs-base.svg)[🧠](results/bm-20251012-3.15.0a0-bb85af3-NOGIL/bm-20251012-vultr-x86_64-python-bb85af343f331b104e3b-3.15.0a0-bb85af3-vs-base-mem.svg) |
| [2025-10-12](results/bm-20251012-3.15.0a0-bb85af3) | python/bb85af343f331b104e3b | bb85af3 | 1.074x ↑<br>[📄](results/bm-20251012-3.15.0a0-bb85af3/bm-20251012-vultr-x86_64-python-bb85af343f331b104e3b-3.15.0a0-bb85af3-vs-3.12.6.md)[📈](results/bm-20251012-3.15.0a0-bb85af3/bm-20251012-vultr-x86_64-python-bb85af343f331b104e3b-3.15.0a0-bb85af3-vs-3.12.6.svg) | 1.038x ↑<br>[📄](results/bm-20251012-3.15.0a0-bb85af3/bm-20251012-vultr-x86_64-python-bb85af343f331b104e3b-3.15.0a0-bb85af3-vs-3.13.0rc2.md)[📈](results/bm-20251012-3.15.0a0-bb85af3/bm-20251012-vultr-x86_64-python-bb85af343f331b104e3b-3.15.0a0-bb85af3-vs-3.13.0rc2.svg) |  |
| [2025-10-12](results/bm-20251012-3.15.0a0-d6dd64a-NOGIL) | python/d6dd64ac654898b4ce71 | d6dd64a (NOGIL) | 1.015x ↓<br>[📄](results/bm-20251012-3.15.0a0-d6dd64a-NOGIL/bm-20251012-vultr-x86_64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a-vs-3.12.6.md)[📈](results/bm-20251012-3.15.0a0-d6dd64a-NOGIL/bm-20251012-vultr-x86_64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a-vs-3.12.6.svg) | 1.049x ↓<br>[📄](results/bm-20251012-3.15.0a0-d6dd64a-NOGIL/bm-20251012-vultr-x86_64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a-vs-3.13.0rc2.md)[📈](results/bm-20251012-3.15.0a0-d6dd64a-NOGIL/bm-20251012-vultr-x86_64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a-vs-3.13.0rc2.svg) | 1.092x ↓<br>[📄](results/bm-20251012-3.15.0a0-d6dd64a-NOGIL/bm-20251012-vultr-x86_64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a-vs-base.md)[📈](results/bm-20251012-3.15.0a0-d6dd64a-NOGIL/bm-20251012-vultr-x86_64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a-vs-base.svg)[🧠](results/bm-20251012-3.15.0a0-d6dd64a-NOGIL/bm-20251012-vultr-x86_64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a-vs-base-mem.svg) |
| [2025-10-12](results/bm-20251012-3.15.0a0-d6dd64a-JIT) | python/d6dd64ac654898b4ce71 | d6dd64a (JIT) | 1.079x ↑<br>[📄](results/bm-20251012-3.15.0a0-d6dd64a-JIT/bm-20251012-vultr-x86_64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a-vs-3.12.6.md)[📈](results/bm-20251012-3.15.0a0-d6dd64a-JIT/bm-20251012-vultr-x86_64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a-vs-3.12.6.svg) | 1.043x ↑<br>[📄](results/bm-20251012-3.15.0a0-d6dd64a-JIT/bm-20251012-vultr-x86_64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a-vs-3.13.0rc2.md)[📈](results/bm-20251012-3.15.0a0-d6dd64a-JIT/bm-20251012-vultr-x86_64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a-vs-3.13.0rc2.svg) | 1.000x ↑<br>[📄](results/bm-20251012-3.15.0a0-d6dd64a-JIT/bm-20251012-vultr-x86_64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a-vs-base.md)[📈](results/bm-20251012-3.15.0a0-d6dd64a-JIT/bm-20251012-vultr-x86_64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a-vs-base.svg)[🧠](results/bm-20251012-3.15.0a0-d6dd64a-JIT/bm-20251012-vultr-x86_64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a-vs-base-mem.svg) |
| [2025-10-12](results/bm-20251012-3.15.0a0-d6dd64a-CLANG) | python/d6dd64ac654898b4ce71 | d6dd64a (CLANG) | 1.122x ↑<br>[📄](results/bm-20251012-3.15.0a0-d6dd64a-CLANG/bm-20251012-vultr-x86_64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a-vs-3.12.6.md)[📈](results/bm-20251012-3.15.0a0-d6dd64a-CLANG/bm-20251012-vultr-x86_64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a-vs-3.12.6.svg) | 1.085x ↑<br>[📄](results/bm-20251012-3.15.0a0-d6dd64a-CLANG/bm-20251012-vultr-x86_64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a-vs-3.13.0rc2.md)[📈](results/bm-20251012-3.15.0a0-d6dd64a-CLANG/bm-20251012-vultr-x86_64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a-vs-3.13.0rc2.svg) | 1.038x ↑<br>[📄](results/bm-20251012-3.15.0a0-d6dd64a-CLANG/bm-20251012-vultr-x86_64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a-vs-base.md)[📈](results/bm-20251012-3.15.0a0-d6dd64a-CLANG/bm-20251012-vultr-x86_64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a-vs-base.svg)[🧠](results/bm-20251012-3.15.0a0-d6dd64a-CLANG/bm-20251012-vultr-x86_64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a-vs-base-mem.svg) |
| [2025-10-12](results/bm-20251012-3.15.0a0-d6dd64a) | python/d6dd64ac654898b4ce71 | d6dd64a | 1.078x ↑<br>[📄](results/bm-20251012-3.15.0a0-d6dd64a/bm-20251012-vultr-x86_64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a-vs-3.12.6.md)[📈](results/bm-20251012-3.15.0a0-d6dd64a/bm-20251012-vultr-x86_64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a-vs-3.12.6.svg) | 1.043x ↑<br>[📄](results/bm-20251012-3.15.0a0-d6dd64a/bm-20251012-vultr-x86_64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a-vs-3.13.0rc2.md)[📈](results/bm-20251012-3.15.0a0-d6dd64a/bm-20251012-vultr-x86_64-python-d6dd64ac654898b4ce71-3.15.0a0-d6dd64a-vs-3.13.0rc2.svg) |  |
| [2025-10-11](results/bm-20251011-3.15.0a0-0786133-NOGIL) | Fidget-Spinner/msvc_tailcall_take_t | 0786133 (NOGIL) | 1.018x ↓<br>[📄](results/bm-20251011-3.15.0a0-0786133-NOGIL/bm-20251011-vultr-x86_64-Fidget%252dSpinner-msvc_tailcall_take_t-3.15.0a0-0786133-vs-3.12.6.md)[📈](results/bm-20251011-3.15.0a0-0786133-NOGIL/bm-20251011-vultr-x86_64-Fidget%252dSpinner-msvc_tailcall_take_t-3.15.0a0-0786133-vs-3.12.6.svg) | 1.051x ↓<br>[📄](results/bm-20251011-3.15.0a0-0786133-NOGIL/bm-20251011-vultr-x86_64-Fidget%252dSpinner-msvc_tailcall_take_t-3.15.0a0-0786133-vs-3.13.0rc2.md)[📈](results/bm-20251011-3.15.0a0-0786133-NOGIL/bm-20251011-vultr-x86_64-Fidget%252dSpinner-msvc_tailcall_take_t-3.15.0a0-0786133-vs-3.13.0rc2.svg) | 1.001x ↓<br>[📄](results/bm-20251011-3.15.0a0-0786133-NOGIL/bm-20251011-vultr-x86_64-Fidget%252dSpinner-msvc_tailcall_take_t-3.15.0a0-0786133-vs-base.md)[📈](results/bm-20251011-3.15.0a0-0786133-NOGIL/bm-20251011-vultr-x86_64-Fidget%252dSpinner-msvc_tailcall_take_t-3.15.0a0-0786133-vs-base.svg)[🧠](results/bm-20251011-3.15.0a0-0786133-NOGIL/bm-20251011-vultr-x86_64-Fidget%252dSpinner-msvc_tailcall_take_t-3.15.0a0-0786133-vs-base-mem.svg) |
| [2025-10-11](results/bm-20251011-3.15.0a0-5776d0d-NOGIL) | python/5776d0d2e08f4d93dcd6 | 5776d0d (NOGIL) | 1.017x ↓<br>[📄](results/bm-20251011-3.15.0a0-5776d0d-NOGIL/bm-20251011-vultr-x86_64-python-5776d0d2e08f4d93dcd6-3.15.0a0-5776d0d-vs-3.12.6.md)[📈](results/bm-20251011-3.15.0a0-5776d0d-NOGIL/bm-20251011-vultr-x86_64-python-5776d0d2e08f4d93dcd6-3.15.0a0-5776d0d-vs-3.12.6.svg) | 1.050x ↓<br>[📄](results/bm-20251011-3.15.0a0-5776d0d-NOGIL/bm-20251011-vultr-x86_64-python-5776d0d2e08f4d93dcd6-3.15.0a0-5776d0d-vs-3.13.0rc2.md)[📈](results/bm-20251011-3.15.0a0-5776d0d-NOGIL/bm-20251011-vultr-x86_64-python-5776d0d2e08f4d93dcd6-3.15.0a0-5776d0d-vs-3.13.0rc2.svg) |  |
| [2025-10-10](results/bm-20251010-3.15.0a0-ff7bb56-NOGIL) | python/ff7bb565d836162eed08 | ff7bb56 (NOGIL) | 1.019x ↓<br>[📄](results/bm-20251010-3.15.0a0-ff7bb56-NOGIL/bm-20251010-vultr-x86_64-python-ff7bb565d836162eed08-3.15.0a0-ff7bb56-vs-3.12.6.md)[📈](results/bm-20251010-3.15.0a0-ff7bb56-NOGIL/bm-20251010-vultr-x86_64-python-ff7bb565d836162eed08-3.15.0a0-ff7bb56-vs-3.12.6.svg) | 1.053x ↓<br>[📄](results/bm-20251010-3.15.0a0-ff7bb56-NOGIL/bm-20251010-vultr-x86_64-python-ff7bb565d836162eed08-3.15.0a0-ff7bb56-vs-3.13.0rc2.md)[📈](results/bm-20251010-3.15.0a0-ff7bb56-NOGIL/bm-20251010-vultr-x86_64-python-ff7bb565d836162eed08-3.15.0a0-ff7bb56-vs-3.13.0rc2.svg) | 1.090x ↓<br>[📄](results/bm-20251010-3.15.0a0-ff7bb56-NOGIL/bm-20251010-vultr-x86_64-python-ff7bb565d836162eed08-3.15.0a0-ff7bb56-vs-base.md)[📈](results/bm-20251010-3.15.0a0-ff7bb56-NOGIL/bm-20251010-vultr-x86_64-python-ff7bb565d836162eed08-3.15.0a0-ff7bb56-vs-base.svg)[🧠](results/bm-20251010-3.15.0a0-ff7bb56-NOGIL/bm-20251010-vultr-x86_64-python-ff7bb565d836162eed08-3.15.0a0-ff7bb56-vs-base-mem.svg) |
| [2025-10-10](results/bm-20251010-3.15.0a0-ff7bb56) | python/ff7bb565d836162eed08 | ff7bb56 | 1.070x ↑<br>[📄](results/bm-20251010-3.15.0a0-ff7bb56/bm-20251010-vultr-x86_64-python-ff7bb565d836162eed08-3.15.0a0-ff7bb56-vs-3.12.6.md)[📈](results/bm-20251010-3.15.0a0-ff7bb56/bm-20251010-vultr-x86_64-python-ff7bb565d836162eed08-3.15.0a0-ff7bb56-vs-3.12.6.svg) | 1.035x ↑<br>[📄](results/bm-20251010-3.15.0a0-ff7bb56/bm-20251010-vultr-x86_64-python-ff7bb565d836162eed08-3.15.0a0-ff7bb56-vs-3.13.0rc2.md)[📈](results/bm-20251010-3.15.0a0-ff7bb56/bm-20251010-vultr-x86_64-python-ff7bb565d836162eed08-3.15.0a0-ff7bb56-vs-3.13.0rc2.svg) |  |
| [2025-10-10](results/bm-20251010-3.15.0a0-3450311-NOGIL) | python/34503111fe2724986701 | 3450311 (NOGIL) | 1.018x ↓<br>[📄](results/bm-20251010-3.15.0a0-3450311-NOGIL/bm-20251010-vultr-x86_64-python-34503111fe2724986701-3.15.0a0-3450311-vs-3.12.6.md)[📈](results/bm-20251010-3.15.0a0-3450311-NOGIL/bm-20251010-vultr-x86_64-python-34503111fe2724986701-3.15.0a0-3450311-vs-3.12.6.svg) | 1.051x ↓<br>[📄](results/bm-20251010-3.15.0a0-3450311-NOGIL/bm-20251010-vultr-x86_64-python-34503111fe2724986701-3.15.0a0-3450311-vs-3.13.0rc2.md)[📈](results/bm-20251010-3.15.0a0-3450311-NOGIL/bm-20251010-vultr-x86_64-python-34503111fe2724986701-3.15.0a0-3450311-vs-3.13.0rc2.svg) | 1.095x ↓<br>[📄](results/bm-20251010-3.15.0a0-3450311-NOGIL/bm-20251010-vultr-x86_64-python-34503111fe2724986701-3.15.0a0-3450311-vs-base.md)[📈](results/bm-20251010-3.15.0a0-3450311-NOGIL/bm-20251010-vultr-x86_64-python-34503111fe2724986701-3.15.0a0-3450311-vs-base.svg)[🧠](results/bm-20251010-3.15.0a0-3450311-NOGIL/bm-20251010-vultr-x86_64-python-34503111fe2724986701-3.15.0a0-3450311-vs-base-mem.svg) |
| [2025-10-10](results/bm-20251010-3.15.0a0-3450311) | python/34503111fe2724986701 | 3450311 | 1.077x ↑<br>[📄](results/bm-20251010-3.15.0a0-3450311/bm-20251010-vultr-x86_64-python-34503111fe2724986701-3.15.0a0-3450311-vs-3.12.6.md)[📈](results/bm-20251010-3.15.0a0-3450311/bm-20251010-vultr-x86_64-python-34503111fe2724986701-3.15.0a0-3450311-vs-3.12.6.svg) | 1.042x ↑<br>[📄](results/bm-20251010-3.15.0a0-3450311/bm-20251010-vultr-x86_64-python-34503111fe2724986701-3.15.0a0-3450311-vs-3.13.0rc2.md)[📈](results/bm-20251010-3.15.0a0-3450311/bm-20251010-vultr-x86_64-python-34503111fe2724986701-3.15.0a0-3450311-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-10-08](results/bm-20251008-3.15.0a0-85ec35d-NOGIL) | python/85ec35d2ab8b764aefd6 | 85ec35d (NOGIL) | 1.075x ↑<br>[📄](results/bm-20251008-3.15.0a0-85ec35d-NOGIL/bm-20251008-macm4pro-arm64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d-vs-3.12.6.md)[📈](results/bm-20251008-3.15.0a0-85ec35d-NOGIL/bm-20251008-macm4pro-arm64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d-vs-3.12.6.svg) | 1.003x ↓<br>[📄](results/bm-20251008-3.15.0a0-85ec35d-NOGIL/bm-20251008-macm4pro-arm64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d-vs-3.13.0rc2.md)[📈](results/bm-20251008-3.15.0a0-85ec35d-NOGIL/bm-20251008-macm4pro-arm64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d-vs-3.13.0rc2.svg) | 1.028x ↓<br>[📄](results/bm-20251008-3.15.0a0-85ec35d-NOGIL/bm-20251008-macm4pro-arm64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d-vs-base.md)[📈](results/bm-20251008-3.15.0a0-85ec35d-NOGIL/bm-20251008-macm4pro-arm64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d-vs-base.svg)[🧠](results/bm-20251008-3.15.0a0-85ec35d-NOGIL/bm-20251008-macm4pro-arm64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d-vs-base-mem.svg) |
| [2025-10-08](results/bm-20251008-3.15.0a0-85ec35d) | python/85ec35d2ab8b764aefd6 | 85ec35d | 1.104x ↑<br>[📄](results/bm-20251008-3.15.0a0-85ec35d/bm-20251008-macm4pro-arm64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d-vs-3.12.6.md)[📈](results/bm-20251008-3.15.0a0-85ec35d/bm-20251008-macm4pro-arm64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d-vs-3.12.6.svg) | 1.024x ↑<br>[📄](results/bm-20251008-3.15.0a0-85ec35d/bm-20251008-macm4pro-arm64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d-vs-3.13.0rc2.md)[📈](results/bm-20251008-3.15.0a0-85ec35d/bm-20251008-macm4pro-arm64-python-85ec35d2ab8b764aefd6-3.15.0a0-85ec35d-vs-3.13.0rc2.svg) |  |
| [2025-10-06](results/bm-20251006-3.15.0a0-3311580-NOGIL) | python/331158065b7426a79121 | 3311580 (NOGIL) | 1.076x ↑<br>[📄](results/bm-20251006-3.15.0a0-3311580-NOGIL/bm-20251006-macm4pro-arm64-python-331158065b7426a79121-3.15.0a0-3311580-vs-3.12.6.md)[📈](results/bm-20251006-3.15.0a0-3311580-NOGIL/bm-20251006-macm4pro-arm64-python-331158065b7426a79121-3.15.0a0-3311580-vs-3.12.6.svg) | 1.002x ↓<br>[📄](results/bm-20251006-3.15.0a0-3311580-NOGIL/bm-20251006-macm4pro-arm64-python-331158065b7426a79121-3.15.0a0-3311580-vs-3.13.0rc2.md)[📈](results/bm-20251006-3.15.0a0-3311580-NOGIL/bm-20251006-macm4pro-arm64-python-331158065b7426a79121-3.15.0a0-3311580-vs-3.13.0rc2.svg) | 1.023x ↓<br>[📄](results/bm-20251006-3.15.0a0-3311580-NOGIL/bm-20251006-macm4pro-arm64-python-331158065b7426a79121-3.15.0a0-3311580-vs-base.md)[📈](results/bm-20251006-3.15.0a0-3311580-NOGIL/bm-20251006-macm4pro-arm64-python-331158065b7426a79121-3.15.0a0-3311580-vs-base.svg)[🧠](results/bm-20251006-3.15.0a0-3311580-NOGIL/bm-20251006-macm4pro-arm64-python-331158065b7426a79121-3.15.0a0-3311580-vs-base-mem.svg) |


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
