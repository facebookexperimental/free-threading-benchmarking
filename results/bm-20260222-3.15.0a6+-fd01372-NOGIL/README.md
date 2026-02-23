# Results

- fork: python/fd01372d4e509b2cbec7
- version: 3.15.0a6+
- config: NOGIL
- commit hash: [fd01372](https://github.com/python/cpython/commit/fd01372)
- commit date: 2026-02-22T18:46:03Z
- commit merge base: [819ea3ca6836026bc611d0c8ea1cd5e95cbefc09](https://github.com/python/cpython/commit/819ea3ca6836026bc611d0c8ea1cd5e95cbefc09)
- commit date: 2026-02-22T18:46:03+00:00
- ref: fd01372d4e509b2cbec7

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/22288921302)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260222-vultr-x86_64-python-fd01372d4e509b2cbec7-3.15.0a6%2B-fd01372.json)

### vs. 3.12.6

- Geometric mean: 1.031x slower (HPT: reliability of 79.94%, 1.00x slower at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260222-vultr-x86_64-python-fd01372d4e509b2cbec7-3.15.0a6%2B-fd01372-vs-3.12.6.md)
- [📈time plot](bm-20260222-vultr-x86_64-python-fd01372d4e509b2cbec7-3.15.0a6%2B-fd01372-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.063x slower (HPT: reliability of 96.43%, 1.00x slower at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260222-vultr-x86_64-python-fd01372d4e509b2cbec7-3.15.0a6%2B-fd01372-vs-3.13.0rc2.md)
- [📈time plot](bm-20260222-vultr-x86_64-python-fd01372d4e509b2cbec7-3.15.0a6%2B-fd01372-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.107x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20260222-vultr-x86_64-python-fd01372d4e509b2cbec7-3.15.0a6%2B-fd01372-vs-base-mem.svg)
- [📄table](bm-20260222-vultr-x86_64-python-fd01372d4e509b2cbec7-3.15.0a6%2B-fd01372-vs-base.md)
- [📈time plot](bm-20260222-vultr-x86_64-python-fd01372d4e509b2cbec7-3.15.0a6%2B-fd01372-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/22288921302)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260222-macm4pro-arm64-python-fd01372d4e509b2cbec7-3.15.0a6%2B-fd01372.json)

### vs. 3.12.6

- Geometric mean: 1.085x faster (HPT: reliability of 98.36%, 1.00x faster at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260222-macm4pro-arm64-python-fd01372d4e509b2cbec7-3.15.0a6%2B-fd01372-vs-3.12.6.md)
- [📈time plot](bm-20260222-macm4pro-arm64-python-fd01372d4e509b2cbec7-3.15.0a6%2B-fd01372-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.007x faster (HPT: reliability of 70.86%, 1.00x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260222-macm4pro-arm64-python-fd01372d4e509b2cbec7-3.15.0a6%2B-fd01372-vs-3.13.0rc2.md)
- [📈time plot](bm-20260222-macm4pro-arm64-python-fd01372d4e509b2cbec7-3.15.0a6%2B-fd01372-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.065x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20260222-macm4pro-arm64-python-fd01372d4e509b2cbec7-3.15.0a6%2B-fd01372-vs-base-mem.svg)
- [📄table](bm-20260222-macm4pro-arm64-python-fd01372d4e509b2cbec7-3.15.0a6%2B-fd01372-vs-base.md)
- [📈time plot](bm-20260222-macm4pro-arm64-python-fd01372d4e509b2cbec7-3.15.0a6%2B-fd01372-vs-base.svg)

