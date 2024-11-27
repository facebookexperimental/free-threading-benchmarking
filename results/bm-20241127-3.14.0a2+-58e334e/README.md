# Results

- fork: python
- version: 3.14.0a2+
- config: 
- commit hash: [58e334e](https://github.com/python/cpython/commit/58e334e)
- commit date: 2024-11-27T16:14:49+01:00
- commit merge base: [9328db7652677a23192cb51b0324a0fdbfa587c9](https://github.com/python/cpython/commit/9328db7652677a23192cb51b0324a0fdbfa587c9)
- ref: 58e334e1431b2ed6b70e

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12057185324)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2%2B-58e334e.json)

### vs. 3.12.6

- Geometric mean: 1.034x faster (HPT: reliability of 99.85%, 1.00x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2%2B-58e334e-vs-3.12.6.md)
- [📈time plot](bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2%2B-58e334e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.004x slower (HPT: reliability of 88.73%, 1.00x slower at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2%2B-58e334e-vs-3.13.0rc2.md)
- [📈time plot](bm-20241127-vultr-x86_64-python-58e334e1431b2ed6b70e-3.14.0a2%2B-58e334e-vs-3.13.0rc2.svg)

