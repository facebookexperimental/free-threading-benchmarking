# Results

- fork: mpage/load_fast_borrow_abs
- version: 3.14.0a5+
- config: NOGIL
- commit hash: [f012a9f](https://github.com/mpage/cpython/commit/f012a9f)
- commit date: 2025-02-28T19:25:30-08:00
- commit merge base: [75f38af7810af1c3ca567d6224a975f85aef970f](https://github.com/python/cpython/commit/75f38af7810af1c3ca567d6224a975f85aef970f)
- ref: load_fast_borrow_abs

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13595977471)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-f012a9f.json)

### vs. 3.12.6

- Geometric mean: 1.017x slower (HPT: reliability of 99.71%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-f012a9f-vs-3.12.6.md)
- [📈time plot](bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-f012a9f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.049x slower (HPT: reliability of 99.90%, 1.02x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-f012a9f-vs-3.13.0rc2.md)
- [📈time plot](bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-f012a9f-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.028x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-f012a9f-vs-base-mem.svg)
- [📄table](bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-f012a9f-vs-base.md)
- [📈time plot](bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-f012a9f-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.108x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.21x
- new benchmarks: html5lib
- [📄table](bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-f012a9f-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-f012a9f-vs-default_base_vs_NOGIL.svg)

