# Results

- fork: python/c5abded09995f208b21e
- version: 3.14.0a5+
- config: NOGIL
- commit hash: [c5abded](https://github.com/python/cpython/commit/c5abded)
- commit date: 2025-03-13T12:31:49-04:00
- commit merge base: [3a91ee97245639c7c4f8852418157d3fc0ec1a82](https://github.com/python/cpython/commit/3a91ee97245639c7c4f8852418157d3fc0ec1a82)
- ref: c5abded09995f208b21e

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13843963224)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250313-vultr-x86_64-python-c5abded09995f208b21e-3.14.0a5%2B-c5abded.json)

### vs. 3.12.6

- Geometric mean: 1.048x slower (HPT: reliability of 100.00%, 1.03x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250313-vultr-x86_64-python-c5abded09995f208b21e-3.14.0a5%2B-c5abded-vs-3.12.6.md)
- [📈time plot](bm-20250313-vultr-x86_64-python-c5abded09995f208b21e-3.14.0a5%2B-c5abded-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.080x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250313-vultr-x86_64-python-c5abded09995f208b21e-3.14.0a5%2B-c5abded-vs-3.13.0rc2.md)
- [📈time plot](bm-20250313-vultr-x86_64-python-c5abded09995f208b21e-3.14.0a5%2B-c5abded-vs-3.13.0rc2.svg)

