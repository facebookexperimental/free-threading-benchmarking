# Results

- fork: python/bdd23c0bb95faa37130f
- version: 3.14.0a7+
- config: 
- commit hash: [bdd23c0](https://github.com/python/cpython/commit/bdd23c0)
- commit date: 2025-04-28T17:23:46-06:00
- commit merge base: [68a737691b0fd591de00f4811bb23a5c280fe859](https://github.com/python/cpython/commit/68a737691b0fd591de00f4811bb23a5c280fe859)
- ref: bdd23c0bb95faa37130f

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14720620102)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250428-vultr-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7%2B-bdd23c0.json)

### vs. 3.12.6

- Geometric mean: 1.117x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250428-vultr-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7%2B-bdd23c0-vs-3.12.6.md)
- [📈time plot](bm-20250428-vultr-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7%2B-bdd23c0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.078x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250428-vultr-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7%2B-bdd23c0-vs-3.13.0rc2.md)
- [📈time plot](bm-20250428-vultr-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7%2B-bdd23c0-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14720620102)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7%2B-bdd23c0.json)

### vs. 3.12.6

- Geometric mean: 1.115x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7%2B-bdd23c0-vs-3.12.6.md)
- [📈time plot](bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7%2B-bdd23c0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.034x faster (HPT: reliability of 92.72%, 1.00x faster at 99th %ile)
- Memory usage: 1.08x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7%2B-bdd23c0-vs-3.13.0rc2.md)
- [📈time plot](bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7%2B-bdd23c0-vs-3.13.0rc2.svg)

