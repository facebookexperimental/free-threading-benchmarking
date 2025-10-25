# Results

- fork: python/d78d7a50b06c4ea10d13
- version: 3.15.0a1+
- config: 
- commit hash: [d78d7a5](https://github.com/python/cpython/commit/d78d7a5)
- commit date: 2025-10-24T22:53:00+03:00
- commit merge base: [4f8e7b5ac59f578d8b328d1238b5e1fee00601bc](https://github.com/python/cpython/commit/4f8e7b5ac59f578d8b328d1238b5e1fee00601bc)
- ref: d78d7a50b06c4ea10d13

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18795392301)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251024-vultr-x86_64-python-d78d7a50b06c4ea10d13-3.15.0a1%2B-d78d7a5.json)

### vs. 3.12.6

- Geometric mean: 1.080x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251024-vultr-x86_64-python-d78d7a50b06c4ea10d13-3.15.0a1%2B-d78d7a5-vs-3.12.6.md)
- [📈time plot](bm-20251024-vultr-x86_64-python-d78d7a50b06c4ea10d13-3.15.0a1%2B-d78d7a5-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.044x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251024-vultr-x86_64-python-d78d7a50b06c4ea10d13-3.15.0a1%2B-d78d7a5-vs-3.13.0rc2.md)
- [📈time plot](bm-20251024-vultr-x86_64-python-d78d7a50b06c4ea10d13-3.15.0a1%2B-d78d7a5-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18795392301)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251024-macm4pro-arm64-python-d78d7a50b06c4ea10d13-3.15.0a1%2B-d78d7a5.json)

### vs. 3.12.6

- Geometric mean: 1.130x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251024-macm4pro-arm64-python-d78d7a50b06c4ea10d13-3.15.0a1%2B-d78d7a5-vs-3.12.6.md)
- [📈time plot](bm-20251024-macm4pro-arm64-python-d78d7a50b06c4ea10d13-3.15.0a1%2B-d78d7a5-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.049x faster (HPT: reliability of 99.97%, 1.01x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251024-macm4pro-arm64-python-d78d7a50b06c4ea10d13-3.15.0a1%2B-d78d7a5-vs-3.13.0rc2.md)
- [📈time plot](bm-20251024-macm4pro-arm64-python-d78d7a50b06c4ea10d13-3.15.0a1%2B-d78d7a5-vs-3.13.0rc2.svg)

