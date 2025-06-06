# Results

- fork: python/231a50fa9a5444836c94
- version: 3.14.0a6+
- config: 
- commit hash: [231a50f](https://github.com/python/cpython/commit/231a50f)
- commit date: 2025-04-04T23:37:41+01:00
- commit merge base: [7473c600a5890ffd87e8761c418bf3312ce7f38c](https://github.com/python/cpython/commit/7473c600a5890ffd87e8761c418bf3312ce7f38c)
- ref: 231a50fa9a5444836c94

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14276400765)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250404-vultr-x86_64-python-231a50fa9a5444836c94-3.14.0a6%2B-231a50f.json)

### vs. 3.12.6

- Geometric mean: 1.067x faster (HPT: reliability of 99.97%, 1.01x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250404-vultr-x86_64-python-231a50fa9a5444836c94-3.14.0a6%2B-231a50f-vs-3.12.6.md)
- [📈time plot](bm-20250404-vultr-x86_64-python-231a50fa9a5444836c94-3.14.0a6%2B-231a50f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.029x faster (HPT: reliability of 73.89%, 1.00x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250404-vultr-x86_64-python-231a50fa9a5444836c94-3.14.0a6%2B-231a50f-vs-3.13.0rc2.md)
- [📈time plot](bm-20250404-vultr-x86_64-python-231a50fa9a5444836c94-3.14.0a6%2B-231a50f-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14276400765)
- cpu model: missing
- platform: macOS-15.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20250404-macm4pro-arm64-python-231a50fa9a5444836c94-3.14.0a6%2B-231a50f.json)

### vs. 3.12.6

- Geometric mean: 1.097x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250404-macm4pro-arm64-python-231a50fa9a5444836c94-3.14.0a6%2B-231a50f-vs-3.12.6.md)
- [📈time plot](bm-20250404-macm4pro-arm64-python-231a50fa9a5444836c94-3.14.0a6%2B-231a50f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.018x faster (HPT: reliability of 53.40%, 1.00x faster at 99th %ile)
- Memory usage: 1.08x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250404-macm4pro-arm64-python-231a50fa9a5444836c94-3.14.0a6%2B-231a50f-vs-3.13.0rc2.md)
- [📈time plot](bm-20250404-macm4pro-arm64-python-231a50fa9a5444836c94-3.14.0a6%2B-231a50f-vs-3.13.0rc2.svg)

