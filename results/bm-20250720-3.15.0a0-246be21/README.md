# Results

- fork: python/246be21de1e2a51d757c
- version: 3.15.0a0
- config: 
- commit hash: [246be21](https://github.com/python/cpython/commit/246be21)
- commit date: 2025-07-20T23:34:32Z
- commit merge base: [aec7f5f8b2e8b5e02869cdb4e1f8a9ef87c9f953](https://github.com/python/cpython/commit/aec7f5f8b2e8b5e02869cdb4e1f8a9ef87c9f953)
- commit date: 2025-07-20T23:34:32+00:00
- ref: 246be21de1e2a51d757c

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16405942202)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250720-vultr-x86_64-python-246be21de1e2a51d757c-3.15.0a0-246be21.json)

### vs. 3.12.6

- Geometric mean: 1.072x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250720-vultr-x86_64-python-246be21de1e2a51d757c-3.15.0a0-246be21-vs-3.12.6.md)
- [📈time plot](bm-20250720-vultr-x86_64-python-246be21de1e2a51d757c-3.15.0a0-246be21-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.036x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250720-vultr-x86_64-python-246be21de1e2a51d757c-3.15.0a0-246be21-vs-3.13.0rc2.md)
- [📈time plot](bm-20250720-vultr-x86_64-python-246be21de1e2a51d757c-3.15.0a0-246be21-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16405942202)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250720-macm4pro-arm64-python-246be21de1e2a51d757c-3.15.0a0-246be21.json)

### vs. 3.12.6

- Geometric mean: 1.085x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250720-macm4pro-arm64-python-246be21de1e2a51d757c-3.15.0a0-246be21-vs-3.12.6.md)
- [📈time plot](bm-20250720-macm4pro-arm64-python-246be21de1e2a51d757c-3.15.0a0-246be21-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.006x faster (HPT: reliability of 60.82%, 1.00x slower at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250720-macm4pro-arm64-python-246be21de1e2a51d757c-3.15.0a0-246be21-vs-3.13.0rc2.md)
- [📈time plot](bm-20250720-macm4pro-arm64-python-246be21de1e2a51d757c-3.15.0a0-246be21-vs-3.13.0rc2.svg)

