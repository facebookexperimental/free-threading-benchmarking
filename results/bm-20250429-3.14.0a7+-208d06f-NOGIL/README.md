# Results

- fork: python/208d06fd515119af49f8
- version: 3.14.0a7+
- config: NOGIL
- commit hash: [208d06f](https://github.com/python/cpython/commit/208d06f)
- commit date: 2025-04-29T08:53:43Z
- commit merge base: [4d54e9cdf6968559da3c428dfb88cbf6ce7e3c18](https://github.com/python/cpython/commit/4d54e9cdf6968559da3c428dfb88cbf6ce7e3c18)
- commit date: 2025-04-29T08:53:43+00:00
- ref: 208d06fd515119af49f8

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14732101454)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250429-vultr-x86_64-python-208d06fd515119af49f8-3.14.0a7%2B-208d06f.json)

### vs. 3.12.6

- Geometric mean: 1.031x faster (HPT: reliability of 62.11%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250429-vultr-x86_64-python-208d06fd515119af49f8-3.14.0a7%2B-208d06f-vs-3.12.6.md)
- [📈time plot](bm-20250429-vultr-x86_64-python-208d06fd515119af49f8-3.14.0a7%2B-208d06f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.002x slower (HPT: reliability of 85.44%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250429-vultr-x86_64-python-208d06fd515119af49f8-3.14.0a7%2B-208d06f-vs-3.13.0rc2.md)
- [📈time plot](bm-20250429-vultr-x86_64-python-208d06fd515119af49f8-3.14.0a7%2B-208d06f-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.081x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.19x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250429-vultr-x86_64-python-208d06fd515119af49f8-3.14.0a7%2B-208d06f-vs-base-mem.svg)
- [📄table](bm-20250429-vultr-x86_64-python-208d06fd515119af49f8-3.14.0a7%2B-208d06f-vs-base.md)
- [📈time plot](bm-20250429-vultr-x86_64-python-208d06fd515119af49f8-3.14.0a7%2B-208d06f-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14732101454)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250429-macm4pro-arm64-python-208d06fd515119af49f8-3.14.0a7%2B-208d06f.json)

### vs. 3.12.6

- Geometric mean: 1.087x faster (HPT: reliability of 89.92%, 1.00x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250429-macm4pro-arm64-python-208d06fd515119af49f8-3.14.0a7%2B-208d06f-vs-3.12.6.md)
- [📈time plot](bm-20250429-macm4pro-arm64-python-208d06fd515119af49f8-3.14.0a7%2B-208d06f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.008x faster (HPT: reliability of 86.32%, 1.00x slower at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250429-macm4pro-arm64-python-208d06fd515119af49f8-3.14.0a7%2B-208d06f-vs-3.13.0rc2.md)
- [📈time plot](bm-20250429-macm4pro-arm64-python-208d06fd515119af49f8-3.14.0a7%2B-208d06f-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.008x slower (HPT: reliability of 99.10%, 1.00x slower at 99th %ile)
- Memory usage: 1.10x
- [🧠memory plot](bm-20250429-macm4pro-arm64-python-208d06fd515119af49f8-3.14.0a7%2B-208d06f-vs-base-mem.svg)
- [📄table](bm-20250429-macm4pro-arm64-python-208d06fd515119af49f8-3.14.0a7%2B-208d06f-vs-base.md)
- [📈time plot](bm-20250429-macm4pro-arm64-python-208d06fd515119af49f8-3.14.0a7%2B-208d06f-vs-base.svg)

