# Results

- fork: python/eb21dea301df801352ac
- version: 3.16.0a2+dev
- config: NOGIL
- commit hash: [eb21dea](https://github.com/python/cpython/commit/eb21dea)
- commit date: 2026-11-12T00:22:10Z
- commit merge base: [f112215dd7ef054655093e880384dbaed0fbfc66](https://github.com/python/cpython/commit/f112215dd7ef054655093e880384dbaed0fbfc66)
- commit date: 2026-11-12T00:22:10+00:00
- ref: eb21dea301df801352ac

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/43127196262)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261112-vultr-x86_64-python-eb21dea301df801352ac-3.16.0a2%2Bdev-eb21dea.json)

### vs. 3.12.6

- Geometric mean: 1.025x slower (HPT: reliability of 58.19%, 1.00x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261112-vultr-x86_64-python-eb21dea301df801352ac-3.16.0a2%2Bdev-eb21dea-vs-3.12.6.md)
- [📈time plot](bm-20261112-vultr-x86_64-python-eb21dea301df801352ac-3.16.0a2%2Bdev-eb21dea-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.058x slower (HPT: reliability of 86.07%, 1.00x slower at 99th %ile)
- Memory usage: 1.30x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261112-vultr-x86_64-python-eb21dea301df801352ac-3.16.0a2%2Bdev-eb21dea-vs-3.13.0rc2.md)
- [📈time plot](bm-20261112-vultr-x86_64-python-eb21dea301df801352ac-3.16.0a2%2Bdev-eb21dea-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.107x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.14x
- [🧠memory plot](bm-20261112-vultr-x86_64-python-eb21dea301df801352ac-3.16.0a2%2Bdev-eb21dea-vs-base-mem.svg)
- [📄table](bm-20261112-vultr-x86_64-python-eb21dea301df801352ac-3.16.0a2%2Bdev-eb21dea-vs-base.md)
- [📈time plot](bm-20261112-vultr-x86_64-python-eb21dea301df801352ac-3.16.0a2%2Bdev-eb21dea-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/43127196262)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261112-macm4pro-arm64-python-eb21dea301df801352ac-3.16.0a2%2Bdev-eb21dea.json)

### vs. 3.12.6

- Geometric mean: 1.063x faster (HPT: reliability of 89.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261112-macm4pro-arm64-python-eb21dea301df801352ac-3.16.0a2%2Bdev-eb21dea-vs-3.12.6.md)
- [📈time plot](bm-20261112-macm4pro-arm64-python-eb21dea301df801352ac-3.16.0a2%2Bdev-eb21dea-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.016x slower (HPT: reliability of 94.35%, 1.00x slower at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261112-macm4pro-arm64-python-eb21dea301df801352ac-3.16.0a2%2Bdev-eb21dea-vs-3.13.0rc2.md)
- [📈time plot](bm-20261112-macm4pro-arm64-python-eb21dea301df801352ac-3.16.0a2%2Bdev-eb21dea-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.106x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.08x
- new benchmarks: coverage
- [🧠memory plot](bm-20261112-macm4pro-arm64-python-eb21dea301df801352ac-3.16.0a2%2Bdev-eb21dea-vs-base-mem.svg)
- [📄table](bm-20261112-macm4pro-arm64-python-eb21dea301df801352ac-3.16.0a2%2Bdev-eb21dea-vs-base.md)
- [📈time plot](bm-20261112-macm4pro-arm64-python-eb21dea301df801352ac-3.16.0a2%2Bdev-eb21dea-vs-base.svg)

