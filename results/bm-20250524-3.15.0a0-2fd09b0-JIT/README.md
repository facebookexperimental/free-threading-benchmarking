# Results

- fork: python/2fd09b011031f3c00c34
- version: 3.15.0a0
- config: JIT
- commit hash: [2fd09b0](https://github.com/python/cpython/commit/2fd09b0)
- commit date: 2025-05-24T12:19:20Z
- commit merge base: [5d9c8fe3f6168785cb608dddd3010042f39bb226](https://github.com/python/cpython/commit/5d9c8fe3f6168785cb608dddd3010042f39bb226)
- commit date: 2025-05-24T12:19:20+00:00
- ref: 2fd09b011031f3c00c34

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15232282695)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250524-vultr-x86_64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0.json)

### vs. 3.12.6

- Geometric mean: 1.104x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250524-vultr-x86_64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-3.12.6.md)
- [📈time plot](bm-20250524-vultr-x86_64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.067x faster (HPT: reliability of 99.97%, 1.00x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250524-vultr-x86_64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-3.13.0rc2.md)
- [📈time plot](bm-20250524-vultr-x86_64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.002x slower (HPT: reliability of 99.73%, 1.00x slower at 99th %ile)
- Memory usage: 1.02x
- [🧠memory plot](bm-20250524-vultr-x86_64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-base-mem.svg)
- [📄table](bm-20250524-vultr-x86_64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-base.md)
- [📈time plot](bm-20250524-vultr-x86_64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15232282695)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250524-macm4pro-arm64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0.json)

### vs. 3.12.6

- Geometric mean: 1.123x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250524-macm4pro-arm64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-3.12.6.md)
- [📈time plot](bm-20250524-macm4pro-arm64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.042x faster (HPT: reliability of 98.03%, 1.00x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250524-macm4pro-arm64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-3.13.0rc2.md)
- [📈time plot](bm-20250524-macm4pro-arm64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.010x faster (HPT: reliability of 99.99%, 1.00x faster at 99th %ile)
- Memory usage: 1.02x
- [🧠memory plot](bm-20250524-macm4pro-arm64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-base-mem.svg)
- [📄table](bm-20250524-macm4pro-arm64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-base.md)
- [📈time plot](bm-20250524-macm4pro-arm64-python-2fd09b011031f3c00c34-3.15.0a0-2fd09b0-vs-base.svg)

