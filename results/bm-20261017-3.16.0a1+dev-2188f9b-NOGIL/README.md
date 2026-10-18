# Results

- fork: python/2188f9b60abb7965548b
- version: 3.16.0a1+dev
- config: NOGIL
- commit hash: [2188f9b](https://github.com/python/cpython/commit/2188f9b)
- commit date: 2026-10-17T23:07:03Z
- commit merge base: [0fedf7852c24727b5a9fa7f2014c18cbaa50cdb9](https://github.com/python/cpython/commit/0fedf7852c24727b5a9fa7f2014c18cbaa50cdb9)
- commit date: 2026-10-17T23:07:03+00:00
- ref: 2188f9b60abb7965548b

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/39082386553)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261017-vultr-x86_64-python-2188f9b60abb7965548b-3.16.0a1%2Bdev-2188f9b.json)

### vs. 3.12.6

- Geometric mean: 1.037x slower (HPT: reliability of 74.54%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261017-vultr-x86_64-python-2188f9b60abb7965548b-3.16.0a1%2Bdev-2188f9b-vs-3.12.6.md)
- [📈time plot](bm-20261017-vultr-x86_64-python-2188f9b60abb7965548b-3.16.0a1%2Bdev-2188f9b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.070x slower (HPT: reliability of 94.48%, 1.00x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261017-vultr-x86_64-python-2188f9b60abb7965548b-3.16.0a1%2Bdev-2188f9b-vs-3.13.0rc2.md)
- [📈time plot](bm-20261017-vultr-x86_64-python-2188f9b60abb7965548b-3.16.0a1%2Bdev-2188f9b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.110x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.17x
- [🧠memory plot](bm-20261017-vultr-x86_64-python-2188f9b60abb7965548b-3.16.0a1%2Bdev-2188f9b-vs-base-mem.svg)
- [📄table](bm-20261017-vultr-x86_64-python-2188f9b60abb7965548b-3.16.0a1%2Bdev-2188f9b-vs-base.md)
- [📈time plot](bm-20261017-vultr-x86_64-python-2188f9b60abb7965548b-3.16.0a1%2Bdev-2188f9b-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/39082386553)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261017-macm4pro-arm64-python-2188f9b60abb7965548b-3.16.0a1%2Bdev-2188f9b.json)

### vs. 3.12.6

- Geometric mean: 1.070x faster (HPT: reliability of 94.94%, 1.00x faster at 99th %ile)
- Memory usage: 1.29x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20261017-macm4pro-arm64-python-2188f9b60abb7965548b-3.16.0a1%2Bdev-2188f9b-vs-3.12.6.md)
- [📈time plot](bm-20261017-macm4pro-arm64-python-2188f9b60abb7965548b-3.16.0a1%2Bdev-2188f9b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.009x slower (HPT: reliability of 83.29%, 1.00x slower at 99th %ile)
- Memory usage: 1.25x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20261017-macm4pro-arm64-python-2188f9b60abb7965548b-3.16.0a1%2Bdev-2188f9b-vs-3.13.0rc2.md)
- [📈time plot](bm-20261017-macm4pro-arm64-python-2188f9b60abb7965548b-3.16.0a1%2Bdev-2188f9b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.098x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.12x
- new benchmarks: coverage
- [🧠memory plot](bm-20261017-macm4pro-arm64-python-2188f9b60abb7965548b-3.16.0a1%2Bdev-2188f9b-vs-base-mem.svg)
- [📄table](bm-20261017-macm4pro-arm64-python-2188f9b60abb7965548b-3.16.0a1%2Bdev-2188f9b-vs-base.md)
- [📈time plot](bm-20261017-macm4pro-arm64-python-2188f9b60abb7965548b-3.16.0a1%2Bdev-2188f9b-vs-base.svg)

