# Results

- fork: python
- version: 3.14.0a1+
- config: NOGIL
- commit hash: [4cd1076](https://github.com/python/cpython/commit/4cd1076)
- commit date: 2024-11-18T11:11:23-08:00
- commit merge base: [933f21c3c92f758fb0615d6a4cca10249c686ae7](https://github.com/python/cpython/commit/933f21c3c92f758fb0615d6a4cca10249c686ae7)
- ref: 4cd10762b06ec57252e3

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11900999306)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241118-vultr-x86_64-python-4cd10762b06ec57252e3-3.14.0a1%2B-4cd1076.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.40x slower at 99th %ile)
- Memory usage: 1.24x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [📄table](bm-20241118-vultr-x86_64-python-4cd10762b06ec57252e3-3.14.0a1%2B-4cd1076-vs-3.12.6.md)
- [📈time plot](bm-20241118-vultr-x86_64-python-4cd10762b06ec57252e3-3.14.0a1%2B-4cd1076-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.41x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http
- [📄table](bm-20241118-vultr-x86_64-python-4cd10762b06ec57252e3-3.14.0a1%2B-4cd1076-vs-3.13.0rc2.md)
- [📈time plot](bm-20241118-vultr-x86_64-python-4cd10762b06ec57252e3-3.14.0a1%2B-4cd1076-vs-3.13.0rc2.svg)

