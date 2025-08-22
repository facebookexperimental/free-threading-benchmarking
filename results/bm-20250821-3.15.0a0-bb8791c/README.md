# Results

- fork: python/bb8791c0b75b5970d109
- version: 3.15.0a0
- config: 
- commit hash: [bb8791c](https://github.com/python/cpython/commit/bb8791c)
- commit date: 2025-08-21T23:12:17+01:00
- commit merge base: [79aeeb880ed968dd49e2807ad1e62ad8174c1361](https://github.com/python/cpython/commit/79aeeb880ed968dd49e2807ad1e62ad8174c1361)
- ref: bb8791c0b75b5970d109

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17142539550)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250821-vultr-x86_64-python-bb8791c0b75b5970d109-3.15.0a0-bb8791c.json)

### vs. 3.12.6

- Geometric mean: 1.074x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250821-vultr-x86_64-python-bb8791c0b75b5970d109-3.15.0a0-bb8791c-vs-3.12.6.md)
- [📈time plot](bm-20250821-vultr-x86_64-python-bb8791c0b75b5970d109-3.15.0a0-bb8791c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.038x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250821-vultr-x86_64-python-bb8791c0b75b5970d109-3.15.0a0-bb8791c-vs-3.13.0rc2.md)
- [📈time plot](bm-20250821-vultr-x86_64-python-bb8791c0b75b5970d109-3.15.0a0-bb8791c-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17142539550)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250821-macm4pro-arm64-python-bb8791c0b75b5970d109-3.15.0a0-bb8791c.json)

### vs. 3.12.6

- Geometric mean: 1.108x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250821-macm4pro-arm64-python-bb8791c0b75b5970d109-3.15.0a0-bb8791c-vs-3.12.6.md)
- [📈time plot](bm-20250821-macm4pro-arm64-python-bb8791c0b75b5970d109-3.15.0a0-bb8791c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.028x faster (HPT: reliability of 98.53%, 1.00x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250821-macm4pro-arm64-python-bb8791c0b75b5970d109-3.15.0a0-bb8791c-vs-3.13.0rc2.md)
- [📈time plot](bm-20250821-macm4pro-arm64-python-bb8791c0b75b5970d109-3.15.0a0-bb8791c-vs-3.13.0rc2.svg)

