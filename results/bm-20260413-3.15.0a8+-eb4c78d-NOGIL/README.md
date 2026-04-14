# Results

- fork: python/eb4c78df07c87237f97e
- version: 3.15.0a8+
- config: NOGIL
- commit hash: [eb4c78d](https://github.com/python/cpython/commit/eb4c78d)
- commit date: 2026-04-13T23:43:55+01:00
- commit merge base: [2662db0c45aa16232136628457a53681b6683c25](https://github.com/python/cpython/commit/2662db0c45aa16232136628457a53681b6683c25)
- ref: eb4c78df07c87237f97e

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/24374753484)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260413-vultr-x86_64-python-eb4c78df07c87237f97e-3.15.0a8%2B-eb4c78d.json)

### vs. 3.12.6

- Geometric mean: 1.026x slower (HPT: reliability of 60.22%, 1.00x slower at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260413-vultr-x86_64-python-eb4c78df07c87237f97e-3.15.0a8%2B-eb4c78d-vs-3.12.6.md)
- [📈time plot](bm-20260413-vultr-x86_64-python-eb4c78df07c87237f97e-3.15.0a8%2B-eb4c78d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.059x slower (HPT: reliability of 90.72%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260413-vultr-x86_64-python-eb4c78df07c87237f97e-3.15.0a8%2B-eb4c78d-vs-3.13.0rc2.md)
- [📈time plot](bm-20260413-vultr-x86_64-python-eb4c78df07c87237f97e-3.15.0a8%2B-eb4c78d-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.089x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20260413-vultr-x86_64-python-eb4c78df07c87237f97e-3.15.0a8%2B-eb4c78d-vs-base-mem.svg)
- [📄table](bm-20260413-vultr-x86_64-python-eb4c78df07c87237f97e-3.15.0a8%2B-eb4c78d-vs-base.md)
- [📈time plot](bm-20260413-vultr-x86_64-python-eb4c78df07c87237f97e-3.15.0a8%2B-eb4c78d-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/24374753484)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260413-macm4pro-arm64-python-eb4c78df07c87237f97e-3.15.0a8%2B-eb4c78d.json)

### vs. 3.12.6

- Geometric mean: 1.091x faster (HPT: reliability of 99.41%, 1.00x faster at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260413-macm4pro-arm64-python-eb4c78df07c87237f97e-3.15.0a8%2B-eb4c78d-vs-3.12.6.md)
- [📈time plot](bm-20260413-macm4pro-arm64-python-eb4c78df07c87237f97e-3.15.0a8%2B-eb4c78d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.012x faster (HPT: reliability of 52.96%, 1.00x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260413-macm4pro-arm64-python-eb4c78df07c87237f97e-3.15.0a8%2B-eb4c78d-vs-3.13.0rc2.md)
- [📈time plot](bm-20260413-macm4pro-arm64-python-eb4c78df07c87237f97e-3.15.0a8%2B-eb4c78d-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.052x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: 1.11x
- [🧠memory plot](bm-20260413-macm4pro-arm64-python-eb4c78df07c87237f97e-3.15.0a8%2B-eb4c78d-vs-base-mem.svg)
- [📄table](bm-20260413-macm4pro-arm64-python-eb4c78df07c87237f97e-3.15.0a8%2B-eb4c78d-vs-base.md)
- [📈time plot](bm-20260413-macm4pro-arm64-python-eb4c78df07c87237f97e-3.15.0a8%2B-eb4c78d-vs-base.svg)

