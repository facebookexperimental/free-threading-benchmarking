# Results

- fork: python/e64395e8eb8d3a9e35e3
- version: 3.15.0a0
- config: NOGIL
- commit hash: [e64395e](https://github.com/python/cpython/commit/e64395e)
- commit date: 2025-05-28T18:15:39-05:00
- commit merge base: [e9d845b41dca9ad84b76ef777d05e647a4b4d8cd](https://github.com/python/cpython/commit/e9d845b41dca9ad84b76ef777d05e647a4b4d8cd)
- ref: e64395e8eb8d3a9e35e3

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15313413014)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250528-vultr-x86_64-python-e64395e8eb8d3a9e35e3-3.15.0a0-e64395e.json)

### vs. 3.12.6

- Geometric mean: 1.018x faster (HPT: reliability of 83.13%, 1.00x slower at 99th %ile)
- Memory usage: 1.44x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250528-vultr-x86_64-python-e64395e8eb8d3a9e35e3-3.15.0a0-e64395e-vs-3.12.6.md)
- [📈time plot](bm-20250528-vultr-x86_64-python-e64395e8eb8d3a9e35e3-3.15.0a0-e64395e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.017x slower (HPT: reliability of 92.07%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250528-vultr-x86_64-python-e64395e8eb8d3a9e35e3-3.15.0a0-e64395e-vs-3.13.0rc2.md)
- [📈time plot](bm-20250528-vultr-x86_64-python-e64395e8eb8d3a9e35e3-3.15.0a0-e64395e-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.086x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.23x
- [🧠memory plot](bm-20250528-vultr-x86_64-python-e64395e8eb8d3a9e35e3-3.15.0a0-e64395e-vs-base-mem.svg)
- [📄table](bm-20250528-vultr-x86_64-python-e64395e8eb8d3a9e35e3-3.15.0a0-e64395e-vs-base.md)
- [📈time plot](bm-20250528-vultr-x86_64-python-e64395e8eb8d3a9e35e3-3.15.0a0-e64395e-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15313413014)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250528-macm4pro-arm64-python-e64395e8eb8d3a9e35e3-3.15.0a0-e64395e.json)

### vs. 3.12.6

- Geometric mean: 1.096x faster (HPT: reliability of 99.21%, 1.00x faster at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250528-macm4pro-arm64-python-e64395e8eb8d3a9e35e3-3.15.0a0-e64395e-vs-3.12.6.md)
- [📈time plot](bm-20250528-macm4pro-arm64-python-e64395e8eb8d3a9e35e3-3.15.0a0-e64395e-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.016x faster (HPT: reliability of 59.90%, 1.00x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250528-macm4pro-arm64-python-e64395e8eb8d3a9e35e3-3.15.0a0-e64395e-vs-3.13.0rc2.md)
- [📈time plot](bm-20250528-macm4pro-arm64-python-e64395e8eb8d3a9e35e3-3.15.0a0-e64395e-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.018x slower (HPT: reliability of 99.46%, 1.00x slower at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: 🔴 dask
- [🧠memory plot](bm-20250528-macm4pro-arm64-python-e64395e8eb8d3a9e35e3-3.15.0a0-e64395e-vs-base-mem.svg)
- [📄table](bm-20250528-macm4pro-arm64-python-e64395e8eb8d3a9e35e3-3.15.0a0-e64395e-vs-base.md)
- [📈time plot](bm-20250528-macm4pro-arm64-python-e64395e8eb8d3a9e35e3-3.15.0a0-e64395e-vs-base.svg)

