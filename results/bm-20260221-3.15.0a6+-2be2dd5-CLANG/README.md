# Results

- fork: python/2be2dd5fc219a5c252d7
- version: 3.15.0a6+
- config: CLANG
- commit hash: [2be2dd5](https://github.com/python/cpython/commit/2be2dd5)
- commit date: 2026-02-21T22:06:59+01:00
- commit merge base: [fbd3b25e00fdfd5e0a30c64848624dc471987c30](https://github.com/python/cpython/commit/fbd3b25e00fdfd5e0a30c64848624dc471987c30)
- ref: 2be2dd5fc219a5c252d7

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/22267099555)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6%2B-2be2dd5.json)

### vs. 3.12.6

- Geometric mean: 1.164x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6%2B-2be2dd5-vs-3.12.6.md)
- [📈time plot](bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6%2B-2be2dd5-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.079x faster (HPT: reliability of 99.96%, 1.00x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6%2B-2be2dd5-vs-3.13.0rc2.md)
- [📈time plot](bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6%2B-2be2dd5-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.011x faster (HPT: reliability of 99.73%, 1.00x faster at 99th %ile)
- Memory usage: 0.98x
- [🧠memory plot](bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6%2B-2be2dd5-vs-base-mem.svg)
- [📄table](bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6%2B-2be2dd5-vs-base.md)
- [📈time plot](bm-20260221-macm4pro-arm64-python-2be2dd5fc219a5c252d7-3.15.0a6%2B-2be2dd5-vs-base.svg)

