# Results

- fork: python/c461aa99e2fabbaf5859
- version: 3.15.0a5+
- config: NOGIL
- commit hash: [c461aa9](https://github.com/python/cpython/commit/c461aa9)
- commit date: 2026-01-15T16:08:55+01:00
- commit merge base: [3514ba2175764e4d746e6862e2fcfc06b5fcd6c2](https://github.com/python/cpython/commit/3514ba2175764e4d746e6862e2fcfc06b5fcd6c2)
- ref: c461aa99e2fabbaf5859

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21051282101)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260115-vultr-x86_64-python-c461aa99e2fabbaf5859-3.15.0a5%2B-c461aa9.json)

### vs. 3.12.6

- Geometric mean: 1.029x slower (HPT: reliability of 79.12%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260115-vultr-x86_64-python-c461aa99e2fabbaf5859-3.15.0a5%2B-c461aa9-vs-3.12.6.md)
- [📈time plot](bm-20260115-vultr-x86_64-python-c461aa99e2fabbaf5859-3.15.0a5%2B-c461aa9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.062x slower (HPT: reliability of 87.52%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260115-vultr-x86_64-python-c461aa99e2fabbaf5859-3.15.0a5%2B-c461aa9-vs-3.13.0rc2.md)
- [📈time plot](bm-20260115-vultr-x86_64-python-c461aa99e2fabbaf5859-3.15.0a5%2B-c461aa9-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.100x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20260115-vultr-x86_64-python-c461aa99e2fabbaf5859-3.15.0a5%2B-c461aa9-vs-base-mem.svg)
- [📄table](bm-20260115-vultr-x86_64-python-c461aa99e2fabbaf5859-3.15.0a5%2B-c461aa9-vs-base.md)
- [📈time plot](bm-20260115-vultr-x86_64-python-c461aa99e2fabbaf5859-3.15.0a5%2B-c461aa9-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21051282101)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260115-macm4pro-arm64-python-c461aa99e2fabbaf5859-3.15.0a5%2B-c461aa9.json)

### vs. 3.12.6

- Geometric mean: 1.075x faster (HPT: reliability of 94.72%, 1.00x faster at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260115-macm4pro-arm64-python-c461aa99e2fabbaf5859-3.15.0a5%2B-c461aa9-vs-3.12.6.md)
- [📈time plot](bm-20260115-macm4pro-arm64-python-c461aa99e2fabbaf5859-3.15.0a5%2B-c461aa9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.003x slower (HPT: reliability of 86.16%, 1.00x slower at 99th %ile)
- Memory usage: 1.30x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260115-macm4pro-arm64-python-c461aa99e2fabbaf5859-3.15.0a5%2B-c461aa9-vs-3.13.0rc2.md)
- [📈time plot](bm-20260115-macm4pro-arm64-python-c461aa99e2fabbaf5859-3.15.0a5%2B-c461aa9-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.070x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.11x
- [🧠memory plot](bm-20260115-macm4pro-arm64-python-c461aa99e2fabbaf5859-3.15.0a5%2B-c461aa9-vs-base-mem.svg)
- [📄table](bm-20260115-macm4pro-arm64-python-c461aa99e2fabbaf5859-3.15.0a5%2B-c461aa9-vs-base.md)
- [📈time plot](bm-20260115-macm4pro-arm64-python-c461aa99e2fabbaf5859-3.15.0a5%2B-c461aa9-vs-base.svg)

