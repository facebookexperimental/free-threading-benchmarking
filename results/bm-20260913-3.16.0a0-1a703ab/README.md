# Results

- fork: python/1a703ab9e6a050b40c46
- version: 3.16.0a0
- config: 
- commit hash: [1a703ab](https://github.com/python/cpython/commit/1a703ab)
- commit date: 2026-09-13T01:09:22+01:00
- commit merge base: [121e27c484539faaf24e6b264846217a8f4b9738](https://github.com/python/cpython/commit/121e27c484539faaf24e6b264846217a8f4b9738)
- ref: 1a703ab9e6a050b40c46

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/34727770454)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [pystats raw](bm-20260913-vultr-x86_64-python-1a703ab9e6a050b40c46-3.16.0a0-1a703ab-pystats.json)
- [pystats table](bm-20260913-vultr-x86_64-python-1a703ab9e6a050b40c46-3.16.0a0-1a703ab-pystats.md)
- [raw results](bm-20260913-vultr-x86_64-python-1a703ab9e6a050b40c46-3.16.0a0-1a703ab.json)

### vs. 3.12.6

- Geometric mean: 1.058x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260913-vultr-x86_64-python-1a703ab9e6a050b40c46-3.16.0a0-1a703ab-vs-3.12.6.md)
- [📈time plot](bm-20260913-vultr-x86_64-python-1a703ab9e6a050b40c46-3.16.0a0-1a703ab-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.023x faster (HPT: reliability of 99.91%, 1.00x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260913-vultr-x86_64-python-1a703ab9e6a050b40c46-3.16.0a0-1a703ab-vs-3.13.0rc2.md)
- [📈time plot](bm-20260913-vultr-x86_64-python-1a703ab9e6a050b40c46-3.16.0a0-1a703ab-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/34727770454)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260913-macm4pro-arm64-python-1a703ab9e6a050b40c46-3.16.0a0-1a703ab.json)

### vs. 3.12.6

- Geometric mean: 1.129x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260913-macm4pro-arm64-python-1a703ab9e6a050b40c46-3.16.0a0-1a703ab-vs-3.12.6.md)
- [📈time plot](bm-20260913-macm4pro-arm64-python-1a703ab9e6a050b40c46-3.16.0a0-1a703ab-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.043x faster (HPT: reliability of 98.64%, 1.00x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260913-macm4pro-arm64-python-1a703ab9e6a050b40c46-3.16.0a0-1a703ab-vs-3.13.0rc2.md)
- [📈time plot](bm-20260913-macm4pro-arm64-python-1a703ab9e6a050b40c46-3.16.0a0-1a703ab-vs-3.13.0rc2.svg)

