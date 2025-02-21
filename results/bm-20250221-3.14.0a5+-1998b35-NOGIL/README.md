# Results

- fork: mpage/load_fast_borrow_abs
- version: 3.14.0a5+
- config: NOGIL
- commit hash: [1998b35](https://github.com/mpage/cpython/commit/1998b35)
- commit date: 2025-02-21T11:45:00-08:00
- commit merge base: [6c450f44c283c61d0e1ada05ead9524a1fe97962](https://github.com/python/cpython/commit/6c450f44c283c61d0e1ada05ead9524a1fe97962)
- ref: load_fast_borrow_abs

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13465084758)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-1998b35.json)

### vs. 3.12.6

- Geometric mean: 1.002x faster (HPT: reliability of 96.18%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-1998b35-vs-3.12.6.md)
- [📈time plot](bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-1998b35-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.031x slower (HPT: reliability of 99.75%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-1998b35-vs-3.13.0rc2.md)
- [📈time plot](bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-1998b35-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.043x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-1998b35-vs-base-mem.svg)
- [📄table](bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-1998b35-vs-base.md)
- [📈time plot](bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-1998b35-vs-base.svg)

