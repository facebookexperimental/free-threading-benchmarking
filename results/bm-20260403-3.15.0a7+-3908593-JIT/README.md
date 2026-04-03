# Results

- fork: python/3908593039bde9d4b591
- version: 3.15.0a7+
- config: JIT
- commit hash: [3908593](https://github.com/python/cpython/commit/3908593)
- commit date: 2026-04-03T10:47:59+02:00
- commit merge base: [f3b74d62698d5f0ee7dd905b8a7b9189e6ef9fce](https://github.com/python/cpython/commit/f3b74d62698d5f0ee7dd905b8a7b9189e6ef9fce)
- ref: 3908593039bde9d4b591

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/23949828264)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260403-vultr-x86_64-python-3908593039bde9d4b591-3.15.0a7%2B-3908593.json)

### vs. 3.12.6

- Geometric mean: 1.165x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260403-vultr-x86_64-python-3908593039bde9d4b591-3.15.0a7%2B-3908593-vs-3.12.6.md)
- [📈time plot](bm-20260403-vultr-x86_64-python-3908593039bde9d4b591-3.15.0a7%2B-3908593-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.126x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260403-vultr-x86_64-python-3908593039bde9d4b591-3.15.0a7%2B-3908593-vs-3.13.0rc2.md)
- [📈time plot](bm-20260403-vultr-x86_64-python-3908593039bde9d4b591-3.15.0a7%2B-3908593-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/23949828264)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260403-macm4pro-arm64-python-3908593039bde9d4b591-3.15.0a7%2B-3908593.json)

### vs. 3.12.6

- Geometric mean: 1.273x faster (HPT: reliability of 100.00%, 1.14x faster at 99th %ile)
- Memory usage: 1.28x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260403-macm4pro-arm64-python-3908593039bde9d4b591-3.15.0a7%2B-3908593-vs-3.12.6.md)
- [📈time plot](bm-20260403-macm4pro-arm64-python-3908593039bde9d4b591-3.15.0a7%2B-3908593-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.181x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260403-macm4pro-arm64-python-3908593039bde9d4b591-3.15.0a7%2B-3908593-vs-3.13.0rc2.md)
- [📈time plot](bm-20260403-macm4pro-arm64-python-3908593039bde9d4b591-3.15.0a7%2B-3908593-vs-3.13.0rc2.svg)

