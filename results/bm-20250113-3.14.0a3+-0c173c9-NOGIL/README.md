# Results

- fork: nascheme/nogil_gc_mark_alive
- version: 3.14.0a3+
- config: NOGIL
- commit hash: [0c173c9](https://github.com/nascheme/cpython/commit/0c173c9)
- commit date: 2025-01-13T17:22:52-08:00
- commit merge base: [a1284e97979ff73ad72ad06c796b904137950576](https://github.com/python/cpython/commit/a1284e97979ff73ad72ad06c796b904137950576)
- ref: nogil_gc_mark_alive

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12759088987)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-0c173c9.json)

### vs. 3.12.6

- Geometric mean: 1.160x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-0c173c9-vs-3.12.6.md)
- [📈time plot](bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-0c173c9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.187x slower (HPT: reliability of 100.00%, 1.14x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-0c173c9-vs-3.13.0rc2.md)
- [📈time plot](bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-0c173c9-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.000x faster (HPT: reliability of 84.15%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-0c173c9-vs-base-mem.svg)
- [📄table](bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-0c173c9-vs-base.md)
- [📈time plot](bm-20250113-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-0c173c9-vs-base.svg)

