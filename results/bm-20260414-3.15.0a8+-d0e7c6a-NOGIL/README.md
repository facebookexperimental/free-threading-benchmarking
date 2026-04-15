# Results

- fork: python/d0e7c6acc936a171d05b
- version: 3.15.0a8+
- config: NOGIL
- commit hash: [d0e7c6a](https://github.com/python/cpython/commit/d0e7c6a)
- commit date: 2026-04-14T17:15:27-07:00
- commit merge base: [94d42bf5c2b95417d6187a57fef94570ba017e33](https://github.com/python/cpython/commit/94d42bf5c2b95417d6187a57fef94570ba017e33)
- ref: d0e7c6acc936a171d05b

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/24430466353)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260414-vultr-x86_64-python-d0e7c6acc936a171d05b-3.15.0a8%2B-d0e7c6a.json)

### vs. 3.12.6

- Geometric mean: 1.015x slower (HPT: reliability of 71.75%, 1.00x slower at 99th %ile)
- Memory usage: 1.44x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260414-vultr-x86_64-python-d0e7c6acc936a171d05b-3.15.0a8%2B-d0e7c6a-vs-3.12.6.md)
- [📈time plot](bm-20260414-vultr-x86_64-python-d0e7c6acc936a171d05b-3.15.0a8%2B-d0e7c6a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.048x slower (HPT: reliability of 88.19%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260414-vultr-x86_64-python-d0e7c6acc936a171d05b-3.15.0a8%2B-d0e7c6a-vs-3.13.0rc2.md)
- [📈time plot](bm-20260414-vultr-x86_64-python-d0e7c6acc936a171d05b-3.15.0a8%2B-d0e7c6a-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.094x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20260414-vultr-x86_64-python-d0e7c6acc936a171d05b-3.15.0a8%2B-d0e7c6a-vs-base-mem.svg)
- [📄table](bm-20260414-vultr-x86_64-python-d0e7c6acc936a171d05b-3.15.0a8%2B-d0e7c6a-vs-base.md)
- [📈time plot](bm-20260414-vultr-x86_64-python-d0e7c6acc936a171d05b-3.15.0a8%2B-d0e7c6a-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/24430466353)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260414-macm4pro-arm64-python-d0e7c6acc936a171d05b-3.15.0a8%2B-d0e7c6a.json)

### vs. 3.12.6

- Geometric mean: 1.100x faster (HPT: reliability of 99.52%, 1.00x faster at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260414-macm4pro-arm64-python-d0e7c6acc936a171d05b-3.15.0a8%2B-d0e7c6a-vs-3.12.6.md)
- [📈time plot](bm-20260414-macm4pro-arm64-python-d0e7c6acc936a171d05b-3.15.0a8%2B-d0e7c6a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.020x faster (HPT: reliability of 51.92%, 1.00x faster at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260414-macm4pro-arm64-python-d0e7c6acc936a171d05b-3.15.0a8%2B-d0e7c6a-vs-3.13.0rc2.md)
- [📈time plot](bm-20260414-macm4pro-arm64-python-d0e7c6acc936a171d05b-3.15.0a8%2B-d0e7c6a-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.058x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20260414-macm4pro-arm64-python-d0e7c6acc936a171d05b-3.15.0a8%2B-d0e7c6a-vs-base-mem.svg)
- [📄table](bm-20260414-macm4pro-arm64-python-d0e7c6acc936a171d05b-3.15.0a8%2B-d0e7c6a-vs-base.md)
- [📈time plot](bm-20260414-macm4pro-arm64-python-d0e7c6acc936a171d05b-3.15.0a8%2B-d0e7c6a-vs-base.svg)

