# Results

- fork: python
- version: 3.14.0a1+
- config: 
- commit hash: [a0f5c8e](https://github.com/python/cpython/commit/a0f5c8e)
- commit date: 2024-10-17T19:08:34-07:00
- commit merge base: [77cebb1ce9baac9e01a45d34113c3bea74940d90](https://github.com/python/cpython/commit/77cebb1ce9baac9e01a45d34113c3bea74940d90)
- ref: main

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11398258763)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [pystats raw](bm-20241017-vultr-x86_64-python-main-3.14.0a1%2B-a0f5c8e-pystats.json)
- [raw results](bm-20241017-vultr-x86_64-python-main-3.14.0a1%2B-a0f5c8e.json)

### vs. 3.12.6

- Geometric mean: 1.00x faster (HPT: reliability of 99.60%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20241017-vultr-x86_64-python-main-3.14.0a1%2B-a0f5c8e-vs-3.12.6.md)
- [📈time plot](bm-20241017-vultr-x86_64-python-main-3.14.0a1%2B-a0f5c8e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.01x slower (HPT: reliability of 52.04%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20241017-vultr-x86_64-python-main-3.14.0a1%2B-a0f5c8e-vs-3.13.0rc2.md)
- [📈time plot](bm-20241017-vultr-x86_64-python-main-3.14.0a1%2B-a0f5c8e-vs-3.13.0rc2.svg)

