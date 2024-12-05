# Results

- fork: colesbury/cheaper_steal
- version: 3.14.0a1+
- config: NOGIL
- commit hash: [ed7085a](https://github.com/colesbury/cpython/commit/ed7085a)
- commit date: 2024-11-18T20:59:42+00:00
- commit merge base: [4cd10762b06ec57252e3c7373e74240b4d0c5ed8](https://github.com/python/cpython/commit/4cd10762b06ec57252e3c7373e74240b4d0c5ed8)
- ref: cheaper_steal

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11900999306)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241118-vultr-x86_64-colesbury-cheaper_steal-3.14.0a1%2B-ed7085a.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.36x slower at 99th %ile)
- Memory usage: 1.24x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [📄table](bm-20241118-vultr-x86_64-colesbury-cheaper_steal-3.14.0a1%2B-ed7085a-vs-3.12.6.md)
- [📈time plot](bm-20241118-vultr-x86_64-colesbury-cheaper_steal-3.14.0a1%2B-ed7085a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.38x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http
- [📄table](bm-20241118-vultr-x86_64-colesbury-cheaper_steal-3.14.0a1%2B-ed7085a-vs-3.13.0rc2.md)
- [📈time plot](bm-20241118-vultr-x86_64-colesbury-cheaper_steal-3.14.0a1%2B-ed7085a-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: not sig (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20241118-vultr-x86_64-colesbury-cheaper_steal-3.14.0a1%2B-ed7085a-vs-base-mem.svg)
- [📄table](bm-20241118-vultr-x86_64-colesbury-cheaper_steal-3.14.0a1%2B-ed7085a-vs-base.md)
- [📈time plot](bm-20241118-vultr-x86_64-colesbury-cheaper_steal-3.14.0a1%2B-ed7085a-vs-base.svg)

