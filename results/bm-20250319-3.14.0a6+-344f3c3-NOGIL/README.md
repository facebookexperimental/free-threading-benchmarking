# Results

- fork: python/344f3c3fd41091188b7e
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [344f3c3](https://github.com/python/cpython/commit/344f3c3)
- commit date: 2025-03-19T23:46:25Z
- commit merge base: [6827c5129c5541a8608323fceda2233d542a5ec2](https://github.com/python/cpython/commit/6827c5129c5541a8608323fceda2233d542a5ec2)
- commit date: 2025-03-19T23:46:25+00:00
- ref: 344f3c3fd41091188b7e

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13959309305)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250319-linux-x86_64-python-344f3c3fd41091188b7e-3.14.0a6%2B-344f3c3.json)

### vs. 3.12.6

- Geometric mean: 1.018x slower (HPT: reliability of 99.82%, 1.01x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250319-linux-x86_64-python-344f3c3fd41091188b7e-3.14.0a6%2B-344f3c3-vs-3.12.6.md)
- [📈time plot](bm-20250319-linux-x86_64-python-344f3c3fd41091188b7e-3.14.0a6%2B-344f3c3-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.053x slower (HPT: reliability of 99.83%, 1.01x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250319-linux-x86_64-python-344f3c3fd41091188b7e-3.14.0a6%2B-344f3c3-vs-3.13.0rc2.md)
- [📈time plot](bm-20250319-linux-x86_64-python-344f3c3fd41091188b7e-3.14.0a6%2B-344f3c3-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.042x slower (HPT: reliability of 99.92%, 1.02x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250319-linux-x86_64-python-344f3c3fd41091188b7e-3.14.0a6%2B-344f3c3-vs-base-mem.svg)
- [📄table](bm-20250319-linux-x86_64-python-344f3c3fd41091188b7e-3.14.0a6%2B-344f3c3-vs-base.md)
- [📈time plot](bm-20250319-linux-x86_64-python-344f3c3fd41091188b7e-3.14.0a6%2B-344f3c3-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13959309305)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250319-vultr-x86_64-python-344f3c3fd41091188b7e-3.14.0a6%2B-344f3c3.json)

### vs. 3.12.6

- Geometric mean: 1.039x slower (HPT: reliability of 99.98%, 1.02x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250319-vultr-x86_64-python-344f3c3fd41091188b7e-3.14.0a6%2B-344f3c3-vs-3.12.6.md)
- [📈time plot](bm-20250319-vultr-x86_64-python-344f3c3fd41091188b7e-3.14.0a6%2B-344f3c3-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.071x slower (HPT: reliability of 99.97%, 1.03x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250319-vultr-x86_64-python-344f3c3fd41091188b7e-3.14.0a6%2B-344f3c3-vs-3.13.0rc2.md)
- [📈time plot](bm-20250319-vultr-x86_64-python-344f3c3fd41091188b7e-3.14.0a6%2B-344f3c3-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.095x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250319-vultr-x86_64-python-344f3c3fd41091188b7e-3.14.0a6%2B-344f3c3-vs-base-mem.svg)
- [📄table](bm-20250319-vultr-x86_64-python-344f3c3fd41091188b7e-3.14.0a6%2B-344f3c3-vs-base.md)
- [📈time plot](bm-20250319-vultr-x86_64-python-344f3c3fd41091188b7e-3.14.0a6%2B-344f3c3-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13959309305)
- cpu model: missing
- platform: macOS-15.3.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250319-macm4pro-arm64-python-344f3c3fd41091188b7e-3.14.0a6%2B-344f3c3.json)

### vs. 3.12.6

- Geometric mean: 1.012x slower (HPT: reliability of 99.54%, 1.00x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250319-macm4pro-arm64-python-344f3c3fd41091188b7e-3.14.0a6%2B-344f3c3-vs-3.12.6.md)
- [📈time plot](bm-20250319-macm4pro-arm64-python-344f3c3fd41091188b7e-3.14.0a6%2B-344f3c3-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.084x slower (HPT: reliability of 99.98%, 1.04x slower at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250319-macm4pro-arm64-python-344f3c3fd41091188b7e-3.14.0a6%2B-344f3c3-vs-3.13.0rc2.md)
- [📈time plot](bm-20250319-macm4pro-arm64-python-344f3c3fd41091188b7e-3.14.0a6%2B-344f3c3-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.083x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: 🔴 dask
- [🧠memory plot](bm-20250319-macm4pro-arm64-python-344f3c3fd41091188b7e-3.14.0a6%2B-344f3c3-vs-base-mem.svg)
- [📄table](bm-20250319-macm4pro-arm64-python-344f3c3fd41091188b7e-3.14.0a6%2B-344f3c3-vs-base.md)
- [📈time plot](bm-20250319-macm4pro-arm64-python-344f3c3fd41091188b7e-3.14.0a6%2B-344f3c3-vs-base.svg)

