# Results

- fork: python
- version: 3.14.0a1+
- config: 
- commit hash: [d6b3e78](https://github.com/python/cpython/commit/d6b3e78)
- commit date: 2024-11-19T00:11:12+00:00
- commit merge base: [0063f5f314350ad5122a86f31df65f5dff4f4e5c](https://github.com/python/cpython/commit/0063f5f314350ad5122a86f31df65f5dff4f4e5c)
- ref: d6b3e78504b3168c432b

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11903695636)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20241119-linux-x86_64-python-d6b3e78504b3168c432b-3.14.0a1%2B-d6b3e78.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 99.96%, 1.00x faster at 99th %ile)
- Memory usage: 1.01x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [📄table](bm-20241119-linux-x86_64-python-d6b3e78504b3168c432b-3.14.0a1%2B-d6b3e78-vs-3.12.6.md)
- [📈time plot](bm-20241119-linux-x86_64-python-d6b3e78504b3168c432b-3.14.0a1%2B-d6b3e78-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 69.41%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http
- [📄table](bm-20241119-linux-x86_64-python-d6b3e78504b3168c432b-3.14.0a1%2B-d6b3e78-vs-3.13.0rc2.md)
- [📈time plot](bm-20241119-linux-x86_64-python-d6b3e78504b3168c432b-3.14.0a1%2B-d6b3e78-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11903695636)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241119-vultr-x86_64-python-d6b3e78504b3168c432b-3.14.0a1%2B-d6b3e78.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 96.70%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [📄table](bm-20241119-vultr-x86_64-python-d6b3e78504b3168c432b-3.14.0a1%2B-d6b3e78-vs-3.12.6.md)
- [📈time plot](bm-20241119-vultr-x86_64-python-d6b3e78504b3168c432b-3.14.0a1%2B-d6b3e78-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 90.50%, 1.00x slower at 99th %ile)
- Memory usage: 0.99x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http
- [📄table](bm-20241119-vultr-x86_64-python-d6b3e78504b3168c432b-3.14.0a1%2B-d6b3e78-vs-3.13.0rc2.md)
- [📈time plot](bm-20241119-vultr-x86_64-python-d6b3e78504b3168c432b-3.14.0a1%2B-d6b3e78-vs-3.13.0rc2.svg)

