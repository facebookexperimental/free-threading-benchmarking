# Results

- fork: python/eb21dea301df801352ac
- version: 3.16.0a2+dev
- config: 
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

- Geometric mean: 1.087x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261112-vultr-x86_64-python-eb21dea301df801352ac-3.16.0a2%2Bdev-eb21dea-vs-3.12.6.md)
- [📈time plot](bm-20261112-vultr-x86_64-python-eb21dea301df801352ac-3.16.0a2%2Bdev-eb21dea-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.051x faster (HPT: reliability of 99.85%, 1.00x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261112-vultr-x86_64-python-eb21dea301df801352ac-3.16.0a2%2Bdev-eb21dea-vs-3.13.0rc2.md)
- [📈time plot](bm-20261112-vultr-x86_64-python-eb21dea301df801352ac-3.16.0a2%2Bdev-eb21dea-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/43127196262)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261112-macm4pro-arm64-python-eb21dea301df801352ac-3.16.0a2%2Bdev-eb21dea.json)

### vs. 3.12.6

- Geometric mean: 1.194x faster (HPT: reliability of 100.00%, 1.10x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261112-macm4pro-arm64-python-eb21dea301df801352ac-3.16.0a2%2Bdev-eb21dea-vs-3.12.6.md)
- [📈time plot](bm-20261112-macm4pro-arm64-python-eb21dea301df801352ac-3.16.0a2%2Bdev-eb21dea-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.103x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261112-macm4pro-arm64-python-eb21dea301df801352ac-3.16.0a2%2Bdev-eb21dea-vs-3.13.0rc2.md)
- [📈time plot](bm-20261112-macm4pro-arm64-python-eb21dea301df801352ac-3.16.0a2%2Bdev-eb21dea-vs-3.13.0rc2.svg)

