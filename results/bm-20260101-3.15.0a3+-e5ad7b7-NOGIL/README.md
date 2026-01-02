# Results

- fork: python/e5ad7b7694c47555e3ea
- version: 3.15.0a3+
- config: NOGIL
- commit hash: [e5ad7b7](https://github.com/python/cpython/commit/e5ad7b7)
- commit date: 2026-01-01T21:10:52Z
- commit merge base: [513ae175bb4839f121b6e6806ec172437f3dcea1](https://github.com/python/cpython/commit/513ae175bb4839f121b6e6806ec172437f3dcea1)
- commit date: 2026-01-01T21:10:52+00:00
- ref: e5ad7b7694c47555e3ea

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20648122245)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260101-vultr-x86_64-python-e5ad7b7694c47555e3ea-3.15.0a3%2B-e5ad7b7.json)

### vs. 3.12.6

- Geometric mean: 1.032x slower (HPT: reliability of 85.54%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260101-vultr-x86_64-python-e5ad7b7694c47555e3ea-3.15.0a3%2B-e5ad7b7-vs-3.12.6.md)
- [📈time plot](bm-20260101-vultr-x86_64-python-e5ad7b7694c47555e3ea-3.15.0a3%2B-e5ad7b7-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.065x slower (HPT: reliability of 94.33%, 1.00x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260101-vultr-x86_64-python-e5ad7b7694c47555e3ea-3.15.0a3%2B-e5ad7b7-vs-3.13.0rc2.md)
- [📈time plot](bm-20260101-vultr-x86_64-python-e5ad7b7694c47555e3ea-3.15.0a3%2B-e5ad7b7-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.102x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20260101-vultr-x86_64-python-e5ad7b7694c47555e3ea-3.15.0a3%2B-e5ad7b7-vs-base-mem.svg)
- [📄table](bm-20260101-vultr-x86_64-python-e5ad7b7694c47555e3ea-3.15.0a3%2B-e5ad7b7-vs-base.md)
- [📈time plot](bm-20260101-vultr-x86_64-python-e5ad7b7694c47555e3ea-3.15.0a3%2B-e5ad7b7-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20648122245)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3%2B-e5ad7b7.json)

### vs. 3.12.6

- Geometric mean: 1.084x faster (HPT: reliability of 95.20%, 1.00x faster at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3%2B-e5ad7b7-vs-3.12.6.md)
- [📈time plot](bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3%2B-e5ad7b7-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.005x faster (HPT: reliability of 73.50%, 1.00x slower at 99th %ile)
- Memory usage: 1.29x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3%2B-e5ad7b7-vs-3.13.0rc2.md)
- [📈time plot](bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3%2B-e5ad7b7-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.066x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.10x
- new benchmarks: asyncio_websockets
- [🧠memory plot](bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3%2B-e5ad7b7-vs-base-mem.svg)
- [📄table](bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3%2B-e5ad7b7-vs-base.md)
- [📈time plot](bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3%2B-e5ad7b7-vs-base.svg)

