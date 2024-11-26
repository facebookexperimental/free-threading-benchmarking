# Results

- fork: python
- version: 3.14.0a1+
- config: 
- commit hash: [b3c6b2c](https://github.com/python/cpython/commit/b3c6b2c)
- commit date: 2024-10-20T23:08:01+02:00
- commit merge base: [ed24702bd0f9925908ce48584c31dfad732208b2](https://github.com/python/cpython/commit/ed24702bd0f9925908ce48584c31dfad732208b2)
- ref: b3c6b2c9e19ea84f617c

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11430924293)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241020-vultr-x86_64-python-b3c6b2c9e19ea84f617c-3.14.0a1%2B-b3c6b2c.json)

### vs. 3.12.6

- Geometric mean: 1.020x faster (HPT: reliability of 99.55%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20241020-vultr-x86_64-python-b3c6b2c9e19ea84f617c-3.14.0a1%2B-b3c6b2c-vs-3.12.6.md)
- [📈time plot](bm-20241020-vultr-x86_64-python-b3c6b2c9e19ea84f617c-3.14.0a1%2B-b3c6b2c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.003x faster (HPT: reliability of 77.73%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20241020-vultr-x86_64-python-b3c6b2c9e19ea84f617c-3.14.0a1%2B-b3c6b2c-vs-3.13.0rc2.md)
- [📈time plot](bm-20241020-vultr-x86_64-python-b3c6b2c9e19ea84f617c-3.14.0a1%2B-b3c6b2c-vs-3.13.0rc2.svg)

