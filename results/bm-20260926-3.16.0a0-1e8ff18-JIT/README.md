# Results

- fork: python/1e8ff18a1215b711136b
- version: 3.16.0a0
- config: JIT
- commit hash: [1e8ff18](https://github.com/python/cpython/commit/1e8ff18)
- commit date: 2026-09-26T20:19:25Z
- commit merge base: [972cfaae3f1349a2b822a0003e96e980c59a402f](https://github.com/python/cpython/commit/972cfaae3f1349a2b822a0003e96e980c59a402f)
- commit date: 2026-09-26T20:19:25+00:00
- ref: 1e8ff18a1215b711136b

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/36282324007)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260926-vultr-x86_64-python-1e8ff18a1215b711136b-3.16.0a0-1e8ff18.json)

### vs. 3.12.6

- Geometric mean: 1.160x faster (HPT: reliability of 100.00%, 1.08x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260926-vultr-x86_64-python-1e8ff18a1215b711136b-3.16.0a0-1e8ff18-vs-3.12.6.md)
- [📈time plot](bm-20260926-vultr-x86_64-python-1e8ff18a1215b711136b-3.16.0a0-1e8ff18-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.121x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260926-vultr-x86_64-python-1e8ff18a1215b711136b-3.16.0a0-1e8ff18-vs-3.13.0rc2.md)
- [📈time plot](bm-20260926-vultr-x86_64-python-1e8ff18a1215b711136b-3.16.0a0-1e8ff18-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.087x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.05x
- [🧠memory plot](bm-20260926-vultr-x86_64-python-1e8ff18a1215b711136b-3.16.0a0-1e8ff18-vs-base-mem.svg)
- [📄table](bm-20260926-vultr-x86_64-python-1e8ff18a1215b711136b-3.16.0a0-1e8ff18-vs-base.md)
- [📈time plot](bm-20260926-vultr-x86_64-python-1e8ff18a1215b711136b-3.16.0a0-1e8ff18-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/36282324007)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260926-macm4pro-arm64-python-1e8ff18a1215b711136b-3.16.0a0-1e8ff18.json)

### vs. 3.12.6

- Geometric mean: 1.255x faster (HPT: reliability of 100.00%, 1.12x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260926-macm4pro-arm64-python-1e8ff18a1215b711136b-3.16.0a0-1e8ff18-vs-3.12.6.md)
- [📈time plot](bm-20260926-macm4pro-arm64-python-1e8ff18a1215b711136b-3.16.0a0-1e8ff18-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.160x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260926-macm4pro-arm64-python-1e8ff18a1215b711136b-3.16.0a0-1e8ff18-vs-3.13.0rc2.md)
- [📈time plot](bm-20260926-macm4pro-arm64-python-1e8ff18a1215b711136b-3.16.0a0-1e8ff18-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.096x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.05x
- [🧠memory plot](bm-20260926-macm4pro-arm64-python-1e8ff18a1215b711136b-3.16.0a0-1e8ff18-vs-base-mem.svg)
- [📄table](bm-20260926-macm4pro-arm64-python-1e8ff18a1215b711136b-3.16.0a0-1e8ff18-vs-base.md)
- [📈time plot](bm-20260926-macm4pro-arm64-python-1e8ff18a1215b711136b-3.16.0a0-1e8ff18-vs-base.svg)

