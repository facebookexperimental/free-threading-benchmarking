# Results

- fork: python/1277a5e5820ee7478654
- version: 3.16.0a1+dev
- config: 
- commit hash: [1277a5e](https://github.com/python/cpython/commit/1277a5e)
- commit date: 2026-10-20T17:25:31-07:00
- commit merge base: [f9c0e1ea27a8731fecc3395ae31fc88277ff24b3](https://github.com/python/cpython/commit/f9c0e1ea27a8731fecc3395ae31fc88277ff24b3)
- ref: 1277a5e5820ee7478654

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/39522505545)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261020-vultr-x86_64-python-1277a5e5820ee7478654-3.16.0a1%2Bdev-1277a5e.json)

### vs. 3.12.6

- Geometric mean: 1.081x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261020-vultr-x86_64-python-1277a5e5820ee7478654-3.16.0a1%2Bdev-1277a5e-vs-3.12.6.md)
- [📈time plot](bm-20261020-vultr-x86_64-python-1277a5e5820ee7478654-3.16.0a1%2Bdev-1277a5e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.044x faster (HPT: reliability of 99.76%, 1.01x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261020-vultr-x86_64-python-1277a5e5820ee7478654-3.16.0a1%2Bdev-1277a5e-vs-3.13.0rc2.md)
- [📈time plot](bm-20261020-vultr-x86_64-python-1277a5e5820ee7478654-3.16.0a1%2Bdev-1277a5e-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/39522505545)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261020-macm4pro-arm64-python-1277a5e5820ee7478654-3.16.0a1%2Bdev-1277a5e.json)

### vs. 3.12.6

- Geometric mean: 1.206x faster (HPT: reliability of 100.00%, 1.11x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261020-macm4pro-arm64-python-1277a5e5820ee7478654-3.16.0a1%2Bdev-1277a5e-vs-3.12.6.md)
- [📈time plot](bm-20261020-macm4pro-arm64-python-1277a5e5820ee7478654-3.16.0a1%2Bdev-1277a5e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.114x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261020-macm4pro-arm64-python-1277a5e5820ee7478654-3.16.0a1%2Bdev-1277a5e-vs-3.13.0rc2.md)
- [📈time plot](bm-20261020-macm4pro-arm64-python-1277a5e5820ee7478654-3.16.0a1%2Bdev-1277a5e-vs-3.13.0rc2.svg)

