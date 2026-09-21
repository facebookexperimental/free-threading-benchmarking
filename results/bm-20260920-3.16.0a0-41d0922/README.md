# Results

- fork: python/41d09220bda74cda6897
- version: 3.16.0a0
- config: 
- commit hash: [41d0922](https://github.com/python/cpython/commit/41d0922)
- commit date: 2026-09-20T22:08:23Z
- commit merge base: [de0d9763682b414c028b3443aeab60fe2daec645](https://github.com/python/cpython/commit/de0d9763682b414c028b3443aeab60fe2daec645)
- commit date: 2026-09-20T22:08:23+00:00
- ref: 41d09220bda74cda6897

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/35548674360)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260920-vultr-x86_64-python-41d09220bda74cda6897-3.16.0a0-41d0922.json)

### vs. 3.12.6

- Geometric mean: 1.065x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260920-vultr-x86_64-python-41d09220bda74cda6897-3.16.0a0-41d0922-vs-3.12.6.md)
- [📈time plot](bm-20260920-vultr-x86_64-python-41d09220bda74cda6897-3.16.0a0-41d0922-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.030x faster (HPT: reliability of 99.95%, 1.00x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260920-vultr-x86_64-python-41d09220bda74cda6897-3.16.0a0-41d0922-vs-3.13.0rc2.md)
- [📈time plot](bm-20260920-vultr-x86_64-python-41d09220bda74cda6897-3.16.0a0-41d0922-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/35548674360)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260920-macm4pro-arm64-python-41d09220bda74cda6897-3.16.0a0-41d0922.json)

### vs. 3.12.6

- Geometric mean: 1.141x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260920-macm4pro-arm64-python-41d09220bda74cda6897-3.16.0a0-41d0922-vs-3.12.6.md)
- [📈time plot](bm-20260920-macm4pro-arm64-python-41d09220bda74cda6897-3.16.0a0-41d0922-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.054x faster (HPT: reliability of 99.77%, 1.00x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260920-macm4pro-arm64-python-41d09220bda74cda6897-3.16.0a0-41d0922-vs-3.13.0rc2.md)
- [📈time plot](bm-20260920-macm4pro-arm64-python-41d09220bda74cda6897-3.16.0a0-41d0922-vs-3.13.0rc2.svg)

