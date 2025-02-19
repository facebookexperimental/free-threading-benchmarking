# Results

- fork: python/bcc9a5dddb777c8195b5
- version: 3.14.0a5+
- config: NOGIL
- commit hash: [bcc9a5d](https://github.com/python/cpython/commit/bcc9a5d)
- commit date: 2025-02-18T21:43:19+00:00
- commit merge base: [51d4bf1e0e5349090da72721c865b6c2b28277f3](https://github.com/python/cpython/commit/51d4bf1e0e5349090da72721c865b6c2b28277f3)
- ref: bcc9a5dddb777c8195b5

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13400781040)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250218-vultr-x86_64-python-bcc9a5dddb777c8195b5-3.14.0a5%2B-bcc9a5d.json)

### vs. 3.12.6

- Geometric mean: 1.046x slower (HPT: reliability of 99.98%, 1.03x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250218-vultr-x86_64-python-bcc9a5dddb777c8195b5-3.14.0a5%2B-bcc9a5d-vs-3.12.6.md)
- [📈time plot](bm-20250218-vultr-x86_64-python-bcc9a5dddb777c8195b5-3.14.0a5%2B-bcc9a5d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.078x slower (HPT: reliability of 99.99%, 1.05x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250218-vultr-x86_64-python-bcc9a5dddb777c8195b5-3.14.0a5%2B-bcc9a5d-vs-3.13.0rc2.md)
- [📈time plot](bm-20250218-vultr-x86_64-python-bcc9a5dddb777c8195b5-3.14.0a5%2B-bcc9a5d-vs-3.13.0rc2.svg)

