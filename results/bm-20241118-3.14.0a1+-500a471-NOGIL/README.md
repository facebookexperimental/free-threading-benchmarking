# Results

- fork: python
- version: 3.14.0a1+
- config: NOGIL
- commit hash: [500a471](https://github.com/python/cpython/commit/500a471)
- commit date: 2024-11-18T07:43:41+08:00
- commit merge base: [0c5c80928c476ac0dcb9a053b15a562af899cfba](https://github.com/python/cpython/commit/0c5c80928c476ac0dcb9a053b15a562af899cfba)
- ref: 500a4712bb42355eeb78

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11883524195)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20241118-linux-x86_64-python-500a4712bb42355eeb78-3.14.0a1%2B-500a471.json)

### vs. 3.12.6

- Geometric mean: 1.302x slower (HPT: reliability of 100.00%, 1.32x slower at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [📄table](bm-20241118-linux-x86_64-python-500a4712bb42355eeb78-3.14.0a1%2B-500a471-vs-3.12.6.md)
- [📈time plot](bm-20241118-linux-x86_64-python-500a4712bb42355eeb78-3.14.0a1%2B-500a471-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.310x slower (HPT: reliability of 100.00%, 1.35x slower at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http
- [📄table](bm-20241118-linux-x86_64-python-500a4712bb42355eeb78-3.14.0a1%2B-500a471-vs-3.13.0rc2.md)
- [📈time plot](bm-20241118-linux-x86_64-python-500a4712bb42355eeb78-3.14.0a1%2B-500a471-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.328x slower (HPT: reliability of 100.00%, 1.39x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20241118-linux-x86_64-python-500a4712bb42355eeb78-3.14.0a1%2B-500a471-vs-base-mem.svg)
- [📄table](bm-20241118-linux-x86_64-python-500a4712bb42355eeb78-3.14.0a1%2B-500a471-vs-base.md)
- [📈time plot](bm-20241118-linux-x86_64-python-500a4712bb42355eeb78-3.14.0a1%2B-500a471-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11883524195)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241118-vultr-x86_64-python-500a4712bb42355eeb78-3.14.0a1%2B-500a471.json)

### vs. 3.12.6

- Geometric mean: 1.350x slower (HPT: reliability of 100.00%, 1.39x slower at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [📄table](bm-20241118-vultr-x86_64-python-500a4712bb42355eeb78-3.14.0a1%2B-500a471-vs-3.12.6.md)
- [📈time plot](bm-20241118-vultr-x86_64-python-500a4712bb42355eeb78-3.14.0a1%2B-500a471-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.360x slower (HPT: reliability of 100.00%, 1.40x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http
- [📄table](bm-20241118-vultr-x86_64-python-500a4712bb42355eeb78-3.14.0a1%2B-500a471-vs-3.13.0rc2.md)
- [📈time plot](bm-20241118-vultr-x86_64-python-500a4712bb42355eeb78-3.14.0a1%2B-500a471-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.359x slower (HPT: reliability of 100.00%, 1.39x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20241118-vultr-x86_64-python-500a4712bb42355eeb78-3.14.0a1%2B-500a471-vs-base-mem.svg)
- [📄table](bm-20241118-vultr-x86_64-python-500a4712bb42355eeb78-3.14.0a1%2B-500a471-vs-base.md)
- [📈time plot](bm-20241118-vultr-x86_64-python-500a4712bb42355eeb78-3.14.0a1%2B-500a471-vs-base.svg)

