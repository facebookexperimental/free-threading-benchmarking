# Results

- fork: python/b8633f9aca9b198e5592
- version: 3.14.0a7+
- config: NOGIL
- commit hash: [b8633f9](https://github.com/python/cpython/commit/b8633f9)
- commit date: 2025-05-01T15:41:44-07:00
- commit merge base: [c14134020f44575635e11e4552cefcfd8cdbe22f](https://github.com/python/cpython/commit/c14134020f44575635e11e4552cefcfd8cdbe22f)
- ref: b8633f9aca9b198e5592

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14789446459)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-6.8.0-1024-aws-x86_64-with-glibc2.35
- [raw results](bm-20250501-linux-x86_64-python-b8633f9aca9b198e5592-3.14.0a7%2B-b8633f9.json)

### vs. 3.12.6

- Geometric mean: 1.087x faster (HPT: reliability of 74.13%, 1.00x faster at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250501-linux-x86_64-python-b8633f9aca9b198e5592-3.14.0a7%2B-b8633f9-vs-3.12.6.md)
- [📈time plot](bm-20250501-linux-x86_64-python-b8633f9aca9b198e5592-3.14.0a7%2B-b8633f9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.047x faster (HPT: reliability of 58.73%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250501-linux-x86_64-python-b8633f9aca9b198e5592-3.14.0a7%2B-b8633f9-vs-3.13.0rc2.md)
- [📈time plot](bm-20250501-linux-x86_64-python-b8633f9aca9b198e5592-3.14.0a7%2B-b8633f9-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.100x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20250501-linux-x86_64-python-b8633f9aca9b198e5592-3.14.0a7%2B-b8633f9-vs-base-mem.svg)
- [📄table](bm-20250501-linux-x86_64-python-b8633f9aca9b198e5592-3.14.0a7%2B-b8633f9-vs-base.md)
- [📈time plot](bm-20250501-linux-x86_64-python-b8633f9aca9b198e5592-3.14.0a7%2B-b8633f9-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14789446459)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250501-vultr-x86_64-python-b8633f9aca9b198e5592-3.14.0a7%2B-b8633f9.json)

### vs. 3.12.6

- Geometric mean: 1.011x faster (HPT: reliability of 93.85%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250501-vultr-x86_64-python-b8633f9aca9b198e5592-3.14.0a7%2B-b8633f9-vs-3.12.6.md)
- [📈time plot](bm-20250501-vultr-x86_64-python-b8633f9aca9b198e5592-3.14.0a7%2B-b8633f9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.022x slower (HPT: reliability of 97.90%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250501-vultr-x86_64-python-b8633f9aca9b198e5592-3.14.0a7%2B-b8633f9-vs-3.13.0rc2.md)
- [📈time plot](bm-20250501-vultr-x86_64-python-b8633f9aca9b198e5592-3.14.0a7%2B-b8633f9-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.093x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250501-vultr-x86_64-python-b8633f9aca9b198e5592-3.14.0a7%2B-b8633f9-vs-base-mem.svg)
- [📄table](bm-20250501-vultr-x86_64-python-b8633f9aca9b198e5592-3.14.0a7%2B-b8633f9-vs-base.md)
- [📈time plot](bm-20250501-vultr-x86_64-python-b8633f9aca9b198e5592-3.14.0a7%2B-b8633f9-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14789446459)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250501-macm4pro-arm64-python-b8633f9aca9b198e5592-3.14.0a7%2B-b8633f9.json)

### vs. 3.12.6

- Geometric mean: 1.082x faster (HPT: reliability of 90.43%, 1.00x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250501-macm4pro-arm64-python-b8633f9aca9b198e5592-3.14.0a7%2B-b8633f9-vs-3.12.6.md)
- [📈time plot](bm-20250501-macm4pro-arm64-python-b8633f9aca9b198e5592-3.14.0a7%2B-b8633f9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.003x faster (HPT: reliability of 81.45%, 1.00x slower at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250501-macm4pro-arm64-python-b8633f9aca9b198e5592-3.14.0a7%2B-b8633f9-vs-3.13.0rc2.md)
- [📈time plot](bm-20250501-macm4pro-arm64-python-b8633f9aca9b198e5592-3.14.0a7%2B-b8633f9-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.015x slower (HPT: reliability of 98.26%, 1.00x slower at 99th %ile)
- Memory usage: 1.11x
- [🧠memory plot](bm-20250501-macm4pro-arm64-python-b8633f9aca9b198e5592-3.14.0a7%2B-b8633f9-vs-base-mem.svg)
- [📄table](bm-20250501-macm4pro-arm64-python-b8633f9aca9b198e5592-3.14.0a7%2B-b8633f9-vs-base.md)
- [📈time plot](bm-20250501-macm4pro-arm64-python-b8633f9aca9b198e5592-3.14.0a7%2B-b8633f9-vs-base.svg)

