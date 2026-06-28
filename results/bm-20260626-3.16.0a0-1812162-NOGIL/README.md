# Results

- fork: python/1812162f81ef03461629
- version: 3.16.0a0
- config: NOGIL
- commit hash: [1812162](https://github.com/python/cpython/commit/1812162)
- commit date: 2026-06-26T18:27:47-05:00
- commit merge base: [5c3555bdc56a8e110a7d366f8ac0a93cd082e90f](https://github.com/python/cpython/commit/5c3555bdc56a8e110a7d366f8ac0a93cd082e90f)
- ref: 1812162f81ef03461629

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/28273696899)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260626-vultr-x86_64-python-1812162f81ef03461629-3.16.0a0-1812162.json)

### vs. 3.12.6

- Geometric mean: 1.035x slower (HPT: reliability of 93.08%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260626-vultr-x86_64-python-1812162f81ef03461629-3.16.0a0-1812162-vs-3.12.6.md)
- [📈time plot](bm-20260626-vultr-x86_64-python-1812162f81ef03461629-3.16.0a0-1812162-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.069x slower (HPT: reliability of 98.03%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260626-vultr-x86_64-python-1812162f81ef03461629-3.16.0a0-1812162-vs-3.13.0rc2.md)
- [📈time plot](bm-20260626-vultr-x86_64-python-1812162f81ef03461629-3.16.0a0-1812162-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.105x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20260626-vultr-x86_64-python-1812162f81ef03461629-3.16.0a0-1812162-vs-base-mem.svg)
- [📄table](bm-20260626-vultr-x86_64-python-1812162f81ef03461629-3.16.0a0-1812162-vs-base.md)
- [📈time plot](bm-20260626-vultr-x86_64-python-1812162f81ef03461629-3.16.0a0-1812162-vs-base.svg)

