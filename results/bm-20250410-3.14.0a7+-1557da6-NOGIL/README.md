# Results

- fork: python/1557da622c89985d14b7
- version: 3.14.0a7+
- config: NOGIL
- commit hash: [1557da6](https://github.com/python/cpython/commit/1557da6)
- commit date: 2025-04-10T16:41:41+03:00
- commit merge base: [5fbe23ee4ec636b78ca26ce0a8b7d83dff77a2ce](https://github.com/python/cpython/commit/5fbe23ee4ec636b78ca26ce0a8b7d83dff77a2ce)
- ref: 1557da622c89985d14b7

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14382441766)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250410-linux-x86_64-python-1557da622c89985d14b7-3.14.0a7%2B-1557da6.json)

### vs. 3.12.6

- Geometric mean: 1.047x faster (HPT: reliability of 53.84%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250410-linux-x86_64-python-1557da622c89985d14b7-3.14.0a7%2B-1557da6-vs-3.12.6.md)
- [📈time plot](bm-20250410-linux-x86_64-python-1557da622c89985d14b7-3.14.0a7%2B-1557da6-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.009x faster (HPT: reliability of 91.36%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250410-linux-x86_64-python-1557da622c89985d14b7-3.14.0a7%2B-1557da6-vs-3.13.0rc2.md)
- [📈time plot](bm-20250410-linux-x86_64-python-1557da622c89985d14b7-3.14.0a7%2B-1557da6-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.070x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250410-linux-x86_64-python-1557da622c89985d14b7-3.14.0a7%2B-1557da6-vs-base-mem.svg)
- [📄table](bm-20250410-linux-x86_64-python-1557da622c89985d14b7-3.14.0a7%2B-1557da6-vs-base.md)
- [📈time plot](bm-20250410-linux-x86_64-python-1557da622c89985d14b7-3.14.0a7%2B-1557da6-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14382441766)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250410-vultr-x86_64-python-1557da622c89985d14b7-3.14.0a7%2B-1557da6.json)

### vs. 3.12.6

- Geometric mean: 1.033x faster (HPT: reliability of 65.64%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250410-vultr-x86_64-python-1557da622c89985d14b7-3.14.0a7%2B-1557da6-vs-3.12.6.md)
- [📈time plot](bm-20250410-vultr-x86_64-python-1557da622c89985d14b7-3.14.0a7%2B-1557da6-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.000x slower (HPT: reliability of 91.89%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250410-vultr-x86_64-python-1557da622c89985d14b7-3.14.0a7%2B-1557da6-vs-3.13.0rc2.md)
- [📈time plot](bm-20250410-vultr-x86_64-python-1557da622c89985d14b7-3.14.0a7%2B-1557da6-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.081x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.19x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250410-vultr-x86_64-python-1557da622c89985d14b7-3.14.0a7%2B-1557da6-vs-base-mem.svg)
- [📄table](bm-20250410-vultr-x86_64-python-1557da622c89985d14b7-3.14.0a7%2B-1557da6-vs-base.md)
- [📈time plot](bm-20250410-vultr-x86_64-python-1557da622c89985d14b7-3.14.0a7%2B-1557da6-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14382441766)
- cpu model: missing
- platform: macOS-15.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20250410-macm4pro-arm64-python-1557da622c89985d14b7-3.14.0a7%2B-1557da6.json)

### vs. 3.12.6

- Geometric mean: 1.106x faster (HPT: reliability of 98.75%, 1.00x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250410-macm4pro-arm64-python-1557da622c89985d14b7-3.14.0a7%2B-1557da6-vs-3.12.6.md)
- [📈time plot](bm-20250410-macm4pro-arm64-python-1557da622c89985d14b7-3.14.0a7%2B-1557da6-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.025x faster (HPT: reliability of 60.54%, 1.00x slower at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250410-macm4pro-arm64-python-1557da622c89985d14b7-3.14.0a7%2B-1557da6-vs-3.13.0rc2.md)
- [📈time plot](bm-20250410-macm4pro-arm64-python-1557da622c89985d14b7-3.14.0a7%2B-1557da6-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.006x slower (HPT: reliability of 99.34%, 1.00x slower at 99th %ile)
- Memory usage: 1.10x
- [🧠memory plot](bm-20250410-macm4pro-arm64-python-1557da622c89985d14b7-3.14.0a7%2B-1557da6-vs-base-mem.svg)
- [📄table](bm-20250410-macm4pro-arm64-python-1557da622c89985d14b7-3.14.0a7%2B-1557da6-vs-base.md)
- [📈time plot](bm-20250410-macm4pro-arm64-python-1557da622c89985d14b7-3.14.0a7%2B-1557da6-vs-base.svg)

