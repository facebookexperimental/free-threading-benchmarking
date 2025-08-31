# Results

- fork: python/d3d94e0ed715829d9bf9
- version: 3.15.0a0
- config: 
- commit hash: [d3d94e0](https://github.com/python/cpython/commit/d3d94e0)
- commit date: 2025-08-30T22:21:25+01:00
- commit merge base: [f58a7c717584241467970623384ce61cbd776f29](https://github.com/python/cpython/commit/f58a7c717584241467970623384ce61cbd776f29)
- ref: d3d94e0ed715829d9bf9

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17350176868)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [pystats raw](bm-20250830-vultr-x86_64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0-pystats.json)
- [pystats table](bm-20250830-vultr-x86_64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0-pystats.md)
- [raw results](bm-20250830-vultr-x86_64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0.json)

### vs. 3.12.6

- Geometric mean: 1.067x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250830-vultr-x86_64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0-vs-3.12.6.md)
- [📈time plot](bm-20250830-vultr-x86_64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.032x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250830-vultr-x86_64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0-vs-3.13.0rc2.md)
- [📈time plot](bm-20250830-vultr-x86_64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17350176868)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0.json)

### vs. 3.12.6

- Geometric mean: 1.090x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0-vs-3.12.6.md)
- [📈time plot](bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.011x faster (HPT: reliability of 51.63%, 1.00x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0-vs-3.13.0rc2.md)
- [📈time plot](bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0-vs-3.13.0rc2.svg)

