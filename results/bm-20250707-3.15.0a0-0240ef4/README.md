# Results

- fork: python/0240ef4705d835e27beb
- version: 3.15.0a0
- config: 
- commit hash: [0240ef4](https://github.com/python/cpython/commit/0240ef4)
- commit date: 2025-07-07T23:30:27+05:30
- commit merge base: [fe187fae8d8321f1b8d3c9560a35efe904de4217](https://github.com/python/cpython/commit/fe187fae8d8321f1b8d3c9560a35efe904de4217)
- ref: 0240ef4705d835e27beb

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16130900797)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250707-vultr-x86_64-python-0240ef4705d835e27beb-3.15.0a0-0240ef4.json)

### vs. 3.12.6

- Geometric mean: 1.071x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250707-vultr-x86_64-python-0240ef4705d835e27beb-3.15.0a0-0240ef4-vs-3.12.6.md)
- [📈time plot](bm-20250707-vultr-x86_64-python-0240ef4705d835e27beb-3.15.0a0-0240ef4-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.035x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250707-vultr-x86_64-python-0240ef4705d835e27beb-3.15.0a0-0240ef4-vs-3.13.0rc2.md)
- [📈time plot](bm-20250707-vultr-x86_64-python-0240ef4705d835e27beb-3.15.0a0-0240ef4-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16130900797)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250707-macm4pro-arm64-python-0240ef4705d835e27beb-3.15.0a0-0240ef4.json)

### vs. 3.12.6

- Geometric mean: 1.096x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250707-macm4pro-arm64-python-0240ef4705d835e27beb-3.15.0a0-0240ef4-vs-3.12.6.md)
- [📈time plot](bm-20250707-macm4pro-arm64-python-0240ef4705d835e27beb-3.15.0a0-0240ef4-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.016x faster (HPT: reliability of 61.82%, 1.00x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250707-macm4pro-arm64-python-0240ef4705d835e27beb-3.15.0a0-0240ef4-vs-3.13.0rc2.md)
- [📈time plot](bm-20250707-macm4pro-arm64-python-0240ef4705d835e27beb-3.15.0a0-0240ef4-vs-3.13.0rc2.svg)

