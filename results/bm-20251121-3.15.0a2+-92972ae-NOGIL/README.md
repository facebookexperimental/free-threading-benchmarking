# Results

- fork: python/92972aea0f0e12dd21bf
- version: 3.15.0a2+
- config: NOGIL
- commit hash: [92972ae](https://github.com/python/cpython/commit/92972ae)
- commit date: 2025-11-21T21:36:30Z
- commit merge base: [2d50dd242e04b94f86cb23c4972c1b423c670175](https://github.com/python/cpython/commit/2d50dd242e04b94f86cb23c4972c1b423c670175)
- commit date: 2025-11-21T21:36:30+00:00
- ref: 92972aea0f0e12dd21bf

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19587224828)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251121-vultr-x86_64-python-92972aea0f0e12dd21bf-3.15.0a2%2B-92972ae.json)

### vs. 3.12.6

- Geometric mean: 1.019x slower (HPT: reliability of 80.20%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251121-vultr-x86_64-python-92972aea0f0e12dd21bf-3.15.0a2%2B-92972ae-vs-3.12.6.md)
- [📈time plot](bm-20251121-vultr-x86_64-python-92972aea0f0e12dd21bf-3.15.0a2%2B-92972ae-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.052x slower (HPT: reliability of 96.28%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251121-vultr-x86_64-python-92972aea0f0e12dd21bf-3.15.0a2%2B-92972ae-vs-3.13.0rc2.md)
- [📈time plot](bm-20251121-vultr-x86_64-python-92972aea0f0e12dd21bf-3.15.0a2%2B-92972ae-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.094x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20251121-vultr-x86_64-python-92972aea0f0e12dd21bf-3.15.0a2%2B-92972ae-vs-base-mem.svg)
- [📄table](bm-20251121-vultr-x86_64-python-92972aea0f0e12dd21bf-3.15.0a2%2B-92972ae-vs-base.md)
- [📈time plot](bm-20251121-vultr-x86_64-python-92972aea0f0e12dd21bf-3.15.0a2%2B-92972ae-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19587224828)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251121-macm4pro-arm64-python-92972aea0f0e12dd21bf-3.15.0a2%2B-92972ae.json)

### vs. 3.12.6

- Geometric mean: 1.104x faster (HPT: reliability of 99.85%, 1.01x faster at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251121-macm4pro-arm64-python-92972aea0f0e12dd21bf-3.15.0a2%2B-92972ae-vs-3.12.6.md)
- [📈time plot](bm-20251121-macm4pro-arm64-python-92972aea0f0e12dd21bf-3.15.0a2%2B-92972ae-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.018x faster (HPT: reliability of 52.17%, 1.00x slower at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251121-macm4pro-arm64-python-92972aea0f0e12dd21bf-3.15.0a2%2B-92972ae-vs-3.13.0rc2.md)
- [📈time plot](bm-20251121-macm4pro-arm64-python-92972aea0f0e12dd21bf-3.15.0a2%2B-92972ae-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.026x slower (HPT: reliability of 99.47%, 1.00x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20251121-macm4pro-arm64-python-92972aea0f0e12dd21bf-3.15.0a2%2B-92972ae-vs-base-mem.svg)
- [📄table](bm-20251121-macm4pro-arm64-python-92972aea0f0e12dd21bf-3.15.0a2%2B-92972ae-vs-base.md)
- [📈time plot](bm-20251121-macm4pro-arm64-python-92972aea0f0e12dd21bf-3.15.0a2%2B-92972ae-vs-base.svg)

