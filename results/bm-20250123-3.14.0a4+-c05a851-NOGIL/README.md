# Results

- fork: python/c05a851ac59e6fb7bd43
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [c05a851](https://github.com/python/cpython/commit/c05a851)
- commit date: 2025-01-23T23:38:51+05:30
- commit merge base: [0b15d9c0d2d30c7d3f17ebb90dd822ef32f977cc](https://github.com/python/cpython/commit/0b15d9c0d2d30c7d3f17ebb90dd822ef32f977cc)
- ref: c05a851ac59e6fb7bd43

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12937349520)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250123-vultr-x86_64-python-c05a851ac59e6fb7bd43-3.14.0a4%2B-c05a851.json)

### vs. 3.12.6

- Geometric mean: 1.058x slower (HPT: reliability of 99.98%, 1.03x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250123-vultr-x86_64-python-c05a851ac59e6fb7bd43-3.14.0a4%2B-c05a851-vs-3.12.6.md)
- [📈time plot](bm-20250123-vultr-x86_64-python-c05a851ac59e6fb7bd43-3.14.0a4%2B-c05a851-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.088x slower (HPT: reliability of 99.99%, 1.05x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250123-vultr-x86_64-python-c05a851ac59e6fb7bd43-3.14.0a4%2B-c05a851-vs-3.13.0rc2.md)
- [📈time plot](bm-20250123-vultr-x86_64-python-c05a851ac59e6fb7bd43-3.14.0a4%2B-c05a851-vs-3.13.0rc2.svg)

