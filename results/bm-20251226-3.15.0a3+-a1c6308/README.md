# Results

- fork: python/a1c630834649d54ffbca
- version: 3.15.0a3+
- config: 
- commit hash: [a1c6308](https://github.com/python/cpython/commit/a1c6308)
- commit date: 2025-12-26T20:30:02Z
- commit merge base: [b3f2d80569185be470e30ddb158f711143187dbf](https://github.com/python/cpython/commit/b3f2d80569185be470e30ddb158f711143187dbf)
- commit date: 2025-12-26T20:30:02+00:00
- ref: a1c630834649d54ffbca

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20531829850)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20251226-vultr-x86_64-python-a1c630834649d54ffbca-3.15.0a3%2B-a1c6308.json)

### vs. 3.12.6

- Geometric mean: 1.079x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251226-vultr-x86_64-python-a1c630834649d54ffbca-3.15.0a3%2B-a1c6308-vs-3.12.6.md)
- [📈time plot](bm-20251226-vultr-x86_64-python-a1c630834649d54ffbca-3.15.0a3%2B-a1c6308-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.043x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251226-vultr-x86_64-python-a1c630834649d54ffbca-3.15.0a3%2B-a1c6308-vs-3.13.0rc2.md)
- [📈time plot](bm-20251226-vultr-x86_64-python-a1c630834649d54ffbca-3.15.0a3%2B-a1c6308-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20531829850)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3%2B-a1c6308.json)

### vs. 3.12.6

- Geometric mean: 1.167x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3%2B-a1c6308-vs-3.12.6.md)
- [📈time plot](bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3%2B-a1c6308-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.082x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3%2B-a1c6308-vs-3.13.0rc2.md)
- [📈time plot](bm-20251226-macm4pro-arm64-python-a1c630834649d54ffbca-3.15.0a3%2B-a1c6308-vs-3.13.0rc2.svg)

