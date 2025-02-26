# Results

- fork: mpage/load_fast_borrow_abs
- version: 3.14.0a5+
- config: NOGIL
- commit hash: [b10c3be](https://github.com/mpage/cpython/commit/b10c3be)
- commit date: 2025-02-26T09:25:31-08:00
- commit merge base: [9e474a98af4184615540467dea16da05f4d284d8](https://github.com/python/cpython/commit/9e474a98af4184615540467dea16da05f4d284d8)
- ref: load_fast_borrow_abs

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13550274665)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-b10c3be.json)

### vs. 3.12.6

- Geometric mean: 1.023x slower (HPT: reliability of 99.88%, 1.01x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-b10c3be-vs-3.12.6.md)
- [📈time plot](bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-b10c3be-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.055x slower (HPT: reliability of 99.95%, 1.03x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-b10c3be-vs-3.13.0rc2.md)
- [📈time plot](bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-b10c3be-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.025x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-b10c3be-vs-base-mem.svg)
- [📄table](bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-b10c3be-vs-base.md)
- [📈time plot](bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-b10c3be-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.109x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [📄table](bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-b10c3be-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20250226-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-b10c3be-vs-default_base_vs_NOGIL.svg)

