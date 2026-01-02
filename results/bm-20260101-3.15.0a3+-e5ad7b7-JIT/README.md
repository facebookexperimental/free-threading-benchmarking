# Results

- fork: python/e5ad7b7694c47555e3ea
- version: 3.15.0a3+
- config: JIT
- commit hash: [e5ad7b7](https://github.com/python/cpython/commit/e5ad7b7)
- commit date: 2026-01-01T21:10:52Z
- commit merge base: [513ae175bb4839f121b6e6806ec172437f3dcea1](https://github.com/python/cpython/commit/513ae175bb4839f121b6e6806ec172437f3dcea1)
- commit date: 2026-01-01T21:10:52+00:00
- ref: e5ad7b7694c47555e3ea

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20648800708)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260101-vultr-x86_64-python-e5ad7b7694c47555e3ea-3.15.0a3%2B-e5ad7b7.json)

### vs. 3.12.6

- Geometric mean: 1.122x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260101-vultr-x86_64-python-e5ad7b7694c47555e3ea-3.15.0a3%2B-e5ad7b7-vs-3.12.6.md)
- [📈time plot](bm-20260101-vultr-x86_64-python-e5ad7b7694c47555e3ea-3.15.0a3%2B-e5ad7b7-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.084x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260101-vultr-x86_64-python-e5ad7b7694c47555e3ea-3.15.0a3%2B-e5ad7b7-vs-3.13.0rc2.md)
- [📈time plot](bm-20260101-vultr-x86_64-python-e5ad7b7694c47555e3ea-3.15.0a3%2B-e5ad7b7-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.039x faster (HPT: reliability of 94.47%, 1.00x faster at 99th %ile)
- Memory usage: 1.03x
- [🧠memory plot](bm-20260101-vultr-x86_64-python-e5ad7b7694c47555e3ea-3.15.0a3%2B-e5ad7b7-vs-base-mem.svg)
- [📄table](bm-20260101-vultr-x86_64-python-e5ad7b7694c47555e3ea-3.15.0a3%2B-e5ad7b7-vs-base.md)
- [📈time plot](bm-20260101-vultr-x86_64-python-e5ad7b7694c47555e3ea-3.15.0a3%2B-e5ad7b7-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20648800708)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3%2B-e5ad7b7.json)

### vs. 3.12.6

- Geometric mean: 1.255x faster (HPT: reliability of 100.00%, 1.14x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: asyncio_websockets, chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3%2B-e5ad7b7-vs-3.12.6.md)
- [📈time plot](bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3%2B-e5ad7b7-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.162x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: asyncio_websockets, chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3%2B-e5ad7b7-vs-3.13.0rc2.md)
- [📈time plot](bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3%2B-e5ad7b7-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.079x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.03x
- [🧠memory plot](bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3%2B-e5ad7b7-vs-base-mem.svg)
- [📄table](bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3%2B-e5ad7b7-vs-base.md)
- [📈time plot](bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3%2B-e5ad7b7-vs-base.svg)

