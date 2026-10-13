# Results

- fork: python/64018ac45cbc3f408412
- version: 3.16.0a0
- config: 
- commit hash: [64018ac](https://github.com/python/cpython/commit/64018ac)
- commit date: 2026-10-12T19:48:41-04:00
- commit merge base: [6979003a1d73383ce798eb1301fe93d4d74b1903](https://github.com/python/cpython/commit/6979003a1d73383ce798eb1301fe93d4d74b1903)
- ref: 64018ac45cbc3f408412

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/38328975530)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261012-vultr-x86_64-python-64018ac45cbc3f408412-3.16.0a0-64018ac.json)

### vs. 3.12.6

- Geometric mean: 1.074x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261012-vultr-x86_64-python-64018ac45cbc3f408412-3.16.0a0-64018ac-vs-3.12.6.md)
- [📈time plot](bm-20261012-vultr-x86_64-python-64018ac45cbc3f408412-3.16.0a0-64018ac-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.037x faster (HPT: reliability of 99.66%, 1.00x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261012-vultr-x86_64-python-64018ac45cbc3f408412-3.16.0a0-64018ac-vs-3.13.0rc2.md)
- [📈time plot](bm-20261012-vultr-x86_64-python-64018ac45cbc3f408412-3.16.0a0-64018ac-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/38328975530)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261012-macm4pro-arm64-python-64018ac45cbc3f408412-3.16.0a0-64018ac.json)

### vs. 3.12.6

- Geometric mean: 1.191x faster (HPT: reliability of 100.00%, 1.10x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261012-macm4pro-arm64-python-64018ac45cbc3f408412-3.16.0a0-64018ac-vs-3.12.6.md)
- [📈time plot](bm-20261012-macm4pro-arm64-python-64018ac45cbc3f408412-3.16.0a0-64018ac-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.101x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261012-macm4pro-arm64-python-64018ac45cbc3f408412-3.16.0a0-64018ac-vs-3.13.0rc2.md)
- [📈time plot](bm-20261012-macm4pro-arm64-python-64018ac45cbc3f408412-3.16.0a0-64018ac-vs-3.13.0rc2.svg)

