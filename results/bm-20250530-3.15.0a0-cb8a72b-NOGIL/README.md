# Results

- fork: python/cb8a72b301f47e76d93a
- version: 3.15.0a0
- config: NOGIL
- commit hash: [cb8a72b](https://github.com/python/cpython/commit/cb8a72b)
- commit date: 2025-05-30T00:32:44+03:00
- commit merge base: [dafd14146f7ca18932894ea445a2f9f98f2a8b01](https://github.com/python/cpython/commit/dafd14146f7ca18932894ea445a2f9f98f2a8b01)
- ref: cb8a72b301f47e76d93a

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15336368625)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250530-vultr-x86_64-python-cb8a72b301f47e76d93a-3.15.0a0-cb8a72b.json)

### vs. 3.12.6

- Geometric mean: 1.015x faster (HPT: reliability of 89.56%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250530-vultr-x86_64-python-cb8a72b301f47e76d93a-3.15.0a0-cb8a72b-vs-3.12.6.md)
- [📈time plot](bm-20250530-vultr-x86_64-python-cb8a72b301f47e76d93a-3.15.0a0-cb8a72b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.020x slower (HPT: reliability of 95.87%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250530-vultr-x86_64-python-cb8a72b301f47e76d93a-3.15.0a0-cb8a72b-vs-3.13.0rc2.md)
- [📈time plot](bm-20250530-vultr-x86_64-python-cb8a72b301f47e76d93a-3.15.0a0-cb8a72b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.086x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.22x
- [🧠memory plot](bm-20250530-vultr-x86_64-python-cb8a72b301f47e76d93a-3.15.0a0-cb8a72b-vs-base-mem.svg)
- [📄table](bm-20250530-vultr-x86_64-python-cb8a72b301f47e76d93a-3.15.0a0-cb8a72b-vs-base.md)
- [📈time plot](bm-20250530-vultr-x86_64-python-cb8a72b301f47e76d93a-3.15.0a0-cb8a72b-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15336368625)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250530-macm4pro-arm64-python-cb8a72b301f47e76d93a-3.15.0a0-cb8a72b.json)

### vs. 3.12.6

- Geometric mean: 1.096x faster (HPT: reliability of 98.44%, 1.00x faster at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250530-macm4pro-arm64-python-cb8a72b301f47e76d93a-3.15.0a0-cb8a72b-vs-3.12.6.md)
- [📈time plot](bm-20250530-macm4pro-arm64-python-cb8a72b301f47e76d93a-3.15.0a0-cb8a72b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.017x faster (HPT: reliability of 61.78%, 1.00x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250530-macm4pro-arm64-python-cb8a72b301f47e76d93a-3.15.0a0-cb8a72b-vs-3.13.0rc2.md)
- [📈time plot](bm-20250530-macm4pro-arm64-python-cb8a72b301f47e76d93a-3.15.0a0-cb8a72b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.014x slower (HPT: reliability of 97.42%, 1.00x slower at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: 🔴 dask
- [🧠memory plot](bm-20250530-macm4pro-arm64-python-cb8a72b301f47e76d93a-3.15.0a0-cb8a72b-vs-base-mem.svg)
- [📄table](bm-20250530-macm4pro-arm64-python-cb8a72b301f47e76d93a-3.15.0a0-cb8a72b-vs-base.md)
- [📈time plot](bm-20250530-macm4pro-arm64-python-cb8a72b301f47e76d93a-3.15.0a0-cb8a72b-vs-base.svg)

