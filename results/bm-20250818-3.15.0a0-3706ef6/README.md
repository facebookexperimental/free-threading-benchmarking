# Results

- fork: python/3706ef66eff2b9e24091
- version: 3.15.0a0
- config: 
- commit hash: [3706ef6](https://github.com/python/cpython/commit/3706ef6)
- commit date: 2025-08-18T20:57:36Z
- commit merge base: [8750e5ecfcfbc337efb511046d34f28b2d26bd68](https://github.com/python/cpython/commit/8750e5ecfcfbc337efb511046d34f28b2d26bd68)
- commit date: 2025-08-18T20:57:36+00:00
- ref: 3706ef66eff2b9e24091

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17056040302)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250818-vultr-x86_64-python-3706ef66eff2b9e24091-3.15.0a0-3706ef6.json)

### vs. 3.12.6

- Geometric mean: 1.066x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250818-vultr-x86_64-python-3706ef66eff2b9e24091-3.15.0a0-3706ef6-vs-3.12.6.md)
- [📈time plot](bm-20250818-vultr-x86_64-python-3706ef66eff2b9e24091-3.15.0a0-3706ef6-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.031x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250818-vultr-x86_64-python-3706ef66eff2b9e24091-3.15.0a0-3706ef6-vs-3.13.0rc2.md)
- [📈time plot](bm-20250818-vultr-x86_64-python-3706ef66eff2b9e24091-3.15.0a0-3706ef6-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17056040302)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250818-macm4pro-arm64-python-3706ef66eff2b9e24091-3.15.0a0-3706ef6.json)

### vs. 3.12.6

- Geometric mean: 1.086x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250818-macm4pro-arm64-python-3706ef66eff2b9e24091-3.15.0a0-3706ef6-vs-3.12.6.md)
- [📈time plot](bm-20250818-macm4pro-arm64-python-3706ef66eff2b9e24091-3.15.0a0-3706ef6-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.007x faster (HPT: reliability of 50.44%, 1.00x slower at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250818-macm4pro-arm64-python-3706ef66eff2b9e24091-3.15.0a0-3706ef6-vs-3.13.0rc2.md)
- [📈time plot](bm-20250818-macm4pro-arm64-python-3706ef66eff2b9e24091-3.15.0a0-3706ef6-vs-3.13.0rc2.svg)

