# Results

- fork: python/b70a567575db37846bee
- version: 3.14.0a3+
- config: 
- commit hash: [b70a567](https://github.com/python/cpython/commit/b70a567)
- commit date: 2025-01-13T17:58:11+01:00
- commit merge base: [53e8942e6938df3a32b783815f1bd4b76eed3dd0](https://github.com/python/cpython/commit/53e8942e6938df3a32b783815f1bd4b76eed3dd0)
- ref: b70a567575db37846bee

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/12758478892)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-45-generic-x86_64-with-glibc2.39
- [raw results](bm-20250113-vultr-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567.json)

### vs. 3.12.6

- Geometric mean: 1.098x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250113-vultr-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-3.12.6.md)
- [📈time plot](bm-20250113-vultr-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.060x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250113-vultr-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-3.13.0rc2.md)
- [📈time plot](bm-20250113-vultr-x86_64-python-b70a567575db37846bee-3.14.0a3%2B-b70a567-vs-3.13.0rc2.svg)

