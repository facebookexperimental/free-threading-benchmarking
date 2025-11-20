# Results

- fork: python/ca1e86f9d963dc298d9a
- version: 3.15.0a2+
- config: NOGIL
- commit hash: [ca1e86f](https://github.com/python/cpython/commit/ca1e86f)
- commit date: 2025-11-19T15:57:44-08:00
- commit merge base: [b4344f7020f066e83a113e0d4f9343cec4e56a1e](https://github.com/python/cpython/commit/b4344f7020f066e83a113e0d4f9343cec4e56a1e)
- ref: ca1e86f9d963dc298d9a

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19520969671)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251119-vultr-x86_64-python-ca1e86f9d963dc298d9a-3.15.0a2%2B-ca1e86f.json)

### vs. 3.12.6

- Geometric mean: 1.012x slower (HPT: reliability of 67.91%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251119-vultr-x86_64-python-ca1e86f9d963dc298d9a-3.15.0a2%2B-ca1e86f-vs-3.12.6.md)
- [📈time plot](bm-20251119-vultr-x86_64-python-ca1e86f9d963dc298d9a-3.15.0a2%2B-ca1e86f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.045x slower (HPT: reliability of 88.00%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251119-vultr-x86_64-python-ca1e86f9d963dc298d9a-3.15.0a2%2B-ca1e86f-vs-3.13.0rc2.md)
- [📈time plot](bm-20251119-vultr-x86_64-python-ca1e86f9d963dc298d9a-3.15.0a2%2B-ca1e86f-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.083x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20251119-vultr-x86_64-python-ca1e86f9d963dc298d9a-3.15.0a2%2B-ca1e86f-vs-base-mem.svg)
- [📄table](bm-20251119-vultr-x86_64-python-ca1e86f9d963dc298d9a-3.15.0a2%2B-ca1e86f-vs-base.md)
- [📈time plot](bm-20251119-vultr-x86_64-python-ca1e86f9d963dc298d9a-3.15.0a2%2B-ca1e86f-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19520969671)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2%2B-ca1e86f.json)

### vs. 3.12.6

- Geometric mean: 1.120x faster (HPT: reliability of 99.98%, 1.02x faster at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2%2B-ca1e86f-vs-3.12.6.md)
- [📈time plot](bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2%2B-ca1e86f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.033x faster (HPT: reliability of 53.10%, 1.00x faster at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2%2B-ca1e86f-vs-3.13.0rc2.md)
- [📈time plot](bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2%2B-ca1e86f-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.008x slower (HPT: reliability of 94.11%, 1.00x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2%2B-ca1e86f-vs-base-mem.svg)
- [📄table](bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2%2B-ca1e86f-vs-base.md)
- [📈time plot](bm-20251119-macm4pro-arm64-python-ca1e86f9d963dc298d9a-3.15.0a2%2B-ca1e86f-vs-base.svg)

