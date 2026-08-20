# Results

- fork: python/bf95881b84662d3dcd35
- version: 3.16.0a0
- config: 
- commit hash: [bf95881](https://github.com/python/cpython/commit/bf95881)
- commit date: 2026-08-19T21:28:43+01:00
- commit merge base: [a2c9a3b0aad0aca332197ac5eed41eb41442fb0c](https://github.com/python/cpython/commit/a2c9a3b0aad0aca332197ac5eed41eb41442fb0c)
- ref: bf95881b84662d3dcd35

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/32316723705)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260819-vultr-x86_64-python-bf95881b84662d3dcd35-3.16.0a0-bf95881.json)

### vs. 3.12.6

- Geometric mean: 1.066x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260819-vultr-x86_64-python-bf95881b84662d3dcd35-3.16.0a0-bf95881-vs-3.12.6.md)
- [📈time plot](bm-20260819-vultr-x86_64-python-bf95881b84662d3dcd35-3.16.0a0-bf95881-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.030x faster (HPT: reliability of 99.83%, 1.00x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260819-vultr-x86_64-python-bf95881b84662d3dcd35-3.16.0a0-bf95881-vs-3.13.0rc2.md)
- [📈time plot](bm-20260819-vultr-x86_64-python-bf95881b84662d3dcd35-3.16.0a0-bf95881-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/32316723705)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260819-macm4pro-arm64-python-bf95881b84662d3dcd35-3.16.0a0-bf95881.json)

### vs. 3.12.6

- Geometric mean: 1.132x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260819-macm4pro-arm64-python-bf95881b84662d3dcd35-3.16.0a0-bf95881-vs-3.12.6.md)
- [📈time plot](bm-20260819-macm4pro-arm64-python-bf95881b84662d3dcd35-3.16.0a0-bf95881-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.046x faster (HPT: reliability of 98.71%, 1.00x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260819-macm4pro-arm64-python-bf95881b84662d3dcd35-3.16.0a0-bf95881-vs-3.13.0rc2.md)
- [📈time plot](bm-20260819-macm4pro-arm64-python-bf95881b84662d3dcd35-3.16.0a0-bf95881-vs-3.13.0rc2.svg)

