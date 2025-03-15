# Results

- fork: mpage/measure_interp_loop_
- version: 3.14.0a5+
- config: NOGIL
- commit hash: [5264e56](https://github.com/mpage/cpython/commit/5264e56)
- commit date: 2025-03-15T09:54:39-07:00
- commit merge base: [1a8e5742cdcf3dba7fc592d036adab49877c42ba](https://github.com/python/cpython/commit/1a8e5742cdcf3dba7fc592d036adab49877c42ba)
- ref: measure_interp_loop_

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13874841504)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250315-vultr-x86_64-mpage-measure_interp_loop_-3.14.0a5%2B-5264e56.json)

### vs. 3.12.6

- Geometric mean: 1.035x slower (HPT: reliability of 99.98%, 1.02x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250315-vultr-x86_64-mpage-measure_interp_loop_-3.14.0a5%2B-5264e56-vs-3.12.6.md)
- [📈time plot](bm-20250315-vultr-x86_64-mpage-measure_interp_loop_-3.14.0a5%2B-5264e56-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.067x slower (HPT: reliability of 99.98%, 1.04x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250315-vultr-x86_64-mpage-measure_interp_loop_-3.14.0a5%2B-5264e56-vs-3.13.0rc2.md)
- [📈time plot](bm-20250315-vultr-x86_64-mpage-measure_interp_loop_-3.14.0a5%2B-5264e56-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.015x faster (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20250315-vultr-x86_64-mpage-measure_interp_loop_-3.14.0a5%2B-5264e56-vs-base-mem.svg)
- [📄table](bm-20250315-vultr-x86_64-mpage-measure_interp_loop_-3.14.0a5%2B-5264e56-vs-base.md)
- [📈time plot](bm-20250315-vultr-x86_64-mpage-measure_interp_loop_-3.14.0a5%2B-5264e56-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.092x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [📄table](bm-20250315-vultr-x86_64-mpage-measure_interp_loop_-3.14.0a5%2B-5264e56-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20250315-vultr-x86_64-mpage-measure_interp_loop_-3.14.0a5%2B-5264e56-vs-default_base_vs_NOGIL.svg)

