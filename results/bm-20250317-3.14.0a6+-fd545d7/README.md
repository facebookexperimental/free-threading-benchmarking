# Results

- fork: python/fd545d735d5f9c048f99
- version: 3.14.0a6+
- config: 
- commit hash: [fd545d7](https://github.com/python/cpython/commit/fd545d7)
- commit date: 2025-03-17T17:23:50+00:00
- commit merge base: [9881fc5483d6298dc969919dddecf2b72ddf8d43](https://github.com/python/cpython/commit/9881fc5483d6298dc969919dddecf2b72ddf8d43)
- ref: fd545d735d5f9c048f99

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13912466045)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6%2B-fd545d7.json)

### vs. 3.12.6

- Geometric mean: 1.061x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers
- [📄table](bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6%2B-fd545d7-vs-3.12.6.md)
- [📈time plot](bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6%2B-fd545d7-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.022x faster (HPT: reliability of 78.26%, 1.00x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers
- [📄table](bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6%2B-fd545d7-vs-3.13.0rc2.md)
- [📈time plot](bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6%2B-fd545d7-vs-3.13.0rc2.svg)

