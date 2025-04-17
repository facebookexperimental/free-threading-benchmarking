# Results

- fork: python/b530e174a3f870f07952
- version: 3.14.0a7+
- config: NOGIL
- commit hash: [b530e17](https://github.com/python/cpython/commit/b530e17)
- commit date: 2025-04-16T22:44:57+01:00
- commit merge base: [591c982c6e57a12fbb869a1e0172d4da82a27d66](https://github.com/python/cpython/commit/591c982c6e57a12fbb869a1e0172d4da82a27d66)
- ref: b530e174a3f870f07952

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14505293875)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250416-linux-x86_64-python-b530e174a3f870f07952-3.14.0a7%2B-b530e17.json)

### vs. 3.12.6

- Geometric mean: 1.017x faster (HPT: reliability of 82.26%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250416-linux-x86_64-python-b530e174a3f870f07952-3.14.0a7%2B-b530e17-vs-3.12.6.md)
- [📈time plot](bm-20250416-linux-x86_64-python-b530e174a3f870f07952-3.14.0a7%2B-b530e17-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.020x slower (HPT: reliability of 93.26%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250416-linux-x86_64-python-b530e174a3f870f07952-3.14.0a7%2B-b530e17-vs-3.13.0rc2.md)
- [📈time plot](bm-20250416-linux-x86_64-python-b530e174a3f870f07952-3.14.0a7%2B-b530e17-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.067x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.19x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250416-linux-x86_64-python-b530e174a3f870f07952-3.14.0a7%2B-b530e17-vs-base-mem.svg)
- [📄table](bm-20250416-linux-x86_64-python-b530e174a3f870f07952-3.14.0a7%2B-b530e17-vs-base.md)
- [📈time plot](bm-20250416-linux-x86_64-python-b530e174a3f870f07952-3.14.0a7%2B-b530e17-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14505293875)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250416-vultr-x86_64-python-b530e174a3f870f07952-3.14.0a7%2B-b530e17.json)

### vs. 3.12.6

- Geometric mean: 1.028x faster (HPT: reliability of 65.46%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250416-vultr-x86_64-python-b530e174a3f870f07952-3.14.0a7%2B-b530e17-vs-3.12.6.md)
- [📈time plot](bm-20250416-vultr-x86_64-python-b530e174a3f870f07952-3.14.0a7%2B-b530e17-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.005x slower (HPT: reliability of 87.56%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250416-vultr-x86_64-python-b530e174a3f870f07952-3.14.0a7%2B-b530e17-vs-3.13.0rc2.md)
- [📈time plot](bm-20250416-vultr-x86_64-python-b530e174a3f870f07952-3.14.0a7%2B-b530e17-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.078x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250416-vultr-x86_64-python-b530e174a3f870f07952-3.14.0a7%2B-b530e17-vs-base-mem.svg)
- [📄table](bm-20250416-vultr-x86_64-python-b530e174a3f870f07952-3.14.0a7%2B-b530e17-vs-base.md)
- [📈time plot](bm-20250416-vultr-x86_64-python-b530e174a3f870f07952-3.14.0a7%2B-b530e17-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14505293875)
- cpu model: missing
- platform: macOS-15.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20250416-macm4pro-arm64-python-b530e174a3f870f07952-3.14.0a7%2B-b530e17.json)

### vs. 3.12.6

- Geometric mean: 1.120x faster (HPT: reliability of 99.92%, 1.01x faster at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250416-macm4pro-arm64-python-b530e174a3f870f07952-3.14.0a7%2B-b530e17-vs-3.12.6.md)
- [📈time plot](bm-20250416-macm4pro-arm64-python-b530e174a3f870f07952-3.14.0a7%2B-b530e17-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.038x faster (HPT: reliability of 52.81%, 1.00x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250416-macm4pro-arm64-python-b530e174a3f870f07952-3.14.0a7%2B-b530e17-vs-3.13.0rc2.md)
- [📈time plot](bm-20250416-macm4pro-arm64-python-b530e174a3f870f07952-3.14.0a7%2B-b530e17-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.010x slower (HPT: reliability of 99.14%, 1.00x slower at 99th %ile)
- Memory usage: 1.11x
- [🧠memory plot](bm-20250416-macm4pro-arm64-python-b530e174a3f870f07952-3.14.0a7%2B-b530e17-vs-base-mem.svg)
- [📄table](bm-20250416-macm4pro-arm64-python-b530e174a3f870f07952-3.14.0a7%2B-b530e17-vs-base.md)
- [📈time plot](bm-20250416-macm4pro-arm64-python-b530e174a3f870f07952-3.14.0a7%2B-b530e17-vs-base.svg)

