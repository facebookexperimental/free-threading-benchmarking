# Results

- fork: python/6e4f64109b0eb6c9f1b5
- version: 3.14.0a4+
- config: 
- commit hash: [6e4f641](https://github.com/python/cpython/commit/6e4f641)
- commit date: 2025-01-15T10:49:02+09:00
- commit merge base: [bd3baa8b1a7755f17b2fc98c7fb7b872fec43af3](https://github.com/python/cpython/commit/bd3baa8b1a7755f17b2fc98c7fb7b872fec43af3)
- ref: 6e4f64109b0eb6c9f1b5

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12782396272)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250115-vultr-x86_64-python-6e4f64109b0eb6c9f1b5-3.14.0a4%2B-6e4f641.json)

### vs. 3.12.6

- Geometric mean: 1.110x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250115-vultr-x86_64-python-6e4f64109b0eb6c9f1b5-3.14.0a4%2B-6e4f641-vs-3.12.6.md)
- [📈time plot](bm-20250115-vultr-x86_64-python-6e4f64109b0eb6c9f1b5-3.14.0a4%2B-6e4f641-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.071x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250115-vultr-x86_64-python-6e4f64109b0eb6c9f1b5-3.14.0a4%2B-6e4f641-vs-3.13.0rc2.md)
- [📈time plot](bm-20250115-vultr-x86_64-python-6e4f64109b0eb6c9f1b5-3.14.0a4%2B-6e4f641-vs-3.13.0rc2.svg)

