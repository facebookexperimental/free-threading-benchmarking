# Results

- fork: python/f96f7c9f5b5db35e8a22
- version: 3.15.0a0
- config: NOGIL
- commit hash: [f96f7c9](https://github.com/python/cpython/commit/f96f7c9)
- commit date: 2025-09-11T17:05:37-04:00
- commit merge base: [5bd4bf04c4ac1ad67760e0b7852a05e796741e6f](https://github.com/python/cpython/commit/5bd4bf04c4ac1ad67760e0b7852a05e796741e6f)
- ref: f96f7c9f5b5db35e8a22

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17660804751)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250911-vultr-x86_64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9.json)

### vs. 3.12.6

- Geometric mean: 1.015x slower (HPT: reliability of 82.02%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250911-vultr-x86_64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9-vs-3.12.6.md)
- [📈time plot](bm-20250911-vultr-x86_64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.049x slower (HPT: reliability of 90.96%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250911-vultr-x86_64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9-vs-3.13.0rc2.md)
- [📈time plot](bm-20250911-vultr-x86_64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.087x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20250911-vultr-x86_64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9-vs-base-mem.svg)
- [📄table](bm-20250911-vultr-x86_64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9-vs-base.md)
- [📈time plot](bm-20250911-vultr-x86_64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17660804751)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250911-macm4pro-arm64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9.json)

### vs. 3.12.6

- Geometric mean: 1.079x faster (HPT: reliability of 91.29%, 1.00x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250911-macm4pro-arm64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9-vs-3.12.6.md)
- [📈time plot](bm-20250911-macm4pro-arm64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.001x faster (HPT: reliability of 76.65%, 1.00x slower at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250911-macm4pro-arm64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9-vs-3.13.0rc2.md)
- [📈time plot](bm-20250911-macm4pro-arm64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.025x slower (HPT: reliability of 99.52%, 1.00x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20250911-macm4pro-arm64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9-vs-base-mem.svg)
- [📄table](bm-20250911-macm4pro-arm64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9-vs-base.md)
- [📈time plot](bm-20250911-macm4pro-arm64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9-vs-base.svg)

