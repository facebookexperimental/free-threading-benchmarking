# Results

- fork: python/461b1d96313de02992d2
- version: 3.16.0a0
- config: NOGIL
- commit hash: [461b1d9](https://github.com/python/cpython/commit/461b1d9)
- commit date: 2026-05-14T23:10:39+02:00
- commit merge base: [c62c3710dc795a60c3c3dc8e2aeeeb16c06da197](https://github.com/python/cpython/commit/c62c3710dc795a60c3c3dc8e2aeeeb16c06da197)
- ref: 461b1d96313de02992d2

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/25894252972)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260514-vultr-x86_64-python-461b1d96313de02992d2-3.16.0a0-461b1d9.json)

### vs. 3.12.6

- Geometric mean: 1.033x slower (HPT: reliability of 87.30%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260514-vultr-x86_64-python-461b1d96313de02992d2-3.16.0a0-461b1d9-vs-3.12.6.md)
- [📈time plot](bm-20260514-vultr-x86_64-python-461b1d96313de02992d2-3.16.0a0-461b1d9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.068x slower (HPT: reliability of 95.98%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260514-vultr-x86_64-python-461b1d96313de02992d2-3.16.0a0-461b1d9-vs-3.13.0rc2.md)
- [📈time plot](bm-20260514-vultr-x86_64-python-461b1d96313de02992d2-3.16.0a0-461b1d9-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.096x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20260514-vultr-x86_64-python-461b1d96313de02992d2-3.16.0a0-461b1d9-vs-base-mem.svg)
- [📄table](bm-20260514-vultr-x86_64-python-461b1d96313de02992d2-3.16.0a0-461b1d9-vs-base.md)
- [📈time plot](bm-20260514-vultr-x86_64-python-461b1d96313de02992d2-3.16.0a0-461b1d9-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/25894252972)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260514-macm4pro-arm64-python-461b1d96313de02992d2-3.16.0a0-461b1d9.json)

### vs. 3.12.6

- Geometric mean: 1.109x faster (HPT: reliability of 99.84%, 1.01x faster at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: 2to3, asyncio_websockets, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260514-macm4pro-arm64-python-461b1d96313de02992d2-3.16.0a0-461b1d9-vs-3.12.6.md)
- [📈time plot](bm-20260514-macm4pro-arm64-python-461b1d96313de02992d2-3.16.0a0-461b1d9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.023x faster (HPT: reliability of 52.85%, 1.00x faster at 99th %ile)
- Memory usage: 1.30x
- missing benchmarks: 2to3, asyncio_websockets, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260514-macm4pro-arm64-python-461b1d96313de02992d2-3.16.0a0-461b1d9-vs-3.13.0rc2.md)
- [📈time plot](bm-20260514-macm4pro-arm64-python-461b1d96313de02992d2-3.16.0a0-461b1d9-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.023x slower (HPT: reliability of 100.00%, 1.02x slower at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: 🔴 asyncio_websockets
- [🧠memory plot](bm-20260514-macm4pro-arm64-python-461b1d96313de02992d2-3.16.0a0-461b1d9-vs-base-mem.svg)
- [📄table](bm-20260514-macm4pro-arm64-python-461b1d96313de02992d2-3.16.0a0-461b1d9-vs-base.md)
- [📈time plot](bm-20260514-macm4pro-arm64-python-461b1d96313de02992d2-3.16.0a0-461b1d9-vs-base.svg)

