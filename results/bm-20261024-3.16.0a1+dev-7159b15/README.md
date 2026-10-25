# Results

- fork: python/7159b152a0b6205941ad
- version: 3.16.0a1+dev
- config: 
- commit hash: [7159b15](https://github.com/python/cpython/commit/7159b15)
- commit date: 2026-10-24T17:06:37-07:00
- commit merge base: [081f6fba35f2b1be8a3166104237f9682b620f90](https://github.com/python/cpython/commit/081f6fba35f2b1be8a3166104237f9682b620f90)
- ref: 7159b152a0b6205941ad

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/40146293472)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [pystats raw](bm-20261024-vultr-x86_64-python-7159b152a0b6205941ad-3.16.0a1%2Bdev-7159b15-pystats.json)
- [pystats table](bm-20261024-vultr-x86_64-python-7159b152a0b6205941ad-3.16.0a1%2Bdev-7159b15-pystats.md)
- [raw results](bm-20261024-vultr-x86_64-python-7159b152a0b6205941ad-3.16.0a1%2Bdev-7159b15.json)

### vs. 3.12.6

- Geometric mean: 1.088x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261024-vultr-x86_64-python-7159b152a0b6205941ad-3.16.0a1%2Bdev-7159b15-vs-3.12.6.md)
- [📈time plot](bm-20261024-vultr-x86_64-python-7159b152a0b6205941ad-3.16.0a1%2Bdev-7159b15-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.050x faster (HPT: reliability of 99.39%, 1.00x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261024-vultr-x86_64-python-7159b152a0b6205941ad-3.16.0a1%2Bdev-7159b15-vs-3.13.0rc2.md)
- [📈time plot](bm-20261024-vultr-x86_64-python-7159b152a0b6205941ad-3.16.0a1%2Bdev-7159b15-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/40146293472)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261024-macm4pro-arm64-python-7159b152a0b6205941ad-3.16.0a1%2Bdev-7159b15.json)

### vs. 3.12.6

- Geometric mean: 1.203x faster (HPT: reliability of 100.00%, 1.10x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20261024-macm4pro-arm64-python-7159b152a0b6205941ad-3.16.0a1%2Bdev-7159b15-vs-3.12.6.md)
- [📈time plot](bm-20261024-macm4pro-arm64-python-7159b152a0b6205941ad-3.16.0a1%2Bdev-7159b15-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.111x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20261024-macm4pro-arm64-python-7159b152a0b6205941ad-3.16.0a1%2Bdev-7159b15-vs-3.13.0rc2.md)
- [📈time plot](bm-20261024-macm4pro-arm64-python-7159b152a0b6205941ad-3.16.0a1%2Bdev-7159b15-vs-3.13.0rc2.svg)

