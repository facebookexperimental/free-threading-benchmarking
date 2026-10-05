# Results

- fork: python/7d25916b41de4fc28e04
- version: 3.16.0a0
- config: NOGIL
- commit hash: [7d25916](https://github.com/python/cpython/commit/7d25916)
- commit date: 2026-10-05T00:37:21Z
- commit merge base: [e0861c6ae70c7e6f16c28399bd2b28c521e11e84](https://github.com/python/cpython/commit/e0861c6ae70c7e6f16c28399bd2b28c521e11e84)
- commit date: 2026-10-05T00:37:21+00:00
- ref: 7d25916b41de4fc28e04

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/37248935473)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261005-vultr-x86_64-python-7d25916b41de4fc28e04-3.16.0a0-7d25916.json)

### vs. 3.12.6

- Geometric mean: 1.049x slower (HPT: reliability of 94.70%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261005-vultr-x86_64-python-7d25916b41de4fc28e04-3.16.0a0-7d25916-vs-3.12.6.md)
- [📈time plot](bm-20261005-vultr-x86_64-python-7d25916b41de4fc28e04-3.16.0a0-7d25916-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.082x slower (HPT: reliability of 99.74%, 1.01x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261005-vultr-x86_64-python-7d25916b41de4fc28e04-3.16.0a0-7d25916-vs-3.13.0rc2.md)
- [📈time plot](bm-20261005-vultr-x86_64-python-7d25916b41de4fc28e04-3.16.0a0-7d25916-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.111x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20261005-vultr-x86_64-python-7d25916b41de4fc28e04-3.16.0a0-7d25916-vs-base-mem.svg)
- [📄table](bm-20261005-vultr-x86_64-python-7d25916b41de4fc28e04-3.16.0a0-7d25916-vs-base.md)
- [📈time plot](bm-20261005-vultr-x86_64-python-7d25916b41de4fc28e04-3.16.0a0-7d25916-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/37248935473)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261005-macm4pro-arm64-python-7d25916b41de4fc28e04-3.16.0a0-7d25916.json)

### vs. 3.12.6

- Geometric mean: 1.080x faster (HPT: reliability of 98.17%, 1.00x faster at 99th %ile)
- Memory usage: 1.28x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261005-macm4pro-arm64-python-7d25916b41de4fc28e04-3.16.0a0-7d25916-vs-3.12.6.md)
- [📈time plot](bm-20261005-macm4pro-arm64-python-7d25916b41de4fc28e04-3.16.0a0-7d25916-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.000x faster (HPT: reliability of 74.85%, 1.00x slower at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261005-macm4pro-arm64-python-7d25916b41de4fc28e04-3.16.0a0-7d25916-vs-3.13.0rc2.md)
- [📈time plot](bm-20261005-macm4pro-arm64-python-7d25916b41de4fc28e04-3.16.0a0-7d25916-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.068x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.12x
- new benchmarks: coverage
- [🧠memory plot](bm-20261005-macm4pro-arm64-python-7d25916b41de4fc28e04-3.16.0a0-7d25916-vs-base-mem.svg)
- [📄table](bm-20261005-macm4pro-arm64-python-7d25916b41de4fc28e04-3.16.0a0-7d25916-vs-base.md)
- [📈time plot](bm-20261005-macm4pro-arm64-python-7d25916b41de4fc28e04-3.16.0a0-7d25916-vs-base.svg)

