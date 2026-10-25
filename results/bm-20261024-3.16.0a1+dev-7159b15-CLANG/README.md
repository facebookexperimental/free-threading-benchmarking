# Results

- fork: python/7159b152a0b6205941ad
- version: 3.16.0a1+dev
- config: CLANG
- commit hash: [7159b15](https://github.com/python/cpython/commit/7159b15)
- commit date: 2026-10-24T17:06:37-07:00
- commit merge base: [081f6fba35f2b1be8a3166104237f9682b620f90](https://github.com/python/cpython/commit/081f6fba35f2b1be8a3166104237f9682b620f90)
- ref: 7159b152a0b6205941ad

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/40146293472)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261024-macm4pro-arm64-python-7159b152a0b6205941ad-3.16.0a1%2Bdev-7159b15.json)

### vs. 3.12.6

- Geometric mean: 1.193x faster (HPT: reliability of 100.00%, 1.09x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20261024-macm4pro-arm64-python-7159b152a0b6205941ad-3.16.0a1%2Bdev-7159b15-vs-3.12.6.md)
- [📈time plot](bm-20261024-macm4pro-arm64-python-7159b152a0b6205941ad-3.16.0a1%2Bdev-7159b15-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.102x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20261024-macm4pro-arm64-python-7159b152a0b6205941ad-3.16.0a1%2Bdev-7159b15-vs-3.13.0rc2.md)
- [📈time plot](bm-20261024-macm4pro-arm64-python-7159b152a0b6205941ad-3.16.0a1%2Bdev-7159b15-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.008x slower (HPT: reliability of 54.58%, 1.00x faster at 99th %ile)
- Memory usage: 0.99x
- [🧠memory plot](bm-20261024-macm4pro-arm64-python-7159b152a0b6205941ad-3.16.0a1%2Bdev-7159b15-vs-base-mem.svg)
- [📄table](bm-20261024-macm4pro-arm64-python-7159b152a0b6205941ad-3.16.0a1%2Bdev-7159b15-vs-base.md)
- [📈time plot](bm-20261024-macm4pro-arm64-python-7159b152a0b6205941ad-3.16.0a1%2Bdev-7159b15-vs-base.svg)

