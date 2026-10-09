# Results

- fork: python/bc12b7285f87f3ca9118
- version: 3.16.0a0
- config: NOGIL
- commit hash: [bc12b72](https://github.com/python/cpython/commit/bc12b72)
- commit date: 2026-10-08T16:45:03-07:00
- commit merge base: [560738126e42208e71fa372c2826f9ccda3e4068](https://github.com/python/cpython/commit/560738126e42208e71fa372c2826f9ccda3e4068)
- ref: bc12b7285f87f3ca9118

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/37866521822)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261008-vultr-x86_64-python-bc12b7285f87f3ca9118-3.16.0a0-bc12b72.json)

### vs. 3.12.6

- Geometric mean: 1.038x slower (HPT: reliability of 70.21%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261008-vultr-x86_64-python-bc12b7285f87f3ca9118-3.16.0a0-bc12b72-vs-3.12.6.md)
- [📈time plot](bm-20261008-vultr-x86_64-python-bc12b7285f87f3ca9118-3.16.0a0-bc12b72-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.071x slower (HPT: reliability of 94.31%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261008-vultr-x86_64-python-bc12b7285f87f3ca9118-3.16.0a0-bc12b72-vs-3.13.0rc2.md)
- [📈time plot](bm-20261008-vultr-x86_64-python-bc12b7285f87f3ca9118-3.16.0a0-bc12b72-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.101x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20261008-vultr-x86_64-python-bc12b7285f87f3ca9118-3.16.0a0-bc12b72-vs-base-mem.svg)
- [📄table](bm-20261008-vultr-x86_64-python-bc12b7285f87f3ca9118-3.16.0a0-bc12b72-vs-base.md)
- [📈time plot](bm-20261008-vultr-x86_64-python-bc12b7285f87f3ca9118-3.16.0a0-bc12b72-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/37866521822)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261008-macm4pro-arm64-python-bc12b7285f87f3ca9118-3.16.0a0-bc12b72.json)

### vs. 3.12.6

- Geometric mean: 1.057x faster (HPT: reliability of 87.39%, 1.00x faster at 99th %ile)
- Memory usage: 1.30x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261008-macm4pro-arm64-python-bc12b7285f87f3ca9118-3.16.0a0-bc12b72-vs-3.12.6.md)
- [📈time plot](bm-20261008-macm4pro-arm64-python-bc12b7285f87f3ca9118-3.16.0a0-bc12b72-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.021x slower (HPT: reliability of 94.31%, 1.00x slower at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261008-macm4pro-arm64-python-bc12b7285f87f3ca9118-3.16.0a0-bc12b72-vs-3.13.0rc2.md)
- [📈time plot](bm-20261008-macm4pro-arm64-python-bc12b7285f87f3ca9118-3.16.0a0-bc12b72-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.083x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.12x
- new benchmarks: coverage
- [🧠memory plot](bm-20261008-macm4pro-arm64-python-bc12b7285f87f3ca9118-3.16.0a0-bc12b72-vs-base-mem.svg)
- [📄table](bm-20261008-macm4pro-arm64-python-bc12b7285f87f3ca9118-3.16.0a0-bc12b72-vs-base.md)
- [📈time plot](bm-20261008-macm4pro-arm64-python-bc12b7285f87f3ca9118-3.16.0a0-bc12b72-vs-base.svg)

