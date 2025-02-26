# Results

- fork: mpage/load_fast_borrow_abs
- version: 3.14.0a5+
- config: 
- commit hash: [48e2f9e](https://github.com/mpage/cpython/commit/48e2f9e)
- commit date: 2025-02-25T23:11:24-08:00
- commit merge base: [0ef4ffeefd1737c18dc9326133c7894d58108c2e](https://github.com/python/cpython/commit/0ef4ffeefd1737c18dc9326133c7894d58108c2e)
- ref: load_fast_borrow_abs

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13538476616)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-48e2f9e.json)

### vs. 3.12.6

- Geometric mean: 1.112x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-48e2f9e-vs-3.12.6.md)
- [📈time plot](bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-48e2f9e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.071x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-48e2f9e-vs-3.13.0rc2.md)
- [📈time plot](bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-48e2f9e-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.012x faster (HPT: reliability of 97.52%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-48e2f9e-vs-base-mem.svg)
- [📄table](bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-48e2f9e-vs-base.md)
- [📈time plot](bm-20250225-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5%2B-48e2f9e-vs-base.svg)

