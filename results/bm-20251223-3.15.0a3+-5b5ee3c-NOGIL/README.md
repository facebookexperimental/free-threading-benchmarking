# Results

- fork: python/5b5ee3c4bf1a28b61063
- version: 3.15.0a3+
- config: NOGIL
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

- Geometric mean: 1.032x slower (HPT: reliability of 91.64%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251223-vultr-x86_64-python-5b5ee3c4bf1a28b61063-3.15.0a3%2B-5b5ee3c-vs-3.12.6.md)
- [📈time plot](bm-20251223-vultr-x86_64-python-5b5ee3c4bf1a28b61063-3.15.0a3%2B-5b5ee3c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.065x slower (HPT: reliability of 96.76%, 1.00x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251223-vultr-x86_64-python-5b5ee3c4bf1a28b61063-3.15.0a3%2B-5b5ee3c-vs-3.13.0rc2.md)
- [📈time plot](bm-20251223-vultr-x86_64-python-5b5ee3c4bf1a28b61063-3.15.0a3%2B-5b5ee3c-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.099x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20251223-vultr-x86_64-python-5b5ee3c4bf1a28b61063-3.15.0a3%2B-5b5ee3c-vs-base-mem.svg)
- [📄table](bm-20251223-vultr-x86_64-python-5b5ee3c4bf1a28b61063-3.15.0a3%2B-5b5ee3c-vs-base.md)
- [📈time plot](bm-20251223-vultr-x86_64-python-5b5ee3c4bf1a28b61063-3.15.0a3%2B-5b5ee3c-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20447728551)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251223-macm4pro-arm64-python-5b5ee3c4bf1a28b61063-3.15.0a3%2B-5b5ee3c.json)

### vs. 3.12.6

- Geometric mean: 1.092x faster (HPT: reliability of 98.69%, 1.00x faster at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251223-macm4pro-arm64-python-5b5ee3c4bf1a28b61063-3.15.0a3%2B-5b5ee3c-vs-3.12.6.md)
- [📈time plot](bm-20251223-macm4pro-arm64-python-5b5ee3c4bf1a28b61063-3.15.0a3%2B-5b5ee3c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.013x faster (HPT: reliability of 55.46%, 1.00x slower at 99th %ile)
- Memory usage: 1.30x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251223-macm4pro-arm64-python-5b5ee3c4bf1a28b61063-3.15.0a3%2B-5b5ee3c-vs-3.13.0rc2.md)
- [📈time plot](bm-20251223-macm4pro-arm64-python-5b5ee3c4bf1a28b61063-3.15.0a3%2B-5b5ee3c-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.054x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.12x
- new benchmarks: dask
- [🧠memory plot](bm-20251223-macm4pro-arm64-python-5b5ee3c4bf1a28b61063-3.15.0a3%2B-5b5ee3c-vs-base-mem.svg)
- [📄table](bm-20251223-macm4pro-arm64-python-5b5ee3c4bf1a28b61063-3.15.0a3%2B-5b5ee3c-vs-base.md)
- [📈time plot](bm-20251223-macm4pro-arm64-python-5b5ee3c4bf1a28b61063-3.15.0a3%2B-5b5ee3c-vs-base.svg)

