# Results

- fork: python/f48702dade921beed3e2
- version: 3.14.0a4+
- config: 
- commit hash: [f48702d](https://github.com/python/cpython/commit/f48702d)
- commit date: 2025-01-16T15:41:40+00:00
- commit merge base: [3893a92d956363fa2443bc5e47d4bae3deddacef](https://github.com/python/cpython/commit/3893a92d956363fa2443bc5e47d4bae3deddacef)
- ref: f48702dade921beed3e2

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12816543762)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250116-vultr-x86_64-python-f48702dade921beed3e2-3.14.0a4%2B-f48702d.json)

### vs. 3.12.6

- Geometric mean: 1.091x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250116-vultr-x86_64-python-f48702dade921beed3e2-3.14.0a4%2B-f48702d-vs-3.12.6.md)
- [📈time plot](bm-20250116-vultr-x86_64-python-f48702dade921beed3e2-3.14.0a4%2B-f48702d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.053x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250116-vultr-x86_64-python-f48702dade921beed3e2-3.14.0a4%2B-f48702d-vs-3.13.0rc2.md)
- [📈time plot](bm-20250116-vultr-x86_64-python-f48702dade921beed3e2-3.14.0a4%2B-f48702d-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.007x slower (HPT: reliability of 100.00%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250116-vultr-x86_64-python-f48702dade921beed3e2-3.14.0a4%2B-f48702d-vs-base-mem.svg)
- [📄table](bm-20250116-vultr-x86_64-python-f48702dade921beed3e2-3.14.0a4%2B-f48702d-vs-base.md)
- [📈time plot](bm-20250116-vultr-x86_64-python-f48702dade921beed3e2-3.14.0a4%2B-f48702d-vs-base.svg)

