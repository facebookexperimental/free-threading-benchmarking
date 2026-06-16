# Results

- fork: python/d63c9940f0bcc5497c42
- version: 3.16.0a0
- config: NOGIL
- commit hash: [d63c994](https://github.com/python/cpython/commit/d63c994)
- commit date: 2026-06-14T19:17:45+00:00
- commit merge base: [a7007322c2a70b01e7c2a9e6b3f8f222d241c7d7](https://github.com/python/cpython/commit/a7007322c2a70b01e7c2a9e6b3f8f222d241c7d7)
- ref: d63c9940f0bcc5497c42

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/27518262030)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260614-vultr-x86_64-python-d63c9940f0bcc5497c42-3.16.0a0-d63c994.json)

### vs. 3.12.6

- Geometric mean: 1.031x slower (HPT: reliability of 84.47%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260614-vultr-x86_64-python-d63c9940f0bcc5497c42-3.16.0a0-d63c994-vs-3.12.6.md)
- [📈time plot](bm-20260614-vultr-x86_64-python-d63c9940f0bcc5497c42-3.16.0a0-d63c994-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.067x slower (HPT: reliability of 97.53%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260614-vultr-x86_64-python-d63c9940f0bcc5497c42-3.16.0a0-d63c994-vs-3.13.0rc2.md)
- [📈time plot](bm-20260614-vultr-x86_64-python-d63c9940f0bcc5497c42-3.16.0a0-d63c994-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.098x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20260614-vultr-x86_64-python-d63c9940f0bcc5497c42-3.16.0a0-d63c994-vs-base-mem.svg)
- [📄table](bm-20260614-vultr-x86_64-python-d63c9940f0bcc5497c42-3.16.0a0-d63c994-vs-base.md)
- [📈time plot](bm-20260614-vultr-x86_64-python-d63c9940f0bcc5497c42-3.16.0a0-d63c994-vs-base.svg)

