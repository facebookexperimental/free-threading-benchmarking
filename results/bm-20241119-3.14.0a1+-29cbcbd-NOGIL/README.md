# Results

- fork: python
- version: 3.14.0a1+
- config: NOGIL
- commit hash: [29cbcbd](https://github.com/python/cpython/commit/29cbcbd)
- commit date: 2024-11-19T18:00:35+02:00
- commit merge base: [c5c9286804e38c95fe717f22ce1bf2f18eee5b17](https://github.com/python/cpython/commit/c5c9286804e38c95fe717f22ce1bf2f18eee5b17)
- ref: 29cbcbd73bbfd8c953c0

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11917792707)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241119-vultr-x86_64-python-29cbcbd73bbfd8c953c0-3.14.0a1%2B-29cbcbd.json)

### vs. 3.12.6

- Geometric mean: 1.55x slower (HPT: reliability of 100.00%, 1.39x slower at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [📄table](bm-20241119-vultr-x86_64-python-29cbcbd73bbfd8c953c0-3.14.0a1%2B-29cbcbd-vs-3.12.6.md)
- [📈time plot](bm-20241119-vultr-x86_64-python-29cbcbd73bbfd8c953c0-3.14.0a1%2B-29cbcbd-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.58x slower (HPT: reliability of 100.00%, 1.40x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http
- [📄table](bm-20241119-vultr-x86_64-python-29cbcbd73bbfd8c953c0-3.14.0a1%2B-29cbcbd-vs-3.13.0rc2.md)
- [📈time plot](bm-20241119-vultr-x86_64-python-29cbcbd73bbfd8c953c0-3.14.0a1%2B-29cbcbd-vs-3.13.0rc2.svg)

