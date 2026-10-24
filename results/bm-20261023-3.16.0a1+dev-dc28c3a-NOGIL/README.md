# Results

- fork: python/dc28c3a358221b1e0ae5
- version: 3.16.0a1+dev
- config: NOGIL
- commit hash: [dc28c3a](https://github.com/python/cpython/commit/dc28c3a)
- commit date: 2026-10-23T17:15:40-07:00
- commit merge base: [46edd6fa41d12e7b1e9fb527ee5604722de9f285](https://github.com/python/cpython/commit/46edd6fa41d12e7b1e9fb527ee5604722de9f285)
- ref: dc28c3a358221b1e0ae5

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/40045877285)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261023-vultr-x86_64-python-dc28c3a358221b1e0ae5-3.16.0a1%2Bdev-dc28c3a.json)

### vs. 3.12.6

- Geometric mean: 1.031x slower (HPT: reliability of 65.39%, 1.00x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261023-vultr-x86_64-python-dc28c3a358221b1e0ae5-3.16.0a1%2Bdev-dc28c3a-vs-3.12.6.md)
- [📈time plot](bm-20261023-vultr-x86_64-python-dc28c3a358221b1e0ae5-3.16.0a1%2Bdev-dc28c3a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.064x slower (HPT: reliability of 87.86%, 1.00x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261023-vultr-x86_64-python-dc28c3a358221b1e0ae5-3.16.0a1%2Bdev-dc28c3a-vs-3.13.0rc2.md)
- [📈time plot](bm-20261023-vultr-x86_64-python-dc28c3a358221b1e0ae5-3.16.0a1%2Bdev-dc28c3a-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.108x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.17x
- [🧠memory plot](bm-20261023-vultr-x86_64-python-dc28c3a358221b1e0ae5-3.16.0a1%2Bdev-dc28c3a-vs-base-mem.svg)
- [📄table](bm-20261023-vultr-x86_64-python-dc28c3a358221b1e0ae5-3.16.0a1%2Bdev-dc28c3a-vs-base.md)
- [📈time plot](bm-20261023-vultr-x86_64-python-dc28c3a358221b1e0ae5-3.16.0a1%2Bdev-dc28c3a-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/40045877285)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261023-macm4pro-arm64-python-dc28c3a358221b1e0ae5-3.16.0a1%2Bdev-dc28c3a.json)

### vs. 3.12.6

- Geometric mean: 1.084x faster (HPT: reliability of 97.26%, 1.00x faster at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261023-macm4pro-arm64-python-dc28c3a358221b1e0ae5-3.16.0a1%2Bdev-dc28c3a-vs-3.12.6.md)
- [📈time plot](bm-20261023-macm4pro-arm64-python-dc28c3a358221b1e0ae5-3.16.0a1%2Bdev-dc28c3a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.004x faster (HPT: reliability of 73.21%, 1.00x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261023-macm4pro-arm64-python-dc28c3a358221b1e0ae5-3.16.0a1%2Bdev-dc28c3a-vs-3.13.0rc2.md)
- [📈time plot](bm-20261023-macm4pro-arm64-python-dc28c3a358221b1e0ae5-3.16.0a1%2Bdev-dc28c3a-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.094x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.11x
- new benchmarks: coverage
- [🧠memory plot](bm-20261023-macm4pro-arm64-python-dc28c3a358221b1e0ae5-3.16.0a1%2Bdev-dc28c3a-vs-base-mem.svg)
- [📄table](bm-20261023-macm4pro-arm64-python-dc28c3a358221b1e0ae5-3.16.0a1%2Bdev-dc28c3a-vs-base.md)
- [📈time plot](bm-20261023-macm4pro-arm64-python-dc28c3a358221b1e0ae5-3.16.0a1%2Bdev-dc28c3a-vs-base.svg)

