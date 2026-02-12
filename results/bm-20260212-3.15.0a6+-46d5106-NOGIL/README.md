# Results

- fork: python/46d5106cfa903329821c
- version: 3.15.0a6+
- config: NOGIL
- commit hash: [46d5106](https://github.com/python/cpython/commit/46d5106)
- commit date: 2026-02-12T00:15:33Z
- commit merge base: [cac0c98450c27dbb6e185ab1c05e1d51d34135d9](https://github.com/python/cpython/commit/cac0c98450c27dbb6e185ab1c05e1d51d34135d9)
- commit date: 2026-02-12T00:15:33+00:00
- ref: 46d5106cfa903329821c

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21928845098)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260212-vultr-x86_64-python-46d5106cfa903329821c-3.15.0a6%2B-46d5106.json)

### vs. 3.12.6

- Geometric mean: 1.030x slower (HPT: reliability of 78.28%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260212-vultr-x86_64-python-46d5106cfa903329821c-3.15.0a6%2B-46d5106-vs-3.12.6.md)
- [📈time plot](bm-20260212-vultr-x86_64-python-46d5106cfa903329821c-3.15.0a6%2B-46d5106-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.063x slower (HPT: reliability of 89.81%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260212-vultr-x86_64-python-46d5106cfa903329821c-3.15.0a6%2B-46d5106-vs-3.13.0rc2.md)
- [📈time plot](bm-20260212-vultr-x86_64-python-46d5106cfa903329821c-3.15.0a6%2B-46d5106-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.098x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20260212-vultr-x86_64-python-46d5106cfa903329821c-3.15.0a6%2B-46d5106-vs-base-mem.svg)
- [📄table](bm-20260212-vultr-x86_64-python-46d5106cfa903329821c-3.15.0a6%2B-46d5106-vs-base.md)
- [📈time plot](bm-20260212-vultr-x86_64-python-46d5106cfa903329821c-3.15.0a6%2B-46d5106-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21928845098)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260212-macm4pro-arm64-python-46d5106cfa903329821c-3.15.0a6%2B-46d5106.json)

### vs. 3.12.6

- Geometric mean: 1.090x faster (HPT: reliability of 99.83%, 1.00x faster at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260212-macm4pro-arm64-python-46d5106cfa903329821c-3.15.0a6%2B-46d5106-vs-3.12.6.md)
- [📈time plot](bm-20260212-macm4pro-arm64-python-46d5106cfa903329821c-3.15.0a6%2B-46d5106-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.011x faster (HPT: reliability of 63.22%, 1.00x slower at 99th %ile)
- Memory usage: 1.30x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260212-macm4pro-arm64-python-46d5106cfa903329821c-3.15.0a6%2B-46d5106-vs-3.13.0rc2.md)
- [📈time plot](bm-20260212-macm4pro-arm64-python-46d5106cfa903329821c-3.15.0a6%2B-46d5106-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.061x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.10x
- [🧠memory plot](bm-20260212-macm4pro-arm64-python-46d5106cfa903329821c-3.15.0a6%2B-46d5106-vs-base-mem.svg)
- [📄table](bm-20260212-macm4pro-arm64-python-46d5106cfa903329821c-3.15.0a6%2B-46d5106-vs-base.md)
- [📈time plot](bm-20260212-macm4pro-arm64-python-46d5106cfa903329821c-3.15.0a6%2B-46d5106-vs-base.svg)

