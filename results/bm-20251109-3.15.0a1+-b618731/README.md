# Results

- fork: python/b618731781c31d4b5b75
- version: 3.15.0a1+
- config: 
- commit hash: [b618731](https://github.com/python/cpython/commit/b618731)
- commit date: 2025-11-09T17:45:38-06:00
- commit merge base: [ec85d3cbfe315086805c33bb64c28a8509098829](https://github.com/python/cpython/commit/ec85d3cbfe315086805c33bb64c28a8509098829)
- ref: b618731781c31d4b5b75

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19216869476)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251109-vultr-x86_64-python-b618731781c31d4b5b75-3.15.0a1%2B-b618731.json)

### vs. 3.12.6

- Geometric mean: 1.085x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251109-vultr-x86_64-python-b618731781c31d4b5b75-3.15.0a1%2B-b618731-vs-3.12.6.md)
- [📈time plot](bm-20251109-vultr-x86_64-python-b618731781c31d4b5b75-3.15.0a1%2B-b618731-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.049x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251109-vultr-x86_64-python-b618731781c31d4b5b75-3.15.0a1%2B-b618731-vs-3.13.0rc2.md)
- [📈time plot](bm-20251109-vultr-x86_64-python-b618731781c31d4b5b75-3.15.0a1%2B-b618731-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19216869476)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251109-macm4pro-arm64-python-b618731781c31d4b5b75-3.15.0a1%2B-b618731.json)

### vs. 3.12.6

- Geometric mean: 1.107x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251109-macm4pro-arm64-python-b618731781c31d4b5b75-3.15.0a1%2B-b618731-vs-3.12.6.md)
- [📈time plot](bm-20251109-macm4pro-arm64-python-b618731781c31d4b5b75-3.15.0a1%2B-b618731-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.026x faster (HPT: reliability of 82.23%, 1.00x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251109-macm4pro-arm64-python-b618731781c31d4b5b75-3.15.0a1%2B-b618731-vs-3.13.0rc2.md)
- [📈time plot](bm-20251109-macm4pro-arm64-python-b618731781c31d4b5b75-3.15.0a1%2B-b618731-vs-3.13.0rc2.svg)

