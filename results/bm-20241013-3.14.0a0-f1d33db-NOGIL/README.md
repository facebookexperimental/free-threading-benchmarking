# Results

- fork: python
- version: 3.14.0a0
- config: NOGIL
- commit hash: [f1d33db](https://github.com/python/cpython/commit/f1d33db)
- commit date: 2024-10-13T16:17:51-04:00
- commit merge base: [cb8e5995d89d9b90e83cf43310ec50e177484e70](https://github.com/python/cpython/commit/cb8e5995d89d9b90e83cf43310ec50e177484e70)
- ref: f1d33dbddd3496b062e1

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11336596568)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db.json)

### vs. 3.12.6

- Geometric mean: 1.54x slower (HPT: reliability of 100.00%, 1.39x slower at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db-vs-3.12.6.md)
- [📈time plot](bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.57x slower (HPT: reliability of 100.00%, 1.41x slower at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db-vs-3.13.0rc2.md)
- [📈time plot](bm-20241013-vultr-x86_64-python-f1d33dbddd3496b062e1-3.14.0a0-f1d33db-vs-3.13.0rc2.svg)

