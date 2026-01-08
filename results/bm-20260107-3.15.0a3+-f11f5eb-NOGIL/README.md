# Results

- fork: python/f11f5ebfe6614de23918
- version: 3.15.0a3+
- config: NOGIL
- commit hash: [f11f5eb](https://github.com/python/cpython/commit/f11f5eb)
- commit date: 2026-01-07T17:56:14-05:00
- commit merge base: [228d95582e080c60335d5f0a229a6698eb69b11c](https://github.com/python/cpython/commit/228d95582e080c60335d5f0a229a6698eb69b11c)
- ref: f11f5ebfe6614de23918

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20801184063)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260107-vultr-x86_64-python-f11f5ebfe6614de23918-3.15.0a3%2B-f11f5eb.json)

### vs. 3.12.6

- Geometric mean: 1.031x slower (HPT: reliability of 75.21%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260107-vultr-x86_64-python-f11f5ebfe6614de23918-3.15.0a3%2B-f11f5eb-vs-3.12.6.md)
- [📈time plot](bm-20260107-vultr-x86_64-python-f11f5ebfe6614de23918-3.15.0a3%2B-f11f5eb-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.064x slower (HPT: reliability of 91.34%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260107-vultr-x86_64-python-f11f5ebfe6614de23918-3.15.0a3%2B-f11f5eb-vs-3.13.0rc2.md)
- [📈time plot](bm-20260107-vultr-x86_64-python-f11f5ebfe6614de23918-3.15.0a3%2B-f11f5eb-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.099x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20260107-vultr-x86_64-python-f11f5ebfe6614de23918-3.15.0a3%2B-f11f5eb-vs-base-mem.svg)
- [📄table](bm-20260107-vultr-x86_64-python-f11f5ebfe6614de23918-3.15.0a3%2B-f11f5eb-vs-base.md)
- [📈time plot](bm-20260107-vultr-x86_64-python-f11f5ebfe6614de23918-3.15.0a3%2B-f11f5eb-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20801184063)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260107-macm4pro-arm64-python-f11f5ebfe6614de23918-3.15.0a3%2B-f11f5eb.json)

### vs. 3.12.6

- Geometric mean: 1.081x faster (HPT: reliability of 96.52%, 1.00x faster at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260107-macm4pro-arm64-python-f11f5ebfe6614de23918-3.15.0a3%2B-f11f5eb-vs-3.12.6.md)
- [📈time plot](bm-20260107-macm4pro-arm64-python-f11f5ebfe6614de23918-3.15.0a3%2B-f11f5eb-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.002x faster (HPT: reliability of 78.76%, 1.00x slower at 99th %ile)
- Memory usage: 1.30x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260107-macm4pro-arm64-python-f11f5ebfe6614de23918-3.15.0a3%2B-f11f5eb-vs-3.13.0rc2.md)
- [📈time plot](bm-20260107-macm4pro-arm64-python-f11f5ebfe6614de23918-3.15.0a3%2B-f11f5eb-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.070x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.11x
- [🧠memory plot](bm-20260107-macm4pro-arm64-python-f11f5ebfe6614de23918-3.15.0a3%2B-f11f5eb-vs-base-mem.svg)
- [📄table](bm-20260107-macm4pro-arm64-python-f11f5ebfe6614de23918-3.15.0a3%2B-f11f5eb-vs-base.md)
- [📈time plot](bm-20260107-macm4pro-arm64-python-f11f5ebfe6614de23918-3.15.0a3%2B-f11f5eb-vs-base.svg)

