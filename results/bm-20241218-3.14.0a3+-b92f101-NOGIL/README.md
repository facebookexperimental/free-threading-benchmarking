# Results

- fork: python/b92f101d0f19a1df3205
- version: 3.14.0a3+
- config: NOGIL
- commit hash: [b92f101](https://github.com/python/cpython/commit/b92f101)
- commit date: 2024-12-18T07:17:09+08:00
- commit merge base: [be8ae086874cac42eea104c1ff21ef5868d50bdd](https://github.com/python/cpython/commit/be8ae086874cac42eea104c1ff21ef5868d50bdd)
- ref: b92f101d0f19a1df3205

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12383866791)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20241218-vultr-x86_64-python-b92f101d0f19a1df3205-3.14.0a3%2B-b92f101.json)

### vs. 3.12.6

- Geometric mean: 1.214x slower (HPT: reliability of 100.00%, 1.16x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20241218-vultr-x86_64-python-b92f101d0f19a1df3205-3.14.0a3%2B-b92f101-vs-3.12.6.md)
- [📈time plot](bm-20241218-vultr-x86_64-python-b92f101d0f19a1df3205-3.14.0a3%2B-b92f101-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.240x slower (HPT: reliability of 100.00%, 1.18x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20241218-vultr-x86_64-python-b92f101d0f19a1df3205-3.14.0a3%2B-b92f101-vs-3.13.0rc2.md)
- [📈time plot](bm-20241218-vultr-x86_64-python-b92f101d0f19a1df3205-3.14.0a3%2B-b92f101-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.269x slower (HPT: reliability of 100.00%, 1.28x slower at 99th %ile)
- Memory usage: 1.19x
- new benchmarks: html5lib
- [🧠memory plot](bm-20241218-vultr-x86_64-python-b92f101d0f19a1df3205-3.14.0a3%2B-b92f101-vs-base-mem.svg)
- [📄table](bm-20241218-vultr-x86_64-python-b92f101d0f19a1df3205-3.14.0a3%2B-b92f101-vs-base.md)
- [📈time plot](bm-20241218-vultr-x86_64-python-b92f101d0f19a1df3205-3.14.0a3%2B-b92f101-vs-base.svg)

