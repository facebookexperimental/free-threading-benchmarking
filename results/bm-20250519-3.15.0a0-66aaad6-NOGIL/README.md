# Results

- fork: python/66aaad61037785639aec
- version: 3.15.0a0
- config: NOGIL
- commit hash: [66aaad6](https://github.com/python/cpython/commit/66aaad6)
- commit date: 2025-05-19T18:59:06-05:00
- commit merge base: [46d7c114d8cd25e5135bcdf2ea799eea43a41a67](https://github.com/python/cpython/commit/46d7c114d8cd25e5135bcdf2ea799eea43a41a67)
- ref: 66aaad61037785639aec

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15126027952)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250519-vultr-x86_64-python-66aaad61037785639aec-3.15.0a0-66aaad6.json)

### vs. 3.12.6

- Geometric mean: 1.010x faster (HPT: reliability of 89.90%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250519-vultr-x86_64-python-66aaad61037785639aec-3.15.0a0-66aaad6-vs-3.12.6.md)
- [📈time plot](bm-20250519-vultr-x86_64-python-66aaad61037785639aec-3.15.0a0-66aaad6-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.025x slower (HPT: reliability of 96.90%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250519-vultr-x86_64-python-66aaad61037785639aec-3.15.0a0-66aaad6-vs-3.13.0rc2.md)
- [📈time plot](bm-20250519-vultr-x86_64-python-66aaad61037785639aec-3.15.0a0-66aaad6-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.097x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.22x
- [🧠memory plot](bm-20250519-vultr-x86_64-python-66aaad61037785639aec-3.15.0a0-66aaad6-vs-base-mem.svg)
- [📄table](bm-20250519-vultr-x86_64-python-66aaad61037785639aec-3.15.0a0-66aaad6-vs-base.md)
- [📈time plot](bm-20250519-vultr-x86_64-python-66aaad61037785639aec-3.15.0a0-66aaad6-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15126027952)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250519-macm4pro-arm64-python-66aaad61037785639aec-3.15.0a0-66aaad6.json)

### vs. 3.12.6

- Geometric mean: 1.073x faster (HPT: reliability of 80.87%, 1.00x faster at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250519-macm4pro-arm64-python-66aaad61037785639aec-3.15.0a0-66aaad6-vs-3.12.6.md)
- [📈time plot](bm-20250519-macm4pro-arm64-python-66aaad61037785639aec-3.15.0a0-66aaad6-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.006x slower (HPT: reliability of 87.46%, 1.00x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250519-macm4pro-arm64-python-66aaad61037785639aec-3.15.0a0-66aaad6-vs-3.13.0rc2.md)
- [📈time plot](bm-20250519-macm4pro-arm64-python-66aaad61037785639aec-3.15.0a0-66aaad6-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.027x slower (HPT: reliability of 99.79%, 1.01x slower at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: 🔴 dask
- [🧠memory plot](bm-20250519-macm4pro-arm64-python-66aaad61037785639aec-3.15.0a0-66aaad6-vs-base-mem.svg)
- [📄table](bm-20250519-macm4pro-arm64-python-66aaad61037785639aec-3.15.0a0-66aaad6-vs-base.md)
- [📈time plot](bm-20250519-macm4pro-arm64-python-66aaad61037785639aec-3.15.0a0-66aaad6-vs-base.svg)

