# Results

- fork: python/20d5494c88985beb925b
- version: 3.15.0a0
- config: CLANG
- commit hash: [20d5494](https://github.com/python/cpython/commit/20d5494)
- commit date: 2025-09-20T11:01:44+03:00
- commit merge base: [69c6b438e84ef2bb94a587e49946a2a4b6454fb3](https://github.com/python/cpython/commit/69c6b438e84ef2bb94a587e49946a2a4b6454fb3)
- ref: 20d5494c88985beb925b

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17886510324)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250920-macm4pro-arm64-python-20d5494c88985beb925b-3.15.0a0-20d5494.json)

### vs. 3.12.6

- Geometric mean: 1.143x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250920-macm4pro-arm64-python-20d5494c88985beb925b-3.15.0a0-20d5494-vs-3.12.6.md)
- [📈time plot](bm-20250920-macm4pro-arm64-python-20d5494c88985beb925b-3.15.0a0-20d5494-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.060x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250920-macm4pro-arm64-python-20d5494c88985beb925b-3.15.0a0-20d5494-vs-3.13.0rc2.md)
- [📈time plot](bm-20250920-macm4pro-arm64-python-20d5494c88985beb925b-3.15.0a0-20d5494-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.034x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 0.98x
- [🧠memory plot](bm-20250920-macm4pro-arm64-python-20d5494c88985beb925b-3.15.0a0-20d5494-vs-base-mem.svg)
- [📄table](bm-20250920-macm4pro-arm64-python-20d5494c88985beb925b-3.15.0a0-20d5494-vs-base.md)
- [📈time plot](bm-20250920-macm4pro-arm64-python-20d5494c88985beb925b-3.15.0a0-20d5494-vs-base.svg)

