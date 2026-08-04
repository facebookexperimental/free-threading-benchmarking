# Results

- fork: python/204febac457c39c6622c
- version: 3.16.0a0
- config: NOGIL
- commit hash: [204feba](https://github.com/python/cpython/commit/204feba)
- commit date: 2026-08-02T20:10:21+02:00
- commit merge base: [685ad027478d3c16e9843bb20ddec4711da3fcd0](https://github.com/python/cpython/commit/685ad027478d3c16e9843bb20ddec4711da3fcd0)
- ref: 204febac457c39c6622c

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/30775192849)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260802-vultr-x86_64-python-204febac457c39c6622c-3.16.0a0-204feba.json)

### vs. 3.12.6

- Geometric mean: 1.032x slower (HPT: reliability of 75.49%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260802-vultr-x86_64-python-204febac457c39c6622c-3.16.0a0-204feba-vs-3.12.6.md)
- [📈time plot](bm-20260802-vultr-x86_64-python-204febac457c39c6622c-3.16.0a0-204feba-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.064x slower (HPT: reliability of 96.25%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260802-vultr-x86_64-python-204febac457c39c6622c-3.16.0a0-204feba-vs-3.13.0rc2.md)
- [📈time plot](bm-20260802-vultr-x86_64-python-204febac457c39c6622c-3.16.0a0-204feba-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.099x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20260802-vultr-x86_64-python-204febac457c39c6622c-3.16.0a0-204feba-vs-base-mem.svg)
- [📄table](bm-20260802-vultr-x86_64-python-204febac457c39c6622c-3.16.0a0-204feba-vs-base.md)
- [📈time plot](bm-20260802-vultr-x86_64-python-204febac457c39c6622c-3.16.0a0-204feba-vs-base.svg)

