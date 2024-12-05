# Results

- fork: python/f0c6fccd08904787a392
- version: 3.14.0a1+
- config: 
- commit hash: [f0c6fcc](https://github.com/python/cpython/commit/f0c6fcc)
- commit date: 2024-11-01T23:10:58+00:00
- commit merge base: [8477951a1c460ff9b7dc7c54e7bf9b66b1722459](https://github.com/python/cpython/commit/8477951a1c460ff9b7dc7c54e7bf9b66b1722459)
- ref: f0c6fccd08904787a392

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11638214316)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241101-vultr-x86_64-python-f0c6fccd08904787a392-3.14.0a1%2B-f0c6fcc.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 99.10%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20241101-vultr-x86_64-python-f0c6fccd08904787a392-3.14.0a1%2B-f0c6fcc-vs-3.12.6.md)
- [📈time plot](bm-20241101-vultr-x86_64-python-f0c6fccd08904787a392-3.14.0a1%2B-f0c6fcc-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 96.97%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20241101-vultr-x86_64-python-f0c6fccd08904787a392-3.14.0a1%2B-f0c6fcc-vs-3.13.0rc2.md)
- [📈time plot](bm-20241101-vultr-x86_64-python-f0c6fccd08904787a392-3.14.0a1%2B-f0c6fcc-vs-3.13.0rc2.svg)

