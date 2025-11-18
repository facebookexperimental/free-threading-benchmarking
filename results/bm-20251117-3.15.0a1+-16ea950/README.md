# Results

- fork: python/16ea9505ce690485bab3
- version: 3.15.0a1+
- config: 
- commit hash: [16ea950](https://github.com/python/cpython/commit/16ea950)
- commit date: 2025-11-17T17:52:13-05:00
- commit merge base: [b3626321b6ebb46dd24acee2aa806450e70febfc](https://github.com/python/cpython/commit/b3626321b6ebb46dd24acee2aa806450e70febfc)
- ref: 16ea9505ce690485bab3

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19449413768)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251117-vultr-x86_64-python-16ea9505ce690485bab3-3.15.0a1%2B-16ea950.json)

### vs. 3.12.6

- Geometric mean: 1.078x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251117-vultr-x86_64-python-16ea9505ce690485bab3-3.15.0a1%2B-16ea950-vs-3.12.6.md)
- [📈time plot](bm-20251117-vultr-x86_64-python-16ea9505ce690485bab3-3.15.0a1%2B-16ea950-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.042x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251117-vultr-x86_64-python-16ea9505ce690485bab3-3.15.0a1%2B-16ea950-vs-3.13.0rc2.md)
- [📈time plot](bm-20251117-vultr-x86_64-python-16ea9505ce690485bab3-3.15.0a1%2B-16ea950-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19449413768)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251117-macm4pro-arm64-python-16ea9505ce690485bab3-3.15.0a1%2B-16ea950.json)

### vs. 3.12.6

- Geometric mean: 1.147x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251117-macm4pro-arm64-python-16ea9505ce690485bab3-3.15.0a1%2B-16ea950-vs-3.12.6.md)
- [📈time plot](bm-20251117-macm4pro-arm64-python-16ea9505ce690485bab3-3.15.0a1%2B-16ea950-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.058x faster (HPT: reliability of 99.98%, 1.01x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251117-macm4pro-arm64-python-16ea9505ce690485bab3-3.15.0a1%2B-16ea950-vs-3.13.0rc2.md)
- [📈time plot](bm-20251117-macm4pro-arm64-python-16ea9505ce690485bab3-3.15.0a1%2B-16ea950-vs-3.13.0rc2.svg)

