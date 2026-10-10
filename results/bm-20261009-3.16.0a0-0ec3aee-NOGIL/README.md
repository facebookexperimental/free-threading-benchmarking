# Results

- fork: python/0ec3aee262b03276a18a
- version: 3.16.0a0
- config: NOGIL
- commit hash: [0ec3aee](https://github.com/python/cpython/commit/0ec3aee)
- commit date: 2026-10-09T22:25:44Z
- commit merge base: [5a22a62b96a68c2dd31784c5e3427ad7b365388a](https://github.com/python/cpython/commit/5a22a62b96a68c2dd31784c5e3427ad7b365388a)
- commit date: 2026-10-09T22:25:44+00:00
- ref: 0ec3aee262b03276a18a

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/38010408728)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261009-vultr-x86_64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee.json)

### vs. 3.12.6

- Geometric mean: 1.043x slower (HPT: reliability of 78.80%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261009-vultr-x86_64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee-vs-3.12.6.md)
- [📈time plot](bm-20261009-vultr-x86_64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.075x slower (HPT: reliability of 97.59%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261009-vultr-x86_64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee-vs-3.13.0rc2.md)
- [📈time plot](bm-20261009-vultr-x86_64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/38010408728)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee.json)

### vs. 3.12.6

- Geometric mean: 1.060x faster (HPT: reliability of 91.23%, 1.00x faster at 99th %ile)
- Memory usage: 1.29x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee-vs-3.12.6.md)
- [📈time plot](bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.019x slower (HPT: reliability of 93.80%, 1.00x slower at 99th %ile)
- Memory usage: 1.25x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee-vs-3.13.0rc2.md)
- [📈time plot](bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.083x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.12x
- new benchmarks: coverage
- [🧠memory plot](bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee-vs-base-mem.svg)
- [📄table](bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee-vs-base.md)
- [📈time plot](bm-20261009-macm4pro-arm64-python-0ec3aee262b03276a18a-3.16.0a0-0ec3aee-vs-base.svg)

