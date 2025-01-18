# Results

- fork: python/1c13c56a34fc4c4d8969
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [1c13c56](https://github.com/python/cpython/commit/1c13c56)
- commit date: 2025-01-14T11:43:42-08:00
- commit merge base: [d906bde250d59c396d8dab92285b832c66cdec27](https://github.com/python/cpython/commit/d906bde250d59c396d8dab92285b832c66cdec27)
- ref: 1c13c56a34fc4c4d8969

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12847866224)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250114-vultr-x86_64-python-1c13c56a34fc4c4d8969-3.14.0a4%2B-1c13c56.json)

### vs. 3.12.6

- Geometric mean: 1.167x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250114-vultr-x86_64-python-1c13c56a34fc4c4d8969-3.14.0a4%2B-1c13c56-vs-3.12.6.md)
- [📈time plot](bm-20250114-vultr-x86_64-python-1c13c56a34fc4c4d8969-3.14.0a4%2B-1c13c56-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.194x slower (HPT: reliability of 100.00%, 1.13x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250114-vultr-x86_64-python-1c13c56a34fc4c4d8969-3.14.0a4%2B-1c13c56-vs-3.13.0rc2.md)
- [📈time plot](bm-20250114-vultr-x86_64-python-1c13c56a34fc4c4d8969-3.14.0a4%2B-1c13c56-vs-3.13.0rc2.svg)

