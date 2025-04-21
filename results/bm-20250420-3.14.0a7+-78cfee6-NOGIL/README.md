# Results

- fork: python/78cfee6f0920ac914ed1
- version: 3.14.0a7+
- config: NOGIL
- commit hash: [78cfee6](https://github.com/python/cpython/commit/78cfee6)
- commit date: 2025-04-20T23:21:29Z
- commit merge base: [dc4a7077aca7f702e09c29433c20cf8bb9feff64](https://github.com/python/cpython/commit/dc4a7077aca7f702e09c29433c20cf8bb9feff64)
- commit date: 2025-04-20T23:21:29+00:00
- ref: 78cfee6f0920ac914ed1

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14564772189)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1071-aws-x86_64-with-glibc2.31
- [raw results](bm-20250420-linux-x86_64-python-78cfee6f0920ac914ed1-3.14.0a7%2B-78cfee6.json)

### vs. 3.12.6

- Geometric mean: 1.142x faster (HPT: reliability of 99.90%, 1.02x faster at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250420-linux-x86_64-python-78cfee6f0920ac914ed1-3.14.0a7%2B-78cfee6-vs-3.12.6.md)
- [📈time plot](bm-20250420-linux-x86_64-python-78cfee6f0920ac914ed1-3.14.0a7%2B-78cfee6-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.102x faster (HPT: reliability of 99.80%, 1.01x faster at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250420-linux-x86_64-python-78cfee6f0920ac914ed1-3.14.0a7%2B-78cfee6-vs-3.13.0rc2.md)
- [📈time plot](bm-20250420-linux-x86_64-python-78cfee6f0920ac914ed1-3.14.0a7%2B-78cfee6-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.080x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.19x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250420-linux-x86_64-python-78cfee6f0920ac914ed1-3.14.0a7%2B-78cfee6-vs-base-mem.svg)
- [📄table](bm-20250420-linux-x86_64-python-78cfee6f0920ac914ed1-3.14.0a7%2B-78cfee6-vs-base.md)
- [📈time plot](bm-20250420-linux-x86_64-python-78cfee6f0920ac914ed1-3.14.0a7%2B-78cfee6-vs-base.svg)

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14564772189)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250420-vultr-x86_64-python-78cfee6f0920ac914ed1-3.14.0a7%2B-78cfee6.json)

### vs. 3.12.6

- Geometric mean: 1.026x faster (HPT: reliability of 74.13%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250420-vultr-x86_64-python-78cfee6f0920ac914ed1-3.14.0a7%2B-78cfee6-vs-3.12.6.md)
- [📈time plot](bm-20250420-vultr-x86_64-python-78cfee6f0920ac914ed1-3.14.0a7%2B-78cfee6-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.008x slower (HPT: reliability of 85.78%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250420-vultr-x86_64-python-78cfee6f0920ac914ed1-3.14.0a7%2B-78cfee6-vs-3.13.0rc2.md)
- [📈time plot](bm-20250420-vultr-x86_64-python-78cfee6f0920ac914ed1-3.14.0a7%2B-78cfee6-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.086x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250420-vultr-x86_64-python-78cfee6f0920ac914ed1-3.14.0a7%2B-78cfee6-vs-base-mem.svg)
- [📄table](bm-20250420-vultr-x86_64-python-78cfee6f0920ac914ed1-3.14.0a7%2B-78cfee6-vs-base.md)
- [📈time plot](bm-20250420-vultr-x86_64-python-78cfee6f0920ac914ed1-3.14.0a7%2B-78cfee6-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14564772189)
- cpu model: missing
- platform: macOS-15.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20250420-macm4pro-arm64-python-78cfee6f0920ac914ed1-3.14.0a7%2B-78cfee6.json)

### vs. 3.12.6

- Geometric mean: 1.115x faster (HPT: reliability of 99.87%, 1.01x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250420-macm4pro-arm64-python-78cfee6f0920ac914ed1-3.14.0a7%2B-78cfee6-vs-3.12.6.md)
- [📈time plot](bm-20250420-macm4pro-arm64-python-78cfee6f0920ac914ed1-3.14.0a7%2B-78cfee6-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.034x faster (HPT: reliability of 54.29%, 1.00x slower at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250420-macm4pro-arm64-python-78cfee6f0920ac914ed1-3.14.0a7%2B-78cfee6-vs-3.13.0rc2.md)
- [📈time plot](bm-20250420-macm4pro-arm64-python-78cfee6f0920ac914ed1-3.14.0a7%2B-78cfee6-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.013x faster (HPT: reliability of 79.59%, 1.00x slower at 99th %ile)
- Memory usage: 1.09x
- [🧠memory plot](bm-20250420-macm4pro-arm64-python-78cfee6f0920ac914ed1-3.14.0a7%2B-78cfee6-vs-base-mem.svg)
- [📄table](bm-20250420-macm4pro-arm64-python-78cfee6f0920ac914ed1-3.14.0a7%2B-78cfee6-vs-base.md)
- [📈time plot](bm-20250420-macm4pro-arm64-python-78cfee6f0920ac914ed1-3.14.0a7%2B-78cfee6-vs-base.svg)

