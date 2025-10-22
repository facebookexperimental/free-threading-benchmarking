# Results

- fork: python/b3a38438d83245e52dff
- version: 3.15.0a1+
- config: 
- commit hash: [b3a3843](https://github.com/python/cpython/commit/b3a3843)
- commit date: 2025-10-22T09:14:48+09:00
- commit merge base: [29b38b7aae884c14085a918282ea7f0798ed7a2a](https://github.com/python/cpython/commit/29b38b7aae884c14085a918282ea7f0798ed7a2a)
- ref: b3a38438d83245e52dff

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18701530889)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251022-vultr-x86_64-python-b3a38438d83245e52dff-3.15.0a1%2B-b3a3843.json)

### vs. 3.12.6

- Geometric mean: 1.077x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251022-vultr-x86_64-python-b3a38438d83245e52dff-3.15.0a1%2B-b3a3843-vs-3.12.6.md)
- [📈time plot](bm-20251022-vultr-x86_64-python-b3a38438d83245e52dff-3.15.0a1%2B-b3a3843-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.041x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251022-vultr-x86_64-python-b3a38438d83245e52dff-3.15.0a1%2B-b3a3843-vs-3.13.0rc2.md)
- [📈time plot](bm-20251022-vultr-x86_64-python-b3a38438d83245e52dff-3.15.0a1%2B-b3a3843-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18701530889)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251022-macm4pro-arm64-python-b3a38438d83245e52dff-3.15.0a1%2B-b3a3843.json)

### vs. 3.12.6

- Geometric mean: 1.086x faster (HPT: reliability of 99.91%, 1.00x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251022-macm4pro-arm64-python-b3a38438d83245e52dff-3.15.0a1%2B-b3a3843-vs-3.12.6.md)
- [📈time plot](bm-20251022-macm4pro-arm64-python-b3a38438d83245e52dff-3.15.0a1%2B-b3a3843-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.008x faster (HPT: reliability of 55.61%, 1.00x slower at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251022-macm4pro-arm64-python-b3a38438d83245e52dff-3.15.0a1%2B-b3a3843-vs-3.13.0rc2.md)
- [📈time plot](bm-20251022-macm4pro-arm64-python-b3a38438d83245e52dff-3.15.0a1%2B-b3a3843-vs-3.13.0rc2.svg)

