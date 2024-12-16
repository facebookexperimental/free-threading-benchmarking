# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
[Most recent pystats on main (0ac40ac)](results/bm-20241214-3.14.0a2%2B-0ac40ac-PYTHON_UOPS/bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-pystats.md)

## linux x86_64 (linux)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2024-12-15](results/bm-20241215-3.14.0a2%2B-3c144b3-NOGIL) | mpage/gh_115999_for_iter_i | 3c144b3 (NOGIL) | 1.036x ↓<br>[📄](results/bm-20241215-3.14.0a2%2B-3c144b3-NOGIL/bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2%2B-3c144b3-vs-3.12.6.md)[📈](results/bm-20241215-3.14.0a2%2B-3c144b3-NOGIL/bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2%2B-3c144b3-vs-3.12.6.svg) | 1.070x ↓<br>[📄](results/bm-20241215-3.14.0a2%2B-3c144b3-NOGIL/bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2%2B-3c144b3-vs-3.13.0rc2.md)[📈](results/bm-20241215-3.14.0a2%2B-3c144b3-NOGIL/bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2%2B-3c144b3-vs-3.13.0rc2.svg) | 1.132x ↑<br>[📄](results/bm-20241215-3.14.0a2%2B-3c144b3-NOGIL/bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2%2B-3c144b3-vs-base.md)[📈](results/bm-20241215-3.14.0a2%2B-3c144b3-NOGIL/bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2%2B-3c144b3-vs-base.svg)[🧠](results/bm-20241215-3.14.0a2%2B-3c144b3-NOGIL/bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2%2B-3c144b3-vs-base-mem.svg) |
| [2024-12-14](results/bm-20241214-3.14.0a2%2B-0ac40ac) | python/0ac40acec045c4ce780c | 0ac40ac | 1.128x ↑<br>[📄](results/bm-20241214-3.14.0a2%2B-0ac40ac/bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-3.12.6.md)[📈](results/bm-20241214-3.14.0a2%2B-0ac40ac/bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-3.12.6.svg) | 1.084x ↑<br>[📄](results/bm-20241214-3.14.0a2%2B-0ac40ac/bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-3.13.0rc2.md)[📈](results/bm-20241214-3.14.0a2%2B-0ac40ac/bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-3.13.0rc2.svg) |  |
| [2024-12-14](results/bm-20241214-3.14.0a2%2B-0ac40ac-NOGIL) | python/0ac40acec045c4ce780c | 0ac40ac (NOGIL) | 1.156x ↓<br>[📄](results/bm-20241214-3.14.0a2%2B-0ac40ac-NOGIL/bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-3.12.6.md)[📈](results/bm-20241214-3.14.0a2%2B-0ac40ac-NOGIL/bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-3.12.6.svg) | 1.185x ↓<br>[📄](results/bm-20241214-3.14.0a2%2B-0ac40ac-NOGIL/bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-3.13.0rc2.md)[📈](results/bm-20241214-3.14.0a2%2B-0ac40ac-NOGIL/bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-3.13.0rc2.svg) | 1.246x ↓<br>[📄](results/bm-20241214-3.14.0a2%2B-0ac40ac-NOGIL/bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-base.md)[📈](results/bm-20241214-3.14.0a2%2B-0ac40ac-NOGIL/bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-base.svg)[🧠](results/bm-20241214-3.14.0a2%2B-0ac40ac-NOGIL/bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-base-mem.svg) |
| [2024-12-13](results/bm-20241213-3.14.0a2%2B-b7e9a16-NOGIL) | mpage/gh_115999_integrate | b7e9a16 (NOGIL) | 1.043x ↓<br>[📄](results/bm-20241213-3.14.0a2%2B-b7e9a16-NOGIL/bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-3.12.6.md)[📈](results/bm-20241213-3.14.0a2%2B-b7e9a16-NOGIL/bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-3.12.6.svg) | 1.075x ↓<br>[📄](results/bm-20241213-3.14.0a2%2B-b7e9a16-NOGIL/bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-3.13.0rc2.md)[📈](results/bm-20241213-3.14.0a2%2B-b7e9a16-NOGIL/bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-3.13.0rc2.svg) | 1.150x ↑<br>[📄](results/bm-20241213-3.14.0a2%2B-b7e9a16-NOGIL/bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-base.md)[📈](results/bm-20241213-3.14.0a2%2B-b7e9a16-NOGIL/bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-base.svg)[🧠](results/bm-20241213-3.14.0a2%2B-b7e9a16-NOGIL/bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-base-mem.svg) |
| [2024-12-13](results/bm-20241213-3.14.0a2%2B-b7e9a16) | mpage/gh_115999_integrate | b7e9a16 | 1.129x ↑<br>[📄](results/bm-20241213-3.14.0a2%2B-b7e9a16/bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-3.12.6.md)[📈](results/bm-20241213-3.14.0a2%2B-b7e9a16/bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-3.12.6.svg) | 1.080x ↑<br>[📄](results/bm-20241213-3.14.0a2%2B-b7e9a16/bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-3.13.0rc2.md)[📈](results/bm-20241213-3.14.0a2%2B-b7e9a16/bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-3.13.0rc2.svg) | 1.004x ↑<br>[📄](results/bm-20241213-3.14.0a2%2B-b7e9a16/bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-base.md)[📈](results/bm-20241213-3.14.0a2%2B-b7e9a16/bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-base.svg)[🧠](results/bm-20241213-3.14.0a2%2B-b7e9a16/bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-base-mem.svg) |
| [2024-12-13](results/bm-20241213-3.14.0a2%2B-2de048c) | python/2de048ce79e621f5ae05 | 2de048c | 1.128x ↑<br>[📄](results/bm-20241213-3.14.0a2%2B-2de048c/bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2%2B-2de048c-vs-3.12.6.md)[📈](results/bm-20241213-3.14.0a2%2B-2de048c/bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2%2B-2de048c-vs-3.12.6.svg) | 1.084x ↑<br>[📄](results/bm-20241213-3.14.0a2%2B-2de048c/bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2%2B-2de048c-vs-3.13.0rc2.md)[📈](results/bm-20241213-3.14.0a2%2B-2de048c/bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2%2B-2de048c-vs-3.13.0rc2.svg) |  |
| [2024-12-13](results/bm-20241213-3.14.0a2%2B-2de048c-NOGIL) | python/2de048ce79e621f5ae05 | 2de048c (NOGIL) | 1.170x ↓<br>[📄](results/bm-20241213-3.14.0a2%2B-2de048c-NOGIL/bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2%2B-2de048c-vs-3.12.6.md)[📈](results/bm-20241213-3.14.0a2%2B-2de048c-NOGIL/bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2%2B-2de048c-vs-3.12.6.svg) | 1.201x ↓<br>[📄](results/bm-20241213-3.14.0a2%2B-2de048c-NOGIL/bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2%2B-2de048c-vs-3.13.0rc2.md)[📈](results/bm-20241213-3.14.0a2%2B-2de048c-NOGIL/bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2%2B-2de048c-vs-3.13.0rc2.svg) | 1.257x ↓<br>[📄](results/bm-20241213-3.14.0a2%2B-2de048c-NOGIL/bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2%2B-2de048c-vs-base.md)[📈](results/bm-20241213-3.14.0a2%2B-2de048c-NOGIL/bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2%2B-2de048c-vs-base.svg)[🧠](results/bm-20241213-3.14.0a2%2B-2de048c-NOGIL/bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2%2B-2de048c-vs-base-mem.svg) |
| [2024-12-13](results/bm-20241213-3.14.0a2%2B-ba2d2fd) | python/ba2d2fda93a03a91ac6c | ba2d2fd | 1.102x ↑<br>[📄](results/bm-20241213-3.14.0a2%2B-ba2d2fd/bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2%2B-ba2d2fd-vs-3.12.6.md)[📈](results/bm-20241213-3.14.0a2%2B-ba2d2fd/bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2%2B-ba2d2fd-vs-3.12.6.svg) | 1.061x ↑<br>[📄](results/bm-20241213-3.14.0a2%2B-ba2d2fd/bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2%2B-ba2d2fd-vs-3.13.0rc2.md)[📈](results/bm-20241213-3.14.0a2%2B-ba2d2fd/bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2%2B-ba2d2fd-vs-3.13.0rc2.svg) |  |
| [2024-12-13](results/bm-20241213-3.14.0a2%2B-ba2d2fd-NOGIL) | python/ba2d2fda93a03a91ac6c | ba2d2fd (NOGIL) | 1.173x ↓<br>[📄](results/bm-20241213-3.14.0a2%2B-ba2d2fd-NOGIL/bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2%2B-ba2d2fd-vs-3.12.6.md)[📈](results/bm-20241213-3.14.0a2%2B-ba2d2fd-NOGIL/bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2%2B-ba2d2fd-vs-3.12.6.svg) | 1.203x ↓<br>[📄](results/bm-20241213-3.14.0a2%2B-ba2d2fd-NOGIL/bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2%2B-ba2d2fd-vs-3.13.0rc2.md)[📈](results/bm-20241213-3.14.0a2%2B-ba2d2fd-NOGIL/bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2%2B-ba2d2fd-vs-3.13.0rc2.svg) | 1.243x ↓<br>[📄](results/bm-20241213-3.14.0a2%2B-ba2d2fd-NOGIL/bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2%2B-ba2d2fd-vs-base.md)[📈](results/bm-20241213-3.14.0a2%2B-ba2d2fd-NOGIL/bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2%2B-ba2d2fd-vs-base.svg)[🧠](results/bm-20241213-3.14.0a2%2B-ba2d2fd-NOGIL/bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2%2B-ba2d2fd-vs-base-mem.svg) |

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2024-12-15](results/bm-20241215-3.14.0a2%2B-47c5a0f) | python/47c5a0f307cff3ed4775 | 47c5a0f | 1.087x ↑<br>[📄](results/bm-20241215-3.14.0a2%2B-47c5a0f/bm-20241215-vultr-x86_64-python-47c5a0f307cff3ed4775-3.14.0a2%2B-47c5a0f-vs-3.12.6.md)[📈](results/bm-20241215-3.14.0a2%2B-47c5a0f/bm-20241215-vultr-x86_64-python-47c5a0f307cff3ed4775-3.14.0a2%2B-47c5a0f-vs-3.12.6.svg) | 1.048x ↑<br>[📄](results/bm-20241215-3.14.0a2%2B-47c5a0f/bm-20241215-vultr-x86_64-python-47c5a0f307cff3ed4775-3.14.0a2%2B-47c5a0f-vs-3.13.0rc2.md)[📈](results/bm-20241215-3.14.0a2%2B-47c5a0f/bm-20241215-vultr-x86_64-python-47c5a0f307cff3ed4775-3.14.0a2%2B-47c5a0f-vs-3.13.0rc2.svg) |  |
| [2024-12-15](results/bm-20241215-3.14.0a2%2B-3c144b3-NOGIL) | mpage/gh_115999_for_iter_i | 3c144b3 (NOGIL) | 1.080x ↓<br>[📄](results/bm-20241215-3.14.0a2%2B-3c144b3-NOGIL/bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2%2B-3c144b3-vs-3.12.6.md)[📈](results/bm-20241215-3.14.0a2%2B-3c144b3-NOGIL/bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2%2B-3c144b3-vs-3.12.6.svg) | 1.109x ↓<br>[📄](results/bm-20241215-3.14.0a2%2B-3c144b3-NOGIL/bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2%2B-3c144b3-vs-3.13.0rc2.md)[📈](results/bm-20241215-3.14.0a2%2B-3c144b3-NOGIL/bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2%2B-3c144b3-vs-3.13.0rc2.svg) | 1.164x ↑<br>[📄](results/bm-20241215-3.14.0a2%2B-3c144b3-NOGIL/bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2%2B-3c144b3-vs-base.md)[📈](results/bm-20241215-3.14.0a2%2B-3c144b3-NOGIL/bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2%2B-3c144b3-vs-base.svg)[🧠](results/bm-20241215-3.14.0a2%2B-3c144b3-NOGIL/bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2%2B-3c144b3-vs-base-mem.svg) |
| [2024-12-14](results/bm-20241214-3.14.0a2%2B-0ac40ac) | python/0ac40acec045c4ce780c | 0ac40ac | 1.084x ↑<br>[📄](results/bm-20241214-3.14.0a2%2B-0ac40ac/bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-3.12.6.md)[📈](results/bm-20241214-3.14.0a2%2B-0ac40ac/bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-3.12.6.svg) | 1.045x ↑<br>[📄](results/bm-20241214-3.14.0a2%2B-0ac40ac/bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-3.13.0rc2.md)[📈](results/bm-20241214-3.14.0a2%2B-0ac40ac/bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-3.13.0rc2.svg) |  |
| [2024-12-14](results/bm-20241214-3.14.0a2%2B-0ac40ac-NOGIL) | python/0ac40acec045c4ce780c | 0ac40ac (NOGIL) | 1.211x ↓<br>[📄](results/bm-20241214-3.14.0a2%2B-0ac40ac-NOGIL/bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-3.12.6.md)[📈](results/bm-20241214-3.14.0a2%2B-0ac40ac-NOGIL/bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-3.12.6.svg) | 1.237x ↓<br>[📄](results/bm-20241214-3.14.0a2%2B-0ac40ac-NOGIL/bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-3.13.0rc2.md)[📈](results/bm-20241214-3.14.0a2%2B-0ac40ac-NOGIL/bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-3.13.0rc2.svg) | 1.265x ↓<br>[📄](results/bm-20241214-3.14.0a2%2B-0ac40ac-NOGIL/bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-base.md)[📈](results/bm-20241214-3.14.0a2%2B-0ac40ac-NOGIL/bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-base.svg)[🧠](results/bm-20241214-3.14.0a2%2B-0ac40ac-NOGIL/bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-base-mem.svg) |
| [2024-12-13](results/bm-20241213-3.14.0a2%2B-b1ed3ee-NOGIL) | mpage/gh_115999_load_attr_ | b1ed3ee (NOGIL) | 1.115x ↓<br>[📄](results/bm-20241213-3.14.0a2%2B-b1ed3ee-NOGIL/bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-b1ed3ee-vs-3.12.6.md)[📈](results/bm-20241213-3.14.0a2%2B-b1ed3ee-NOGIL/bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-b1ed3ee-vs-3.12.6.svg) | 1.144x ↓<br>[📄](results/bm-20241213-3.14.0a2%2B-b1ed3ee-NOGIL/bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-b1ed3ee-vs-3.13.0rc2.md)[📈](results/bm-20241213-3.14.0a2%2B-b1ed3ee-NOGIL/bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-b1ed3ee-vs-3.13.0rc2.svg) | 1.127x ↑<br>[📄](results/bm-20241213-3.14.0a2%2B-b1ed3ee-NOGIL/bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-b1ed3ee-vs-base.md)[📈](results/bm-20241213-3.14.0a2%2B-b1ed3ee-NOGIL/bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-b1ed3ee-vs-base.svg)[🧠](results/bm-20241213-3.14.0a2%2B-b1ed3ee-NOGIL/bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-b1ed3ee-vs-base-mem.svg) |
| [2024-12-13](results/bm-20241213-3.14.0a2%2B-b1ed3ee) | mpage/gh_115999_load_attr_ | b1ed3ee | 1.091x ↑<br>[📄](results/bm-20241213-3.14.0a2%2B-b1ed3ee/bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-b1ed3ee-vs-3.12.6.md)[📈](results/bm-20241213-3.14.0a2%2B-b1ed3ee/bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-b1ed3ee-vs-3.12.6.svg) | 1.053x ↑<br>[📄](results/bm-20241213-3.14.0a2%2B-b1ed3ee/bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-b1ed3ee-vs-3.13.0rc2.md)[📈](results/bm-20241213-3.14.0a2%2B-b1ed3ee/bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-b1ed3ee-vs-3.13.0rc2.svg) | 1.007x ↑<br>[📄](results/bm-20241213-3.14.0a2%2B-b1ed3ee/bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-b1ed3ee-vs-base.md)[📈](results/bm-20241213-3.14.0a2%2B-b1ed3ee/bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-b1ed3ee-vs-base.svg)[🧠](results/bm-20241213-3.14.0a2%2B-b1ed3ee/bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-b1ed3ee-vs-base-mem.svg) |
| [2024-12-13](results/bm-20241213-3.14.0a2%2B-b7e9a16-NOGIL) | mpage/gh_115999_integrate | b7e9a16 (NOGIL) | 1.084x ↓<br>[📄](results/bm-20241213-3.14.0a2%2B-b7e9a16-NOGIL/bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-3.12.6.md)[📈](results/bm-20241213-3.14.0a2%2B-b7e9a16-NOGIL/bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-3.12.6.svg) | 1.114x ↓<br>[📄](results/bm-20241213-3.14.0a2%2B-b7e9a16-NOGIL/bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-3.13.0rc2.md)[📈](results/bm-20241213-3.14.0a2%2B-b7e9a16-NOGIL/bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-3.13.0rc2.svg) | 1.160x ↑<br>[📄](results/bm-20241213-3.14.0a2%2B-b7e9a16-NOGIL/bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-base.md)[📈](results/bm-20241213-3.14.0a2%2B-b7e9a16-NOGIL/bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-base.svg)[🧠](results/bm-20241213-3.14.0a2%2B-b7e9a16-NOGIL/bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-base-mem.svg) |
| [2024-12-13](results/bm-20241213-3.14.0a2%2B-b7e9a16) | mpage/gh_115999_integrate | b7e9a16 | 1.087x ↑<br>[📄](results/bm-20241213-3.14.0a2%2B-b7e9a16/bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-3.12.6.md)[📈](results/bm-20241213-3.14.0a2%2B-b7e9a16/bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-3.12.6.svg) | 1.048x ↑<br>[📄](results/bm-20241213-3.14.0a2%2B-b7e9a16/bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-3.13.0rc2.md)[📈](results/bm-20241213-3.14.0a2%2B-b7e9a16/bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-3.13.0rc2.svg) | 1.001x ↑<br>[📄](results/bm-20241213-3.14.0a2%2B-b7e9a16/bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-base.md)[📈](results/bm-20241213-3.14.0a2%2B-b7e9a16/bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-base.svg)[🧠](results/bm-20241213-3.14.0a2%2B-b7e9a16/bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-base-mem.svg) |
| [2024-12-13](results/bm-20241213-3.14.0a2%2B-5dd775b-NOGIL) | python/5dd775bed086909722ec | 5dd775b (NOGIL) | 1.219x ↓<br>[📄](results/bm-20241213-3.14.0a2%2B-5dd775b-NOGIL/bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2%2B-5dd775b-vs-3.12.6.md)[📈](results/bm-20241213-3.14.0a2%2B-5dd775b-NOGIL/bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2%2B-5dd775b-vs-3.12.6.svg) | 1.244x ↓<br>[📄](results/bm-20241213-3.14.0a2%2B-5dd775b-NOGIL/bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2%2B-5dd775b-vs-3.13.0rc2.md)[📈](results/bm-20241213-3.14.0a2%2B-5dd775b-NOGIL/bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2%2B-5dd775b-vs-3.13.0rc2.svg) | 1.272x ↓<br>[📄](results/bm-20241213-3.14.0a2%2B-5dd775b-NOGIL/bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2%2B-5dd775b-vs-base.md)[📈](results/bm-20241213-3.14.0a2%2B-5dd775b-NOGIL/bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2%2B-5dd775b-vs-base.svg)[🧠](results/bm-20241213-3.14.0a2%2B-5dd775b-NOGIL/bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2%2B-5dd775b-vs-base-mem.svg) |
| [2024-12-13](results/bm-20241213-3.14.0a2%2B-5dd775b) | python/5dd775bed086909722ec | 5dd775b | 1.083x ↑<br>[📄](results/bm-20241213-3.14.0a2%2B-5dd775b/bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2%2B-5dd775b-vs-3.12.6.md)[📈](results/bm-20241213-3.14.0a2%2B-5dd775b/bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2%2B-5dd775b-vs-3.12.6.svg) | 1.044x ↑<br>[📄](results/bm-20241213-3.14.0a2%2B-5dd775b/bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2%2B-5dd775b-vs-3.13.0rc2.md)[📈](results/bm-20241213-3.14.0a2%2B-5dd775b/bm-20241213-vultr-x86_64-python-5dd775bed086909722ec-3.14.0a2%2B-5dd775b-vs-3.13.0rc2.svg) |  |
| [2024-12-13](results/bm-20241213-3.14.0a2%2B-0e874cd-NOGIL) | mpage/gh_115999_load_attr_ | 0e874cd (NOGIL) | 1.120x ↓<br>[📄](results/bm-20241213-3.14.0a2%2B-0e874cd-NOGIL/bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-0e874cd-vs-3.12.6.md)[📈](results/bm-20241213-3.14.0a2%2B-0e874cd-NOGIL/bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-0e874cd-vs-3.12.6.svg) | 1.149x ↓<br>[📄](results/bm-20241213-3.14.0a2%2B-0e874cd-NOGIL/bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-0e874cd-vs-3.13.0rc2.md)[📈](results/bm-20241213-3.14.0a2%2B-0e874cd-NOGIL/bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-0e874cd-vs-3.13.0rc2.svg) | 1.121x ↑<br>[📄](results/bm-20241213-3.14.0a2%2B-0e874cd-NOGIL/bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-0e874cd-vs-base.md)[📈](results/bm-20241213-3.14.0a2%2B-0e874cd-NOGIL/bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-0e874cd-vs-base.svg)[🧠](results/bm-20241213-3.14.0a2%2B-0e874cd-NOGIL/bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-0e874cd-vs-base-mem.svg) |
| [2024-12-13](results/bm-20241213-3.14.0a2%2B-0e874cd) | mpage/gh_115999_load_attr_ | 0e874cd | 1.088x ↑<br>[📄](results/bm-20241213-3.14.0a2%2B-0e874cd/bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-0e874cd-vs-3.12.6.md)[📈](results/bm-20241213-3.14.0a2%2B-0e874cd/bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-0e874cd-vs-3.12.6.svg) | 1.048x ↑<br>[📄](results/bm-20241213-3.14.0a2%2B-0e874cd/bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-0e874cd-vs-3.13.0rc2.md)[📈](results/bm-20241213-3.14.0a2%2B-0e874cd/bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-0e874cd-vs-3.13.0rc2.svg) | 1.004x ↑<br>[📄](results/bm-20241213-3.14.0a2%2B-0e874cd/bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-0e874cd-vs-base.md)[📈](results/bm-20241213-3.14.0a2%2B-0e874cd/bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-0e874cd-vs-base.svg)[🧠](results/bm-20241213-3.14.0a2%2B-0e874cd/bm-20241213-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-0e874cd-vs-base-mem.svg) |
| [2024-12-13](results/bm-20241213-3.14.0a2%2B-2de048c) | python/2de048ce79e621f5ae05 | 2de048c | 1.083x ↑<br>[📄](results/bm-20241213-3.14.0a2%2B-2de048c/bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2%2B-2de048c-vs-3.12.6.md)[📈](results/bm-20241213-3.14.0a2%2B-2de048c/bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2%2B-2de048c-vs-3.12.6.svg) | 1.044x ↑<br>[📄](results/bm-20241213-3.14.0a2%2B-2de048c/bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2%2B-2de048c-vs-3.13.0rc2.md)[📈](results/bm-20241213-3.14.0a2%2B-2de048c/bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2%2B-2de048c-vs-3.13.0rc2.svg) |  |
| [2024-12-13](results/bm-20241213-3.14.0a2%2B-2de048c-NOGIL) | python/2de048ce79e621f5ae05 | 2de048c (NOGIL) | 1.215x ↓<br>[📄](results/bm-20241213-3.14.0a2%2B-2de048c-NOGIL/bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2%2B-2de048c-vs-3.12.6.md)[📈](results/bm-20241213-3.14.0a2%2B-2de048c-NOGIL/bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2%2B-2de048c-vs-3.12.6.svg) | 1.240x ↓<br>[📄](results/bm-20241213-3.14.0a2%2B-2de048c-NOGIL/bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2%2B-2de048c-vs-3.13.0rc2.md)[📈](results/bm-20241213-3.14.0a2%2B-2de048c-NOGIL/bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2%2B-2de048c-vs-3.13.0rc2.svg) | 1.269x ↓<br>[📄](results/bm-20241213-3.14.0a2%2B-2de048c-NOGIL/bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2%2B-2de048c-vs-base.md)[📈](results/bm-20241213-3.14.0a2%2B-2de048c-NOGIL/bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2%2B-2de048c-vs-base.svg)[🧠](results/bm-20241213-3.14.0a2%2B-2de048c-NOGIL/bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2%2B-2de048c-vs-base-mem.svg) |
| [2024-12-13](results/bm-20241213-3.14.0a2%2B-f920dcd-NOGIL) | nascheme/gh_115999_specialize | f920dcd (NOGIL) | 1.202x ↓<br>[📄](results/bm-20241213-3.14.0a2%2B-f920dcd-NOGIL/bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-f920dcd-vs-3.12.6.md)[📈](results/bm-20241213-3.14.0a2%2B-f920dcd-NOGIL/bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-f920dcd-vs-3.12.6.svg) | 1.228x ↓<br>[📄](results/bm-20241213-3.14.0a2%2B-f920dcd-NOGIL/bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-f920dcd-vs-3.13.0rc2.md)[📈](results/bm-20241213-3.14.0a2%2B-f920dcd-NOGIL/bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-f920dcd-vs-3.13.0rc2.svg) | 1.026x ↑<br>[📄](results/bm-20241213-3.14.0a2%2B-f920dcd-NOGIL/bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-f920dcd-vs-base.md)[📈](results/bm-20241213-3.14.0a2%2B-f920dcd-NOGIL/bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-f920dcd-vs-base.svg)[🧠](results/bm-20241213-3.14.0a2%2B-f920dcd-NOGIL/bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-f920dcd-vs-base-mem.svg) |
| [2024-12-13](results/bm-20241213-3.14.0a2%2B-ba2d2fd) | python/ba2d2fda93a03a91ac6c | ba2d2fd | 1.080x ↑<br>[📄](results/bm-20241213-3.14.0a2%2B-ba2d2fd/bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2%2B-ba2d2fd-vs-3.12.6.md)[📈](results/bm-20241213-3.14.0a2%2B-ba2d2fd/bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2%2B-ba2d2fd-vs-3.12.6.svg) | 1.042x ↑<br>[📄](results/bm-20241213-3.14.0a2%2B-ba2d2fd/bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2%2B-ba2d2fd-vs-3.13.0rc2.md)[📈](results/bm-20241213-3.14.0a2%2B-ba2d2fd/bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2%2B-ba2d2fd-vs-3.13.0rc2.svg) |  |
| [2024-12-13](results/bm-20241213-3.14.0a2%2B-ba2d2fd-NOGIL) | python/ba2d2fda93a03a91ac6c | ba2d2fd (NOGIL) | 1.228x ↓<br>[📄](results/bm-20241213-3.14.0a2%2B-ba2d2fd-NOGIL/bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2%2B-ba2d2fd-vs-3.12.6.md)[📈](results/bm-20241213-3.14.0a2%2B-ba2d2fd-NOGIL/bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2%2B-ba2d2fd-vs-3.12.6.svg) | 1.252x ↓<br>[📄](results/bm-20241213-3.14.0a2%2B-ba2d2fd-NOGIL/bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2%2B-ba2d2fd-vs-3.13.0rc2.md)[📈](results/bm-20241213-3.14.0a2%2B-ba2d2fd-NOGIL/bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2%2B-ba2d2fd-vs-3.13.0rc2.svg) | 1.279x ↓<br>[📄](results/bm-20241213-3.14.0a2%2B-ba2d2fd-NOGIL/bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2%2B-ba2d2fd-vs-base.md)[📈](results/bm-20241213-3.14.0a2%2B-ba2d2fd-NOGIL/bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2%2B-ba2d2fd-vs-base.svg)[🧠](results/bm-20241213-3.14.0a2%2B-ba2d2fd-NOGIL/bm-20241213-vultr-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2%2B-ba2d2fd-vs-base-mem.svg) |
| [2024-12-13](results/bm-20241213-3.14.0a2%2B-d6ea4f1) | nascheme/gh_115999_specialize | d6ea4f1 | 1.082x ↑<br>[📄](results/bm-20241213-3.14.0a2%2B-d6ea4f1/bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-d6ea4f1-vs-3.12.6.md)[📈](results/bm-20241213-3.14.0a2%2B-d6ea4f1/bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-d6ea4f1-vs-3.12.6.svg) | 1.044x ↑<br>[📄](results/bm-20241213-3.14.0a2%2B-d6ea4f1/bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-d6ea4f1-vs-3.13.0rc2.md)[📈](results/bm-20241213-3.14.0a2%2B-d6ea4f1/bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-d6ea4f1-vs-3.13.0rc2.svg) | 1.001x ↑<br>[📄](results/bm-20241213-3.14.0a2%2B-d6ea4f1/bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-d6ea4f1-vs-base.md)[📈](results/bm-20241213-3.14.0a2%2B-d6ea4f1/bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-d6ea4f1-vs-base.svg)[🧠](results/bm-20241213-3.14.0a2%2B-d6ea4f1/bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-d6ea4f1-vs-base-mem.svg) |
| [2024-12-13](results/bm-20241213-3.14.0a2%2B-d6ea4f1-NOGIL) | nascheme/gh_115999_specialize | d6ea4f1 (NOGIL) | 1.197x ↓<br>[📄](results/bm-20241213-3.14.0a2%2B-d6ea4f1-NOGIL/bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-d6ea4f1-vs-3.12.6.md)[📈](results/bm-20241213-3.14.0a2%2B-d6ea4f1-NOGIL/bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-d6ea4f1-vs-3.12.6.svg) | 1.222x ↓<br>[📄](results/bm-20241213-3.14.0a2%2B-d6ea4f1-NOGIL/bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-d6ea4f1-vs-3.13.0rc2.md)[📈](results/bm-20241213-3.14.0a2%2B-d6ea4f1-NOGIL/bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-d6ea4f1-vs-3.13.0rc2.svg) | 1.033x ↑<br>[📄](results/bm-20241213-3.14.0a2%2B-d6ea4f1-NOGIL/bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-d6ea4f1-vs-base.md)[📈](results/bm-20241213-3.14.0a2%2B-d6ea4f1-NOGIL/bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-d6ea4f1-vs-base.svg)[🧠](results/bm-20241213-3.14.0a2%2B-d6ea4f1-NOGIL/bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-d6ea4f1-vs-base-mem.svg) |
| [2024-12-12](results/bm-20241212-3.14.0a2%2B-39cab3f) | mpage/gh_115999_load_attr_ | 39cab3f | 1.080x ↑<br>[📄](results/bm-20241212-3.14.0a2%2B-39cab3f/bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-39cab3f-vs-3.12.6.md)[📈](results/bm-20241212-3.14.0a2%2B-39cab3f/bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-39cab3f-vs-3.12.6.svg) | 1.041x ↑<br>[📄](results/bm-20241212-3.14.0a2%2B-39cab3f/bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-39cab3f-vs-3.13.0rc2.md)[📈](results/bm-20241212-3.14.0a2%2B-39cab3f/bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-39cab3f-vs-3.13.0rc2.svg) | 1.004x ↓<br>[📄](results/bm-20241212-3.14.0a2%2B-39cab3f/bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-39cab3f-vs-base.md)[📈](results/bm-20241212-3.14.0a2%2B-39cab3f/bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-39cab3f-vs-base.svg)[🧠](results/bm-20241212-3.14.0a2%2B-39cab3f/bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-39cab3f-vs-base-mem.svg) |
| [2024-12-12](results/bm-20241212-3.14.0a2%2B-39cab3f-NOGIL) | mpage/gh_115999_load_attr_ | 39cab3f (NOGIL) | 1.136x ↓<br>[📄](results/bm-20241212-3.14.0a2%2B-39cab3f-NOGIL/bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-39cab3f-vs-3.12.6.md)[📈](results/bm-20241212-3.14.0a2%2B-39cab3f-NOGIL/bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-39cab3f-vs-3.12.6.svg) | 1.164x ↓<br>[📄](results/bm-20241212-3.14.0a2%2B-39cab3f-NOGIL/bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-39cab3f-vs-3.13.0rc2.md)[📈](results/bm-20241212-3.14.0a2%2B-39cab3f-NOGIL/bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-39cab3f-vs-3.13.0rc2.svg) | 1.106x ↑<br>[📄](results/bm-20241212-3.14.0a2%2B-39cab3f-NOGIL/bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-39cab3f-vs-base.md)[📈](results/bm-20241212-3.14.0a2%2B-39cab3f-NOGIL/bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-39cab3f-vs-base.svg)[🧠](results/bm-20241212-3.14.0a2%2B-39cab3f-NOGIL/bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2%2B-39cab3f-vs-base-mem.svg) |
| [2024-12-12](results/bm-20241212-3.14.0a2%2B-487fdbe-NOGIL) | python/487fdbed40734fd77214 | 487fdbe (NOGIL) | 1.221x ↓<br>[📄](results/bm-20241212-3.14.0a2%2B-487fdbe-NOGIL/bm-20241212-vultr-x86_64-python-487fdbed40734fd77214-3.14.0a2%2B-487fdbe-vs-3.12.6.md)[📈](results/bm-20241212-3.14.0a2%2B-487fdbe-NOGIL/bm-20241212-vultr-x86_64-python-487fdbed40734fd77214-3.14.0a2%2B-487fdbe-vs-3.12.6.svg) | 1.246x ↓<br>[📄](results/bm-20241212-3.14.0a2%2B-487fdbe-NOGIL/bm-20241212-vultr-x86_64-python-487fdbed40734fd77214-3.14.0a2%2B-487fdbe-vs-3.13.0rc2.md)[📈](results/bm-20241212-3.14.0a2%2B-487fdbe-NOGIL/bm-20241212-vultr-x86_64-python-487fdbed40734fd77214-3.14.0a2%2B-487fdbe-vs-3.13.0rc2.svg) | 1.275x ↓<br>[📄](results/bm-20241212-3.14.0a2%2B-487fdbe-NOGIL/bm-20241212-vultr-x86_64-python-487fdbed40734fd77214-3.14.0a2%2B-487fdbe-vs-base.md)[📈](results/bm-20241212-3.14.0a2%2B-487fdbe-NOGIL/bm-20241212-vultr-x86_64-python-487fdbed40734fd77214-3.14.0a2%2B-487fdbe-vs-base.svg)[🧠](results/bm-20241212-3.14.0a2%2B-487fdbe-NOGIL/bm-20241212-vultr-x86_64-python-487fdbed40734fd77214-3.14.0a2%2B-487fdbe-vs-base-mem.svg) |
| [2024-12-12](results/bm-20241212-3.14.0a2%2B-487fdbe) | python/487fdbed40734fd77214 | 487fdbe | 1.085x ↑<br>[📄](results/bm-20241212-3.14.0a2%2B-487fdbe/bm-20241212-vultr-x86_64-python-487fdbed40734fd77214-3.14.0a2%2B-487fdbe-vs-3.12.6.md)[📈](results/bm-20241212-3.14.0a2%2B-487fdbe/bm-20241212-vultr-x86_64-python-487fdbed40734fd77214-3.14.0a2%2B-487fdbe-vs-3.12.6.svg) | 1.045x ↑<br>[📄](results/bm-20241212-3.14.0a2%2B-487fdbe/bm-20241212-vultr-x86_64-python-487fdbed40734fd77214-3.14.0a2%2B-487fdbe-vs-3.13.0rc2.md)[📈](results/bm-20241212-3.14.0a2%2B-487fdbe/bm-20241212-vultr-x86_64-python-487fdbed40734fd77214-3.14.0a2%2B-487fdbe-vs-3.13.0rc2.svg) |  |


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
