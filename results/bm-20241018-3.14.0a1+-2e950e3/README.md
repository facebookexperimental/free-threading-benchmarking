# Results

- fork: python
- version: 3.14.0a1+
- config: 
- commit hash: [2e950e3](https://github.com/python/cpython/commit/2e950e3)
- commit date: 2024-10-18T16:51:29+03:00
- commit merge base: [cda0ec8e7c4e9a010e5f73c5afaf18f86cb27b97](https://github.com/python/cpython/commit/cda0ec8e7c4e9a010e5f73c5afaf18f86cb27b97)
- ref: main

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11405745068)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241018-vultr-x86_64-python-main-3.14.0a1%2B-2e950e3.json)

### vs. 3.12.6

- Geometric mean: 1.01x faster (HPT: reliability of 99.97%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20241018-vultr-x86_64-python-main-3.14.0a1%2B-2e950e3-vs-3.12.6.md)
- [📈time plot](bm-20241018-vultr-x86_64-python-main-3.14.0a1%2B-2e950e3-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.01x slower (HPT: reliability of 93.31%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20241018-vultr-x86_64-python-main-3.14.0a1%2B-2e950e3-vs-3.13.0rc2.md)
- [📈time plot](bm-20241018-vultr-x86_64-python-main-3.14.0a1%2B-2e950e3-vs-3.13.0rc2.svg)

