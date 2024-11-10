# Results

- fork: python
- version: 3.14.0a1+
- config: NOGIL
- commit hash: [9d08423](https://github.com/python/cpython/commit/9d08423)
- commit date: 2024-11-09T23:01:32+00:00
- commit merge base: [266328552e922fd9030cd699e10a25f03a67c8ba](https://github.com/python/cpython/commit/266328552e922fd9030cd699e10a25f03a67c8ba)
- ref: 9d08423b6e0fa89ce9cf

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11760507472)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20241109-linux-x86_64-python-9d08423b6e0fa89ce9cf-3.14.0a1%2B-9d08423.json)

### vs. 3.12.6

- Geometric mean: 1.44x slower (HPT: reliability of 100.00%, 1.34x slower at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [📄table](bm-20241109-linux-x86_64-python-9d08423b6e0fa89ce9cf-3.14.0a1%2B-9d08423-vs-3.12.6.md)
- [📈time plot](bm-20241109-linux-x86_64-python-9d08423b6e0fa89ce9cf-3.14.0a1%2B-9d08423-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.47x slower (HPT: reliability of 100.00%, 1.36x slower at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http
- [📄table](bm-20241109-linux-x86_64-python-9d08423b6e0fa89ce9cf-3.14.0a1%2B-9d08423-vs-3.13.0rc2.md)
- [📈time plot](bm-20241109-linux-x86_64-python-9d08423b6e0fa89ce9cf-3.14.0a1%2B-9d08423-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.46x slower (HPT: reliability of 100.00%, 1.36x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20241109-linux-x86_64-python-9d08423b6e0fa89ce9cf-3.14.0a1%2B-9d08423-vs-base-mem.svg)
- [📄table](bm-20241109-linux-x86_64-python-9d08423b6e0fa89ce9cf-3.14.0a1%2B-9d08423-vs-base.md)
- [📈time plot](bm-20241109-linux-x86_64-python-9d08423b6e0fa89ce9cf-3.14.0a1%2B-9d08423-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11760507472)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241109-vultr-x86_64-python-9d08423b6e0fa89ce9cf-3.14.0a1%2B-9d08423.json)

### vs. 3.12.6

- Geometric mean: 1.56x slower (HPT: reliability of 100.00%, 1.39x slower at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [📄table](bm-20241109-vultr-x86_64-python-9d08423b6e0fa89ce9cf-3.14.0a1%2B-9d08423-vs-3.12.6.md)
- [📈time plot](bm-20241109-vultr-x86_64-python-9d08423b6e0fa89ce9cf-3.14.0a1%2B-9d08423-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.58x slower (HPT: reliability of 100.00%, 1.41x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http
- [📄table](bm-20241109-vultr-x86_64-python-9d08423b6e0fa89ce9cf-3.14.0a1%2B-9d08423-vs-3.13.0rc2.md)
- [📈time plot](bm-20241109-vultr-x86_64-python-9d08423b6e0fa89ce9cf-3.14.0a1%2B-9d08423-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.54x slower (HPT: reliability of 100.00%, 1.41x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20241109-vultr-x86_64-python-9d08423b6e0fa89ce9cf-3.14.0a1%2B-9d08423-vs-base-mem.svg)
- [📄table](bm-20241109-vultr-x86_64-python-9d08423b6e0fa89ce9cf-3.14.0a1%2B-9d08423-vs-base.md)
- [📈time plot](bm-20241109-vultr-x86_64-python-9d08423b6e0fa89ce9cf-3.14.0a1%2B-9d08423-vs-base.svg)

