# Results

- fork: python/e6ef47ac229b5c4a62b9
- version: 3.14.0a7+
- config: NOGIL
- commit hash: [e6ef47a](https://github.com/python/cpython/commit/e6ef47a)
- commit date: 2025-04-12T05:05:03+08:00
- commit merge base: [deda47d6e18d61e982045b795e3599838823db6a](https://github.com/python/cpython/commit/deda47d6e18d61e982045b795e3599838823db6a)
- ref: e6ef47ac229b5c4a62b9

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14414871158)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250412-vultr-x86_64-python-e6ef47ac229b5c4a62b9-3.14.0a7%2B-e6ef47a.json)

### vs. 3.12.6

- Geometric mean: 1.024x faster (HPT: reliability of 70.67%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250412-vultr-x86_64-python-e6ef47ac229b5c4a62b9-3.14.0a7%2B-e6ef47a-vs-3.12.6.md)
- [📈time plot](bm-20250412-vultr-x86_64-python-e6ef47ac229b5c4a62b9-3.14.0a7%2B-e6ef47a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.009x slower (HPT: reliability of 95.60%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250412-vultr-x86_64-python-e6ef47ac229b5c4a62b9-3.14.0a7%2B-e6ef47a-vs-3.13.0rc2.md)
- [📈time plot](bm-20250412-vultr-x86_64-python-e6ef47ac229b5c4a62b9-3.14.0a7%2B-e6ef47a-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.087x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250412-vultr-x86_64-python-e6ef47ac229b5c4a62b9-3.14.0a7%2B-e6ef47a-vs-base-mem.svg)
- [📄table](bm-20250412-vultr-x86_64-python-e6ef47ac229b5c4a62b9-3.14.0a7%2B-e6ef47a-vs-base.md)
- [📈time plot](bm-20250412-vultr-x86_64-python-e6ef47ac229b5c4a62b9-3.14.0a7%2B-e6ef47a-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14414871158)
- cpu model: missing
- platform: macOS-15.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20250412-macm4pro-arm64-python-e6ef47ac229b5c4a62b9-3.14.0a7%2B-e6ef47a.json)

### vs. 3.12.6

- Geometric mean: 1.114x faster (HPT: reliability of 99.82%, 1.01x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250412-macm4pro-arm64-python-e6ef47ac229b5c4a62b9-3.14.0a7%2B-e6ef47a-vs-3.12.6.md)
- [📈time plot](bm-20250412-macm4pro-arm64-python-e6ef47ac229b5c4a62b9-3.14.0a7%2B-e6ef47a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.033x faster (HPT: reliability of 55.02%, 1.00x slower at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250412-macm4pro-arm64-python-e6ef47ac229b5c4a62b9-3.14.0a7%2B-e6ef47a-vs-3.13.0rc2.md)
- [📈time plot](bm-20250412-macm4pro-arm64-python-e6ef47ac229b5c4a62b9-3.14.0a7%2B-e6ef47a-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.007x slower (HPT: reliability of 99.41%, 1.00x slower at 99th %ile)
- Memory usage: 1.10x
- [🧠memory plot](bm-20250412-macm4pro-arm64-python-e6ef47ac229b5c4a62b9-3.14.0a7%2B-e6ef47a-vs-base-mem.svg)
- [📄table](bm-20250412-macm4pro-arm64-python-e6ef47ac229b5c4a62b9-3.14.0a7%2B-e6ef47a-vs-base.md)
- [📈time plot](bm-20250412-macm4pro-arm64-python-e6ef47ac229b5c4a62b9-3.14.0a7%2B-e6ef47a-vs-base.svg)

