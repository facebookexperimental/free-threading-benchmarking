# Results

- fork: python/cd6abe27a2582786da7b
- version: 3.14.0a5+
- config: NOGIL
- commit hash: [cd6abe2](https://github.com/python/cpython/commit/cd6abe2)
- commit date: 2025-02-24T00:20:37+00:00
- commit merge base: [071820113f11b8f6a21f98652d0840e10268114c](https://github.com/python/cpython/commit/071820113f11b8f6a21f98652d0840e10268114c)
- ref: cd6abe27a2582786da7b

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13488381889)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250224-vultr-x86_64-python-cd6abe27a2582786da7b-3.14.0a5%2B-cd6abe2.json)

### vs. 3.12.6

- Geometric mean: 1.045x slower (HPT: reliability of 100.00%, 1.03x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250224-vultr-x86_64-python-cd6abe27a2582786da7b-3.14.0a5%2B-cd6abe2-vs-3.12.6.md)
- [📈time plot](bm-20250224-vultr-x86_64-python-cd6abe27a2582786da7b-3.14.0a5%2B-cd6abe2-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.077x slower (HPT: reliability of 99.99%, 1.05x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250224-vultr-x86_64-python-cd6abe27a2582786da7b-3.14.0a5%2B-cd6abe2-vs-3.13.0rc2.md)
- [📈time plot](bm-20250224-vultr-x86_64-python-cd6abe27a2582786da7b-3.14.0a5%2B-cd6abe2-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.123x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250224-vultr-x86_64-python-cd6abe27a2582786da7b-3.14.0a5%2B-cd6abe2-vs-base-mem.svg)
- [📄table](bm-20250224-vultr-x86_64-python-cd6abe27a2582786da7b-3.14.0a5%2B-cd6abe2-vs-base.md)
- [📈time plot](bm-20250224-vultr-x86_64-python-cd6abe27a2582786da7b-3.14.0a5%2B-cd6abe2-vs-base.svg)

