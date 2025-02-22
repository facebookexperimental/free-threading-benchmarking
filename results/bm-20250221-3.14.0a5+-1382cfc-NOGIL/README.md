# Results

- fork: mpage/load_fast_borrow_abs
- version: 3.14.0a5+
- config: NOGIL
- commit hash: [1382cfc](https://github.com/mpage/cpython/commit/1382cfc)
- commit date: 2025-02-21T21:41:01-08:00
- commit merge base: [6c450f44c283c61d0e1ada05ead9524a1fe97962](https://github.com/python/cpython/commit/6c450f44c283c61d0e1ada05ead9524a1fe97962)
- ref: load_fast_borrow_abs

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13470658959)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-1382cfc.json)

### vs. 3.12.6

- Geometric mean: 1.012x faster (HPT: reliability of 91.01%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-1382cfc-vs-3.12.6.md)
- [📈time plot](bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-1382cfc-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.021x slower (HPT: reliability of 96.82%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-1382cfc-vs-3.13.0rc2.md)
- [📈time plot](bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-1382cfc-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.053x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.03x
- [🧠memory plot](bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-1382cfc-vs-base-mem.svg)
- [📄table](bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-1382cfc-vs-base.md)
- [📈time plot](bm-20250221-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-1382cfc-vs-base.svg)

