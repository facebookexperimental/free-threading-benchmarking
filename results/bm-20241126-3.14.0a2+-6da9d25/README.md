# Results

- fork: python/6da9d252ac39d5334245
- version: 3.14.0a2+
- config: 
- commit hash: [6da9d25](https://github.com/python/cpython/commit/6da9d25)
- commit date: 2024-11-26T16:39:33+00:00
- commit merge base: [987311d42e3ec838de8ff27f9f0575aa791a6bde](https://github.com/python/cpython/commit/987311d42e3ec838de8ff27f9f0575aa791a6bde)
- ref: 6da9d252ac39d5334245

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12129988631)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241126-vultr-x86_64-python-6da9d252ac39d5334245-3.14.0a2%2B-6da9d25.json)

### vs. 3.12.6

- Geometric mean: 1.040x faster (HPT: reliability of 99.97%, 1.00x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241126-vultr-x86_64-python-6da9d252ac39d5334245-3.14.0a2%2B-6da9d25-vs-3.12.6.md)
- [📈time plot](bm-20241126-vultr-x86_64-python-6da9d252ac39d5334245-3.14.0a2%2B-6da9d25-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.002x faster (HPT: reliability of 82.63%, 1.00x slower at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241126-vultr-x86_64-python-6da9d252ac39d5334245-3.14.0a2%2B-6da9d25-vs-3.13.0rc2.md)
- [📈time plot](bm-20241126-vultr-x86_64-python-6da9d252ac39d5334245-3.14.0a2%2B-6da9d25-vs-3.13.0rc2.svg)

