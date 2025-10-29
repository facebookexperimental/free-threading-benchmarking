# Results

- fork: python/ce4b0ede16aea62ee7b1
- version: 3.15.0a1+
- config: NOGIL
- commit hash: [ce4b0ed](https://github.com/python/cpython/commit/ce4b0ed)
- commit date: 2025-10-28T19:56:23Z
- commit merge base: [c6d4c79c9abac5c5cc2e7b429d72946d15c5e132](https://github.com/python/cpython/commit/c6d4c79c9abac5c5cc2e7b429d72946d15c5e132)
- commit date: 2025-10-28T19:56:23+00:00
- ref: ce4b0ede16aea62ee7b1

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18893203484)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251028-vultr-x86_64-python-ce4b0ede16aea62ee7b1-3.15.0a1%2B-ce4b0ed.json)

### vs. 3.12.6

- Geometric mean: 1.018x slower (HPT: reliability of 81.00%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251028-vultr-x86_64-python-ce4b0ede16aea62ee7b1-3.15.0a1%2B-ce4b0ed-vs-3.12.6.md)
- [📈time plot](bm-20251028-vultr-x86_64-python-ce4b0ede16aea62ee7b1-3.15.0a1%2B-ce4b0ed-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.051x slower (HPT: reliability of 97.65%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251028-vultr-x86_64-python-ce4b0ede16aea62ee7b1-3.15.0a1%2B-ce4b0ed-vs-3.13.0rc2.md)
- [📈time plot](bm-20251028-vultr-x86_64-python-ce4b0ede16aea62ee7b1-3.15.0a1%2B-ce4b0ed-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.094x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20251028-vultr-x86_64-python-ce4b0ede16aea62ee7b1-3.15.0a1%2B-ce4b0ed-vs-base-mem.svg)
- [📄table](bm-20251028-vultr-x86_64-python-ce4b0ede16aea62ee7b1-3.15.0a1%2B-ce4b0ed-vs-base.md)
- [📈time plot](bm-20251028-vultr-x86_64-python-ce4b0ede16aea62ee7b1-3.15.0a1%2B-ce4b0ed-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18893203484)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251028-macm4pro-arm64-python-ce4b0ede16aea62ee7b1-3.15.0a1%2B-ce4b0ed.json)

### vs. 3.12.6

- Geometric mean: 1.074x faster (HPT: reliability of 93.36%, 1.00x faster at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251028-macm4pro-arm64-python-ce4b0ede16aea62ee7b1-3.15.0a1%2B-ce4b0ed-vs-3.12.6.md)
- [📈time plot](bm-20251028-macm4pro-arm64-python-ce4b0ede16aea62ee7b1-3.15.0a1%2B-ce4b0ed-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.004x slower (HPT: reliability of 76.31%, 1.00x slower at 99th %ile)
- Memory usage: 1.29x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251028-macm4pro-arm64-python-ce4b0ede16aea62ee7b1-3.15.0a1%2B-ce4b0ed-vs-3.13.0rc2.md)
- [📈time plot](bm-20251028-macm4pro-arm64-python-ce4b0ede16aea62ee7b1-3.15.0a1%2B-ce4b0ed-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.032x slower (HPT: reliability of 99.95%, 1.01x slower at 99th %ile)
- Memory usage: 1.13x
- [🧠memory plot](bm-20251028-macm4pro-arm64-python-ce4b0ede16aea62ee7b1-3.15.0a1%2B-ce4b0ed-vs-base-mem.svg)
- [📄table](bm-20251028-macm4pro-arm64-python-ce4b0ede16aea62ee7b1-3.15.0a1%2B-ce4b0ed-vs-base.md)
- [📈time plot](bm-20251028-macm4pro-arm64-python-ce4b0ede16aea62ee7b1-3.15.0a1%2B-ce4b0ed-vs-base.svg)

