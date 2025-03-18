# Results

- fork: mpage/load_fast_borrow_abs
- version: 3.14.0a6+
- config: 
- commit hash: [6c2f07d](https://github.com/mpage/cpython/commit/6c2f07d)
- commit date: 2025-03-17T16:26:27-07:00
- commit merge base: [fd545d735d5f9c048f99767c700f72853a9b7acd](https://github.com/python/cpython/commit/fd545d735d5f9c048f99767c700f72853a9b7acd)
- ref: load_fast_borrow_abs

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13912466045)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6%2B-6c2f07d.json)

### vs. 3.12.6

- Geometric mean: 1.096x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6%2B-6c2f07d-vs-3.12.6.md)
- [📈time plot](bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6%2B-6c2f07d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.056x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6%2B-6c2f07d-vs-3.13.0rc2.md)
- [📈time plot](bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6%2B-6c2f07d-vs-3.13.0rc2.svg)

