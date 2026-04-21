# Results

- fork: python/d206d42834b2a34aee11
- version: 3.15.0a8+
- config: NOGIL
- commit hash: [d206d42](https://github.com/python/cpython/commit/d206d42)
- commit date: 2026-04-21T07:04:50+08:00
- commit merge base: [f6ed7c0acbd9234226cab5cca12f9d312809103e](https://github.com/python/cpython/commit/f6ed7c0acbd9234226cab5cca12f9d312809103e)
- ref: d206d42834b2a34aee11

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/24698083877)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260421-vultr-x86_64-python-d206d42834b2a34aee11-3.15.0a8%2B-d206d42.json)

### vs. 3.12.6

- Geometric mean: 1.016x slower (HPT: reliability of 63.69%, 1.00x slower at 99th %ile)
- Memory usage: 1.44x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260421-vultr-x86_64-python-d206d42834b2a34aee11-3.15.0a8%2B-d206d42-vs-3.12.6.md)
- [📈time plot](bm-20260421-vultr-x86_64-python-d206d42834b2a34aee11-3.15.0a8%2B-d206d42-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.048x slower (HPT: reliability of 87.42%, 1.00x slower at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260421-vultr-x86_64-python-d206d42834b2a34aee11-3.15.0a8%2B-d206d42-vs-3.13.0rc2.md)
- [📈time plot](bm-20260421-vultr-x86_64-python-d206d42834b2a34aee11-3.15.0a8%2B-d206d42-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.094x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20260421-vultr-x86_64-python-d206d42834b2a34aee11-3.15.0a8%2B-d206d42-vs-base-mem.svg)
- [📄table](bm-20260421-vultr-x86_64-python-d206d42834b2a34aee11-3.15.0a8%2B-d206d42-vs-base.md)
- [📈time plot](bm-20260421-vultr-x86_64-python-d206d42834b2a34aee11-3.15.0a8%2B-d206d42-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/24698083877)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260421-macm4pro-arm64-python-d206d42834b2a34aee11-3.15.0a8%2B-d206d42.json)

### vs. 3.12.6

- Geometric mean: 1.101x faster (HPT: reliability of 99.60%, 1.00x faster at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260421-macm4pro-arm64-python-d206d42834b2a34aee11-3.15.0a8%2B-d206d42-vs-3.12.6.md)
- [📈time plot](bm-20260421-macm4pro-arm64-python-d206d42834b2a34aee11-3.15.0a8%2B-d206d42-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.022x faster (HPT: reliability of 60.25%, 1.00x faster at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260421-macm4pro-arm64-python-d206d42834b2a34aee11-3.15.0a8%2B-d206d42-vs-3.13.0rc2.md)
- [📈time plot](bm-20260421-macm4pro-arm64-python-d206d42834b2a34aee11-3.15.0a8%2B-d206d42-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.030x slower (HPT: reliability of 100.00%, 1.02x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20260421-macm4pro-arm64-python-d206d42834b2a34aee11-3.15.0a8%2B-d206d42-vs-base-mem.svg)
- [📄table](bm-20260421-macm4pro-arm64-python-d206d42834b2a34aee11-3.15.0a8%2B-d206d42-vs-base.md)
- [📈time plot](bm-20260421-macm4pro-arm64-python-d206d42834b2a34aee11-3.15.0a8%2B-d206d42-vs-base.svg)

