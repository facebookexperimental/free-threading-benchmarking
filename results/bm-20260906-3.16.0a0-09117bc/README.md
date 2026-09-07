# Results

- fork: python/09117bc3173b6854f3d6
- version: 3.16.0a0
- config: 
- commit hash: [09117bc](https://github.com/python/cpython/commit/09117bc)
- commit date: 2026-09-06T21:15:44+01:00
- commit merge base: [878b5e256aa40c45e12a0cd5c63f8a249f7c3704](https://github.com/python/cpython/commit/878b5e256aa40c45e12a0cd5c63f8a249f7c3704)
- ref: 09117bc3173b6854f3d6

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/34070809565)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260906-vultr-x86_64-python-09117bc3173b6854f3d6-3.16.0a0-09117bc.json)

### vs. 3.12.6

- Geometric mean: 1.069x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260906-vultr-x86_64-python-09117bc3173b6854f3d6-3.16.0a0-09117bc-vs-3.12.6.md)
- [📈time plot](bm-20260906-vultr-x86_64-python-09117bc3173b6854f3d6-3.16.0a0-09117bc-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.033x faster (HPT: reliability of 99.98%, 1.00x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260906-vultr-x86_64-python-09117bc3173b6854f3d6-3.16.0a0-09117bc-vs-3.13.0rc2.md)
- [📈time plot](bm-20260906-vultr-x86_64-python-09117bc3173b6854f3d6-3.16.0a0-09117bc-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/34070809565)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260906-macm4pro-arm64-python-09117bc3173b6854f3d6-3.16.0a0-09117bc.json)

### vs. 3.12.6

- Geometric mean: 1.161x faster (HPT: reliability of 100.00%, 1.08x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260906-macm4pro-arm64-python-09117bc3173b6854f3d6-3.16.0a0-09117bc-vs-3.12.6.md)
- [📈time plot](bm-20260906-macm4pro-arm64-python-09117bc3173b6854f3d6-3.16.0a0-09117bc-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.073x faster (HPT: reliability of 99.99%, 1.01x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260906-macm4pro-arm64-python-09117bc3173b6854f3d6-3.16.0a0-09117bc-vs-3.13.0rc2.md)
- [📈time plot](bm-20260906-macm4pro-arm64-python-09117bc3173b6854f3d6-3.16.0a0-09117bc-vs-3.13.0rc2.svg)

