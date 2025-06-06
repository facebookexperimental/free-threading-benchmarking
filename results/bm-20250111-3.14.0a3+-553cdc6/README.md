# Results

- fork: python/553cdc6d6856c1b4539a
- version: 3.14.0a3+
- config: 
- commit hash: [553cdc6](https://github.com/python/cpython/commit/553cdc6)
- commit date: 2025-01-11T01:03:12+00:00
- commit merge base: [1b39b502d33c68f52fd775c4e6c2174baddd40bd](https://github.com/python/cpython/commit/1b39b502d33c68f52fd775c4e6c2174baddd40bd)
- ref: 553cdc6d6856c1b4539a

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12720021809)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250111-vultr-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6.json)

### vs. 3.12.6

- Geometric mean: 1.101x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250111-vultr-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-3.12.6.md)
- [📈time plot](bm-20250111-vultr-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.062x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250111-vultr-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-3.13.0rc2.md)
- [📈time plot](bm-20250111-vultr-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.001x faster (HPT: reliability of 66.11%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250111-vultr-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-base-mem.svg)
- [📄table](bm-20250111-vultr-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-base.md)
- [📈time plot](bm-20250111-vultr-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-base.svg)

