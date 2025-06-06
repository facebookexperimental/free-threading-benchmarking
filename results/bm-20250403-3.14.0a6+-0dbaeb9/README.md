# Results

- fork: python/0dbaeb94a8b39972ebda
- version: 3.14.0a6+
- config: 
- commit hash: [0dbaeb9](https://github.com/python/cpython/commit/0dbaeb9)
- commit date: 2025-04-03T22:32:29+02:00
- commit merge base: [b6c92ec419cfa1e4483b072996bab403c9970a5d](https://github.com/python/cpython/commit/b6c92ec419cfa1e4483b072996bab403c9970a5d)
- ref: 0dbaeb94a8b39972ebda

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14255350648)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6%2B-0dbaeb9.json)

### vs. 3.12.6

- Geometric mean: 1.070x faster (HPT: reliability of 99.99%, 1.01x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6%2B-0dbaeb9-vs-3.12.6.md)
- [📈time plot](bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6%2B-0dbaeb9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.032x faster (HPT: reliability of 89.93%, 1.00x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6%2B-0dbaeb9-vs-3.13.0rc2.md)
- [📈time plot](bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6%2B-0dbaeb9-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14255350648)
- cpu model: missing
- platform: macOS-15.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20250403-macm4pro-arm64-python-0dbaeb94a8b39972ebda-3.14.0a6%2B-0dbaeb9.json)

### vs. 3.12.6

- Geometric mean: 1.099x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250403-macm4pro-arm64-python-0dbaeb94a8b39972ebda-3.14.0a6%2B-0dbaeb9-vs-3.12.6.md)
- [📈time plot](bm-20250403-macm4pro-arm64-python-0dbaeb94a8b39972ebda-3.14.0a6%2B-0dbaeb9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.019x faster (HPT: reliability of 55.90%, 1.00x faster at 99th %ile)
- Memory usage: 1.08x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250403-macm4pro-arm64-python-0dbaeb94a8b39972ebda-3.14.0a6%2B-0dbaeb9-vs-3.13.0rc2.md)
- [📈time plot](bm-20250403-macm4pro-arm64-python-0dbaeb94a8b39972ebda-3.14.0a6%2B-0dbaeb9-vs-3.13.0rc2.svg)

