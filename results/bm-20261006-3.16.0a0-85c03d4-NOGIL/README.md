# Results

- fork: python/85c03d47a240247d4179
- version: 3.16.0a0
- config: NOGIL
- commit hash: [85c03d4](https://github.com/python/cpython/commit/85c03d4)
- commit date: 2026-10-06T00:06:09Z
- commit merge base: [047157b8915604c3d3f9914cbba7e458b2abfe7b](https://github.com/python/cpython/commit/047157b8915604c3d3f9914cbba7e458b2abfe7b)
- commit date: 2026-10-06T00:06:09+00:00
- ref: 85c03d47a240247d4179

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/37395558258)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261006-vultr-x86_64-python-85c03d47a240247d4179-3.16.0a0-85c03d4.json)

### vs. 3.12.6

- Geometric mean: 1.039x slower (HPT: reliability of 72.75%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261006-vultr-x86_64-python-85c03d47a240247d4179-3.16.0a0-85c03d4-vs-3.12.6.md)
- [📈time plot](bm-20261006-vultr-x86_64-python-85c03d47a240247d4179-3.16.0a0-85c03d4-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.072x slower (HPT: reliability of 94.59%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261006-vultr-x86_64-python-85c03d47a240247d4179-3.16.0a0-85c03d4-vs-3.13.0rc2.md)
- [📈time plot](bm-20261006-vultr-x86_64-python-85c03d47a240247d4179-3.16.0a0-85c03d4-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.102x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20261006-vultr-x86_64-python-85c03d47a240247d4179-3.16.0a0-85c03d4-vs-base-mem.svg)
- [📄table](bm-20261006-vultr-x86_64-python-85c03d47a240247d4179-3.16.0a0-85c03d4-vs-base.md)
- [📈time plot](bm-20261006-vultr-x86_64-python-85c03d47a240247d4179-3.16.0a0-85c03d4-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/37395558258)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261006-macm4pro-arm64-python-85c03d47a240247d4179-3.16.0a0-85c03d4.json)

### vs. 3.12.6

- Geometric mean: 1.059x faster (HPT: reliability of 88.10%, 1.00x faster at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261006-macm4pro-arm64-python-85c03d47a240247d4179-3.16.0a0-85c03d4-vs-3.12.6.md)
- [📈time plot](bm-20261006-macm4pro-arm64-python-85c03d47a240247d4179-3.16.0a0-85c03d4-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.019x slower (HPT: reliability of 94.31%, 1.00x slower at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261006-macm4pro-arm64-python-85c03d47a240247d4179-3.16.0a0-85c03d4-vs-3.13.0rc2.md)
- [📈time plot](bm-20261006-macm4pro-arm64-python-85c03d47a240247d4179-3.16.0a0-85c03d4-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.078x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.11x
- new benchmarks: coverage
- [🧠memory plot](bm-20261006-macm4pro-arm64-python-85c03d47a240247d4179-3.16.0a0-85c03d4-vs-base-mem.svg)
- [📄table](bm-20261006-macm4pro-arm64-python-85c03d47a240247d4179-3.16.0a0-85c03d4-vs-base.md)
- [📈time plot](bm-20261006-macm4pro-arm64-python-85c03d47a240247d4179-3.16.0a0-85c03d4-vs-base.svg)

