# Results

- fork: nascheme/nogil_gc_mark_alive
- version: 3.14.0a3+
- config: NOGIL
- commit hash: [f509a13](https://github.com/nascheme/cpython/commit/f509a13)
- commit date: 2025-01-09T20:26:29-08:00
- commit merge base: [a1284e97979ff73ad72ad06c796b904137950576](https://github.com/python/cpython/commit/a1284e97979ff73ad72ad06c796b904137950576)
- ref: nogil_gc_mark_alive

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12715443462)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250109-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-f509a13.json)

### vs. 3.12.6

- Geometric mean: 1.184x slower (HPT: reliability of 100.00%, 1.15x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250109-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-f509a13-vs-3.12.6.md)
- [📈time plot](bm-20250109-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-f509a13-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.213x slower (HPT: reliability of 100.00%, 1.19x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250109-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-f509a13-vs-3.13.0rc2.md)
- [📈time plot](bm-20250109-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-f509a13-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.058x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250109-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-f509a13-vs-base-mem.svg)
- [📄table](bm-20250109-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-f509a13-vs-base.md)
- [📈time plot](bm-20250109-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-f509a13-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.253x slower (HPT: reliability of 100.00%, 1.27x slower at 99th %ile)
- Memory usage: 1.19x
- [📄table](bm-20250109-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-f509a13-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20250109-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3%2B-f509a13-vs-default_base_vs_NOGIL.svg)

