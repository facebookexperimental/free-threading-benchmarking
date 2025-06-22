# Results

- fork: python/b14986c91464b06e9016
- version: 3.15.0a0
- config: NOGIL
- commit hash: [b14986c](https://github.com/python/cpython/commit/b14986c)
- commit date: 2025-06-21T22:03:17+05:30
- commit merge base: [6a16b3c440cf9ecabecd3e90f44310e3b0765780](https://github.com/python/cpython/commit/6a16b3c440cf9ecabecd3e90f44310e3b0765780)
- ref: b14986c91464b06e9016

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15800985329)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250621-vultr-x86_64-python-b14986c91464b06e9016-3.15.0a0-b14986c.json)

### vs. 3.12.6

- Geometric mean: 1.017x faster (HPT: reliability of 85.97%, 1.00x slower at 99th %ile)
- Memory usage: 1.44x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250621-vultr-x86_64-python-b14986c91464b06e9016-3.15.0a0-b14986c-vs-3.12.6.md)
- [📈time plot](bm-20250621-vultr-x86_64-python-b14986c91464b06e9016-3.15.0a0-b14986c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.019x slower (HPT: reliability of 96.04%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250621-vultr-x86_64-python-b14986c91464b06e9016-3.15.0a0-b14986c-vs-3.13.0rc2.md)
- [📈time plot](bm-20250621-vultr-x86_64-python-b14986c91464b06e9016-3.15.0a0-b14986c-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.083x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.22x
- [🧠memory plot](bm-20250621-vultr-x86_64-python-b14986c91464b06e9016-3.15.0a0-b14986c-vs-base-mem.svg)
- [📄table](bm-20250621-vultr-x86_64-python-b14986c91464b06e9016-3.15.0a0-b14986c-vs-base.md)
- [📈time plot](bm-20250621-vultr-x86_64-python-b14986c91464b06e9016-3.15.0a0-b14986c-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15800985329)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250621-macm4pro-arm64-python-b14986c91464b06e9016-3.15.0a0-b14986c.json)

### vs. 3.12.6

- Geometric mean: 1.092x faster (HPT: reliability of 97.16%, 1.00x faster at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250621-macm4pro-arm64-python-b14986c91464b06e9016-3.15.0a0-b14986c-vs-3.12.6.md)
- [📈time plot](bm-20250621-macm4pro-arm64-python-b14986c91464b06e9016-3.15.0a0-b14986c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.013x faster (HPT: reliability of 81.84%, 1.00x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250621-macm4pro-arm64-python-b14986c91464b06e9016-3.15.0a0-b14986c-vs-3.13.0rc2.md)
- [📈time plot](bm-20250621-macm4pro-arm64-python-b14986c91464b06e9016-3.15.0a0-b14986c-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.008x slower (HPT: reliability of 95.27%, 1.00x slower at 99th %ile)
- Memory usage: 1.13x
- [🧠memory plot](bm-20250621-macm4pro-arm64-python-b14986c91464b06e9016-3.15.0a0-b14986c-vs-base-mem.svg)
- [📄table](bm-20250621-macm4pro-arm64-python-b14986c91464b06e9016-3.15.0a0-b14986c-vs-base.md)
- [📈time plot](bm-20250621-macm4pro-arm64-python-b14986c91464b06e9016-3.15.0a0-b14986c-vs-base.svg)

