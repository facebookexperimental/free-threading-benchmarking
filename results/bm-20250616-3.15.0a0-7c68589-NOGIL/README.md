# Results

- fork: python/7c685894cd9c2c669f09
- version: 3.15.0a0
- config: NOGIL
- commit hash: [7c68589](https://github.com/python/cpython/commit/7c68589)
- commit date: 2025-06-16T19:35:59-04:00
- commit merge base: [a450a0ddec7a2813fb4603f0df406fa33750654a](https://github.com/python/cpython/commit/a450a0ddec7a2813fb4603f0df406fa33750654a)
- ref: 7c685894cd9c2c669f09

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15695010937)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250616-vultr-x86_64-python-7c685894cd9c2c669f09-3.15.0a0-7c68589.json)

### vs. 3.12.6

- Geometric mean: 1.012x faster (HPT: reliability of 88.75%, 1.00x slower at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250616-vultr-x86_64-python-7c685894cd9c2c669f09-3.15.0a0-7c68589-vs-3.12.6.md)
- [📈time plot](bm-20250616-vultr-x86_64-python-7c685894cd9c2c669f09-3.15.0a0-7c68589-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.023x slower (HPT: reliability of 94.75%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250616-vultr-x86_64-python-7c685894cd9c2c669f09-3.15.0a0-7c68589-vs-3.13.0rc2.md)
- [📈time plot](bm-20250616-vultr-x86_64-python-7c685894cd9c2c669f09-3.15.0a0-7c68589-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.092x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.22x
- [🧠memory plot](bm-20250616-vultr-x86_64-python-7c685894cd9c2c669f09-3.15.0a0-7c68589-vs-base-mem.svg)
- [📄table](bm-20250616-vultr-x86_64-python-7c685894cd9c2c669f09-3.15.0a0-7c68589-vs-base.md)
- [📈time plot](bm-20250616-vultr-x86_64-python-7c685894cd9c2c669f09-3.15.0a0-7c68589-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15695010937)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250616-macm4pro-arm64-python-7c685894cd9c2c669f09-3.15.0a0-7c68589.json)

### vs. 3.12.6

- Geometric mean: 1.091x faster (HPT: reliability of 96.80%, 1.00x faster at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250616-macm4pro-arm64-python-7c685894cd9c2c669f09-3.15.0a0-7c68589-vs-3.12.6.md)
- [📈time plot](bm-20250616-macm4pro-arm64-python-7c685894cd9c2c669f09-3.15.0a0-7c68589-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.013x faster (HPT: reliability of 79.40%, 1.00x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250616-macm4pro-arm64-python-7c685894cd9c2c669f09-3.15.0a0-7c68589-vs-3.13.0rc2.md)
- [📈time plot](bm-20250616-macm4pro-arm64-python-7c685894cd9c2c669f09-3.15.0a0-7c68589-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.014x slower (HPT: reliability of 95.64%, 1.00x slower at 99th %ile)
- Memory usage: 1.13x
- [🧠memory plot](bm-20250616-macm4pro-arm64-python-7c685894cd9c2c669f09-3.15.0a0-7c68589-vs-base-mem.svg)
- [📄table](bm-20250616-macm4pro-arm64-python-7c685894cd9c2c669f09-3.15.0a0-7c68589-vs-base.md)
- [📈time plot](bm-20250616-macm4pro-arm64-python-7c685894cd9c2c669f09-3.15.0a0-7c68589-vs-base.svg)

