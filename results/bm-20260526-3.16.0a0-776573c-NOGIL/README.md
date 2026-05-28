# Results

- fork: python/776573c9f08f70ae9cb2
- version: 3.16.0a0
- config: NOGIL
- commit hash: [776573c](https://github.com/python/cpython/commit/776573c)
- commit date: 2026-05-26T21:16:16+00:00
- commit merge base: [8ab7b43a14bed4780febbd7586a41cfe459aa6d5](https://github.com/python/cpython/commit/8ab7b43a14bed4780febbd7586a41cfe459aa6d5)
- ref: 776573c9f08f70ae9cb2

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/26484321904)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260526-vultr-x86_64-python-776573c9f08f70ae9cb2-3.16.0a0-776573c.json)

### vs. 3.12.6

- Geometric mean: 1.033x slower (HPT: reliability of 86.63%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260526-vultr-x86_64-python-776573c9f08f70ae9cb2-3.16.0a0-776573c-vs-3.12.6.md)
- [📈time plot](bm-20260526-vultr-x86_64-python-776573c9f08f70ae9cb2-3.16.0a0-776573c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.068x slower (HPT: reliability of 97.70%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260526-vultr-x86_64-python-776573c9f08f70ae9cb2-3.16.0a0-776573c-vs-3.13.0rc2.md)
- [📈time plot](bm-20260526-vultr-x86_64-python-776573c9f08f70ae9cb2-3.16.0a0-776573c-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.098x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20260526-vultr-x86_64-python-776573c9f08f70ae9cb2-3.16.0a0-776573c-vs-base-mem.svg)
- [📄table](bm-20260526-vultr-x86_64-python-776573c9f08f70ae9cb2-3.16.0a0-776573c-vs-base.md)
- [📈time plot](bm-20260526-vultr-x86_64-python-776573c9f08f70ae9cb2-3.16.0a0-776573c-vs-base.svg)

