# Results

- fork: python/494360afd00dc8f6b549
- version: 3.14.0a1+
- config: NOGIL
- commit hash: [494360a](https://github.com/python/cpython/commit/494360a)
- commit date: 2024-11-12T10:11:40+10:00
- commit merge base: [a6d48e8f8323758771f5e130f67c9bdf7b4f25c5](https://github.com/python/cpython/commit/a6d48e8f8323758771f5e130f67c9bdf7b4f25c5)
- ref: 494360afd00dc8f6b549

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11788331803)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20241112-linux-x86_64-python-494360afd00dc8f6b549-3.14.0a1%2B-494360a.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.35x slower at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [📄table](bm-20241112-linux-x86_64-python-494360afd00dc8f6b549-3.14.0a1%2B-494360a-vs-3.12.6.md)
- [📈time plot](bm-20241112-linux-x86_64-python-494360afd00dc8f6b549-3.14.0a1%2B-494360a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.37x slower at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http
- [📄table](bm-20241112-linux-x86_64-python-494360afd00dc8f6b549-3.14.0a1%2B-494360a-vs-3.13.0rc2.md)
- [📈time plot](bm-20241112-linux-x86_64-python-494360afd00dc8f6b549-3.14.0a1%2B-494360a-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.36x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20241112-linux-x86_64-python-494360afd00dc8f6b549-3.14.0a1%2B-494360a-vs-base-mem.svg)
- [📄table](bm-20241112-linux-x86_64-python-494360afd00dc8f6b549-3.14.0a1%2B-494360a-vs-base.md)
- [📈time plot](bm-20241112-linux-x86_64-python-494360afd00dc8f6b549-3.14.0a1%2B-494360a-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11788331803)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241112-vultr-x86_64-python-494360afd00dc8f6b549-3.14.0a1%2B-494360a.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.39x slower at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [📄table](bm-20241112-vultr-x86_64-python-494360afd00dc8f6b549-3.14.0a1%2B-494360a-vs-3.12.6.md)
- [📈time plot](bm-20241112-vultr-x86_64-python-494360afd00dc8f6b549-3.14.0a1%2B-494360a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.40x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http
- [📄table](bm-20241112-vultr-x86_64-python-494360afd00dc8f6b549-3.14.0a1%2B-494360a-vs-3.13.0rc2.md)
- [📈time plot](bm-20241112-vultr-x86_64-python-494360afd00dc8f6b549-3.14.0a1%2B-494360a-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.41x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20241112-vultr-x86_64-python-494360afd00dc8f6b549-3.14.0a1%2B-494360a-vs-base-mem.svg)
- [📄table](bm-20241112-vultr-x86_64-python-494360afd00dc8f6b549-3.14.0a1%2B-494360a-vs-base.md)
- [📈time plot](bm-20241112-vultr-x86_64-python-494360afd00dc8f6b549-3.14.0a1%2B-494360a-vs-base.svg)

