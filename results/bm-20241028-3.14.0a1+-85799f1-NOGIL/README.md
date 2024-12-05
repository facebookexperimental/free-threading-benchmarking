# Results

- fork: python/85799f1ffd5f285ef93a
- version: 3.14.0a1+
- config: NOGIL
- commit hash: [85799f1](https://github.com/python/cpython/commit/85799f1)
- commit date: 2024-10-28T21:53:18+00:00
- commit merge base: [00ea179879726ae221ac7084bdc14752c45ff558](https://github.com/python/cpython/commit/00ea179879726ae221ac7084bdc14752c45ff558)
- ref: 85799f1ffd5f285ef93a

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11564919277)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241028-vultr-x86_64-python-85799f1ffd5f285ef93a-3.14.0a1%2B-85799f1.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.39x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20241028-vultr-x86_64-python-85799f1ffd5f285ef93a-3.14.0a1%2B-85799f1-vs-3.12.6.md)
- [📈time plot](bm-20241028-vultr-x86_64-python-85799f1ffd5f285ef93a-3.14.0a1%2B-85799f1-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.41x slower at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20241028-vultr-x86_64-python-85799f1ffd5f285ef93a-3.14.0a1%2B-85799f1-vs-3.13.0rc2.md)
- [📈time plot](bm-20241028-vultr-x86_64-python-85799f1ffd5f285ef93a-3.14.0a1%2B-85799f1-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.42x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20241028-vultr-x86_64-python-85799f1ffd5f285ef93a-3.14.0a1%2B-85799f1-vs-base-mem.svg)
- [📄table](bm-20241028-vultr-x86_64-python-85799f1ffd5f285ef93a-3.14.0a1%2B-85799f1-vs-base.md)
- [📈time plot](bm-20241028-vultr-x86_64-python-85799f1ffd5f285ef93a-3.14.0a1%2B-85799f1-vs-base.svg)

