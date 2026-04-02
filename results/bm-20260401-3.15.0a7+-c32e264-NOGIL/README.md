# Results

- fork: python/c32e264227b1fee3a643
- version: 3.15.0a7+
- config: NOGIL
- commit hash: [c32e264](https://github.com/python/cpython/commit/c32e264)
- commit date: 2026-04-01T22:54:06Z
- commit merge base: [b456cb25a98985bdbce6987a37f01da4e2ed478e](https://github.com/python/cpython/commit/b456cb25a98985bdbce6987a37f01da4e2ed478e)
- commit date: 2026-04-01T22:54:06+00:00
- ref: c32e264227b1fee3a643

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/23877884215)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260401-vultr-x86_64-python-c32e264227b1fee3a643-3.15.0a7%2B-c32e264.json)

### vs. 3.12.6

- Geometric mean: 1.026x slower (HPT: reliability of 69.61%, 1.00x slower at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260401-vultr-x86_64-python-c32e264227b1fee3a643-3.15.0a7%2B-c32e264-vs-3.12.6.md)
- [📈time plot](bm-20260401-vultr-x86_64-python-c32e264227b1fee3a643-3.15.0a7%2B-c32e264-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.058x slower (HPT: reliability of 89.81%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260401-vultr-x86_64-python-c32e264227b1fee3a643-3.15.0a7%2B-c32e264-vs-3.13.0rc2.md)
- [📈time plot](bm-20260401-vultr-x86_64-python-c32e264227b1fee3a643-3.15.0a7%2B-c32e264-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.106x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20260401-vultr-x86_64-python-c32e264227b1fee3a643-3.15.0a7%2B-c32e264-vs-base-mem.svg)
- [📄table](bm-20260401-vultr-x86_64-python-c32e264227b1fee3a643-3.15.0a7%2B-c32e264-vs-base.md)
- [📈time plot](bm-20260401-vultr-x86_64-python-c32e264227b1fee3a643-3.15.0a7%2B-c32e264-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/23877884215)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260401-macm4pro-arm64-python-c32e264227b1fee3a643-3.15.0a7%2B-c32e264.json)

### vs. 3.12.6

- Geometric mean: 1.097x faster (HPT: reliability of 99.48%, 1.00x faster at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260401-macm4pro-arm64-python-c32e264227b1fee3a643-3.15.0a7%2B-c32e264-vs-3.12.6.md)
- [📈time plot](bm-20260401-macm4pro-arm64-python-c32e264227b1fee3a643-3.15.0a7%2B-c32e264-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.018x faster (HPT: reliability of 52.81%, 1.00x faster at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260401-macm4pro-arm64-python-c32e264227b1fee3a643-3.15.0a7%2B-c32e264-vs-3.13.0rc2.md)
- [📈time plot](bm-20260401-macm4pro-arm64-python-c32e264227b1fee3a643-3.15.0a7%2B-c32e264-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.051x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20260401-macm4pro-arm64-python-c32e264227b1fee3a643-3.15.0a7%2B-c32e264-vs-base-mem.svg)
- [📄table](bm-20260401-macm4pro-arm64-python-c32e264227b1fee3a643-3.15.0a7%2B-c32e264-vs-base.md)
- [📈time plot](bm-20260401-macm4pro-arm64-python-c32e264227b1fee3a643-3.15.0a7%2B-c32e264-vs-base.svg)

