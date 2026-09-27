# Results

- fork: python/1e8ff18a1215b711136b
- version: 3.16.0a0
- config: CLANG
- commit hash: [1e8ff18](https://github.com/python/cpython/commit/1e8ff18)
- commit date: 2026-09-26T20:19:25Z
- commit merge base: [972cfaae3f1349a2b822a0003e96e980c59a402f](https://github.com/python/cpython/commit/972cfaae3f1349a2b822a0003e96e980c59a402f)
- ref: 1e8ff18a1215b711136b

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/36282324007)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260926-macm4pro-arm64-python-1e8ff18a1215b711136b-3.16.0a0-1e8ff18.json)

### vs. 3.12.6

- Geometric mean: 1.139x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260926-macm4pro-arm64-python-1e8ff18a1215b711136b-3.16.0a0-1e8ff18-vs-3.12.6.md)
- [📈time plot](bm-20260926-macm4pro-arm64-python-1e8ff18a1215b711136b-3.16.0a0-1e8ff18-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.052x faster (HPT: reliability of 98.89%, 1.00x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260926-macm4pro-arm64-python-1e8ff18a1215b711136b-3.16.0a0-1e8ff18-vs-3.13.0rc2.md)
- [📈time plot](bm-20260926-macm4pro-arm64-python-1e8ff18a1215b711136b-3.16.0a0-1e8ff18-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.007x slower (HPT: reliability of 84.81%, 1.00x slower at 99th %ile)
- Memory usage: 0.99x
- [🧠memory plot](bm-20260926-macm4pro-arm64-python-1e8ff18a1215b711136b-3.16.0a0-1e8ff18-vs-base-mem.svg)
- [📄table](bm-20260926-macm4pro-arm64-python-1e8ff18a1215b711136b-3.16.0a0-1e8ff18-vs-base.md)
- [📈time plot](bm-20260926-macm4pro-arm64-python-1e8ff18a1215b711136b-3.16.0a0-1e8ff18-vs-base.svg)

