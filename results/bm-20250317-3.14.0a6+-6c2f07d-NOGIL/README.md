# Results

- fork: mpage/load_fast_borrow_abs
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [6c2f07d](https://github.com/mpage/cpython/commit/6c2f07d)
- commit date: 2025-03-17T16:26:27-07:00
- commit merge base: [fd545d735d5f9c048f99767c700f72853a9b7acd](https://github.com/python/cpython/commit/fd545d735d5f9c048f99767c700f72853a9b7acd)
- ref: load_fast_borrow_abs

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13912462625)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6%2B-6c2f07d.json)

### vs. 3.12.6

- Geometric mean: 1.020x slower (HPT: reliability of 99.49%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6%2B-6c2f07d-vs-3.12.6.md)
- [📈time plot](bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6%2B-6c2f07d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.052x slower (HPT: reliability of 99.88%, 1.01x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6%2B-6c2f07d-vs-3.13.0rc2.md)
- [📈time plot](bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6%2B-6c2f07d-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.027x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6%2B-6c2f07d-vs-base-mem.svg)
- [📄table](bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6%2B-6c2f07d-vs-base.md)
- [📈time plot](bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6%2B-6c2f07d-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.079x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [📄table](bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6%2B-6c2f07d-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6%2B-6c2f07d-vs-default_base_vs_NOGIL.svg)

