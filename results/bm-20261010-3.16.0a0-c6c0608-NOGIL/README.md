# Results

- fork: python/c6c060843b7635b5a1f8
- version: 3.16.0a0
- config: NOGIL
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

- Geometric mean: 1.039x slower (HPT: reliability of 77.33%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261010-vultr-x86_64-python-c6c060843b7635b5a1f8-3.16.0a0-c6c0608-vs-3.12.6.md)
- [📈time plot](bm-20261010-vultr-x86_64-python-c6c060843b7635b5a1f8-3.16.0a0-c6c0608-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.072x slower (HPT: reliability of 91.88%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261010-vultr-x86_64-python-c6c060843b7635b5a1f8-3.16.0a0-c6c0608-vs-3.13.0rc2.md)
- [📈time plot](bm-20261010-vultr-x86_64-python-c6c060843b7635b5a1f8-3.16.0a0-c6c0608-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.099x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20261010-vultr-x86_64-python-c6c060843b7635b5a1f8-3.16.0a0-c6c0608-vs-base-mem.svg)
- [📄table](bm-20261010-vultr-x86_64-python-c6c060843b7635b5a1f8-3.16.0a0-c6c0608-vs-base.md)
- [📈time plot](bm-20261010-vultr-x86_64-python-c6c060843b7635b5a1f8-3.16.0a0-c6c0608-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/38098297743)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261010-macm4pro-arm64-python-c6c060843b7635b5a1f8-3.16.0a0-c6c0608.json)

### vs. 3.12.6

- Geometric mean: 1.066x faster (HPT: reliability of 91.60%, 1.00x faster at 99th %ile)
- Memory usage: 1.30x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20261010-macm4pro-arm64-python-c6c060843b7635b5a1f8-3.16.0a0-c6c0608-vs-3.12.6.md)
- [📈time plot](bm-20261010-macm4pro-arm64-python-c6c060843b7635b5a1f8-3.16.0a0-c6c0608-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.013x slower (HPT: reliability of 84.80%, 1.00x slower at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20261010-macm4pro-arm64-python-c6c060843b7635b5a1f8-3.16.0a0-c6c0608-vs-3.13.0rc2.md)
- [📈time plot](bm-20261010-macm4pro-arm64-python-c6c060843b7635b5a1f8-3.16.0a0-c6c0608-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.084x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.12x
- new benchmarks: coverage
- [🧠memory plot](bm-20261010-macm4pro-arm64-python-c6c060843b7635b5a1f8-3.16.0a0-c6c0608-vs-base-mem.svg)
- [📄table](bm-20261010-macm4pro-arm64-python-c6c060843b7635b5a1f8-3.16.0a0-c6c0608-vs-base.md)
- [📈time plot](bm-20261010-macm4pro-arm64-python-c6c060843b7635b5a1f8-3.16.0a0-c6c0608-vs-base.svg)

