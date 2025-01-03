# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
[Most recent pystats on main (f9a5a3a)](results/bm-20241228-3.14.0a3%2B-f9a5a3a-PYTHON_UOPS/bm-20241228-vultr-x86_64-python-f9a5a3a3ef34e63dc197-3.14.0a3%2B-f9a5a3a-pystats.md)

## linux x86_64 (linux)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-01-01](results/bm-20250101-3.14.0a3%2B-c810ed7-NOGIL) | python/c810ed7c8e0a7464d197 | c810ed7 (NOGIL) | 1.106x ↓<br>[📄](results/bm-20250101-3.14.0a3%2B-c810ed7-NOGIL/bm-20250101-linux-x86_64-python-c810ed7c8e0a7464d197-3.14.0a3%2B-c810ed7-vs-3.12.6.md)[📈](results/bm-20250101-3.14.0a3%2B-c810ed7-NOGIL/bm-20250101-linux-x86_64-python-c810ed7c8e0a7464d197-3.14.0a3%2B-c810ed7-vs-3.12.6.svg) | 1.137x ↓<br>[📄](results/bm-20250101-3.14.0a3%2B-c810ed7-NOGIL/bm-20250101-linux-x86_64-python-c810ed7c8e0a7464d197-3.14.0a3%2B-c810ed7-vs-3.13.0rc2.md)[📈](results/bm-20250101-3.14.0a3%2B-c810ed7-NOGIL/bm-20250101-linux-x86_64-python-c810ed7c8e0a7464d197-3.14.0a3%2B-c810ed7-vs-3.13.0rc2.svg) | 1.201x ↓<br>[📄](results/bm-20250101-3.14.0a3%2B-c810ed7-NOGIL/bm-20250101-linux-x86_64-python-c810ed7c8e0a7464d197-3.14.0a3%2B-c810ed7-vs-base.md)[📈](results/bm-20250101-3.14.0a3%2B-c810ed7-NOGIL/bm-20250101-linux-x86_64-python-c810ed7c8e0a7464d197-3.14.0a3%2B-c810ed7-vs-base.svg)[🧠](results/bm-20250101-3.14.0a3%2B-c810ed7-NOGIL/bm-20250101-linux-x86_64-python-c810ed7c8e0a7464d197-3.14.0a3%2B-c810ed7-vs-base-mem.svg) |
| [2025-01-01](results/bm-20250101-3.14.0a3%2B-c810ed7) | python/c810ed7c8e0a7464d197 | c810ed7 | 1.128x ↑<br>[📄](results/bm-20250101-3.14.0a3%2B-c810ed7/bm-20250101-linux-x86_64-python-c810ed7c8e0a7464d197-3.14.0a3%2B-c810ed7-vs-3.12.6.md)[📈](results/bm-20250101-3.14.0a3%2B-c810ed7/bm-20250101-linux-x86_64-python-c810ed7c8e0a7464d197-3.14.0a3%2B-c810ed7-vs-3.12.6.svg) | 1.086x ↑<br>[📄](results/bm-20250101-3.14.0a3%2B-c810ed7/bm-20250101-linux-x86_64-python-c810ed7c8e0a7464d197-3.14.0a3%2B-c810ed7-vs-3.13.0rc2.md)[📈](results/bm-20250101-3.14.0a3%2B-c810ed7/bm-20250101-linux-x86_64-python-c810ed7c8e0a7464d197-3.14.0a3%2B-c810ed7-vs-3.13.0rc2.svg) |  |
| [2024-12-31](results/bm-20241231-3.14.0a3%2B-c5438fd-NOGIL) | python/c5438fdf4706a70bdd19 | c5438fd (NOGIL) | 1.104x ↓<br>[📄](results/bm-20241231-3.14.0a3%2B-c5438fd-NOGIL/bm-20241231-linux-x86_64-python-c5438fdf4706a70bdd19-3.14.0a3%2B-c5438fd-vs-3.12.6.md)[📈](results/bm-20241231-3.14.0a3%2B-c5438fd-NOGIL/bm-20241231-linux-x86_64-python-c5438fdf4706a70bdd19-3.14.0a3%2B-c5438fd-vs-3.12.6.svg) | 1.136x ↓<br>[📄](results/bm-20241231-3.14.0a3%2B-c5438fd-NOGIL/bm-20241231-linux-x86_64-python-c5438fdf4706a70bdd19-3.14.0a3%2B-c5438fd-vs-3.13.0rc2.md)[📈](results/bm-20241231-3.14.0a3%2B-c5438fd-NOGIL/bm-20241231-linux-x86_64-python-c5438fdf4706a70bdd19-3.14.0a3%2B-c5438fd-vs-3.13.0rc2.svg) | 1.214x ↓<br>[📄](results/bm-20241231-3.14.0a3%2B-c5438fd-NOGIL/bm-20241231-linux-x86_64-python-c5438fdf4706a70bdd19-3.14.0a3%2B-c5438fd-vs-base.md)[📈](results/bm-20241231-3.14.0a3%2B-c5438fd-NOGIL/bm-20241231-linux-x86_64-python-c5438fdf4706a70bdd19-3.14.0a3%2B-c5438fd-vs-base.svg)[🧠](results/bm-20241231-3.14.0a3%2B-c5438fd-NOGIL/bm-20241231-linux-x86_64-python-c5438fdf4706a70bdd19-3.14.0a3%2B-c5438fd-vs-base-mem.svg) |
| [2024-12-31](results/bm-20241231-3.14.0a3%2B-c5438fd) | python/c5438fdf4706a70bdd19 | c5438fd | 1.145x ↑<br>[📄](results/bm-20241231-3.14.0a3%2B-c5438fd/bm-20241231-linux-x86_64-python-c5438fdf4706a70bdd19-3.14.0a3%2B-c5438fd-vs-3.12.6.md)[📈](results/bm-20241231-3.14.0a3%2B-c5438fd/bm-20241231-linux-x86_64-python-c5438fdf4706a70bdd19-3.14.0a3%2B-c5438fd-vs-3.12.6.svg) | 1.100x ↑<br>[📄](results/bm-20241231-3.14.0a3%2B-c5438fd/bm-20241231-linux-x86_64-python-c5438fdf4706a70bdd19-3.14.0a3%2B-c5438fd-vs-3.13.0rc2.md)[📈](results/bm-20241231-3.14.0a3%2B-c5438fd/bm-20241231-linux-x86_64-python-c5438fdf4706a70bdd19-3.14.0a3%2B-c5438fd-vs-3.13.0rc2.svg) |  |
| [2024-12-30](results/bm-20241230-3.14.0a3%2B-dafe7a4) | python/dafe7a44630aa32bb411 | dafe7a4 | 1.139x ↑<br>[📄](results/bm-20241230-3.14.0a3%2B-dafe7a4/bm-20241230-linux-x86_64-python-dafe7a44630aa32bb411-3.14.0a3%2B-dafe7a4-vs-3.12.6.md)[📈](results/bm-20241230-3.14.0a3%2B-dafe7a4/bm-20241230-linux-x86_64-python-dafe7a44630aa32bb411-3.14.0a3%2B-dafe7a4-vs-3.12.6.svg) | 1.096x ↑<br>[📄](results/bm-20241230-3.14.0a3%2B-dafe7a4/bm-20241230-linux-x86_64-python-dafe7a44630aa32bb411-3.14.0a3%2B-dafe7a4-vs-3.13.0rc2.md)[📈](results/bm-20241230-3.14.0a3%2B-dafe7a4/bm-20241230-linux-x86_64-python-dafe7a44630aa32bb411-3.14.0a3%2B-dafe7a4-vs-3.13.0rc2.svg) |  |
| [2024-12-30](results/bm-20241230-3.14.0a3%2B-dafe7a4-NOGIL) | python/dafe7a44630aa32bb411 | dafe7a4 (NOGIL) | 1.106x ↓<br>[📄](results/bm-20241230-3.14.0a3%2B-dafe7a4-NOGIL/bm-20241230-linux-x86_64-python-dafe7a44630aa32bb411-3.14.0a3%2B-dafe7a4-vs-3.12.6.md)[📈](results/bm-20241230-3.14.0a3%2B-dafe7a4-NOGIL/bm-20241230-linux-x86_64-python-dafe7a44630aa32bb411-3.14.0a3%2B-dafe7a4-vs-3.12.6.svg) | 1.139x ↓<br>[📄](results/bm-20241230-3.14.0a3%2B-dafe7a4-NOGIL/bm-20241230-linux-x86_64-python-dafe7a44630aa32bb411-3.14.0a3%2B-dafe7a4-vs-3.13.0rc2.md)[📈](results/bm-20241230-3.14.0a3%2B-dafe7a4-NOGIL/bm-20241230-linux-x86_64-python-dafe7a44630aa32bb411-3.14.0a3%2B-dafe7a4-vs-3.13.0rc2.svg) | 1.213x ↓<br>[📄](results/bm-20241230-3.14.0a3%2B-dafe7a4-NOGIL/bm-20241230-linux-x86_64-python-dafe7a44630aa32bb411-3.14.0a3%2B-dafe7a4-vs-base.md)[📈](results/bm-20241230-3.14.0a3%2B-dafe7a4-NOGIL/bm-20241230-linux-x86_64-python-dafe7a44630aa32bb411-3.14.0a3%2B-dafe7a4-vs-base.svg)[🧠](results/bm-20241230-3.14.0a3%2B-dafe7a4-NOGIL/bm-20241230-linux-x86_64-python-dafe7a44630aa32bb411-3.14.0a3%2B-dafe7a4-vs-base-mem.svg) |

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2025-01-02](results/bm-20250102-3.14.0a3%2B-8b96368) | mpage/gh_115999_load_attr_ | 8b96368 | 1.098x ↑<br>[📄](results/bm-20250102-3.14.0a3%2B-8b96368/bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3%2B-8b96368-vs-3.12.6.md)[📈](results/bm-20250102-3.14.0a3%2B-8b96368/bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3%2B-8b96368-vs-3.12.6.svg) | 1.060x ↑<br>[📄](results/bm-20250102-3.14.0a3%2B-8b96368/bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3%2B-8b96368-vs-3.13.0rc2.md)[📈](results/bm-20250102-3.14.0a3%2B-8b96368/bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3%2B-8b96368-vs-3.13.0rc2.svg) |  |
| [2025-01-01](results/bm-20250101-3.14.0a3%2B-c810ed7-NOGIL) | python/c810ed7c8e0a7464d197 | c810ed7 (NOGIL) | 1.166x ↓<br>[📄](results/bm-20250101-3.14.0a3%2B-c810ed7-NOGIL/bm-20250101-vultr-x86_64-python-c810ed7c8e0a7464d197-3.14.0a3%2B-c810ed7-vs-3.12.6.md)[📈](results/bm-20250101-3.14.0a3%2B-c810ed7-NOGIL/bm-20250101-vultr-x86_64-python-c810ed7c8e0a7464d197-3.14.0a3%2B-c810ed7-vs-3.12.6.svg) | 1.193x ↓<br>[📄](results/bm-20250101-3.14.0a3%2B-c810ed7-NOGIL/bm-20250101-vultr-x86_64-python-c810ed7c8e0a7464d197-3.14.0a3%2B-c810ed7-vs-3.13.0rc2.md)[📈](results/bm-20250101-3.14.0a3%2B-c810ed7-NOGIL/bm-20250101-vultr-x86_64-python-c810ed7c8e0a7464d197-3.14.0a3%2B-c810ed7-vs-3.13.0rc2.svg) | 1.237x ↓<br>[📄](results/bm-20250101-3.14.0a3%2B-c810ed7-NOGIL/bm-20250101-vultr-x86_64-python-c810ed7c8e0a7464d197-3.14.0a3%2B-c810ed7-vs-base.md)[📈](results/bm-20250101-3.14.0a3%2B-c810ed7-NOGIL/bm-20250101-vultr-x86_64-python-c810ed7c8e0a7464d197-3.14.0a3%2B-c810ed7-vs-base.svg)[🧠](results/bm-20250101-3.14.0a3%2B-c810ed7-NOGIL/bm-20250101-vultr-x86_64-python-c810ed7c8e0a7464d197-3.14.0a3%2B-c810ed7-vs-base-mem.svg) |
| [2025-01-01](results/bm-20250101-3.14.0a3%2B-c810ed7) | python/c810ed7c8e0a7464d197 | c810ed7 | 1.099x ↑<br>[📄](results/bm-20250101-3.14.0a3%2B-c810ed7/bm-20250101-vultr-x86_64-python-c810ed7c8e0a7464d197-3.14.0a3%2B-c810ed7-vs-3.12.6.md)[📈](results/bm-20250101-3.14.0a3%2B-c810ed7/bm-20250101-vultr-x86_64-python-c810ed7c8e0a7464d197-3.14.0a3%2B-c810ed7-vs-3.12.6.svg) | 1.060x ↑<br>[📄](results/bm-20250101-3.14.0a3%2B-c810ed7/bm-20250101-vultr-x86_64-python-c810ed7c8e0a7464d197-3.14.0a3%2B-c810ed7-vs-3.13.0rc2.md)[📈](results/bm-20250101-3.14.0a3%2B-c810ed7/bm-20250101-vultr-x86_64-python-c810ed7c8e0a7464d197-3.14.0a3%2B-c810ed7-vs-3.13.0rc2.svg) |  |
| [2025-01-01](results/bm-20250101-3.14.0a3%2B-bb9d955-NOGIL) | python/bb9d955e16c5578bdbc7 | bb9d955 (NOGIL) | 1.165x ↓<br>[📄](results/bm-20250101-3.14.0a3%2B-bb9d955-NOGIL/bm-20250101-vultr-x86_64-python-bb9d955e16c5578bdbc7-3.14.0a3%2B-bb9d955-vs-3.12.6.md)[📈](results/bm-20250101-3.14.0a3%2B-bb9d955-NOGIL/bm-20250101-vultr-x86_64-python-bb9d955e16c5578bdbc7-3.14.0a3%2B-bb9d955-vs-3.12.6.svg) | 1.192x ↓<br>[📄](results/bm-20250101-3.14.0a3%2B-bb9d955-NOGIL/bm-20250101-vultr-x86_64-python-bb9d955e16c5578bdbc7-3.14.0a3%2B-bb9d955-vs-3.13.0rc2.md)[📈](results/bm-20250101-3.14.0a3%2B-bb9d955-NOGIL/bm-20250101-vultr-x86_64-python-bb9d955e16c5578bdbc7-3.14.0a3%2B-bb9d955-vs-3.13.0rc2.svg) |  |
| [2025-01-01](results/bm-20250101-3.14.0a3%2B-41a86a6-NOGIL) | kumaraditya303/asyncio_tsafe | 41a86a6 (NOGIL) | 1.173x ↓<br>[📄](results/bm-20250101-3.14.0a3%2B-41a86a6-NOGIL/bm-20250101-vultr-x86_64-kumaraditya303-asyncio_tsafe-3.14.0a3%2B-41a86a6-vs-3.12.6.md)[📈](results/bm-20250101-3.14.0a3%2B-41a86a6-NOGIL/bm-20250101-vultr-x86_64-kumaraditya303-asyncio_tsafe-3.14.0a3%2B-41a86a6-vs-3.12.6.svg) | 1.200x ↓<br>[📄](results/bm-20250101-3.14.0a3%2B-41a86a6-NOGIL/bm-20250101-vultr-x86_64-kumaraditya303-asyncio_tsafe-3.14.0a3%2B-41a86a6-vs-3.13.0rc2.md)[📈](results/bm-20250101-3.14.0a3%2B-41a86a6-NOGIL/bm-20250101-vultr-x86_64-kumaraditya303-asyncio_tsafe-3.14.0a3%2B-41a86a6-vs-3.13.0rc2.svg) | 1.008x ↓<br>[📄](results/bm-20250101-3.14.0a3%2B-41a86a6-NOGIL/bm-20250101-vultr-x86_64-kumaraditya303-asyncio_tsafe-3.14.0a3%2B-41a86a6-vs-base.md)[📈](results/bm-20250101-3.14.0a3%2B-41a86a6-NOGIL/bm-20250101-vultr-x86_64-kumaraditya303-asyncio_tsafe-3.14.0a3%2B-41a86a6-vs-base.svg)[🧠](results/bm-20250101-3.14.0a3%2B-41a86a6-NOGIL/bm-20250101-vultr-x86_64-kumaraditya303-asyncio_tsafe-3.14.0a3%2B-41a86a6-vs-base-mem.svg) |
| [2024-12-31](results/bm-20241231-3.14.0a3%2B-c5438fd-NOGIL) | python/c5438fdf4706a70bdd19 | c5438fd (NOGIL) | 1.174x ↓<br>[📄](results/bm-20241231-3.14.0a3%2B-c5438fd-NOGIL/bm-20241231-vultr-x86_64-python-c5438fdf4706a70bdd19-3.14.0a3%2B-c5438fd-vs-3.12.6.md)[📈](results/bm-20241231-3.14.0a3%2B-c5438fd-NOGIL/bm-20241231-vultr-x86_64-python-c5438fdf4706a70bdd19-3.14.0a3%2B-c5438fd-vs-3.12.6.svg) | 1.201x ↓<br>[📄](results/bm-20241231-3.14.0a3%2B-c5438fd-NOGIL/bm-20241231-vultr-x86_64-python-c5438fdf4706a70bdd19-3.14.0a3%2B-c5438fd-vs-3.13.0rc2.md)[📈](results/bm-20241231-3.14.0a3%2B-c5438fd-NOGIL/bm-20241231-vultr-x86_64-python-c5438fdf4706a70bdd19-3.14.0a3%2B-c5438fd-vs-3.13.0rc2.svg) | 1.244x ↓<br>[📄](results/bm-20241231-3.14.0a3%2B-c5438fd-NOGIL/bm-20241231-vultr-x86_64-python-c5438fdf4706a70bdd19-3.14.0a3%2B-c5438fd-vs-base.md)[📈](results/bm-20241231-3.14.0a3%2B-c5438fd-NOGIL/bm-20241231-vultr-x86_64-python-c5438fdf4706a70bdd19-3.14.0a3%2B-c5438fd-vs-base.svg)[🧠](results/bm-20241231-3.14.0a3%2B-c5438fd-NOGIL/bm-20241231-vultr-x86_64-python-c5438fdf4706a70bdd19-3.14.0a3%2B-c5438fd-vs-base-mem.svg) |
| [2024-12-31](results/bm-20241231-3.14.0a3%2B-c5438fd) | python/c5438fdf4706a70bdd19 | c5438fd | 1.101x ↑<br>[📄](results/bm-20241231-3.14.0a3%2B-c5438fd/bm-20241231-vultr-x86_64-python-c5438fdf4706a70bdd19-3.14.0a3%2B-c5438fd-vs-3.12.6.md)[📈](results/bm-20241231-3.14.0a3%2B-c5438fd/bm-20241231-vultr-x86_64-python-c5438fdf4706a70bdd19-3.14.0a3%2B-c5438fd-vs-3.12.6.svg) | 1.062x ↑<br>[📄](results/bm-20241231-3.14.0a3%2B-c5438fd/bm-20241231-vultr-x86_64-python-c5438fdf4706a70bdd19-3.14.0a3%2B-c5438fd-vs-3.13.0rc2.md)[📈](results/bm-20241231-3.14.0a3%2B-c5438fd/bm-20241231-vultr-x86_64-python-c5438fdf4706a70bdd19-3.14.0a3%2B-c5438fd-vs-3.13.0rc2.svg) |  |
| [2024-12-30](results/bm-20241230-3.14.0a3%2B-dafe7a4) | python/dafe7a44630aa32bb411 | dafe7a4 | 1.091x ↑<br>[📄](results/bm-20241230-3.14.0a3%2B-dafe7a4/bm-20241230-vultr-x86_64-python-dafe7a44630aa32bb411-3.14.0a3%2B-dafe7a4-vs-3.12.6.md)[📈](results/bm-20241230-3.14.0a3%2B-dafe7a4/bm-20241230-vultr-x86_64-python-dafe7a44630aa32bb411-3.14.0a3%2B-dafe7a4-vs-3.12.6.svg) | 1.052x ↑<br>[📄](results/bm-20241230-3.14.0a3%2B-dafe7a4/bm-20241230-vultr-x86_64-python-dafe7a44630aa32bb411-3.14.0a3%2B-dafe7a4-vs-3.13.0rc2.md)[📈](results/bm-20241230-3.14.0a3%2B-dafe7a4/bm-20241230-vultr-x86_64-python-dafe7a44630aa32bb411-3.14.0a3%2B-dafe7a4-vs-3.13.0rc2.svg) |  |
| [2024-12-30](results/bm-20241230-3.14.0a3%2B-dafe7a4-NOGIL) | python/dafe7a44630aa32bb411 | dafe7a4 (NOGIL) | 1.168x ↓<br>[📄](results/bm-20241230-3.14.0a3%2B-dafe7a4-NOGIL/bm-20241230-vultr-x86_64-python-dafe7a44630aa32bb411-3.14.0a3%2B-dafe7a4-vs-3.12.6.md)[📈](results/bm-20241230-3.14.0a3%2B-dafe7a4-NOGIL/bm-20241230-vultr-x86_64-python-dafe7a44630aa32bb411-3.14.0a3%2B-dafe7a4-vs-3.12.6.svg) | 1.194x ↓<br>[📄](results/bm-20241230-3.14.0a3%2B-dafe7a4-NOGIL/bm-20241230-vultr-x86_64-python-dafe7a44630aa32bb411-3.14.0a3%2B-dafe7a4-vs-3.13.0rc2.md)[📈](results/bm-20241230-3.14.0a3%2B-dafe7a4-NOGIL/bm-20241230-vultr-x86_64-python-dafe7a44630aa32bb411-3.14.0a3%2B-dafe7a4-vs-3.13.0rc2.svg) | 1.233x ↓<br>[📄](results/bm-20241230-3.14.0a3%2B-dafe7a4-NOGIL/bm-20241230-vultr-x86_64-python-dafe7a44630aa32bb411-3.14.0a3%2B-dafe7a4-vs-base.md)[📈](results/bm-20241230-3.14.0a3%2B-dafe7a4-NOGIL/bm-20241230-vultr-x86_64-python-dafe7a44630aa32bb411-3.14.0a3%2B-dafe7a4-vs-base.svg)[🧠](results/bm-20241230-3.14.0a3%2B-dafe7a4-NOGIL/bm-20241230-vultr-x86_64-python-dafe7a44630aa32bb411-3.14.0a3%2B-dafe7a4-vs-base-mem.svg) |


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
