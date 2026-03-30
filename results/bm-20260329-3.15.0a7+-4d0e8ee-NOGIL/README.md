# Results

- fork: python/4d0e8ee649ceff96b130
- version: 3.15.0a7+
- config: NOGIL
- commit hash: [4d0e8ee](https://github.com/python/cpython/commit/4d0e8ee)
- commit date: 2026-03-29T12:58:12-07:00
- commit merge base: [e39d84a37dfc8bcdc0eb4d6f3ce7d5ee829d7f30](https://github.com/python/cpython/commit/e39d84a37dfc8bcdc0eb4d6f3ce7d5ee829d7f30)
- ref: 4d0e8ee649ceff96b130

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/23723110852)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260329-vultr-x86_64-python-4d0e8ee649ceff96b130-3.15.0a7%2B-4d0e8ee.json)

### vs. 3.12.6

- Geometric mean: 1.029x slower (HPT: reliability of 73.51%, 1.00x slower at 99th %ile)
- Memory usage: 1.44x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260329-vultr-x86_64-python-4d0e8ee649ceff96b130-3.15.0a7%2B-4d0e8ee-vs-3.12.6.md)
- [📈time plot](bm-20260329-vultr-x86_64-python-4d0e8ee649ceff96b130-3.15.0a7%2B-4d0e8ee-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.062x slower (HPT: reliability of 91.79%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260329-vultr-x86_64-python-4d0e8ee649ceff96b130-3.15.0a7%2B-4d0e8ee-vs-3.13.0rc2.md)
- [📈time plot](bm-20260329-vultr-x86_64-python-4d0e8ee649ceff96b130-3.15.0a7%2B-4d0e8ee-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.104x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20260329-vultr-x86_64-python-4d0e8ee649ceff96b130-3.15.0a7%2B-4d0e8ee-vs-base-mem.svg)
- [📄table](bm-20260329-vultr-x86_64-python-4d0e8ee649ceff96b130-3.15.0a7%2B-4d0e8ee-vs-base.md)
- [📈time plot](bm-20260329-vultr-x86_64-python-4d0e8ee649ceff96b130-3.15.0a7%2B-4d0e8ee-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/23723110852)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7%2B-4d0e8ee.json)

### vs. 3.12.6

- Geometric mean: 1.108x faster (HPT: reliability of 99.96%, 1.01x faster at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7%2B-4d0e8ee-vs-3.12.6.md)
- [📈time plot](bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7%2B-4d0e8ee-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.028x faster (HPT: reliability of 62.10%, 1.00x faster at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7%2B-4d0e8ee-vs-3.13.0rc2.md)
- [📈time plot](bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7%2B-4d0e8ee-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.045x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7%2B-4d0e8ee-vs-base-mem.svg)
- [📄table](bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7%2B-4d0e8ee-vs-base.md)
- [📈time plot](bm-20260329-macm4pro-arm64-python-4d0e8ee649ceff96b130-3.15.0a7%2B-4d0e8ee-vs-base.svg)

