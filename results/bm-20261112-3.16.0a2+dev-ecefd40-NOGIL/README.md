# Results

- fork: python/ecefd40671f340d543c2
- version: 3.16.0a2+dev
- config: NOGIL
- commit hash: [ecefd40](https://github.com/python/cpython/commit/ecefd40)
- commit date: 2026-11-12T15:50:45-08:00
- commit merge base: [78a70f862e3b7f28c62bd9352af83920678f399a](https://github.com/python/cpython/commit/78a70f862e3b7f28c62bd9352af83920678f399a)
- ref: ecefd40671f340d543c2

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/43336902289)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261112-vultr-x86_64-python-ecefd40671f340d543c2-3.16.0a2%2Bdev-ecefd40.json)

### vs. 3.12.6

- Geometric mean: 1.027x slower (HPT: reliability of 74.70%, 1.00x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261112-vultr-x86_64-python-ecefd40671f340d543c2-3.16.0a2%2Bdev-ecefd40-vs-3.12.6.md)
- [📈time plot](bm-20261112-vultr-x86_64-python-ecefd40671f340d543c2-3.16.0a2%2Bdev-ecefd40-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.060x slower (HPT: reliability of 88.64%, 1.00x slower at 99th %ile)
- Memory usage: 1.30x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261112-vultr-x86_64-python-ecefd40671f340d543c2-3.16.0a2%2Bdev-ecefd40-vs-3.13.0rc2.md)
- [📈time plot](bm-20261112-vultr-x86_64-python-ecefd40671f340d543c2-3.16.0a2%2Bdev-ecefd40-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.114x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.14x
- [🧠memory plot](bm-20261112-vultr-x86_64-python-ecefd40671f340d543c2-3.16.0a2%2Bdev-ecefd40-vs-base-mem.svg)
- [📄table](bm-20261112-vultr-x86_64-python-ecefd40671f340d543c2-3.16.0a2%2Bdev-ecefd40-vs-base.md)
- [📈time plot](bm-20261112-vultr-x86_64-python-ecefd40671f340d543c2-3.16.0a2%2Bdev-ecefd40-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/43336902289)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261112-macm4pro-arm64-python-ecefd40671f340d543c2-3.16.0a2%2Bdev-ecefd40.json)

### vs. 3.12.6

- Geometric mean: 1.061x faster (HPT: reliability of 88.02%, 1.00x faster at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261112-macm4pro-arm64-python-ecefd40671f340d543c2-3.16.0a2%2Bdev-ecefd40-vs-3.12.6.md)
- [📈time plot](bm-20261112-macm4pro-arm64-python-ecefd40671f340d543c2-3.16.0a2%2Bdev-ecefd40-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.017x slower (HPT: reliability of 95.67%, 1.00x slower at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261112-macm4pro-arm64-python-ecefd40671f340d543c2-3.16.0a2%2Bdev-ecefd40-vs-3.13.0rc2.md)
- [📈time plot](bm-20261112-macm4pro-arm64-python-ecefd40671f340d543c2-3.16.0a2%2Bdev-ecefd40-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.103x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.08x
- new benchmarks: coverage
- [🧠memory plot](bm-20261112-macm4pro-arm64-python-ecefd40671f340d543c2-3.16.0a2%2Bdev-ecefd40-vs-base-mem.svg)
- [📄table](bm-20261112-macm4pro-arm64-python-ecefd40671f340d543c2-3.16.0a2%2Bdev-ecefd40-vs-base.md)
- [📈time plot](bm-20261112-macm4pro-arm64-python-ecefd40671f340d543c2-3.16.0a2%2Bdev-ecefd40-vs-base.svg)

