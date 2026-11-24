# Results

- fork: python/4ec6eb0496922cb466a8
- version: 3.16.0a2+dev
- config: NOGIL
- commit hash: [4ec6eb0](https://github.com/python/cpython/commit/4ec6eb0)
- commit date: 2026-11-24T00:32:41+02:00
- commit merge base: [1590d78fc37ce88435cc0522f928861e6586bc25](https://github.com/python/cpython/commit/1590d78fc37ce88435cc0522f928861e6586bc25)
- ref: 4ec6eb0496922cb466a8

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/45296736022)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261124-vultr-x86_64-python-4ec6eb0496922cb466a8-3.16.0a2%2Bdev-4ec6eb0.json)

### vs. 3.12.6

- Geometric mean: 1.025x slower (HPT: reliability of 74.70%, 1.00x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261124-vultr-x86_64-python-4ec6eb0496922cb466a8-3.16.0a2%2Bdev-4ec6eb0-vs-3.12.6.md)
- [📈time plot](bm-20261124-vultr-x86_64-python-4ec6eb0496922cb466a8-3.16.0a2%2Bdev-4ec6eb0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.059x slower (HPT: reliability of 87.56%, 1.00x slower at 99th %ile)
- Memory usage: 1.30x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261124-vultr-x86_64-python-4ec6eb0496922cb466a8-3.16.0a2%2Bdev-4ec6eb0-vs-3.13.0rc2.md)
- [📈time plot](bm-20261124-vultr-x86_64-python-4ec6eb0496922cb466a8-3.16.0a2%2Bdev-4ec6eb0-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.114x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.14x
- [🧠memory plot](bm-20261124-vultr-x86_64-python-4ec6eb0496922cb466a8-3.16.0a2%2Bdev-4ec6eb0-vs-base-mem.svg)
- [📄table](bm-20261124-vultr-x86_64-python-4ec6eb0496922cb466a8-3.16.0a2%2Bdev-4ec6eb0-vs-base.md)
- [📈time plot](bm-20261124-vultr-x86_64-python-4ec6eb0496922cb466a8-3.16.0a2%2Bdev-4ec6eb0-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/45296736022)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261124-macm4pro-arm64-python-4ec6eb0496922cb466a8-3.16.0a2%2Bdev-4ec6eb0.json)

### vs. 3.12.6

- Geometric mean: 1.075x faster (HPT: reliability of 97.77%, 1.00x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261124-macm4pro-arm64-python-4ec6eb0496922cb466a8-3.16.0a2%2Bdev-4ec6eb0-vs-3.12.6.md)
- [📈time plot](bm-20261124-macm4pro-arm64-python-4ec6eb0496922cb466a8-3.16.0a2%2Bdev-4ec6eb0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.005x slower (HPT: reliability of 89.79%, 1.00x slower at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261124-macm4pro-arm64-python-4ec6eb0496922cb466a8-3.16.0a2%2Bdev-4ec6eb0-vs-3.13.0rc2.md)
- [📈time plot](bm-20261124-macm4pro-arm64-python-4ec6eb0496922cb466a8-3.16.0a2%2Bdev-4ec6eb0-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.097x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.07x
- new benchmarks: coverage
- [🧠memory plot](bm-20261124-macm4pro-arm64-python-4ec6eb0496922cb466a8-3.16.0a2%2Bdev-4ec6eb0-vs-base-mem.svg)
- [📄table](bm-20261124-macm4pro-arm64-python-4ec6eb0496922cb466a8-3.16.0a2%2Bdev-4ec6eb0-vs-base.md)
- [📈time plot](bm-20261124-macm4pro-arm64-python-4ec6eb0496922cb466a8-3.16.0a2%2Bdev-4ec6eb0-vs-base.svg)

