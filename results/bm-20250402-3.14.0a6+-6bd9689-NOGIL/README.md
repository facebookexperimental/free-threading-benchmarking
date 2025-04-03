# Results

- fork: python/6bd96894269be4754a81
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [6bd9689](https://github.com/python/cpython/commit/6bd9689)
- commit date: 2025-04-02T19:50:01-04:00
- commit merge base: [06822bfbf625e9777813542be0b8a2d10a685f30](https://github.com/python/cpython/commit/06822bfbf625e9777813542be0b8a2d10a685f30)
- ref: 6bd96894269be4754a81

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14231997048)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250402-vultr-x86_64-python-6bd96894269be4754a81-3.14.0a6%2B-6bd9689.json)

### vs. 3.12.6

- Geometric mean: 1.076x slower (HPT: reliability of 99.99%, 1.05x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250402-vultr-x86_64-python-6bd96894269be4754a81-3.14.0a6%2B-6bd9689-vs-3.12.6.md)
- [📈time plot](bm-20250402-vultr-x86_64-python-6bd96894269be4754a81-3.14.0a6%2B-6bd9689-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.105x slower (HPT: reliability of 99.98%, 1.07x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250402-vultr-x86_64-python-6bd96894269be4754a81-3.14.0a6%2B-6bd9689-vs-3.13.0rc2.md)
- [📈time plot](bm-20250402-vultr-x86_64-python-6bd96894269be4754a81-3.14.0a6%2B-6bd9689-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14232219173)
- cpu model: missing
- platform: macOS-15.3.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250402-macm4pro-arm64-python-6bd96894269be4754a81-3.14.0a6%2B-6bd9689.json)

### vs. 3.12.6

- Geometric mean: 1.028x faster (HPT: reliability of 85.41%, 1.00x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250402-macm4pro-arm64-python-6bd96894269be4754a81-3.14.0a6%2B-6bd9689-vs-3.12.6.md)
- [📈time plot](bm-20250402-macm4pro-arm64-python-6bd96894269be4754a81-3.14.0a6%2B-6bd9689-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.046x slower (HPT: reliability of 99.09%, 1.00x slower at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250402-macm4pro-arm64-python-6bd96894269be4754a81-3.14.0a6%2B-6bd9689-vs-3.13.0rc2.md)
- [📈time plot](bm-20250402-macm4pro-arm64-python-6bd96894269be4754a81-3.14.0a6%2B-6bd9689-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.023x slower (HPT: reliability of 99.59%, 1.00x slower at 99th %ile)
- Memory usage: 1.11x
- [🧠memory plot](bm-20250402-macm4pro-arm64-python-6bd96894269be4754a81-3.14.0a6%2B-6bd9689-vs-base-mem.svg)
- [📄table](bm-20250402-macm4pro-arm64-python-6bd96894269be4754a81-3.14.0a6%2B-6bd9689-vs-base.md)
- [📈time plot](bm-20250402-macm4pro-arm64-python-6bd96894269be4754a81-3.14.0a6%2B-6bd9689-vs-base.svg)

