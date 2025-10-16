# Results

- fork: python/7f371ed84ba471bb1b11
- version: 3.15.0a1+
- config: NOGIL
- commit hash: [7f371ed](https://github.com/python/cpython/commit/7f371ed)
- commit date: 2025-10-16T05:40:39+08:00
- commit merge base: [65d1a14d59a16b441963bad3ca4b4783d37afd1d](https://github.com/python/cpython/commit/65d1a14d59a16b441963bad3ca4b4783d37afd1d)
- ref: 7f371ed84ba471bb1b11

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18546420799)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251016-vultr-x86_64-python-7f371ed84ba471bb1b11-3.15.0a1%2B-7f371ed.json)

### vs. 3.12.6

- Geometric mean: 1.014x slower (HPT: reliability of 78.70%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251016-vultr-x86_64-python-7f371ed84ba471bb1b11-3.15.0a1%2B-7f371ed-vs-3.12.6.md)
- [📈time plot](bm-20251016-vultr-x86_64-python-7f371ed84ba471bb1b11-3.15.0a1%2B-7f371ed-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.048x slower (HPT: reliability of 93.15%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251016-vultr-x86_64-python-7f371ed84ba471bb1b11-3.15.0a1%2B-7f371ed-vs-3.13.0rc2.md)
- [📈time plot](bm-20251016-vultr-x86_64-python-7f371ed84ba471bb1b11-3.15.0a1%2B-7f371ed-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.087x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20251016-vultr-x86_64-python-7f371ed84ba471bb1b11-3.15.0a1%2B-7f371ed-vs-base-mem.svg)
- [📄table](bm-20251016-vultr-x86_64-python-7f371ed84ba471bb1b11-3.15.0a1%2B-7f371ed-vs-base.md)
- [📈time plot](bm-20251016-vultr-x86_64-python-7f371ed84ba471bb1b11-3.15.0a1%2B-7f371ed-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18546420799)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251016-macm4pro-arm64-python-7f371ed84ba471bb1b11-3.15.0a1%2B-7f371ed.json)

### vs. 3.12.6

- Geometric mean: 1.086x faster (HPT: reliability of 96.91%, 1.00x faster at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251016-macm4pro-arm64-python-7f371ed84ba471bb1b11-3.15.0a1%2B-7f371ed-vs-3.12.6.md)
- [📈time plot](bm-20251016-macm4pro-arm64-python-7f371ed84ba471bb1b11-3.15.0a1%2B-7f371ed-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.008x faster (HPT: reliability of 64.61%, 1.00x slower at 99th %ile)
- Memory usage: 1.30x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251016-macm4pro-arm64-python-7f371ed84ba471bb1b11-3.15.0a1%2B-7f371ed-vs-3.13.0rc2.md)
- [📈time plot](bm-20251016-macm4pro-arm64-python-7f371ed84ba471bb1b11-3.15.0a1%2B-7f371ed-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.033x slower (HPT: reliability of 99.53%, 1.00x slower at 99th %ile)
- Memory usage: 1.14x
- [🧠memory plot](bm-20251016-macm4pro-arm64-python-7f371ed84ba471bb1b11-3.15.0a1%2B-7f371ed-vs-base-mem.svg)
- [📄table](bm-20251016-macm4pro-arm64-python-7f371ed84ba471bb1b11-3.15.0a1%2B-7f371ed-vs-base.md)
- [📈time plot](bm-20251016-macm4pro-arm64-python-7f371ed84ba471bb1b11-3.15.0a1%2B-7f371ed-vs-base.svg)

