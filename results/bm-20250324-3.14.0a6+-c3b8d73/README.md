# Results

- fork: python/c3b8d73208a25735b635
- version: 3.14.0a6+
- config: 
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

- Geometric mean: 1.101x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250324-linux-x86_64-python-c3b8d73208a25735b635-3.14.0a6%2B-c3b8d73-vs-3.12.6.md)
- [📈time plot](bm-20250324-linux-x86_64-python-c3b8d73208a25735b635-3.14.0a6%2B-c3b8d73-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.056x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250324-linux-x86_64-python-c3b8d73208a25735b635-3.14.0a6%2B-c3b8d73-vs-3.13.0rc2.md)
- [📈time plot](bm-20250324-linux-x86_64-python-c3b8d73208a25735b635-3.14.0a6%2B-c3b8d73-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14048763148)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250324-vultr-x86_64-python-c3b8d73208a25735b635-3.14.0a6%2B-c3b8d73.json)

### vs. 3.12.6

- Geometric mean: 1.072x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250324-vultr-x86_64-python-c3b8d73208a25735b635-3.14.0a6%2B-c3b8d73-vs-3.12.6.md)
- [📈time plot](bm-20250324-vultr-x86_64-python-c3b8d73208a25735b635-3.14.0a6%2B-c3b8d73-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.033x faster (HPT: reliability of 97.77%, 1.00x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250324-vultr-x86_64-python-c3b8d73208a25735b635-3.14.0a6%2B-c3b8d73-vs-3.13.0rc2.md)
- [📈time plot](bm-20250324-vultr-x86_64-python-c3b8d73208a25735b635-3.14.0a6%2B-c3b8d73-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14048763148)
- cpu model: missing
- platform: macOS-15.3.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250324-macm4pro-arm64-python-c3b8d73208a25735b635-3.14.0a6%2B-c3b8d73.json)

### vs. 3.12.6

- Geometric mean: 1.067x faster (HPT: reliability of 99.81%, 1.00x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250324-macm4pro-arm64-python-c3b8d73208a25735b635-3.14.0a6%2B-c3b8d73-vs-3.12.6.md)
- [📈time plot](bm-20250324-macm4pro-arm64-python-c3b8d73208a25735b635-3.14.0a6%2B-c3b8d73-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.009x slower (HPT: reliability of 87.63%, 1.00x slower at 99th %ile)
- Memory usage: 1.07x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250324-macm4pro-arm64-python-c3b8d73208a25735b635-3.14.0a6%2B-c3b8d73-vs-3.13.0rc2.md)
- [📈time plot](bm-20250324-macm4pro-arm64-python-c3b8d73208a25735b635-3.14.0a6%2B-c3b8d73-vs-3.13.0rc2.svg)

