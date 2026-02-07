# Results

- fork: python/74db4404eaa9b4448b50
- version: 3.15.0a5+
- config: 
- commit hash: [74db440](https://github.com/python/cpython/commit/74db440)
- commit date: 2026-02-06T13:26:44-08:00
- commit merge base: [895e83727d6d686ab7dd5494f3ccd52b0726502e](https://github.com/python/cpython/commit/895e83727d6d686ab7dd5494f3ccd52b0726502e)
- ref: 74db4404eaa9b4448b50

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21770835267)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260206-vultr-x86_64-python-74db4404eaa9b4448b50-3.15.0a5%2B-74db440.json)

### vs. 3.12.6

- Geometric mean: 1.076x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260206-vultr-x86_64-python-74db4404eaa9b4448b50-3.15.0a5%2B-74db440-vs-3.12.6.md)
- [📈time plot](bm-20260206-vultr-x86_64-python-74db4404eaa9b4448b50-3.15.0a5%2B-74db440-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.040x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260206-vultr-x86_64-python-74db4404eaa9b4448b50-3.15.0a5%2B-74db440-vs-3.13.0rc2.md)
- [📈time plot](bm-20260206-vultr-x86_64-python-74db4404eaa9b4448b50-3.15.0a5%2B-74db440-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21770835267)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260206-macm4pro-arm64-python-74db4404eaa9b4448b50-3.15.0a5%2B-74db440.json)

### vs. 3.12.6

- Geometric mean: 1.195x faster (HPT: reliability of 100.00%, 1.10x faster at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260206-macm4pro-arm64-python-74db4404eaa9b4448b50-3.15.0a5%2B-74db440-vs-3.12.6.md)
- [📈time plot](bm-20260206-macm4pro-arm64-python-74db4404eaa9b4448b50-3.15.0a5%2B-74db440-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.109x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260206-macm4pro-arm64-python-74db4404eaa9b4448b50-3.15.0a5%2B-74db440-vs-3.13.0rc2.md)
- [📈time plot](bm-20260206-macm4pro-arm64-python-74db4404eaa9b4448b50-3.15.0a5%2B-74db440-vs-3.13.0rc2.svg)

