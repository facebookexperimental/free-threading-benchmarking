# Results

- fork: mpage/load_fast_borrow_abs
- version: 3.14.0a5+
- config: 
- commit hash: [b10c3be](https://github.com/mpage/cpython/commit/b10c3be)
- commit date: 2025-02-26T09:25:31-08:00
- commit merge base: [9e474a98af4184615540467dea16da05f4d284d8](https://github.com/python/cpython/commit/9e474a98af4184615540467dea16da05f4d284d8)
- ref: load_fast_borrow_abs

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13550277224)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-b10c3be.json)

### vs. 3.12.6

- Geometric mean: 1.101x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-b10c3be-vs-3.12.6.md)
- [📈time plot](bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-b10c3be-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.061x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-b10c3be-vs-3.13.0rc2.md)
- [📈time plot](bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-b10c3be-vs-3.13.0rc2.svg)

