# Results

- fork: python/83ba8c2bba834c0b92de
- version: 3.14.0a1+
- config: NOGIL
- commit hash: [83ba8c2](https://github.com/python/cpython/commit/83ba8c2)
- commit date: 2024-11-05T15:53:54-08:00
- commit merge base: [fc233f46d3761b4e808be2c44fda0b843179004e](https://github.com/python/cpython/commit/fc233f46d3761b4e808be2c44fda0b843179004e)
- ref: 83ba8c2bba834c0b92de

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11694803058)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241105-vultr-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1%2B-83ba8c2.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.38x slower at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [📄table](bm-20241105-vultr-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1%2B-83ba8c2-vs-3.12.6.md)
- [📈time plot](bm-20241105-vultr-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1%2B-83ba8c2-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.40x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http
- [📄table](bm-20241105-vultr-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1%2B-83ba8c2-vs-3.13.0rc2.md)
- [📈time plot](bm-20241105-vultr-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1%2B-83ba8c2-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.41x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20241105-vultr-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1%2B-83ba8c2-vs-base-mem.svg)
- [📄table](bm-20241105-vultr-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1%2B-83ba8c2-vs-base.md)
- [📈time plot](bm-20241105-vultr-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1%2B-83ba8c2-vs-base.svg)

