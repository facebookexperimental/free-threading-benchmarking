# Results

- fork: python/322f14eeff9e3b5853ea
- version: 3.14.0a1+
- config: NOGIL
- commit hash: [322f14e](https://github.com/python/cpython/commit/322f14e)
- commit date: 2024-10-18T16:05:12-06:00
- commit merge base: [c8fd4b12e3db49d795de55f74d9bac445c059f1b](https://github.com/python/cpython/commit/c8fd4b12e3db49d795de55f74d9bac445c059f1b)
- ref: 322f14eeff9e3b5853ea

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11412841746)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241018-vultr-x86_64-python-322f14eeff9e3b5853ea-3.14.0a1%2B-322f14e.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.39x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20241018-vultr-x86_64-python-322f14eeff9e3b5853ea-3.14.0a1%2B-322f14e-vs-3.12.6.md)
- [📈time plot](bm-20241018-vultr-x86_64-python-322f14eeff9e3b5853ea-3.14.0a1%2B-322f14e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.42x slower at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20241018-vultr-x86_64-python-322f14eeff9e3b5853ea-3.14.0a1%2B-322f14e-vs-3.13.0rc2.md)
- [📈time plot](bm-20241018-vultr-x86_64-python-322f14eeff9e3b5853ea-3.14.0a1%2B-322f14e-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.43x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20241018-vultr-x86_64-python-322f14eeff9e3b5853ea-3.14.0a1%2B-322f14e-vs-base-mem.svg)
- [📄table](bm-20241018-vultr-x86_64-python-322f14eeff9e3b5853ea-3.14.0a1%2B-322f14e-vs-base.md)
- [📈time plot](bm-20241018-vultr-x86_64-python-322f14eeff9e3b5853ea-3.14.0a1%2B-322f14e-vs-base.svg)

