# Results

- fork: python/ec7fad79d24e79961b86
- version: 3.15.0a0
- config: NOGIL
- commit hash: [ec7fad7](https://github.com/python/cpython/commit/ec7fad7)
- commit date: 2025-07-23T11:50:15-07:00
- commit merge base: [a10235ea672d0cfae2949beca0478b7c3b2eafb0](https://github.com/python/cpython/commit/a10235ea672d0cfae2949beca0478b7c3b2eafb0)
- ref: ec7fad79d24e79961b86

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16484806817)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250723-vultr-x86_64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7.json)

### vs. 3.12.6

- Geometric mean: 1.028x slower (HPT: reliability of 95.43%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250723-vultr-x86_64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7-vs-3.12.6.md)
- [📈time plot](bm-20250723-vultr-x86_64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.060x slower (HPT: reliability of 97.85%, 1.00x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250723-vultr-x86_64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7-vs-3.13.0rc2.md)
- [📈time plot](bm-20250723-vultr-x86_64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.098x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20250723-vultr-x86_64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7-vs-base-mem.svg)
- [📄table](bm-20250723-vultr-x86_64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7-vs-base.md)
- [📈time plot](bm-20250723-vultr-x86_64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16484806817)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7.json)

### vs. 3.12.6

- Geometric mean: 1.090x faster (HPT: reliability of 97.65%, 1.00x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7-vs-3.12.6.md)
- [📈time plot](bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.011x faster (HPT: reliability of 65.16%, 1.00x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7-vs-3.13.0rc2.md)
- [📈time plot](bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.001x slower (HPT: reliability of 89.74%, 1.00x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7-vs-base-mem.svg)
- [📄table](bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7-vs-base.md)
- [📈time plot](bm-20250723-macm4pro-arm64-python-ec7fad79d24e79961b86-3.15.0a0-ec7fad7-vs-base.svg)

