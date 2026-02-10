# Results

- fork: python/a9b6788ae6f045d83e89
- version: 3.15.0a5+
- config: NOGIL
- commit hash: [a9b6788](https://github.com/python/cpython/commit/a9b6788)
- commit date: 2026-02-10T00:01:17Z
- commit merge base: [30cfe6ee23a8974625c9860bc401f60ed75b2dea](https://github.com/python/cpython/commit/30cfe6ee23a8974625c9860bc401f60ed75b2dea)
- commit date: 2026-02-10T00:01:17+00:00
- ref: a9b6788ae6f045d83e89

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21846880236)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260210-vultr-x86_64-python-a9b6788ae6f045d83e89-3.15.0a5%2B-a9b6788.json)

### vs. 3.12.6

- Geometric mean: 1.030x slower (HPT: reliability of 81.51%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260210-vultr-x86_64-python-a9b6788ae6f045d83e89-3.15.0a5%2B-a9b6788-vs-3.12.6.md)
- [📈time plot](bm-20260210-vultr-x86_64-python-a9b6788ae6f045d83e89-3.15.0a5%2B-a9b6788-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.063x slower (HPT: reliability of 89.81%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260210-vultr-x86_64-python-a9b6788ae6f045d83e89-3.15.0a5%2B-a9b6788-vs-3.13.0rc2.md)
- [📈time plot](bm-20260210-vultr-x86_64-python-a9b6788ae6f045d83e89-3.15.0a5%2B-a9b6788-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.105x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20260210-vultr-x86_64-python-a9b6788ae6f045d83e89-3.15.0a5%2B-a9b6788-vs-base-mem.svg)
- [📄table](bm-20260210-vultr-x86_64-python-a9b6788ae6f045d83e89-3.15.0a5%2B-a9b6788-vs-base.md)
- [📈time plot](bm-20260210-vultr-x86_64-python-a9b6788ae6f045d83e89-3.15.0a5%2B-a9b6788-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21846880236)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260210-macm4pro-arm64-python-a9b6788ae6f045d83e89-3.15.0a5%2B-a9b6788.json)

### vs. 3.12.6

- Geometric mean: 1.110x faster (HPT: reliability of 99.99%, 1.02x faster at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260210-macm4pro-arm64-python-a9b6788ae6f045d83e89-3.15.0a5%2B-a9b6788-vs-3.12.6.md)
- [📈time plot](bm-20260210-macm4pro-arm64-python-a9b6788ae6f045d83e89-3.15.0a5%2B-a9b6788-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.030x faster (HPT: reliability of 72.87%, 1.00x faster at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260210-macm4pro-arm64-python-a9b6788ae6f045d83e89-3.15.0a5%2B-a9b6788-vs-3.13.0rc2.md)
- [📈time plot](bm-20260210-macm4pro-arm64-python-a9b6788ae6f045d83e89-3.15.0a5%2B-a9b6788-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.054x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.10x
- [🧠memory plot](bm-20260210-macm4pro-arm64-python-a9b6788ae6f045d83e89-3.15.0a5%2B-a9b6788-vs-base-mem.svg)
- [📄table](bm-20260210-macm4pro-arm64-python-a9b6788ae6f045d83e89-3.15.0a5%2B-a9b6788-vs-base.md)
- [📈time plot](bm-20260210-macm4pro-arm64-python-a9b6788ae6f045d83e89-3.15.0a5%2B-a9b6788-vs-base.svg)

