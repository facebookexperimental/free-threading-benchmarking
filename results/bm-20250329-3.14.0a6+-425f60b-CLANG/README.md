# Results

- fork: python/425f60b9eb253c57bc32
- version: 3.14.0a6+
- config: CLANG
- commit hash: [425f60b](https://github.com/python/cpython/commit/425f60b)
- commit date: 2025-03-29T21:15:48Z
- commit merge base: [c6b1a073438d93d4e62957accc73487df6711851](https://github.com/python/cpython/commit/c6b1a073438d93d4e62957accc73487df6711851)
- commit date: 2025-03-29T21:15:48+00:00
- ref: 425f60b9eb253c57bc32

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14150698572)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250329-vultr-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b.json)

### vs. 3.12.6

- Geometric mean: 1.159x faster (HPT: reliability of 100.00%, 1.09x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250329-vultr-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.12.6.md)
- [📈time plot](bm-20250329-vultr-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.118x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, html5lib, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250329-vultr-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.13.0rc2.md)
- [📈time plot](bm-20250329-vultr-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.044x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.03x
- [🧠memory plot](bm-20250329-vultr-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-base-mem.svg)
- [📄table](bm-20250329-vultr-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-base.md)
- [📈time plot](bm-20250329-vultr-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14150698572)
- cpu model: missing
- platform: macOS-15.3.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250329-macm4pro-arm64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b.json)

### vs. 3.12.6

- Geometric mean: 1.167x faster (HPT: reliability of 100.00%, 1.10x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250329-macm4pro-arm64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.12.6.md)
- [📈time plot](bm-20250329-macm4pro-arm64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.082x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.07x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250329-macm4pro-arm64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.13.0rc2.md)
- [📈time plot](bm-20250329-macm4pro-arm64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.121x faster (HPT: reliability of 100.00%, 1.09x faster at 99th %ile)
- Memory usage: 0.99x
- [🧠memory plot](bm-20250329-macm4pro-arm64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-base-mem.svg)
- [📄table](bm-20250329-macm4pro-arm64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-base.md)
- [📈time plot](bm-20250329-macm4pro-arm64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-base.svg)

