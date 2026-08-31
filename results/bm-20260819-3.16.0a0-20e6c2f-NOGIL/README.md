# Results

- fork: python/20e6c2fc7c174342214d
- version: 3.16.0a0
- config: NOGIL
- commit hash: [20e6c2f](https://github.com/python/cpython/commit/20e6c2f)
- commit date: 2026-08-19T10:44:02+01:00
- commit merge base: [97688346ada2df3e5b9c279348862c3d64ab0823](https://github.com/python/cpython/commit/97688346ada2df3e5b9c279348862c3d64ab0823)
- ref: 20e6c2fc7c174342214d

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/33439585676)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260819-vultr-x86_64-python-20e6c2fc7c174342214d-3.16.0a0-20e6c2f.json)

### vs. 3.12.6

- Geometric mean: 1.037x slower (HPT: reliability of 85.84%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260819-vultr-x86_64-python-20e6c2fc7c174342214d-3.16.0a0-20e6c2f-vs-3.12.6.md)
- [📈time plot](bm-20260819-vultr-x86_64-python-20e6c2fc7c174342214d-3.16.0a0-20e6c2f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.069x slower (HPT: reliability of 96.29%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260819-vultr-x86_64-python-20e6c2fc7c174342214d-3.16.0a0-20e6c2f-vs-3.13.0rc2.md)
- [📈time plot](bm-20260819-vultr-x86_64-python-20e6c2fc7c174342214d-3.16.0a0-20e6c2f-vs-3.13.0rc2.svg)

