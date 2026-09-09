# Results

- fork: python/f8f8c30ed4e20208e8ba
- version: 3.16.0a0
- config: 
- commit hash: [f8f8c30](https://github.com/python/cpython/commit/f8f8c30)
- commit date: 2026-09-08T20:20:25-04:00
- commit merge base: [2ddc218b20625ef4a6293aee3696e605c6bac5b9](https://github.com/python/cpython/commit/2ddc218b20625ef4a6293aee3696e605c6bac5b9)
- ref: f8f8c30ed4e20208e8ba

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/34296063123)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260908-vultr-x86_64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30.json)

### vs. 3.12.6

- Geometric mean: 1.067x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260908-vultr-x86_64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30-vs-3.12.6.md)
- [📈time plot](bm-20260908-vultr-x86_64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.032x faster (HPT: reliability of 99.92%, 1.00x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260908-vultr-x86_64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30-vs-3.13.0rc2.md)
- [📈time plot](bm-20260908-vultr-x86_64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/34296063123)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30.json)

### vs. 3.12.6

- Geometric mean: 1.145x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30-vs-3.12.6.md)
- [📈time plot](bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.058x faster (HPT: reliability of 99.89%, 1.01x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30-vs-3.13.0rc2.md)
- [📈time plot](bm-20260908-macm4pro-arm64-python-f8f8c30ed4e20208e8ba-3.16.0a0-f8f8c30-vs-3.13.0rc2.svg)

