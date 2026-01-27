# Results

- fork: python/25206173619f5f387c88
- version: 3.15.0a5+
- config: 
- commit hash: [2520617](https://github.com/python/cpython/commit/2520617)
- commit date: 2026-01-26T21:15:21Z
- commit merge base: [7febbe6b600e63544d5e7000cf377eeead858a39](https://github.com/python/cpython/commit/7febbe6b600e63544d5e7000cf377eeead858a39)
- commit date: 2026-01-26T21:15:21+00:00
- ref: 25206173619f5f387c88

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21379642857)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260126-vultr-x86_64-python-25206173619f5f387c88-3.15.0a5%2B-2520617.json)

### vs. 3.12.6

- Geometric mean: 1.083x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260126-vultr-x86_64-python-25206173619f5f387c88-3.15.0a5%2B-2520617-vs-3.12.6.md)
- [📈time plot](bm-20260126-vultr-x86_64-python-25206173619f5f387c88-3.15.0a5%2B-2520617-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.047x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260126-vultr-x86_64-python-25206173619f5f387c88-3.15.0a5%2B-2520617-vs-3.13.0rc2.md)
- [📈time plot](bm-20260126-vultr-x86_64-python-25206173619f5f387c88-3.15.0a5%2B-2520617-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21379642857)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260126-macm4pro-arm64-python-25206173619f5f387c88-3.15.0a5%2B-2520617.json)

### vs. 3.12.6

- Geometric mean: 1.198x faster (HPT: reliability of 100.00%, 1.10x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260126-macm4pro-arm64-python-25206173619f5f387c88-3.15.0a5%2B-2520617-vs-3.12.6.md)
- [📈time plot](bm-20260126-macm4pro-arm64-python-25206173619f5f387c88-3.15.0a5%2B-2520617-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.111x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260126-macm4pro-arm64-python-25206173619f5f387c88-3.15.0a5%2B-2520617-vs-3.13.0rc2.md)
- [📈time plot](bm-20260126-macm4pro-arm64-python-25206173619f5f387c88-3.15.0a5%2B-2520617-vs-3.13.0rc2.svg)

