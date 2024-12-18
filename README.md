# Faster CPython Benchmark Infrastructure

🔒 [▶️ START A BENCHMARK RUN](../../actions/workflows/benchmark.yml)

## Results

Here are some recent and important revisions. 👉 [Complete list of results](RESULTS.md).

<!-- START table -->
[Most recent pystats on main (0ac40ac)](results/bm-20241214-3.14.0a2%2B-0ac40ac-PYTHON_UOPS/bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-pystats.md)

## linux x86_64 (linux)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2024-12-18](results/bm-20241218-3.14.0a3%2B-b92f101-NOGIL) | python/b92f101d0f19a1df3205 | b92f101 (NOGIL) | 1.163x ↓<br>[📄](results/bm-20241218-3.14.0a3%2B-b92f101-NOGIL/bm-20241218-linux-x86_64-python-b92f101d0f19a1df3205-3.14.0a3%2B-b92f101-vs-3.12.6.md)[📈](results/bm-20241218-3.14.0a3%2B-b92f101-NOGIL/bm-20241218-linux-x86_64-python-b92f101d0f19a1df3205-3.14.0a3%2B-b92f101-vs-3.12.6.svg) | 1.192x ↓<br>[📄](results/bm-20241218-3.14.0a3%2B-b92f101-NOGIL/bm-20241218-linux-x86_64-python-b92f101d0f19a1df3205-3.14.0a3%2B-b92f101-vs-3.13.0rc2.md)[📈](results/bm-20241218-3.14.0a3%2B-b92f101-NOGIL/bm-20241218-linux-x86_64-python-b92f101d0f19a1df3205-3.14.0a3%2B-b92f101-vs-3.13.0rc2.svg) | 1.236x ↓<br>[📄](results/bm-20241218-3.14.0a3%2B-b92f101-NOGIL/bm-20241218-linux-x86_64-python-b92f101d0f19a1df3205-3.14.0a3%2B-b92f101-vs-base.md)[📈](results/bm-20241218-3.14.0a3%2B-b92f101-NOGIL/bm-20241218-linux-x86_64-python-b92f101d0f19a1df3205-3.14.0a3%2B-b92f101-vs-base.svg)[🧠](results/bm-20241218-3.14.0a3%2B-b92f101-NOGIL/bm-20241218-linux-x86_64-python-b92f101d0f19a1df3205-3.14.0a3%2B-b92f101-vs-base-mem.svg) |
| [2024-12-18](results/bm-20241218-3.14.0a3%2B-b92f101) | python/b92f101d0f19a1df3205 | b92f101 | 1.105x ↑<br>[📄](results/bm-20241218-3.14.0a3%2B-b92f101/bm-20241218-linux-x86_64-python-b92f101d0f19a1df3205-3.14.0a3%2B-b92f101-vs-3.12.6.md)[📈](results/bm-20241218-3.14.0a3%2B-b92f101/bm-20241218-linux-x86_64-python-b92f101d0f19a1df3205-3.14.0a3%2B-b92f101-vs-3.12.6.svg) | 1.064x ↑<br>[📄](results/bm-20241218-3.14.0a3%2B-b92f101/bm-20241218-linux-x86_64-python-b92f101d0f19a1df3205-3.14.0a3%2B-b92f101-vs-3.13.0rc2.md)[📈](results/bm-20241218-3.14.0a3%2B-b92f101/bm-20241218-linux-x86_64-python-b92f101d0f19a1df3205-3.14.0a3%2B-b92f101-vs-3.13.0rc2.svg) |  |
| [2024-12-16](results/bm-20241216-3.14.0a2%2B-cfeaa99) | python/cfeaa992ba9bad9be268 | cfeaa99 | 1.118x ↑<br>[📄](results/bm-20241216-3.14.0a2%2B-cfeaa99/bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2%2B-cfeaa99-vs-3.12.6.md)[📈](results/bm-20241216-3.14.0a2%2B-cfeaa99/bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2%2B-cfeaa99-vs-3.12.6.svg) | 1.072x ↑<br>[📄](results/bm-20241216-3.14.0a2%2B-cfeaa99/bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2%2B-cfeaa99-vs-3.13.0rc2.md)[📈](results/bm-20241216-3.14.0a2%2B-cfeaa99/bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2%2B-cfeaa99-vs-3.13.0rc2.svg) |  |
| [2024-12-16](results/bm-20241216-3.14.0a2%2B-cfeaa99-NOGIL) | python/cfeaa992ba9bad9be268 | cfeaa99 (NOGIL) | 1.158x ↓<br>[📄](results/bm-20241216-3.14.0a2%2B-cfeaa99-NOGIL/bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2%2B-cfeaa99-vs-3.12.6.md)[📈](results/bm-20241216-3.14.0a2%2B-cfeaa99-NOGIL/bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2%2B-cfeaa99-vs-3.12.6.svg) | 1.186x ↓<br>[📄](results/bm-20241216-3.14.0a2%2B-cfeaa99-NOGIL/bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2%2B-cfeaa99-vs-3.13.0rc2.md)[📈](results/bm-20241216-3.14.0a2%2B-cfeaa99-NOGIL/bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2%2B-cfeaa99-vs-3.13.0rc2.svg) | 1.240x ↓<br>[📄](results/bm-20241216-3.14.0a2%2B-cfeaa99-NOGIL/bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2%2B-cfeaa99-vs-base.md)[📈](results/bm-20241216-3.14.0a2%2B-cfeaa99-NOGIL/bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2%2B-cfeaa99-vs-base.svg)[🧠](results/bm-20241216-3.14.0a2%2B-cfeaa99-NOGIL/bm-20241216-linux-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2%2B-cfeaa99-vs-base-mem.svg) |
| [2024-12-15](results/bm-20241215-3.14.0a2%2B-47c5a0f) | python/47c5a0f307cff3ed4775 | 47c5a0f | 1.125x ↑<br>[📄](results/bm-20241215-3.14.0a2%2B-47c5a0f/bm-20241215-linux-x86_64-python-47c5a0f307cff3ed4775-3.14.0a2%2B-47c5a0f-vs-3.12.6.md)[📈](results/bm-20241215-3.14.0a2%2B-47c5a0f/bm-20241215-linux-x86_64-python-47c5a0f307cff3ed4775-3.14.0a2%2B-47c5a0f-vs-3.12.6.svg) | 1.080x ↑<br>[📄](results/bm-20241215-3.14.0a2%2B-47c5a0f/bm-20241215-linux-x86_64-python-47c5a0f307cff3ed4775-3.14.0a2%2B-47c5a0f-vs-3.13.0rc2.md)[📈](results/bm-20241215-3.14.0a2%2B-47c5a0f/bm-20241215-linux-x86_64-python-47c5a0f307cff3ed4775-3.14.0a2%2B-47c5a0f-vs-3.13.0rc2.svg) |  |
| [2024-12-15](results/bm-20241215-3.14.0a2%2B-47c5a0f-NOGIL) | python/47c5a0f307cff3ed4775 | 47c5a0f (NOGIL) | 1.150x ↓<br>[📄](results/bm-20241215-3.14.0a2%2B-47c5a0f-NOGIL/bm-20241215-linux-x86_64-python-47c5a0f307cff3ed4775-3.14.0a2%2B-47c5a0f-vs-3.12.6.md)[📈](results/bm-20241215-3.14.0a2%2B-47c5a0f-NOGIL/bm-20241215-linux-x86_64-python-47c5a0f307cff3ed4775-3.14.0a2%2B-47c5a0f-vs-3.12.6.svg) | 1.180x ↓<br>[📄](results/bm-20241215-3.14.0a2%2B-47c5a0f-NOGIL/bm-20241215-linux-x86_64-python-47c5a0f307cff3ed4775-3.14.0a2%2B-47c5a0f-vs-3.13.0rc2.md)[📈](results/bm-20241215-3.14.0a2%2B-47c5a0f-NOGIL/bm-20241215-linux-x86_64-python-47c5a0f307cff3ed4775-3.14.0a2%2B-47c5a0f-vs-3.13.0rc2.svg) | 1.238x ↓<br>[📄](results/bm-20241215-3.14.0a2%2B-47c5a0f-NOGIL/bm-20241215-linux-x86_64-python-47c5a0f307cff3ed4775-3.14.0a2%2B-47c5a0f-vs-base.md)[📈](results/bm-20241215-3.14.0a2%2B-47c5a0f-NOGIL/bm-20241215-linux-x86_64-python-47c5a0f307cff3ed4775-3.14.0a2%2B-47c5a0f-vs-base.svg)[🧠](results/bm-20241215-3.14.0a2%2B-47c5a0f-NOGIL/bm-20241215-linux-x86_64-python-47c5a0f307cff3ed4775-3.14.0a2%2B-47c5a0f-vs-base-mem.svg) |
| [2024-12-15](results/bm-20241215-3.14.0a2%2B-3c144b3-NOGIL) | mpage/gh_115999_for_iter_i | 3c144b3 (NOGIL) | 1.036x ↓<br>[📄](results/bm-20241215-3.14.0a2%2B-3c144b3-NOGIL/bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2%2B-3c144b3-vs-3.12.6.md)[📈](results/bm-20241215-3.14.0a2%2B-3c144b3-NOGIL/bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2%2B-3c144b3-vs-3.12.6.svg) | 1.070x ↓<br>[📄](results/bm-20241215-3.14.0a2%2B-3c144b3-NOGIL/bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2%2B-3c144b3-vs-3.13.0rc2.md)[📈](results/bm-20241215-3.14.0a2%2B-3c144b3-NOGIL/bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2%2B-3c144b3-vs-3.13.0rc2.svg) | 1.132x ↑<br>[📄](results/bm-20241215-3.14.0a2%2B-3c144b3-NOGIL/bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2%2B-3c144b3-vs-base.md)[📈](results/bm-20241215-3.14.0a2%2B-3c144b3-NOGIL/bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2%2B-3c144b3-vs-base.svg)[🧠](results/bm-20241215-3.14.0a2%2B-3c144b3-NOGIL/bm-20241215-linux-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2%2B-3c144b3-vs-base-mem.svg) |
| [2024-12-14](results/bm-20241214-3.14.0a2%2B-0ac40ac) | python/0ac40acec045c4ce780c | 0ac40ac | 1.128x ↑<br>[📄](results/bm-20241214-3.14.0a2%2B-0ac40ac/bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-3.12.6.md)[📈](results/bm-20241214-3.14.0a2%2B-0ac40ac/bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-3.12.6.svg) | 1.084x ↑<br>[📄](results/bm-20241214-3.14.0a2%2B-0ac40ac/bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-3.13.0rc2.md)[📈](results/bm-20241214-3.14.0a2%2B-0ac40ac/bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-3.13.0rc2.svg) |  |
| [2024-12-14](results/bm-20241214-3.14.0a2%2B-0ac40ac-NOGIL) | python/0ac40acec045c4ce780c | 0ac40ac (NOGIL) | 1.156x ↓<br>[📄](results/bm-20241214-3.14.0a2%2B-0ac40ac-NOGIL/bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-3.12.6.md)[📈](results/bm-20241214-3.14.0a2%2B-0ac40ac-NOGIL/bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-3.12.6.svg) | 1.185x ↓<br>[📄](results/bm-20241214-3.14.0a2%2B-0ac40ac-NOGIL/bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-3.13.0rc2.md)[📈](results/bm-20241214-3.14.0a2%2B-0ac40ac-NOGIL/bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-3.13.0rc2.svg) | 1.246x ↓<br>[📄](results/bm-20241214-3.14.0a2%2B-0ac40ac-NOGIL/bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-base.md)[📈](results/bm-20241214-3.14.0a2%2B-0ac40ac-NOGIL/bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-base.svg)[🧠](results/bm-20241214-3.14.0a2%2B-0ac40ac-NOGIL/bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-base-mem.svg) |
| [2024-12-13](results/bm-20241213-3.14.0a2%2B-b7e9a16-NOGIL) | mpage/gh_115999_integrate | b7e9a16 (NOGIL) | 1.043x ↓<br>[📄](results/bm-20241213-3.14.0a2%2B-b7e9a16-NOGIL/bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-3.12.6.md)[📈](results/bm-20241213-3.14.0a2%2B-b7e9a16-NOGIL/bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-3.12.6.svg) | 1.075x ↓<br>[📄](results/bm-20241213-3.14.0a2%2B-b7e9a16-NOGIL/bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-3.13.0rc2.md)[📈](results/bm-20241213-3.14.0a2%2B-b7e9a16-NOGIL/bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-3.13.0rc2.svg) | 1.150x ↑<br>[📄](results/bm-20241213-3.14.0a2%2B-b7e9a16-NOGIL/bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-base.md)[📈](results/bm-20241213-3.14.0a2%2B-b7e9a16-NOGIL/bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-base.svg)[🧠](results/bm-20241213-3.14.0a2%2B-b7e9a16-NOGIL/bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-base-mem.svg) |
| [2024-12-13](results/bm-20241213-3.14.0a2%2B-b7e9a16) | mpage/gh_115999_integrate | b7e9a16 | 1.129x ↑<br>[📄](results/bm-20241213-3.14.0a2%2B-b7e9a16/bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-3.12.6.md)[📈](results/bm-20241213-3.14.0a2%2B-b7e9a16/bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-3.12.6.svg) | 1.080x ↑<br>[📄](results/bm-20241213-3.14.0a2%2B-b7e9a16/bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-3.13.0rc2.md)[📈](results/bm-20241213-3.14.0a2%2B-b7e9a16/bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-3.13.0rc2.svg) | 1.004x ↑<br>[📄](results/bm-20241213-3.14.0a2%2B-b7e9a16/bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-base.md)[📈](results/bm-20241213-3.14.0a2%2B-b7e9a16/bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-base.svg)[🧠](results/bm-20241213-3.14.0a2%2B-b7e9a16/bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-base-mem.svg) |
| [2024-12-13](results/bm-20241213-3.14.0a2%2B-2de048c) | python/2de048ce79e621f5ae05 | 2de048c | 1.128x ↑<br>[📄](results/bm-20241213-3.14.0a2%2B-2de048c/bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2%2B-2de048c-vs-3.12.6.md)[📈](results/bm-20241213-3.14.0a2%2B-2de048c/bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2%2B-2de048c-vs-3.12.6.svg) | 1.084x ↑<br>[📄](results/bm-20241213-3.14.0a2%2B-2de048c/bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2%2B-2de048c-vs-3.13.0rc2.md)[📈](results/bm-20241213-3.14.0a2%2B-2de048c/bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2%2B-2de048c-vs-3.13.0rc2.svg) |  |
| [2024-12-13](results/bm-20241213-3.14.0a2%2B-2de048c-NOGIL) | python/2de048ce79e621f5ae05 | 2de048c (NOGIL) | 1.170x ↓<br>[📄](results/bm-20241213-3.14.0a2%2B-2de048c-NOGIL/bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2%2B-2de048c-vs-3.12.6.md)[📈](results/bm-20241213-3.14.0a2%2B-2de048c-NOGIL/bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2%2B-2de048c-vs-3.12.6.svg) | 1.201x ↓<br>[📄](results/bm-20241213-3.14.0a2%2B-2de048c-NOGIL/bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2%2B-2de048c-vs-3.13.0rc2.md)[📈](results/bm-20241213-3.14.0a2%2B-2de048c-NOGIL/bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2%2B-2de048c-vs-3.13.0rc2.svg) | 1.257x ↓<br>[📄](results/bm-20241213-3.14.0a2%2B-2de048c-NOGIL/bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2%2B-2de048c-vs-base.md)[📈](results/bm-20241213-3.14.0a2%2B-2de048c-NOGIL/bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2%2B-2de048c-vs-base.svg)[🧠](results/bm-20241213-3.14.0a2%2B-2de048c-NOGIL/bm-20241213-linux-x86_64-python-2de048ce79e621f5ae05-3.14.0a2%2B-2de048c-vs-base-mem.svg) |

## linux x86_64 (vultr)
| date | fork/ref | hash/flags | vs. 3.12.6: | vs. 3.13.0rc2: | vs. base: |
| --- | --- | --- | ---: | ---: | ---: |
| [2024-12-18](results/bm-20241218-3.14.0a3%2B-b92f101-NOGIL) | python/b92f101d0f19a1df3205 | b92f101 (NOGIL) | 1.214x ↓<br>[📄](results/bm-20241218-3.14.0a3%2B-b92f101-NOGIL/bm-20241218-vultr-x86_64-python-b92f101d0f19a1df3205-3.14.0a3%2B-b92f101-vs-3.12.6.md)[📈](results/bm-20241218-3.14.0a3%2B-b92f101-NOGIL/bm-20241218-vultr-x86_64-python-b92f101d0f19a1df3205-3.14.0a3%2B-b92f101-vs-3.12.6.svg) | 1.240x ↓<br>[📄](results/bm-20241218-3.14.0a3%2B-b92f101-NOGIL/bm-20241218-vultr-x86_64-python-b92f101d0f19a1df3205-3.14.0a3%2B-b92f101-vs-3.13.0rc2.md)[📈](results/bm-20241218-3.14.0a3%2B-b92f101-NOGIL/bm-20241218-vultr-x86_64-python-b92f101d0f19a1df3205-3.14.0a3%2B-b92f101-vs-3.13.0rc2.svg) | 1.269x ↓<br>[📄](results/bm-20241218-3.14.0a3%2B-b92f101-NOGIL/bm-20241218-vultr-x86_64-python-b92f101d0f19a1df3205-3.14.0a3%2B-b92f101-vs-base.md)[📈](results/bm-20241218-3.14.0a3%2B-b92f101-NOGIL/bm-20241218-vultr-x86_64-python-b92f101d0f19a1df3205-3.14.0a3%2B-b92f101-vs-base.svg)[🧠](results/bm-20241218-3.14.0a3%2B-b92f101-NOGIL/bm-20241218-vultr-x86_64-python-b92f101d0f19a1df3205-3.14.0a3%2B-b92f101-vs-base-mem.svg) |
| [2024-12-18](results/bm-20241218-3.14.0a3%2B-b92f101) | python/b92f101d0f19a1df3205 | b92f101 | 1.085x ↑<br>[📄](results/bm-20241218-3.14.0a3%2B-b92f101/bm-20241218-vultr-x86_64-python-b92f101d0f19a1df3205-3.14.0a3%2B-b92f101-vs-3.12.6.md)[📈](results/bm-20241218-3.14.0a3%2B-b92f101/bm-20241218-vultr-x86_64-python-b92f101d0f19a1df3205-3.14.0a3%2B-b92f101-vs-3.12.6.svg) | 1.046x ↑<br>[📄](results/bm-20241218-3.14.0a3%2B-b92f101/bm-20241218-vultr-x86_64-python-b92f101d0f19a1df3205-3.14.0a3%2B-b92f101-vs-3.13.0rc2.md)[📈](results/bm-20241218-3.14.0a3%2B-b92f101/bm-20241218-vultr-x86_64-python-b92f101d0f19a1df3205-3.14.0a3%2B-b92f101-vs-3.13.0rc2.svg) |  |
| [2024-12-17](results/bm-20241217-3.14.0a2%2B-699f4e9-NOGIL) | nascheme/gh_115999_specialize | 699f4e9 (NOGIL) | 1.206x ↓<br>[📄](results/bm-20241217-3.14.0a2%2B-699f4e9-NOGIL/bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-699f4e9-vs-3.12.6.md)[📈](results/bm-20241217-3.14.0a2%2B-699f4e9-NOGIL/bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-699f4e9-vs-3.12.6.svg) | 1.231x ↓<br>[📄](results/bm-20241217-3.14.0a2%2B-699f4e9-NOGIL/bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-699f4e9-vs-3.13.0rc2.md)[📈](results/bm-20241217-3.14.0a2%2B-699f4e9-NOGIL/bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-699f4e9-vs-3.13.0rc2.svg) | 1.012x ↑<br>[📄](results/bm-20241217-3.14.0a2%2B-699f4e9-NOGIL/bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-699f4e9-vs-base.md)[📈](results/bm-20241217-3.14.0a2%2B-699f4e9-NOGIL/bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-699f4e9-vs-base.svg)[🧠](results/bm-20241217-3.14.0a2%2B-699f4e9-NOGIL/bm-20241217-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-699f4e9-vs-base-mem.svg) |
| [2024-12-17](results/bm-20241217-3.14.0a2%2B-3aa9426) | corona10/gh_115999_BINARY_SUB | 3aa9426 | 1.061x ↑<br>[📄](results/bm-20241217-3.14.0a2%2B-3aa9426/bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-3aa9426-vs-3.12.6.md)[📈](results/bm-20241217-3.14.0a2%2B-3aa9426/bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-3aa9426-vs-3.12.6.svg) | 1.022x ↑<br>[📄](results/bm-20241217-3.14.0a2%2B-3aa9426/bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-3aa9426-vs-3.13.0rc2.md)[📈](results/bm-20241217-3.14.0a2%2B-3aa9426/bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-3aa9426-vs-3.13.0rc2.svg) | 1.004x ↓<br>[📄](results/bm-20241217-3.14.0a2%2B-3aa9426/bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-3aa9426-vs-base.md)[📈](results/bm-20241217-3.14.0a2%2B-3aa9426/bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-3aa9426-vs-base.svg)[🧠](results/bm-20241217-3.14.0a2%2B-3aa9426/bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-3aa9426-vs-base-mem.svg) |
| [2024-12-17](results/bm-20241217-3.14.0a2%2B-3aa9426-NOGIL) | corona10/gh_115999_BINARY_SUB | 3aa9426 (NOGIL) | 1.226x ↓<br>[📄](results/bm-20241217-3.14.0a2%2B-3aa9426-NOGIL/bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-3aa9426-vs-3.12.6.md)[📈](results/bm-20241217-3.14.0a2%2B-3aa9426-NOGIL/bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-3aa9426-vs-3.12.6.svg) | 1.250x ↓<br>[📄](results/bm-20241217-3.14.0a2%2B-3aa9426-NOGIL/bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-3aa9426-vs-3.13.0rc2.md)[📈](results/bm-20241217-3.14.0a2%2B-3aa9426-NOGIL/bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-3aa9426-vs-3.13.0rc2.svg) | 1.006x ↑<br>[📄](results/bm-20241217-3.14.0a2%2B-3aa9426-NOGIL/bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-3aa9426-vs-base.md)[📈](results/bm-20241217-3.14.0a2%2B-3aa9426-NOGIL/bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-3aa9426-vs-base.svg)[🧠](results/bm-20241217-3.14.0a2%2B-3aa9426-NOGIL/bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-3aa9426-vs-base-mem.svg) |
| [2024-12-17](results/bm-20241217-3.14.0a2%2B-7b72e7b-NOGIL) | corona10/gh_115999_BINARY_SUB | 7b72e7b (NOGIL) | 1.224x ↓<br>[📄](results/bm-20241217-3.14.0a2%2B-7b72e7b-NOGIL/bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-7b72e7b-vs-3.12.6.md)[📈](results/bm-20241217-3.14.0a2%2B-7b72e7b-NOGIL/bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-7b72e7b-vs-3.12.6.svg) | 1.249x ↓<br>[📄](results/bm-20241217-3.14.0a2%2B-7b72e7b-NOGIL/bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-7b72e7b-vs-3.13.0rc2.md)[📈](results/bm-20241217-3.14.0a2%2B-7b72e7b-NOGIL/bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-7b72e7b-vs-3.13.0rc2.svg) | 1.008x ↑<br>[📄](results/bm-20241217-3.14.0a2%2B-7b72e7b-NOGIL/bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-7b72e7b-vs-base.md)[📈](results/bm-20241217-3.14.0a2%2B-7b72e7b-NOGIL/bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-7b72e7b-vs-base.svg)[🧠](results/bm-20241217-3.14.0a2%2B-7b72e7b-NOGIL/bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-7b72e7b-vs-base-mem.svg) |
| [2024-12-17](results/bm-20241217-3.14.0a2%2B-7b72e7b) | corona10/gh_115999_BINARY_SUB | 7b72e7b | 1.066x ↑<br>[📄](results/bm-20241217-3.14.0a2%2B-7b72e7b/bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-7b72e7b-vs-3.12.6.md)[📈](results/bm-20241217-3.14.0a2%2B-7b72e7b/bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-7b72e7b-vs-3.12.6.svg) | 1.027x ↑<br>[📄](results/bm-20241217-3.14.0a2%2B-7b72e7b/bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-7b72e7b-vs-3.13.0rc2.md)[📈](results/bm-20241217-3.14.0a2%2B-7b72e7b/bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-7b72e7b-vs-3.13.0rc2.svg) | 1.000x ↑<br>[📄](results/bm-20241217-3.14.0a2%2B-7b72e7b/bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-7b72e7b-vs-base.md)[📈](results/bm-20241217-3.14.0a2%2B-7b72e7b/bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-7b72e7b-vs-base.svg)[🧠](results/bm-20241217-3.14.0a2%2B-7b72e7b/bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2%2B-7b72e7b-vs-base-mem.svg) |
| [2024-12-16](results/bm-20241216-3.14.0a2%2B-cfeaa99) | python/cfeaa992ba9bad9be268 | cfeaa99 | 1.088x ↑<br>[📄](results/bm-20241216-3.14.0a2%2B-cfeaa99/bm-20241216-vultr-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2%2B-cfeaa99-vs-3.12.6.md)[📈](results/bm-20241216-3.14.0a2%2B-cfeaa99/bm-20241216-vultr-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2%2B-cfeaa99-vs-3.12.6.svg) | 1.049x ↑<br>[📄](results/bm-20241216-3.14.0a2%2B-cfeaa99/bm-20241216-vultr-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2%2B-cfeaa99-vs-3.13.0rc2.md)[📈](results/bm-20241216-3.14.0a2%2B-cfeaa99/bm-20241216-vultr-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2%2B-cfeaa99-vs-3.13.0rc2.svg) |  |
| [2024-12-16](results/bm-20241216-3.14.0a2%2B-cfeaa99-NOGIL) | python/cfeaa992ba9bad9be268 | cfeaa99 (NOGIL) | 1.212x ↓<br>[📄](results/bm-20241216-3.14.0a2%2B-cfeaa99-NOGIL/bm-20241216-vultr-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2%2B-cfeaa99-vs-3.12.6.md)[📈](results/bm-20241216-3.14.0a2%2B-cfeaa99-NOGIL/bm-20241216-vultr-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2%2B-cfeaa99-vs-3.12.6.svg) | 1.237x ↓<br>[📄](results/bm-20241216-3.14.0a2%2B-cfeaa99-NOGIL/bm-20241216-vultr-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2%2B-cfeaa99-vs-3.13.0rc2.md)[📈](results/bm-20241216-3.14.0a2%2B-cfeaa99-NOGIL/bm-20241216-vultr-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2%2B-cfeaa99-vs-3.13.0rc2.svg) | 1.269x ↓<br>[📄](results/bm-20241216-3.14.0a2%2B-cfeaa99-NOGIL/bm-20241216-vultr-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2%2B-cfeaa99-vs-base.md)[📈](results/bm-20241216-3.14.0a2%2B-cfeaa99-NOGIL/bm-20241216-vultr-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2%2B-cfeaa99-vs-base.svg)[🧠](results/bm-20241216-3.14.0a2%2B-cfeaa99-NOGIL/bm-20241216-vultr-x86_64-python-cfeaa992ba9bad9be268-3.14.0a2%2B-cfeaa99-vs-base-mem.svg) |
| [2024-12-15](results/bm-20241215-3.14.0a2%2B-47c5a0f) | python/47c5a0f307cff3ed4775 | 47c5a0f | 1.087x ↑<br>[📄](results/bm-20241215-3.14.0a2%2B-47c5a0f/bm-20241215-vultr-x86_64-python-47c5a0f307cff3ed4775-3.14.0a2%2B-47c5a0f-vs-3.12.6.md)[📈](results/bm-20241215-3.14.0a2%2B-47c5a0f/bm-20241215-vultr-x86_64-python-47c5a0f307cff3ed4775-3.14.0a2%2B-47c5a0f-vs-3.12.6.svg) | 1.048x ↑<br>[📄](results/bm-20241215-3.14.0a2%2B-47c5a0f/bm-20241215-vultr-x86_64-python-47c5a0f307cff3ed4775-3.14.0a2%2B-47c5a0f-vs-3.13.0rc2.md)[📈](results/bm-20241215-3.14.0a2%2B-47c5a0f/bm-20241215-vultr-x86_64-python-47c5a0f307cff3ed4775-3.14.0a2%2B-47c5a0f-vs-3.13.0rc2.svg) |  |
| [2024-12-15](results/bm-20241215-3.14.0a2%2B-47c5a0f-NOGIL) | python/47c5a0f307cff3ed4775 | 47c5a0f (NOGIL) | 1.215x ↓<br>[📄](results/bm-20241215-3.14.0a2%2B-47c5a0f-NOGIL/bm-20241215-vultr-x86_64-python-47c5a0f307cff3ed4775-3.14.0a2%2B-47c5a0f-vs-3.12.6.md)[📈](results/bm-20241215-3.14.0a2%2B-47c5a0f-NOGIL/bm-20241215-vultr-x86_64-python-47c5a0f307cff3ed4775-3.14.0a2%2B-47c5a0f-vs-3.12.6.svg) | 1.240x ↓<br>[📄](results/bm-20241215-3.14.0a2%2B-47c5a0f-NOGIL/bm-20241215-vultr-x86_64-python-47c5a0f307cff3ed4775-3.14.0a2%2B-47c5a0f-vs-3.13.0rc2.md)[📈](results/bm-20241215-3.14.0a2%2B-47c5a0f-NOGIL/bm-20241215-vultr-x86_64-python-47c5a0f307cff3ed4775-3.14.0a2%2B-47c5a0f-vs-3.13.0rc2.svg) | 1.271x ↓<br>[📄](results/bm-20241215-3.14.0a2%2B-47c5a0f-NOGIL/bm-20241215-vultr-x86_64-python-47c5a0f307cff3ed4775-3.14.0a2%2B-47c5a0f-vs-base.md)[📈](results/bm-20241215-3.14.0a2%2B-47c5a0f-NOGIL/bm-20241215-vultr-x86_64-python-47c5a0f307cff3ed4775-3.14.0a2%2B-47c5a0f-vs-base.svg)[🧠](results/bm-20241215-3.14.0a2%2B-47c5a0f-NOGIL/bm-20241215-vultr-x86_64-python-47c5a0f307cff3ed4775-3.14.0a2%2B-47c5a0f-vs-base-mem.svg) |
| [2024-12-15](results/bm-20241215-3.14.0a2%2B-3c144b3-NOGIL) | mpage/gh_115999_for_iter_i | 3c144b3 (NOGIL) | 1.080x ↓<br>[📄](results/bm-20241215-3.14.0a2%2B-3c144b3-NOGIL/bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2%2B-3c144b3-vs-3.12.6.md)[📈](results/bm-20241215-3.14.0a2%2B-3c144b3-NOGIL/bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2%2B-3c144b3-vs-3.12.6.svg) | 1.109x ↓<br>[📄](results/bm-20241215-3.14.0a2%2B-3c144b3-NOGIL/bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2%2B-3c144b3-vs-3.13.0rc2.md)[📈](results/bm-20241215-3.14.0a2%2B-3c144b3-NOGIL/bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2%2B-3c144b3-vs-3.13.0rc2.svg) | 1.164x ↑<br>[📄](results/bm-20241215-3.14.0a2%2B-3c144b3-NOGIL/bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2%2B-3c144b3-vs-base.md)[📈](results/bm-20241215-3.14.0a2%2B-3c144b3-NOGIL/bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2%2B-3c144b3-vs-base.svg)[🧠](results/bm-20241215-3.14.0a2%2B-3c144b3-NOGIL/bm-20241215-vultr-x86_64-mpage-gh_115999_for_iter_i-3.14.0a2%2B-3c144b3-vs-base-mem.svg) |
| [2024-12-14](results/bm-20241214-3.14.0a2%2B-0ac40ac) | python/0ac40acec045c4ce780c | 0ac40ac | 1.084x ↑<br>[📄](results/bm-20241214-3.14.0a2%2B-0ac40ac/bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-3.12.6.md)[📈](results/bm-20241214-3.14.0a2%2B-0ac40ac/bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-3.12.6.svg) | 1.045x ↑<br>[📄](results/bm-20241214-3.14.0a2%2B-0ac40ac/bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-3.13.0rc2.md)[📈](results/bm-20241214-3.14.0a2%2B-0ac40ac/bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-3.13.0rc2.svg) |  |
| [2024-12-14](results/bm-20241214-3.14.0a2%2B-0ac40ac-NOGIL) | python/0ac40acec045c4ce780c | 0ac40ac (NOGIL) | 1.211x ↓<br>[📄](results/bm-20241214-3.14.0a2%2B-0ac40ac-NOGIL/bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-3.12.6.md)[📈](results/bm-20241214-3.14.0a2%2B-0ac40ac-NOGIL/bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-3.12.6.svg) | 1.237x ↓<br>[📄](results/bm-20241214-3.14.0a2%2B-0ac40ac-NOGIL/bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-3.13.0rc2.md)[📈](results/bm-20241214-3.14.0a2%2B-0ac40ac-NOGIL/bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-3.13.0rc2.svg) | 1.265x ↓<br>[📄](results/bm-20241214-3.14.0a2%2B-0ac40ac-NOGIL/bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-base.md)[📈](results/bm-20241214-3.14.0a2%2B-0ac40ac-NOGIL/bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-base.svg)[🧠](results/bm-20241214-3.14.0a2%2B-0ac40ac-NOGIL/bm-20241214-vultr-x86_64-python-0ac40acec045c4ce780c-3.14.0a2%2B-0ac40ac-vs-base-mem.svg) |
| [2024-12-13](results/bm-20241213-3.14.0a2%2B-b7e9a16-NOGIL) | mpage/gh_115999_integrate | b7e9a16 (NOGIL) | 1.084x ↓<br>[📄](results/bm-20241213-3.14.0a2%2B-b7e9a16-NOGIL/bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-3.12.6.md)[📈](results/bm-20241213-3.14.0a2%2B-b7e9a16-NOGIL/bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-3.12.6.svg) | 1.114x ↓<br>[📄](results/bm-20241213-3.14.0a2%2B-b7e9a16-NOGIL/bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-3.13.0rc2.md)[📈](results/bm-20241213-3.14.0a2%2B-b7e9a16-NOGIL/bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-3.13.0rc2.svg) | 1.160x ↑<br>[📄](results/bm-20241213-3.14.0a2%2B-b7e9a16-NOGIL/bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-base.md)[📈](results/bm-20241213-3.14.0a2%2B-b7e9a16-NOGIL/bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-base.svg)[🧠](results/bm-20241213-3.14.0a2%2B-b7e9a16-NOGIL/bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-base-mem.svg) |
| [2024-12-13](results/bm-20241213-3.14.0a2%2B-b7e9a16) | mpage/gh_115999_integrate | b7e9a16 | 1.087x ↑<br>[📄](results/bm-20241213-3.14.0a2%2B-b7e9a16/bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-3.12.6.md)[📈](results/bm-20241213-3.14.0a2%2B-b7e9a16/bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-3.12.6.svg) | 1.048x ↑<br>[📄](results/bm-20241213-3.14.0a2%2B-b7e9a16/bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-3.13.0rc2.md)[📈](results/bm-20241213-3.14.0a2%2B-b7e9a16/bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-3.13.0rc2.svg) | 1.001x ↑<br>[📄](results/bm-20241213-3.14.0a2%2B-b7e9a16/bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-base.md)[📈](results/bm-20241213-3.14.0a2%2B-b7e9a16/bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-base.svg)[🧠](results/bm-20241213-3.14.0a2%2B-b7e9a16/bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2%2B-b7e9a16-vs-base-mem.svg) |
| [2024-12-13](results/bm-20241213-3.14.0a2%2B-4c484ab-NOGIL) | nascheme/gh_115999_specialize | 4c484ab (NOGIL) | 1.193x ↓<br>[📄](results/bm-20241213-3.14.0a2%2B-4c484ab-NOGIL/bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-4c484ab-vs-3.12.6.md)[📈](results/bm-20241213-3.14.0a2%2B-4c484ab-NOGIL/bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-4c484ab-vs-3.12.6.svg) | 1.219x ↓<br>[📄](results/bm-20241213-3.14.0a2%2B-4c484ab-NOGIL/bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-4c484ab-vs-3.13.0rc2.md)[📈](results/bm-20241213-3.14.0a2%2B-4c484ab-NOGIL/bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-4c484ab-vs-3.13.0rc2.svg) | 1.027x ↑<br>[📄](results/bm-20241213-3.14.0a2%2B-4c484ab-NOGIL/bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-4c484ab-vs-base.md)[📈](results/bm-20241213-3.14.0a2%2B-4c484ab-NOGIL/bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-4c484ab-vs-base.svg)[🧠](results/bm-20241213-3.14.0a2%2B-4c484ab-NOGIL/bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-4c484ab-vs-base-mem.svg) |
| [2024-12-13](results/bm-20241213-3.14.0a2%2B-4c484ab) | nascheme/gh_115999_specialize | 4c484ab | 1.078x ↑<br>[📄](results/bm-20241213-3.14.0a2%2B-4c484ab/bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-4c484ab-vs-3.12.6.md)[📈](results/bm-20241213-3.14.0a2%2B-4c484ab/bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-4c484ab-vs-3.12.6.svg) | 1.040x ↑<br>[📄](results/bm-20241213-3.14.0a2%2B-4c484ab/bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-4c484ab-vs-3.13.0rc2.md)[📈](results/bm-20241213-3.14.0a2%2B-4c484ab/bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-4c484ab-vs-3.13.0rc2.svg) | 1.006x ↓<br>[📄](results/bm-20241213-3.14.0a2%2B-4c484ab/bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-4c484ab-vs-base.md)[📈](results/bm-20241213-3.14.0a2%2B-4c484ab/bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-4c484ab-vs-base.svg)[🧠](results/bm-20241213-3.14.0a2%2B-4c484ab/bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2%2B-4c484ab-vs-base-mem.svg) |
| [2024-12-13](results/bm-20241213-3.14.0a2%2B-2de048c) | python/2de048ce79e621f5ae05 | 2de048c | 1.083x ↑<br>[📄](results/bm-20241213-3.14.0a2%2B-2de048c/bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2%2B-2de048c-vs-3.12.6.md)[📈](results/bm-20241213-3.14.0a2%2B-2de048c/bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2%2B-2de048c-vs-3.12.6.svg) | 1.044x ↑<br>[📄](results/bm-20241213-3.14.0a2%2B-2de048c/bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2%2B-2de048c-vs-3.13.0rc2.md)[📈](results/bm-20241213-3.14.0a2%2B-2de048c/bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2%2B-2de048c-vs-3.13.0rc2.svg) |  |
| [2024-12-13](results/bm-20241213-3.14.0a2%2B-2de048c-NOGIL) | python/2de048ce79e621f5ae05 | 2de048c (NOGIL) | 1.215x ↓<br>[📄](results/bm-20241213-3.14.0a2%2B-2de048c-NOGIL/bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2%2B-2de048c-vs-3.12.6.md)[📈](results/bm-20241213-3.14.0a2%2B-2de048c-NOGIL/bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2%2B-2de048c-vs-3.12.6.svg) | 1.240x ↓<br>[📄](results/bm-20241213-3.14.0a2%2B-2de048c-NOGIL/bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2%2B-2de048c-vs-3.13.0rc2.md)[📈](results/bm-20241213-3.14.0a2%2B-2de048c-NOGIL/bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2%2B-2de048c-vs-3.13.0rc2.svg) | 1.269x ↓<br>[📄](results/bm-20241213-3.14.0a2%2B-2de048c-NOGIL/bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2%2B-2de048c-vs-base.md)[📈](results/bm-20241213-3.14.0a2%2B-2de048c-NOGIL/bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2%2B-2de048c-vs-base.svg)[🧠](results/bm-20241213-3.14.0a2%2B-2de048c-NOGIL/bm-20241213-vultr-x86_64-python-2de048ce79e621f5ae05-3.14.0a2%2B-2de048c-vs-base-mem.svg) |
| [2024-12-08](results/bm-20241208-3.14.0a2%2B-7015485) | python/70154855cf698560dd9a | 7015485 | 1.065x ↑<br>[📄](results/bm-20241208-3.14.0a2%2B-7015485/bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2%2B-7015485-vs-3.12.6.md)[📈](results/bm-20241208-3.14.0a2%2B-7015485/bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2%2B-7015485-vs-3.12.6.svg) | 1.027x ↑<br>[📄](results/bm-20241208-3.14.0a2%2B-7015485/bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2%2B-7015485-vs-3.13.0rc2.md)[📈](results/bm-20241208-3.14.0a2%2B-7015485/bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2%2B-7015485-vs-3.13.0rc2.svg) | 1.003x ↑<br>[📄](results/bm-20241208-3.14.0a2%2B-7015485/bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2%2B-7015485-vs-base.md)[📈](results/bm-20241208-3.14.0a2%2B-7015485/bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2%2B-7015485-vs-base.svg)[🧠](results/bm-20241208-3.14.0a2%2B-7015485/bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2%2B-7015485-vs-base-mem.svg) |
| [2024-12-08](results/bm-20241208-3.14.0a2%2B-7015485-NOGIL) | python/70154855cf698560dd9a | 7015485 (NOGIL) | 1.231x ↓<br>[📄](results/bm-20241208-3.14.0a2%2B-7015485-NOGIL/bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2%2B-7015485-vs-3.12.6.md)[📈](results/bm-20241208-3.14.0a2%2B-7015485-NOGIL/bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2%2B-7015485-vs-3.12.6.svg) | 1.256x ↓<br>[📄](results/bm-20241208-3.14.0a2%2B-7015485-NOGIL/bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2%2B-7015485-vs-3.13.0rc2.md)[📈](results/bm-20241208-3.14.0a2%2B-7015485-NOGIL/bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2%2B-7015485-vs-3.13.0rc2.svg) | 1.004x ↓<br>[📄](results/bm-20241208-3.14.0a2%2B-7015485-NOGIL/bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2%2B-7015485-vs-base.md)[📈](results/bm-20241208-3.14.0a2%2B-7015485-NOGIL/bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2%2B-7015485-vs-base.svg)[🧠](results/bm-20241208-3.14.0a2%2B-7015485-NOGIL/bm-20241208-vultr-x86_64-python-70154855cf698560dd9a-3.14.0a2%2B-7015485-vs-base-mem.svg) |


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
