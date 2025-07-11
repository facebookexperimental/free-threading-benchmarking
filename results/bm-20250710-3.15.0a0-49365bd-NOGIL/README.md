# Results

- fork: python/49365bd110a254a6a304
- version: 3.15.0a0
- config: NOGIL
- commit hash: [49365bd](https://github.com/python/cpython/commit/49365bd)
- commit date: 2025-07-10T16:49:09-07:00
- commit merge base: [56c6f04b8862c20ff6eddc4400f170ad91e55f66](https://github.com/python/cpython/commit/56c6f04b8862c20ff6eddc4400f170ad91e55f66)
- ref: 49365bd110a254a6a304

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16208933228)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250710-vultr-x86_64-python-49365bd110a254a6a304-3.15.0a0-49365bd.json)

### vs. 3.12.6

- Geometric mean: 1.025x slower (HPT: reliability of 95.20%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250710-vultr-x86_64-python-49365bd110a254a6a304-3.15.0a0-49365bd-vs-3.12.6.md)
- [📈time plot](bm-20250710-vultr-x86_64-python-49365bd110a254a6a304-3.15.0a0-49365bd-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.057x slower (HPT: reliability of 97.97%, 1.00x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250710-vultr-x86_64-python-49365bd110a254a6a304-3.15.0a0-49365bd-vs-3.13.0rc2.md)
- [📈time plot](bm-20250710-vultr-x86_64-python-49365bd110a254a6a304-3.15.0a0-49365bd-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.095x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20250710-vultr-x86_64-python-49365bd110a254a6a304-3.15.0a0-49365bd-vs-base-mem.svg)
- [📄table](bm-20250710-vultr-x86_64-python-49365bd110a254a6a304-3.15.0a0-49365bd-vs-base.md)
- [📈time plot](bm-20250710-vultr-x86_64-python-49365bd110a254a6a304-3.15.0a0-49365bd-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16208933228)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250710-macm4pro-arm64-python-49365bd110a254a6a304-3.15.0a0-49365bd.json)

### vs. 3.12.6

- Geometric mean: 1.093x faster (HPT: reliability of 95.75%, 1.00x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250710-macm4pro-arm64-python-49365bd110a254a6a304-3.15.0a0-49365bd-vs-3.12.6.md)
- [📈time plot](bm-20250710-macm4pro-arm64-python-49365bd110a254a6a304-3.15.0a0-49365bd-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.014x faster (HPT: reliability of 79.92%, 1.00x slower at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250710-macm4pro-arm64-python-49365bd110a254a6a304-3.15.0a0-49365bd-vs-3.13.0rc2.md)
- [📈time plot](bm-20250710-macm4pro-arm64-python-49365bd110a254a6a304-3.15.0a0-49365bd-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.002x faster (HPT: reliability of 91.22%, 1.00x slower at 99th %ile)
- Memory usage: 1.11x
- [🧠memory plot](bm-20250710-macm4pro-arm64-python-49365bd110a254a6a304-3.15.0a0-49365bd-vs-base-mem.svg)
- [📄table](bm-20250710-macm4pro-arm64-python-49365bd110a254a6a304-3.15.0a0-49365bd-vs-base.md)
- [📈time plot](bm-20250710-macm4pro-arm64-python-49365bd110a254a6a304-3.15.0a0-49365bd-vs-base.svg)

