# Results

- fork: python/ae4788809d674f8e27fa
- version: 3.14.0a4+
- config: 
- commit hash: [ae47888](https://github.com/python/cpython/commit/ae47888)
- commit date: 2025-02-02T16:17:02+00:00
- commit merge base: [0612a89ffcf0bb52b1750a3466671ba8daad1d87](https://github.com/python/cpython/commit/0612a89ffcf0bb52b1750a3466671ba8daad1d87)
- ref: ae4788809d674f8e27fa

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13100479381)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250202-vultr-x86_64-python-ae4788809d674f8e27fa-3.14.0a4%2B-ae47888.json)

### vs. 3.12.6

- Geometric mean: 1.100x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250202-vultr-x86_64-python-ae4788809d674f8e27fa-3.14.0a4%2B-ae47888-vs-3.12.6.md)
- [📈time plot](bm-20250202-vultr-x86_64-python-ae4788809d674f8e27fa-3.14.0a4%2B-ae47888-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.061x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250202-vultr-x86_64-python-ae4788809d674f8e27fa-3.14.0a4%2B-ae47888-vs-3.13.0rc2.md)
- [📈time plot](bm-20250202-vultr-x86_64-python-ae4788809d674f8e27fa-3.14.0a4%2B-ae47888-vs-3.13.0rc2.svg)

