# Results

- fork: python/725da50520c5cc3002f6
- version: 3.15.0a0
- config: NOGIL
- commit hash: [725da50](https://github.com/python/cpython/commit/725da50)
- commit date: 2025-06-18T17:57:14-06:00
- commit merge base: [15f2bac02c5e106f04a93ce73fd93cc305253405](https://github.com/python/cpython/commit/15f2bac02c5e106f04a93ce73fd93cc305253405)
- ref: 725da50520c5cc3002f6

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15746475855)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250618-vultr-x86_64-python-725da50520c5cc3002f6-3.15.0a0-725da50.json)

### vs. 3.12.6

- Geometric mean: 1.010x faster (HPT: reliability of 83.13%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250618-vultr-x86_64-python-725da50520c5cc3002f6-3.15.0a0-725da50-vs-3.12.6.md)
- [📈time plot](bm-20250618-vultr-x86_64-python-725da50520c5cc3002f6-3.15.0a0-725da50-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.025x slower (HPT: reliability of 97.59%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250618-vultr-x86_64-python-725da50520c5cc3002f6-3.15.0a0-725da50-vs-3.13.0rc2.md)
- [📈time plot](bm-20250618-vultr-x86_64-python-725da50520c5cc3002f6-3.15.0a0-725da50-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.088x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.22x
- [🧠memory plot](bm-20250618-vultr-x86_64-python-725da50520c5cc3002f6-3.15.0a0-725da50-vs-base-mem.svg)
- [📄table](bm-20250618-vultr-x86_64-python-725da50520c5cc3002f6-3.15.0a0-725da50-vs-base.md)
- [📈time plot](bm-20250618-vultr-x86_64-python-725da50520c5cc3002f6-3.15.0a0-725da50-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/15746475855)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250618-macm4pro-arm64-python-725da50520c5cc3002f6-3.15.0a0-725da50.json)

### vs. 3.12.6

- Geometric mean: 1.090x faster (HPT: reliability of 96.64%, 1.00x faster at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250618-macm4pro-arm64-python-725da50520c5cc3002f6-3.15.0a0-725da50-vs-3.12.6.md)
- [📈time plot](bm-20250618-macm4pro-arm64-python-725da50520c5cc3002f6-3.15.0a0-725da50-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.011x faster (HPT: reliability of 76.43%, 1.00x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250618-macm4pro-arm64-python-725da50520c5cc3002f6-3.15.0a0-725da50-vs-3.13.0rc2.md)
- [📈time plot](bm-20250618-macm4pro-arm64-python-725da50520c5cc3002f6-3.15.0a0-725da50-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.019x slower (HPT: reliability of 98.49%, 1.00x slower at 99th %ile)
- Memory usage: 1.13x
- [🧠memory plot](bm-20250618-macm4pro-arm64-python-725da50520c5cc3002f6-3.15.0a0-725da50-vs-base-mem.svg)
- [📄table](bm-20250618-macm4pro-arm64-python-725da50520c5cc3002f6-3.15.0a0-725da50-vs-base.md)
- [📈time plot](bm-20250618-macm4pro-arm64-python-725da50520c5cc3002f6-3.15.0a0-725da50-vs-base.svg)

