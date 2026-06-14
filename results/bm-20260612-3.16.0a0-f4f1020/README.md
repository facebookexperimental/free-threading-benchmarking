# Results

- fork: python/f4f102027a9b0edc72a0
- version: 3.16.0a0
- config: 
- commit hash: [f4f1020](https://github.com/python/cpython/commit/f4f1020)
- commit date: 2026-06-12T16:02:33+00:00
- commit merge base: [d986124d83465190987357f987ee24bd7a817cac](https://github.com/python/cpython/commit/d986124d83465190987357f987ee24bd7a817cac)
- ref: f4f102027a9b0edc72a0

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/27451971125)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260612-vultr-x86_64-python-f4f102027a9b0edc72a0-3.16.0a0-f4f1020.json)

### vs. 3.12.6

- Geometric mean: 1.073x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260612-vultr-x86_64-python-f4f102027a9b0edc72a0-3.16.0a0-f4f1020-vs-3.12.6.md)
- [📈time plot](bm-20260612-vultr-x86_64-python-f4f102027a9b0edc72a0-3.16.0a0-f4f1020-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.033x faster (HPT: reliability of 99.94%, 1.01x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260612-vultr-x86_64-python-f4f102027a9b0edc72a0-3.16.0a0-f4f1020-vs-3.13.0rc2.md)
- [📈time plot](bm-20260612-vultr-x86_64-python-f4f102027a9b0edc72a0-3.16.0a0-f4f1020-vs-3.13.0rc2.svg)

