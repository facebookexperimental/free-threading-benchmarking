# Results

- fork: python/8ba0d7bbc295781bf279
- version: 3.14.0a5+
- config: NOGIL
- commit hash: [8ba0d7b](https://github.com/python/cpython/commit/8ba0d7b)
- commit date: 2025-02-27T14:00:14+00:00
- commit merge base: [d027787c8d89f59a9f0b1d7cc6972f5e16ffc740](https://github.com/python/cpython/commit/d027787c8d89f59a9f0b1d7cc6972f5e16ffc740)
- ref: 8ba0d7bbc295781bf279

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13591203800)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250227-vultr-x86_64-python-8ba0d7bbc295781bf279-3.14.0a5%2B-8ba0d7b.json)

### vs. 3.12.6

- Geometric mean: 1.052x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250227-vultr-x86_64-python-8ba0d7bbc295781bf279-3.14.0a5%2B-8ba0d7b-vs-3.12.6.md)
- [📈time plot](bm-20250227-vultr-x86_64-python-8ba0d7bbc295781bf279-3.14.0a5%2B-8ba0d7b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.084x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250227-vultr-x86_64-python-8ba0d7bbc295781bf279-3.14.0a5%2B-8ba0d7b-vs-3.13.0rc2.md)
- [📈time plot](bm-20250227-vultr-x86_64-python-8ba0d7bbc295781bf279-3.14.0a5%2B-8ba0d7b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.008x slower (HPT: reliability of 88.85%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250227-vultr-x86_64-python-8ba0d7bbc295781bf279-3.14.0a5%2B-8ba0d7b-vs-base-mem.svg)
- [📄table](bm-20250227-vultr-x86_64-python-8ba0d7bbc295781bf279-3.14.0a5%2B-8ba0d7b-vs-base.md)
- [📈time plot](bm-20250227-vultr-x86_64-python-8ba0d7bbc295781bf279-3.14.0a5%2B-8ba0d7b-vs-base.svg)

