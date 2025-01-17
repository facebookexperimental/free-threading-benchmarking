# Results

- fork: python/3efe28a40b136164f0d3
- version: 3.14.0a3+
- config: NOGIL
- commit hash: [3efe28a](https://github.com/python/cpython/commit/3efe28a)
- commit date: 2025-01-13T15:36:55+00:00
- commit merge base: [75214f87f1ddd1d7b9a5b663a9c688b1bd41c098](https://github.com/python/cpython/commit/75214f87f1ddd1d7b9a5b663a9c688b1bd41c098)
- ref: 3efe28a40b136164f0d3

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12818478183)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250113-vultr-x86_64-python-3efe28a40b136164f0d3-3.14.0a3%2B-3efe28a.json)

### vs. 3.12.6

- Geometric mean: 1.167x slower (HPT: reliability of 100.00%, 1.13x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250113-vultr-x86_64-python-3efe28a40b136164f0d3-3.14.0a3%2B-3efe28a-vs-3.12.6.md)
- [📈time plot](bm-20250113-vultr-x86_64-python-3efe28a40b136164f0d3-3.14.0a3%2B-3efe28a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.195x slower (HPT: reliability of 100.00%, 1.14x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250113-vultr-x86_64-python-3efe28a40b136164f0d3-3.14.0a3%2B-3efe28a-vs-3.13.0rc2.md)
- [📈time plot](bm-20250113-vultr-x86_64-python-3efe28a40b136164f0d3-3.14.0a3%2B-3efe28a-vs-3.13.0rc2.svg)

