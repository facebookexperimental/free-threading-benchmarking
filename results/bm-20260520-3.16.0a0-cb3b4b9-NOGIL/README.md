# Results

- fork: python/cb3b4b98d8d141c9de04
- version: 3.16.0a0
- config: NOGIL
- commit hash: [cb3b4b9](https://github.com/python/cpython/commit/cb3b4b9)
- commit date: 2026-05-20T12:40:15-07:00
- commit merge base: [87a879f4d0ec2e545e84c898c5ce452a6c87b09e](https://github.com/python/cpython/commit/87a879f4d0ec2e545e84c898c5ce452a6c87b09e)
- ref: cb3b4b98d8d141c9de04

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/26199117883)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260520-vultr-x86_64-python-cb3b4b98d8d141c9de04-3.16.0a0-cb3b4b9.json)

### vs. 3.12.6

- Geometric mean: 1.038x slower (HPT: reliability of 93.45%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260520-vultr-x86_64-python-cb3b4b98d8d141c9de04-3.16.0a0-cb3b4b9-vs-3.12.6.md)
- [📈time plot](bm-20260520-vultr-x86_64-python-cb3b4b98d8d141c9de04-3.16.0a0-cb3b4b9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.072x slower (HPT: reliability of 97.70%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260520-vultr-x86_64-python-cb3b4b98d8d141c9de04-3.16.0a0-cb3b4b9-vs-3.13.0rc2.md)
- [📈time plot](bm-20260520-vultr-x86_64-python-cb3b4b98d8d141c9de04-3.16.0a0-cb3b4b9-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.099x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20260520-vultr-x86_64-python-cb3b4b98d8d141c9de04-3.16.0a0-cb3b4b9-vs-base-mem.svg)
- [📄table](bm-20260520-vultr-x86_64-python-cb3b4b98d8d141c9de04-3.16.0a0-cb3b4b9-vs-base.md)
- [📈time plot](bm-20260520-vultr-x86_64-python-cb3b4b98d8d141c9de04-3.16.0a0-cb3b4b9-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/26199117883)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260520-macm4pro-arm64-python-cb3b4b98d8d141c9de04-3.16.0a0-cb3b4b9.json)

### vs. 3.12.6

- Geometric mean: 1.099x faster (HPT: reliability of 99.58%, 1.00x faster at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: 2to3, asyncio_websockets, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260520-macm4pro-arm64-python-cb3b4b98d8d141c9de04-3.16.0a0-cb3b4b9-vs-3.12.6.md)
- [📈time plot](bm-20260520-macm4pro-arm64-python-cb3b4b98d8d141c9de04-3.16.0a0-cb3b4b9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.014x faster (HPT: reliability of 69.33%, 1.00x slower at 99th %ile)
- Memory usage: 1.30x
- missing benchmarks: 2to3, asyncio_websockets, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260520-macm4pro-arm64-python-cb3b4b98d8d141c9de04-3.16.0a0-cb3b4b9-vs-3.13.0rc2.md)
- [📈time plot](bm-20260520-macm4pro-arm64-python-cb3b4b98d8d141c9de04-3.16.0a0-cb3b4b9-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.021x slower (HPT: reliability of 99.98%, 1.01x slower at 99th %ile)
- Memory usage: 1.11x
- new benchmarks: dask
- [🧠memory plot](bm-20260520-macm4pro-arm64-python-cb3b4b98d8d141c9de04-3.16.0a0-cb3b4b9-vs-base-mem.svg)
- [📄table](bm-20260520-macm4pro-arm64-python-cb3b4b98d8d141c9de04-3.16.0a0-cb3b4b9-vs-base.md)
- [📈time plot](bm-20260520-macm4pro-arm64-python-cb3b4b98d8d141c9de04-3.16.0a0-cb3b4b9-vs-base.svg)

