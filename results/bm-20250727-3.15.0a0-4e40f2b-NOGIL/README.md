# Results

- fork: python/4e40f2bea7edfa5ba7e2
- version: 3.15.0a0
- config: NOGIL
- commit hash: [4e40f2b](https://github.com/python/cpython/commit/4e40f2b)
- commit date: 2025-07-27T12:59:08-07:00
- commit merge base: [6784ef7da7cbf1a944fd0685630ced54e4a0066c](https://github.com/python/cpython/commit/6784ef7da7cbf1a944fd0685630ced54e4a0066c)
- ref: 4e40f2bea7edfa5ba7e2

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16557232628)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b.json)

### vs. 3.12.6

- Geometric mean: 1.027x slower (HPT: reliability of 97.43%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b-vs-3.12.6.md)
- [📈time plot](bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.059x slower (HPT: reliability of 98.49%, 1.00x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b-vs-3.13.0rc2.md)
- [📈time plot](bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.093x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b-vs-base-mem.svg)
- [📄table](bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b-vs-base.md)
- [📈time plot](bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16557232628)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250727-macm4pro-arm64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b.json)

### vs. 3.12.6

- Geometric mean: 1.091x faster (HPT: reliability of 98.10%, 1.00x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250727-macm4pro-arm64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b-vs-3.12.6.md)
- [📈time plot](bm-20250727-macm4pro-arm64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.012x faster (HPT: reliability of 59.53%, 1.00x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250727-macm4pro-arm64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b-vs-3.13.0rc2.md)
- [📈time plot](bm-20250727-macm4pro-arm64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.008x slower (HPT: reliability of 92.63%, 1.00x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20250727-macm4pro-arm64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b-vs-base-mem.svg)
- [📄table](bm-20250727-macm4pro-arm64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b-vs-base.md)
- [📈time plot](bm-20250727-macm4pro-arm64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b-vs-base.svg)

