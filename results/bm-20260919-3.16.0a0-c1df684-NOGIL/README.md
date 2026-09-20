# Results

- fork: python/c1df6843d36233ec1da7
- version: 3.16.0a0
- config: NOGIL
- commit hash: [c1df684](https://github.com/python/cpython/commit/c1df684)
- commit date: 2026-09-19T22:04:42Z
- commit merge base: [a1669c95d980f6cabceaaf61e3c49873b5e03efa](https://github.com/python/cpython/commit/a1669c95d980f6cabceaaf61e3c49873b5e03efa)
- commit date: 2026-09-19T22:04:42+00:00
- ref: c1df6843d36233ec1da7

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/35478571947)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260919-vultr-x86_64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684.json)

### vs. 3.12.6

- Geometric mean: 1.049x slower (HPT: reliability of 88.74%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260919-vultr-x86_64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684-vs-3.12.6.md)
- [📈time plot](bm-20260919-vultr-x86_64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.080x slower (HPT: reliability of 99.18%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260919-vultr-x86_64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684-vs-3.13.0rc2.md)
- [📈time plot](bm-20260919-vultr-x86_64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.111x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20260919-vultr-x86_64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684-vs-base-mem.svg)
- [📄table](bm-20260919-vultr-x86_64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684-vs-base.md)
- [📈time plot](bm-20260919-vultr-x86_64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/35478571947)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684.json)

### vs. 3.12.6

- Geometric mean: 1.003x slower (HPT: reliability of 87.22%, 1.00x slower at 99th %ile)
- Memory usage: 1.30x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684-vs-3.12.6.md)
- [📈time plot](bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.077x slower (HPT: reliability of 99.89%, 1.03x slower at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684-vs-3.13.0rc2.md)
- [📈time plot](bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.115x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.12x
- new benchmarks: coverage
- [🧠memory plot](bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684-vs-base-mem.svg)
- [📄table](bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684-vs-base.md)
- [📈time plot](bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684-vs-base.svg)

