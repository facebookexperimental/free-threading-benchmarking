# Results

- fork: python/ee521e8ac19ad012ebc4
- version: 3.16.0a0
- config: NOGIL
- commit hash: [ee521e8](https://github.com/python/cpython/commit/ee521e8)
- commit date: 2026-08-24T20:19:30+01:00
- commit merge base: [c3f7c33dd7c6496d474979d5bd7f5dc22103dd22](https://github.com/python/cpython/commit/c3f7c33dd7c6496d474979d5bd7f5dc22103dd22)
- ref: ee521e8ac19ad012ebc4

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/32793018860)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260824-vultr-x86_64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8.json)

### vs. 3.12.6

- Geometric mean: 1.042x slower (HPT: reliability of 90.86%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260824-vultr-x86_64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8-vs-3.12.6.md)
- [📈time plot](bm-20260824-vultr-x86_64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.074x slower (HPT: reliability of 98.34%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260824-vultr-x86_64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8-vs-3.13.0rc2.md)
- [📈time plot](bm-20260824-vultr-x86_64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.107x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20260824-vultr-x86_64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8-vs-base-mem.svg)
- [📄table](bm-20260824-vultr-x86_64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8-vs-base.md)
- [📈time plot](bm-20260824-vultr-x86_64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/32793018860)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260824-macm4pro-arm64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8.json)

### vs. 3.12.6

- Geometric mean: 1.016x faster (HPT: reliability of 74.60%, 1.00x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260824-macm4pro-arm64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8-vs-3.12.6.md)
- [📈time plot](bm-20260824-macm4pro-arm64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.059x slower (HPT: reliability of 99.57%, 1.00x slower at 99th %ile)
- Memory usage: 1.28x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260824-macm4pro-arm64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8-vs-3.13.0rc2.md)
- [📈time plot](bm-20260824-macm4pro-arm64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.112x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.12x
- new benchmarks: coverage
- [🧠memory plot](bm-20260824-macm4pro-arm64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8-vs-base-mem.svg)
- [📄table](bm-20260824-macm4pro-arm64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8-vs-base.md)
- [📈time plot](bm-20260824-macm4pro-arm64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8-vs-base.svg)

