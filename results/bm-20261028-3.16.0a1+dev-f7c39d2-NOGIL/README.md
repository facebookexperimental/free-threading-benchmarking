# Results

- fork: python/f7c39d2316e59f17148d
- version: 3.16.0a1+dev
- config: NOGIL
- commit hash: [f7c39d2](https://github.com/python/cpython/commit/f7c39d2)
- commit date: 2026-10-28T22:51:07Z
- commit merge base: [8e605fe7d80ff715ca813e2c1434da34990c6e18](https://github.com/python/cpython/commit/8e605fe7d80ff715ca813e2c1434da34990c6e18)
- commit date: 2026-10-28T22:51:07+00:00
- ref: f7c39d2316e59f17148d

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/40794423519)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261028-vultr-x86_64-python-f7c39d2316e59f17148d-3.16.0a1%2Bdev-f7c39d2.json)

### vs. 3.12.6

- Geometric mean: 1.032x slower (HPT: reliability of 70.90%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261028-vultr-x86_64-python-f7c39d2316e59f17148d-3.16.0a1%2Bdev-f7c39d2-vs-3.12.6.md)
- [📈time plot](bm-20261028-vultr-x86_64-python-f7c39d2316e59f17148d-3.16.0a1%2Bdev-f7c39d2-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.064x slower (HPT: reliability of 93.96%, 1.00x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261028-vultr-x86_64-python-f7c39d2316e59f17148d-3.16.0a1%2Bdev-f7c39d2-vs-3.13.0rc2.md)
- [📈time plot](bm-20261028-vultr-x86_64-python-f7c39d2316e59f17148d-3.16.0a1%2Bdev-f7c39d2-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.117x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.17x
- [🧠memory plot](bm-20261028-vultr-x86_64-python-f7c39d2316e59f17148d-3.16.0a1%2Bdev-f7c39d2-vs-base-mem.svg)
- [📄table](bm-20261028-vultr-x86_64-python-f7c39d2316e59f17148d-3.16.0a1%2Bdev-f7c39d2-vs-base.md)
- [📈time plot](bm-20261028-vultr-x86_64-python-f7c39d2316e59f17148d-3.16.0a1%2Bdev-f7c39d2-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/40794423519)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261028-macm4pro-arm64-python-f7c39d2316e59f17148d-3.16.0a1%2Bdev-f7c39d2.json)

### vs. 3.12.6

- Geometric mean: 1.079x faster (HPT: reliability of 94.82%, 1.00x faster at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261028-macm4pro-arm64-python-f7c39d2316e59f17148d-3.16.0a1%2Bdev-f7c39d2-vs-3.12.6.md)
- [📈time plot](bm-20261028-macm4pro-arm64-python-f7c39d2316e59f17148d-3.16.0a1%2Bdev-f7c39d2-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.001x slower (HPT: reliability of 77.73%, 1.00x slower at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261028-macm4pro-arm64-python-f7c39d2316e59f17148d-3.16.0a1%2Bdev-f7c39d2-vs-3.13.0rc2.md)
- [📈time plot](bm-20261028-macm4pro-arm64-python-f7c39d2316e59f17148d-3.16.0a1%2Bdev-f7c39d2-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.105x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.11x
- new benchmarks: coverage
- [🧠memory plot](bm-20261028-macm4pro-arm64-python-f7c39d2316e59f17148d-3.16.0a1%2Bdev-f7c39d2-vs-base-mem.svg)
- [📄table](bm-20261028-macm4pro-arm64-python-f7c39d2316e59f17148d-3.16.0a1%2Bdev-f7c39d2-vs-base.md)
- [📈time plot](bm-20261028-macm4pro-arm64-python-f7c39d2316e59f17148d-3.16.0a1%2Bdev-f7c39d2-vs-base.svg)

