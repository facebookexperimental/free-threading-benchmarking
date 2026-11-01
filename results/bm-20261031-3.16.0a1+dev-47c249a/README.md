# Results

- fork: python/47c249adf3bc2ae3264a
- version: 3.16.0a1+dev
- config: 
- commit hash: [47c249a](https://github.com/python/cpython/commit/47c249a)
- commit date: 2026-10-31T23:43:11Z
- commit merge base: [e7acd6a82f2feec196b84fdfc1d1533e37024221](https://github.com/python/cpython/commit/e7acd6a82f2feec196b84fdfc1d1533e37024221)
- commit date: 2026-10-31T23:43:11+00:00
- ref: 47c249adf3bc2ae3264a

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/41255850807)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [pystats raw](bm-20261031-vultr-x86_64-python-47c249adf3bc2ae3264a-3.16.0a1%2Bdev-47c249a-pystats.json)
- [pystats table](bm-20261031-vultr-x86_64-python-47c249adf3bc2ae3264a-3.16.0a1%2Bdev-47c249a-pystats.md)
- [raw results](bm-20261031-vultr-x86_64-python-47c249adf3bc2ae3264a-3.16.0a1%2Bdev-47c249a.json)

### vs. 3.12.6

- Geometric mean: 1.091x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261031-vultr-x86_64-python-47c249adf3bc2ae3264a-3.16.0a1%2Bdev-47c249a-vs-3.12.6.md)
- [📈time plot](bm-20261031-vultr-x86_64-python-47c249adf3bc2ae3264a-3.16.0a1%2Bdev-47c249a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.055x faster (HPT: reliability of 99.99%, 1.01x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261031-vultr-x86_64-python-47c249adf3bc2ae3264a-3.16.0a1%2Bdev-47c249a-vs-3.13.0rc2.md)
- [📈time plot](bm-20261031-vultr-x86_64-python-47c249adf3bc2ae3264a-3.16.0a1%2Bdev-47c249a-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/41255850807)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1%2Bdev-47c249a.json)

### vs. 3.12.6

- Geometric mean: 1.216x faster (HPT: reliability of 100.00%, 1.12x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1%2Bdev-47c249a-vs-3.12.6.md)
- [📈time plot](bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1%2Bdev-47c249a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.123x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1%2Bdev-47c249a-vs-3.13.0rc2.md)
- [📈time plot](bm-20261031-macm4pro-arm64-python-47c249adf3bc2ae3264a-3.16.0a1%2Bdev-47c249a-vs-3.13.0rc2.svg)

