# Results

- fork: python/a26a301f8b09c1825b28
- version: 3.14.0a6+
- config: 
- commit hash: [a26a301](https://github.com/python/cpython/commit/a26a301)
- commit date: 2025-03-25T16:35:39-07:00
- commit merge base: [488174dc68f90217fd43aa95d87441cc6bad6a29](https://github.com/python/cpython/commit/488174dc68f90217fd43aa95d87441cc6bad6a29)
- ref: a26a301f8b09c1825b28

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14072728396)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250325-linux-x86_64-python-a26a301f8b09c1825b28-3.14.0a6%2B-a26a301.json)

### vs. 3.12.6

- Geometric mean: 1.101x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250325-linux-x86_64-python-a26a301f8b09c1825b28-3.14.0a6%2B-a26a301-vs-3.12.6.md)
- [📈time plot](bm-20250325-linux-x86_64-python-a26a301f8b09c1825b28-3.14.0a6%2B-a26a301-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.056x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250325-linux-x86_64-python-a26a301f8b09c1825b28-3.14.0a6%2B-a26a301-vs-3.13.0rc2.md)
- [📈time plot](bm-20250325-linux-x86_64-python-a26a301f8b09c1825b28-3.14.0a6%2B-a26a301-vs-3.13.0rc2.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14072728396)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250325-vultr-x86_64-python-a26a301f8b09c1825b28-3.14.0a6%2B-a26a301.json)

### vs. 3.12.6

- Geometric mean: 1.071x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250325-vultr-x86_64-python-a26a301f8b09c1825b28-3.14.0a6%2B-a26a301-vs-3.12.6.md)
- [📈time plot](bm-20250325-vultr-x86_64-python-a26a301f8b09c1825b28-3.14.0a6%2B-a26a301-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.032x faster (HPT: reliability of 97.80%, 1.00x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250325-vultr-x86_64-python-a26a301f8b09c1825b28-3.14.0a6%2B-a26a301-vs-3.13.0rc2.md)
- [📈time plot](bm-20250325-vultr-x86_64-python-a26a301f8b09c1825b28-3.14.0a6%2B-a26a301-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14072728396)
- cpu model: missing
- platform: macOS-15.3.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250325-macm4pro-arm64-python-a26a301f8b09c1825b28-3.14.0a6%2B-a26a301.json)

### vs. 3.12.6

- Geometric mean: 1.009x faster (HPT: reliability of 89.64%, 1.00x slower at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250325-macm4pro-arm64-python-a26a301f8b09c1825b28-3.14.0a6%2B-a26a301-vs-3.12.6.md)
- [📈time plot](bm-20250325-macm4pro-arm64-python-a26a301f8b09c1825b28-3.14.0a6%2B-a26a301-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.063x slower (HPT: reliability of 99.99%, 1.02x slower at 99th %ile)
- Memory usage: 1.07x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250325-macm4pro-arm64-python-a26a301f8b09c1825b28-3.14.0a6%2B-a26a301-vs-3.13.0rc2.md)
- [📈time plot](bm-20250325-macm4pro-arm64-python-a26a301f8b09c1825b28-3.14.0a6%2B-a26a301-vs-3.13.0rc2.svg)

