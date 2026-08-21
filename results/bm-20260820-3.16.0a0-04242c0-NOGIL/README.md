# Results

- fork: python/04242c027feeff726acb
- version: 3.16.0a0
- config: NOGIL
- commit hash: [04242c0](https://github.com/python/cpython/commit/04242c0)
- commit date: 2026-08-20T12:24:45-07:00
- commit merge base: [83531fd39f24f873671c38b981061afe1730613f](https://github.com/python/cpython/commit/83531fd39f24f873671c38b981061afe1730613f)
- ref: 04242c027feeff726acb

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/32432147477)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260820-vultr-x86_64-python-04242c027feeff726acb-3.16.0a0-04242c0.json)

### vs. 3.12.6

- Geometric mean: 1.035x slower (HPT: reliability of 76.26%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260820-vultr-x86_64-python-04242c027feeff726acb-3.16.0a0-04242c0-vs-3.12.6.md)
- [📈time plot](bm-20260820-vultr-x86_64-python-04242c027feeff726acb-3.16.0a0-04242c0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.067x slower (HPT: reliability of 96.04%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260820-vultr-x86_64-python-04242c027feeff726acb-3.16.0a0-04242c0-vs-3.13.0rc2.md)
- [📈time plot](bm-20260820-vultr-x86_64-python-04242c027feeff726acb-3.16.0a0-04242c0-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.104x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20260820-vultr-x86_64-python-04242c027feeff726acb-3.16.0a0-04242c0-vs-base-mem.svg)
- [📄table](bm-20260820-vultr-x86_64-python-04242c027feeff726acb-3.16.0a0-04242c0-vs-base.md)
- [📈time plot](bm-20260820-vultr-x86_64-python-04242c027feeff726acb-3.16.0a0-04242c0-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/32432147477)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0.json)

### vs. 3.12.6

- Geometric mean: 1.010x faster (HPT: reliability of 81.16%, 1.00x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0-vs-3.12.6.md)
- [📈time plot](bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.064x slower (HPT: reliability of 99.78%, 1.01x slower at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0-vs-3.13.0rc2.md)
- [📈time plot](bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.106x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.12x
- new benchmarks: coverage
- [🧠memory plot](bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0-vs-base-mem.svg)
- [📄table](bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0-vs-base.md)
- [📈time plot](bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0-vs-base.svg)

