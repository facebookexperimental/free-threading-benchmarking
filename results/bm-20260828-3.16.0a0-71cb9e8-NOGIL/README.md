# Results

- fork: python/71cb9e8b64c4a8997195
- version: 3.16.0a0
- config: NOGIL
- commit hash: [71cb9e8](https://github.com/python/cpython/commit/71cb9e8)
- commit date: 2026-08-28T23:37:42Z
- commit merge base: [683ef4082d374eb26c1ead33f8fd989eeadc742d](https://github.com/python/cpython/commit/683ef4082d374eb26c1ead33f8fd989eeadc742d)
- commit date: 2026-08-28T23:37:42+00:00
- ref: 71cb9e8b64c4a8997195

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/33224063199)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260828-vultr-x86_64-python-71cb9e8b64c4a8997195-3.16.0a0-71cb9e8.json)

### vs. 3.12.6

- Geometric mean: 1.042x slower (HPT: reliability of 93.28%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260828-vultr-x86_64-python-71cb9e8b64c4a8997195-3.16.0a0-71cb9e8-vs-3.12.6.md)
- [📈time plot](bm-20260828-vultr-x86_64-python-71cb9e8b64c4a8997195-3.16.0a0-71cb9e8-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.074x slower (HPT: reliability of 98.21%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260828-vultr-x86_64-python-71cb9e8b64c4a8997195-3.16.0a0-71cb9e8-vs-3.13.0rc2.md)
- [📈time plot](bm-20260828-vultr-x86_64-python-71cb9e8b64c4a8997195-3.16.0a0-71cb9e8-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.103x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20260828-vultr-x86_64-python-71cb9e8b64c4a8997195-3.16.0a0-71cb9e8-vs-base-mem.svg)
- [📄table](bm-20260828-vultr-x86_64-python-71cb9e8b64c4a8997195-3.16.0a0-71cb9e8-vs-base.md)
- [📈time plot](bm-20260828-vultr-x86_64-python-71cb9e8b64c4a8997195-3.16.0a0-71cb9e8-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/33224063199)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260828-macm4pro-arm64-python-71cb9e8b64c4a8997195-3.16.0a0-71cb9e8.json)

### vs. 3.12.6

- Geometric mean: 1.011x faster (HPT: reliability of 69.77%, 1.00x slower at 99th %ile)
- Memory usage: 1.29x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260828-macm4pro-arm64-python-71cb9e8b64c4a8997195-3.16.0a0-71cb9e8-vs-3.12.6.md)
- [📈time plot](bm-20260828-macm4pro-arm64-python-71cb9e8b64c4a8997195-3.16.0a0-71cb9e8-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.063x slower (HPT: reliability of 99.85%, 1.01x slower at 99th %ile)
- Memory usage: 1.24x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260828-macm4pro-arm64-python-71cb9e8b64c4a8997195-3.16.0a0-71cb9e8-vs-3.13.0rc2.md)
- [📈time plot](bm-20260828-macm4pro-arm64-python-71cb9e8b64c4a8997195-3.16.0a0-71cb9e8-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.107x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.12x
- new benchmarks: coverage
- [🧠memory plot](bm-20260828-macm4pro-arm64-python-71cb9e8b64c4a8997195-3.16.0a0-71cb9e8-vs-base-mem.svg)
- [📄table](bm-20260828-macm4pro-arm64-python-71cb9e8b64c4a8997195-3.16.0a0-71cb9e8-vs-base.md)
- [📈time plot](bm-20260828-macm4pro-arm64-python-71cb9e8b64c4a8997195-3.16.0a0-71cb9e8-vs-base.svg)

