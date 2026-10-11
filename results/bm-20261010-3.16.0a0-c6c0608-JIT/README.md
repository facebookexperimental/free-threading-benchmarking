# Results

- fork: python/c6c060843b7635b5a1f8
- version: 3.16.0a0
- config: JIT
- commit hash: [c6c0608](https://github.com/python/cpython/commit/c6c0608)
- commit date: 2026-10-10T23:12:35Z
- commit merge base: [fbbf4f48c48cd9de2373494b2408c1424fe7ef3f](https://github.com/python/cpython/commit/fbbf4f48c48cd9de2373494b2408c1424fe7ef3f)
- commit date: 2026-10-10T23:12:35+00:00
- ref: c6c060843b7635b5a1f8

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/38098297743)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261010-vultr-x86_64-python-c6c060843b7635b5a1f8-3.16.0a0-c6c0608.json)

### vs. 3.12.6

- Geometric mean: 1.180x faster (HPT: reliability of 100.00%, 1.10x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261010-vultr-x86_64-python-c6c060843b7635b5a1f8-3.16.0a0-c6c0608-vs-3.12.6.md)
- [📈time plot](bm-20261010-vultr-x86_64-python-c6c060843b7635b5a1f8-3.16.0a0-c6c0608-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.139x faster (HPT: reliability of 100.00%, 1.09x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261010-vultr-x86_64-python-c6c060843b7635b5a1f8-3.16.0a0-c6c0608-vs-3.13.0rc2.md)
- [📈time plot](bm-20261010-vultr-x86_64-python-c6c060843b7635b5a1f8-3.16.0a0-c6c0608-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.105x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.05x
- [🧠memory plot](bm-20261010-vultr-x86_64-python-c6c060843b7635b5a1f8-3.16.0a0-c6c0608-vs-base-mem.svg)
- [📄table](bm-20261010-vultr-x86_64-python-c6c060843b7635b5a1f8-3.16.0a0-c6c0608-vs-base.md)
- [📈time plot](bm-20261010-vultr-x86_64-python-c6c060843b7635b5a1f8-3.16.0a0-c6c0608-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/38098297743)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261010-macm4pro-arm64-python-c6c060843b7635b5a1f8-3.16.0a0-c6c0608.json)

### vs. 3.12.6

- Geometric mean: 1.300x faster (HPT: reliability of 100.00%, 1.19x faster at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20261010-macm4pro-arm64-python-c6c060843b7635b5a1f8-3.16.0a0-c6c0608-vs-3.12.6.md)
- [📈time plot](bm-20261010-macm4pro-arm64-python-c6c060843b7635b5a1f8-3.16.0a0-c6c0608-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.201x faster (HPT: reliability of 100.00%, 1.09x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20261010-macm4pro-arm64-python-c6c060843b7635b5a1f8-3.16.0a0-c6c0608-vs-3.13.0rc2.md)
- [📈time plot](bm-20261010-macm4pro-arm64-python-c6c060843b7635b5a1f8-3.16.0a0-c6c0608-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.113x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.04x
- [🧠memory plot](bm-20261010-macm4pro-arm64-python-c6c060843b7635b5a1f8-3.16.0a0-c6c0608-vs-base-mem.svg)
- [📄table](bm-20261010-macm4pro-arm64-python-c6c060843b7635b5a1f8-3.16.0a0-c6c0608-vs-base.md)
- [📈time plot](bm-20261010-macm4pro-arm64-python-c6c060843b7635b5a1f8-3.16.0a0-c6c0608-vs-base.svg)

