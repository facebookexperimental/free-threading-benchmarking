# Results

- fork: python/4b21d154b4864531641f
- version: 3.16.0a1+dev
- config: 
- commit hash: [4b21d15](https://github.com/python/cpython/commit/4b21d15)
- commit date: 2026-11-01T20:41:32Z
- commit merge base: [a7c03835e4d6110eeef5aef63fc429b732b877e4](https://github.com/python/cpython/commit/a7c03835e4d6110eeef5aef63fc429b732b877e4)
- commit date: 2026-11-01T20:41:32+00:00
- ref: 4b21d154b4864531641f

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/41367217066)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261101-vultr-x86_64-python-4b21d154b4864531641f-3.16.0a1%2Bdev-4b21d15.json)

### vs. 3.12.6

- Geometric mean: 1.087x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261101-vultr-x86_64-python-4b21d154b4864531641f-3.16.0a1%2Bdev-4b21d15-vs-3.12.6.md)
- [📈time plot](bm-20261101-vultr-x86_64-python-4b21d154b4864531641f-3.16.0a1%2Bdev-4b21d15-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.052x faster (HPT: reliability of 99.94%, 1.01x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261101-vultr-x86_64-python-4b21d154b4864531641f-3.16.0a1%2Bdev-4b21d15-vs-3.13.0rc2.md)
- [📈time plot](bm-20261101-vultr-x86_64-python-4b21d154b4864531641f-3.16.0a1%2Bdev-4b21d15-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/41367217066)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261101-macm4pro-arm64-python-4b21d154b4864531641f-3.16.0a1%2Bdev-4b21d15.json)

### vs. 3.12.6

- Geometric mean: 1.208x faster (HPT: reliability of 100.00%, 1.11x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261101-macm4pro-arm64-python-4b21d154b4864531641f-3.16.0a1%2Bdev-4b21d15-vs-3.12.6.md)
- [📈time plot](bm-20261101-macm4pro-arm64-python-4b21d154b4864531641f-3.16.0a1%2Bdev-4b21d15-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.116x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261101-macm4pro-arm64-python-4b21d154b4864531641f-3.16.0a1%2Bdev-4b21d15-vs-3.13.0rc2.md)
- [📈time plot](bm-20261101-macm4pro-arm64-python-4b21d154b4864531641f-3.16.0a1%2Bdev-4b21d15-vs-3.13.0rc2.svg)

