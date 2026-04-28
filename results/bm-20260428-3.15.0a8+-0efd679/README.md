# Results

- fork: python/0efd679a6ce3b57ec3c5
- version: 3.15.0a8+
- config: 
- commit hash: [0efd679](https://github.com/python/cpython/commit/0efd679)
- commit date: 2026-04-28T00:06:23+01:00
- commit merge base: [005555a3f0ae20ee8154eb4ee172e1e355144c8c](https://github.com/python/cpython/commit/005555a3f0ae20ee8154eb4ee172e1e355144c8c)
- ref: 0efd679a6ce3b57ec3c5

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/25027787568)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260428-vultr-x86_64-python-0efd679a6ce3b57ec3c5-3.15.0a8%2B-0efd679.json)

### vs. 3.12.6

- Geometric mean: 1.086x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260428-vultr-x86_64-python-0efd679a6ce3b57ec3c5-3.15.0a8%2B-0efd679-vs-3.12.6.md)
- [📈time plot](bm-20260428-vultr-x86_64-python-0efd679a6ce3b57ec3c5-3.15.0a8%2B-0efd679-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.050x faster (HPT: reliability of 99.99%, 1.01x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260428-vultr-x86_64-python-0efd679a6ce3b57ec3c5-3.15.0a8%2B-0efd679-vs-3.13.0rc2.md)
- [📈time plot](bm-20260428-vultr-x86_64-python-0efd679a6ce3b57ec3c5-3.15.0a8%2B-0efd679-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/25027787568)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260428-macm4pro-arm64-python-0efd679a6ce3b57ec3c5-3.15.0a8%2B-0efd679.json)

### vs. 3.12.6

- Geometric mean: 1.174x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260428-macm4pro-arm64-python-0efd679a6ce3b57ec3c5-3.15.0a8%2B-0efd679-vs-3.12.6.md)
- [📈time plot](bm-20260428-macm4pro-arm64-python-0efd679a6ce3b57ec3c5-3.15.0a8%2B-0efd679-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.089x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260428-macm4pro-arm64-python-0efd679a6ce3b57ec3c5-3.15.0a8%2B-0efd679-vs-3.13.0rc2.md)
- [📈time plot](bm-20260428-macm4pro-arm64-python-0efd679a6ce3b57ec3c5-3.15.0a8%2B-0efd679-vs-3.13.0rc2.svg)

