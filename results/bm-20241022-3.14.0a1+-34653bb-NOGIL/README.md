# Results

- fork: python
- version: 3.14.0a1+
- config: NOGIL
- commit hash: [34653bb](https://github.com/python/cpython/commit/34653bb)
- commit date: 2024-10-22T13:42:22-07:00
- commit merge base: [aaed91cabcedc16c089c4b1c9abb1114659a83d3](https://github.com/python/cpython/commit/aaed91cabcedc16c089c4b1c9abb1114659a83d3)
- ref: 34653bba644aa5481613

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11470674451)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1070-aws-x86_64-with-glibc2.31
- [raw results](bm-20241022-linux-x86_64-python-34653bba644aa5481613-3.14.0a1%2B-34653bb.json)

### vs. 3.12.6

- Geometric mean: 1.48x slower (HPT: reliability of 100.00%, 1.35x slower at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20241022-linux-x86_64-python-34653bba644aa5481613-3.14.0a1%2B-34653bb-vs-3.12.6.md)
- [📈time plot](bm-20241022-linux-x86_64-python-34653bba644aa5481613-3.14.0a1%2B-34653bb-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.50x slower (HPT: reliability of 100.00%, 1.39x slower at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20241022-linux-x86_64-python-34653bba644aa5481613-3.14.0a1%2B-34653bb-vs-3.13.0rc2.md)
- [📈time plot](bm-20241022-linux-x86_64-python-34653bba644aa5481613-3.14.0a1%2B-34653bb-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.43x slower (HPT: reliability of 100.00%, 1.34x slower at 99th %ile)
- Memory usage: 1.15x
- [🧠memory plot](bm-20241022-linux-x86_64-python-34653bba644aa5481613-3.14.0a1%2B-34653bb-vs-base-mem.svg)
- [📄table](bm-20241022-linux-x86_64-python-34653bba644aa5481613-3.14.0a1%2B-34653bb-vs-base.md)
- [📈time plot](bm-20241022-linux-x86_64-python-34653bba644aa5481613-3.14.0a1%2B-34653bb-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11470674451)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241022-vultr-x86_64-python-34653bba644aa5481613-3.14.0a1%2B-34653bb.json)

### vs. 3.12.6

- Geometric mean: 1.55x slower (HPT: reliability of 100.00%, 1.39x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20241022-vultr-x86_64-python-34653bba644aa5481613-3.14.0a1%2B-34653bb-vs-3.12.6.md)
- [📈time plot](bm-20241022-vultr-x86_64-python-34653bba644aa5481613-3.14.0a1%2B-34653bb-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.57x slower (HPT: reliability of 100.00%, 1.41x slower at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20241022-vultr-x86_64-python-34653bba644aa5481613-3.14.0a1%2B-34653bb-vs-3.13.0rc2.md)
- [📈time plot](bm-20241022-vultr-x86_64-python-34653bba644aa5481613-3.14.0a1%2B-34653bb-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.54x slower (HPT: reliability of 100.00%, 1.42x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20241022-vultr-x86_64-python-34653bba644aa5481613-3.14.0a1%2B-34653bb-vs-base-mem.svg)
- [📄table](bm-20241022-vultr-x86_64-python-34653bba644aa5481613-3.14.0a1%2B-34653bb-vs-base.md)
- [📈time plot](bm-20241022-vultr-x86_64-python-34653bba644aa5481613-3.14.0a1%2B-34653bb-vs-base.svg)

