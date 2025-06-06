# Results

- fork: python/34653bba644aa5481613
- version: 3.14.0a1+
- config: NOGIL
- commit hash: [34653bb](https://github.com/python/cpython/commit/34653bb)
- commit date: 2024-10-22T13:42:22-07:00
- commit merge base: [aaed91cabcedc16c089c4b1c9abb1114659a83d3](https://github.com/python/cpython/commit/aaed91cabcedc16c089c4b1c9abb1114659a83d3)
- ref: 34653bba644aa5481613

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11470674451)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241022-vultr-x86_64-python-34653bba644aa5481613-3.14.0a1%2B-34653bb.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.39x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20241022-vultr-x86_64-python-34653bba644aa5481613-3.14.0a1%2B-34653bb-vs-3.12.6.md)
- [📈time plot](bm-20241022-vultr-x86_64-python-34653bba644aa5481613-3.14.0a1%2B-34653bb-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.41x slower at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20241022-vultr-x86_64-python-34653bba644aa5481613-3.14.0a1%2B-34653bb-vs-3.13.0rc2.md)
- [📈time plot](bm-20241022-vultr-x86_64-python-34653bba644aa5481613-3.14.0a1%2B-34653bb-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.42x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20241022-vultr-x86_64-python-34653bba644aa5481613-3.14.0a1%2B-34653bb-vs-base-mem.svg)
- [📄table](bm-20241022-vultr-x86_64-python-34653bba644aa5481613-3.14.0a1%2B-34653bb-vs-base.md)
- [📈time plot](bm-20241022-vultr-x86_64-python-34653bba644aa5481613-3.14.0a1%2B-34653bb-vs-base.svg)

