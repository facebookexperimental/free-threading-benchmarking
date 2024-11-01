# Results

- fork: python
- version: 3.14.0a1+
- config: NOGIL
- commit hash: [d0abd0b](https://github.com/python/cpython/commit/d0abd0b)
- commit date: 2024-10-31T21:44:34+00:00
- commit merge base: [dd3c0fa3fd2795326dae0e0ed63c668f5506cf32](https://github.com/python/cpython/commit/dd3c0fa3fd2795326dae0e0ed63c668f5506cf32)
- ref: d0abd0b826cfa574d151

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11621986646)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241031-vultr-x86_64-python-d0abd0b826cfa574d151-3.14.0a1%2B-d0abd0b.json)

### vs. 3.12.6

- Geometric mean: 1.54x slower (HPT: reliability of 100.00%, 1.39x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20241031-vultr-x86_64-python-d0abd0b826cfa574d151-3.14.0a1%2B-d0abd0b-vs-3.12.6.md)
- [📈time plot](bm-20241031-vultr-x86_64-python-d0abd0b826cfa574d151-3.14.0a1%2B-d0abd0b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.56x slower (HPT: reliability of 100.00%, 1.41x slower at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20241031-vultr-x86_64-python-d0abd0b826cfa574d151-3.14.0a1%2B-d0abd0b-vs-3.13.0rc2.md)
- [📈time plot](bm-20241031-vultr-x86_64-python-d0abd0b826cfa574d151-3.14.0a1%2B-d0abd0b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.54x slower (HPT: reliability of 100.00%, 1.41x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20241031-vultr-x86_64-python-d0abd0b826cfa574d151-3.14.0a1%2B-d0abd0b-vs-base-mem.svg)
- [📄table](bm-20241031-vultr-x86_64-python-d0abd0b826cfa574d151-3.14.0a1%2B-d0abd0b-vs-base.md)
- [📈time plot](bm-20241031-vultr-x86_64-python-d0abd0b826cfa574d151-3.14.0a1%2B-d0abd0b-vs-base.svg)

