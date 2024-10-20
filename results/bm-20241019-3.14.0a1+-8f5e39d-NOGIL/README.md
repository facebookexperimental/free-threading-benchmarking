# Results

- fork: python
- version: 3.14.0a1+
- config: NOGIL
- commit hash: [8f5e39d](https://github.com/python/cpython/commit/8f5e39d)
- commit date: 2024-10-19T17:46:57-04:00
- commit merge base: [4c53b2577531c77193430cdcd66ad6385fcda81f](https://github.com/python/cpython/commit/4c53b2577531c77193430cdcd66ad6385fcda81f)
- ref: 8f5e39d5c885318e3128

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11421789318)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241019-vultr-x86_64-python-8f5e39d5c885318e3128-3.14.0a1%2B-8f5e39d.json)

### vs. 3.12.6

- Geometric mean: 1.55x slower (HPT: reliability of 100.00%, 1.40x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20241019-vultr-x86_64-python-8f5e39d5c885318e3128-3.14.0a1%2B-8f5e39d-vs-3.12.6.md)
- [📈time plot](bm-20241019-vultr-x86_64-python-8f5e39d5c885318e3128-3.14.0a1%2B-8f5e39d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.57x slower (HPT: reliability of 100.00%, 1.41x slower at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20241019-vultr-x86_64-python-8f5e39d5c885318e3128-3.14.0a1%2B-8f5e39d-vs-3.13.0rc2.md)
- [📈time plot](bm-20241019-vultr-x86_64-python-8f5e39d5c885318e3128-3.14.0a1%2B-8f5e39d-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.54x slower (HPT: reliability of 100.00%, 1.43x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20241019-vultr-x86_64-python-8f5e39d5c885318e3128-3.14.0a1%2B-8f5e39d-vs-base-mem.svg)
- [📄table](bm-20241019-vultr-x86_64-python-8f5e39d5c885318e3128-3.14.0a1%2B-8f5e39d-vs-base.md)
- [📈time plot](bm-20241019-vultr-x86_64-python-8f5e39d5c885318e3128-3.14.0a1%2B-8f5e39d-vs-base.svg)

