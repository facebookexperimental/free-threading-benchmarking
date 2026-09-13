# Results

- fork: python/12a1de1a4e22732700cf
- version: 3.16.0a0
- config: NOGIL
- commit hash: [12a1de1](https://github.com/python/cpython/commit/12a1de1)
- commit date: 2026-09-13T00:28:39Z
- commit merge base: [1a703ab9e6a050b40c469788ec7758713c6bf62b](https://github.com/python/cpython/commit/1a703ab9e6a050b40c469788ec7758713c6bf62b)
- commit date: 2026-09-13T00:28:39+00:00
- ref: 12a1de1a4e22732700cf

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/34728802136)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260913-vultr-x86_64-python-12a1de1a4e22732700cf-3.16.0a0-12a1de1.json)

### vs. 3.12.6

- Geometric mean: 1.049x slower (HPT: reliability of 89.84%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260913-vultr-x86_64-python-12a1de1a4e22732700cf-3.16.0a0-12a1de1-vs-3.12.6.md)
- [📈time plot](bm-20260913-vultr-x86_64-python-12a1de1a4e22732700cf-3.16.0a0-12a1de1-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.081x slower (HPT: reliability of 99.06%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260913-vultr-x86_64-python-12a1de1a4e22732700cf-3.16.0a0-12a1de1-vs-3.13.0rc2.md)
- [📈time plot](bm-20260913-vultr-x86_64-python-12a1de1a4e22732700cf-3.16.0a0-12a1de1-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.000x faster (HPT: reliability of 98.88%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: 🔴 asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list
- [🧠memory plot](bm-20260913-vultr-x86_64-python-12a1de1a4e22732700cf-3.16.0a0-12a1de1-vs-base-mem.svg)
- [📄table](bm-20260913-vultr-x86_64-python-12a1de1a4e22732700cf-3.16.0a0-12a1de1-vs-base.md)
- [📈time plot](bm-20260913-vultr-x86_64-python-12a1de1a4e22732700cf-3.16.0a0-12a1de1-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.105x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260913-vultr-x86_64-python-12a1de1a4e22732700cf-3.16.0a0-12a1de1-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20260913-vultr-x86_64-python-12a1de1a4e22732700cf-3.16.0a0-12a1de1-vs-default_base_vs_NOGIL.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/34728802136)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260913-macm4pro-arm64-python-12a1de1a4e22732700cf-3.16.0a0-12a1de1.json)

### vs. 3.12.6

- Geometric mean: 1.003x faster (HPT: reliability of 83.96%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260913-macm4pro-arm64-python-12a1de1a4e22732700cf-3.16.0a0-12a1de1-vs-3.12.6.md)
- [📈time plot](bm-20260913-macm4pro-arm64-python-12a1de1a4e22732700cf-3.16.0a0-12a1de1-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.071x slower (HPT: reliability of 99.83%, 1.02x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260913-macm4pro-arm64-python-12a1de1a4e22732700cf-3.16.0a0-12a1de1-vs-3.13.0rc2.md)
- [📈time plot](bm-20260913-macm4pro-arm64-python-12a1de1a4e22732700cf-3.16.0a0-12a1de1-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.003x faster (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: 🔴 asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list
- [🧠memory plot](bm-20260913-macm4pro-arm64-python-12a1de1a4e22732700cf-3.16.0a0-12a1de1-vs-base-mem.svg)
- [📄table](bm-20260913-macm4pro-arm64-python-12a1de1a4e22732700cf-3.16.0a0-12a1de1-vs-base.md)
- [📈time plot](bm-20260913-macm4pro-arm64-python-12a1de1a4e22732700cf-3.16.0a0-12a1de1-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.110x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list
- new benchmarks: coverage
- [📄table](bm-20260913-macm4pro-arm64-python-12a1de1a4e22732700cf-3.16.0a0-12a1de1-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20260913-macm4pro-arm64-python-12a1de1a4e22732700cf-3.16.0a0-12a1de1-vs-default_base_vs_NOGIL.svg)

