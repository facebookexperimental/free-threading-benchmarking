# Results

- fork: python/180b3eb697bf5bb0088f
- version: 3.15.0a0
- config: NOGIL
- commit hash: [180b3eb](https://github.com/python/cpython/commit/180b3eb)
- commit date: 2025-07-16T22:59:30+05:30
- commit merge base: [b7d722547bcc9e92dca4837b9fdbe7457788820b](https://github.com/python/cpython/commit/b7d722547bcc9e92dca4837b9fdbe7457788820b)
- ref: 180b3eb697bf5bb0088f

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16333246852)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250716-vultr-x86_64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb.json)

### vs. 3.12.6

- Geometric mean: 1.021x slower (HPT: reliability of 93.40%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250716-vultr-x86_64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb-vs-3.12.6.md)
- [📈time plot](bm-20250716-vultr-x86_64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.054x slower (HPT: reliability of 96.04%, 1.00x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250716-vultr-x86_64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb-vs-3.13.0rc2.md)
- [📈time plot](bm-20250716-vultr-x86_64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.093x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20250716-vultr-x86_64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb-vs-base-mem.svg)
- [📄table](bm-20250716-vultr-x86_64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb-vs-base.md)
- [📈time plot](bm-20250716-vultr-x86_64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16333246852)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb.json)

### vs. 3.12.6

- Geometric mean: 1.100x faster (HPT: reliability of 97.88%, 1.00x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb-vs-3.12.6.md)
- [📈time plot](bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.021x faster (HPT: reliability of 70.61%, 1.00x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb-vs-3.13.0rc2.md)
- [📈time plot](bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.003x slower (HPT: reliability of 97.17%, 1.00x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb-vs-base-mem.svg)
- [📄table](bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb-vs-base.md)
- [📈time plot](bm-20250716-macm4pro-arm64-python-180b3eb697bf5bb0088f-3.15.0a0-180b3eb-vs-base.svg)

