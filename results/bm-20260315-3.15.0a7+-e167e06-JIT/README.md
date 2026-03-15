# Results

- fork: python/e167e06f8c6b24f7b54e
- version: 3.15.0a7+
- config: JIT
- commit hash: [e167e06](https://github.com/python/cpython/commit/e167e06)
- commit date: 2026-03-15T12:48:56+03:00
- commit merge base: [1dfe99ae3bed6cac01732b47bf7fa637abadf51b](https://github.com/python/cpython/commit/1dfe99ae3bed6cac01732b47bf7fa637abadf51b)
- ref: e167e06f8c6b24f7b54e

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/23111046235)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260315-vultr-x86_64-python-e167e06f8c6b24f7b54e-3.15.0a7%2B-e167e06.json)

### vs. 3.12.6

- Geometric mean: 1.137x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260315-vultr-x86_64-python-e167e06f8c6b24f7b54e-3.15.0a7%2B-e167e06-vs-3.12.6.md)
- [📈time plot](bm-20260315-vultr-x86_64-python-e167e06f8c6b24f7b54e-3.15.0a7%2B-e167e06-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.099x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260315-vultr-x86_64-python-e167e06f8c6b24f7b54e-3.15.0a7%2B-e167e06-vs-3.13.0rc2.md)
- [📈time plot](bm-20260315-vultr-x86_64-python-e167e06f8c6b24f7b54e-3.15.0a7%2B-e167e06-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/23111046235)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260315-macm4pro-arm64-python-e167e06f8c6b24f7b54e-3.15.0a7%2B-e167e06.json)

### vs. 3.12.6

- Geometric mean: 1.260x faster (HPT: reliability of 100.00%, 1.12x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260315-macm4pro-arm64-python-e167e06f8c6b24f7b54e-3.15.0a7%2B-e167e06-vs-3.12.6.md)
- [📈time plot](bm-20260315-macm4pro-arm64-python-e167e06f8c6b24f7b54e-3.15.0a7%2B-e167e06-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.168x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260315-macm4pro-arm64-python-e167e06f8c6b24f7b54e-3.15.0a7%2B-e167e06-vs-3.13.0rc2.md)
- [📈time plot](bm-20260315-macm4pro-arm64-python-e167e06f8c6b24f7b54e-3.15.0a7%2B-e167e06-vs-3.13.0rc2.svg)

