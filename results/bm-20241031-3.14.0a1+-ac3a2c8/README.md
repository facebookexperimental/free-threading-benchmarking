# Results

- fork: python
- version: 3.14.0a1+
- config: 
- commit hash: [ac3a2c8](https://github.com/python/cpython/commit/ac3a2c8)
- commit date: 2024-10-31T00:12:37+00:00
- commit merge base: [951cb2c369e8b8fb9f93662658391a53fd727787](https://github.com/python/cpython/commit/951cb2c369e8b8fb9f93662658391a53fd727787)
- ref: ac3a2c8abceeec448486

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11603802920)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241031-vultr-x86_64-python-ac3a2c8abceeec448486-3.14.0a1%2B-ac3a2c8.json)

### vs. 3.12.6

- Geometric mean: 1.018x faster (HPT: reliability of 99.33%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20241031-vultr-x86_64-python-ac3a2c8abceeec448486-3.14.0a1%2B-ac3a2c8-vs-3.12.6.md)
- [📈time plot](bm-20241031-vultr-x86_64-python-ac3a2c8abceeec448486-3.14.0a1%2B-ac3a2c8-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.001x faster (HPT: reliability of 87.78%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20241031-vultr-x86_64-python-ac3a2c8abceeec448486-3.14.0a1%2B-ac3a2c8-vs-3.13.0rc2.md)
- [📈time plot](bm-20241031-vultr-x86_64-python-ac3a2c8abceeec448486-3.14.0a1%2B-ac3a2c8-vs-3.13.0rc2.svg)

