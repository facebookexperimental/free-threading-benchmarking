# Results

- fork: python
- version: 3.14.0a1+
- config: 
- commit hash: [9d6366b](https://github.com/python/cpython/commit/9d6366b)
- commit date: 2024-11-17T01:56:01+00:00
- commit merge base: [acbd5c9c6c62dac34d2ed1a789d36fe61841c16d](https://github.com/python/cpython/commit/acbd5c9c6c62dac34d2ed1a789d36fe61841c16d)
- ref: 9d6366b60d01305fc5e4

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11917864398)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1%2B-9d6366b.json)

### vs. 3.12.6

- Geometric mean: 1.024x faster (HPT: reliability of 99.76%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [📄table](bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1%2B-9d6366b-vs-3.12.6.md)
- [📈time plot](bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1%2B-9d6366b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.007x faster (HPT: reliability of 61.46%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http
- [📄table](bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1%2B-9d6366b-vs-3.13.0rc2.md)
- [📈time plot](bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1%2B-9d6366b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.003x faster (HPT: reliability of 85.57%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1%2B-9d6366b-vs-base-mem.svg)
- [📄table](bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1%2B-9d6366b-vs-base.md)
- [📈time plot](bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1%2B-9d6366b-vs-base.svg)

