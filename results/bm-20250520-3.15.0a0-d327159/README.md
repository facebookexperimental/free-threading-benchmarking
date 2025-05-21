# Results

- fork: python/d327159eb4dd286973d1
- version: 3.15.0a0
- config: 
- commit hash: [d327159](https://github.com/python/cpython/commit/d327159)
- commit date: 2025-05-20T19:54:09-04:00
- commit merge base: [6856a04d68bc1b779b5756a8a7c0ef08d684a630](https://github.com/python/cpython/commit/6856a04d68bc1b779b5756a8a7c0ef08d684a630)
- ref: d327159eb4dd286973d1

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15150656690)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-6.8.0-1024-aws-x86_64-with-glibc2.35
- [raw results](bm-20250520-linux-x86_64-python-d327159eb4dd286973d1-3.15.0a0-d327159.json)

### vs. 3.12.6

- Geometric mean: 1.226x faster (HPT: reliability of 100.00%, 1.12x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250520-linux-x86_64-python-d327159eb4dd286973d1-3.15.0a0-d327159-vs-3.12.6.md)
- [📈time plot](bm-20250520-linux-x86_64-python-d327159eb4dd286973d1-3.15.0a0-d327159-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.179x faster (HPT: reliability of 100.00%, 1.11x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250520-linux-x86_64-python-d327159eb4dd286973d1-3.15.0a0-d327159-vs-3.13.0rc2.md)
- [📈time plot](bm-20250520-linux-x86_64-python-d327159eb4dd286973d1-3.15.0a0-d327159-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15150656690)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250520-vultr-x86_64-python-d327159eb4dd286973d1-3.15.0a0-d327159.json)

### vs. 3.12.6

- Geometric mean: 1.113x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250520-vultr-x86_64-python-d327159eb4dd286973d1-3.15.0a0-d327159-vs-3.12.6.md)
- [📈time plot](bm-20250520-vultr-x86_64-python-d327159eb4dd286973d1-3.15.0a0-d327159-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.075x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250520-vultr-x86_64-python-d327159eb4dd286973d1-3.15.0a0-d327159-vs-3.13.0rc2.md)
- [📈time plot](bm-20250520-vultr-x86_64-python-d327159eb4dd286973d1-3.15.0a0-d327159-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15150656690)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250520-macm4pro-arm64-python-d327159eb4dd286973d1-3.15.0a0-d327159.json)

### vs. 3.12.6

- Geometric mean: 1.102x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250520-macm4pro-arm64-python-d327159eb4dd286973d1-3.15.0a0-d327159-vs-3.12.6.md)
- [📈time plot](bm-20250520-macm4pro-arm64-python-d327159eb4dd286973d1-3.15.0a0-d327159-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.023x faster (HPT: reliability of 87.96%, 1.00x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250520-macm4pro-arm64-python-d327159eb4dd286973d1-3.15.0a0-d327159-vs-3.13.0rc2.md)
- [📈time plot](bm-20250520-macm4pro-arm64-python-d327159eb4dd286973d1-3.15.0a0-d327159-vs-3.13.0rc2.svg)

