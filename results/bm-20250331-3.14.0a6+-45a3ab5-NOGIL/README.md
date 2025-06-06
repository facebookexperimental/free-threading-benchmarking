# Results

- fork: python/45a3ab5a81769eadd94d
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [45a3ab5](https://github.com/python/cpython/commit/45a3ab5)
- commit date: 2025-03-31T23:13:17+02:00
- commit merge base: [2e96f5ae4d1700d77a53180b4866c5b9f002e62d](https://github.com/python/cpython/commit/2e96f5ae4d1700d77a53180b4866c5b9f002e62d)
- ref: 45a3ab5a81769eadd94d

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14184261824)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250331-vultr-x86_64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5.json)

### vs. 3.12.6

- Geometric mean: 1.089x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250331-vultr-x86_64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5-vs-3.12.6.md)
- [📈time plot](bm-20250331-vultr-x86_64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.119x slower (HPT: reliability of 99.99%, 1.08x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250331-vultr-x86_64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5-vs-3.13.0rc2.md)
- [📈time plot](bm-20250331-vultr-x86_64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.177x slower (HPT: reliability of 100.00%, 1.17x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250331-vultr-x86_64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5-vs-base-mem.svg)
- [📄table](bm-20250331-vultr-x86_64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5-vs-base.md)
- [📈time plot](bm-20250331-vultr-x86_64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14184261824)
- cpu model: missing
- platform: macOS-15.3.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5.json)

### vs. 3.12.6

- Geometric mean: 1.052x slower (HPT: reliability of 99.73%, 1.01x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5-vs-3.12.6.md)
- [📈time plot](bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.121x slower (HPT: reliability of 99.99%, 1.06x slower at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5-vs-3.13.0rc2.md)
- [📈time plot](bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.096x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.10x
- [🧠memory plot](bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5-vs-base-mem.svg)
- [📄table](bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5-vs-base.md)
- [📈time plot](bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6%2B-45a3ab5-vs-base.svg)

