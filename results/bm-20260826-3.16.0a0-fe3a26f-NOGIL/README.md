# Results

- fork: python/fe3a26f43fad1d6eed20
- version: 3.16.0a0
- config: NOGIL
- commit hash: [fe3a26f](https://github.com/python/cpython/commit/fe3a26f)
- commit date: 2026-08-26T21:50:41Z
- commit merge base: [7f3d09b6e8018c3710dfde9f71c63d47a047beb1](https://github.com/python/cpython/commit/7f3d09b6e8018c3710dfde9f71c63d47a047beb1)
- commit date: 2026-08-26T21:50:41+00:00
- ref: fe3a26f43fad1d6eed20

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/33031117908)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260826-vultr-x86_64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f.json)

### vs. 3.12.6

- Geometric mean: 1.038x slower (HPT: reliability of 85.51%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260826-vultr-x86_64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f-vs-3.12.6.md)
- [📈time plot](bm-20260826-vultr-x86_64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.070x slower (HPT: reliability of 97.53%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260826-vultr-x86_64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f-vs-3.13.0rc2.md)
- [📈time plot](bm-20260826-vultr-x86_64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.103x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20260826-vultr-x86_64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f-vs-base-mem.svg)
- [📄table](bm-20260826-vultr-x86_64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f-vs-base.md)
- [📈time plot](bm-20260826-vultr-x86_64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/33031117908)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260826-macm4pro-arm64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f.json)

### vs. 3.12.6

- Geometric mean: 1.015x faster (HPT: reliability of 64.86%, 1.00x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260826-macm4pro-arm64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f-vs-3.12.6.md)
- [📈time plot](bm-20260826-macm4pro-arm64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.060x slower (HPT: reliability of 99.62%, 1.01x slower at 99th %ile)
- Memory usage: 1.28x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260826-macm4pro-arm64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f-vs-3.13.0rc2.md)
- [📈time plot](bm-20260826-macm4pro-arm64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.107x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.12x
- new benchmarks: coverage
- [🧠memory plot](bm-20260826-macm4pro-arm64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f-vs-base-mem.svg)
- [📄table](bm-20260826-macm4pro-arm64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f-vs-base.md)
- [📈time plot](bm-20260826-macm4pro-arm64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f-vs-base.svg)

