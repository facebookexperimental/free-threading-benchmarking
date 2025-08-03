# Results

- fork: python/801cf3fcdd27d8b6dd0f
- version: 3.15.0a0
- config: CLANG
- commit hash: [801cf3f](https://github.com/python/cpython/commit/801cf3f)
- commit date: 2025-08-02T16:49:34+01:00
- commit merge base: [7475887e1e5d7abc0e48c8ea50e4fe123582cdbd](https://github.com/python/cpython/commit/7475887e1e5d7abc0e48c8ea50e4fe123582cdbd)
- ref: 801cf3fcdd27d8b6dd0f

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16699144340)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f.json)

### vs. 3.12.6

- Geometric mean: 1.140x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f-vs-3.12.6.md)
- [📈time plot](bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.058x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f-vs-3.13.0rc2.md)
- [📈time plot](bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.036x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f-vs-base-mem.svg)
- [📄table](bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f-vs-base.md)
- [📈time plot](bm-20250802-macm4pro-arm64-python-801cf3fcdd27d8b6dd0f-3.15.0a0-801cf3f-vs-base.svg)

