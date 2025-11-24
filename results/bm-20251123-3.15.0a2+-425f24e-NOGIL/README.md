# Results

- fork: python/425f24e4fad672c21130
- version: 3.15.0a2+
- config: NOGIL
- commit hash: [425f24e](https://github.com/python/cpython/commit/425f24e)
- commit date: 2025-11-23T15:37:15-08:00
- commit merge base: [23b67aa037cbb89b2a3d2c5fc716ca18f5b15b87](https://github.com/python/cpython/commit/23b67aa037cbb89b2a3d2c5fc716ca18f5b15b87)
- ref: 425f24e4fad672c21130

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19619725789)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251123-vultr-x86_64-python-425f24e4fad672c21130-3.15.0a2%2B-425f24e.json)

### vs. 3.12.6

- Geometric mean: 1.021x slower (HPT: reliability of 75.36%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251123-vultr-x86_64-python-425f24e4fad672c21130-3.15.0a2%2B-425f24e-vs-3.12.6.md)
- [📈time plot](bm-20251123-vultr-x86_64-python-425f24e4fad672c21130-3.15.0a2%2B-425f24e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.054x slower (HPT: reliability of 92.07%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251123-vultr-x86_64-python-425f24e4fad672c21130-3.15.0a2%2B-425f24e-vs-3.13.0rc2.md)
- [📈time plot](bm-20251123-vultr-x86_64-python-425f24e4fad672c21130-3.15.0a2%2B-425f24e-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19619725789)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251123-macm4pro-arm64-python-425f24e4fad672c21130-3.15.0a2%2B-425f24e.json)

### vs. 3.12.6

- Geometric mean: 1.103x faster (HPT: reliability of 99.87%, 1.01x faster at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251123-macm4pro-arm64-python-425f24e4fad672c21130-3.15.0a2%2B-425f24e-vs-3.12.6.md)
- [📈time plot](bm-20251123-macm4pro-arm64-python-425f24e4fad672c21130-3.15.0a2%2B-425f24e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.017x faster (HPT: reliability of 54.50%, 1.00x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251123-macm4pro-arm64-python-425f24e4fad672c21130-3.15.0a2%2B-425f24e-vs-3.13.0rc2.md)
- [📈time plot](bm-20251123-macm4pro-arm64-python-425f24e4fad672c21130-3.15.0a2%2B-425f24e-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.030x slower (HPT: reliability of 99.93%, 1.01x slower at 99th %ile)
- Memory usage: 1.11x
- [🧠memory plot](bm-20251123-macm4pro-arm64-python-425f24e4fad672c21130-3.15.0a2%2B-425f24e-vs-base-mem.svg)
- [📄table](bm-20251123-macm4pro-arm64-python-425f24e4fad672c21130-3.15.0a2%2B-425f24e-vs-base.md)
- [📈time plot](bm-20251123-macm4pro-arm64-python-425f24e4fad672c21130-3.15.0a2%2B-425f24e-vs-base.svg)

