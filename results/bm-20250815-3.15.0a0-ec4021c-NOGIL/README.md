# Results

- fork: python/ec4021c6d73407fd4d22
- version: 3.15.0a0
- config: NOGIL
- commit hash: [ec4021c](https://github.com/python/cpython/commit/ec4021c)
- commit date: 2025-08-15T14:19:23-07:00
- commit merge base: [d86c2257a69a8d6c650c0db470499463131a569f](https://github.com/python/cpython/commit/d86c2257a69a8d6c650c0db470499463131a569f)
- ref: ec4021c6d73407fd4d22

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17002036517)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250815-vultr-x86_64-python-ec4021c6d73407fd4d22-3.15.0a0-ec4021c.json)

### vs. 3.12.6

- Geometric mean: 1.024x slower (HPT: reliability of 96.55%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250815-vultr-x86_64-python-ec4021c6d73407fd4d22-3.15.0a0-ec4021c-vs-3.12.6.md)
- [📈time plot](bm-20250815-vultr-x86_64-python-ec4021c6d73407fd4d22-3.15.0a0-ec4021c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.057x slower (HPT: reliability of 98.42%, 1.00x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250815-vultr-x86_64-python-ec4021c6d73407fd4d22-3.15.0a0-ec4021c-vs-3.13.0rc2.md)
- [📈time plot](bm-20250815-vultr-x86_64-python-ec4021c6d73407fd4d22-3.15.0a0-ec4021c-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.092x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20250815-vultr-x86_64-python-ec4021c6d73407fd4d22-3.15.0a0-ec4021c-vs-base-mem.svg)
- [📄table](bm-20250815-vultr-x86_64-python-ec4021c6d73407fd4d22-3.15.0a0-ec4021c-vs-base.md)
- [📈time plot](bm-20250815-vultr-x86_64-python-ec4021c6d73407fd4d22-3.15.0a0-ec4021c-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17002036517)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250815-macm4pro-arm64-python-ec4021c6d73407fd4d22-3.15.0a0-ec4021c.json)

### vs. 3.12.6

- Geometric mean: 1.074x faster (HPT: reliability of 91.58%, 1.00x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250815-macm4pro-arm64-python-ec4021c6d73407fd4d22-3.15.0a0-ec4021c-vs-3.12.6.md)
- [📈time plot](bm-20250815-macm4pro-arm64-python-ec4021c6d73407fd4d22-3.15.0a0-ec4021c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.004x slower (HPT: reliability of 89.25%, 1.00x slower at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250815-macm4pro-arm64-python-ec4021c6d73407fd4d22-3.15.0a0-ec4021c-vs-3.13.0rc2.md)
- [📈time plot](bm-20250815-macm4pro-arm64-python-ec4021c6d73407fd4d22-3.15.0a0-ec4021c-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.001x slower (HPT: reliability of 83.14%, 1.00x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20250815-macm4pro-arm64-python-ec4021c6d73407fd4d22-3.15.0a0-ec4021c-vs-base-mem.svg)
- [📄table](bm-20250815-macm4pro-arm64-python-ec4021c6d73407fd4d22-3.15.0a0-ec4021c-vs-base.md)
- [📈time plot](bm-20250815-macm4pro-arm64-python-ec4021c6d73407fd4d22-3.15.0a0-ec4021c-vs-base.svg)

