# Results

- fork: python/d05140f9f77d7dfc753d
- version: 3.14.0a4+
- config: 
- commit hash: [d05140f](https://github.com/python/cpython/commit/d05140f)
- commit date: 2025-01-15T21:13:59+00:00
- commit merge base: [5eee2fe2b05c1a2836184e047fbd4176945cbf10](https://github.com/python/cpython/commit/5eee2fe2b05c1a2836184e047fbd4176945cbf10)
- ref: d05140f9f77d7dfc753d

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12797514494)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4%2B-d05140f.json)

### vs. 3.12.6

- Geometric mean: 1.083x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4%2B-d05140f-vs-3.12.6.md)
- [📈time plot](bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4%2B-d05140f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.045x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4%2B-d05140f-vs-3.13.0rc2.md)
- [📈time plot](bm-20250115-vultr-x86_64-python-d05140f9f77d7dfc753d-3.14.0a4%2B-d05140f-vs-3.13.0rc2.svg)

