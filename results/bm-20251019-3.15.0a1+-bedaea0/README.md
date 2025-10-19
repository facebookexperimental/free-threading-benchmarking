# Results

- fork: python/bedaea05987738c4c6b9
- version: 3.15.0a1+
- config: 
- commit hash: [bedaea0](https://github.com/python/cpython/commit/bedaea0)
- commit date: 2025-10-19T00:20:04+01:00
- commit merge base: [920de7ccdcfa7284b6d23a124771b17c66dd3e4f](https://github.com/python/cpython/commit/920de7ccdcfa7284b6d23a124771b17c66dd3e4f)
- ref: bedaea05987738c4c6b9

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18622795374)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [pystats raw](bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-pystats.json)
- [pystats table](bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-pystats.md)
- [raw results](bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0.json)

### vs. 3.12.6

- Geometric mean: 1.066x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-vs-3.12.6.md)
- [📈time plot](bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.029x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-vs-3.13.0rc2.md)
- [📈time plot](bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18622795374)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0.json)

### vs. 3.12.6

- Geometric mean: 1.104x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-vs-3.12.6.md)
- [📈time plot](bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.025x faster (HPT: reliability of 95.07%, 1.00x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-vs-3.13.0rc2.md)
- [📈time plot](bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-vs-3.13.0rc2.svg)

