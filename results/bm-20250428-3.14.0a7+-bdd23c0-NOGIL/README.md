# Results

- fork: python/bdd23c0bb95faa37130f
- version: 3.14.0a7+
- config: NOGIL
- commit hash: [bdd23c0](https://github.com/python/cpython/commit/bdd23c0)
- commit date: 2025-04-28T17:23:46-06:00
- commit merge base: [68a737691b0fd591de00f4811bb23a5c280fe859](https://github.com/python/cpython/commit/68a737691b0fd591de00f4811bb23a5c280fe859)
- ref: bdd23c0bb95faa37130f

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14720620102)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-6.8.0-1024-aws-x86_64-with-glibc2.35
- [raw results](bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7%2B-bdd23c0.json)

### vs. 3.12.6

- Geometric mean: 1.103x faster (HPT: reliability of 89.64%, 1.00x faster at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7%2B-bdd23c0-vs-3.12.6.md)
- [📈time plot](bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7%2B-bdd23c0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.061x faster (HPT: reliability of 60.59%, 1.00x faster at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7%2B-bdd23c0-vs-3.13.0rc2.md)
- [📈time plot](bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7%2B-bdd23c0-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.086x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7%2B-bdd23c0-vs-base-mem.svg)
- [📄table](bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7%2B-bdd23c0-vs-base.md)
- [📈time plot](bm-20250428-linux-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7%2B-bdd23c0-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14720620102)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250428-vultr-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7%2B-bdd23c0.json)

### vs. 3.12.6

- Geometric mean: 1.036x faster (HPT: reliability of 57.93%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250428-vultr-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7%2B-bdd23c0-vs-3.12.6.md)
- [📈time plot](bm-20250428-vultr-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7%2B-bdd23c0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.002x faster (HPT: reliability of 83.82%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250428-vultr-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7%2B-bdd23c0-vs-3.13.0rc2.md)
- [📈time plot](bm-20250428-vultr-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7%2B-bdd23c0-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.079x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250428-vultr-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7%2B-bdd23c0-vs-base-mem.svg)
- [📄table](bm-20250428-vultr-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7%2B-bdd23c0-vs-base.md)
- [📈time plot](bm-20250428-vultr-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7%2B-bdd23c0-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14720620102)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7%2B-bdd23c0.json)

### vs. 3.12.6

- Geometric mean: 1.100x faster (HPT: reliability of 98.08%, 1.00x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7%2B-bdd23c0-vs-3.12.6.md)
- [📈time plot](bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7%2B-bdd23c0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.020x faster (HPT: reliability of 65.44%, 1.00x slower at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7%2B-bdd23c0-vs-3.13.0rc2.md)
- [📈time plot](bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7%2B-bdd23c0-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.016x slower (HPT: reliability of 99.30%, 1.00x slower at 99th %ile)
- Memory usage: 1.10x
- [🧠memory plot](bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7%2B-bdd23c0-vs-base-mem.svg)
- [📄table](bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7%2B-bdd23c0-vs-base.md)
- [📈time plot](bm-20250428-macm4pro-arm64-python-bdd23c0bb95faa37130f-3.14.0a7%2B-bdd23c0-vs-base.svg)

