# Results

- fork: python/2188f9b60abb7965548b
- version: 3.16.0a1+dev
- config: CLANG
- commit hash: [2188f9b](https://github.com/python/cpython/commit/2188f9b)
- commit date: 2026-10-17T23:07:03Z
- commit merge base: [0fedf7852c24727b5a9fa7f2014c18cbaa50cdb9](https://github.com/python/cpython/commit/0fedf7852c24727b5a9fa7f2014c18cbaa50cdb9)
- ref: 2188f9b60abb7965548b

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/39082386553)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261017-macm4pro-arm64-python-2188f9b60abb7965548b-3.16.0a1%2Bdev-2188f9b.json)

### vs. 3.12.6

- Geometric mean: 1.186x faster (HPT: reliability of 100.00%, 1.09x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20261017-macm4pro-arm64-python-2188f9b60abb7965548b-3.16.0a1%2Bdev-2188f9b-vs-3.12.6.md)
- [📈time plot](bm-20261017-macm4pro-arm64-python-2188f9b60abb7965548b-3.16.0a1%2Bdev-2188f9b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.096x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20261017-macm4pro-arm64-python-2188f9b60abb7965548b-3.16.0a1%2Bdev-2188f9b-vs-3.13.0rc2.md)
- [📈time plot](bm-20261017-macm4pro-arm64-python-2188f9b60abb7965548b-3.16.0a1%2Bdev-2188f9b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.004x slower (HPT: reliability of 74.80%, 1.00x faster at 99th %ile)
- Memory usage: 0.99x
- [🧠memory plot](bm-20261017-macm4pro-arm64-python-2188f9b60abb7965548b-3.16.0a1%2Bdev-2188f9b-vs-base-mem.svg)
- [📄table](bm-20261017-macm4pro-arm64-python-2188f9b60abb7965548b-3.16.0a1%2Bdev-2188f9b-vs-base.md)
- [📈time plot](bm-20261017-macm4pro-arm64-python-2188f9b60abb7965548b-3.16.0a1%2Bdev-2188f9b-vs-base.svg)

