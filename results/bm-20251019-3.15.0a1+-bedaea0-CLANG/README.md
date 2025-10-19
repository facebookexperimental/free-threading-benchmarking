# Results

- fork: python/bedaea05987738c4c6b9
- version: 3.15.0a1+
- config: CLANG
- commit hash: [bedaea0](https://github.com/python/cpython/commit/bedaea0)
- commit date: 2025-10-19T00:20:04+01:00
- commit merge base: [920de7ccdcfa7284b6d23a124771b17c66dd3e4f](https://github.com/python/cpython/commit/920de7ccdcfa7284b6d23a124771b17c66dd3e4f)
- ref: bedaea05987738c4c6b9

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18622795374)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0.json)

### vs. 3.12.6

- Geometric mean: 1.153x faster (HPT: reliability of 100.00%, 1.09x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-vs-3.12.6.md)
- [📈time plot](bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.069x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-vs-3.13.0rc2.md)
- [📈time plot](bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.046x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-vs-base-mem.svg)
- [📄table](bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-vs-base.md)
- [📈time plot](bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1%2B-bedaea0-vs-base.svg)

