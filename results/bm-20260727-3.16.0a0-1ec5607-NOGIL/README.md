# Results

- fork: python/1ec56076642091c446ec
- version: 3.16.0a0
- config: NOGIL
- commit hash: [1ec5607](https://github.com/python/cpython/commit/1ec5607)
- commit date: 2026-07-27T13:45:40-07:00
- commit merge base: [0284ce81c9615432473abac709d5b261a49399ad](https://github.com/python/cpython/commit/0284ce81c9615432473abac709d5b261a49399ad)
- ref: 1ec56076642091c446ec

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/30318016631)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260727-vultr-x86_64-python-1ec56076642091c446ec-3.16.0a0-1ec5607.json)

### vs. 3.12.6

- Geometric mean: 1.035x slower (HPT: reliability of 82.61%, 1.00x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260727-vultr-x86_64-python-1ec56076642091c446ec-3.16.0a0-1ec5607-vs-3.12.6.md)
- [📈time plot](bm-20260727-vultr-x86_64-python-1ec56076642091c446ec-3.16.0a0-1ec5607-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.067x slower (HPT: reliability of 97.50%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260727-vultr-x86_64-python-1ec56076642091c446ec-3.16.0a0-1ec5607-vs-3.13.0rc2.md)
- [📈time plot](bm-20260727-vultr-x86_64-python-1ec56076642091c446ec-3.16.0a0-1ec5607-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.100x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20260727-vultr-x86_64-python-1ec56076642091c446ec-3.16.0a0-1ec5607-vs-base-mem.svg)
- [📄table](bm-20260727-vultr-x86_64-python-1ec56076642091c446ec-3.16.0a0-1ec5607-vs-base.md)
- [📈time plot](bm-20260727-vultr-x86_64-python-1ec56076642091c446ec-3.16.0a0-1ec5607-vs-base.svg)

