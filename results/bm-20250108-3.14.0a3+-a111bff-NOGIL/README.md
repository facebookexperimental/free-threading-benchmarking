# Results

- fork: nascheme/nogil_gc_mark_alive
- version: 3.14.0a3+
- config: NOGIL
- commit hash: [a111bff](https://github.com/nascheme/cpython/commit/a111bff)
- commit date: 2025-01-08T16:55:09-08:00
- commit merge base: [a1284e97979ff73ad72ad06c796b904137950576](https://github.com/python/cpython/commit/a1284e97979ff73ad72ad06c796b904137950576)
- ref: nogil_gc_mark_alive

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12695725784)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250108-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-a111bff.json)

### vs. 3.12.6

- Geometric mean: 1.161x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250108-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-a111bff-vs-3.12.6.md)
- [📈time plot](bm-20250108-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-a111bff-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.188x slower (HPT: reliability of 100.00%, 1.14x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250108-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-a111bff-vs-3.13.0rc2.md)
- [📈time plot](bm-20250108-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-a111bff-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.002x slower (HPT: reliability of 98.39%, 1.00x slower at 99th %ile)
- Memory usage: 1.02x
- [🧠memory plot](bm-20250108-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-a111bff-vs-base-mem.svg)
- [📄table](bm-20250108-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-a111bff-vs-base.md)
- [📈time plot](bm-20250108-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-a111bff-vs-base.svg)

