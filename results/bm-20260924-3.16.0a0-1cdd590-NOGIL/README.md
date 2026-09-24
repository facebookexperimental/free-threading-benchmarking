# Results

- fork: python/1cdd590cb547597ab64b
- version: 3.16.0a0
- config: NOGIL
- commit hash: [1cdd590](https://github.com/python/cpython/commit/1cdd590)
- commit date: 2026-09-24T01:23:06+01:00
- commit merge base: [6893326350024d0ed3a6fa4ff59e4139b2647411](https://github.com/python/cpython/commit/6893326350024d0ed3a6fa4ff59e4139b2647411)
- ref: 1cdd590cb547597ab64b

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/35939491903)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260924-vultr-x86_64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590.json)

### vs. 3.12.6

- Geometric mean: 1.044x slower (HPT: reliability of 83.24%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260924-vultr-x86_64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590-vs-3.12.6.md)
- [📈time plot](bm-20260924-vultr-x86_64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.076x slower (HPT: reliability of 98.68%, 1.00x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260924-vultr-x86_64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590-vs-3.13.0rc2.md)
- [📈time plot](bm-20260924-vultr-x86_64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.104x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20260924-vultr-x86_64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590-vs-base-mem.svg)
- [📄table](bm-20260924-vultr-x86_64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590-vs-base.md)
- [📈time plot](bm-20260924-vultr-x86_64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/35939491903)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590.json)

### vs. 3.12.6

- Geometric mean: 1.082x faster (HPT: reliability of 97.16%, 1.00x faster at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590-vs-3.12.6.md)
- [📈time plot](bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.002x faster (HPT: reliability of 92.73%, 1.00x slower at 99th %ile)
- Memory usage: 1.30x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590-vs-3.13.0rc2.md)
- [📈time plot](bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.042x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: 1.12x
- new benchmarks: coverage
- [🧠memory plot](bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590-vs-base-mem.svg)
- [📄table](bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590-vs-base.md)
- [📈time plot](bm-20260924-macm4pro-arm64-python-1cdd590cb547597ab64b-3.16.0a0-1cdd590-vs-base.svg)

