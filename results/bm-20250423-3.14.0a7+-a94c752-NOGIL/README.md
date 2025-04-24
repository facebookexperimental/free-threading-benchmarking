# Results

- fork: python/a94c7528b596e9ec234f
- version: 3.14.0a7+
- config: NOGIL
- commit hash: [a94c752](https://github.com/python/cpython/commit/a94c752)
- commit date: 2025-04-23T23:40:24Z
- commit merge base: [402dba29281c1e1092ff32875c91f23bacabb677](https://github.com/python/cpython/commit/402dba29281c1e1092ff32875c91f23bacabb677)
- commit date: 2025-04-23T23:40:24+00:00
- ref: a94c7528b596e9ec234f

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14630705743)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250423-vultr-x86_64-python-a94c7528b596e9ec234f-3.14.0a7%2B-a94c752.json)

### vs. 3.12.6

- Geometric mean: 1.026x faster (HPT: reliability of 66.33%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250423-vultr-x86_64-python-a94c7528b596e9ec234f-3.14.0a7%2B-a94c752-vs-3.12.6.md)
- [📈time plot](bm-20250423-vultr-x86_64-python-a94c7528b596e9ec234f-3.14.0a7%2B-a94c752-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.007x slower (HPT: reliability of 85.44%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250423-vultr-x86_64-python-a94c7528b596e9ec234f-3.14.0a7%2B-a94c752-vs-3.13.0rc2.md)
- [📈time plot](bm-20250423-vultr-x86_64-python-a94c7528b596e9ec234f-3.14.0a7%2B-a94c752-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.085x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250423-vultr-x86_64-python-a94c7528b596e9ec234f-3.14.0a7%2B-a94c752-vs-base-mem.svg)
- [📄table](bm-20250423-vultr-x86_64-python-a94c7528b596e9ec234f-3.14.0a7%2B-a94c752-vs-base.md)
- [📈time plot](bm-20250423-vultr-x86_64-python-a94c7528b596e9ec234f-3.14.0a7%2B-a94c752-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14630705743)
- cpu model: missing
- platform: macOS-15.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20250423-macm4pro-arm64-python-a94c7528b596e9ec234f-3.14.0a7%2B-a94c752.json)

### vs. 3.12.6

- Geometric mean: 1.092x faster (HPT: reliability of 95.98%, 1.00x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250423-macm4pro-arm64-python-a94c7528b596e9ec234f-3.14.0a7%2B-a94c752-vs-3.12.6.md)
- [📈time plot](bm-20250423-macm4pro-arm64-python-a94c7528b596e9ec234f-3.14.0a7%2B-a94c752-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.012x faster (HPT: reliability of 71.50%, 1.00x slower at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250423-macm4pro-arm64-python-a94c7528b596e9ec234f-3.14.0a7%2B-a94c752-vs-3.13.0rc2.md)
- [📈time plot](bm-20250423-macm4pro-arm64-python-a94c7528b596e9ec234f-3.14.0a7%2B-a94c752-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.021x slower (HPT: reliability of 99.64%, 1.00x slower at 99th %ile)
- Memory usage: 1.10x
- [🧠memory plot](bm-20250423-macm4pro-arm64-python-a94c7528b596e9ec234f-3.14.0a7%2B-a94c752-vs-base-mem.svg)
- [📄table](bm-20250423-macm4pro-arm64-python-a94c7528b596e9ec234f-3.14.0a7%2B-a94c752-vs-base.md)
- [📈time plot](bm-20250423-macm4pro-arm64-python-a94c7528b596e9ec234f-3.14.0a7%2B-a94c752-vs-base.svg)

