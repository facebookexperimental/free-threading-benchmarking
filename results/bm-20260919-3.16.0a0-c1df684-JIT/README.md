# Results

- fork: python/c1df6843d36233ec1da7
- version: 3.16.0a0
- config: JIT
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

- Geometric mean: 1.156x faster (HPT: reliability of 100.00%, 1.08x faster at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260919-vultr-x86_64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684-vs-3.12.6.md)
- [📈time plot](bm-20260919-vultr-x86_64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.118x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260919-vultr-x86_64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684-vs-3.13.0rc2.md)
- [📈time plot](bm-20260919-vultr-x86_64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.077x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.05x
- [🧠memory plot](bm-20260919-vultr-x86_64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684-vs-base-mem.svg)
- [📄table](bm-20260919-vultr-x86_64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684-vs-base.md)
- [📈time plot](bm-20260919-vultr-x86_64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/35478571947)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684.json)

### vs. 3.12.6

- Geometric mean: 1.239x faster (HPT: reliability of 100.00%, 1.11x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684-vs-3.12.6.md)
- [📈time plot](bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.145x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684-vs-3.13.0rc2.md)
- [📈time plot](bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.100x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.05x
- [🧠memory plot](bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684-vs-base-mem.svg)
- [📄table](bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684-vs-base.md)
- [📈time plot](bm-20260919-macm4pro-arm64-python-c1df6843d36233ec1da7-3.16.0a0-c1df684-vs-base.svg)

