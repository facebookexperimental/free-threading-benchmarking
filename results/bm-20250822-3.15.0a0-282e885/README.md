# Results

- fork: python/282e88506b1d3c2ea2a0
- version: 3.15.0a0
- config: 
- commit hash: [282e885](https://github.com/python/cpython/commit/282e885)
- commit date: 2025-08-22T16:52:30-07:00
- commit merge base: [90b932e65080008dfd974b2e03c3068dbb72b95d](https://github.com/python/cpython/commit/90b932e65080008dfd974b2e03c3068dbb72b95d)
- ref: 282e88506b1d3c2ea2a0

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17168785768)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250822-vultr-x86_64-python-282e88506b1d3c2ea2a0-3.15.0a0-282e885.json)

### vs. 3.12.6

- Geometric mean: 1.064x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250822-vultr-x86_64-python-282e88506b1d3c2ea2a0-3.15.0a0-282e885-vs-3.12.6.md)
- [📈time plot](bm-20250822-vultr-x86_64-python-282e88506b1d3c2ea2a0-3.15.0a0-282e885-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.029x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250822-vultr-x86_64-python-282e88506b1d3c2ea2a0-3.15.0a0-282e885-vs-3.13.0rc2.md)
- [📈time plot](bm-20250822-vultr-x86_64-python-282e88506b1d3c2ea2a0-3.15.0a0-282e885-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17168785768)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250822-macm4pro-arm64-python-282e88506b1d3c2ea2a0-3.15.0a0-282e885.json)

### vs. 3.12.6

- Geometric mean: 1.100x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250822-macm4pro-arm64-python-282e88506b1d3c2ea2a0-3.15.0a0-282e885-vs-3.12.6.md)
- [📈time plot](bm-20250822-macm4pro-arm64-python-282e88506b1d3c2ea2a0-3.15.0a0-282e885-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.021x faster (HPT: reliability of 89.11%, 1.00x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250822-macm4pro-arm64-python-282e88506b1d3c2ea2a0-3.15.0a0-282e885-vs-3.13.0rc2.md)
- [📈time plot](bm-20250822-macm4pro-arm64-python-282e88506b1d3c2ea2a0-3.15.0a0-282e885-vs-3.13.0rc2.svg)

