# Results

- fork: python/d910b93f786982a11d7d
- version: 3.15.0a0
- config: NOGIL
- commit hash: [d910b93](https://github.com/python/cpython/commit/d910b93)
- commit date: 2025-08-27T23:41:31Z
- commit merge base: [bbcb75c986c47887e6c0757e63d59cd7af544f39](https://github.com/python/cpython/commit/bbcb75c986c47887e6c0757e63d59cd7af544f39)
- commit date: 2025-08-27T23:41:31+00:00
- ref: d910b93f786982a11d7d

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17282131557)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250827-vultr-x86_64-python-d910b93f786982a11d7d-3.15.0a0-d910b93.json)

### vs. 3.12.6

- Geometric mean: 1.027x slower (HPT: reliability of 95.25%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250827-vultr-x86_64-python-d910b93f786982a11d7d-3.15.0a0-d910b93-vs-3.12.6.md)
- [📈time plot](bm-20250827-vultr-x86_64-python-d910b93f786982a11d7d-3.15.0a0-d910b93-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.059x slower (HPT: reliability of 98.09%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250827-vultr-x86_64-python-d910b93f786982a11d7d-3.15.0a0-d910b93-vs-3.13.0rc2.md)
- [📈time plot](bm-20250827-vultr-x86_64-python-d910b93f786982a11d7d-3.15.0a0-d910b93-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.099x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20250827-vultr-x86_64-python-d910b93f786982a11d7d-3.15.0a0-d910b93-vs-base-mem.svg)
- [📄table](bm-20250827-vultr-x86_64-python-d910b93f786982a11d7d-3.15.0a0-d910b93-vs-base.md)
- [📈time plot](bm-20250827-vultr-x86_64-python-d910b93f786982a11d7d-3.15.0a0-d910b93-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17282131557)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250827-macm4pro-arm64-python-d910b93f786982a11d7d-3.15.0a0-d910b93.json)

### vs. 3.12.6

- Geometric mean: 1.072x faster (HPT: reliability of 89.18%, 1.00x faster at 99th %ile)
- Memory usage: 1.25x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250827-macm4pro-arm64-python-d910b93f786982a11d7d-3.15.0a0-d910b93-vs-3.12.6.md)
- [📈time plot](bm-20250827-macm4pro-arm64-python-d910b93f786982a11d7d-3.15.0a0-d910b93-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.005x slower (HPT: reliability of 91.46%, 1.00x slower at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250827-macm4pro-arm64-python-d910b93f786982a11d7d-3.15.0a0-d910b93-vs-3.13.0rc2.md)
- [📈time plot](bm-20250827-macm4pro-arm64-python-d910b93f786982a11d7d-3.15.0a0-d910b93-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.031x slower (HPT: reliability of 99.88%, 1.00x slower at 99th %ile)
- Memory usage: 1.11x
- [🧠memory plot](bm-20250827-macm4pro-arm64-python-d910b93f786982a11d7d-3.15.0a0-d910b93-vs-base-mem.svg)
- [📄table](bm-20250827-macm4pro-arm64-python-d910b93f786982a11d7d-3.15.0a0-d910b93-vs-base.md)
- [📈time plot](bm-20250827-macm4pro-arm64-python-d910b93f786982a11d7d-3.15.0a0-d910b93-vs-base.svg)

