# Results

- fork: python/24e5a55ccb0c5db68136
- version: 3.16.0a0
- config: NOGIL
- commit hash: [24e5a55](https://github.com/python/cpython/commit/24e5a55)
- commit date: 2026-08-27T21:11:05+01:00
- commit merge base: [45e5b1b0a97795e2ac82a306ce366efd55bd15b4](https://github.com/python/cpython/commit/45e5b1b0a97795e2ac82a306ce366efd55bd15b4)
- ref: 24e5a55ccb0c5db68136

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/33137988342)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260827-vultr-x86_64-python-24e5a55ccb0c5db68136-3.16.0a0-24e5a55.json)

### vs. 3.12.6

- Geometric mean: 1.041x slower (HPT: reliability of 90.02%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260827-vultr-x86_64-python-24e5a55ccb0c5db68136-3.16.0a0-24e5a55-vs-3.12.6.md)
- [📈time plot](bm-20260827-vultr-x86_64-python-24e5a55ccb0c5db68136-3.16.0a0-24e5a55-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.074x slower (HPT: reliability of 97.88%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260827-vultr-x86_64-python-24e5a55ccb0c5db68136-3.16.0a0-24e5a55-vs-3.13.0rc2.md)
- [📈time plot](bm-20260827-vultr-x86_64-python-24e5a55ccb0c5db68136-3.16.0a0-24e5a55-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.106x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20260827-vultr-x86_64-python-24e5a55ccb0c5db68136-3.16.0a0-24e5a55-vs-base-mem.svg)
- [📄table](bm-20260827-vultr-x86_64-python-24e5a55ccb0c5db68136-3.16.0a0-24e5a55-vs-base.md)
- [📈time plot](bm-20260827-vultr-x86_64-python-24e5a55ccb0c5db68136-3.16.0a0-24e5a55-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/33137988342)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260827-macm4pro-arm64-python-24e5a55ccb0c5db68136-3.16.0a0-24e5a55.json)

### vs. 3.12.6

- Geometric mean: 1.020x faster (HPT: reliability of 65.15%, 1.00x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260827-macm4pro-arm64-python-24e5a55ccb0c5db68136-3.16.0a0-24e5a55-vs-3.12.6.md)
- [📈time plot](bm-20260827-macm4pro-arm64-python-24e5a55ccb0c5db68136-3.16.0a0-24e5a55-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.055x slower (HPT: reliability of 99.39%, 1.00x slower at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260827-macm4pro-arm64-python-24e5a55ccb0c5db68136-3.16.0a0-24e5a55-vs-3.13.0rc2.md)
- [📈time plot](bm-20260827-macm4pro-arm64-python-24e5a55ccb0c5db68136-3.16.0a0-24e5a55-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.103x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.11x
- new benchmarks: coverage
- [🧠memory plot](bm-20260827-macm4pro-arm64-python-24e5a55ccb0c5db68136-3.16.0a0-24e5a55-vs-base-mem.svg)
- [📄table](bm-20260827-macm4pro-arm64-python-24e5a55ccb0c5db68136-3.16.0a0-24e5a55-vs-base.md)
- [📈time plot](bm-20260827-macm4pro-arm64-python-24e5a55ccb0c5db68136-3.16.0a0-24e5a55-vs-base.svg)

