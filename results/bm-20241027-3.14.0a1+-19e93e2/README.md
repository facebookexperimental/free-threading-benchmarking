# Results

- fork: python
- version: 3.14.0a1+
- config: 
- commit hash: [19e93e2](https://github.com/python/cpython/commit/19e93e2)
- commit date: 2024-10-27T22:55:48+01:00
- commit merge base: [6870eb3f7322ed64a1ca8bbda5cf4e121e181b54](https://github.com/python/cpython/commit/6870eb3f7322ed64a1ca8bbda5cf4e121e181b54)
- ref: 19e93e2e269889ecb3c4

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11545097848)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241027-vultr-x86_64-python-19e93e2e269889ecb3c4-3.14.0a1%2B-19e93e2.json)

### vs. 3.12.6

- Geometric mean: 1.017x faster (HPT: reliability of 94.67%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
- [📄table](bm-20241027-vultr-x86_64-python-19e93e2e269889ecb3c4-3.14.0a1%2B-19e93e2-vs-3.12.6.md)
- [📈time plot](bm-20241027-vultr-x86_64-python-19e93e2e269889ecb3c4-3.14.0a1%2B-19e93e2-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.000x slower (HPT: reliability of 87.94%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn
- [📄table](bm-20241027-vultr-x86_64-python-19e93e2e269889ecb3c4-3.14.0a1%2B-19e93e2-vs-3.13.0rc2.md)
- [📈time plot](bm-20241027-vultr-x86_64-python-19e93e2e269889ecb3c4-3.14.0a1%2B-19e93e2-vs-3.13.0rc2.svg)

