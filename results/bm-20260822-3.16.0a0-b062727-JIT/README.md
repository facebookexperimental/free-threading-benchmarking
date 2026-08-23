# Results

- fork: python/b062727097e997bcb900
- version: 3.16.0a0
- config: JIT
- commit hash: [b062727](https://github.com/python/cpython/commit/b062727)
- commit date: 2026-08-22T19:45:59+01:00
- commit merge base: [6f42535b333b6d2d56ba2b27e436c37e8ae63a02](https://github.com/python/cpython/commit/6f42535b333b6d2d56ba2b27e436c37e8ae63a02)
- ref: b062727097e997bcb900

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/32607113629)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260822-vultr-x86_64-python-b062727097e997bcb900-3.16.0a0-b062727.json)

### vs. 3.12.6

- Geometric mean: 1.161x faster (HPT: reliability of 100.00%, 1.08x faster at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260822-vultr-x86_64-python-b062727097e997bcb900-3.16.0a0-b062727-vs-3.12.6.md)
- [📈time plot](bm-20260822-vultr-x86_64-python-b062727097e997bcb900-3.16.0a0-b062727-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.123x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260822-vultr-x86_64-python-b062727097e997bcb900-3.16.0a0-b062727-vs-3.13.0rc2.md)
- [📈time plot](bm-20260822-vultr-x86_64-python-b062727097e997bcb900-3.16.0a0-b062727-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.080x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.05x
- [🧠memory plot](bm-20260822-vultr-x86_64-python-b062727097e997bcb900-3.16.0a0-b062727-vs-base-mem.svg)
- [📄table](bm-20260822-vultr-x86_64-python-b062727097e997bcb900-3.16.0a0-b062727-vs-base.md)
- [📈time plot](bm-20260822-vultr-x86_64-python-b062727097e997bcb900-3.16.0a0-b062727-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/32607113629)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260822-macm4pro-arm64-python-b062727097e997bcb900-3.16.0a0-b062727.json)

### vs. 3.12.6

- Geometric mean: 1.249x faster (HPT: reliability of 100.00%, 1.13x faster at 99th %ile)
- Memory usage: 1.24x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260822-macm4pro-arm64-python-b062727097e997bcb900-3.16.0a0-b062727-vs-3.12.6.md)
- [📈time plot](bm-20260822-macm4pro-arm64-python-b062727097e997bcb900-3.16.0a0-b062727-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.154x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260822-macm4pro-arm64-python-b062727097e997bcb900-3.16.0a0-b062727-vs-3.13.0rc2.md)
- [📈time plot](bm-20260822-macm4pro-arm64-python-b062727097e997bcb900-3.16.0a0-b062727-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.100x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.05x
- [🧠memory plot](bm-20260822-macm4pro-arm64-python-b062727097e997bcb900-3.16.0a0-b062727-vs-base-mem.svg)
- [📄table](bm-20260822-macm4pro-arm64-python-b062727097e997bcb900-3.16.0a0-b062727-vs-base.md)
- [📈time plot](bm-20260822-macm4pro-arm64-python-b062727097e997bcb900-3.16.0a0-b062727-vs-base.svg)

