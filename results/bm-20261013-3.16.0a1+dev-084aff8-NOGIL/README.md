# Results

- fork: python/084aff869c4aa2f2cbdf
- version: 3.16.0a1+dev
- config: NOGIL
- commit hash: [084aff8](https://github.com/python/cpython/commit/084aff8)
- commit date: 2026-10-13T23:53:38Z
- commit merge base: [8138bf11a5d32e8db003a86606be8e4c61e14d4b](https://github.com/python/cpython/commit/8138bf11a5d32e8db003a86606be8e4c61e14d4b)
- commit date: 2026-10-13T23:53:38+00:00
- ref: 084aff869c4aa2f2cbdf

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/38491168522)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261013-vultr-x86_64-python-084aff869c4aa2f2cbdf-3.16.0a1%2Bdev-084aff8.json)

### vs. 3.12.6

- Geometric mean: 1.044x slower (HPT: reliability of 84.46%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261013-vultr-x86_64-python-084aff869c4aa2f2cbdf-3.16.0a1%2Bdev-084aff8-vs-3.12.6.md)
- [📈time plot](bm-20261013-vultr-x86_64-python-084aff869c4aa2f2cbdf-3.16.0a1%2Bdev-084aff8-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.077x slower (HPT: reliability of 98.50%, 1.00x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261013-vultr-x86_64-python-084aff869c4aa2f2cbdf-3.16.0a1%2Bdev-084aff8-vs-3.13.0rc2.md)
- [📈time plot](bm-20261013-vultr-x86_64-python-084aff869c4aa2f2cbdf-3.16.0a1%2Bdev-084aff8-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.119x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20261013-vultr-x86_64-python-084aff869c4aa2f2cbdf-3.16.0a1%2Bdev-084aff8-vs-base-mem.svg)
- [📄table](bm-20261013-vultr-x86_64-python-084aff869c4aa2f2cbdf-3.16.0a1%2Bdev-084aff8-vs-base.md)
- [📈time plot](bm-20261013-vultr-x86_64-python-084aff869c4aa2f2cbdf-3.16.0a1%2Bdev-084aff8-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/38491168522)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261013-macm4pro-arm64-python-084aff869c4aa2f2cbdf-3.16.0a1%2Bdev-084aff8.json)

### vs. 3.12.6

- Geometric mean: 1.063x faster (HPT: reliability of 90.26%, 1.00x faster at 99th %ile)
- Memory usage: 1.29x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261013-macm4pro-arm64-python-084aff869c4aa2f2cbdf-3.16.0a1%2Bdev-084aff8-vs-3.12.6.md)
- [📈time plot](bm-20261013-macm4pro-arm64-python-084aff869c4aa2f2cbdf-3.16.0a1%2Bdev-084aff8-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.015x slower (HPT: reliability of 89.29%, 1.00x slower at 99th %ile)
- Memory usage: 1.25x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261013-macm4pro-arm64-python-084aff869c4aa2f2cbdf-3.16.0a1%2Bdev-084aff8-vs-3.13.0rc2.md)
- [📈time plot](bm-20261013-macm4pro-arm64-python-084aff869c4aa2f2cbdf-3.16.0a1%2Bdev-084aff8-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.098x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.12x
- new benchmarks: coverage
- [🧠memory plot](bm-20261013-macm4pro-arm64-python-084aff869c4aa2f2cbdf-3.16.0a1%2Bdev-084aff8-vs-base-mem.svg)
- [📄table](bm-20261013-macm4pro-arm64-python-084aff869c4aa2f2cbdf-3.16.0a1%2Bdev-084aff8-vs-base.md)
- [📈time plot](bm-20261013-macm4pro-arm64-python-084aff869c4aa2f2cbdf-3.16.0a1%2Bdev-084aff8-vs-base.svg)

