# Results

- fork: python
- version: 3.14.0a1+
- config: 
- commit hash: [9441993](https://github.com/python/cpython/commit/9441993)
- commit date: 2024-11-03T21:22:49+00:00
- commit merge base: [ac556a2ad1213b8bb81372fe6fb762f5fcb076de](https://github.com/python/cpython/commit/ac556a2ad1213b8bb81372fe6fb762f5fcb076de)
- ref: 9441993f272f42e4a97d

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11655970905)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241103-vultr-x86_64-python-9441993f272f42e4a97d-3.14.0a1%2B-9441993.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 98.44%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20241103-vultr-x86_64-python-9441993f272f42e4a97d-3.14.0a1%2B-9441993-vs-3.12.6.md)
- [📈time plot](bm-20241103-vultr-x86_64-python-9441993f272f42e4a97d-3.14.0a1%2B-9441993-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 97.16%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20241103-vultr-x86_64-python-9441993f272f42e4a97d-3.14.0a1%2B-9441993-vs-3.13.0rc2.md)
- [📈time plot](bm-20241103-vultr-x86_64-python-9441993f272f42e4a97d-3.14.0a1%2B-9441993-vs-3.13.0rc2.svg)

