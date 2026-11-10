# Results

- fork: python/e891a9117985888df3e5
- version: 3.16.0a1+dev
- config: NOGIL
- commit hash: [e891a91](https://github.com/python/cpython/commit/e891a91)
- commit date: 2026-11-09T23:49:01Z
- commit merge base: [4e10d4fef5c073faaaf04ce5e03749a5dbe7716b](https://github.com/python/cpython/commit/4e10d4fef5c073faaaf04ce5e03749a5dbe7716b)
- commit date: 2026-11-09T23:49:01+00:00
- ref: e891a9117985888df3e5

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/42727943198)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261109-vultr-x86_64-python-e891a9117985888df3e5-3.16.0a1%2Bdev-e891a91.json)

### vs. 3.12.6

- Geometric mean: 1.024x slower (HPT: reliability of 57.02%, 1.00x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261109-vultr-x86_64-python-e891a9117985888df3e5-3.16.0a1%2Bdev-e891a91-vs-3.12.6.md)
- [📈time plot](bm-20261109-vultr-x86_64-python-e891a9117985888df3e5-3.16.0a1%2Bdev-e891a91-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.056x slower (HPT: reliability of 86.50%, 1.00x slower at 99th %ile)
- Memory usage: 1.30x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261109-vultr-x86_64-python-e891a9117985888df3e5-3.16.0a1%2Bdev-e891a91-vs-3.13.0rc2.md)
- [📈time plot](bm-20261109-vultr-x86_64-python-e891a9117985888df3e5-3.16.0a1%2Bdev-e891a91-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.106x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.14x
- [🧠memory plot](bm-20261109-vultr-x86_64-python-e891a9117985888df3e5-3.16.0a1%2Bdev-e891a91-vs-base-mem.svg)
- [📄table](bm-20261109-vultr-x86_64-python-e891a9117985888df3e5-3.16.0a1%2Bdev-e891a91-vs-base.md)
- [📈time plot](bm-20261109-vultr-x86_64-python-e891a9117985888df3e5-3.16.0a1%2Bdev-e891a91-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/42727943198)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261109-macm4pro-arm64-python-e891a9117985888df3e5-3.16.0a1%2Bdev-e891a91.json)

### vs. 3.12.6

- Geometric mean: 1.066x faster (HPT: reliability of 90.46%, 1.00x faster at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261109-macm4pro-arm64-python-e891a9117985888df3e5-3.16.0a1%2Bdev-e891a91-vs-3.12.6.md)
- [📈time plot](bm-20261109-macm4pro-arm64-python-e891a9117985888df3e5-3.16.0a1%2Bdev-e891a91-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.013x slower (HPT: reliability of 92.29%, 1.00x slower at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261109-macm4pro-arm64-python-e891a9117985888df3e5-3.16.0a1%2Bdev-e891a91-vs-3.13.0rc2.md)
- [📈time plot](bm-20261109-macm4pro-arm64-python-e891a9117985888df3e5-3.16.0a1%2Bdev-e891a91-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.107x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.07x
- new benchmarks: coverage
- [🧠memory plot](bm-20261109-macm4pro-arm64-python-e891a9117985888df3e5-3.16.0a1%2Bdev-e891a91-vs-base-mem.svg)
- [📄table](bm-20261109-macm4pro-arm64-python-e891a9117985888df3e5-3.16.0a1%2Bdev-e891a91-vs-base.md)
- [📈time plot](bm-20261109-macm4pro-arm64-python-e891a9117985888df3e5-3.16.0a1%2Bdev-e891a91-vs-base.svg)

