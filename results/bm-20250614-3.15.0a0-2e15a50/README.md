# Results

- fork: python/2e15a50851da66eb8227
- version: 3.15.0a0
- config: 
- commit hash: [2e15a50](https://github.com/python/cpython/commit/2e15a50)
- commit date: 2025-06-14T16:04:16Z
- commit merge base: [fc413ecb8f4bf1c59b29932695e3538548eb1a8a](https://github.com/python/cpython/commit/fc413ecb8f4bf1c59b29932695e3538548eb1a8a)
- commit date: 2025-06-14T16:04:16+00:00
- ref: 2e15a50851da66eb8227

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15657462322)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [pystats raw](bm-20250614-vultr-x86_64-python-2e15a50851da66eb8227-3.15.0a0-2e15a50-pystats.json)
- [pystats table](bm-20250614-vultr-x86_64-python-2e15a50851da66eb8227-3.15.0a0-2e15a50-pystats.md)
- [raw results](bm-20250614-vultr-x86_64-python-2e15a50851da66eb8227-3.15.0a0-2e15a50.json)

### vs. 3.12.6

- Geometric mean: 1.112x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250614-vultr-x86_64-python-2e15a50851da66eb8227-3.15.0a0-2e15a50-vs-3.12.6.md)
- [📈time plot](bm-20250614-vultr-x86_64-python-2e15a50851da66eb8227-3.15.0a0-2e15a50-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.074x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250614-vultr-x86_64-python-2e15a50851da66eb8227-3.15.0a0-2e15a50-vs-3.13.0rc2.md)
- [📈time plot](bm-20250614-vultr-x86_64-python-2e15a50851da66eb8227-3.15.0a0-2e15a50-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15657462322)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250614-macm4pro-arm64-python-2e15a50851da66eb8227-3.15.0a0-2e15a50.json)

### vs. 3.12.6

- Geometric mean: 1.105x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250614-macm4pro-arm64-python-2e15a50851da66eb8227-3.15.0a0-2e15a50-vs-3.12.6.md)
- [📈time plot](bm-20250614-macm4pro-arm64-python-2e15a50851da66eb8227-3.15.0a0-2e15a50-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.025x faster (HPT: reliability of 72.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.09x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250614-macm4pro-arm64-python-2e15a50851da66eb8227-3.15.0a0-2e15a50-vs-3.13.0rc2.md)
- [📈time plot](bm-20250614-macm4pro-arm64-python-2e15a50851da66eb8227-3.15.0a0-2e15a50-vs-3.13.0rc2.svg)

