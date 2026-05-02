# Results

- fork: python/be9c7cb4b50f8007b610
- version: 3.15.0a8+
- config: 
- commit hash: [be9c7cb](https://github.com/python/cpython/commit/be9c7cb)
- commit date: 2026-05-01T16:51:06-07:00
- commit merge base: [bb911a2319365a4155e7398b4b7978589d8bed49](https://github.com/python/cpython/commit/bb911a2319365a4155e7398b4b7978589d8bed49)
- ref: be9c7cb4b50f8007b610

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/25239568048)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260501-vultr-x86_64-python-be9c7cb4b50f8007b610-3.15.0a8%2B-be9c7cb.json)

### vs. 3.12.6

- Geometric mean: 1.046x faster (HPT: reliability of 99.98%, 1.02x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260501-vultr-x86_64-python-be9c7cb4b50f8007b610-3.15.0a8%2B-be9c7cb-vs-3.12.6.md)
- [📈time plot](bm-20260501-vultr-x86_64-python-be9c7cb4b50f8007b610-3.15.0a8%2B-be9c7cb-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.011x faster (HPT: reliability of 98.84%, 1.00x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260501-vultr-x86_64-python-be9c7cb4b50f8007b610-3.15.0a8%2B-be9c7cb-vs-3.13.0rc2.md)
- [📈time plot](bm-20260501-vultr-x86_64-python-be9c7cb4b50f8007b610-3.15.0a8%2B-be9c7cb-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/25239568048)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260501-macm4pro-arm64-python-be9c7cb4b50f8007b610-3.15.0a8%2B-be9c7cb.json)

### vs. 3.12.6

- Geometric mean: 1.128x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260501-macm4pro-arm64-python-be9c7cb4b50f8007b610-3.15.0a8%2B-be9c7cb-vs-3.12.6.md)
- [📈time plot](bm-20260501-macm4pro-arm64-python-be9c7cb4b50f8007b610-3.15.0a8%2B-be9c7cb-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.046x faster (HPT: reliability of 99.92%, 1.00x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260501-macm4pro-arm64-python-be9c7cb4b50f8007b610-3.15.0a8%2B-be9c7cb-vs-3.13.0rc2.md)
- [📈time plot](bm-20260501-macm4pro-arm64-python-be9c7cb4b50f8007b610-3.15.0a8%2B-be9c7cb-vs-3.13.0rc2.svg)

