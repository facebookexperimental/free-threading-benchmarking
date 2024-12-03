# Results

- fork: python
- version: 3.14.0a2+
- config: NOGIL
- commit hash: [8ba9f5b](https://github.com/python/cpython/commit/8ba9f5b)
- commit date: 2024-12-03T18:08:39+02:00
- commit merge base: [412e11fe6e37f15971ef855f88b8b01bb3297679](https://github.com/python/cpython/commit/412e11fe6e37f15971ef855f88b8b01bb3297679)
- ref: 8ba9f5bca9c0ce6130e1

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12145110414)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241203-vultr-x86_64-python-8ba9f5bca9c0ce6130e1-3.14.0a2%2B-8ba9f5b.json)

### vs. 3.12.6

- Geometric mean: 1.257x slower (HPT: reliability of 100.00%, 1.22x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241203-vultr-x86_64-python-8ba9f5bca9c0ce6130e1-3.14.0a2%2B-8ba9f5b-vs-3.12.6.md)
- [📈time plot](bm-20241203-vultr-x86_64-python-8ba9f5bca9c0ce6130e1-3.14.0a2%2B-8ba9f5b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.282x slower (HPT: reliability of 100.00%, 1.24x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241203-vultr-x86_64-python-8ba9f5bca9c0ce6130e1-3.14.0a2%2B-8ba9f5b-vs-3.13.0rc2.md)
- [📈time plot](bm-20241203-vultr-x86_64-python-8ba9f5bca9c0ce6130e1-3.14.0a2%2B-8ba9f5b-vs-3.13.0rc2.svg)

