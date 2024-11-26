# Results

- fork: python
- version: 3.14.0a1+
- config: 
- commit hash: [4ae5061](https://github.com/python/cpython/commit/4ae5061)
- commit date: 2024-11-13T15:45:08-08:00
- commit merge base: [fd4b5453df74e249987553b12c14ad75fafa4991](https://github.com/python/cpython/commit/fd4b5453df74e249987553b12c14ad75fafa4991)
- ref: 4ae50615d2beef0f93d9

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11828233702)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20241113-linux-x86_64-python-4ae50615d2beef0f93d9-3.14.0a1%2B-4ae5061.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 87.88%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [📄table](bm-20241113-linux-x86_64-python-4ae50615d2beef0f93d9-3.14.0a1%2B-4ae5061-vs-3.12.6.md)
- [📈time plot](bm-20241113-linux-x86_64-python-4ae50615d2beef0f93d9-3.14.0a1%2B-4ae5061-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 71.99%, 1.00x slower at 99th %ile)
- Memory usage: 1.01x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http
- [📄table](bm-20241113-linux-x86_64-python-4ae50615d2beef0f93d9-3.14.0a1%2B-4ae5061-vs-3.13.0rc2.md)
- [📈time plot](bm-20241113-linux-x86_64-python-4ae50615d2beef0f93d9-3.14.0a1%2B-4ae5061-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11828233702)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241113-vultr-x86_64-python-4ae50615d2beef0f93d9-3.14.0a1%2B-4ae5061.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 98.55%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [📄table](bm-20241113-vultr-x86_64-python-4ae50615d2beef0f93d9-3.14.0a1%2B-4ae5061-vs-3.12.6.md)
- [📈time plot](bm-20241113-vultr-x86_64-python-4ae50615d2beef0f93d9-3.14.0a1%2B-4ae5061-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 92.62%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http
- [📄table](bm-20241113-vultr-x86_64-python-4ae50615d2beef0f93d9-3.14.0a1%2B-4ae5061-vs-3.13.0rc2.md)
- [📈time plot](bm-20241113-vultr-x86_64-python-4ae50615d2beef0f93d9-3.14.0a1%2B-4ae5061-vs-3.13.0rc2.svg)

