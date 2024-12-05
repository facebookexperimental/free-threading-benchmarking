# Results

- fork: python/3fecbe9255391be1ac3c
- version: 3.14.0a1+
- config: 
- commit hash: [3fecbe9](https://github.com/python/cpython/commit/3fecbe9)
- commit date: 2024-11-15T00:22:50+00:00
- commit merge base: [9a456383bed52010b90bd491277ea855626a7bba](https://github.com/python/cpython/commit/9a456383bed52010b90bd491277ea855626a7bba)
- ref: 3fecbe9255391be1ac3c

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11847880488)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1%2B-3fecbe9.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 99.97%, 1.01x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [📄table](bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1%2B-3fecbe9-vs-3.12.6.md)
- [📈time plot](bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1%2B-3fecbe9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 99.82%, 1.00x faster at 99th %ile)
- Memory usage: 1.01x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http
- [📄table](bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1%2B-3fecbe9-vs-3.13.0rc2.md)
- [📈time plot](bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1%2B-3fecbe9-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/11847880488)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1%2B-3fecbe9.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 96.22%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http
- [📄table](bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1%2B-3fecbe9-vs-3.12.6.md)
- [📈time plot](bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1%2B-3fecbe9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 95.40%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http
- [📄table](bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1%2B-3fecbe9-vs-3.13.0rc2.md)
- [📈time plot](bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1%2B-3fecbe9-vs-3.13.0rc2.svg)

