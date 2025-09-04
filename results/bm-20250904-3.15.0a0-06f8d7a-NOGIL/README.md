# Results

- fork: python/06f8d7aa9f448128d6eb
- version: 3.15.0a0
- config: NOGIL
- commit hash: [06f8d7a](https://github.com/python/cpython/commit/06f8d7a)
- commit date: 2025-09-04T00:27:14+01:00
- commit merge base: [3b4cd885634abc029b409cb566e8d9a530d061f8](https://github.com/python/cpython/commit/3b4cd885634abc029b409cb566e8d9a530d061f8)
- ref: 06f8d7aa9f448128d6eb

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17449570042)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250904-vultr-x86_64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a.json)

### vs. 3.12.6

- Geometric mean: 1.023x slower (HPT: reliability of 90.07%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250904-vultr-x86_64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a-vs-3.12.6.md)
- [📈time plot](bm-20250904-vultr-x86_64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.056x slower (HPT: reliability of 98.15%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250904-vultr-x86_64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a-vs-3.13.0rc2.md)
- [📈time plot](bm-20250904-vultr-x86_64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.091x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20250904-vultr-x86_64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a-vs-base-mem.svg)
- [📄table](bm-20250904-vultr-x86_64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a-vs-base.md)
- [📈time plot](bm-20250904-vultr-x86_64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17449570042)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250904-macm4pro-arm64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a.json)

### vs. 3.12.6

- Geometric mean: 1.075x faster (HPT: reliability of 91.11%, 1.00x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250904-macm4pro-arm64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a-vs-3.12.6.md)
- [📈time plot](bm-20250904-macm4pro-arm64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.003x slower (HPT: reliability of 80.13%, 1.00x slower at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250904-macm4pro-arm64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a-vs-3.13.0rc2.md)
- [📈time plot](bm-20250904-macm4pro-arm64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.021x slower (HPT: reliability of 99.62%, 1.00x slower at 99th %ile)
- Memory usage: 1.11x
- [🧠memory plot](bm-20250904-macm4pro-arm64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a-vs-base-mem.svg)
- [📄table](bm-20250904-macm4pro-arm64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a-vs-base.md)
- [📈time plot](bm-20250904-macm4pro-arm64-python-06f8d7aa9f448128d6eb-3.15.0a0-06f8d7a-vs-base.svg)

