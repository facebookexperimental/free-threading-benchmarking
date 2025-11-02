# Results

- fork: python/2f60b8f02fe7cb83dd58
- version: 3.15.0a1+
- config: NOGIL
- commit hash: [2f60b8f](https://github.com/python/cpython/commit/2f60b8f)
- commit date: 2025-11-01T16:41:23Z
- commit merge base: [b1554146c29182803d1df23d6367c07a429d21ba](https://github.com/python/cpython/commit/b1554146c29182803d1df23d6367c07a429d21ba)
- commit date: 2025-11-01T16:41:23+00:00
- ref: 2f60b8f02fe7cb83dd58

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19004655593)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251101-vultr-x86_64-python-2f60b8f02fe7cb83dd58-3.15.0a1%2B-2f60b8f.json)

### vs. 3.12.6

- Geometric mean: 1.014x slower (HPT: reliability of 83.37%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251101-vultr-x86_64-python-2f60b8f02fe7cb83dd58-3.15.0a1%2B-2f60b8f-vs-3.12.6.md)
- [📈time plot](bm-20251101-vultr-x86_64-python-2f60b8f02fe7cb83dd58-3.15.0a1%2B-2f60b8f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.048x slower (HPT: reliability of 94.70%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251101-vultr-x86_64-python-2f60b8f02fe7cb83dd58-3.15.0a1%2B-2f60b8f-vs-3.13.0rc2.md)
- [📈time plot](bm-20251101-vultr-x86_64-python-2f60b8f02fe7cb83dd58-3.15.0a1%2B-2f60b8f-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.092x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20251101-vultr-x86_64-python-2f60b8f02fe7cb83dd58-3.15.0a1%2B-2f60b8f-vs-base-mem.svg)
- [📄table](bm-20251101-vultr-x86_64-python-2f60b8f02fe7cb83dd58-3.15.0a1%2B-2f60b8f-vs-base.md)
- [📈time plot](bm-20251101-vultr-x86_64-python-2f60b8f02fe7cb83dd58-3.15.0a1%2B-2f60b8f-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19004655593)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1%2B-2f60b8f.json)

### vs. 3.12.6

- Geometric mean: 1.072x faster (HPT: reliability of 92.03%, 1.00x faster at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1%2B-2f60b8f-vs-3.12.6.md)
- [📈time plot](bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1%2B-2f60b8f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.006x slower (HPT: reliability of 83.83%, 1.00x slower at 99th %ile)
- Memory usage: 1.30x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1%2B-2f60b8f-vs-3.13.0rc2.md)
- [📈time plot](bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1%2B-2f60b8f-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.042x slower (HPT: reliability of 99.99%, 1.01x slower at 99th %ile)
- Memory usage: 1.13x
- [🧠memory plot](bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1%2B-2f60b8f-vs-base-mem.svg)
- [📄table](bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1%2B-2f60b8f-vs-base.md)
- [📈time plot](bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1%2B-2f60b8f-vs-base.svg)

