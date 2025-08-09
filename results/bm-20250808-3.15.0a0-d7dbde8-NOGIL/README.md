# Results

- fork: python/d7dbde895884d58e3da7
- version: 3.15.0a0
- config: NOGIL
- commit hash: [d7dbde8](https://github.com/python/cpython/commit/d7dbde8)
- commit date: 2025-08-08T12:07:15-07:00
- commit merge base: [34d7351ac770ac49875fc39396b2a97828ba05ad](https://github.com/python/cpython/commit/34d7351ac770ac49875fc39396b2a97828ba05ad)
- ref: d7dbde895884d58e3da7

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16843183473)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250808-vultr-x86_64-python-d7dbde895884d58e3da7-3.15.0a0-d7dbde8.json)

### vs. 3.12.6

- Geometric mean: 1.023x slower (HPT: reliability of 92.22%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250808-vultr-x86_64-python-d7dbde895884d58e3da7-3.15.0a0-d7dbde8-vs-3.12.6.md)
- [📈time plot](bm-20250808-vultr-x86_64-python-d7dbde895884d58e3da7-3.15.0a0-d7dbde8-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.056x slower (HPT: reliability of 98.95%, 1.00x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250808-vultr-x86_64-python-d7dbde895884d58e3da7-3.15.0a0-d7dbde8-vs-3.13.0rc2.md)
- [📈time plot](bm-20250808-vultr-x86_64-python-d7dbde895884d58e3da7-3.15.0a0-d7dbde8-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.091x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20250808-vultr-x86_64-python-d7dbde895884d58e3da7-3.15.0a0-d7dbde8-vs-base-mem.svg)
- [📄table](bm-20250808-vultr-x86_64-python-d7dbde895884d58e3da7-3.15.0a0-d7dbde8-vs-base.md)
- [📈time plot](bm-20250808-vultr-x86_64-python-d7dbde895884d58e3da7-3.15.0a0-d7dbde8-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16843183473)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250808-macm4pro-arm64-python-d7dbde895884d58e3da7-3.15.0a0-d7dbde8.json)

### vs. 3.12.6

- Geometric mean: 1.087x faster (HPT: reliability of 97.48%, 1.00x faster at 99th %ile)
- Memory usage: 1.25x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250808-macm4pro-arm64-python-d7dbde895884d58e3da7-3.15.0a0-d7dbde8-vs-3.12.6.md)
- [📈time plot](bm-20250808-macm4pro-arm64-python-d7dbde895884d58e3da7-3.15.0a0-d7dbde8-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.008x faster (HPT: reliability of 74.92%, 1.00x slower at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250808-macm4pro-arm64-python-d7dbde895884d58e3da7-3.15.0a0-d7dbde8-vs-3.13.0rc2.md)
- [📈time plot](bm-20250808-macm4pro-arm64-python-d7dbde895884d58e3da7-3.15.0a0-d7dbde8-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.014x slower (HPT: reliability of 93.42%, 1.00x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20250808-macm4pro-arm64-python-d7dbde895884d58e3da7-3.15.0a0-d7dbde8-vs-base-mem.svg)
- [📄table](bm-20250808-macm4pro-arm64-python-d7dbde895884d58e3da7-3.15.0a0-d7dbde8-vs-base.md)
- [📈time plot](bm-20250808-macm4pro-arm64-python-d7dbde895884d58e3da7-3.15.0a0-d7dbde8-vs-base.svg)

