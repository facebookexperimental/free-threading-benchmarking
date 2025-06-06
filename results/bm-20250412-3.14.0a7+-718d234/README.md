# Results

- fork: python/718d234e4086a65d78c8
- version: 3.14.0a7+
- config: 
- commit hash: [718d234](https://github.com/python/cpython/commit/718d234)
- commit date: 2025-04-12T22:35:28Z
- commit merge base: [f2f86d3f459a89273ea22389bb57eed402908302](https://github.com/python/cpython/commit/f2f86d3f459a89273ea22389bb57eed402908302)
- commit date: 2025-04-12T22:35:28+00:00
- ref: 718d234e4086a65d78c8

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14424572441)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250412-vultr-x86_64-python-718d234e4086a65d78c8-3.14.0a7%2B-718d234.json)

### vs. 3.12.6

- Geometric mean: 1.121x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250412-vultr-x86_64-python-718d234e4086a65d78c8-3.14.0a7%2B-718d234-vs-3.12.6.md)
- [📈time plot](bm-20250412-vultr-x86_64-python-718d234e4086a65d78c8-3.14.0a7%2B-718d234-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.082x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, html5lib, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250412-vultr-x86_64-python-718d234e4086a65d78c8-3.14.0a7%2B-718d234-vs-3.13.0rc2.md)
- [📈time plot](bm-20250412-vultr-x86_64-python-718d234e4086a65d78c8-3.14.0a7%2B-718d234-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14424572441)
- cpu model: missing
- platform: macOS-15.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20250412-macm4pro-arm64-python-718d234e4086a65d78c8-3.14.0a7%2B-718d234.json)

### vs. 3.12.6

- Geometric mean: 1.114x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250412-macm4pro-arm64-python-718d234e4086a65d78c8-3.14.0a7%2B-718d234-vs-3.12.6.md)
- [📈time plot](bm-20250412-macm4pro-arm64-python-718d234e4086a65d78c8-3.14.0a7%2B-718d234-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.033x faster (HPT: reliability of 89.85%, 1.00x faster at 99th %ile)
- Memory usage: 1.08x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250412-macm4pro-arm64-python-718d234e4086a65d78c8-3.14.0a7%2B-718d234-vs-3.13.0rc2.md)
- [📈time plot](bm-20250412-macm4pro-arm64-python-718d234e4086a65d78c8-3.14.0a7%2B-718d234-vs-3.13.0rc2.svg)

