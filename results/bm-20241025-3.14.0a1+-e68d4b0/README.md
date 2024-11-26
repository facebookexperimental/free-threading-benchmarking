# Results

- fork: python
- version: 3.14.0a1+
- config: 
- commit hash: [e68d4b0](https://github.com/python/cpython/commit/e68d4b0)
- commit date: 2024-10-25T07:51:16+08:00
- commit merge base: [fed501d7247053ce46a2ba512bf0e4bb4f483be6](https://github.com/python/cpython/commit/fed501d7247053ce46a2ba512bf0e4bb4f483be6)
- ref: e68d4b08ff13a06a2c28

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11509575727)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241025-vultr-x86_64-python-e68d4b08ff13a06a2c28-3.14.0a1%2B-e68d4b0.json)

### vs. 3.12.6

- Geometric mean: 1.021x faster (HPT: reliability of 99.54%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20241025-vultr-x86_64-python-e68d4b08ff13a06a2c28-3.14.0a1%2B-e68d4b0-vs-3.12.6.md)
- [📈time plot](bm-20241025-vultr-x86_64-python-e68d4b08ff13a06a2c28-3.14.0a1%2B-e68d4b0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.004x faster (HPT: reliability of 50.90%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20241025-vultr-x86_64-python-e68d4b08ff13a06a2c28-3.14.0a1%2B-e68d4b0-vs-3.13.0rc2.md)
- [📈time plot](bm-20241025-vultr-x86_64-python-e68d4b08ff13a06a2c28-3.14.0a1%2B-e68d4b0-vs-3.13.0rc2.svg)

