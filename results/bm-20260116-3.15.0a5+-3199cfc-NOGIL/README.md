# Results

- fork: python/3199cfcf7661b0c9bd73
- version: 3.15.0a5+
- config: NOGIL
- commit hash: [3199cfc](https://github.com/python/cpython/commit/3199cfc)
- commit date: 2026-01-16T21:40:28+02:00
- commit merge base: [5996636ab5f1f0fd0bac2ff7cce0fbe156168f87](https://github.com/python/cpython/commit/5996636ab5f1f0fd0bac2ff7cce0fbe156168f87)
- ref: 3199cfcf7661b0c9bd73

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21085124994)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260116-vultr-x86_64-python-3199cfcf7661b0c9bd73-3.15.0a5%2B-3199cfc.json)

### vs. 3.12.6

- Geometric mean: 1.028x slower (HPT: reliability of 71.43%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260116-vultr-x86_64-python-3199cfcf7661b0c9bd73-3.15.0a5%2B-3199cfc-vs-3.12.6.md)
- [📈time plot](bm-20260116-vultr-x86_64-python-3199cfcf7661b0c9bd73-3.15.0a5%2B-3199cfc-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.061x slower (HPT: reliability of 90.64%, 1.00x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260116-vultr-x86_64-python-3199cfcf7661b0c9bd73-3.15.0a5%2B-3199cfc-vs-3.13.0rc2.md)
- [📈time plot](bm-20260116-vultr-x86_64-python-3199cfcf7661b0c9bd73-3.15.0a5%2B-3199cfc-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.094x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20260116-vultr-x86_64-python-3199cfcf7661b0c9bd73-3.15.0a5%2B-3199cfc-vs-base-mem.svg)
- [📄table](bm-20260116-vultr-x86_64-python-3199cfcf7661b0c9bd73-3.15.0a5%2B-3199cfc-vs-base.md)
- [📈time plot](bm-20260116-vultr-x86_64-python-3199cfcf7661b0c9bd73-3.15.0a5%2B-3199cfc-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21085124994)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260116-macm4pro-arm64-python-3199cfcf7661b0c9bd73-3.15.0a5%2B-3199cfc.json)

### vs. 3.12.6

- Geometric mean: 1.095x faster (HPT: reliability of 99.66%, 1.00x faster at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260116-macm4pro-arm64-python-3199cfcf7661b0c9bd73-3.15.0a5%2B-3199cfc-vs-3.12.6.md)
- [📈time plot](bm-20260116-macm4pro-arm64-python-3199cfcf7661b0c9bd73-3.15.0a5%2B-3199cfc-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.016x faster (HPT: reliability of 51.04%, 1.00x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260116-macm4pro-arm64-python-3199cfcf7661b0c9bd73-3.15.0a5%2B-3199cfc-vs-3.13.0rc2.md)
- [📈time plot](bm-20260116-macm4pro-arm64-python-3199cfcf7661b0c9bd73-3.15.0a5%2B-3199cfc-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.039x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20260116-macm4pro-arm64-python-3199cfcf7661b0c9bd73-3.15.0a5%2B-3199cfc-vs-base-mem.svg)
- [📄table](bm-20260116-macm4pro-arm64-python-3199cfcf7661b0c9bd73-3.15.0a5%2B-3199cfc-vs-base.md)
- [📈time plot](bm-20260116-macm4pro-arm64-python-3199cfcf7661b0c9bd73-3.15.0a5%2B-3199cfc-vs-base.svg)

