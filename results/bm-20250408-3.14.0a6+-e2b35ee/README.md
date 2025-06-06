# Results

- fork: python/e2b35ee22950bc5dc541
- version: 3.14.0a6+
- config: 
- commit hash: [e2b35ee](https://github.com/python/cpython/commit/e2b35ee)
- commit date: 2025-04-08T09:23:48+09:00
- commit merge base: [f5639d87f59043d3075dbd3d9075f30e872dd91a](https://github.com/python/cpython/commit/f5639d87f59043d3075dbd3d9075f30e872dd91a)
- ref: e2b35ee22950bc5dc541

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14322252201)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6%2B-e2b35ee.json)

### vs. 3.12.6

- Geometric mean: 1.075x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6%2B-e2b35ee-vs-3.12.6.md)
- [📈time plot](bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6%2B-e2b35ee-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.037x faster (HPT: reliability of 95.06%, 1.00x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6%2B-e2b35ee-vs-3.13.0rc2.md)
- [📈time plot](bm-20250408-vultr-x86_64-python-e2b35ee22950bc5dc541-3.14.0a6%2B-e2b35ee-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14322252201)
- cpu model: missing
- platform: macOS-15.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20250408-macm4pro-arm64-python-e2b35ee22950bc5dc541-3.14.0a6%2B-e2b35ee.json)

### vs. 3.12.6

- Geometric mean: 1.105x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250408-macm4pro-arm64-python-e2b35ee22950bc5dc541-3.14.0a6%2B-e2b35ee-vs-3.12.6.md)
- [📈time plot](bm-20250408-macm4pro-arm64-python-e2b35ee22950bc5dc541-3.14.0a6%2B-e2b35ee-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.025x faster (HPT: reliability of 67.73%, 1.00x faster at 99th %ile)
- Memory usage: 1.08x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250408-macm4pro-arm64-python-e2b35ee22950bc5dc541-3.14.0a6%2B-e2b35ee-vs-3.13.0rc2.md)
- [📈time plot](bm-20250408-macm4pro-arm64-python-e2b35ee22950bc5dc541-3.14.0a6%2B-e2b35ee-vs-3.13.0rc2.svg)

