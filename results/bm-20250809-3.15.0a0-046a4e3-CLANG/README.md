# Results

- fork: python/046a4e39b3f8ac5cb13e
- version: 3.15.0a0
- config: CLANG
- commit hash: [046a4e3](https://github.com/python/cpython/commit/046a4e3)
- commit date: 2025-08-09T18:25:49Z
- commit merge base: [af15e1d13ea26575afbb94b814e541586547a706](https://github.com/python/cpython/commit/af15e1d13ea26575afbb94b814e541586547a706)
- commit date: 2025-08-09T18:25:49+00:00
- ref: 046a4e39b3f8ac5cb13e

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16855182111)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250809-vultr-x86_64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3.json)

### vs. 3.12.6

- Geometric mean: 1.120x faster (HPT: reliability of 100.00%, 1.10x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250809-vultr-x86_64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3-vs-3.12.6.md)
- [📈time plot](bm-20250809-vultr-x86_64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.083x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250809-vultr-x86_64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3-vs-3.13.0rc2.md)
- [📈time plot](bm-20250809-vultr-x86_64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.048x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.03x
- [🧠memory plot](bm-20250809-vultr-x86_64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3-vs-base-mem.svg)
- [📄table](bm-20250809-vultr-x86_64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3-vs-base.md)
- [📈time plot](bm-20250809-vultr-x86_64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16855182111)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3.json)

### vs. 3.12.6

- Geometric mean: 1.143x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3-vs-3.12.6.md)
- [📈time plot](bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.060x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3-vs-3.13.0rc2.md)
- [📈time plot](bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.052x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3-vs-base-mem.svg)
- [📄table](bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3-vs-base.md)
- [📈time plot](bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3-vs-base.svg)

