# Results

- fork: python/63cc1257db468a368d64
- version: 3.15.0a5+
- config: CLANG
- commit hash: [63cc125](https://github.com/python/cpython/commit/63cc125)
- commit date: 2026-01-17T19:16:12-05:00
- commit merge base: [7ca9e7ad053c24ae40fc68bc931ca1ff8abbc956](https://github.com/python/cpython/commit/7ca9e7ad053c24ae40fc68bc931ca1ff8abbc956)
- ref: 63cc1257db468a368d64

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21103064804)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260117-macm4pro-arm64-python-63cc1257db468a368d64-3.15.0a5%2B-63cc125.json)

### vs. 3.12.6

- Geometric mean: 1.194x faster (HPT: reliability of 100.00%, 1.09x faster at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260117-macm4pro-arm64-python-63cc1257db468a368d64-3.15.0a5%2B-63cc125-vs-3.12.6.md)
- [📈time plot](bm-20260117-macm4pro-arm64-python-63cc1257db468a368d64-3.15.0a5%2B-63cc125-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.107x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260117-macm4pro-arm64-python-63cc1257db468a368d64-3.15.0a5%2B-63cc125-vs-3.13.0rc2.md)
- [📈time plot](bm-20260117-macm4pro-arm64-python-63cc1257db468a368d64-3.15.0a5%2B-63cc125-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.033x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 0.99x
- [🧠memory plot](bm-20260117-macm4pro-arm64-python-63cc1257db468a368d64-3.15.0a5%2B-63cc125-vs-base-mem.svg)
- [📄table](bm-20260117-macm4pro-arm64-python-63cc1257db468a368d64-3.15.0a5%2B-63cc125-vs-base.md)
- [📈time plot](bm-20260117-macm4pro-arm64-python-63cc1257db468a368d64-3.15.0a5%2B-63cc125-vs-base.svg)

