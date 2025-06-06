# Results

- fork: python/425f60b9eb253c57bc32
- version: 3.14.0a6+
- config: NOGIL
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

- Geometric mean: 1.086x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250329-vultr-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.12.6.md)
- [📈time plot](bm-20250329-vultr-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.117x slower (HPT: reliability of 99.99%, 1.08x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250329-vultr-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.13.0rc2.md)
- [📈time plot](bm-20250329-vultr-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.178x slower (HPT: reliability of 100.00%, 1.17x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250329-vultr-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-base-mem.svg)
- [📄table](bm-20250329-vultr-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-base.md)
- [📈time plot](bm-20250329-vultr-x86_64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14150698572)
- cpu model: missing
- platform: macOS-15.3.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250329-macm4pro-arm64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b.json)

### vs. 3.12.6

- Geometric mean: 1.085x faster (HPT: reliability of 97.69%, 1.00x faster at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250329-macm4pro-arm64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.12.6.md)
- [📈time plot](bm-20250329-macm4pro-arm64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.006x faster (HPT: reliability of 64.06%, 1.00x slower at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250329-macm4pro-arm64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.13.0rc2.md)
- [📈time plot](bm-20250329-macm4pro-arm64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.039x faster (HPT: reliability of 99.67%, 1.00x faster at 99th %ile)
- Memory usage: 1.11x
- [🧠memory plot](bm-20250329-macm4pro-arm64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-base-mem.svg)
- [📄table](bm-20250329-macm4pro-arm64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-base.md)
- [📈time plot](bm-20250329-macm4pro-arm64-python-425f60b9eb253c57bc32-3.14.0a6%2B-425f60b-vs-base.svg)

