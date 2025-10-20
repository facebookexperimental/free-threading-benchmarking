# Results

- fork: python/ed672f7a8a3c843d8e6e
- version: 3.15.0a1+
- config: 
- commit hash: [ed672f7](https://github.com/python/cpython/commit/ed672f7)
- commit date: 2025-10-19T16:16:35-04:00
- commit merge base: [f9323213c98c9f1f7f3bf5af883b73047432fe50](https://github.com/python/cpython/commit/f9323213c98c9f1f7f3bf5af883b73047432fe50)
- ref: ed672f7a8a3c843d8e6e

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18638404683)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251019-vultr-x86_64-python-ed672f7a8a3c843d8e6e-3.15.0a1%2B-ed672f7.json)

### vs. 3.12.6

- Geometric mean: 1.065x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251019-vultr-x86_64-python-ed672f7a8a3c843d8e6e-3.15.0a1%2B-ed672f7-vs-3.12.6.md)
- [📈time plot](bm-20251019-vultr-x86_64-python-ed672f7a8a3c843d8e6e-3.15.0a1%2B-ed672f7-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.029x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251019-vultr-x86_64-python-ed672f7a8a3c843d8e6e-3.15.0a1%2B-ed672f7-vs-3.13.0rc2.md)
- [📈time plot](bm-20251019-vultr-x86_64-python-ed672f7a8a3c843d8e6e-3.15.0a1%2B-ed672f7-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18638404683)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251019-macm4pro-arm64-python-ed672f7a8a3c843d8e6e-3.15.0a1%2B-ed672f7.json)

### vs. 3.12.6

- Geometric mean: 1.083x faster (HPT: reliability of 99.99%, 1.02x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251019-macm4pro-arm64-python-ed672f7a8a3c843d8e6e-3.15.0a1%2B-ed672f7-vs-3.12.6.md)
- [📈time plot](bm-20251019-macm4pro-arm64-python-ed672f7a8a3c843d8e6e-3.15.0a1%2B-ed672f7-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.004x faster (HPT: reliability of 53.84%, 1.00x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251019-macm4pro-arm64-python-ed672f7a8a3c843d8e6e-3.15.0a1%2B-ed672f7-vs-3.13.0rc2.md)
- [📈time plot](bm-20251019-macm4pro-arm64-python-ed672f7a8a3c843d8e6e-3.15.0a1%2B-ed672f7-vs-3.13.0rc2.svg)

