# Results

- fork: python/ac7511062bf8e16ad489
- version: 3.15.0a0
- config: NOGIL
- commit hash: [ac75110](https://github.com/python/cpython/commit/ac75110)
- commit date: 2025-06-01T17:35:58+02:00
- commit merge base: [f806463e16428ea4b379bf547bafa11f43a480ef](https://github.com/python/cpython/commit/f806463e16428ea4b379bf547bafa11f43a480ef)
- ref: ac7511062bf8e16ad489

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15381141267)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250601-vultr-x86_64-python-ac7511062bf8e16ad489-3.15.0a0-ac75110.json)

### vs. 3.12.6

- Geometric mean: 1.016x faster (HPT: reliability of 88.38%, 1.00x slower at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250601-vultr-x86_64-python-ac7511062bf8e16ad489-3.15.0a0-ac75110-vs-3.12.6.md)
- [📈time plot](bm-20250601-vultr-x86_64-python-ac7511062bf8e16ad489-3.15.0a0-ac75110-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.019x slower (HPT: reliability of 95.75%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250601-vultr-x86_64-python-ac7511062bf8e16ad489-3.15.0a0-ac75110-vs-3.13.0rc2.md)
- [📈time plot](bm-20250601-vultr-x86_64-python-ac7511062bf8e16ad489-3.15.0a0-ac75110-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.092x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.22x
- [🧠memory plot](bm-20250601-vultr-x86_64-python-ac7511062bf8e16ad489-3.15.0a0-ac75110-vs-base-mem.svg)
- [📄table](bm-20250601-vultr-x86_64-python-ac7511062bf8e16ad489-3.15.0a0-ac75110-vs-base.md)
- [📈time plot](bm-20250601-vultr-x86_64-python-ac7511062bf8e16ad489-3.15.0a0-ac75110-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15381141267)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250601-macm4pro-arm64-python-ac7511062bf8e16ad489-3.15.0a0-ac75110.json)

### vs. 3.12.6

- Geometric mean: 1.085x faster (HPT: reliability of 96.17%, 1.00x faster at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250601-macm4pro-arm64-python-ac7511062bf8e16ad489-3.15.0a0-ac75110-vs-3.12.6.md)
- [📈time plot](bm-20250601-macm4pro-arm64-python-ac7511062bf8e16ad489-3.15.0a0-ac75110-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.006x faster (HPT: reliability of 81.27%, 1.00x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250601-macm4pro-arm64-python-ac7511062bf8e16ad489-3.15.0a0-ac75110-vs-3.13.0rc2.md)
- [📈time plot](bm-20250601-macm4pro-arm64-python-ac7511062bf8e16ad489-3.15.0a0-ac75110-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.018x slower (HPT: reliability of 99.11%, 1.00x slower at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: 🔴 dask
- [🧠memory plot](bm-20250601-macm4pro-arm64-python-ac7511062bf8e16ad489-3.15.0a0-ac75110-vs-base-mem.svg)
- [📄table](bm-20250601-macm4pro-arm64-python-ac7511062bf8e16ad489-3.15.0a0-ac75110-vs-base.md)
- [📈time plot](bm-20250601-macm4pro-arm64-python-ac7511062bf8e16ad489-3.15.0a0-ac75110-vs-base.svg)

