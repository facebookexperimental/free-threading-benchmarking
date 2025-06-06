# Results

- fork: python/bc26f95e8ff60ccca981
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [bc26f95](https://github.com/python/cpython/commit/bc26f95)
- commit date: 2025-03-22T15:44:56-07:00
- commit merge base: [18249d938335312d618a3962ec7590bea709d58e](https://github.com/python/cpython/commit/18249d938335312d618a3962ec7590bea709d58e)
- ref: bc26f95e8ff60ccca981

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14013620569)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6%2B-bc26f95.json)

### vs. 3.12.6

- Geometric mean: 1.047x slower (HPT: reliability of 99.99%, 1.03x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6%2B-bc26f95-vs-3.12.6.md)
- [📈time plot](bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6%2B-bc26f95-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.079x slower (HPT: reliability of 99.99%, 1.04x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6%2B-bc26f95-vs-3.13.0rc2.md)
- [📈time plot](bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6%2B-bc26f95-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.111x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.21x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6%2B-bc26f95-vs-base-mem.svg)
- [📄table](bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6%2B-bc26f95-vs-base.md)
- [📈time plot](bm-20250322-vultr-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6%2B-bc26f95-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14013620569)
- cpu model: missing
- platform: macOS-15.3.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6%2B-bc26f95.json)

### vs. 3.12.6

- Geometric mean: 1.015x slower (HPT: reliability of 99.48%, 1.00x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6%2B-bc26f95-vs-3.12.6.md)
- [📈time plot](bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6%2B-bc26f95-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.086x slower (HPT: reliability of 99.98%, 1.04x slower at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6%2B-bc26f95-vs-3.13.0rc2.md)
- [📈time plot](bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6%2B-bc26f95-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.034x slower (HPT: reliability of 99.94%, 1.01x slower at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: 🔴 dask
- [🧠memory plot](bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6%2B-bc26f95-vs-base-mem.svg)
- [📄table](bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6%2B-bc26f95-vs-base.md)
- [📈time plot](bm-20250322-macm4pro-arm64-python-bc26f95e8ff60ccca981-3.14.0a6%2B-bc26f95-vs-base.svg)

