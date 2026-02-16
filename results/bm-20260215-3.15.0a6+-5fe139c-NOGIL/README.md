# Results

- fork: python/5fe139cc39fb8110b3d6
- version: 3.15.0a6+
- config: NOGIL
- commit hash: [5fe139c](https://github.com/python/cpython/commit/5fe139c)
- commit date: 2026-02-15T18:36:47Z
- commit merge base: [23c488d6197191d355be6733699a295c20806932](https://github.com/python/cpython/commit/23c488d6197191d355be6733699a295c20806932)
- commit date: 2026-02-15T18:36:47+00:00
- ref: 5fe139cc39fb8110b3d6

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/22046216888)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260215-vultr-x86_64-python-5fe139cc39fb8110b3d6-3.15.0a6%2B-5fe139c.json)

### vs. 3.12.6

- Geometric mean: 1.031x slower (HPT: reliability of 88.00%, 1.00x slower at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260215-vultr-x86_64-python-5fe139cc39fb8110b3d6-3.15.0a6%2B-5fe139c-vs-3.12.6.md)
- [📈time plot](bm-20260215-vultr-x86_64-python-5fe139cc39fb8110b3d6-3.15.0a6%2B-5fe139c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.064x slower (HPT: reliability of 95.61%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260215-vultr-x86_64-python-5fe139cc39fb8110b3d6-3.15.0a6%2B-5fe139c-vs-3.13.0rc2.md)
- [📈time plot](bm-20260215-vultr-x86_64-python-5fe139cc39fb8110b3d6-3.15.0a6%2B-5fe139c-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.106x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20260215-vultr-x86_64-python-5fe139cc39fb8110b3d6-3.15.0a6%2B-5fe139c-vs-base-mem.svg)
- [📄table](bm-20260215-vultr-x86_64-python-5fe139cc39fb8110b3d6-3.15.0a6%2B-5fe139c-vs-base.md)
- [📈time plot](bm-20260215-vultr-x86_64-python-5fe139cc39fb8110b3d6-3.15.0a6%2B-5fe139c-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/22046216888)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260215-macm4pro-arm64-python-5fe139cc39fb8110b3d6-3.15.0a6%2B-5fe139c.json)

### vs. 3.12.6

- Geometric mean: 1.091x faster (HPT: reliability of 99.63%, 1.00x faster at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260215-macm4pro-arm64-python-5fe139cc39fb8110b3d6-3.15.0a6%2B-5fe139c-vs-3.12.6.md)
- [📈time plot](bm-20260215-macm4pro-arm64-python-5fe139cc39fb8110b3d6-3.15.0a6%2B-5fe139c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.012x faster (HPT: reliability of 57.51%, 1.00x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260215-macm4pro-arm64-python-5fe139cc39fb8110b3d6-3.15.0a6%2B-5fe139c-vs-3.13.0rc2.md)
- [📈time plot](bm-20260215-macm4pro-arm64-python-5fe139cc39fb8110b3d6-3.15.0a6%2B-5fe139c-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.061x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.11x
- [🧠memory plot](bm-20260215-macm4pro-arm64-python-5fe139cc39fb8110b3d6-3.15.0a6%2B-5fe139c-vs-base-mem.svg)
- [📄table](bm-20260215-macm4pro-arm64-python-5fe139cc39fb8110b3d6-3.15.0a6%2B-5fe139c-vs-base.md)
- [📈time plot](bm-20260215-macm4pro-arm64-python-5fe139cc39fb8110b3d6-3.15.0a6%2B-5fe139c-vs-base.svg)

