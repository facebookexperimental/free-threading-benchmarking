# Results

- fork: python/37b5a0d671685645db8f
- version: 3.15.0a0
- config: 
- commit hash: [37b5a0d](https://github.com/python/cpython/commit/37b5a0d)
- commit date: 2025-08-07T23:43:18Z
- commit merge base: [350c58ba4ee13019b0cde70b49bfeadc63f4ceb8](https://github.com/python/cpython/commit/350c58ba4ee13019b0cde70b49bfeadc63f4ceb8)
- commit date: 2025-08-07T23:43:18+00:00
- ref: 37b5a0d671685645db8f

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16818918114)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250807-vultr-x86_64-python-37b5a0d671685645db8f-3.15.0a0-37b5a0d.json)

### vs. 3.12.6

- Geometric mean: 1.073x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250807-vultr-x86_64-python-37b5a0d671685645db8f-3.15.0a0-37b5a0d-vs-3.12.6.md)
- [📈time plot](bm-20250807-vultr-x86_64-python-37b5a0d671685645db8f-3.15.0a0-37b5a0d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.038x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250807-vultr-x86_64-python-37b5a0d671685645db8f-3.15.0a0-37b5a0d-vs-3.13.0rc2.md)
- [📈time plot](bm-20250807-vultr-x86_64-python-37b5a0d671685645db8f-3.15.0a0-37b5a0d-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16818918114)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250807-macm4pro-arm64-python-37b5a0d671685645db8f-3.15.0a0-37b5a0d.json)

### vs. 3.12.6

- Geometric mean: 1.089x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250807-macm4pro-arm64-python-37b5a0d671685645db8f-3.15.0a0-37b5a0d-vs-3.12.6.md)
- [📈time plot](bm-20250807-macm4pro-arm64-python-37b5a0d671685645db8f-3.15.0a0-37b5a0d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.010x faster (HPT: reliability of 58.52%, 1.00x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250807-macm4pro-arm64-python-37b5a0d671685645db8f-3.15.0a0-37b5a0d-vs-3.13.0rc2.md)
- [📈time plot](bm-20250807-macm4pro-arm64-python-37b5a0d671685645db8f-3.15.0a0-37b5a0d-vs-3.13.0rc2.svg)

