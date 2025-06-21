# Results

- fork: python/4ddf505d9982dc8afead
- version: 3.15.0a0
- config: NOGIL
- commit hash: [4ddf505](https://github.com/python/cpython/commit/4ddf505)
- commit date: 2025-06-20T18:45:36-04:00
- commit merge base: [c5ea8e8e8fc725f39ed23ff6259b3cc157a0785f](https://github.com/python/cpython/commit/c5ea8e8e8fc725f39ed23ff6259b3cc157a0785f)
- ref: 4ddf505d9982dc8afead

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15790092754)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505.json)

### vs. 3.12.6

- Geometric mean: 1.019x faster (HPT: reliability of 78.56%, 1.00x slower at 99th %ile)
- Memory usage: 1.44x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505-vs-3.12.6.md)
- [📈time plot](bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.017x slower (HPT: reliability of 94.10%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505-vs-3.13.0rc2.md)
- [📈time plot](bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.087x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.22x
- [🧠memory plot](bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505-vs-base-mem.svg)
- [📄table](bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505-vs-base.md)
- [📈time plot](bm-20250620-vultr-x86_64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15790092754)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250620-macm4pro-arm64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505.json)

### vs. 3.12.6

- Geometric mean: 1.096x faster (HPT: reliability of 97.56%, 1.00x faster at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250620-macm4pro-arm64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505-vs-3.12.6.md)
- [📈time plot](bm-20250620-macm4pro-arm64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.017x faster (HPT: reliability of 71.50%, 1.00x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250620-macm4pro-arm64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505-vs-3.13.0rc2.md)
- [📈time plot](bm-20250620-macm4pro-arm64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.008x slower (HPT: reliability of 94.66%, 1.00x slower at 99th %ile)
- Memory usage: 1.13x
- [🧠memory plot](bm-20250620-macm4pro-arm64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505-vs-base-mem.svg)
- [📄table](bm-20250620-macm4pro-arm64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505-vs-base.md)
- [📈time plot](bm-20250620-macm4pro-arm64-python-4ddf505d9982dc8afead-3.15.0a0-4ddf505-vs-base.svg)

