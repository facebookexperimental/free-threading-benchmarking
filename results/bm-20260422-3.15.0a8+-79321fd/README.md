# Results

- fork: python/79321fdce3227cf09bb8
- version: 3.15.0a8+
- config: 
- commit hash: [79321fd](https://github.com/python/cpython/commit/79321fd)
- commit date: 2026-04-22T17:56:14-05:00
- commit merge base: [76b3923d688c0efc580658476c5f525ec8735104](https://github.com/python/cpython/commit/76b3923d688c0efc580658476c5f525ec8735104)
- ref: 79321fdce3227cf09bb8

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/24810463156)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260422-vultr-x86_64-python-79321fdce3227cf09bb8-3.15.0a8%2B-79321fd.json)

### vs. 3.12.6

- Geometric mean: 1.080x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260422-vultr-x86_64-python-79321fdce3227cf09bb8-3.15.0a8%2B-79321fd-vs-3.12.6.md)
- [📈time plot](bm-20260422-vultr-x86_64-python-79321fdce3227cf09bb8-3.15.0a8%2B-79321fd-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.044x faster (HPT: reliability of 99.97%, 1.01x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260422-vultr-x86_64-python-79321fdce3227cf09bb8-3.15.0a8%2B-79321fd-vs-3.13.0rc2.md)
- [📈time plot](bm-20260422-vultr-x86_64-python-79321fdce3227cf09bb8-3.15.0a8%2B-79321fd-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/24810463156)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8%2B-79321fd.json)

### vs. 3.12.6

- Geometric mean: 1.177x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.24x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8%2B-79321fd-vs-3.12.6.md)
- [📈time plot](bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8%2B-79321fd-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.092x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8%2B-79321fd-vs-3.13.0rc2.md)
- [📈time plot](bm-20260422-macm4pro-arm64-python-79321fdce3227cf09bb8-3.15.0a8%2B-79321fd-vs-3.13.0rc2.svg)

