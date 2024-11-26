# Results

- fork: python
- version: 3.14.0a1+
- config: 
- commit hash: [d3be6f9](https://github.com/python/cpython/commit/d3be6f9)
- commit date: 2024-10-23T16:27:55-07:00
- commit merge base: [8f2c0f7a03b71485b5635cb47c000e4e8ace8800](https://github.com/python/cpython/commit/8f2c0f7a03b71485b5635cb47c000e4e8ace8800)
- ref: d3be6f945a4def7d123b

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11490282607)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241023-vultr-x86_64-python-d3be6f945a4def7d123b-3.14.0a1%2B-d3be6f9.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 99.78%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20241023-vultr-x86_64-python-d3be6f945a4def7d123b-3.14.0a1%2B-d3be6f9-vs-3.12.6.md)
- [📈time plot](bm-20241023-vultr-x86_64-python-d3be6f945a4def7d123b-3.14.0a1%2B-d3be6f9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 59.30%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20241023-vultr-x86_64-python-d3be6f945a4def7d123b-3.14.0a1%2B-d3be6f9-vs-3.13.0rc2.md)
- [📈time plot](bm-20241023-vultr-x86_64-python-d3be6f945a4def7d123b-3.14.0a1%2B-d3be6f9-vs-3.13.0rc2.svg)

