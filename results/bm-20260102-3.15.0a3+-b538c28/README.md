# Results

- fork: python/b538c2832d582a428a6f
- version: 3.15.0a3+
- config: 
- commit hash: [b538c28](https://github.com/python/cpython/commit/b538c28)
- commit date: 2026-01-02T20:43:00Z
- commit merge base: [136f6d835588e0f72cecdff855afc8f424381ed5](https://github.com/python/cpython/commit/136f6d835588e0f72cecdff855afc8f424381ed5)
- commit date: 2026-01-02T20:43:00+00:00
- ref: b538c2832d582a428a6f

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20669556183)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260102-vultr-x86_64-python-b538c2832d582a428a6f-3.15.0a3%2B-b538c28.json)

### vs. 3.12.6

- Geometric mean: 1.074x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260102-vultr-x86_64-python-b538c2832d582a428a6f-3.15.0a3%2B-b538c28-vs-3.12.6.md)
- [📈time plot](bm-20260102-vultr-x86_64-python-b538c2832d582a428a6f-3.15.0a3%2B-b538c28-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.038x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260102-vultr-x86_64-python-b538c2832d582a428a6f-3.15.0a3%2B-b538c28-vs-3.13.0rc2.md)
- [📈time plot](bm-20260102-vultr-x86_64-python-b538c2832d582a428a6f-3.15.0a3%2B-b538c28-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20669556183)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260102-macm4pro-arm64-python-b538c2832d582a428a6f-3.15.0a3%2B-b538c28.json)

### vs. 3.12.6

- Geometric mean: 1.162x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: asyncio_websockets, chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260102-macm4pro-arm64-python-b538c2832d582a428a6f-3.15.0a3%2B-b538c28-vs-3.12.6.md)
- [📈time plot](bm-20260102-macm4pro-arm64-python-b538c2832d582a428a6f-3.15.0a3%2B-b538c28-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.076x faster (HPT: reliability of 99.99%, 1.01x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: asyncio_websockets, chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260102-macm4pro-arm64-python-b538c2832d582a428a6f-3.15.0a3%2B-b538c28-vs-3.13.0rc2.md)
- [📈time plot](bm-20260102-macm4pro-arm64-python-b538c2832d582a428a6f-3.15.0a3%2B-b538c28-vs-3.13.0rc2.svg)

