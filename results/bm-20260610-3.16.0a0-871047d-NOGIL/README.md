# Results

- fork: python/871047dbb82ab9a89f36
- version: 3.16.0a0
- config: NOGIL
- commit hash: [871047d](https://github.com/python/cpython/commit/871047d)
- commit date: 2026-06-10T13:43:09-07:00
- commit merge base: [e60c42dc3f5a8dd9b10bc9a8a028ef2765469650](https://github.com/python/cpython/commit/e60c42dc3f5a8dd9b10bc9a8a028ef2765469650)
- ref: 871047dbb82ab9a89f36

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/27316847266)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260610-vultr-x86_64-python-871047dbb82ab9a89f36-3.16.0a0-871047d.json)

### vs. 3.12.6

- Geometric mean: 1.040x slower (HPT: reliability of 90.03%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260610-vultr-x86_64-python-871047dbb82ab9a89f36-3.16.0a0-871047d-vs-3.12.6.md)
- [📈time plot](bm-20260610-vultr-x86_64-python-871047dbb82ab9a89f36-3.16.0a0-871047d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.076x slower (HPT: reliability of 99.66%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260610-vultr-x86_64-python-871047dbb82ab9a89f36-3.16.0a0-871047d-vs-3.13.0rc2.md)
- [📈time plot](bm-20260610-vultr-x86_64-python-871047dbb82ab9a89f36-3.16.0a0-871047d-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.103x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20260610-vultr-x86_64-python-871047dbb82ab9a89f36-3.16.0a0-871047d-vs-base-mem.svg)
- [📄table](bm-20260610-vultr-x86_64-python-871047dbb82ab9a89f36-3.16.0a0-871047d-vs-base.md)
- [📈time plot](bm-20260610-vultr-x86_64-python-871047dbb82ab9a89f36-3.16.0a0-871047d-vs-base.svg)

