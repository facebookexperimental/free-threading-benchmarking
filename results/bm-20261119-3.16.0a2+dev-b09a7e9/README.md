# Results

- fork: python/b09a7e92fb0ab958a52a
- version: 3.16.0a2+dev
- config: 
- commit hash: [b09a7e9](https://github.com/python/cpython/commit/b09a7e9)
- commit date: 2026-11-19T16:02:40-08:00
- commit merge base: [f84083b08ab40b08c8d608a320008418b331932e](https://github.com/python/cpython/commit/f84083b08ab40b08c8d608a320008418b331932e)
- ref: b09a7e92fb0ab958a52a

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/44645460205)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261119-vultr-x86_64-python-b09a7e92fb0ab958a52a-3.16.0a2%2Bdev-b09a7e9.json)

### vs. 3.12.6

- Geometric mean: 1.091x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261119-vultr-x86_64-python-b09a7e92fb0ab958a52a-3.16.0a2%2Bdev-b09a7e9-vs-3.12.6.md)
- [📈time plot](bm-20261119-vultr-x86_64-python-b09a7e92fb0ab958a52a-3.16.0a2%2Bdev-b09a7e9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.054x faster (HPT: reliability of 99.92%, 1.01x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261119-vultr-x86_64-python-b09a7e92fb0ab958a52a-3.16.0a2%2Bdev-b09a7e9-vs-3.13.0rc2.md)
- [📈time plot](bm-20261119-vultr-x86_64-python-b09a7e92fb0ab958a52a-3.16.0a2%2Bdev-b09a7e9-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/44645460205)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261119-macm4pro-arm64-python-b09a7e92fb0ab958a52a-3.16.0a2%2Bdev-b09a7e9.json)

### vs. 3.12.6

- Geometric mean: 1.190x faster (HPT: reliability of 100.00%, 1.09x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261119-macm4pro-arm64-python-b09a7e92fb0ab958a52a-3.16.0a2%2Bdev-b09a7e9-vs-3.12.6.md)
- [📈time plot](bm-20261119-macm4pro-arm64-python-b09a7e92fb0ab958a52a-3.16.0a2%2Bdev-b09a7e9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.099x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261119-macm4pro-arm64-python-b09a7e92fb0ab958a52a-3.16.0a2%2Bdev-b09a7e9-vs-3.13.0rc2.md)
- [📈time plot](bm-20261119-macm4pro-arm64-python-b09a7e92fb0ab958a52a-3.16.0a2%2Bdev-b09a7e9-vs-3.13.0rc2.svg)

