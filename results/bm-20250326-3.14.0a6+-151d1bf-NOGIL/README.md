# Results

- fork: python/151d1bfd1bb7ca9a36bb
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [151d1bf](https://github.com/python/cpython/commit/151d1bf)
- commit date: 2025-03-26T18:36:04-04:00
- commit merge base: [52b5eb95b770fa00ebbd449ba40cab4a0e7c7df7](https://github.com/python/cpython/commit/52b5eb95b770fa00ebbd449ba40cab4a0e7c7df7)
- ref: 151d1bfd1bb7ca9a36bb

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14096104884)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6%2B-151d1bf.json)

### vs. 3.12.6

- Geometric mean: 1.007x slower (HPT: reliability of 98.76%, 1.00x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6%2B-151d1bf-vs-3.12.6.md)
- [📈time plot](bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6%2B-151d1bf-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.043x slower (HPT: reliability of 99.32%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6%2B-151d1bf-vs-3.13.0rc2.md)
- [📈time plot](bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6%2B-151d1bf-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.111x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6%2B-151d1bf-vs-base-mem.svg)
- [📄table](bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6%2B-151d1bf-vs-base.md)
- [📈time plot](bm-20250326-linux-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6%2B-151d1bf-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14096104884)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250326-vultr-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6%2B-151d1bf.json)

### vs. 3.12.6

- Geometric mean: 1.093x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250326-vultr-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6%2B-151d1bf-vs-3.12.6.md)
- [📈time plot](bm-20250326-vultr-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6%2B-151d1bf-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.123x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250326-vultr-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6%2B-151d1bf-vs-3.13.0rc2.md)
- [📈time plot](bm-20250326-vultr-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6%2B-151d1bf-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.181x slower (HPT: reliability of 100.00%, 1.18x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250326-vultr-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6%2B-151d1bf-vs-base-mem.svg)
- [📄table](bm-20250326-vultr-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6%2B-151d1bf-vs-base.md)
- [📈time plot](bm-20250326-vultr-x86_64-python-151d1bfd1bb7ca9a36bb-3.14.0a6%2B-151d1bf-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14096104884)
- cpu model: missing
- platform: macOS-15.3.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6%2B-151d1bf.json)

### vs. 3.12.6

- Geometric mean: 1.065x slower (HPT: reliability of 99.97%, 1.04x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6%2B-151d1bf-vs-3.12.6.md)
- [📈time plot](bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6%2B-151d1bf-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.132x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6%2B-151d1bf-vs-3.13.0rc2.md)
- [📈time plot](bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6%2B-151d1bf-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.080x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: 🔴 dask
- [🧠memory plot](bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6%2B-151d1bf-vs-base-mem.svg)
- [📄table](bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6%2B-151d1bf-vs-base.md)
- [📈time plot](bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6%2B-151d1bf-vs-base.svg)

