# Results

- fork: python/b74fb8e220a50a958032
- version: 3.15.0a0
- config: NOGIL
- commit hash: [b74fb8e](https://github.com/python/cpython/commit/b74fb8e)
- commit date: 2025-07-13T23:27:48+03:00
- commit merge base: [283b05052338dd735cd4927011afc3735d9c6c7c](https://github.com/python/cpython/commit/283b05052338dd735cd4927011afc3735d9c6c7c)
- ref: b74fb8e220a50a958032

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16255162891)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250713-vultr-x86_64-python-b74fb8e220a50a958032-3.15.0a0-b74fb8e.json)

### vs. 3.12.6

- Geometric mean: 1.022x slower (HPT: reliability of 91.79%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250713-vultr-x86_64-python-b74fb8e220a50a958032-3.15.0a0-b74fb8e-vs-3.12.6.md)
- [📈time plot](bm-20250713-vultr-x86_64-python-b74fb8e220a50a958032-3.15.0a0-b74fb8e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.055x slower (HPT: reliability of 96.12%, 1.00x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250713-vultr-x86_64-python-b74fb8e220a50a958032-3.15.0a0-b74fb8e-vs-3.13.0rc2.md)
- [📈time plot](bm-20250713-vultr-x86_64-python-b74fb8e220a50a958032-3.15.0a0-b74fb8e-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.094x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20250713-vultr-x86_64-python-b74fb8e220a50a958032-3.15.0a0-b74fb8e-vs-base-mem.svg)
- [📄table](bm-20250713-vultr-x86_64-python-b74fb8e220a50a958032-3.15.0a0-b74fb8e-vs-base.md)
- [📈time plot](bm-20250713-vultr-x86_64-python-b74fb8e220a50a958032-3.15.0a0-b74fb8e-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16255162891)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250713-macm4pro-arm64-python-b74fb8e220a50a958032-3.15.0a0-b74fb8e.json)

### vs. 3.12.6

- Geometric mean: 1.099x faster (HPT: reliability of 98.48%, 1.00x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250713-macm4pro-arm64-python-b74fb8e220a50a958032-3.15.0a0-b74fb8e-vs-3.12.6.md)
- [📈time plot](bm-20250713-macm4pro-arm64-python-b74fb8e220a50a958032-3.15.0a0-b74fb8e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.019x faster (HPT: reliability of 68.26%, 1.00x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250713-macm4pro-arm64-python-b74fb8e220a50a958032-3.15.0a0-b74fb8e-vs-3.13.0rc2.md)
- [📈time plot](bm-20250713-macm4pro-arm64-python-b74fb8e220a50a958032-3.15.0a0-b74fb8e-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.001x faster (HPT: reliability of 96.01%, 1.00x slower at 99th %ile)
- Memory usage: 1.11x
- [🧠memory plot](bm-20250713-macm4pro-arm64-python-b74fb8e220a50a958032-3.15.0a0-b74fb8e-vs-base-mem.svg)
- [📄table](bm-20250713-macm4pro-arm64-python-b74fb8e220a50a958032-3.15.0a0-b74fb8e-vs-base.md)
- [📈time plot](bm-20250713-macm4pro-arm64-python-b74fb8e220a50a958032-3.15.0a0-b74fb8e-vs-base.svg)

