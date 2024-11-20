# Results

- fork: python
- version: 3.14.0a2+
- config: NOGIL
- commit hash: [c9b399f](https://github.com/python/cpython/commit/c9b399f)
- commit date: 2024-11-19T21:19:30+00:00
- commit merge base: [2cdfb41d0c3bfea37983fc872951bc3b2a4d90b8](https://github.com/python/cpython/commit/2cdfb41d0c3bfea37983fc872951bc3b2a4d90b8)
- ref: c9b399fbdb01584dcfff

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11924250585)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2%2B-c9b399f.json)

### vs. 3.12.6

- Geometric mean: 1.41x slower (HPT: reliability of 100.00%, 1.31x slower at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [📄table](bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2%2B-c9b399f-vs-3.12.6.md)
- [📈time plot](bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2%2B-c9b399f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.43x slower (HPT: reliability of 100.00%, 1.35x slower at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http
- [📄table](bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2%2B-c9b399f-vs-3.13.0rc2.md)
- [📈time plot](bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2%2B-c9b399f-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.43x slower (HPT: reliability of 100.00%, 1.35x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2%2B-c9b399f-vs-base-mem.svg)
- [📄table](bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2%2B-c9b399f-vs-base.md)
- [📈time plot](bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2%2B-c9b399f-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11924250585)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241119-vultr-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2%2B-c9b399f.json)

### vs. 3.12.6

- Geometric mean: 1.54x slower (HPT: reliability of 100.00%, 1.38x slower at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [📄table](bm-20241119-vultr-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2%2B-c9b399f-vs-3.12.6.md)
- [📈time plot](bm-20241119-vultr-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2%2B-c9b399f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.56x slower (HPT: reliability of 100.00%, 1.40x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http
- [📄table](bm-20241119-vultr-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2%2B-c9b399f-vs-3.13.0rc2.md)
- [📈time plot](bm-20241119-vultr-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2%2B-c9b399f-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.53x slower (HPT: reliability of 100.00%, 1.40x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20241119-vultr-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2%2B-c9b399f-vs-base-mem.svg)
- [📄table](bm-20241119-vultr-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2%2B-c9b399f-vs-base.md)
- [📈time plot](bm-20241119-vultr-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2%2B-c9b399f-vs-base.svg)

