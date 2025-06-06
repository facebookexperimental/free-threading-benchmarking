# Results

- fork: python/883c2f682bab38344bf8
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [883c2f6](https://github.com/python/cpython/commit/883c2f6)
- commit date: 2025-03-20T16:59:41-07:00
- commit merge base: [844765b20f993e69fd6b7b70341f636fb84b473d](https://github.com/python/cpython/commit/844765b20f993e69fd6b7b70341f636fb84b473d)
- ref: 883c2f682bab38344bf8

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13981963596)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250320-vultr-x86_64-python-883c2f682bab38344bf8-3.14.0a6%2B-883c2f6.json)

### vs. 3.12.6

- Geometric mean: 1.040x slower (HPT: reliability of 99.99%, 1.02x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250320-vultr-x86_64-python-883c2f682bab38344bf8-3.14.0a6%2B-883c2f6-vs-3.12.6.md)
- [📈time plot](bm-20250320-vultr-x86_64-python-883c2f682bab38344bf8-3.14.0a6%2B-883c2f6-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.072x slower (HPT: reliability of 99.99%, 1.03x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250320-vultr-x86_64-python-883c2f682bab38344bf8-3.14.0a6%2B-883c2f6-vs-3.13.0rc2.md)
- [📈time plot](bm-20250320-vultr-x86_64-python-883c2f682bab38344bf8-3.14.0a6%2B-883c2f6-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.100x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.21x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250320-vultr-x86_64-python-883c2f682bab38344bf8-3.14.0a6%2B-883c2f6-vs-base-mem.svg)
- [📄table](bm-20250320-vultr-x86_64-python-883c2f682bab38344bf8-3.14.0a6%2B-883c2f6-vs-base.md)
- [📈time plot](bm-20250320-vultr-x86_64-python-883c2f682bab38344bf8-3.14.0a6%2B-883c2f6-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13981963596)
- cpu model: missing
- platform: macOS-15.3.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250320-macm4pro-arm64-python-883c2f682bab38344bf8-3.14.0a6%2B-883c2f6.json)

### vs. 3.12.6

- Geometric mean: 1.010x slower (HPT: reliability of 99.01%, 1.00x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250320-macm4pro-arm64-python-883c2f682bab38344bf8-3.14.0a6%2B-883c2f6-vs-3.12.6.md)
- [📈time plot](bm-20250320-macm4pro-arm64-python-883c2f682bab38344bf8-3.14.0a6%2B-883c2f6-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.082x slower (HPT: reliability of 99.97%, 1.04x slower at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250320-macm4pro-arm64-python-883c2f682bab38344bf8-3.14.0a6%2B-883c2f6-vs-3.13.0rc2.md)
- [📈time plot](bm-20250320-macm4pro-arm64-python-883c2f682bab38344bf8-3.14.0a6%2B-883c2f6-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.035x slower (HPT: reliability of 99.94%, 1.01x slower at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: 🔴 dask
- [🧠memory plot](bm-20250320-macm4pro-arm64-python-883c2f682bab38344bf8-3.14.0a6%2B-883c2f6-vs-base-mem.svg)
- [📄table](bm-20250320-macm4pro-arm64-python-883c2f682bab38344bf8-3.14.0a6%2B-883c2f6-vs-base.md)
- [📈time plot](bm-20250320-macm4pro-arm64-python-883c2f682bab38344bf8-3.14.0a6%2B-883c2f6-vs-base.svg)

