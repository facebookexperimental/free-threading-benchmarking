# Results

- fork: python/993a0c65a7b1836aa208
- version: 3.16.0a0
- config: 
- commit hash: [993a0c6](https://github.com/python/cpython/commit/993a0c6)
- commit date: 2026-07-27T06:37:20+08:00
- commit merge base: [5afbb60e0283caaf34990bbe8437111ebaae04a4](https://github.com/python/cpython/commit/5afbb60e0283caaf34990bbe8437111ebaae04a4)
- ref: 993a0c65a7b1836aa208

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/30228219476)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260727-vultr-x86_64-python-993a0c65a7b1836aa208-3.16.0a0-993a0c6.json)

### vs. 3.12.6

- Geometric mean: 1.067x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260727-vultr-x86_64-python-993a0c65a7b1836aa208-3.16.0a0-993a0c6-vs-3.12.6.md)
- [📈time plot](bm-20260727-vultr-x86_64-python-993a0c65a7b1836aa208-3.16.0a0-993a0c6-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.032x faster (HPT: reliability of 99.73%, 1.00x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260727-vultr-x86_64-python-993a0c65a7b1836aa208-3.16.0a0-993a0c6-vs-3.13.0rc2.md)
- [📈time plot](bm-20260727-vultr-x86_64-python-993a0c65a7b1836aa208-3.16.0a0-993a0c6-vs-3.13.0rc2.svg)

