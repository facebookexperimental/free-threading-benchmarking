# Results

- fork: python/553cdc6d6856c1b4539a
- version: 3.14.0a3+
- config: 
- commit hash: [553cdc6](https://github.com/python/cpython/commit/553cdc6)
- commit date: 2025-01-11T01:03:12+00:00
- commit merge base: [1b39b502d33c68f52fd775c4e6c2174baddd40bd](https://github.com/python/cpython/commit/1b39b502d33c68f52fd775c4e6c2174baddd40bd)
- ref: 553cdc6d6856c1b4539a

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12720021809)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250111-linux-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6.json)

### vs. 3.12.6

- Geometric mean: 1.071x faster (HPT: reliability of 99.98%, 1.01x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250111-linux-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-3.12.6.md)
- [📈time plot](bm-20250111-linux-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.034x faster (HPT: reliability of 97.69%, 1.00x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250111-linux-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-3.13.0rc2.md)
- [📈time plot](bm-20250111-linux-x86_64-python-553cdc6d6856c1b4539a-3.14.0a3%2B-553cdc6-vs-3.13.0rc2.svg)

