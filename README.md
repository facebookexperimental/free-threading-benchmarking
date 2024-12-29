# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
[Most recent pystats on main (f9a5a3a)](results/bm-20241228-3.14.0a3%2B-f9a5a3a-PYTHON_UOPS/bm-20241228-vultr-x86_64-python-f9a5a3a3ef34e63dc197-3.14.0a3%2B-f9a5a3a-pystats.md)

## linux x86_64 (linux)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2024-12-28](results/bm-20241228-3.14.0a3%2B-f9a5a3a-NOGIL) | python/f9a5a3a3ef34e63dc197 | f9a5a3a (NOGIL) | 1.105x ↓<br>[📄](results/bm-20241228-3.14.0a3%2B-f9a5a3a-NOGIL/bm-20241228-linux-x86_64-python-f9a5a3a3ef34e63dc197-3.14.0a3%2B-f9a5a3a-vs-3.12.6.md)[📈](results/bm-20241228-3.14.0a3%2B-f9a5a3a-NOGIL/bm-20241228-linux-x86_64-python-f9a5a3a3ef34e63dc197-3.14.0a3%2B-f9a5a3a-vs-3.12.6.svg) | 1.136x ↓<br>[📄](results/bm-20241228-3.14.0a3%2B-f9a5a3a-NOGIL/bm-20241228-linux-x86_64-python-f9a5a3a3ef34e63dc197-3.14.0a3%2B-f9a5a3a-vs-3.13.0rc2.md)[📈](results/bm-20241228-3.14.0a3%2B-f9a5a3a-NOGIL/bm-20241228-linux-x86_64-python-f9a5a3a3ef34e63dc197-3.14.0a3%2B-f9a5a3a-vs-3.13.0rc2.svg) | 1.208x ↓<br>[📄](results/bm-20241228-3.14.0a3%2B-f9a5a3a-NOGIL/bm-20241228-linux-x86_64-python-f9a5a3a3ef34e63dc197-3.14.0a3%2B-f9a5a3a-vs-base.md)[📈](results/bm-20241228-3.14.0a3%2B-f9a5a3a-NOGIL/bm-20241228-linux-x86_64-python-f9a5a3a3ef34e63dc197-3.14.0a3%2B-f9a5a3a-vs-base.svg)[🧠](results/bm-20241228-3.14.0a3%2B-f9a5a3a-NOGIL/bm-20241228-linux-x86_64-python-f9a5a3a3ef34e63dc197-3.14.0a3%2B-f9a5a3a-vs-base-mem.svg) |
| [2024-12-28](results/bm-20241228-3.14.0a3%2B-f9a5a3a) | python/f9a5a3a3ef34e63dc197 | f9a5a3a | 1.138x ↑<br>[📄](results/bm-20241228-3.14.0a3%2B-f9a5a3a/bm-20241228-linux-x86_64-python-f9a5a3a3ef34e63dc197-3.14.0a3%2B-f9a5a3a-vs-3.12.6.md)[📈](results/bm-20241228-3.14.0a3%2B-f9a5a3a/bm-20241228-linux-x86_64-python-f9a5a3a3ef34e63dc197-3.14.0a3%2B-f9a5a3a-vs-3.12.6.svg) | 1.092x ↑<br>[📄](results/bm-20241228-3.14.0a3%2B-f9a5a3a/bm-20241228-linux-x86_64-python-f9a5a3a3ef34e63dc197-3.14.0a3%2B-f9a5a3a-vs-3.13.0rc2.md)[📈](results/bm-20241228-3.14.0a3%2B-f9a5a3a/bm-20241228-linux-x86_64-python-f9a5a3a3ef34e63dc197-3.14.0a3%2B-f9a5a3a-vs-3.13.0rc2.svg) |  |
| [2024-12-27](results/bm-20241227-3.14.0a3%2B-aeb9b65) | python/aeb9b65aa26444529e4a | aeb9b65 | 1.155x ↑<br>[📄](results/bm-20241227-3.14.0a3%2B-aeb9b65/bm-20241227-linux-x86_64-python-aeb9b65aa26444529e4a-3.14.0a3%2B-aeb9b65-vs-3.12.6.md)[📈](results/bm-20241227-3.14.0a3%2B-aeb9b65/bm-20241227-linux-x86_64-python-aeb9b65aa26444529e4a-3.14.0a3%2B-aeb9b65-vs-3.12.6.svg) | 1.107x ↑<br>[📄](results/bm-20241227-3.14.0a3%2B-aeb9b65/bm-20241227-linux-x86_64-python-aeb9b65aa26444529e4a-3.14.0a3%2B-aeb9b65-vs-3.13.0rc2.md)[📈](results/bm-20241227-3.14.0a3%2B-aeb9b65/bm-20241227-linux-x86_64-python-aeb9b65aa26444529e4a-3.14.0a3%2B-aeb9b65-vs-3.13.0rc2.svg) |  |
| [2024-12-27](results/bm-20241227-3.14.0a3%2B-aeb9b65-NOGIL) | python/aeb9b65aa26444529e4a | aeb9b65 (NOGIL) | 1.091x ↓<br>[📄](results/bm-20241227-3.14.0a3%2B-aeb9b65-NOGIL/bm-20241227-linux-x86_64-python-aeb9b65aa26444529e4a-3.14.0a3%2B-aeb9b65-vs-3.12.6.md)[📈](results/bm-20241227-3.14.0a3%2B-aeb9b65-NOGIL/bm-20241227-linux-x86_64-python-aeb9b65aa26444529e4a-3.14.0a3%2B-aeb9b65-vs-3.12.6.svg) | 1.124x ↓<br>[📄](results/bm-20241227-3.14.0a3%2B-aeb9b65-NOGIL/bm-20241227-linux-x86_64-python-aeb9b65aa26444529e4a-3.14.0a3%2B-aeb9b65-vs-3.13.0rc2.md)[📈](results/bm-20241227-3.14.0a3%2B-aeb9b65-NOGIL/bm-20241227-linux-x86_64-python-aeb9b65aa26444529e4a-3.14.0a3%2B-aeb9b65-vs-3.13.0rc2.svg) | 1.208x ↓<br>[📄](results/bm-20241227-3.14.0a3%2B-aeb9b65-NOGIL/bm-20241227-linux-x86_64-python-aeb9b65aa26444529e4a-3.14.0a3%2B-aeb9b65-vs-base.md)[📈](results/bm-20241227-3.14.0a3%2B-aeb9b65-NOGIL/bm-20241227-linux-x86_64-python-aeb9b65aa26444529e4a-3.14.0a3%2B-aeb9b65-vs-base.svg)[🧠](results/bm-20241227-3.14.0a3%2B-aeb9b65-NOGIL/bm-20241227-linux-x86_64-python-aeb9b65aa26444529e4a-3.14.0a3%2B-aeb9b65-vs-base-mem.svg) |
| [2024-12-26](results/bm-20241226-3.14.0a3%2B-ea2b537) | python/ea2b53739f1128184b41 | ea2b537 | 1.114x ↑<br>[📄](results/bm-20241226-3.14.0a3%2B-ea2b537/bm-20241226-linux-x86_64-python-ea2b53739f1128184b41-3.14.0a3%2B-ea2b537-vs-3.12.6.md)[📈](results/bm-20241226-3.14.0a3%2B-ea2b537/bm-20241226-linux-x86_64-python-ea2b53739f1128184b41-3.14.0a3%2B-ea2b537-vs-3.12.6.svg) | 1.072x ↑<br>[📄](results/bm-20241226-3.14.0a3%2B-ea2b537/bm-20241226-linux-x86_64-python-ea2b53739f1128184b41-3.14.0a3%2B-ea2b537-vs-3.13.0rc2.md)[📈](results/bm-20241226-3.14.0a3%2B-ea2b537/bm-20241226-linux-x86_64-python-ea2b53739f1128184b41-3.14.0a3%2B-ea2b537-vs-3.13.0rc2.svg) |  |
| [2024-12-26](results/bm-20241226-3.14.0a3%2B-ea2b537-NOGIL) | python/ea2b53739f1128184b41 | ea2b537 (NOGIL) | 1.142x ↓<br>[📄](results/bm-20241226-3.14.0a3%2B-ea2b537-NOGIL/bm-20241226-linux-x86_64-python-ea2b53739f1128184b41-3.14.0a3%2B-ea2b537-vs-3.12.6.md)[📈](results/bm-20241226-3.14.0a3%2B-ea2b537-NOGIL/bm-20241226-linux-x86_64-python-ea2b53739f1128184b41-3.14.0a3%2B-ea2b537-vs-3.12.6.svg) | 1.173x ↓<br>[📄](results/bm-20241226-3.14.0a3%2B-ea2b537-NOGIL/bm-20241226-linux-x86_64-python-ea2b53739f1128184b41-3.14.0a3%2B-ea2b537-vs-3.13.0rc2.md)[📈](results/bm-20241226-3.14.0a3%2B-ea2b537-NOGIL/bm-20241226-linux-x86_64-python-ea2b53739f1128184b41-3.14.0a3%2B-ea2b537-vs-3.13.0rc2.svg) | 1.224x ↓<br>[📄](results/bm-20241226-3.14.0a3%2B-ea2b537-NOGIL/bm-20241226-linux-x86_64-python-ea2b53739f1128184b41-3.14.0a3%2B-ea2b537-vs-base.md)[📈](results/bm-20241226-3.14.0a3%2B-ea2b537-NOGIL/bm-20241226-linux-x86_64-python-ea2b53739f1128184b41-3.14.0a3%2B-ea2b537-vs-base.svg)[🧠](results/bm-20241226-3.14.0a3%2B-ea2b537-NOGIL/bm-20241226-linux-x86_64-python-ea2b53739f1128184b41-3.14.0a3%2B-ea2b537-vs-base-mem.svg) |
| [2024-12-25](results/bm-20241225-3.14.0a3%2B-5c814c8-NOGIL) | python/5c814c83cdd3dc42bd96 | 5c814c8 (NOGIL) | 1.130x ↓<br>[📄](results/bm-20241225-3.14.0a3%2B-5c814c8-NOGIL/bm-20241225-linux-x86_64-python-5c814c83cdd3dc42bd96-3.14.0a3%2B-5c814c8-vs-3.12.6.md)[📈](results/bm-20241225-3.14.0a3%2B-5c814c8-NOGIL/bm-20241225-linux-x86_64-python-5c814c83cdd3dc42bd96-3.14.0a3%2B-5c814c8-vs-3.12.6.svg) | 1.158x ↓<br>[📄](results/bm-20241225-3.14.0a3%2B-5c814c8-NOGIL/bm-20241225-linux-x86_64-python-5c814c83cdd3dc42bd96-3.14.0a3%2B-5c814c8-vs-3.13.0rc2.md)[📈](results/bm-20241225-3.14.0a3%2B-5c814c8-NOGIL/bm-20241225-linux-x86_64-python-5c814c83cdd3dc42bd96-3.14.0a3%2B-5c814c8-vs-3.13.0rc2.svg) | 1.201x ↓<br>[📄](results/bm-20241225-3.14.0a3%2B-5c814c8-NOGIL/bm-20241225-linux-x86_64-python-5c814c83cdd3dc42bd96-3.14.0a3%2B-5c814c8-vs-base.md)[📈](results/bm-20241225-3.14.0a3%2B-5c814c8-NOGIL/bm-20241225-linux-x86_64-python-5c814c83cdd3dc42bd96-3.14.0a3%2B-5c814c8-vs-base.svg)[🧠](results/bm-20241225-3.14.0a3%2B-5c814c8-NOGIL/bm-20241225-linux-x86_64-python-5c814c83cdd3dc42bd96-3.14.0a3%2B-5c814c8-vs-base-mem.svg) |
| [2024-12-25](results/bm-20241225-3.14.0a3%2B-5c814c8) | python/5c814c83cdd3dc42bd96 | 5c814c8 | 1.100x ↑<br>[📄](results/bm-20241225-3.14.0a3%2B-5c814c8/bm-20241225-linux-x86_64-python-5c814c83cdd3dc42bd96-3.14.0a3%2B-5c814c8-vs-3.12.6.md)[📈](results/bm-20241225-3.14.0a3%2B-5c814c8/bm-20241225-linux-x86_64-python-5c814c83cdd3dc42bd96-3.14.0a3%2B-5c814c8-vs-3.12.6.svg) | 1.056x ↑<br>[📄](results/bm-20241225-3.14.0a3%2B-5c814c8/bm-20241225-linux-x86_64-python-5c814c83cdd3dc42bd96-3.14.0a3%2B-5c814c8-vs-3.13.0rc2.md)[📈](results/bm-20241225-3.14.0a3%2B-5c814c8/bm-20241225-linux-x86_64-python-5c814c83cdd3dc42bd96-3.14.0a3%2B-5c814c8-vs-3.13.0rc2.svg) |  |

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2024-12-28](results/bm-20241228-3.14.0a3%2B-f9a5a3a-NOGIL) | python/f9a5a3a3ef34e63dc197 | f9a5a3a (NOGIL) | 1.174x ↓<br>[📄](results/bm-20241228-3.14.0a3%2B-f9a5a3a-NOGIL/bm-20241228-vultr-x86_64-python-f9a5a3a3ef34e63dc197-3.14.0a3%2B-f9a5a3a-vs-3.12.6.md)[📈](results/bm-20241228-3.14.0a3%2B-f9a5a3a-NOGIL/bm-20241228-vultr-x86_64-python-f9a5a3a3ef34e63dc197-3.14.0a3%2B-f9a5a3a-vs-3.12.6.svg) | 1.201x ↓<br>[📄](results/bm-20241228-3.14.0a3%2B-f9a5a3a-NOGIL/bm-20241228-vultr-x86_64-python-f9a5a3a3ef34e63dc197-3.14.0a3%2B-f9a5a3a-vs-3.13.0rc2.md)[📈](results/bm-20241228-3.14.0a3%2B-f9a5a3a-NOGIL/bm-20241228-vultr-x86_64-python-f9a5a3a3ef34e63dc197-3.14.0a3%2B-f9a5a3a-vs-3.13.0rc2.svg) | 1.239x ↓<br>[📄](results/bm-20241228-3.14.0a3%2B-f9a5a3a-NOGIL/bm-20241228-vultr-x86_64-python-f9a5a3a3ef34e63dc197-3.14.0a3%2B-f9a5a3a-vs-base.md)[📈](results/bm-20241228-3.14.0a3%2B-f9a5a3a-NOGIL/bm-20241228-vultr-x86_64-python-f9a5a3a3ef34e63dc197-3.14.0a3%2B-f9a5a3a-vs-base.svg)[🧠](results/bm-20241228-3.14.0a3%2B-f9a5a3a-NOGIL/bm-20241228-vultr-x86_64-python-f9a5a3a3ef34e63dc197-3.14.0a3%2B-f9a5a3a-vs-base-mem.svg) |
| [2024-12-28](results/bm-20241228-3.14.0a3%2B-f9a5a3a) | python/f9a5a3a3ef34e63dc197 | f9a5a3a | 1.092x ↑<br>[📄](results/bm-20241228-3.14.0a3%2B-f9a5a3a/bm-20241228-vultr-x86_64-python-f9a5a3a3ef34e63dc197-3.14.0a3%2B-f9a5a3a-vs-3.12.6.md)[📈](results/bm-20241228-3.14.0a3%2B-f9a5a3a/bm-20241228-vultr-x86_64-python-f9a5a3a3ef34e63dc197-3.14.0a3%2B-f9a5a3a-vs-3.12.6.svg) | 1.053x ↑<br>[📄](results/bm-20241228-3.14.0a3%2B-f9a5a3a/bm-20241228-vultr-x86_64-python-f9a5a3a3ef34e63dc197-3.14.0a3%2B-f9a5a3a-vs-3.13.0rc2.md)[📈](results/bm-20241228-3.14.0a3%2B-f9a5a3a/bm-20241228-vultr-x86_64-python-f9a5a3a3ef34e63dc197-3.14.0a3%2B-f9a5a3a-vs-3.13.0rc2.svg) |  |
| [2024-12-27](results/bm-20241227-3.14.0a3%2B-aeb9b65) | python/aeb9b65aa26444529e4a | aeb9b65 | 1.092x ↑<br>[📄](results/bm-20241227-3.14.0a3%2B-aeb9b65/bm-20241227-vultr-x86_64-python-aeb9b65aa26444529e4a-3.14.0a3%2B-aeb9b65-vs-3.12.6.md)[📈](results/bm-20241227-3.14.0a3%2B-aeb9b65/bm-20241227-vultr-x86_64-python-aeb9b65aa26444529e4a-3.14.0a3%2B-aeb9b65-vs-3.12.6.svg) | 1.054x ↑<br>[📄](results/bm-20241227-3.14.0a3%2B-aeb9b65/bm-20241227-vultr-x86_64-python-aeb9b65aa26444529e4a-3.14.0a3%2B-aeb9b65-vs-3.13.0rc2.md)[📈](results/bm-20241227-3.14.0a3%2B-aeb9b65/bm-20241227-vultr-x86_64-python-aeb9b65aa26444529e4a-3.14.0a3%2B-aeb9b65-vs-3.13.0rc2.svg) |  |
| [2024-12-27](results/bm-20241227-3.14.0a3%2B-aeb9b65-NOGIL) | python/aeb9b65aa26444529e4a | aeb9b65 (NOGIL) | 1.167x ↓<br>[📄](results/bm-20241227-3.14.0a3%2B-aeb9b65-NOGIL/bm-20241227-vultr-x86_64-python-aeb9b65aa26444529e4a-3.14.0a3%2B-aeb9b65-vs-3.12.6.md)[📈](results/bm-20241227-3.14.0a3%2B-aeb9b65-NOGIL/bm-20241227-vultr-x86_64-python-aeb9b65aa26444529e4a-3.14.0a3%2B-aeb9b65-vs-3.12.6.svg) | 1.193x ↓<br>[📄](results/bm-20241227-3.14.0a3%2B-aeb9b65-NOGIL/bm-20241227-vultr-x86_64-python-aeb9b65aa26444529e4a-3.14.0a3%2B-aeb9b65-vs-3.13.0rc2.md)[📈](results/bm-20241227-3.14.0a3%2B-aeb9b65-NOGIL/bm-20241227-vultr-x86_64-python-aeb9b65aa26444529e4a-3.14.0a3%2B-aeb9b65-vs-3.13.0rc2.svg) | 1.232x ↓<br>[📄](results/bm-20241227-3.14.0a3%2B-aeb9b65-NOGIL/bm-20241227-vultr-x86_64-python-aeb9b65aa26444529e4a-3.14.0a3%2B-aeb9b65-vs-base.md)[📈](results/bm-20241227-3.14.0a3%2B-aeb9b65-NOGIL/bm-20241227-vultr-x86_64-python-aeb9b65aa26444529e4a-3.14.0a3%2B-aeb9b65-vs-base.svg)[🧠](results/bm-20241227-3.14.0a3%2B-aeb9b65-NOGIL/bm-20241227-vultr-x86_64-python-aeb9b65aa26444529e4a-3.14.0a3%2B-aeb9b65-vs-base-mem.svg) |
| [2024-12-26](results/bm-20241226-3.14.0a3%2B-ea2b537) | python/ea2b53739f1128184b41 | ea2b537 | 1.091x ↑<br>[📄](results/bm-20241226-3.14.0a3%2B-ea2b537/bm-20241226-vultr-x86_64-python-ea2b53739f1128184b41-3.14.0a3%2B-ea2b537-vs-3.12.6.md)[📈](results/bm-20241226-3.14.0a3%2B-ea2b537/bm-20241226-vultr-x86_64-python-ea2b53739f1128184b41-3.14.0a3%2B-ea2b537-vs-3.12.6.svg) | 1.053x ↑<br>[📄](results/bm-20241226-3.14.0a3%2B-ea2b537/bm-20241226-vultr-x86_64-python-ea2b53739f1128184b41-3.14.0a3%2B-ea2b537-vs-3.13.0rc2.md)[📈](results/bm-20241226-3.14.0a3%2B-ea2b537/bm-20241226-vultr-x86_64-python-ea2b53739f1128184b41-3.14.0a3%2B-ea2b537-vs-3.13.0rc2.svg) |  |
| [2024-12-26](results/bm-20241226-3.14.0a3%2B-ea2b537-NOGIL) | python/ea2b53739f1128184b41 | ea2b537 (NOGIL) | 1.162x ↓<br>[📄](results/bm-20241226-3.14.0a3%2B-ea2b537-NOGIL/bm-20241226-vultr-x86_64-python-ea2b53739f1128184b41-3.14.0a3%2B-ea2b537-vs-3.12.6.md)[📈](results/bm-20241226-3.14.0a3%2B-ea2b537-NOGIL/bm-20241226-vultr-x86_64-python-ea2b53739f1128184b41-3.14.0a3%2B-ea2b537-vs-3.12.6.svg) | 1.189x ↓<br>[📄](results/bm-20241226-3.14.0a3%2B-ea2b537-NOGIL/bm-20241226-vultr-x86_64-python-ea2b53739f1128184b41-3.14.0a3%2B-ea2b537-vs-3.13.0rc2.md)[📈](results/bm-20241226-3.14.0a3%2B-ea2b537-NOGIL/bm-20241226-vultr-x86_64-python-ea2b53739f1128184b41-3.14.0a3%2B-ea2b537-vs-3.13.0rc2.svg) | 1.228x ↓<br>[📄](results/bm-20241226-3.14.0a3%2B-ea2b537-NOGIL/bm-20241226-vultr-x86_64-python-ea2b53739f1128184b41-3.14.0a3%2B-ea2b537-vs-base.md)[📈](results/bm-20241226-3.14.0a3%2B-ea2b537-NOGIL/bm-20241226-vultr-x86_64-python-ea2b53739f1128184b41-3.14.0a3%2B-ea2b537-vs-base.svg)[🧠](results/bm-20241226-3.14.0a3%2B-ea2b537-NOGIL/bm-20241226-vultr-x86_64-python-ea2b53739f1128184b41-3.14.0a3%2B-ea2b537-vs-base-mem.svg) |
| [2024-12-25](results/bm-20241225-3.14.0a3%2B-5c814c8-NOGIL) | python/5c814c83cdd3dc42bd96 | 5c814c8 (NOGIL) | 1.170x ↓<br>[📄](results/bm-20241225-3.14.0a3%2B-5c814c8-NOGIL/bm-20241225-vultr-x86_64-python-5c814c83cdd3dc42bd96-3.14.0a3%2B-5c814c8-vs-3.12.6.md)[📈](results/bm-20241225-3.14.0a3%2B-5c814c8-NOGIL/bm-20241225-vultr-x86_64-python-5c814c83cdd3dc42bd96-3.14.0a3%2B-5c814c8-vs-3.12.6.svg) | 1.197x ↓<br>[📄](results/bm-20241225-3.14.0a3%2B-5c814c8-NOGIL/bm-20241225-vultr-x86_64-python-5c814c83cdd3dc42bd96-3.14.0a3%2B-5c814c8-vs-3.13.0rc2.md)[📈](results/bm-20241225-3.14.0a3%2B-5c814c8-NOGIL/bm-20241225-vultr-x86_64-python-5c814c83cdd3dc42bd96-3.14.0a3%2B-5c814c8-vs-3.13.0rc2.svg) | 1.238x ↓<br>[📄](results/bm-20241225-3.14.0a3%2B-5c814c8-NOGIL/bm-20241225-vultr-x86_64-python-5c814c83cdd3dc42bd96-3.14.0a3%2B-5c814c8-vs-base.md)[📈](results/bm-20241225-3.14.0a3%2B-5c814c8-NOGIL/bm-20241225-vultr-x86_64-python-5c814c83cdd3dc42bd96-3.14.0a3%2B-5c814c8-vs-base.svg)[🧠](results/bm-20241225-3.14.0a3%2B-5c814c8-NOGIL/bm-20241225-vultr-x86_64-python-5c814c83cdd3dc42bd96-3.14.0a3%2B-5c814c8-vs-base-mem.svg) |
| [2024-12-25](results/bm-20241225-3.14.0a3%2B-5c814c8) | python/5c814c83cdd3dc42bd96 | 5c814c8 | 1.097x ↑<br>[📄](results/bm-20241225-3.14.0a3%2B-5c814c8/bm-20241225-vultr-x86_64-python-5c814c83cdd3dc42bd96-3.14.0a3%2B-5c814c8-vs-3.12.6.md)[📈](results/bm-20241225-3.14.0a3%2B-5c814c8/bm-20241225-vultr-x86_64-python-5c814c83cdd3dc42bd96-3.14.0a3%2B-5c814c8-vs-3.12.6.svg) | 1.058x ↑<br>[📄](results/bm-20241225-3.14.0a3%2B-5c814c8/bm-20241225-vultr-x86_64-python-5c814c83cdd3dc42bd96-3.14.0a3%2B-5c814c8-vs-3.13.0rc2.md)[📈](results/bm-20241225-3.14.0a3%2B-5c814c8/bm-20241225-vultr-x86_64-python-5c814c83cdd3dc42bd96-3.14.0a3%2B-5c814c8-vs-3.13.0rc2.svg) |  |


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
