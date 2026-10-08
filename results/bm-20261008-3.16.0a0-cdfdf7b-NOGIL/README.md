# Results

- fork: python/cdfdf7bb73a5751ecec7
- version: 3.16.0a0
- config: NOGIL
- commit hash: [cdfdf7b](https://github.com/python/cpython/commit/cdfdf7b)
- commit date: 2026-10-08T08:58:23+09:00
- commit merge base: [12fbc90e063b118f489241ae9f806a9d694a5682](https://github.com/python/cpython/commit/12fbc90e063b118f489241ae9f806a9d694a5682)
- ref: cdfdf7bb73a5751ecec7

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/37709408250)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b.json)

### vs. 3.12.6

- Geometric mean: 1.042x slower (HPT: reliability of 78.07%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b-vs-3.12.6.md)
- [📈time plot](bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.074x slower (HPT: reliability of 97.26%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b-vs-3.13.0rc2.md)
- [📈time plot](bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.107x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b-vs-base-mem.svg)
- [📄table](bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b-vs-base.md)
- [📈time plot](bm-20261008-vultr-x86_64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/37709408250)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261008-macm4pro-arm64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b.json)

### vs. 3.12.6

- Geometric mean: 1.056x faster (HPT: reliability of 87.14%, 1.00x faster at 99th %ile)
- Memory usage: 1.30x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261008-macm4pro-arm64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b-vs-3.12.6.md)
- [📈time plot](bm-20261008-macm4pro-arm64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.022x slower (HPT: reliability of 94.57%, 1.00x slower at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261008-macm4pro-arm64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b-vs-3.13.0rc2.md)
- [📈time plot](bm-20261008-macm4pro-arm64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.084x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.12x
- new benchmarks: coverage
- [🧠memory plot](bm-20261008-macm4pro-arm64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b-vs-base-mem.svg)
- [📄table](bm-20261008-macm4pro-arm64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b-vs-base.md)
- [📈time plot](bm-20261008-macm4pro-arm64-python-cdfdf7bb73a5751ecec7-3.16.0a0-cdfdf7b-vs-base.svg)

