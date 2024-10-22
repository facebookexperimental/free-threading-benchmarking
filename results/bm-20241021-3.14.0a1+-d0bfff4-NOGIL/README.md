# Results

- fork: python
- version: 3.14.0a1+
- config: NOGIL
- commit hash: [d0bfff4](https://github.com/python/cpython/commit/d0bfff4)
- commit date: 2024-10-21T23:37:31+01:00
- commit merge base: [4848b0b92ce2737cea08fa3b322fd0f0a671bb07](https://github.com/python/cpython/commit/4848b0b92ce2737cea08fa3b322fd0f0a671bb07)
- ref: d0bfff47fb2aea9272b5

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11450862793)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1070-aws-x86_64-with-glibc2.31
- [raw results](bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1%2B-d0bfff4.json)

### vs. 3.12.6

- Geometric mean: 1.51x slower (HPT: reliability of 100.00%, 1.41x slower at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1%2B-d0bfff4-vs-3.12.6.md)
- [📈time plot](bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1%2B-d0bfff4-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.53x slower (HPT: reliability of 100.00%, 1.44x slower at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1%2B-d0bfff4-vs-3.13.0rc2.md)
- [📈time plot](bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1%2B-d0bfff4-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.51x slower (HPT: reliability of 100.00%, 1.44x slower at 99th %ile)
- Memory usage: 1.15x
- [🧠memory plot](bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1%2B-d0bfff4-vs-base-mem.svg)
- [📄table](bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1%2B-d0bfff4-vs-base.md)
- [📈time plot](bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1%2B-d0bfff4-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11450862793)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241021-vultr-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1%2B-d0bfff4.json)

### vs. 3.12.6

- Geometric mean: 1.55x slower (HPT: reliability of 100.00%, 1.39x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20241021-vultr-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1%2B-d0bfff4-vs-3.12.6.md)
- [📈time plot](bm-20241021-vultr-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1%2B-d0bfff4-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.57x slower (HPT: reliability of 100.00%, 1.41x slower at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20241021-vultr-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1%2B-d0bfff4-vs-3.13.0rc2.md)
- [📈time plot](bm-20241021-vultr-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1%2B-d0bfff4-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.54x slower (HPT: reliability of 100.00%, 1.42x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20241021-vultr-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1%2B-d0bfff4-vs-base-mem.svg)
- [📄table](bm-20241021-vultr-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1%2B-d0bfff4-vs-base.md)
- [📈time plot](bm-20241021-vultr-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1%2B-d0bfff4-vs-base.svg)

