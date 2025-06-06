# Results

- fork: python/71cf4dd622832848cace
- version: 3.15.0a0
- config: 
- commit hash: [71cf4dd](https://github.com/python/cpython/commit/71cf4dd)
- commit date: 2025-05-16T23:29:14+03:00
- commit merge base: [ea2d707bd59963bd4f53407108026930ff12ae56](https://github.com/python/cpython/commit/ea2d707bd59963bd4f53407108026930ff12ae56)
- ref: 71cf4dd622832848cace

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15079689200)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250516-vultr-x86_64-python-71cf4dd622832848cace-3.15.0a0-71cf4dd.json)

### vs. 3.12.6

- Geometric mean: 1.106x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250516-vultr-x86_64-python-71cf4dd622832848cace-3.15.0a0-71cf4dd-vs-3.12.6.md)
- [📈time plot](bm-20250516-vultr-x86_64-python-71cf4dd622832848cace-3.15.0a0-71cf4dd-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.068x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250516-vultr-x86_64-python-71cf4dd622832848cace-3.15.0a0-71cf4dd-vs-3.13.0rc2.md)
- [📈time plot](bm-20250516-vultr-x86_64-python-71cf4dd622832848cace-3.15.0a0-71cf4dd-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15079689200)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250516-macm4pro-arm64-python-71cf4dd622832848cace-3.15.0a0-71cf4dd.json)

### vs. 3.12.6

- Geometric mean: 1.105x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250516-macm4pro-arm64-python-71cf4dd622832848cace-3.15.0a0-71cf4dd-vs-3.12.6.md)
- [📈time plot](bm-20250516-macm4pro-arm64-python-71cf4dd622832848cace-3.15.0a0-71cf4dd-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.025x faster (HPT: reliability of 87.96%, 1.00x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250516-macm4pro-arm64-python-71cf4dd622832848cace-3.15.0a0-71cf4dd-vs-3.13.0rc2.md)
- [📈time plot](bm-20250516-macm4pro-arm64-python-71cf4dd622832848cace-3.15.0a0-71cf4dd-vs-3.13.0rc2.svg)

