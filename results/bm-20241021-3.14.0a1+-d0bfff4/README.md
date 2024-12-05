# Results

- fork: python/d0bfff47fb2aea9272b5
- version: 3.14.0a1+
- config: 
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

- Geometric mean: not sig (HPT: reliability of 80.43%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1%2B-d0bfff4-vs-3.12.6.md)
- [📈time plot](bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1%2B-d0bfff4-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 98.61%, 1.00x slower at 99th %ile)
- Memory usage: 1.01x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1%2B-d0bfff4-vs-3.13.0rc2.md)
- [📈time plot](bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1%2B-d0bfff4-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11450862793)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241021-vultr-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1%2B-d0bfff4.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 80.88%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20241021-vultr-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1%2B-d0bfff4-vs-3.12.6.md)
- [📈time plot](bm-20241021-vultr-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1%2B-d0bfff4-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 99.07%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20241021-vultr-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1%2B-d0bfff4-vs-3.13.0rc2.md)
- [📈time plot](bm-20241021-vultr-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1%2B-d0bfff4-vs-3.13.0rc2.svg)

