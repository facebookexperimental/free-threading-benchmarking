# Results

- fork: python
- version: 3.14.0a1+
- config: 
- commit hash: [f435de6](https://github.com/python/cpython/commit/f435de6)
- commit date: 2024-11-10T23:44:56+02:00
- commit merge base: [ca878b6e45f9c7934842f7bb94274e671b155e09](https://github.com/python/cpython/commit/ca878b6e45f9c7934842f7bb94274e671b155e09)
- ref: f435de6765e032799585

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11769821222)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20241110-linux-x86_64-python-f435de6765e032799585-3.14.0a1%2B-f435de6.json)

### vs. 3.12.6

- Geometric mean: 1.026x faster (HPT: reliability of 87.46%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [📄table](bm-20241110-linux-x86_64-python-f435de6765e032799585-3.14.0a1%2B-f435de6-vs-3.12.6.md)
- [📈time plot](bm-20241110-linux-x86_64-python-f435de6765e032799585-3.14.0a1%2B-f435de6-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.014x faster (HPT: reliability of 62.72%, 1.00x faster at 99th %ile)
- Memory usage: 1.01x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http
- [📄table](bm-20241110-linux-x86_64-python-f435de6765e032799585-3.14.0a1%2B-f435de6-vs-3.13.0rc2.md)
- [📈time plot](bm-20241110-linux-x86_64-python-f435de6765e032799585-3.14.0a1%2B-f435de6-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11769821222)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241110-vultr-x86_64-python-f435de6765e032799585-3.14.0a1%2B-f435de6.json)

### vs. 3.12.6

- Geometric mean: 1.018x faster (HPT: reliability of 96.94%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [📄table](bm-20241110-vultr-x86_64-python-f435de6765e032799585-3.14.0a1%2B-f435de6-vs-3.12.6.md)
- [📈time plot](bm-20241110-vultr-x86_64-python-f435de6765e032799585-3.14.0a1%2B-f435de6-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.002x faster (HPT: reliability of 80.32%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http
- [📄table](bm-20241110-vultr-x86_64-python-f435de6765e032799585-3.14.0a1%2B-f435de6-vs-3.13.0rc2.md)
- [📈time plot](bm-20241110-vultr-x86_64-python-f435de6765e032799585-3.14.0a1%2B-f435de6-vs-3.13.0rc2.svg)

