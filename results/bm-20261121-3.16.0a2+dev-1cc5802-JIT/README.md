# Results

- fork: python/1cc580249141838a5208
- version: 3.16.0a2+dev
- config: JIT
- commit hash: [1cc5802](https://github.com/python/cpython/commit/1cc5802)
- commit date: 2026-11-21T16:07:13-08:00
- commit merge base: [639c34b5f0d64ac8c39cca0d46a9ab9dafc82703](https://github.com/python/cpython/commit/639c34b5f0d64ac8c39cca0d46a9ab9dafc82703)
- ref: 1cc580249141838a5208

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/44965547301)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261121-vultr-x86_64-python-1cc580249141838a5208-3.16.0a2%2Bdev-1cc5802.json)

### vs. 3.12.6

- Geometric mean: 1.216x faster (HPT: reliability of 100.00%, 1.12x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261121-vultr-x86_64-python-1cc580249141838a5208-3.16.0a2%2Bdev-1cc5802-vs-3.12.6.md)
- [📈time plot](bm-20261121-vultr-x86_64-python-1cc580249141838a5208-3.16.0a2%2Bdev-1cc5802-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.175x faster (HPT: reliability of 100.00%, 1.12x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261121-vultr-x86_64-python-1cc580249141838a5208-3.16.0a2%2Bdev-1cc5802-vs-3.13.0rc2.md)
- [📈time plot](bm-20261121-vultr-x86_64-python-1cc580249141838a5208-3.16.0a2%2Bdev-1cc5802-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.098x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.05x
- [🧠memory plot](bm-20261121-vultr-x86_64-python-1cc580249141838a5208-3.16.0a2%2Bdev-1cc5802-vs-base-mem.svg)
- [📄table](bm-20261121-vultr-x86_64-python-1cc580249141838a5208-3.16.0a2%2Bdev-1cc5802-vs-base.md)
- [📈time plot](bm-20261121-vultr-x86_64-python-1cc580249141838a5208-3.16.0a2%2Bdev-1cc5802-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/44965547301)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261121-macm4pro-arm64-python-1cc580249141838a5208-3.16.0a2%2Bdev-1cc5802.json)

### vs. 3.12.6

- Geometric mean: 1.339x faster (HPT: reliability of 100.00%, 1.21x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20261121-macm4pro-arm64-python-1cc580249141838a5208-3.16.0a2%2Bdev-1cc5802-vs-3.12.6.md)
- [📈time plot](bm-20261121-macm4pro-arm64-python-1cc580249141838a5208-3.16.0a2%2Bdev-1cc5802-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.237x faster (HPT: reliability of 100.00%, 1.13x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20261121-macm4pro-arm64-python-1cc580249141838a5208-3.16.0a2%2Bdev-1cc5802-vs-3.13.0rc2.md)
- [📈time plot](bm-20261121-macm4pro-arm64-python-1cc580249141838a5208-3.16.0a2%2Bdev-1cc5802-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.117x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.04x
- [🧠memory plot](bm-20261121-macm4pro-arm64-python-1cc580249141838a5208-3.16.0a2%2Bdev-1cc5802-vs-base-mem.svg)
- [📄table](bm-20261121-macm4pro-arm64-python-1cc580249141838a5208-3.16.0a2%2Bdev-1cc5802-vs-base.md)
- [📈time plot](bm-20261121-macm4pro-arm64-python-1cc580249141838a5208-3.16.0a2%2Bdev-1cc5802-vs-base.svg)

