# Results

- fork: python/bd2c7e8c8b10f4d31eab
- version: 3.15.0a1+
- config: NOGIL
- commit hash: [bd2c7e8](https://github.com/python/cpython/commit/bd2c7e8)
- commit date: 2025-10-22T16:11:48-07:00
- commit merge base: [e5f4299f138ef46378dc5766b33de7eb8937392b](https://github.com/python/cpython/commit/e5f4299f138ef46378dc5766b33de7eb8937392b)
- ref: bd2c7e8c8b10f4d31eab

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18733695179)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251022-vultr-x86_64-python-bd2c7e8c8b10f4d31eab-3.15.0a1%2B-bd2c7e8.json)

### vs. 3.12.6

- Geometric mean: 1.016x slower (HPT: reliability of 79.26%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251022-vultr-x86_64-python-bd2c7e8c8b10f4d31eab-3.15.0a1%2B-bd2c7e8-vs-3.12.6.md)
- [📈time plot](bm-20251022-vultr-x86_64-python-bd2c7e8c8b10f4d31eab-3.15.0a1%2B-bd2c7e8-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.049x slower (HPT: reliability of 95.52%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251022-vultr-x86_64-python-bd2c7e8c8b10f4d31eab-3.15.0a1%2B-bd2c7e8-vs-3.13.0rc2.md)
- [📈time plot](bm-20251022-vultr-x86_64-python-bd2c7e8c8b10f4d31eab-3.15.0a1%2B-bd2c7e8-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.088x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20251022-vultr-x86_64-python-bd2c7e8c8b10f4d31eab-3.15.0a1%2B-bd2c7e8-vs-base-mem.svg)
- [📄table](bm-20251022-vultr-x86_64-python-bd2c7e8c8b10f4d31eab-3.15.0a1%2B-bd2c7e8-vs-base.md)
- [📈time plot](bm-20251022-vultr-x86_64-python-bd2c7e8c8b10f4d31eab-3.15.0a1%2B-bd2c7e8-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18733695179)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251022-macm4pro-arm64-python-bd2c7e8c8b10f4d31eab-3.15.0a1%2B-bd2c7e8.json)

### vs. 3.12.6

- Geometric mean: 1.075x faster (HPT: reliability of 94.60%, 1.00x faster at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251022-macm4pro-arm64-python-bd2c7e8c8b10f4d31eab-3.15.0a1%2B-bd2c7e8-vs-3.12.6.md)
- [📈time plot](bm-20251022-macm4pro-arm64-python-bd2c7e8c8b10f4d31eab-3.15.0a1%2B-bd2c7e8-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.002x slower (HPT: reliability of 78.32%, 1.00x slower at 99th %ile)
- Memory usage: 1.29x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251022-macm4pro-arm64-python-bd2c7e8c8b10f4d31eab-3.15.0a1%2B-bd2c7e8-vs-3.13.0rc2.md)
- [📈time plot](bm-20251022-macm4pro-arm64-python-bd2c7e8c8b10f4d31eab-3.15.0a1%2B-bd2c7e8-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.008x slower (HPT: reliability of 97.76%, 1.00x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20251022-macm4pro-arm64-python-bd2c7e8c8b10f4d31eab-3.15.0a1%2B-bd2c7e8-vs-base-mem.svg)
- [📄table](bm-20251022-macm4pro-arm64-python-bd2c7e8c8b10f4d31eab-3.15.0a1%2B-bd2c7e8-vs-base.md)
- [📈time plot](bm-20251022-macm4pro-arm64-python-bd2c7e8c8b10f4d31eab-3.15.0a1%2B-bd2c7e8-vs-base.svg)

