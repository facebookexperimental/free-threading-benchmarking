# Results

- fork: python/553cdc6d6856c1b4539a
- version: 3.14.0a3+
- config: NOGIL
- commit hash: [553cdc6](https://github.com/python/cpython/commit/553cdc6)
- commit date: 2025-01-11T01:03:12+00:00
- commit merge base: [1b39b502d33c68f52fd775c4e6c2174baddd40bd](https://github.com/python/cpython/commit/1b39b502d33c68f52fd775c4e6c2174baddd40bd)
- ref: 553cdc6d6856c1b4539a

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12818460672)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250111-vultr-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6.json)

### vs. 3.12.6

- Geometric mean: 1.160x slower (HPT: reliability of 100.00%, 1.13x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250111-vultr-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-3.12.6.md)
- [📈time plot](bm-20250111-vultr-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.187x slower (HPT: reliability of 100.00%, 1.14x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250111-vultr-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-3.13.0rc2.md)
- [📈time plot](bm-20250111-vultr-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.002x slower (HPT: reliability of 80.63%, 1.00x slower at 99th %ile)
- Memory usage: 0.99x
- [🧠memory plot](bm-20250111-vultr-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-base-mem.svg)
- [📄table](bm-20250111-vultr-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-base.md)
- [📈time plot](bm-20250111-vultr-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.232x slower (HPT: reliability of 100.00%, 1.23x slower at 99th %ile)
- Memory usage: 1.19x
- new benchmarks: html5lib
- [📄table](bm-20250111-vultr-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20250111-vultr-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-default_base_vs_NOGIL.svg)

