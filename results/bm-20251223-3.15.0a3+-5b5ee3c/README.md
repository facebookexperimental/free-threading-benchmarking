# Results

- fork: python/5b5ee3c4bf1a28b61063
- version: 3.15.0a3+
- config: 
- commit hash: [5b5ee3c](https://github.com/python/cpython/commit/5b5ee3c)
- commit date: 2025-12-23T00:28:08Z
- commit merge base: [9e513012341607458196f64a78b8ef80819cae2a](https://github.com/python/cpython/commit/9e513012341607458196f64a78b8ef80819cae2a)
- commit date: 2025-12-23T00:28:08+00:00
- ref: 5b5ee3c4bf1a28b61063

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20447728551)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20251223-vultr-x86_64-python-5b5ee3c4bf1a28b61063-3.15.0a3%2B-5b5ee3c.json)

### vs. 3.12.6

- Geometric mean: 1.067x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251223-vultr-x86_64-python-5b5ee3c4bf1a28b61063-3.15.0a3%2B-5b5ee3c-vs-3.12.6.md)
- [📈time plot](bm-20251223-vultr-x86_64-python-5b5ee3c4bf1a28b61063-3.15.0a3%2B-5b5ee3c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.032x faster (HPT: reliability of 99.94%, 1.01x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251223-vultr-x86_64-python-5b5ee3c4bf1a28b61063-3.15.0a3%2B-5b5ee3c-vs-3.13.0rc2.md)
- [📈time plot](bm-20251223-vultr-x86_64-python-5b5ee3c4bf1a28b61063-3.15.0a3%2B-5b5ee3c-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20447728551)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251223-macm4pro-arm64-python-5b5ee3c4bf1a28b61063-3.15.0a3%2B-5b5ee3c.json)

### vs. 3.12.6

- Geometric mean: 1.154x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251223-macm4pro-arm64-python-5b5ee3c4bf1a28b61063-3.15.0a3%2B-5b5ee3c-vs-3.12.6.md)
- [📈time plot](bm-20251223-macm4pro-arm64-python-5b5ee3c4bf1a28b61063-3.15.0a3%2B-5b5ee3c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.070x faster (HPT: reliability of 99.96%, 1.01x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251223-macm4pro-arm64-python-5b5ee3c4bf1a28b61063-3.15.0a3%2B-5b5ee3c-vs-3.13.0rc2.md)
- [📈time plot](bm-20251223-macm4pro-arm64-python-5b5ee3c4bf1a28b61063-3.15.0a3%2B-5b5ee3c-vs-3.13.0rc2.svg)

