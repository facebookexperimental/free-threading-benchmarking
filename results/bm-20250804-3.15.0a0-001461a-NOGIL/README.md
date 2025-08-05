# Results

- fork: python/001461a29235216eb9c8
- version: 3.15.0a0
- config: NOGIL
- commit hash: [001461a](https://github.com/python/cpython/commit/001461a)
- commit date: 2025-08-04T23:08:26+01:00
- commit merge base: [4dae9b1ff16feae03bddb57ec3be5c42de14b1d2](https://github.com/python/cpython/commit/4dae9b1ff16feae03bddb57ec3be5c42de14b1d2)
- ref: 001461a29235216eb9c8

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16737398324)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250804-vultr-x86_64-python-001461a29235216eb9c8-3.15.0a0-001461a.json)

### vs. 3.12.6

- Geometric mean: 1.025x slower (HPT: reliability of 92.89%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250804-vultr-x86_64-python-001461a29235216eb9c8-3.15.0a0-001461a-vs-3.12.6.md)
- [📈time plot](bm-20250804-vultr-x86_64-python-001461a29235216eb9c8-3.15.0a0-001461a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.058x slower (HPT: reliability of 97.31%, 1.00x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250804-vultr-x86_64-python-001461a29235216eb9c8-3.15.0a0-001461a-vs-3.13.0rc2.md)
- [📈time plot](bm-20250804-vultr-x86_64-python-001461a29235216eb9c8-3.15.0a0-001461a-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.086x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20250804-vultr-x86_64-python-001461a29235216eb9c8-3.15.0a0-001461a-vs-base-mem.svg)
- [📄table](bm-20250804-vultr-x86_64-python-001461a29235216eb9c8-3.15.0a0-001461a-vs-base.md)
- [📈time plot](bm-20250804-vultr-x86_64-python-001461a29235216eb9c8-3.15.0a0-001461a-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16737398324)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250804-macm4pro-arm64-python-001461a29235216eb9c8-3.15.0a0-001461a.json)

### vs. 3.12.6

- Geometric mean: 1.094x faster (HPT: reliability of 99.16%, 1.00x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250804-macm4pro-arm64-python-001461a29235216eb9c8-3.15.0a0-001461a-vs-3.12.6.md)
- [📈time plot](bm-20250804-macm4pro-arm64-python-001461a29235216eb9c8-3.15.0a0-001461a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.015x faster (HPT: reliability of 55.61%, 1.00x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250804-macm4pro-arm64-python-001461a29235216eb9c8-3.15.0a0-001461a-vs-3.13.0rc2.md)
- [📈time plot](bm-20250804-macm4pro-arm64-python-001461a29235216eb9c8-3.15.0a0-001461a-vs-3.13.0rc2.svg)

