# Results

- fork: python/98e2c3af4794d6c6ebe4
- version: 3.15.0a0
- config: NOGIL
- commit hash: [98e2c3a](https://github.com/python/cpython/commit/98e2c3a)
- commit date: 2025-05-09T20:17:12Z
- commit merge base: [bbe9c31edc4fc3e1cdc908e9a06593c394f4bfdb](https://github.com/python/cpython/commit/bbe9c31edc4fc3e1cdc908e9a06593c394f4bfdb)
- commit date: 2025-05-09T20:17:12+00:00
- ref: 98e2c3af4794d6c6ebe4

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14939938728)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-6.8.0-1024-aws-x86_64-with-glibc2.35
- [raw results](bm-20250509-linux-x86_64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a.json)

### vs. 3.12.6

- Geometric mean: 1.121x faster (HPT: reliability of 97.19%, 1.00x faster at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250509-linux-x86_64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a-vs-3.12.6.md)
- [📈time plot](bm-20250509-linux-x86_64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.080x faster (HPT: reliability of 93.15%, 1.00x faster at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250509-linux-x86_64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a-vs-3.13.0rc2.md)
- [📈time plot](bm-20250509-linux-x86_64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.083x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.22x
- [🧠memory plot](bm-20250509-linux-x86_64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a-vs-base-mem.svg)
- [📄table](bm-20250509-linux-x86_64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a-vs-base.md)
- [📈time plot](bm-20250509-linux-x86_64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14939938728)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250509-vultr-x86_64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a.json)

### vs. 3.12.6

- Geometric mean: 1.009x faster (HPT: reliability of 90.96%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250509-vultr-x86_64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a-vs-3.12.6.md)
- [📈time plot](bm-20250509-vultr-x86_64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.025x slower (HPT: reliability of 97.67%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250509-vultr-x86_64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a-vs-3.13.0rc2.md)
- [📈time plot](bm-20250509-vultr-x86_64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.094x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.22x
- [🧠memory plot](bm-20250509-vultr-x86_64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a-vs-base-mem.svg)
- [📄table](bm-20250509-vultr-x86_64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a-vs-base.md)
- [📈time plot](bm-20250509-vultr-x86_64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14939938728)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250509-macm4pro-arm64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a.json)

### vs. 3.12.6

- Geometric mean: 1.082x faster (HPT: reliability of 93.64%, 1.00x faster at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250509-macm4pro-arm64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a-vs-3.12.6.md)
- [📈time plot](bm-20250509-macm4pro-arm64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.003x faster (HPT: reliability of 78.08%, 1.00x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250509-macm4pro-arm64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a-vs-3.13.0rc2.md)
- [📈time plot](bm-20250509-macm4pro-arm64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.007x slower (HPT: reliability of 94.52%, 1.00x slower at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: 🔴 dask
- [🧠memory plot](bm-20250509-macm4pro-arm64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a-vs-base-mem.svg)
- [📄table](bm-20250509-macm4pro-arm64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a-vs-base.md)
- [📈time plot](bm-20250509-macm4pro-arm64-python-98e2c3af4794d6c6ebe4-3.15.0a0-98e2c3a-vs-base.svg)

