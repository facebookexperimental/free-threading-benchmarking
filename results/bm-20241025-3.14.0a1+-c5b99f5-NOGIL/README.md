# Results

- fork: python
- version: 3.14.0a1+
- config: NOGIL
- commit hash: [c5b99f5](https://github.com/python/cpython/commit/c5b99f5)
- commit date: 2024-10-25T23:45:09+05:30
- commit merge base: [13844094609cf8265a2eed023e33c7002f3f530d](https://github.com/python/cpython/commit/13844094609cf8265a2eed023e33c7002f3f530d)
- ref: c5b99f5c2c5347d66b9d

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11527223207)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241025-vultr-x86_64-python-c5b99f5c2c5347d66b9d-3.14.0a1%2B-c5b99f5.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.40x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20241025-vultr-x86_64-python-c5b99f5c2c5347d66b9d-3.14.0a1%2B-c5b99f5-vs-3.12.6.md)
- [📈time plot](bm-20241025-vultr-x86_64-python-c5b99f5c2c5347d66b9d-3.14.0a1%2B-c5b99f5-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.42x slower at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20241025-vultr-x86_64-python-c5b99f5c2c5347d66b9d-3.14.0a1%2B-c5b99f5-vs-3.13.0rc2.md)
- [📈time plot](bm-20241025-vultr-x86_64-python-c5b99f5c2c5347d66b9d-3.14.0a1%2B-c5b99f5-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.43x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20241025-vultr-x86_64-python-c5b99f5c2c5347d66b9d-3.14.0a1%2B-c5b99f5-vs-base-mem.svg)
- [📄table](bm-20241025-vultr-x86_64-python-c5b99f5c2c5347d66b9d-3.14.0a1%2B-c5b99f5-vs-base.md)
- [📈time plot](bm-20241025-vultr-x86_64-python-c5b99f5c2c5347d66b9d-3.14.0a1%2B-c5b99f5-vs-base.svg)

