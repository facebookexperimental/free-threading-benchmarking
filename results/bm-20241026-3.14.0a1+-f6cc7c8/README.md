# Results

- fork: python
- version: 3.14.0a1+
- config: 
- commit hash: [f6cc7c8](https://github.com/python/cpython/commit/f6cc7c8)
- commit date: 2024-10-26T23:40:31+02:00
- commit merge base: [26d627779f79d8d5650fe7be348432eccc28f8f9](https://github.com/python/cpython/commit/26d627779f79d8d5650fe7be348432eccc28f8f9)
- ref: f6cc7c8bd01d8468af70

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11535982459)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [pystats raw](bm-20241026-vultr-x86_64-python-f6cc7c8bd01d8468af70-3.14.0a1%2B-f6cc7c8-pystats.json)
- [pystats table](bm-20241026-vultr-x86_64-python-f6cc7c8bd01d8468af70-3.14.0a1%2B-f6cc7c8-pystats.md)
- [raw results](bm-20241026-vultr-x86_64-python-f6cc7c8bd01d8468af70-3.14.0a1%2B-f6cc7c8.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 99.56%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20241026-vultr-x86_64-python-f6cc7c8bd01d8468af70-3.14.0a1%2B-f6cc7c8-vs-3.12.6.md)
- [📈time plot](bm-20241026-vultr-x86_64-python-f6cc7c8bd01d8468af70-3.14.0a1%2B-f6cc7c8-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 73.50%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20241026-vultr-x86_64-python-f6cc7c8bd01d8468af70-3.14.0a1%2B-f6cc7c8-vs-3.13.0rc2.md)
- [📈time plot](bm-20241026-vultr-x86_64-python-f6cc7c8bd01d8468af70-3.14.0a1%2B-f6cc7c8-vs-3.13.0rc2.svg)

