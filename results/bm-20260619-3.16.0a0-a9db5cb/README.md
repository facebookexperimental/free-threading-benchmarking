# Results

- fork: python/a9db5cb52fefffc8fcdd
- version: 3.16.0a0
- config: 
- commit hash: [a9db5cb](https://github.com/python/cpython/commit/a9db5cb)
- commit date: 2026-06-19T23:39:34+00:00
- commit merge base: [66cc04855100c3865bd01adfe92a3a02dbc3a914](https://github.com/python/cpython/commit/66cc04855100c3865bd01adfe92a3a02dbc3a914)
- ref: a9db5cb52fefffc8fcdd

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/27855515455)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb.json)

### vs. 3.12.6

- Geometric mean: 1.078x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb-vs-3.12.6.md)
- [📈time plot](bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.041x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb-vs-3.13.0rc2.md)
- [📈time plot](bm-20260619-vultr-x86_64-python-a9db5cb52fefffc8fcdd-3.16.0a0-a9db5cb-vs-3.13.0rc2.svg)

