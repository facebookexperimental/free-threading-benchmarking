# Results

- fork: python
- version: 3.14.0a1+
- config: 
- commit hash: [85036c8](https://github.com/python/cpython/commit/85036c8)
- commit date: 2024-11-07T10:48:27+00:00
- commit merge base: [c9cda1608edf7664c10f4f467e24591062c2fe62](https://github.com/python/cpython/commit/c9cda1608edf7664c10f4f467e24591062c2fe62)
- ref: 85036c8d612007356d21

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11804452687)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241107-vultr-x86_64-python-85036c8d612007356d21-3.14.0a1%2B-85036c8.json)

### vs. 3.12.6

- Geometric mean: 1.020x faster (HPT: reliability of 99.53%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [📄table](bm-20241107-vultr-x86_64-python-85036c8d612007356d21-3.14.0a1%2B-85036c8-vs-3.12.6.md)
- [📈time plot](bm-20241107-vultr-x86_64-python-85036c8d612007356d21-3.14.0a1%2B-85036c8-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.004x faster (HPT: reliability of 64.91%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http
- [📄table](bm-20241107-vultr-x86_64-python-85036c8d612007356d21-3.14.0a1%2B-85036c8-vs-3.13.0rc2.md)
- [📈time plot](bm-20241107-vultr-x86_64-python-85036c8d612007356d21-3.14.0a1%2B-85036c8-vs-3.13.0rc2.svg)

