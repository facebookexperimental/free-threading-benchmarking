# Results

- fork: python/c3b8d73208a25735b635
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [c3b8d73](https://github.com/python/cpython/commit/c3b8d73)
- commit date: 2025-03-24T23:15:51Z
- commit merge base: [97ab8fc16a8e0b0e2e68777d0d2f035b3d75a229](https://github.com/python/cpython/commit/97ab8fc16a8e0b0e2e68777d0d2f035b3d75a229)
- commit date: 2025-03-24T23:15:51+00:00
- ref: c3b8d73208a25735b635

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14048763148)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250324-linux-x86_64-python-c3b8d73208a25735b635-3.14.0a6%2B-c3b8d73.json)

### vs. 3.12.6

- Geometric mean: 1.035x slower (HPT: reliability of 99.88%, 1.02x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250324-linux-x86_64-python-c3b8d73208a25735b635-3.14.0a6%2B-c3b8d73-vs-3.12.6.md)
- [📈time plot](bm-20250324-linux-x86_64-python-c3b8d73208a25735b635-3.14.0a6%2B-c3b8d73-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.069x slower (HPT: reliability of 99.97%, 1.04x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250324-linux-x86_64-python-c3b8d73208a25735b635-3.14.0a6%2B-c3b8d73-vs-3.13.0rc2.md)
- [📈time plot](bm-20250324-linux-x86_64-python-c3b8d73208a25735b635-3.14.0a6%2B-c3b8d73-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.119x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250324-linux-x86_64-python-c3b8d73208a25735b635-3.14.0a6%2B-c3b8d73-vs-base-mem.svg)
- [📄table](bm-20250324-linux-x86_64-python-c3b8d73208a25735b635-3.14.0a6%2B-c3b8d73-vs-base.md)
- [📈time plot](bm-20250324-linux-x86_64-python-c3b8d73208a25735b635-3.14.0a6%2B-c3b8d73-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14048763148)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250324-vultr-x86_64-python-c3b8d73208a25735b635-3.14.0a6%2B-c3b8d73.json)

### vs. 3.12.6

- Geometric mean: 1.046x slower (HPT: reliability of 99.99%, 1.03x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250324-vultr-x86_64-python-c3b8d73208a25735b635-3.14.0a6%2B-c3b8d73-vs-3.12.6.md)
- [📈time plot](bm-20250324-vultr-x86_64-python-c3b8d73208a25735b635-3.14.0a6%2B-c3b8d73-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.078x slower (HPT: reliability of 99.99%, 1.03x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250324-vultr-x86_64-python-c3b8d73208a25735b635-3.14.0a6%2B-c3b8d73-vs-3.13.0rc2.md)
- [📈time plot](bm-20250324-vultr-x86_64-python-c3b8d73208a25735b635-3.14.0a6%2B-c3b8d73-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.115x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250324-vultr-x86_64-python-c3b8d73208a25735b635-3.14.0a6%2B-c3b8d73-vs-base-mem.svg)
- [📄table](bm-20250324-vultr-x86_64-python-c3b8d73208a25735b635-3.14.0a6%2B-c3b8d73-vs-base.md)
- [📈time plot](bm-20250324-vultr-x86_64-python-c3b8d73208a25735b635-3.14.0a6%2B-c3b8d73-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14048763148)
- cpu model: missing
- platform: macOS-15.3.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250324-macm4pro-arm64-python-c3b8d73208a25735b635-3.14.0a6%2B-c3b8d73.json)

### vs. 3.12.6

- Geometric mean: 1.056x faster (HPT: reliability of 67.61%, 1.00x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250324-macm4pro-arm64-python-c3b8d73208a25735b635-3.14.0a6%2B-c3b8d73-vs-3.12.6.md)
- [📈time plot](bm-20250324-macm4pro-arm64-python-c3b8d73208a25735b635-3.14.0a6%2B-c3b8d73-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.021x slower (HPT: reliability of 90.71%, 1.00x slower at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250324-macm4pro-arm64-python-c3b8d73208a25735b635-3.14.0a6%2B-c3b8d73-vs-3.13.0rc2.md)
- [📈time plot](bm-20250324-macm4pro-arm64-python-c3b8d73208a25735b635-3.14.0a6%2B-c3b8d73-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.012x slower (HPT: reliability of 98.29%, 1.00x slower at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: 🔴 dask
- [🧠memory plot](bm-20250324-macm4pro-arm64-python-c3b8d73208a25735b635-3.14.0a6%2B-c3b8d73-vs-base-mem.svg)
- [📄table](bm-20250324-macm4pro-arm64-python-c3b8d73208a25735b635-3.14.0a6%2B-c3b8d73-vs-base.md)
- [📈time plot](bm-20250324-macm4pro-arm64-python-c3b8d73208a25735b635-3.14.0a6%2B-c3b8d73-vs-base.svg)

