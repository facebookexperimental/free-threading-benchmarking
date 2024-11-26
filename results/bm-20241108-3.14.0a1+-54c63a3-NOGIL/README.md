# Results

- fork: python
- version: 3.14.0a1+
- config: NOGIL
- commit hash: [54c63a3](https://github.com/python/cpython/commit/54c63a3)
- commit date: 2024-11-08T16:47:51+00:00
- commit merge base: [fa4092259763ffad45a5bb9ef55f515dc6a69ad2](https://github.com/python/cpython/commit/fa4092259763ffad45a5bb9ef55f515dc6a69ad2)
- ref: 54c63a32d06cb5f07a66

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11749358113)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20241108-linux-x86_64-python-54c63a32d06cb5f07a66-3.14.0a1%2B-54c63a3.json)

### vs. 3.12.6

- Geometric mean: 1.318x slower (HPT: reliability of 100.00%, 1.34x slower at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [📄table](bm-20241108-linux-x86_64-python-54c63a32d06cb5f07a66-3.14.0a1%2B-54c63a3-vs-3.12.6.md)
- [📈time plot](bm-20241108-linux-x86_64-python-54c63a32d06cb5f07a66-3.14.0a1%2B-54c63a3-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.325x slower (HPT: reliability of 100.00%, 1.38x slower at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http
- [📄table](bm-20241108-linux-x86_64-python-54c63a32d06cb5f07a66-3.14.0a1%2B-54c63a3-vs-3.13.0rc2.md)
- [📈time plot](bm-20241108-linux-x86_64-python-54c63a32d06cb5f07a66-3.14.0a1%2B-54c63a3-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.336x slower (HPT: reliability of 100.00%, 1.37x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20241108-linux-x86_64-python-54c63a32d06cb5f07a66-3.14.0a1%2B-54c63a3-vs-base-mem.svg)
- [📄table](bm-20241108-linux-x86_64-python-54c63a32d06cb5f07a66-3.14.0a1%2B-54c63a3-vs-base.md)
- [📈time plot](bm-20241108-linux-x86_64-python-54c63a32d06cb5f07a66-3.14.0a1%2B-54c63a3-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11751529623)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241108-vultr-x86_64-python-54c63a32d06cb5f07a66-3.14.0a1%2B-54c63a3.json)

### vs. 3.12.6

- Geometric mean: 1.352x slower (HPT: reliability of 100.00%, 1.39x slower at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [📄table](bm-20241108-vultr-x86_64-python-54c63a32d06cb5f07a66-3.14.0a1%2B-54c63a3-vs-3.12.6.md)
- [📈time plot](bm-20241108-vultr-x86_64-python-54c63a32d06cb5f07a66-3.14.0a1%2B-54c63a3-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.362x slower (HPT: reliability of 100.00%, 1.40x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http
- [📄table](bm-20241108-vultr-x86_64-python-54c63a32d06cb5f07a66-3.14.0a1%2B-54c63a3-vs-3.13.0rc2.md)
- [📈time plot](bm-20241108-vultr-x86_64-python-54c63a32d06cb5f07a66-3.14.0a1%2B-54c63a3-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.365x slower (HPT: reliability of 100.00%, 1.41x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20241108-vultr-x86_64-python-54c63a32d06cb5f07a66-3.14.0a1%2B-54c63a3-vs-base-mem.svg)
- [📄table](bm-20241108-vultr-x86_64-python-54c63a32d06cb5f07a66-3.14.0a1%2B-54c63a3-vs-base.md)
- [📈time plot](bm-20241108-vultr-x86_64-python-54c63a32d06cb5f07a66-3.14.0a1%2B-54c63a3-vs-base.svg)

