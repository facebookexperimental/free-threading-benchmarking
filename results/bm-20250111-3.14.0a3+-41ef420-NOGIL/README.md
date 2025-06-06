# Results

- fork: nascheme/nogil_gc_mark_alive
- version: 3.14.0a3+
- config: NOGIL
- commit hash: [41ef420](https://github.com/nascheme/cpython/commit/41ef420)
- commit date: 2025-01-11T16:55:18-08:00
- commit merge base: [a1284e97979ff73ad72ad06c796b904137950576](https://github.com/python/cpython/commit/a1284e97979ff73ad72ad06c796b904137950576)
- ref: nogil_gc_mark_alive

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12735235199)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250111-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-41ef420.json)

### vs. 3.12.6

- Geometric mean: 1.151x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250111-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-41ef420-vs-3.12.6.md)
- [📈time plot](bm-20250111-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-41ef420-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.178x slower (HPT: reliability of 100.00%, 1.13x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250111-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-41ef420-vs-3.13.0rc2.md)
- [📈time plot](bm-20250111-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-41ef420-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.009x faster (HPT: reliability of 99.99%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- [🧠memory plot](bm-20250111-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-41ef420-vs-base-mem.svg)
- [📄table](bm-20250111-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-41ef420-vs-base.md)
- [📈time plot](bm-20250111-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-41ef420-vs-base.svg)

