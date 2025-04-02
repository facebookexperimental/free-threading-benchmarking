# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
- [Most recent  pystats on main (a3990df)](results/bm-20250308-3.14.0a5%2B-a3990df/bm-20250308-linux-x86_64-python-a3990df6121880e8c678-3.14.0a5%2B-a3990df-pystats.md)
- [Most recent PYTHON_UOPS pystats on main (425f60b)](results/bm-20250329-3.14.0a6%2B-425f60b-PYTHON_UOPS/bm-20250329-linux-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-pystats.md)

## linux x86_64 (linux)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-03-31](results/bm-20250331-3.14.0a6%2B-45a3ab5-NOGIL) | python/45a3ab5a81769eadd94d | 45a3ab5 (NOGIL) | 1.032x ↑<br>[📄](results/bm-20250331-3.14.0a6%2B-45a3ab5-NOGIL/bm-20250331-linux-x86_64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5-vs-3.12.6.md)[📈](results/bm-20250331-3.14.0a6%2B-45a3ab5-NOGIL/bm-20250331-linux-x86_64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5-vs-3.12.6.svg) | 1.004x ↓<br>[📄](results/bm-20250331-3.14.0a6%2B-45a3ab5-NOGIL/bm-20250331-linux-x86_64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5-vs-3.13.0rc2.md)[📈](results/bm-20250331-3.14.0a6%2B-45a3ab5-NOGIL/bm-20250331-linux-x86_64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5-vs-3.13.0rc2.svg) | 1.104x ↓<br>[📄](results/bm-20250331-3.14.0a6%2B-45a3ab5-NOGIL/bm-20250331-linux-x86_64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5-vs-base.md)[📈](results/bm-20250331-3.14.0a6%2B-45a3ab5-NOGIL/bm-20250331-linux-x86_64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5-vs-base.svg)[🧠](results/bm-20250331-3.14.0a6%2B-45a3ab5-NOGIL/bm-20250331-linux-x86_64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5-vs-base-mem.svg) |
| [2025-03-31](results/bm-20250331-3.14.0a6%2B-45a3ab5) | python/45a3ab5a81769eadd94d | 45a3ab5 | 1.152x ↑<br>[📄](results/bm-20250331-3.14.0a6%2B-45a3ab5/bm-20250331-linux-x86_64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5-vs-3.12.6.md)[📈](results/bm-20250331-3.14.0a6%2B-45a3ab5/bm-20250331-linux-x86_64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5-vs-3.12.6.svg) | 1.106x ↑<br>[📄](results/bm-20250331-3.14.0a6%2B-45a3ab5/bm-20250331-linux-x86_64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5-vs-3.13.0rc2.md)[📈](results/bm-20250331-3.14.0a6%2B-45a3ab5/bm-20250331-linux-x86_64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5-vs-3.13.0rc2.svg) |  |
| [2025-03-30](results/bm-20250330-3.14.0a6%2B-685fd74-NOGIL) | python/685fd74f81e673dc0430 | 685fd74 (NOGIL) | 1.042x ↑<br>[📄](results/bm-20250330-3.14.0a6%2B-685fd74-NOGIL/bm-20250330-linux-x86_64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74-vs-3.12.6.md)[📈](results/bm-20250330-3.14.0a6%2B-685fd74-NOGIL/bm-20250330-linux-x86_64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74-vs-3.12.6.svg) | 1.004x ↑<br>[📄](results/bm-20250330-3.14.0a6%2B-685fd74-NOGIL/bm-20250330-linux-x86_64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74-vs-3.13.0rc2.md)[📈](results/bm-20250330-3.14.0a6%2B-685fd74-NOGIL/bm-20250330-linux-x86_64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74-vs-3.13.0rc2.svg) | 1.110x ↓<br>[📄](results/bm-20250330-3.14.0a6%2B-685fd74-NOGIL/bm-20250330-linux-x86_64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74-vs-base.md)[📈](results/bm-20250330-3.14.0a6%2B-685fd74-NOGIL/bm-20250330-linux-x86_64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74-vs-base.svg)[🧠](results/bm-20250330-3.14.0a6%2B-685fd74-NOGIL/bm-20250330-linux-x86_64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74-vs-base-mem.svg) |
| [2025-03-30](results/bm-20250330-3.14.0a6%2B-685fd74) | python/685fd74f81e673dc0430 | 685fd74 | 1.167x ↑<br>[📄](results/bm-20250330-3.14.0a6%2B-685fd74/bm-20250330-linux-x86_64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74-vs-3.12.6.md)[📈](results/bm-20250330-3.14.0a6%2B-685fd74/bm-20250330-linux-x86_64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74-vs-3.12.6.svg) | 1.119x ↑<br>[📄](results/bm-20250330-3.14.0a6%2B-685fd74/bm-20250330-linux-x86_64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74-vs-3.13.0rc2.md)[📈](results/bm-20250330-3.14.0a6%2B-685fd74/bm-20250330-linux-x86_64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74-vs-3.13.0rc2.svg) |  |
| [2025-03-29](results/bm-20250329-3.14.0a6%2B-425f60b-NOGIL) | python/425f60b9eb253c57bc32 | 425f60b (NOGIL) | 1.039x ↑<br>[📄](results/bm-20250329-3.14.0a6%2B-425f60b-NOGIL/bm-20250329-linux-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.12.6.md)[📈](results/bm-20250329-3.14.0a6%2B-425f60b-NOGIL/bm-20250329-linux-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.12.6.svg) | 1.002x ↑<br>[📄](results/bm-20250329-3.14.0a6%2B-425f60b-NOGIL/bm-20250329-linux-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.13.0rc2.md)[📈](results/bm-20250329-3.14.0a6%2B-425f60b-NOGIL/bm-20250329-linux-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.13.0rc2.svg) | 1.114x ↓<br>[📄](results/bm-20250329-3.14.0a6%2B-425f60b-NOGIL/bm-20250329-linux-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-base.md)[📈](results/bm-20250329-3.14.0a6%2B-425f60b-NOGIL/bm-20250329-linux-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-base.svg)[🧠](results/bm-20250329-3.14.0a6%2B-425f60b-NOGIL/bm-20250329-linux-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-base-mem.svg) |
| [2025-03-29](results/bm-20250329-3.14.0a6%2B-425f60b-JIT) | python/425f60b9eb253c57bc32 | 425f60b (JIT) | 1.170x ↑<br>[📄](results/bm-20250329-3.14.0a6%2B-425f60b-JIT/bm-20250329-linux-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.12.6.md)[📈](results/bm-20250329-3.14.0a6%2B-425f60b-JIT/bm-20250329-linux-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.12.6.svg) | 1.126x ↑<br>[📄](results/bm-20250329-3.14.0a6%2B-425f60b-JIT/bm-20250329-linux-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.13.0rc2.md)[📈](results/bm-20250329-3.14.0a6%2B-425f60b-JIT/bm-20250329-linux-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.13.0rc2.svg) | 1.001x ↓<br>[📄](results/bm-20250329-3.14.0a6%2B-425f60b-JIT/bm-20250329-linux-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-base.md)[📈](results/bm-20250329-3.14.0a6%2B-425f60b-JIT/bm-20250329-linux-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-base.svg)[🧠](results/bm-20250329-3.14.0a6%2B-425f60b-JIT/bm-20250329-linux-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-base-mem.svg) |
| [2025-03-29](results/bm-20250329-3.14.0a6%2B-425f60b-CLANG) | python/425f60b9eb253c57bc32 | 425f60b (CLANG) | 1.199x ↑<br>[📄](results/bm-20250329-3.14.0a6%2B-425f60b-CLANG/bm-20250329-linux-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.12.6.md)[📈](results/bm-20250329-3.14.0a6%2B-425f60b-CLANG/bm-20250329-linux-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.12.6.svg) | 1.151x ↑<br>[📄](results/bm-20250329-3.14.0a6%2B-425f60b-CLANG/bm-20250329-linux-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.13.0rc2.md)[📈](results/bm-20250329-3.14.0a6%2B-425f60b-CLANG/bm-20250329-linux-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.13.0rc2.svg) | 1.018x ↑<br>[📄](results/bm-20250329-3.14.0a6%2B-425f60b-CLANG/bm-20250329-linux-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-base.md)[📈](results/bm-20250329-3.14.0a6%2B-425f60b-CLANG/bm-20250329-linux-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-base.svg)[🧠](results/bm-20250329-3.14.0a6%2B-425f60b-CLANG/bm-20250329-linux-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-base-mem.svg) |
| [2025-03-29](results/bm-20250329-3.14.0a6%2B-425f60b) | python/425f60b9eb253c57bc32 | 425f60b | 1.174x ↑<br>[📄](results/bm-20250329-3.14.0a6%2B-425f60b/bm-20250329-linux-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.12.6.md)[📈](results/bm-20250329-3.14.0a6%2B-425f60b/bm-20250329-linux-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.12.6.svg) | 1.128x ↑<br>[📄](results/bm-20250329-3.14.0a6%2B-425f60b/bm-20250329-linux-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.13.0rc2.md)[📈](results/bm-20250329-3.14.0a6%2B-425f60b/bm-20250329-linux-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.13.0rc2.svg) |  |

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-04-01](results/bm-20250401-3.14.0a6%2B-395a6d3-NOGIL) | nascheme/gh_127266_type_slots | 395a6d3 (NOGIL) | 1.086x ↓<br>[📄](results/bm-20250401-3.14.0a6%2B-395a6d3-NOGIL/bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6%2B-395a6d3-vs-3.12.6.md)[📈](results/bm-20250401-3.14.0a6%2B-395a6d3-NOGIL/bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6%2B-395a6d3-vs-3.12.6.svg) | 1.116x ↓<br>[📄](results/bm-20250401-3.14.0a6%2B-395a6d3-NOGIL/bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6%2B-395a6d3-vs-3.13.0rc2.md)[📈](results/bm-20250401-3.14.0a6%2B-395a6d3-NOGIL/bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6%2B-395a6d3-vs-3.13.0rc2.svg) | 1.001x ↑<br>[📄](results/bm-20250401-3.14.0a6%2B-395a6d3-NOGIL/bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6%2B-395a6d3-vs-base.md)[📈](results/bm-20250401-3.14.0a6%2B-395a6d3-NOGIL/bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6%2B-395a6d3-vs-base.svg)[🧠](results/bm-20250401-3.14.0a6%2B-395a6d3-NOGIL/bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6%2B-395a6d3-vs-base-mem.svg) |
| [2025-04-01](results/bm-20250401-3.14.0a6%2B-395a6d3) | nascheme/gh_127266_type_slots | 395a6d3 | 1.112x ↑<br>[📄](results/bm-20250401-3.14.0a6%2B-395a6d3/bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6%2B-395a6d3-vs-3.12.6.md)[📈](results/bm-20250401-3.14.0a6%2B-395a6d3/bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6%2B-395a6d3-vs-3.12.6.svg) | 1.071x ↑<br>[📄](results/bm-20250401-3.14.0a6%2B-395a6d3/bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6%2B-395a6d3-vs-3.13.0rc2.md)[📈](results/bm-20250401-3.14.0a6%2B-395a6d3/bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6%2B-395a6d3-vs-3.13.0rc2.svg) | 1.005x ↑<br>[📄](results/bm-20250401-3.14.0a6%2B-395a6d3/bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6%2B-395a6d3-vs-base.md)[📈](results/bm-20250401-3.14.0a6%2B-395a6d3/bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6%2B-395a6d3-vs-base.svg)[🧠](results/bm-20250401-3.14.0a6%2B-395a6d3/bm-20250401-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a6%2B-395a6d3-vs-base-mem.svg) |
| [2025-04-01](results/bm-20250401-3.14.0a6%2B-fe5c4c5-NOGIL) | python/fe5c4c53e7bc6d780686 | fe5c4c5 (NOGIL) | 1.088x ↓<br>[📄](results/bm-20250401-3.14.0a6%2B-fe5c4c5-NOGIL/bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6%2B-fe5c4c5-vs-3.12.6.md)[📈](results/bm-20250401-3.14.0a6%2B-fe5c4c5-NOGIL/bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6%2B-fe5c4c5-vs-3.12.6.svg) | 1.118x ↓<br>[📄](results/bm-20250401-3.14.0a6%2B-fe5c4c5-NOGIL/bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6%2B-fe5c4c5-vs-3.13.0rc2.md)[📈](results/bm-20250401-3.14.0a6%2B-fe5c4c5-NOGIL/bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6%2B-fe5c4c5-vs-3.13.0rc2.svg) | 1.002x ↑<br>[📄](results/bm-20250401-3.14.0a6%2B-fe5c4c5-NOGIL/bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6%2B-fe5c4c5-vs-base.md)[📈](results/bm-20250401-3.14.0a6%2B-fe5c4c5-NOGIL/bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6%2B-fe5c4c5-vs-base.svg)[🧠](results/bm-20250401-3.14.0a6%2B-fe5c4c5-NOGIL/bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6%2B-fe5c4c5-vs-base-mem.svg) |
| [2025-04-01](results/bm-20250401-3.14.0a6%2B-fe5c4c5) | python/fe5c4c53e7bc6d780686 | fe5c4c5 | 1.106x ↑<br>[📄](results/bm-20250401-3.14.0a6%2B-fe5c4c5/bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6%2B-fe5c4c5-vs-3.12.6.md)[📈](results/bm-20250401-3.14.0a6%2B-fe5c4c5/bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6%2B-fe5c4c5-vs-3.12.6.svg) | 1.066x ↑<br>[📄](results/bm-20250401-3.14.0a6%2B-fe5c4c5/bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6%2B-fe5c4c5-vs-3.13.0rc2.md)[📈](results/bm-20250401-3.14.0a6%2B-fe5c4c5/bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6%2B-fe5c4c5-vs-3.13.0rc2.svg) | 1.002x ↑<br>[📄](results/bm-20250401-3.14.0a6%2B-fe5c4c5/bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6%2B-fe5c4c5-vs-base.md)[📈](results/bm-20250401-3.14.0a6%2B-fe5c4c5/bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6%2B-fe5c4c5-vs-base.svg)[🧠](results/bm-20250401-3.14.0a6%2B-fe5c4c5/bm-20250401-vultr-x86_64-python-fe5c4c53e7bc6d780686-3.14.0a6%2B-fe5c4c5-vs-base-mem.svg) |
| [2025-03-31](results/bm-20250331-3.14.0a6%2B-45a3ab5-NOGIL) | python/45a3ab5a81769eadd94d | 45a3ab5 (NOGIL) | 1.089x ↓<br>[📄](results/bm-20250331-3.14.0a6%2B-45a3ab5-NOGIL/bm-20250331-vultr-x86_64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5-vs-3.12.6.md)[📈](results/bm-20250331-3.14.0a6%2B-45a3ab5-NOGIL/bm-20250331-vultr-x86_64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5-vs-3.12.6.svg) | 1.119x ↓<br>[📄](results/bm-20250331-3.14.0a6%2B-45a3ab5-NOGIL/bm-20250331-vultr-x86_64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5-vs-3.13.0rc2.md)[📈](results/bm-20250331-3.14.0a6%2B-45a3ab5-NOGIL/bm-20250331-vultr-x86_64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5-vs-3.13.0rc2.svg) | 1.177x ↓<br>[📄](results/bm-20250331-3.14.0a6%2B-45a3ab5-NOGIL/bm-20250331-vultr-x86_64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5-vs-base.md)[📈](results/bm-20250331-3.14.0a6%2B-45a3ab5-NOGIL/bm-20250331-vultr-x86_64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5-vs-base.svg)[🧠](results/bm-20250331-3.14.0a6%2B-45a3ab5-NOGIL/bm-20250331-vultr-x86_64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5-vs-base-mem.svg) |
| [2025-03-31](results/bm-20250331-3.14.0a6%2B-45a3ab5) | python/45a3ab5a81769eadd94d | 45a3ab5 | 1.103x ↑<br>[📄](results/bm-20250331-3.14.0a6%2B-45a3ab5/bm-20250331-vultr-x86_64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5-vs-3.12.6.md)[📈](results/bm-20250331-3.14.0a6%2B-45a3ab5/bm-20250331-vultr-x86_64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5-vs-3.12.6.svg) | 1.063x ↑<br>[📄](results/bm-20250331-3.14.0a6%2B-45a3ab5/bm-20250331-vultr-x86_64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5-vs-3.13.0rc2.md)[📈](results/bm-20250331-3.14.0a6%2B-45a3ab5/bm-20250331-vultr-x86_64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5-vs-3.13.0rc2.svg) |  |
| [2025-03-30](results/bm-20250330-3.14.0a6%2B-685fd74-NOGIL) | python/685fd74f81e673dc0430 | 685fd74 (NOGIL) | 1.092x ↓<br>[📄](results/bm-20250330-3.14.0a6%2B-685fd74-NOGIL/bm-20250330-vultr-x86_64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74-vs-3.12.6.md)[📈](results/bm-20250330-3.14.0a6%2B-685fd74-NOGIL/bm-20250330-vultr-x86_64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74-vs-3.12.6.svg) | 1.122x ↓<br>[📄](results/bm-20250330-3.14.0a6%2B-685fd74-NOGIL/bm-20250330-vultr-x86_64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74-vs-3.13.0rc2.md)[📈](results/bm-20250330-3.14.0a6%2B-685fd74-NOGIL/bm-20250330-vultr-x86_64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74-vs-3.13.0rc2.svg) | 1.185x ↓<br>[📄](results/bm-20250330-3.14.0a6%2B-685fd74-NOGIL/bm-20250330-vultr-x86_64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74-vs-base.md)[📈](results/bm-20250330-3.14.0a6%2B-685fd74-NOGIL/bm-20250330-vultr-x86_64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74-vs-base.svg)[🧠](results/bm-20250330-3.14.0a6%2B-685fd74-NOGIL/bm-20250330-vultr-x86_64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74-vs-base-mem.svg) |
| [2025-03-30](results/bm-20250330-3.14.0a6%2B-685fd74) | python/685fd74f81e673dc0430 | 685fd74 | 1.111x ↑<br>[📄](results/bm-20250330-3.14.0a6%2B-685fd74/bm-20250330-vultr-x86_64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74-vs-3.12.6.md)[📈](results/bm-20250330-3.14.0a6%2B-685fd74/bm-20250330-vultr-x86_64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74-vs-3.12.6.svg) | 1.070x ↑<br>[📄](results/bm-20250330-3.14.0a6%2B-685fd74/bm-20250330-vultr-x86_64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74-vs-3.13.0rc2.md)[📈](results/bm-20250330-3.14.0a6%2B-685fd74/bm-20250330-vultr-x86_64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74-vs-3.13.0rc2.svg) |  |
| [2025-03-29](results/bm-20250329-3.14.0a6%2B-425f60b-NOGIL) | python/425f60b9eb253c57bc32 | 425f60b (NOGIL) | 1.086x ↓<br>[📄](results/bm-20250329-3.14.0a6%2B-425f60b-NOGIL/bm-20250329-vultr-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.12.6.md)[📈](results/bm-20250329-3.14.0a6%2B-425f60b-NOGIL/bm-20250329-vultr-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.12.6.svg) | 1.117x ↓<br>[📄](results/bm-20250329-3.14.0a6%2B-425f60b-NOGIL/bm-20250329-vultr-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.13.0rc2.md)[📈](results/bm-20250329-3.14.0a6%2B-425f60b-NOGIL/bm-20250329-vultr-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.13.0rc2.svg) | 1.178x ↓<br>[📄](results/bm-20250329-3.14.0a6%2B-425f60b-NOGIL/bm-20250329-vultr-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-base.md)[📈](results/bm-20250329-3.14.0a6%2B-425f60b-NOGIL/bm-20250329-vultr-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-base.svg)[🧠](results/bm-20250329-3.14.0a6%2B-425f60b-NOGIL/bm-20250329-vultr-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-base-mem.svg) |
| [2025-03-29](results/bm-20250329-3.14.0a6%2B-425f60b-JIT) | python/425f60b9eb253c57bc32 | 425f60b (JIT) | 1.094x ↑<br>[📄](results/bm-20250329-3.14.0a6%2B-425f60b-JIT/bm-20250329-vultr-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.12.6.md)[📈](results/bm-20250329-3.14.0a6%2B-425f60b-JIT/bm-20250329-vultr-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.12.6.svg) | 1.055x ↑<br>[📄](results/bm-20250329-3.14.0a6%2B-425f60b-JIT/bm-20250329-vultr-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.13.0rc2.md)[📈](results/bm-20250329-3.14.0a6%2B-425f60b-JIT/bm-20250329-vultr-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.13.0rc2.svg) | 1.014x ↓<br>[📄](results/bm-20250329-3.14.0a6%2B-425f60b-JIT/bm-20250329-vultr-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-base.md)[📈](results/bm-20250329-3.14.0a6%2B-425f60b-JIT/bm-20250329-vultr-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-base.svg)[🧠](results/bm-20250329-3.14.0a6%2B-425f60b-JIT/bm-20250329-vultr-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-base-mem.svg) |
| [2025-03-29](results/bm-20250329-3.14.0a6%2B-425f60b-CLANG) | python/425f60b9eb253c57bc32 | 425f60b (CLANG) | 1.159x ↑<br>[📄](results/bm-20250329-3.14.0a6%2B-425f60b-CLANG/bm-20250329-vultr-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.12.6.md)[📈](results/bm-20250329-3.14.0a6%2B-425f60b-CLANG/bm-20250329-vultr-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.12.6.svg) | 1.118x ↑<br>[📄](results/bm-20250329-3.14.0a6%2B-425f60b-CLANG/bm-20250329-vultr-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.13.0rc2.md)[📈](results/bm-20250329-3.14.0a6%2B-425f60b-CLANG/bm-20250329-vultr-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.13.0rc2.svg) | 1.044x ↑<br>[📄](results/bm-20250329-3.14.0a6%2B-425f60b-CLANG/bm-20250329-vultr-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-base.md)[📈](results/bm-20250329-3.14.0a6%2B-425f60b-CLANG/bm-20250329-vultr-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-base.svg)[🧠](results/bm-20250329-3.14.0a6%2B-425f60b-CLANG/bm-20250329-vultr-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-base-mem.svg) |
| [2025-03-29](results/bm-20250329-3.14.0a6%2B-425f60b) | python/425f60b9eb253c57bc32 | 425f60b | 1.108x ↑<br>[📄](results/bm-20250329-3.14.0a6%2B-425f60b/bm-20250329-vultr-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.12.6.md)[📈](results/bm-20250329-3.14.0a6%2B-425f60b/bm-20250329-vultr-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.12.6.svg) | 1.069x ↑<br>[📄](results/bm-20250329-3.14.0a6%2B-425f60b/bm-20250329-vultr-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.13.0rc2.md)[📈](results/bm-20250329-3.14.0a6%2B-425f60b/bm-20250329-vultr-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.13.0rc2.svg) |  |

## darwin arm64 (macm4pro)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-04-01](results/bm-20250401-3.14.0a6%2B-3a8cefb) | python/3a8cefba0b60bd25c6b1 | 3a8cefb | 1.105x ↑<br>[📄](results/bm-20250401-3.14.0a6%2B-3a8cefb/bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6%2B-3a8cefb-vs-3.12.6.md)[📈](results/bm-20250401-3.14.0a6%2B-3a8cefb/bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6%2B-3a8cefb-vs-3.12.6.svg) | 1.024x ↑<br>[📄](results/bm-20250401-3.14.0a6%2B-3a8cefb/bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6%2B-3a8cefb-vs-3.13.0rc2.md)[📈](results/bm-20250401-3.14.0a6%2B-3a8cefb/bm-20250401-macm4pro-arm64-python-3a8cefba0b60bd25c6b1-3.14.0a6%2B-3a8cefb-vs-3.13.0rc2.svg) |  |
| [2025-03-31](results/bm-20250331-3.14.0a6%2B-45a3ab5-NOGIL) | python/45a3ab5a81769eadd94d | 45a3ab5 (NOGIL) | 1.052x ↓<br>[📄](results/bm-20250331-3.14.0a6%2B-45a3ab5-NOGIL/bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5-vs-3.12.6.md)[📈](results/bm-20250331-3.14.0a6%2B-45a3ab5-NOGIL/bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5-vs-3.12.6.svg) | 1.121x ↓<br>[📄](results/bm-20250331-3.14.0a6%2B-45a3ab5-NOGIL/bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5-vs-3.13.0rc2.md)[📈](results/bm-20250331-3.14.0a6%2B-45a3ab5-NOGIL/bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5-vs-3.13.0rc2.svg) | 1.096x ↓<br>[📄](results/bm-20250331-3.14.0a6%2B-45a3ab5-NOGIL/bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5-vs-base.md)[📈](results/bm-20250331-3.14.0a6%2B-45a3ab5-NOGIL/bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5-vs-base.svg)[🧠](results/bm-20250331-3.14.0a6%2B-45a3ab5-NOGIL/bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5-vs-base-mem.svg) |
| [2025-03-31](results/bm-20250331-3.14.0a6%2B-45a3ab5) | python/45a3ab5a81769eadd94d | 45a3ab5 | 1.046x ↑<br>[📄](results/bm-20250331-3.14.0a6%2B-45a3ab5/bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5-vs-3.12.6.md)[📈](results/bm-20250331-3.14.0a6%2B-45a3ab5/bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5-vs-3.12.6.svg) | 1.030x ↓<br>[📄](results/bm-20250331-3.14.0a6%2B-45a3ab5/bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5-vs-3.13.0rc2.md)[📈](results/bm-20250331-3.14.0a6%2B-45a3ab5/bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5-vs-3.13.0rc2.svg) |  |
| [2025-03-30](results/bm-20250330-3.14.0a6%2B-685fd74-NOGIL) | python/685fd74f81e673dc0430 | 685fd74 (NOGIL) | 1.005x ↑<br>[📄](results/bm-20250330-3.14.0a6%2B-685fd74-NOGIL/bm-20250330-macm4pro-arm64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74-vs-3.12.6.md)[📈](results/bm-20250330-3.14.0a6%2B-685fd74-NOGIL/bm-20250330-macm4pro-arm64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74-vs-3.12.6.svg) | 1.068x ↓<br>[📄](results/bm-20250330-3.14.0a6%2B-685fd74-NOGIL/bm-20250330-macm4pro-arm64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74-vs-3.13.0rc2.md)[📈](results/bm-20250330-3.14.0a6%2B-685fd74-NOGIL/bm-20250330-macm4pro-arm64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74-vs-3.13.0rc2.svg) | 1.036x ↓<br>[📄](results/bm-20250330-3.14.0a6%2B-685fd74-NOGIL/bm-20250330-macm4pro-arm64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74-vs-base.md)[📈](results/bm-20250330-3.14.0a6%2B-685fd74-NOGIL/bm-20250330-macm4pro-arm64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74-vs-base.svg)[🧠](results/bm-20250330-3.14.0a6%2B-685fd74-NOGIL/bm-20250330-macm4pro-arm64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74-vs-base-mem.svg) |
| [2025-03-30](results/bm-20250330-3.14.0a6%2B-685fd74) | python/685fd74f81e673dc0430 | 685fd74 | 1.041x ↑<br>[📄](results/bm-20250330-3.14.0a6%2B-685fd74/bm-20250330-macm4pro-arm64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74-vs-3.12.6.md)[📈](results/bm-20250330-3.14.0a6%2B-685fd74/bm-20250330-macm4pro-arm64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74-vs-3.12.6.svg) | 1.035x ↓<br>[📄](results/bm-20250330-3.14.0a6%2B-685fd74/bm-20250330-macm4pro-arm64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74-vs-3.13.0rc2.md)[📈](results/bm-20250330-3.14.0a6%2B-685fd74/bm-20250330-macm4pro-arm64-python-685fd74f81e673dc0430-3.14.0a6%2B-685fd74-vs-3.13.0rc2.svg) |  |
| [2025-03-29](results/bm-20250329-3.14.0a6%2B-425f60b-NOGIL) | python/425f60b9eb253c57bc32 | 425f60b (NOGIL) | 1.085x ↑<br>[📄](results/bm-20250329-3.14.0a6%2B-425f60b-NOGIL/bm-20250329-macm4pro-arm64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.12.6.md)[📈](results/bm-20250329-3.14.0a6%2B-425f60b-NOGIL/bm-20250329-macm4pro-arm64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.12.6.svg) | 1.006x ↑<br>[📄](results/bm-20250329-3.14.0a6%2B-425f60b-NOGIL/bm-20250329-macm4pro-arm64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.13.0rc2.md)[📈](results/bm-20250329-3.14.0a6%2B-425f60b-NOGIL/bm-20250329-macm4pro-arm64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.13.0rc2.svg) | 1.039x ↑<br>[📄](results/bm-20250329-3.14.0a6%2B-425f60b-NOGIL/bm-20250329-macm4pro-arm64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-base.md)[📈](results/bm-20250329-3.14.0a6%2B-425f60b-NOGIL/bm-20250329-macm4pro-arm64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-base.svg)[🧠](results/bm-20250329-3.14.0a6%2B-425f60b-NOGIL/bm-20250329-macm4pro-arm64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-base-mem.svg) |
| [2025-03-29](results/bm-20250329-3.14.0a6%2B-425f60b-JIT) | python/425f60b9eb253c57bc32 | 425f60b (JIT) | 1.067x ↑<br>[📄](results/bm-20250329-3.14.0a6%2B-425f60b-JIT/bm-20250329-macm4pro-arm64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.12.6.md)[📈](results/bm-20250329-3.14.0a6%2B-425f60b-JIT/bm-20250329-macm4pro-arm64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.12.6.svg) | 1.011x ↓<br>[📄](results/bm-20250329-3.14.0a6%2B-425f60b-JIT/bm-20250329-macm4pro-arm64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.13.0rc2.md)[📈](results/bm-20250329-3.14.0a6%2B-425f60b-JIT/bm-20250329-macm4pro-arm64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.13.0rc2.svg) | 1.022x ↑<br>[📄](results/bm-20250329-3.14.0a6%2B-425f60b-JIT/bm-20250329-macm4pro-arm64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-base.md)[📈](results/bm-20250329-3.14.0a6%2B-425f60b-JIT/bm-20250329-macm4pro-arm64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-base.svg)[🧠](results/bm-20250329-3.14.0a6%2B-425f60b-JIT/bm-20250329-macm4pro-arm64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-base-mem.svg) |
| [2025-03-29](results/bm-20250329-3.14.0a6%2B-425f60b-CLANG) | python/425f60b9eb253c57bc32 | 425f60b (CLANG) | 1.167x ↑<br>[📄](results/bm-20250329-3.14.0a6%2B-425f60b-CLANG/bm-20250329-macm4pro-arm64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.12.6.md)[📈](results/bm-20250329-3.14.0a6%2B-425f60b-CLANG/bm-20250329-macm4pro-arm64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.12.6.svg) | 1.082x ↑<br>[📄](results/bm-20250329-3.14.0a6%2B-425f60b-CLANG/bm-20250329-macm4pro-arm64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.13.0rc2.md)[📈](results/bm-20250329-3.14.0a6%2B-425f60b-CLANG/bm-20250329-macm4pro-arm64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.13.0rc2.svg) | 1.121x ↑<br>[📄](results/bm-20250329-3.14.0a6%2B-425f60b-CLANG/bm-20250329-macm4pro-arm64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-base.md)[📈](results/bm-20250329-3.14.0a6%2B-425f60b-CLANG/bm-20250329-macm4pro-arm64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-base.svg)[🧠](results/bm-20250329-3.14.0a6%2B-425f60b-CLANG/bm-20250329-macm4pro-arm64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-base-mem.svg) |
| [2025-03-29](results/bm-20250329-3.14.0a6%2B-425f60b) | python/425f60b9eb253c57bc32 | 425f60b | 1.044x ↑<br>[📄](results/bm-20250329-3.14.0a6%2B-425f60b/bm-20250329-macm4pro-arm64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.12.6.md)[📈](results/bm-20250329-3.14.0a6%2B-425f60b/bm-20250329-macm4pro-arm64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.12.6.svg) | 1.032x ↓<br>[📄](results/bm-20250329-3.14.0a6%2B-425f60b/bm-20250329-macm4pro-arm64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.13.0rc2.md)[📈](results/bm-20250329-3.14.0a6%2B-425f60b/bm-20250329-macm4pro-arm64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.13.0rc2.svg) |  |


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
