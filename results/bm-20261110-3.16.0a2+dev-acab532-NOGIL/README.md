# Results

- fork: python/acab53212d89b298ba0d
- version: 3.16.0a2+dev
- config: NOGIL
- commit hash: [acab532](https://github.com/python/cpython/commit/acab532)
- commit date: 2026-11-10T22:58:40Z
- commit merge base: [226813c0f7834b55be51e912a3d8555e652d9026](https://github.com/python/cpython/commit/226813c0f7834b55be51e912a3d8555e652d9026)
- commit date: 2026-11-10T22:58:40+00:00
- ref: acab53212d89b298ba0d

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/42931153744)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261110-vultr-x86_64-python-acab53212d89b298ba0d-3.16.0a2%2Bdev-acab532.json)

### vs. 3.12.6

- Geometric mean: 1.029x slower (HPT: reliability of 74.85%, 1.00x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261110-vultr-x86_64-python-acab53212d89b298ba0d-3.16.0a2%2Bdev-acab532-vs-3.12.6.md)
- [📈time plot](bm-20261110-vultr-x86_64-python-acab53212d89b298ba0d-3.16.0a2%2Bdev-acab532-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.062x slower (HPT: reliability of 90.61%, 1.00x slower at 99th %ile)
- Memory usage: 1.30x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261110-vultr-x86_64-python-acab53212d89b298ba0d-3.16.0a2%2Bdev-acab532-vs-3.13.0rc2.md)
- [📈time plot](bm-20261110-vultr-x86_64-python-acab53212d89b298ba0d-3.16.0a2%2Bdev-acab532-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.115x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.14x
- [🧠memory plot](bm-20261110-vultr-x86_64-python-acab53212d89b298ba0d-3.16.0a2%2Bdev-acab532-vs-base-mem.svg)
- [📄table](bm-20261110-vultr-x86_64-python-acab53212d89b298ba0d-3.16.0a2%2Bdev-acab532-vs-base.md)
- [📈time plot](bm-20261110-vultr-x86_64-python-acab53212d89b298ba0d-3.16.0a2%2Bdev-acab532-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/42931153744)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261110-macm4pro-arm64-python-acab53212d89b298ba0d-3.16.0a2%2Bdev-acab532.json)

### vs. 3.12.6

- Geometric mean: 1.063x faster (HPT: reliability of 85.43%, 1.00x faster at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261110-macm4pro-arm64-python-acab53212d89b298ba0d-3.16.0a2%2Bdev-acab532-vs-3.12.6.md)
- [📈time plot](bm-20261110-macm4pro-arm64-python-acab53212d89b298ba0d-3.16.0a2%2Bdev-acab532-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.016x slower (HPT: reliability of 94.65%, 1.00x slower at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261110-macm4pro-arm64-python-acab53212d89b298ba0d-3.16.0a2%2Bdev-acab532-vs-3.13.0rc2.md)
- [📈time plot](bm-20261110-macm4pro-arm64-python-acab53212d89b298ba0d-3.16.0a2%2Bdev-acab532-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.104x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.08x
- new benchmarks: coverage
- [🧠memory plot](bm-20261110-macm4pro-arm64-python-acab53212d89b298ba0d-3.16.0a2%2Bdev-acab532-vs-base-mem.svg)
- [📄table](bm-20261110-macm4pro-arm64-python-acab53212d89b298ba0d-3.16.0a2%2Bdev-acab532-vs-base.md)
- [📈time plot](bm-20261110-macm4pro-arm64-python-acab53212d89b298ba0d-3.16.0a2%2Bdev-acab532-vs-base.svg)

