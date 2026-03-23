# Results

- fork: python/fb8d8d9c9f9cbc94fa58
- version: 3.15.0a7+
- config: NOGIL
- commit hash: [fb8d8d9](https://github.com/python/cpython/commit/fb8d8d9)
- commit date: 2026-03-22T19:58:31-04:00
- commit merge base: [4561f6418a691b3e89aef0901f53fe0dfb7f7c0e](https://github.com/python/cpython/commit/4561f6418a691b3e89aef0901f53fe0dfb7f7c0e)
- ref: fb8d8d9c9f9cbc94fa58

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/23416519586)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260322-vultr-x86_64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7%2B-fb8d8d9.json)

### vs. 3.12.6

- Geometric mean: 1.031x slower (HPT: reliability of 80.73%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260322-vultr-x86_64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7%2B-fb8d8d9-vs-3.12.6.md)
- [📈time plot](bm-20260322-vultr-x86_64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7%2B-fb8d8d9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.063x slower (HPT: reliability of 96.62%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260322-vultr-x86_64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7%2B-fb8d8d9-vs-3.13.0rc2.md)
- [📈time plot](bm-20260322-vultr-x86_64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7%2B-fb8d8d9-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.097x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20260322-vultr-x86_64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7%2B-fb8d8d9-vs-base-mem.svg)
- [📄table](bm-20260322-vultr-x86_64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7%2B-fb8d8d9-vs-base.md)
- [📈time plot](bm-20260322-vultr-x86_64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7%2B-fb8d8d9-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/23416519586)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260322-macm4pro-arm64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7%2B-fb8d8d9.json)

### vs. 3.12.6

- Geometric mean: 1.107x faster (HPT: reliability of 99.95%, 1.01x faster at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260322-macm4pro-arm64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7%2B-fb8d8d9-vs-3.12.6.md)
- [📈time plot](bm-20260322-macm4pro-arm64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7%2B-fb8d8d9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.027x faster (HPT: reliability of 62.52%, 1.00x faster at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260322-macm4pro-arm64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7%2B-fb8d8d9-vs-3.13.0rc2.md)
- [📈time plot](bm-20260322-macm4pro-arm64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7%2B-fb8d8d9-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.045x slower (HPT: reliability of 100.00%, 1.03x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20260322-macm4pro-arm64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7%2B-fb8d8d9-vs-base-mem.svg)
- [📄table](bm-20260322-macm4pro-arm64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7%2B-fb8d8d9-vs-base.md)
- [📈time plot](bm-20260322-macm4pro-arm64-python-fb8d8d9c9f9cbc94fa58-3.15.0a7%2B-fb8d8d9-vs-base.svg)

