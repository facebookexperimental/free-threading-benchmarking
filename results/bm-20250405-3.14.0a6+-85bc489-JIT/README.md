# Results

- fork: python/85bc489b649fe261f962
- version: 3.14.0a6+
- config: JIT
- commit hash: [85bc489](https://github.com/python/cpython/commit/85bc489)
- commit date: 2025-04-05T15:56:01-07:00
- commit merge base: [ad6a032cebf59d1668caa7e726aa5da72e1cbb5c](https://github.com/python/cpython/commit/ad6a032cebf59d1668caa7e726aa5da72e1cbb5c)
- ref: 85bc489b649fe261f962

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14287076184)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250405-vultr-x86_64-python-85bc489b649fe261f962-3.14.0a6%2B-85bc489.json)

### vs. 3.12.6

- Geometric mean: 1.085x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250405-vultr-x86_64-python-85bc489b649fe261f962-3.14.0a6%2B-85bc489-vs-3.12.6.md)
- [📈time plot](bm-20250405-vultr-x86_64-python-85bc489b649fe261f962-3.14.0a6%2B-85bc489-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.047x faster (HPT: reliability of 94.96%, 1.00x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, html5lib, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250405-vultr-x86_64-python-85bc489b649fe261f962-3.14.0a6%2B-85bc489-vs-3.13.0rc2.md)
- [📈time plot](bm-20250405-vultr-x86_64-python-85bc489b649fe261f962-3.14.0a6%2B-85bc489-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.007x faster (HPT: reliability of 56.31%, 1.00x slower at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20250405-vultr-x86_64-python-85bc489b649fe261f962-3.14.0a6%2B-85bc489-vs-base-mem.svg)
- [📄table](bm-20250405-vultr-x86_64-python-85bc489b649fe261f962-3.14.0a6%2B-85bc489-vs-base.md)
- [📈time plot](bm-20250405-vultr-x86_64-python-85bc489b649fe261f962-3.14.0a6%2B-85bc489-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14287076184)
- cpu model: missing
- platform: macOS-15.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20250405-macm4pro-arm64-python-85bc489b649fe261f962-3.14.0a6%2B-85bc489.json)

### vs. 3.12.6

- Geometric mean: 1.110x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250405-macm4pro-arm64-python-85bc489b649fe261f962-3.14.0a6%2B-85bc489-vs-3.12.6.md)
- [📈time plot](bm-20250405-macm4pro-arm64-python-85bc489b649fe261f962-3.14.0a6%2B-85bc489-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.029x faster (HPT: reliability of 93.12%, 1.00x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250405-macm4pro-arm64-python-85bc489b649fe261f962-3.14.0a6%2B-85bc489-vs-3.13.0rc2.md)
- [📈time plot](bm-20250405-macm4pro-arm64-python-85bc489b649fe261f962-3.14.0a6%2B-85bc489-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.008x faster (HPT: reliability of 98.89%, 1.00x faster at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20250405-macm4pro-arm64-python-85bc489b649fe261f962-3.14.0a6%2B-85bc489-vs-base-mem.svg)
- [📄table](bm-20250405-macm4pro-arm64-python-85bc489b649fe261f962-3.14.0a6%2B-85bc489-vs-base.md)
- [📈time plot](bm-20250405-macm4pro-arm64-python-85bc489b649fe261f962-3.14.0a6%2B-85bc489-vs-base.svg)

