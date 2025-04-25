# Results

- fork: python/e54e8288521c1bd5fa49
- version: 3.14.0a7+
- config: 
- commit hash: [e54e828](https://github.com/python/cpython/commit/e54e828)
- commit date: 2025-04-24T18:25:29-06:00
- commit merge base: [c9f3f5b4ed52d7bed6073ffa39717ece47202558](https://github.com/python/cpython/commit/c9f3f5b4ed52d7bed6073ffa39717ece47202558)
- ref: e54e8288521c1bd5fa49

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14654263351)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250424-vultr-x86_64-python-e54e8288521c1bd5fa49-3.14.0a7%2B-e54e828.json)

### vs. 3.12.6

- Geometric mean: 1.113x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250424-vultr-x86_64-python-e54e8288521c1bd5fa49-3.14.0a7%2B-e54e828-vs-3.12.6.md)
- [📈time plot](bm-20250424-vultr-x86_64-python-e54e8288521c1bd5fa49-3.14.0a7%2B-e54e828-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.074x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250424-vultr-x86_64-python-e54e8288521c1bd5fa49-3.14.0a7%2B-e54e828-vs-3.13.0rc2.md)
- [📈time plot](bm-20250424-vultr-x86_64-python-e54e8288521c1bd5fa49-3.14.0a7%2B-e54e828-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14654263351)
- cpu model: missing
- platform: macOS-15.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20250424-macm4pro-arm64-python-e54e8288521c1bd5fa49-3.14.0a7%2B-e54e828.json)

### vs. 3.12.6

- Geometric mean: 1.124x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250424-macm4pro-arm64-python-e54e8288521c1bd5fa49-3.14.0a7%2B-e54e828-vs-3.12.6.md)
- [📈time plot](bm-20250424-macm4pro-arm64-python-e54e8288521c1bd5fa49-3.14.0a7%2B-e54e828-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.042x faster (HPT: reliability of 99.12%, 1.00x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250424-macm4pro-arm64-python-e54e8288521c1bd5fa49-3.14.0a7%2B-e54e828-vs-3.13.0rc2.md)
- [📈time plot](bm-20250424-macm4pro-arm64-python-e54e8288521c1bd5fa49-3.14.0a7%2B-e54e828-vs-3.13.0rc2.svg)

