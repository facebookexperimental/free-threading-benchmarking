# Results

- fork: python/0f866cbfefd797b4dae2
- version: 3.15.0a0
- config: NOGIL
- commit hash: [0f866cb](https://github.com/python/cpython/commit/0f866cb)
- commit date: 2025-06-10T13:38:32Z
- commit merge base: [ff2b5f40c2bf5c71255caac8a743c09ba0758c02](https://github.com/python/cpython/commit/ff2b5f40c2bf5c71255caac8a743c09ba0758c02)
- commit date: 2025-06-10T13:38:32+00:00
- ref: 0f866cbfefd797b4dae2

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15573140329)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb.json)

### vs. 3.12.6

- Geometric mean: 1.017x faster (HPT: reliability of 85.43%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb-vs-3.12.6.md)
- [📈time plot](bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.018x slower (HPT: reliability of 95.20%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb-vs-3.13.0rc2.md)
- [📈time plot](bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.088x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.22x
- [🧠memory plot](bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb-vs-base-mem.svg)
- [📄table](bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb-vs-base.md)
- [📈time plot](bm-20250610-vultr-x86_64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15573140329)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb.json)

### vs. 3.12.6

- Geometric mean: 1.100x faster (HPT: reliability of 98.90%, 1.00x faster at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb-vs-3.12.6.md)
- [📈time plot](bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.020x faster (HPT: reliability of 62.64%, 1.00x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb-vs-3.13.0rc2.md)
- [📈time plot](bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.020x slower (HPT: reliability of 98.63%, 1.00x slower at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: 🔴 dask
- [🧠memory plot](bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb-vs-base-mem.svg)
- [📄table](bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb-vs-base.md)
- [📈time plot](bm-20250610-macm4pro-arm64-python-0f866cbfefd797b4dae2-3.15.0a0-0f866cb-vs-base.svg)

