# Results

- fork: python/98b4cd6fe9348ac24d5c
- version: 3.15.0a0
- config: NOGIL
- commit hash: [98b4cd6](https://github.com/python/cpython/commit/98b4cd6)
- commit date: 2025-09-02T21:29:05+01:00
- commit merge base: [32032ee376fe20670e9a35e56beff48e59201261](https://github.com/python/cpython/commit/32032ee376fe20670e9a35e56beff48e59201261)
- ref: 98b4cd6fe9348ac24d5c

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17419368235)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250902-vultr-x86_64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6.json)

### vs. 3.12.6

- Geometric mean: 1.029x slower (HPT: reliability of 89.20%, 1.00x slower at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250902-vultr-x86_64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6-vs-3.12.6.md)
- [📈time plot](bm-20250902-vultr-x86_64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.061x slower (HPT: reliability of 98.63%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250902-vultr-x86_64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6-vs-3.13.0rc2.md)
- [📈time plot](bm-20250902-vultr-x86_64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.094x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20250902-vultr-x86_64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6-vs-base-mem.svg)
- [📄table](bm-20250902-vultr-x86_64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6-vs-base.md)
- [📈time plot](bm-20250902-vultr-x86_64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17419368235)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6.json)

### vs. 3.12.6

- Geometric mean: 1.075x faster (HPT: reliability of 93.22%, 1.00x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6-vs-3.12.6.md)
- [📈time plot](bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.003x slower (HPT: reliability of 83.46%, 1.00x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6-vs-3.13.0rc2.md)
- [📈time plot](bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.022x slower (HPT: reliability of 99.71%, 1.00x slower at 99th %ile)
- Memory usage: 1.11x
- [🧠memory plot](bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6-vs-base-mem.svg)
- [📄table](bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6-vs-base.md)
- [📈time plot](bm-20250902-macm4pro-arm64-python-98b4cd6fe9348ac24d5c-3.15.0a0-98b4cd6-vs-base.svg)

