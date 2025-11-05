# Results

- fork: python/fa02422918ac3251cdf8
- version: 3.15.0a1+
- config: 
- commit hash: [fa02422](https://github.com/python/cpython/commit/fa02422)
- commit date: 2025-11-04T19:05:49-05:00
- commit merge base: [d5b00c74b30a159d8d8c03e152c6cf8e8b1431b2](https://github.com/python/cpython/commit/d5b00c74b30a159d8d8c03e152c6cf8e8b1431b2)
- ref: fa02422918ac3251cdf8

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19087183143)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251104-vultr-x86_64-python-fa02422918ac3251cdf8-3.15.0a1%2B-fa02422.json)

### vs. 3.12.6

- Geometric mean: 1.085x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251104-vultr-x86_64-python-fa02422918ac3251cdf8-3.15.0a1%2B-fa02422-vs-3.12.6.md)
- [📈time plot](bm-20251104-vultr-x86_64-python-fa02422918ac3251cdf8-3.15.0a1%2B-fa02422-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.049x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251104-vultr-x86_64-python-fa02422918ac3251cdf8-3.15.0a1%2B-fa02422-vs-3.13.0rc2.md)
- [📈time plot](bm-20251104-vultr-x86_64-python-fa02422918ac3251cdf8-3.15.0a1%2B-fa02422-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19087183143)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251104-macm4pro-arm64-python-fa02422918ac3251cdf8-3.15.0a1%2B-fa02422.json)

### vs. 3.12.6

- Geometric mean: 1.120x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251104-macm4pro-arm64-python-fa02422918ac3251cdf8-3.15.0a1%2B-fa02422-vs-3.12.6.md)
- [📈time plot](bm-20251104-macm4pro-arm64-python-fa02422918ac3251cdf8-3.15.0a1%2B-fa02422-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.038x faster (HPT: reliability of 99.12%, 1.00x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251104-macm4pro-arm64-python-fa02422918ac3251cdf8-3.15.0a1%2B-fa02422-vs-3.13.0rc2.md)
- [📈time plot](bm-20251104-macm4pro-arm64-python-fa02422918ac3251cdf8-3.15.0a1%2B-fa02422-vs-3.13.0rc2.svg)

