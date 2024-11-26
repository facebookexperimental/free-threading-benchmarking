# Results

- fork: python
- version: 3.14.0a1+
- config: 
- commit hash: [d4b6d84](https://github.com/python/cpython/commit/d4b6d84)
- commit date: 2024-10-29T17:13:11-07:00
- commit merge base: [2d37c719ed7c54430257028be6b48a1e2d065973](https://github.com/python/cpython/commit/2d37c719ed7c54430257028be6b48a1e2d065973)
- ref: d4b6d84cc84029b598fc

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11584647167)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241029-vultr-x86_64-python-d4b6d84cc84029b598fc-3.14.0a1%2B-d4b6d84.json)

### vs. 3.12.6

- Geometric mean: 1.018x faster (HPT: reliability of 97.18%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20241029-vultr-x86_64-python-d4b6d84cc84029b598fc-3.14.0a1%2B-d4b6d84-vs-3.12.6.md)
- [📈time plot](bm-20241029-vultr-x86_64-python-d4b6d84cc84029b598fc-3.14.0a1%2B-d4b6d84-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.001x faster (HPT: reliability of 93.10%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20241029-vultr-x86_64-python-d4b6d84cc84029b598fc-3.14.0a1%2B-d4b6d84-vs-3.13.0rc2.md)
- [📈time plot](bm-20241029-vultr-x86_64-python-d4b6d84cc84029b598fc-3.14.0a1%2B-d4b6d84-vs-3.13.0rc2.svg)

