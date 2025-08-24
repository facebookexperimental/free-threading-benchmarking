# Results

- fork: python/6fcac09401e336b25833
- version: 3.15.0a0
- config: NOGIL
- commit hash: [6fcac09](https://github.com/python/cpython/commit/6fcac09)
- commit date: 2025-08-23T15:18:46Z
- commit merge base: [ab1bef8ad27ad531a1109cfc016ea627d94f9cc1](https://github.com/python/cpython/commit/ab1bef8ad27ad531a1109cfc016ea627d94f9cc1)
- commit date: 2025-08-23T15:18:46+00:00
- ref: 6fcac09401e336b25833

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17181749269)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250823-vultr-x86_64-python-6fcac09401e336b25833-3.15.0a0-6fcac09.json)

### vs. 3.12.6

- Geometric mean: 1.028x slower (HPT: reliability of 96.65%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250823-vultr-x86_64-python-6fcac09401e336b25833-3.15.0a0-6fcac09-vs-3.12.6.md)
- [📈time plot](bm-20250823-vultr-x86_64-python-6fcac09401e336b25833-3.15.0a0-6fcac09-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.060x slower (HPT: reliability of 98.76%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250823-vultr-x86_64-python-6fcac09401e336b25833-3.15.0a0-6fcac09-vs-3.13.0rc2.md)
- [📈time plot](bm-20250823-vultr-x86_64-python-6fcac09401e336b25833-3.15.0a0-6fcac09-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.099x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20250823-vultr-x86_64-python-6fcac09401e336b25833-3.15.0a0-6fcac09-vs-base-mem.svg)
- [📄table](bm-20250823-vultr-x86_64-python-6fcac09401e336b25833-3.15.0a0-6fcac09-vs-base.md)
- [📈time plot](bm-20250823-vultr-x86_64-python-6fcac09401e336b25833-3.15.0a0-6fcac09-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17181749269)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250823-macm4pro-arm64-python-6fcac09401e336b25833-3.15.0a0-6fcac09.json)

### vs. 3.12.6

- Geometric mean: 1.089x faster (HPT: reliability of 97.99%, 1.00x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250823-macm4pro-arm64-python-6fcac09401e336b25833-3.15.0a0-6fcac09-vs-3.12.6.md)
- [📈time plot](bm-20250823-macm4pro-arm64-python-6fcac09401e336b25833-3.15.0a0-6fcac09-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.010x faster (HPT: reliability of 68.66%, 1.00x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250823-macm4pro-arm64-python-6fcac09401e336b25833-3.15.0a0-6fcac09-vs-3.13.0rc2.md)
- [📈time plot](bm-20250823-macm4pro-arm64-python-6fcac09401e336b25833-3.15.0a0-6fcac09-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.027x slower (HPT: reliability of 99.61%, 1.00x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20250823-macm4pro-arm64-python-6fcac09401e336b25833-3.15.0a0-6fcac09-vs-base-mem.svg)
- [📄table](bm-20250823-macm4pro-arm64-python-6fcac09401e336b25833-3.15.0a0-6fcac09-vs-base.md)
- [📈time plot](bm-20250823-macm4pro-arm64-python-6fcac09401e336b25833-3.15.0a0-6fcac09-vs-base.svg)

