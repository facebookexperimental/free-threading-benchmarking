# Results

- fork: DinoV/501ce683eb76f21d5fdc
- version: 3.16.0a1+dev
- config: NOGIL
- commit hash: [501ce68](https://github.com/DinoV/cpython/commit/501ce68)
- commit date: 2026-10-23T10:54:05-07:00
- commit merge base: [0615b5c0d9ee3854bc50fe2bcc68e6799cead14a](https://github.com/python/cpython/commit/0615b5c0d9ee3854bc50fe2bcc68e6799cead14a)
- ref: 501ce683eb76f21d5fdc

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/40000440133)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261023-vultr-x86_64-DinoV-501ce683eb76f21d5fdc-3.16.0a1%2Bdev-501ce68.json)

### vs. 3.12.6

- Geometric mean: 1.053x slower (HPT: reliability of 85.96%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261023-vultr-x86_64-DinoV-501ce683eb76f21d5fdc-3.16.0a1%2Bdev-501ce68-vs-3.12.6.md)
- [📈time plot](bm-20261023-vultr-x86_64-DinoV-501ce683eb76f21d5fdc-3.16.0a1%2Bdev-501ce68-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.086x slower (HPT: reliability of 99.33%, 1.00x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261023-vultr-x86_64-DinoV-501ce683eb76f21d5fdc-3.16.0a1%2Bdev-501ce68-vs-3.13.0rc2.md)
- [📈time plot](bm-20261023-vultr-x86_64-DinoV-501ce683eb76f21d5fdc-3.16.0a1%2Bdev-501ce68-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.016x slower (HPT: reliability of 100.00%, 1.00x slower at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20261023-vultr-x86_64-DinoV-501ce683eb76f21d5fdc-3.16.0a1%2Bdev-501ce68-vs-base-mem.svg)
- [📄table](bm-20261023-vultr-x86_64-DinoV-501ce683eb76f21d5fdc-3.16.0a1%2Bdev-501ce68-vs-base.md)
- [📈time plot](bm-20261023-vultr-x86_64-DinoV-501ce683eb76f21d5fdc-3.16.0a1%2Bdev-501ce68-vs-base.svg)

