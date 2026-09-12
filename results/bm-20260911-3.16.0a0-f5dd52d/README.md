# Results

- fork: python/f5dd52df16e1b3f3f8cc
- version: 3.16.0a0
- config: 
- commit hash: [f5dd52d](https://github.com/python/cpython/commit/f5dd52d)
- commit date: 2026-09-11T23:22:35Z
- commit merge base: [d9565e54b1fc6d63c5be9afd58114499128fa57b](https://github.com/python/cpython/commit/d9565e54b1fc6d63c5be9afd58114499128fa57b)
- commit date: 2026-09-11T23:22:35+00:00
- ref: f5dd52df16e1b3f3f8cc

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/34662344653)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d.json)

### vs. 3.12.6

- Geometric mean: 1.056x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d-vs-3.12.6.md)
- [📈time plot](bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.021x faster (HPT: reliability of 99.14%, 1.00x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d-vs-3.13.0rc2.md)
- [📈time plot](bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/34662344653)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260911-macm4pro-arm64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d.json)

### vs. 3.12.6

- Geometric mean: 1.140x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260911-macm4pro-arm64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d-vs-3.12.6.md)
- [📈time plot](bm-20260911-macm4pro-arm64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.053x faster (HPT: reliability of 99.67%, 1.00x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260911-macm4pro-arm64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d-vs-3.13.0rc2.md)
- [📈time plot](bm-20260911-macm4pro-arm64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d-vs-3.13.0rc2.svg)

