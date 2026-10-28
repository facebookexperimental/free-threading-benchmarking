# Results

- fork: python/6c695bfad45ddde73d0d
- version: 3.16.0a1+dev
- config: 
- commit hash: [6c695bf](https://github.com/python/cpython/commit/6c695bf)
- commit date: 2026-10-27T22:56:42Z
- commit merge base: [926b0bf3110bf86550ef248cf911e24fc123ec64](https://github.com/python/cpython/commit/926b0bf3110bf86550ef248cf911e24fc123ec64)
- commit date: 2026-10-27T22:56:42+00:00
- ref: 6c695bfad45ddde73d0d

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/40609157495)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261027-vultr-x86_64-python-6c695bfad45ddde73d0d-3.16.0a1%2Bdev-6c695bf.json)

### vs. 3.12.6

- Geometric mean: 1.090x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261027-vultr-x86_64-python-6c695bfad45ddde73d0d-3.16.0a1%2Bdev-6c695bf-vs-3.12.6.md)
- [📈time plot](bm-20261027-vultr-x86_64-python-6c695bfad45ddde73d0d-3.16.0a1%2Bdev-6c695bf-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.054x faster (HPT: reliability of 99.99%, 1.01x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261027-vultr-x86_64-python-6c695bfad45ddde73d0d-3.16.0a1%2Bdev-6c695bf-vs-3.13.0rc2.md)
- [📈time plot](bm-20261027-vultr-x86_64-python-6c695bfad45ddde73d0d-3.16.0a1%2Bdev-6c695bf-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/40609157495)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1%2Bdev-6c695bf.json)

### vs. 3.12.6

- Geometric mean: 1.212x faster (HPT: reliability of 100.00%, 1.11x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1%2Bdev-6c695bf-vs-3.12.6.md)
- [📈time plot](bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1%2Bdev-6c695bf-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.120x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1%2Bdev-6c695bf-vs-3.13.0rc2.md)
- [📈time plot](bm-20261027-macm4pro-arm64-python-6c695bfad45ddde73d0d-3.16.0a1%2Bdev-6c695bf-vs-3.13.0rc2.svg)

