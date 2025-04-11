# Results

- fork: python/e5f68fd29b3bd867207f
- version: 3.14.0a7+
- config: NOGIL
- commit hash: [e5f68fd](https://github.com/python/cpython/commit/e5f68fd)
- commit date: 2025-04-10T23:17:33+01:00
- commit merge base: [66cdb2bd8ab93a4691bead7f5d1e54e5ca6895b4](https://github.com/python/cpython/commit/66cdb2bd8ab93a4691bead7f5d1e54e5ca6895b4)
- ref: e5f68fd29b3bd867207f

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14392878426)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250410-linux-x86_64-python-e5f68fd29b3bd867207f-3.14.0a7%2B-e5f68fd.json)

### vs. 3.12.6

- Geometric mean: 1.045x faster (HPT: reliability of 61.03%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250410-linux-x86_64-python-e5f68fd29b3bd867207f-3.14.0a7%2B-e5f68fd-vs-3.12.6.md)
- [📈time plot](bm-20250410-linux-x86_64-python-e5f68fd29b3bd867207f-3.14.0a7%2B-e5f68fd-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.010x faster (HPT: reliability of 89.45%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250410-linux-x86_64-python-e5f68fd29b3bd867207f-3.14.0a7%2B-e5f68fd-vs-3.13.0rc2.md)
- [📈time plot](bm-20250410-linux-x86_64-python-e5f68fd29b3bd867207f-3.14.0a7%2B-e5f68fd-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.093x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.19x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250410-linux-x86_64-python-e5f68fd29b3bd867207f-3.14.0a7%2B-e5f68fd-vs-base-mem.svg)
- [📄table](bm-20250410-linux-x86_64-python-e5f68fd29b3bd867207f-3.14.0a7%2B-e5f68fd-vs-base.md)
- [📈time plot](bm-20250410-linux-x86_64-python-e5f68fd29b3bd867207f-3.14.0a7%2B-e5f68fd-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14392878426)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250410-vultr-x86_64-python-e5f68fd29b3bd867207f-3.14.0a7%2B-e5f68fd.json)

### vs. 3.12.6

- Geometric mean: 1.032x faster (HPT: reliability of 57.75%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250410-vultr-x86_64-python-e5f68fd29b3bd867207f-3.14.0a7%2B-e5f68fd-vs-3.12.6.md)
- [📈time plot](bm-20250410-vultr-x86_64-python-e5f68fd29b3bd867207f-3.14.0a7%2B-e5f68fd-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.001x slower (HPT: reliability of 84.76%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250410-vultr-x86_64-python-e5f68fd29b3bd867207f-3.14.0a7%2B-e5f68fd-vs-3.13.0rc2.md)
- [📈time plot](bm-20250410-vultr-x86_64-python-e5f68fd29b3bd867207f-3.14.0a7%2B-e5f68fd-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.075x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.19x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250410-vultr-x86_64-python-e5f68fd29b3bd867207f-3.14.0a7%2B-e5f68fd-vs-base-mem.svg)
- [📄table](bm-20250410-vultr-x86_64-python-e5f68fd29b3bd867207f-3.14.0a7%2B-e5f68fd-vs-base.md)
- [📈time plot](bm-20250410-vultr-x86_64-python-e5f68fd29b3bd867207f-3.14.0a7%2B-e5f68fd-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14392878426)
- cpu model: missing
- platform: macOS-15.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20250410-macm4pro-arm64-python-e5f68fd29b3bd867207f-3.14.0a7%2B-e5f68fd.json)

### vs. 3.12.6

- Geometric mean: 1.118x faster (HPT: reliability of 99.89%, 1.01x faster at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250410-macm4pro-arm64-python-e5f68fd29b3bd867207f-3.14.0a7%2B-e5f68fd-vs-3.12.6.md)
- [📈time plot](bm-20250410-macm4pro-arm64-python-e5f68fd29b3bd867207f-3.14.0a7%2B-e5f68fd-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.037x faster (HPT: reliability of 50.00%, 1.00x slower at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250410-macm4pro-arm64-python-e5f68fd29b3bd867207f-3.14.0a7%2B-e5f68fd-vs-3.13.0rc2.md)
- [📈time plot](bm-20250410-macm4pro-arm64-python-e5f68fd29b3bd867207f-3.14.0a7%2B-e5f68fd-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.001x slower (HPT: reliability of 93.68%, 1.00x slower at 99th %ile)
- Memory usage: 1.11x
- [🧠memory plot](bm-20250410-macm4pro-arm64-python-e5f68fd29b3bd867207f-3.14.0a7%2B-e5f68fd-vs-base-mem.svg)
- [📄table](bm-20250410-macm4pro-arm64-python-e5f68fd29b3bd867207f-3.14.0a7%2B-e5f68fd-vs-base.md)
- [📈time plot](bm-20250410-macm4pro-arm64-python-e5f68fd29b3bd867207f-3.14.0a7%2B-e5f68fd-vs-base.svg)

