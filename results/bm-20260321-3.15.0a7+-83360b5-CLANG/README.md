# Results

- fork: python/83360b5869a4981c87dc
- version: 3.15.0a7+
- config: CLANG
- commit hash: [83360b5](https://github.com/python/cpython/commit/83360b5)
- commit date: 2026-03-21T18:02:06+02:00
- commit merge base: [f6b5eed47de2de13da94332231eb9c3f4769c78d](https://github.com/python/cpython/commit/f6b5eed47de2de13da94332231eb9c3f4769c78d)
- ref: 83360b5869a4981c87dc

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/23391964030)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260321-macm4pro-arm64-python-83360b5869a4981c87dc-3.15.0a7%2B-83360b5.json)

### vs. 3.12.6

- Geometric mean: 1.176x faster (HPT: reliability of 100.00%, 1.08x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260321-macm4pro-arm64-python-83360b5869a4981c87dc-3.15.0a7%2B-83360b5-vs-3.12.6.md)
- [📈time plot](bm-20260321-macm4pro-arm64-python-83360b5869a4981c87dc-3.15.0a7%2B-83360b5-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.090x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260321-macm4pro-arm64-python-83360b5869a4981c87dc-3.15.0a7%2B-83360b5-vs-3.13.0rc2.md)
- [📈time plot](bm-20260321-macm4pro-arm64-python-83360b5869a4981c87dc-3.15.0a7%2B-83360b5-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.039x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 0.99x
- [🧠memory plot](bm-20260321-macm4pro-arm64-python-83360b5869a4981c87dc-3.15.0a7%2B-83360b5-vs-base-mem.svg)
- [📄table](bm-20260321-macm4pro-arm64-python-83360b5869a4981c87dc-3.15.0a7%2B-83360b5-vs-base.md)
- [📈time plot](bm-20260321-macm4pro-arm64-python-83360b5869a4981c87dc-3.15.0a7%2B-83360b5-vs-base.svg)

