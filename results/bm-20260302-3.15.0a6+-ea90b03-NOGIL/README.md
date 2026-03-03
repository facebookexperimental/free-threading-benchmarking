# Results

- fork: python/ea90b032a016122e7871
- version: 3.15.0a6+
- config: NOGIL
- commit hash: [ea90b03](https://github.com/python/cpython/commit/ea90b03)
- commit date: 2026-03-02T23:39:07+02:00
- commit merge base: [46c5c57226862bc078bcdf0c9f5b40951b8615a5](https://github.com/python/cpython/commit/46c5c57226862bc078bcdf0c9f5b40951b8615a5)
- ref: ea90b032a016122e7871

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/22602595698)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260302-vultr-x86_64-python-ea90b032a016122e7871-3.15.0a6%2B-ea90b03.json)

### vs. 3.12.6

- Geometric mean: 1.025x slower (HPT: reliability of 72.08%, 1.00x slower at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260302-vultr-x86_64-python-ea90b032a016122e7871-3.15.0a6%2B-ea90b03-vs-3.12.6.md)
- [📈time plot](bm-20260302-vultr-x86_64-python-ea90b032a016122e7871-3.15.0a6%2B-ea90b03-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.058x slower (HPT: reliability of 84.99%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260302-vultr-x86_64-python-ea90b032a016122e7871-3.15.0a6%2B-ea90b03-vs-3.13.0rc2.md)
- [📈time plot](bm-20260302-vultr-x86_64-python-ea90b032a016122e7871-3.15.0a6%2B-ea90b03-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.094x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20260302-vultr-x86_64-python-ea90b032a016122e7871-3.15.0a6%2B-ea90b03-vs-base-mem.svg)
- [📄table](bm-20260302-vultr-x86_64-python-ea90b032a016122e7871-3.15.0a6%2B-ea90b03-vs-base.md)
- [📈time plot](bm-20260302-vultr-x86_64-python-ea90b032a016122e7871-3.15.0a6%2B-ea90b03-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/22602595698)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260302-macm4pro-arm64-python-ea90b032a016122e7871-3.15.0a6%2B-ea90b03.json)

### vs. 3.12.6

- Geometric mean: 1.090x faster (HPT: reliability of 99.09%, 1.00x faster at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260302-macm4pro-arm64-python-ea90b032a016122e7871-3.15.0a6%2B-ea90b03-vs-3.12.6.md)
- [📈time plot](bm-20260302-macm4pro-arm64-python-ea90b032a016122e7871-3.15.0a6%2B-ea90b03-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.011x faster (HPT: reliability of 62.52%, 1.00x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260302-macm4pro-arm64-python-ea90b032a016122e7871-3.15.0a6%2B-ea90b03-vs-3.13.0rc2.md)
- [📈time plot](bm-20260302-macm4pro-arm64-python-ea90b032a016122e7871-3.15.0a6%2B-ea90b03-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.041x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20260302-macm4pro-arm64-python-ea90b032a016122e7871-3.15.0a6%2B-ea90b03-vs-base-mem.svg)
- [📄table](bm-20260302-macm4pro-arm64-python-ea90b032a016122e7871-3.15.0a6%2B-ea90b03-vs-base.md)
- [📈time plot](bm-20260302-macm4pro-arm64-python-ea90b032a016122e7871-3.15.0a6%2B-ea90b03-vs-base.svg)

