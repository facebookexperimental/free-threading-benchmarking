# Results

- fork: python/43c60ec2fddd316a4a6b
- version: 3.16.0a0
- config: 
- commit hash: [43c60ec](https://github.com/python/cpython/commit/43c60ec)
- commit date: 2026-05-24T16:17:38+00:00
- commit merge base: [cb72193c8c48a29c6f877863684b9f56f095c7c3](https://github.com/python/cpython/commit/cb72193c8c48a29c6f877863684b9f56f095c7c3)
- ref: 43c60ec2fddd316a4a6b

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/26377903398)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260524-vultr-x86_64-python-43c60ec2fddd316a4a6b-3.16.0a0-43c60ec.json)

### vs. 3.12.6

- Geometric mean: 1.065x faster (HPT: reliability of 99.99%, 1.03x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260524-vultr-x86_64-python-43c60ec2fddd316a4a6b-3.16.0a0-43c60ec-vs-3.12.6.md)
- [📈time plot](bm-20260524-vultr-x86_64-python-43c60ec2fddd316a4a6b-3.16.0a0-43c60ec-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.027x faster (HPT: reliability of 99.37%, 1.00x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260524-vultr-x86_64-python-43c60ec2fddd316a4a6b-3.16.0a0-43c60ec-vs-3.13.0rc2.md)
- [📈time plot](bm-20260524-vultr-x86_64-python-43c60ec2fddd316a4a6b-3.16.0a0-43c60ec-vs-3.13.0rc2.svg)

