# Results

- fork: python
- version: 3.14.0a1+
- config: NOGIL
- commit hash: [532fc08](https://github.com/python/cpython/commit/532fc08)
- commit date: 2024-11-04T21:48:09+01:00
- commit merge base: [9b7294c3a560f43f1e26a0f48c258829076d6464](https://github.com/python/cpython/commit/9b7294c3a560f43f1e26a0f48c258829076d6464)
- ref: 532fc08102d62c04d55f

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11675102423)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20241104-linux-x86_64-python-532fc08102d62c04d55f-3.14.0a1%2B-532fc08.json)

### vs. 3.12.6

- Geometric mean: 1.57x slower (HPT: reliability of 100.00%, 1.47x slower at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [📄table](bm-20241104-linux-x86_64-python-532fc08102d62c04d55f-3.14.0a1%2B-532fc08-vs-3.12.6.md)
- [📈time plot](bm-20241104-linux-x86_64-python-532fc08102d62c04d55f-3.14.0a1%2B-532fc08-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.59x slower (HPT: reliability of 100.00%, 1.46x slower at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http
- [📄table](bm-20241104-linux-x86_64-python-532fc08102d62c04d55f-3.14.0a1%2B-532fc08-vs-3.13.0rc2.md)
- [📈time plot](bm-20241104-linux-x86_64-python-532fc08102d62c04d55f-3.14.0a1%2B-532fc08-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.39x slower (HPT: reliability of 100.00%, 1.32x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20241104-linux-x86_64-python-532fc08102d62c04d55f-3.14.0a1%2B-532fc08-vs-base-mem.svg)
- [📄table](bm-20241104-linux-x86_64-python-532fc08102d62c04d55f-3.14.0a1%2B-532fc08-vs-base.md)
- [📈time plot](bm-20241104-linux-x86_64-python-532fc08102d62c04d55f-3.14.0a1%2B-532fc08-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11675102423)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241104-vultr-x86_64-python-532fc08102d62c04d55f-3.14.0a1%2B-532fc08.json)

### vs. 3.12.6

- Geometric mean: 1.56x slower (HPT: reliability of 100.00%, 1.40x slower at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [📄table](bm-20241104-vultr-x86_64-python-532fc08102d62c04d55f-3.14.0a1%2B-532fc08-vs-3.12.6.md)
- [📈time plot](bm-20241104-vultr-x86_64-python-532fc08102d62c04d55f-3.14.0a1%2B-532fc08-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.58x slower (HPT: reliability of 100.00%, 1.41x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http
- [📄table](bm-20241104-vultr-x86_64-python-532fc08102d62c04d55f-3.14.0a1%2B-532fc08-vs-3.13.0rc2.md)
- [📈time plot](bm-20241104-vultr-x86_64-python-532fc08102d62c04d55f-3.14.0a1%2B-532fc08-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.55x slower (HPT: reliability of 100.00%, 1.40x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20241104-vultr-x86_64-python-532fc08102d62c04d55f-3.14.0a1%2B-532fc08-vs-base-mem.svg)
- [📄table](bm-20241104-vultr-x86_64-python-532fc08102d62c04d55f-3.14.0a1%2B-532fc08-vs-base.md)
- [📈time plot](bm-20241104-vultr-x86_64-python-532fc08102d62c04d55f-3.14.0a1%2B-532fc08-vs-base.svg)

