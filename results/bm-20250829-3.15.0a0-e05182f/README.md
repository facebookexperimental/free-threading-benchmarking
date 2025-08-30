# Results

- fork: python/e05182f98ea100b6e267
- version: 3.15.0a0
- config: 
- commit hash: [e05182f](https://github.com/python/cpython/commit/e05182f)
- commit date: 2025-08-29T11:49:35-07:00
- commit merge base: [5f7906715adea645d8141d5337851872cfca4381](https://github.com/python/cpython/commit/5f7906715adea645d8141d5337851872cfca4381)
- ref: e05182f98ea100b6e267

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17336921888)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250829-vultr-x86_64-python-e05182f98ea100b6e267-3.15.0a0-e05182f.json)

### vs. 3.12.6

- Geometric mean: 1.069x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250829-vultr-x86_64-python-e05182f98ea100b6e267-3.15.0a0-e05182f-vs-3.12.6.md)
- [📈time plot](bm-20250829-vultr-x86_64-python-e05182f98ea100b6e267-3.15.0a0-e05182f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.034x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250829-vultr-x86_64-python-e05182f98ea100b6e267-3.15.0a0-e05182f-vs-3.13.0rc2.md)
- [📈time plot](bm-20250829-vultr-x86_64-python-e05182f98ea100b6e267-3.15.0a0-e05182f-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17336921888)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250829-macm4pro-arm64-python-e05182f98ea100b6e267-3.15.0a0-e05182f.json)

### vs. 3.12.6

- Geometric mean: 1.097x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250829-macm4pro-arm64-python-e05182f98ea100b6e267-3.15.0a0-e05182f-vs-3.12.6.md)
- [📈time plot](bm-20250829-macm4pro-arm64-python-e05182f98ea100b6e267-3.15.0a0-e05182f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.018x faster (HPT: reliability of 77.67%, 1.00x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250829-macm4pro-arm64-python-e05182f98ea100b6e267-3.15.0a0-e05182f-vs-3.13.0rc2.md)
- [📈time plot](bm-20250829-macm4pro-arm64-python-e05182f98ea100b6e267-3.15.0a0-e05182f-vs-3.13.0rc2.svg)

