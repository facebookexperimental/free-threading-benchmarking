# Results

- fork: python/a3d0306ca08d09b1417d
- version: 3.15.0a0
- config: 
- commit hash: [a3d0306](https://github.com/python/cpython/commit/a3d0306)
- commit date: 2025-05-22T15:54:56-07:00
- commit merge base: [2da2be4b8400d6de8709e68ca62408af164ee291](https://github.com/python/cpython/commit/2da2be4b8400d6de8709e68ca62408af164ee291)
- ref: a3d0306ca08d09b1417d

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15199512197)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-6.8.0-1024-aws-x86_64-with-glibc2.35
- [raw results](bm-20250522-linux-x86_64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306.json)

### vs. 3.12.6

- Geometric mean: 1.205x faster (HPT: reliability of 100.00%, 1.11x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250522-linux-x86_64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306-vs-3.12.6.md)
- [📈time plot](bm-20250522-linux-x86_64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.160x faster (HPT: reliability of 100.00%, 1.09x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250522-linux-x86_64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306-vs-3.13.0rc2.md)
- [📈time plot](bm-20250522-linux-x86_64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15199512197)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250522-vultr-x86_64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306.json)

### vs. 3.12.6

- Geometric mean: 1.104x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250522-vultr-x86_64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306-vs-3.12.6.md)
- [📈time plot](bm-20250522-vultr-x86_64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.066x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250522-vultr-x86_64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306-vs-3.13.0rc2.md)
- [📈time plot](bm-20250522-vultr-x86_64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15199512197)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250522-macm4pro-arm64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306.json)

### vs. 3.12.6

- Geometric mean: 1.107x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250522-macm4pro-arm64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306-vs-3.12.6.md)
- [📈time plot](bm-20250522-macm4pro-arm64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.027x faster (HPT: reliability of 95.44%, 1.00x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250522-macm4pro-arm64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306-vs-3.13.0rc2.md)
- [📈time plot](bm-20250522-macm4pro-arm64-python-a3d0306ca08d09b1417d-3.15.0a0-a3d0306-vs-3.13.0rc2.svg)

