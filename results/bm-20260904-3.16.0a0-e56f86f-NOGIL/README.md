# Results

- fork: python/e56f86fb6cc7cf14c255
- version: 3.16.0a0
- config: NOGIL
- commit hash: [e56f86f](https://github.com/python/cpython/commit/e56f86f)
- commit date: 2026-09-04T17:15:44Z
- commit merge base: [3a7a22b5b0cf292ab9e7d046980085c227f7fdaa](https://github.com/python/cpython/commit/3a7a22b5b0cf292ab9e7d046980085c227f7fdaa)
- commit date: 2026-09-04T17:15:44+00:00
- ref: e56f86fb6cc7cf14c255

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/33933704173)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260904-vultr-x86_64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f.json)

### vs. 3.12.6

- Geometric mean: 1.047x slower (HPT: reliability of 89.84%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260904-vultr-x86_64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f-vs-3.12.6.md)
- [📈time plot](bm-20260904-vultr-x86_64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.079x slower (HPT: reliability of 99.09%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260904-vultr-x86_64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f-vs-3.13.0rc2.md)
- [📈time plot](bm-20260904-vultr-x86_64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.109x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20260904-vultr-x86_64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f-vs-base-mem.svg)
- [📄table](bm-20260904-vultr-x86_64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f-vs-base.md)
- [📈time plot](bm-20260904-vultr-x86_64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/33933704173)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260904-macm4pro-arm64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f.json)

### vs. 3.12.6

- Geometric mean: 1.056x faster (HPT: reliability of 87.63%, 1.00x faster at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260904-macm4pro-arm64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f-vs-3.12.6.md)
- [📈time plot](bm-20260904-macm4pro-arm64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.022x slower (HPT: reliability of 95.52%, 1.00x slower at 99th %ile)
- Memory usage: 1.29x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260904-macm4pro-arm64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f-vs-3.13.0rc2.md)
- [📈time plot](bm-20260904-macm4pro-arm64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.077x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.12x
- new benchmarks: coverage
- [🧠memory plot](bm-20260904-macm4pro-arm64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f-vs-base-mem.svg)
- [📄table](bm-20260904-macm4pro-arm64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f-vs-base.md)
- [📈time plot](bm-20260904-macm4pro-arm64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f-vs-base.svg)

