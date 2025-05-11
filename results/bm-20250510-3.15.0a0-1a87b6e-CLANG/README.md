# Results

- fork: python/1a87b6e9ae6da255f304
- version: 3.15.0a0
- config: CLANG
- commit hash: [1a87b6e](https://github.com/python/cpython/commit/1a87b6e)
- commit date: 2025-05-10T22:37:17Z
- commit merge base: [dc191d248456855d228b09f0e0206e0b656f113c](https://github.com/python/cpython/commit/dc191d248456855d228b09f0e0206e0b656f113c)
- commit date: 2025-05-10T22:37:17+00:00
- ref: 1a87b6e9ae6da255f304

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14950406813)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250510-vultr-x86_64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e.json)

### vs. 3.12.6

- Geometric mean: 1.155x faster (HPT: reliability of 100.00%, 1.08x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250510-vultr-x86_64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e-vs-3.12.6.md)
- [📈time plot](bm-20250510-vultr-x86_64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.117x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250510-vultr-x86_64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e-vs-3.13.0rc2.md)
- [📈time plot](bm-20250510-vultr-x86_64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.043x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.04x
- [🧠memory plot](bm-20250510-vultr-x86_64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e-vs-base-mem.svg)
- [📄table](bm-20250510-vultr-x86_64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e-vs-base.md)
- [📈time plot](bm-20250510-vultr-x86_64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14950406813)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e.json)

### vs. 3.12.6

- Geometric mean: 1.146x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e-vs-3.12.6.md)
- [📈time plot](bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.063x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e-vs-3.13.0rc2.md)
- [📈time plot](bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.052x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.03x
- [🧠memory plot](bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e-vs-base-mem.svg)
- [📄table](bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e-vs-base.md)
- [📈time plot](bm-20250510-macm4pro-arm64-python-1a87b6e9ae6da255f304-3.15.0a0-1a87b6e-vs-base.svg)

