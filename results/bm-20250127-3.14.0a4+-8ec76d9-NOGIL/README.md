# Results

- fork: python/8ec76d90340287eb3587
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [8ec76d9](https://github.com/python/cpython/commit/8ec76d9)
- commit date: 2025-01-27T18:17:17+02:00
- commit merge base: [d8e16ef7037ac254e4799d2991c7fc3fe576c545](https://github.com/python/cpython/commit/d8e16ef7037ac254e4799d2991c7fc3fe576c545)
- ref: 8ec76d90340287eb3587

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13004409760)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250127-vultr-x86_64-python-8ec76d90340287eb3587-3.14.0a4%2B-8ec76d9.json)

### vs. 3.12.6

- Geometric mean: 1.066x slower (HPT: reliability of 99.99%, 1.04x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250127-vultr-x86_64-python-8ec76d90340287eb3587-3.14.0a4%2B-8ec76d9-vs-3.12.6.md)
- [📈time plot](bm-20250127-vultr-x86_64-python-8ec76d90340287eb3587-3.14.0a4%2B-8ec76d9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.096x slower (HPT: reliability of 99.99%, 1.05x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250127-vultr-x86_64-python-8ec76d90340287eb3587-3.14.0a4%2B-8ec76d9-vs-3.13.0rc2.md)
- [📈time plot](bm-20250127-vultr-x86_64-python-8ec76d90340287eb3587-3.14.0a4%2B-8ec76d9-vs-3.13.0rc2.svg)

