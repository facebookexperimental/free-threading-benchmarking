# Results

- fork: python/a4f28a52b4b54c34100e
- version: 3.16.0a0
- config: NOGIL
- commit hash: [a4f28a5](https://github.com/python/cpython/commit/a4f28a5)
- commit date: 2026-10-01T21:39:34Z
- commit merge base: [ab01d184746b3ea383f69317c16fc726d885c968](https://github.com/python/cpython/commit/ab01d184746b3ea383f69317c16fc726d885c968)
- commit date: 2026-10-01T21:39:34+00:00
- ref: a4f28a52b4b54c34100e

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/36947438017)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261001-vultr-x86_64-python-a4f28a52b4b54c34100e-3.16.0a0-a4f28a5.json)

### vs. 3.12.6

- Geometric mean: 1.043x slower (HPT: reliability of 86.61%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261001-vultr-x86_64-python-a4f28a52b4b54c34100e-3.16.0a0-a4f28a5-vs-3.12.6.md)
- [📈time plot](bm-20261001-vultr-x86_64-python-a4f28a52b4b54c34100e-3.16.0a0-a4f28a5-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.076x slower (HPT: reliability of 98.52%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261001-vultr-x86_64-python-a4f28a52b4b54c34100e-3.16.0a0-a4f28a5-vs-3.13.0rc2.md)
- [📈time plot](bm-20261001-vultr-x86_64-python-a4f28a52b4b54c34100e-3.16.0a0-a4f28a5-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.104x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20261001-vultr-x86_64-python-a4f28a52b4b54c34100e-3.16.0a0-a4f28a5-vs-base-mem.svg)
- [📄table](bm-20261001-vultr-x86_64-python-a4f28a52b4b54c34100e-3.16.0a0-a4f28a5-vs-base.md)
- [📈time plot](bm-20261001-vultr-x86_64-python-a4f28a52b4b54c34100e-3.16.0a0-a4f28a5-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/36947438017)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261001-macm4pro-arm64-python-a4f28a52b4b54c34100e-3.16.0a0-a4f28a5.json)

### vs. 3.12.6

- Geometric mean: 1.053x faster (HPT: reliability of 82.60%, 1.00x faster at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261001-macm4pro-arm64-python-a4f28a52b4b54c34100e-3.16.0a0-a4f28a5-vs-3.12.6.md)
- [📈time plot](bm-20261001-macm4pro-arm64-python-a4f28a52b4b54c34100e-3.16.0a0-a4f28a5-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.025x slower (HPT: reliability of 97.58%, 1.00x slower at 99th %ile)
- Memory usage: 1.29x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261001-macm4pro-arm64-python-a4f28a52b4b54c34100e-3.16.0a0-a4f28a5-vs-3.13.0rc2.md)
- [📈time plot](bm-20261001-macm4pro-arm64-python-a4f28a52b4b54c34100e-3.16.0a0-a4f28a5-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.077x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.11x
- new benchmarks: coverage
- [🧠memory plot](bm-20261001-macm4pro-arm64-python-a4f28a52b4b54c34100e-3.16.0a0-a4f28a5-vs-base-mem.svg)
- [📄table](bm-20261001-macm4pro-arm64-python-a4f28a52b4b54c34100e-3.16.0a0-a4f28a5-vs-base.md)
- [📈time plot](bm-20261001-macm4pro-arm64-python-a4f28a52b4b54c34100e-3.16.0a0-a4f28a5-vs-base.svg)

