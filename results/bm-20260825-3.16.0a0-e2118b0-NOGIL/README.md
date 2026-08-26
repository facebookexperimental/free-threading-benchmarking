# Results

- fork: python/e2118b0ac21191bfeecd
- version: 3.16.0a0
- config: NOGIL
- commit hash: [e2118b0](https://github.com/python/cpython/commit/e2118b0)
- commit date: 2026-08-25T16:48:54-07:00
- commit merge base: [7cc333439b6426a43cdbca690d9170c9db0d8669](https://github.com/python/cpython/commit/7cc333439b6426a43cdbca690d9170c9db0d8669)
- ref: e2118b0ac21191bfeecd

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/32914518010)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0.json)

### vs. 3.12.6

- Geometric mean: 1.036x slower (HPT: reliability of 81.44%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0-vs-3.12.6.md)
- [📈time plot](bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.068x slower (HPT: reliability of 97.59%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0-vs-3.13.0rc2.md)
- [📈time plot](bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.099x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0-vs-base-mem.svg)
- [📄table](bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0-vs-base.md)
- [📈time plot](bm-20260825-vultr-x86_64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/32914518010)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260825-macm4pro-arm64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0.json)

### vs. 3.12.6

- Geometric mean: 1.017x faster (HPT: reliability of 65.58%, 1.00x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260825-macm4pro-arm64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0-vs-3.12.6.md)
- [📈time plot](bm-20260825-macm4pro-arm64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.058x slower (HPT: reliability of 99.47%, 1.00x slower at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260825-macm4pro-arm64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0-vs-3.13.0rc2.md)
- [📈time plot](bm-20260825-macm4pro-arm64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.104x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.12x
- new benchmarks: coverage
- [🧠memory plot](bm-20260825-macm4pro-arm64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0-vs-base-mem.svg)
- [📄table](bm-20260825-macm4pro-arm64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0-vs-base.md)
- [📈time plot](bm-20260825-macm4pro-arm64-python-e2118b0ac21191bfeecd-3.16.0a0-e2118b0-vs-base.svg)

