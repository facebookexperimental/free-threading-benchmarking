# Results

- fork: python/4ca9fc08f89bf7172d41
- version: 3.14.0a4+
- config: NOGIL
- commit hash: [4ca9fc0](https://github.com/python/cpython/commit/4ca9fc0)
- commit date: 2025-01-30T18:05:32+01:00
- commit merge base: [4e47e05045b7b05c7e166bda2afd60191314e326](https://github.com/python/cpython/commit/4e47e05045b7b05c7e166bda2afd60191314e326)
- ref: 4ca9fc08f89bf7172d41

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13066803451)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250130-vultr-x86_64-python-4ca9fc08f89bf7172d41-3.14.0a4%2B-4ca9fc0.json)

### vs. 3.12.6

- Geometric mean: 1.048x slower (HPT: reliability of 99.98%, 1.03x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250130-vultr-x86_64-python-4ca9fc08f89bf7172d41-3.14.0a4%2B-4ca9fc0-vs-3.12.6.md)
- [📈time plot](bm-20250130-vultr-x86_64-python-4ca9fc08f89bf7172d41-3.14.0a4%2B-4ca9fc0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.079x slower (HPT: reliability of 99.99%, 1.04x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250130-vultr-x86_64-python-4ca9fc08f89bf7172d41-3.14.0a4%2B-4ca9fc0-vs-3.13.0rc2.md)
- [📈time plot](bm-20250130-vultr-x86_64-python-4ca9fc08f89bf7172d41-3.14.0a4%2B-4ca9fc0-vs-3.13.0rc2.svg)

