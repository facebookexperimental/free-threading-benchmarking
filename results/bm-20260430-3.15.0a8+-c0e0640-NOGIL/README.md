# Results

- fork: python/c0e064003954142b4ba8
- version: 3.15.0a8+
- config: NOGIL
- commit hash: [c0e0640](https://github.com/python/cpython/commit/c0e0640)
- commit date: 2026-04-30T22:09:36Z
- commit merge base: [bdbb55c403d2ab6b4b0a3e994d21b623fee4a544](https://github.com/python/cpython/commit/bdbb55c403d2ab6b4b0a3e994d21b623fee4a544)
- commit date: 2026-04-30T22:09:36+00:00
- ref: c0e064003954142b4ba8

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/25197031846)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260430-vultr-x86_64-python-c0e064003954142b4ba8-3.15.0a8%2B-c0e0640.json)

### vs. 3.12.6

- Geometric mean: 1.014x slower (HPT: reliability of 60.89%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260430-vultr-x86_64-python-c0e064003954142b4ba8-3.15.0a8%2B-c0e0640-vs-3.12.6.md)
- [📈time plot](bm-20260430-vultr-x86_64-python-c0e064003954142b4ba8-3.15.0a8%2B-c0e0640-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.046x slower (HPT: reliability of 79.37%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260430-vultr-x86_64-python-c0e064003954142b4ba8-3.15.0a8%2B-c0e0640-vs-3.13.0rc2.md)
- [📈time plot](bm-20260430-vultr-x86_64-python-c0e064003954142b4ba8-3.15.0a8%2B-c0e0640-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.081x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20260430-vultr-x86_64-python-c0e064003954142b4ba8-3.15.0a8%2B-c0e0640-vs-base-mem.svg)
- [📄table](bm-20260430-vultr-x86_64-python-c0e064003954142b4ba8-3.15.0a8%2B-c0e0640-vs-base.md)
- [📈time plot](bm-20260430-vultr-x86_64-python-c0e064003954142b4ba8-3.15.0a8%2B-c0e0640-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/25197031846)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260430-macm4pro-arm64-python-c0e064003954142b4ba8-3.15.0a8%2B-c0e0640.json)

### vs. 3.12.6

- Geometric mean: 1.110x faster (HPT: reliability of 99.81%, 1.01x faster at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260430-macm4pro-arm64-python-c0e064003954142b4ba8-3.15.0a8%2B-c0e0640-vs-3.12.6.md)
- [📈time plot](bm-20260430-macm4pro-arm64-python-c0e064003954142b4ba8-3.15.0a8%2B-c0e0640-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.029x faster (HPT: reliability of 68.33%, 1.00x faster at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260430-macm4pro-arm64-python-c0e064003954142b4ba8-3.15.0a8%2B-c0e0640-vs-3.13.0rc2.md)
- [📈time plot](bm-20260430-macm4pro-arm64-python-c0e064003954142b4ba8-3.15.0a8%2B-c0e0640-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.024x slower (HPT: reliability of 99.83%, 1.01x slower at 99th %ile)
- Memory usage: 1.14x
- [🧠memory plot](bm-20260430-macm4pro-arm64-python-c0e064003954142b4ba8-3.15.0a8%2B-c0e0640-vs-base-mem.svg)
- [📄table](bm-20260430-macm4pro-arm64-python-c0e064003954142b4ba8-3.15.0a8%2B-c0e0640-vs-base.md)
- [📈time plot](bm-20260430-macm4pro-arm64-python-c0e064003954142b4ba8-3.15.0a8%2B-c0e0640-vs-base.svg)

