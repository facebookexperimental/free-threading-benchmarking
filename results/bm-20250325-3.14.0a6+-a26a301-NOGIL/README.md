# Results

- fork: python/a26a301f8b09c1825b28
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [a26a301](https://github.com/python/cpython/commit/a26a301)
- commit date: 2025-03-25T16:35:39-07:00
- commit merge base: [488174dc68f90217fd43aa95d87441cc6bad6a29](https://github.com/python/cpython/commit/488174dc68f90217fd43aa95d87441cc6bad6a29)
- ref: a26a301f8b09c1825b28

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14072728396)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250325-vultr-x86_64-python-a26a301f8b09c1825b28-3.14.0a6%2B-a26a301.json)

### vs. 3.12.6

- Geometric mean: 1.047x slower (HPT: reliability of 99.99%, 1.03x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250325-vultr-x86_64-python-a26a301f8b09c1825b28-3.14.0a6%2B-a26a301-vs-3.12.6.md)
- [📈time plot](bm-20250325-vultr-x86_64-python-a26a301f8b09c1825b28-3.14.0a6%2B-a26a301-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.079x slower (HPT: reliability of 99.99%, 1.04x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250325-vultr-x86_64-python-a26a301f8b09c1825b28-3.14.0a6%2B-a26a301-vs-3.13.0rc2.md)
- [📈time plot](bm-20250325-vultr-x86_64-python-a26a301f8b09c1825b28-3.14.0a6%2B-a26a301-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.114x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250325-vultr-x86_64-python-a26a301f8b09c1825b28-3.14.0a6%2B-a26a301-vs-base-mem.svg)
- [📄table](bm-20250325-vultr-x86_64-python-a26a301f8b09c1825b28-3.14.0a6%2B-a26a301-vs-base.md)
- [📈time plot](bm-20250325-vultr-x86_64-python-a26a301f8b09c1825b28-3.14.0a6%2B-a26a301-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14072728396)
- cpu model: missing
- platform: macOS-15.3.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250325-macm4pro-arm64-python-a26a301f8b09c1825b28-3.14.0a6%2B-a26a301.json)

### vs. 3.12.6

- Geometric mean: 1.025x slower (HPT: reliability of 99.86%, 1.01x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250325-macm4pro-arm64-python-a26a301f8b09c1825b28-3.14.0a6%2B-a26a301-vs-3.12.6.md)
- [📈time plot](bm-20250325-macm4pro-arm64-python-a26a301f8b09c1825b28-3.14.0a6%2B-a26a301-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.095x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250325-macm4pro-arm64-python-a26a301f8b09c1825b28-3.14.0a6%2B-a26a301-vs-3.13.0rc2.md)
- [📈time plot](bm-20250325-macm4pro-arm64-python-a26a301f8b09c1825b28-3.14.0a6%2B-a26a301-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.035x slower (HPT: reliability of 99.94%, 1.01x slower at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: 🔴 dask
- [🧠memory plot](bm-20250325-macm4pro-arm64-python-a26a301f8b09c1825b28-3.14.0a6%2B-a26a301-vs-base-mem.svg)
- [📄table](bm-20250325-macm4pro-arm64-python-a26a301f8b09c1825b28-3.14.0a6%2B-a26a301-vs-base.md)
- [📈time plot](bm-20250325-macm4pro-arm64-python-a26a301f8b09c1825b28-3.14.0a6%2B-a26a301-vs-base.svg)

