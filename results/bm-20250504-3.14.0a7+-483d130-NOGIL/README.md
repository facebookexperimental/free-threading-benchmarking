# Results

- fork: python/483d130e504f63aaf3af
- version: 3.14.0a7+
- config: NOGIL
- commit hash: [483d130](https://github.com/python/cpython/commit/483d130)
- commit date: 2025-05-04T23:46:21Z
- commit merge base: [30840706b029645b9631b92c687834fcced6413e](https://github.com/python/cpython/commit/30840706b029645b9631b92c687834fcced6413e)
- commit date: 2025-05-04T23:46:21+00:00
- ref: 483d130e504f63aaf3af

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14826714583)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-6.8.0-1024-aws-x86_64-with-glibc2.35
- [raw results](bm-20250504-linux-x86_64-python-483d130e504f63aaf3af-3.14.0a7%2B-483d130.json)

### vs. 3.12.6

- Geometric mean: 1.109x faster (HPT: reliability of 95.05%, 1.00x faster at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250504-linux-x86_64-python-483d130e504f63aaf3af-3.14.0a7%2B-483d130-vs-3.12.6.md)
- [📈time plot](bm-20250504-linux-x86_64-python-483d130e504f63aaf3af-3.14.0a7%2B-483d130-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.068x faster (HPT: reliability of 69.27%, 1.00x faster at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250504-linux-x86_64-python-483d130e504f63aaf3af-3.14.0a7%2B-483d130-vs-3.13.0rc2.md)
- [📈time plot](bm-20250504-linux-x86_64-python-483d130e504f63aaf3af-3.14.0a7%2B-483d130-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.087x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20250504-linux-x86_64-python-483d130e504f63aaf3af-3.14.0a7%2B-483d130-vs-base-mem.svg)
- [📄table](bm-20250504-linux-x86_64-python-483d130e504f63aaf3af-3.14.0a7%2B-483d130-vs-base.md)
- [📈time plot](bm-20250504-linux-x86_64-python-483d130e504f63aaf3af-3.14.0a7%2B-483d130-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14826714583)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250504-vultr-x86_64-python-483d130e504f63aaf3af-3.14.0a7%2B-483d130.json)

### vs. 3.12.6

- Geometric mean: 1.011x faster (HPT: reliability of 93.55%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250504-vultr-x86_64-python-483d130e504f63aaf3af-3.14.0a7%2B-483d130-vs-3.12.6.md)
- [📈time plot](bm-20250504-vultr-x86_64-python-483d130e504f63aaf3af-3.14.0a7%2B-483d130-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.021x slower (HPT: reliability of 97.23%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250504-vultr-x86_64-python-483d130e504f63aaf3af-3.14.0a7%2B-483d130-vs-3.13.0rc2.md)
- [📈time plot](bm-20250504-vultr-x86_64-python-483d130e504f63aaf3af-3.14.0a7%2B-483d130-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.085x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250504-vultr-x86_64-python-483d130e504f63aaf3af-3.14.0a7%2B-483d130-vs-base-mem.svg)
- [📄table](bm-20250504-vultr-x86_64-python-483d130e504f63aaf3af-3.14.0a7%2B-483d130-vs-base.md)
- [📈time plot](bm-20250504-vultr-x86_64-python-483d130e504f63aaf3af-3.14.0a7%2B-483d130-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14826714583)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250504-macm4pro-arm64-python-483d130e504f63aaf3af-3.14.0a7%2B-483d130.json)

### vs. 3.12.6

- Geometric mean: 1.097x faster (HPT: reliability of 98.15%, 1.00x faster at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250504-macm4pro-arm64-python-483d130e504f63aaf3af-3.14.0a7%2B-483d130-vs-3.12.6.md)
- [📈time plot](bm-20250504-macm4pro-arm64-python-483d130e504f63aaf3af-3.14.0a7%2B-483d130-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.018x faster (HPT: reliability of 63.50%, 1.00x slower at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250504-macm4pro-arm64-python-483d130e504f63aaf3af-3.14.0a7%2B-483d130-vs-3.13.0rc2.md)
- [📈time plot](bm-20250504-macm4pro-arm64-python-483d130e504f63aaf3af-3.14.0a7%2B-483d130-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.019x slower (HPT: reliability of 99.31%, 1.00x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20250504-macm4pro-arm64-python-483d130e504f63aaf3af-3.14.0a7%2B-483d130-vs-base-mem.svg)
- [📄table](bm-20250504-macm4pro-arm64-python-483d130e504f63aaf3af-3.14.0a7%2B-483d130-vs-base.md)
- [📈time plot](bm-20250504-macm4pro-arm64-python-483d130e504f63aaf3af-3.14.0a7%2B-483d130-vs-base.svg)

