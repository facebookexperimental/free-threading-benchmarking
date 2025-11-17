# Results

- fork: python/8be3b2f479431f670f2e
- version: 3.15.0a1+
- config: 
- commit hash: [8be3b2f](https://github.com/python/cpython/commit/8be3b2f)
- commit date: 2025-11-16T13:57:07-08:00
- commit merge base: [be699d6c7c8793d3eb464f2e5d3f10262fe3bc37](https://github.com/python/cpython/commit/be699d6c7c8793d3eb464f2e5d3f10262fe3bc37)
- ref: 8be3b2f479431f670f2e

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19414565246)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251116-vultr-x86_64-python-8be3b2f479431f670f2e-3.15.0a1%2B-8be3b2f.json)

### vs. 3.12.6

- Geometric mean: 1.076x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251116-vultr-x86_64-python-8be3b2f479431f670f2e-3.15.0a1%2B-8be3b2f-vs-3.12.6.md)
- [📈time plot](bm-20251116-vultr-x86_64-python-8be3b2f479431f670f2e-3.15.0a1%2B-8be3b2f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.040x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251116-vultr-x86_64-python-8be3b2f479431f670f2e-3.15.0a1%2B-8be3b2f-vs-3.13.0rc2.md)
- [📈time plot](bm-20251116-vultr-x86_64-python-8be3b2f479431f670f2e-3.15.0a1%2B-8be3b2f-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19414565246)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251116-macm4pro-arm64-python-8be3b2f479431f670f2e-3.15.0a1%2B-8be3b2f.json)

### vs. 3.12.6

- Geometric mean: 1.149x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251116-macm4pro-arm64-python-8be3b2f479431f670f2e-3.15.0a1%2B-8be3b2f-vs-3.12.6.md)
- [📈time plot](bm-20251116-macm4pro-arm64-python-8be3b2f479431f670f2e-3.15.0a1%2B-8be3b2f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.059x faster (HPT: reliability of 99.98%, 1.02x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251116-macm4pro-arm64-python-8be3b2f479431f670f2e-3.15.0a1%2B-8be3b2f-vs-3.13.0rc2.md)
- [📈time plot](bm-20251116-macm4pro-arm64-python-8be3b2f479431f670f2e-3.15.0a1%2B-8be3b2f-vs-3.13.0rc2.svg)

