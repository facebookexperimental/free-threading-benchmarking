# Results

- fork: python/03017a8cc2242d881a30
- version: 3.15.0a0
- config: 
- commit hash: [03017a8](https://github.com/python/cpython/commit/03017a8)
- commit date: 2025-07-18T19:07:46+03:00
- commit merge base: [28937d3a21cf8168c853ae43374a8287c21f71c9](https://github.com/python/cpython/commit/28937d3a21cf8168c853ae43374a8287c21f71c9)
- ref: 03017a8cc2242d881a30

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16382877609)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250718-vultr-x86_64-python-03017a8cc2242d881a30-3.15.0a0-03017a8.json)

### vs. 3.12.6

- Geometric mean: 1.068x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250718-vultr-x86_64-python-03017a8cc2242d881a30-3.15.0a0-03017a8-vs-3.12.6.md)
- [📈time plot](bm-20250718-vultr-x86_64-python-03017a8cc2242d881a30-3.15.0a0-03017a8-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.032x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250718-vultr-x86_64-python-03017a8cc2242d881a30-3.15.0a0-03017a8-vs-3.13.0rc2.md)
- [📈time plot](bm-20250718-vultr-x86_64-python-03017a8cc2242d881a30-3.15.0a0-03017a8-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.001x slower (HPT: reliability of 82.52%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250718-vultr-x86_64-python-03017a8cc2242d881a30-3.15.0a0-03017a8-vs-base-mem.svg)
- [📄table](bm-20250718-vultr-x86_64-python-03017a8cc2242d881a30-3.15.0a0-03017a8-vs-base.md)
- [📈time plot](bm-20250718-vultr-x86_64-python-03017a8cc2242d881a30-3.15.0a0-03017a8-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16382877609)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250718-macm4pro-arm64-python-03017a8cc2242d881a30-3.15.0a0-03017a8.json)

### vs. 3.12.6

- Geometric mean: 1.107x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250718-macm4pro-arm64-python-03017a8cc2242d881a30-3.15.0a0-03017a8-vs-3.12.6.md)
- [📈time plot](bm-20250718-macm4pro-arm64-python-03017a8cc2242d881a30-3.15.0a0-03017a8-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.027x faster (HPT: reliability of 73.48%, 1.00x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250718-macm4pro-arm64-python-03017a8cc2242d881a30-3.15.0a0-03017a8-vs-3.13.0rc2.md)
- [📈time plot](bm-20250718-macm4pro-arm64-python-03017a8cc2242d881a30-3.15.0a0-03017a8-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.004x slower (HPT: reliability of 99.92%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250718-macm4pro-arm64-python-03017a8cc2242d881a30-3.15.0a0-03017a8-vs-base-mem.svg)
- [📄table](bm-20250718-macm4pro-arm64-python-03017a8cc2242d881a30-3.15.0a0-03017a8-vs-base.md)
- [📈time plot](bm-20250718-macm4pro-arm64-python-03017a8cc2242d881a30-3.15.0a0-03017a8-vs-base.svg)

