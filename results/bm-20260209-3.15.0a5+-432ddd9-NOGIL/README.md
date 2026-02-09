# Results

- fork: python/432ddd99e2b06a75a4f4
- version: 3.15.0a5+
- config: NOGIL
- commit hash: [432ddd9](https://github.com/python/cpython/commit/432ddd9)
- commit date: 2026-02-09T00:10:43+02:00
- commit merge base: [3dd7a3c65ad4ac330ad44a519efa017484530e1a](https://github.com/python/cpython/commit/3dd7a3c65ad4ac330ad44a519efa017484530e1a)
- ref: 432ddd99e2b06a75a4f4

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21808436742)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260209-vultr-x86_64-python-432ddd99e2b06a75a4f4-3.15.0a5%2B-432ddd9.json)

### vs. 3.12.6

- Geometric mean: 1.033x slower (HPT: reliability of 83.73%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260209-vultr-x86_64-python-432ddd99e2b06a75a4f4-3.15.0a5%2B-432ddd9-vs-3.12.6.md)
- [📈time plot](bm-20260209-vultr-x86_64-python-432ddd99e2b06a75a4f4-3.15.0a5%2B-432ddd9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.065x slower (HPT: reliability of 94.75%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260209-vultr-x86_64-python-432ddd99e2b06a75a4f4-3.15.0a5%2B-432ddd9-vs-3.13.0rc2.md)
- [📈time plot](bm-20260209-vultr-x86_64-python-432ddd99e2b06a75a4f4-3.15.0a5%2B-432ddd9-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.108x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20260209-vultr-x86_64-python-432ddd99e2b06a75a4f4-3.15.0a5%2B-432ddd9-vs-base-mem.svg)
- [📄table](bm-20260209-vultr-x86_64-python-432ddd99e2b06a75a4f4-3.15.0a5%2B-432ddd9-vs-base.md)
- [📈time plot](bm-20260209-vultr-x86_64-python-432ddd99e2b06a75a4f4-3.15.0a5%2B-432ddd9-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21808436742)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260209-macm4pro-arm64-python-432ddd99e2b06a75a4f4-3.15.0a5%2B-432ddd9.json)

### vs. 3.12.6

- Geometric mean: 1.107x faster (HPT: reliability of 99.98%, 1.02x faster at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260209-macm4pro-arm64-python-432ddd99e2b06a75a4f4-3.15.0a5%2B-432ddd9-vs-3.12.6.md)
- [📈time plot](bm-20260209-macm4pro-arm64-python-432ddd99e2b06a75a4f4-3.15.0a5%2B-432ddd9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.027x faster (HPT: reliability of 69.32%, 1.00x faster at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260209-macm4pro-arm64-python-432ddd99e2b06a75a4f4-3.15.0a5%2B-432ddd9-vs-3.13.0rc2.md)
- [📈time plot](bm-20260209-macm4pro-arm64-python-432ddd99e2b06a75a4f4-3.15.0a5%2B-432ddd9-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.056x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.11x
- [🧠memory plot](bm-20260209-macm4pro-arm64-python-432ddd99e2b06a75a4f4-3.15.0a5%2B-432ddd9-vs-base-mem.svg)
- [📄table](bm-20260209-macm4pro-arm64-python-432ddd99e2b06a75a4f4-3.15.0a5%2B-432ddd9-vs-base.md)
- [📈time plot](bm-20260209-macm4pro-arm64-python-432ddd99e2b06a75a4f4-3.15.0a5%2B-432ddd9-vs-base.svg)

