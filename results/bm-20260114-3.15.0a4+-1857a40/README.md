# Results

- fork: python/1857a40807daeae3a1bf
- version: 3.15.0a4+
- config: 
- commit hash: [1857a40](https://github.com/python/cpython/commit/1857a40)
- commit date: 2026-01-14T06:03:04+08:00
- commit merge base: [2873c31edf2d5a93fef4f8b667e6a16088ab2ad6](https://github.com/python/cpython/commit/2873c31edf2d5a93fef4f8b667e6a16088ab2ad6)
- ref: 1857a40807daeae3a1bf

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20977753672)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260114-vultr-x86_64-python-1857a40807daeae3a1bf-3.15.0a4%2B-1857a40.json)

### vs. 3.12.6

- Geometric mean: 1.076x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260114-vultr-x86_64-python-1857a40807daeae3a1bf-3.15.0a4%2B-1857a40-vs-3.12.6.md)
- [📈time plot](bm-20260114-vultr-x86_64-python-1857a40807daeae3a1bf-3.15.0a4%2B-1857a40-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.040x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260114-vultr-x86_64-python-1857a40807daeae3a1bf-3.15.0a4%2B-1857a40-vs-3.13.0rc2.md)
- [📈time plot](bm-20260114-vultr-x86_64-python-1857a40807daeae3a1bf-3.15.0a4%2B-1857a40-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20977753672)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260114-macm4pro-arm64-python-1857a40807daeae3a1bf-3.15.0a4%2B-1857a40.json)

### vs. 3.12.6

- Geometric mean: 1.158x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260114-macm4pro-arm64-python-1857a40807daeae3a1bf-3.15.0a4%2B-1857a40-vs-3.12.6.md)
- [📈time plot](bm-20260114-macm4pro-arm64-python-1857a40807daeae3a1bf-3.15.0a4%2B-1857a40-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.074x faster (HPT: reliability of 99.98%, 1.01x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260114-macm4pro-arm64-python-1857a40807daeae3a1bf-3.15.0a4%2B-1857a40-vs-3.13.0rc2.md)
- [📈time plot](bm-20260114-macm4pro-arm64-python-1857a40807daeae3a1bf-3.15.0a4%2B-1857a40-vs-3.13.0rc2.svg)

