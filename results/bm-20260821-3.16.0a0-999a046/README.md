# Results

- fork: python/999a046b24cff4ba0e72
- version: 3.16.0a0
- config: 
- commit hash: [999a046](https://github.com/python/cpython/commit/999a046)
- commit date: 2026-08-21T10:02:24-07:00
- commit merge base: [862befdb99c8268f570c28adaa342eb6586fa0dc](https://github.com/python/cpython/commit/862befdb99c8268f570c28adaa342eb6586fa0dc)
- ref: 999a046b24cff4ba0e72

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/32539823852)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260821-vultr-x86_64-python-999a046b24cff4ba0e72-3.16.0a0-999a046.json)

### vs. 3.12.6

- Geometric mean: 1.073x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260821-vultr-x86_64-python-999a046b24cff4ba0e72-3.16.0a0-999a046-vs-3.12.6.md)
- [📈time plot](bm-20260821-vultr-x86_64-python-999a046b24cff4ba0e72-3.16.0a0-999a046-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.038x faster (HPT: reliability of 99.99%, 1.01x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260821-vultr-x86_64-python-999a046b24cff4ba0e72-3.16.0a0-999a046-vs-3.13.0rc2.md)
- [📈time plot](bm-20260821-vultr-x86_64-python-999a046b24cff4ba0e72-3.16.0a0-999a046-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/32539823852)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260821-macm4pro-arm64-python-999a046b24cff4ba0e72-3.16.0a0-999a046.json)

### vs. 3.12.6

- Geometric mean: 1.128x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260821-macm4pro-arm64-python-999a046b24cff4ba0e72-3.16.0a0-999a046-vs-3.12.6.md)
- [📈time plot](bm-20260821-macm4pro-arm64-python-999a046b24cff4ba0e72-3.16.0a0-999a046-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.041x faster (HPT: reliability of 97.98%, 1.00x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260821-macm4pro-arm64-python-999a046b24cff4ba0e72-3.16.0a0-999a046-vs-3.13.0rc2.md)
- [📈time plot](bm-20260821-macm4pro-arm64-python-999a046b24cff4ba0e72-3.16.0a0-999a046-vs-3.13.0rc2.svg)

