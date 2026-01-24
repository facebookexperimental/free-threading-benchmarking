# Results

- fork: python/58ccf21cbb92e0e99cbe
- version: 3.15.0a5+
- config: NOGIL
- commit hash: [58ccf21](https://github.com/python/cpython/commit/58ccf21)
- commit date: 2026-01-23T15:07:27-06:00
- commit merge base: [25a10b60b04ab2fa802409dc6f211cf2ca028a0a](https://github.com/python/cpython/commit/25a10b60b04ab2fa802409dc6f211cf2ca028a0a)
- ref: 58ccf21cbb92e0e99cbe

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21305809365)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260123-vultr-x86_64-python-58ccf21cbb92e0e99cbe-3.15.0a5%2B-58ccf21.json)

### vs. 3.12.6

- Geometric mean: 1.029x slower (HPT: reliability of 69.27%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260123-vultr-x86_64-python-58ccf21cbb92e0e99cbe-3.15.0a5%2B-58ccf21-vs-3.12.6.md)
- [📈time plot](bm-20260123-vultr-x86_64-python-58ccf21cbb92e0e99cbe-3.15.0a5%2B-58ccf21-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.062x slower (HPT: reliability of 94.65%, 1.00x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260123-vultr-x86_64-python-58ccf21cbb92e0e99cbe-3.15.0a5%2B-58ccf21-vs-3.13.0rc2.md)
- [📈time plot](bm-20260123-vultr-x86_64-python-58ccf21cbb92e0e99cbe-3.15.0a5%2B-58ccf21-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.105x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20260123-vultr-x86_64-python-58ccf21cbb92e0e99cbe-3.15.0a5%2B-58ccf21-vs-base-mem.svg)
- [📄table](bm-20260123-vultr-x86_64-python-58ccf21cbb92e0e99cbe-3.15.0a5%2B-58ccf21-vs-base.md)
- [📈time plot](bm-20260123-vultr-x86_64-python-58ccf21cbb92e0e99cbe-3.15.0a5%2B-58ccf21-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21305809365)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260123-macm4pro-arm64-python-58ccf21cbb92e0e99cbe-3.15.0a5%2B-58ccf21.json)

### vs. 3.12.6

- Geometric mean: 1.108x faster (HPT: reliability of 99.95%, 1.01x faster at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260123-macm4pro-arm64-python-58ccf21cbb92e0e99cbe-3.15.0a5%2B-58ccf21-vs-3.12.6.md)
- [📈time plot](bm-20260123-macm4pro-arm64-python-58ccf21cbb92e0e99cbe-3.15.0a5%2B-58ccf21-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.028x faster (HPT: reliability of 70.22%, 1.00x faster at 99th %ile)
- Memory usage: 1.30x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260123-macm4pro-arm64-python-58ccf21cbb92e0e99cbe-3.15.0a5%2B-58ccf21-vs-3.13.0rc2.md)
- [📈time plot](bm-20260123-macm4pro-arm64-python-58ccf21cbb92e0e99cbe-3.15.0a5%2B-58ccf21-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.058x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.11x
- [🧠memory plot](bm-20260123-macm4pro-arm64-python-58ccf21cbb92e0e99cbe-3.15.0a5%2B-58ccf21-vs-base-mem.svg)
- [📄table](bm-20260123-macm4pro-arm64-python-58ccf21cbb92e0e99cbe-3.15.0a5%2B-58ccf21-vs-base.md)
- [📈time plot](bm-20260123-macm4pro-arm64-python-58ccf21cbb92e0e99cbe-3.15.0a5%2B-58ccf21-vs-base.svg)

