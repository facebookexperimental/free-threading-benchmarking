# Results

- fork: python/7d9a22f50923309955a2
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [7d9a22f](https://github.com/python/cpython/commit/7d9a22f)
- commit date: 2025-02-05T16:39:42+00:00
- commit merge base: [58a4357e29a15135e6fd99f320c60f8ea0472d27](https://github.com/python/cpython/commit/58a4357e29a15135e6fd99f320c60f8ea0472d27)
- ref: 7d9a22f50923309955a2

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13168056150)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250205-vultr-x86_64-python-7d9a22f50923309955a2-3.14.0a4%2B-7d9a22f.json)

### vs. 3.12.6

- Geometric mean: 1.047x slower (HPT: reliability of 99.97%, 1.03x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250205-vultr-x86_64-python-7d9a22f50923309955a2-3.14.0a4%2B-7d9a22f-vs-3.12.6.md)
- [📈time plot](bm-20250205-vultr-x86_64-python-7d9a22f50923309955a2-3.14.0a4%2B-7d9a22f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.078x slower (HPT: reliability of 99.99%, 1.05x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250205-vultr-x86_64-python-7d9a22f50923309955a2-3.14.0a4%2B-7d9a22f-vs-3.13.0rc2.md)
- [📈time plot](bm-20250205-vultr-x86_64-python-7d9a22f50923309955a2-3.14.0a4%2B-7d9a22f-vs-3.13.0rc2.svg)

