# Results

- fork: python/de9c32fc34fe2e000de1
- version: 3.16.0a0
- config: 
- commit hash: [de9c32f](https://github.com/python/cpython/commit/de9c32f)
- commit date: 2026-05-20T00:47:44Z
- commit merge base: [1f3c2679f1a2a106019ceedc7a61c278a445c264](https://github.com/python/cpython/commit/1f3c2679f1a2a106019ceedc7a61c278a445c264)
- commit date: 2026-05-20T00:47:44+00:00
- ref: de9c32fc34fe2e000de1

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/26134795677)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260520-vultr-x86_64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f.json)

### vs. 3.12.6

- Geometric mean: 1.062x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260520-vultr-x86_64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f-vs-3.12.6.md)
- [📈time plot](bm-20260520-vultr-x86_64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.024x faster (HPT: reliability of 99.71%, 1.00x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260520-vultr-x86_64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f-vs-3.13.0rc2.md)
- [📈time plot](bm-20260520-vultr-x86_64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/26134795677)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260520-macm4pro-arm64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f.json)

### vs. 3.12.6

- Geometric mean: 1.123x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: 2to3, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260520-macm4pro-arm64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f-vs-3.12.6.md)
- [📈time plot](bm-20260520-macm4pro-arm64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.037x faster (HPT: reliability of 99.35%, 1.00x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: 2to3, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260520-macm4pro-arm64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f-vs-3.13.0rc2.md)
- [📈time plot](bm-20260520-macm4pro-arm64-python-de9c32fc34fe2e000de1-3.16.0a0-de9c32f-vs-3.13.0rc2.svg)

