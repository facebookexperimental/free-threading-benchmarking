# Results

- fork: python/327a257e6ae4ad0e3b6e
- version: 3.14.0a4+
- config: 
- commit hash: [327a257](https://github.com/python/cpython/commit/327a257)
- commit date: 2025-01-23T01:18:26+01:00
- commit merge base: [719c9dd72f43d81072999f0ded8209c07de7fbd0](https://github.com/python/cpython/commit/719c9dd72f43d81072999f0ded8209c07de7fbd0)
- ref: 327a257e6ae4ad0e3b6e

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12919607130)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250123-vultr-x86_64-python-327a257e6ae4ad0e3b6e-3.14.0a4%2B-327a257.json)

### vs. 3.12.6

- Geometric mean: 1.085x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250123-vultr-x86_64-python-327a257e6ae4ad0e3b6e-3.14.0a4%2B-327a257-vs-3.12.6.md)
- [📈time plot](bm-20250123-vultr-x86_64-python-327a257e6ae4ad0e3b6e-3.14.0a4%2B-327a257-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.046x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250123-vultr-x86_64-python-327a257e6ae4ad0e3b6e-3.14.0a4%2B-327a257-vs-3.13.0rc2.md)
- [📈time plot](bm-20250123-vultr-x86_64-python-327a257e6ae4ad0e3b6e-3.14.0a4%2B-327a257-vs-3.13.0rc2.svg)

