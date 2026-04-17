# Results

- fork: python/2a07ff980b412559f6ce
- version: 3.15.0a8+
- config: NOGIL
- commit hash: [2a07ff9](https://github.com/python/cpython/commit/2a07ff9)
- commit date: 2026-04-17T01:55:03+02:00
- commit merge base: [2faceeec5c0fb06498a9654d429180ac4610c65a](https://github.com/python/cpython/commit/2faceeec5c0fb06498a9654d429180ac4610c65a)
- ref: 2a07ff980b412559f6ce

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/24541811935)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260417-vultr-x86_64-python-2a07ff980b412559f6ce-3.15.0a8%2B-2a07ff9.json)

### vs. 3.12.6

- Geometric mean: 1.011x slower (HPT: reliability of 56.85%, 1.00x slower at 99th %ile)
- Memory usage: 1.44x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260417-vultr-x86_64-python-2a07ff980b412559f6ce-3.15.0a8%2B-2a07ff9-vs-3.12.6.md)
- [📈time plot](bm-20260417-vultr-x86_64-python-2a07ff980b412559f6ce-3.15.0a8%2B-2a07ff9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.044x slower (HPT: reliability of 85.97%, 1.00x slower at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260417-vultr-x86_64-python-2a07ff980b412559f6ce-3.15.0a8%2B-2a07ff9-vs-3.13.0rc2.md)
- [📈time plot](bm-20260417-vultr-x86_64-python-2a07ff980b412559f6ce-3.15.0a8%2B-2a07ff9-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.091x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20260417-vultr-x86_64-python-2a07ff980b412559f6ce-3.15.0a8%2B-2a07ff9-vs-base-mem.svg)
- [📄table](bm-20260417-vultr-x86_64-python-2a07ff980b412559f6ce-3.15.0a8%2B-2a07ff9-vs-base.md)
- [📈time plot](bm-20260417-vultr-x86_64-python-2a07ff980b412559f6ce-3.15.0a8%2B-2a07ff9-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/24541811935)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260417-macm4pro-arm64-python-2a07ff980b412559f6ce-3.15.0a8%2B-2a07ff9.json)

### vs. 3.12.6

- Geometric mean: 1.106x faster (HPT: reliability of 99.83%, 1.01x faster at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260417-macm4pro-arm64-python-2a07ff980b412559f6ce-3.15.0a8%2B-2a07ff9-vs-3.12.6.md)
- [📈time plot](bm-20260417-macm4pro-arm64-python-2a07ff980b412559f6ce-3.15.0a8%2B-2a07ff9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.026x faster (HPT: reliability of 66.12%, 1.00x faster at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260417-macm4pro-arm64-python-2a07ff980b412559f6ce-3.15.0a8%2B-2a07ff9-vs-3.13.0rc2.md)
- [📈time plot](bm-20260417-macm4pro-arm64-python-2a07ff980b412559f6ce-3.15.0a8%2B-2a07ff9-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.028x slower (HPT: reliability of 100.00%, 1.02x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20260417-macm4pro-arm64-python-2a07ff980b412559f6ce-3.15.0a8%2B-2a07ff9-vs-base-mem.svg)
- [📄table](bm-20260417-macm4pro-arm64-python-2a07ff980b412559f6ce-3.15.0a8%2B-2a07ff9-vs-base.md)
- [📈time plot](bm-20260417-macm4pro-arm64-python-2a07ff980b412559f6ce-3.15.0a8%2B-2a07ff9-vs-base.svg)

