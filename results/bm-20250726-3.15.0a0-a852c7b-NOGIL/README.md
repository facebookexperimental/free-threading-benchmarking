# Results

- fork: python/a852c7bdd48979218a0c
- version: 3.15.0a0
- config: NOGIL
- commit hash: [a852c7b](https://github.com/python/cpython/commit/a852c7b)
- commit date: 2025-07-26T18:01:51+01:00
- commit merge base: [d5fa437dfb50e2e47632cdc994e3257608688f30](https://github.com/python/cpython/commit/d5fa437dfb50e2e47632cdc994e3257608688f30)
- ref: a852c7bdd48979218a0c

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16545280060)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250726-vultr-x86_64-python-a852c7bdd48979218a0c-3.15.0a0-a852c7b.json)

### vs. 3.12.6

- Geometric mean: 1.027x slower (HPT: reliability of 97.25%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250726-vultr-x86_64-python-a852c7bdd48979218a0c-3.15.0a0-a852c7b-vs-3.12.6.md)
- [📈time plot](bm-20250726-vultr-x86_64-python-a852c7bdd48979218a0c-3.15.0a0-a852c7b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.060x slower (HPT: reliability of 96.86%, 1.00x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250726-vultr-x86_64-python-a852c7bdd48979218a0c-3.15.0a0-a852c7b-vs-3.13.0rc2.md)
- [📈time plot](bm-20250726-vultr-x86_64-python-a852c7bdd48979218a0c-3.15.0a0-a852c7b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.096x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20250726-vultr-x86_64-python-a852c7bdd48979218a0c-3.15.0a0-a852c7b-vs-base-mem.svg)
- [📄table](bm-20250726-vultr-x86_64-python-a852c7bdd48979218a0c-3.15.0a0-a852c7b-vs-base.md)
- [📈time plot](bm-20250726-vultr-x86_64-python-a852c7bdd48979218a0c-3.15.0a0-a852c7b-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16545280060)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250726-macm4pro-arm64-python-a852c7bdd48979218a0c-3.15.0a0-a852c7b.json)

### vs. 3.12.6

- Geometric mean: 1.087x faster (HPT: reliability of 96.50%, 1.00x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250726-macm4pro-arm64-python-a852c7bdd48979218a0c-3.15.0a0-a852c7b-vs-3.12.6.md)
- [📈time plot](bm-20250726-macm4pro-arm64-python-a852c7bdd48979218a0c-3.15.0a0-a852c7b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.008x faster (HPT: reliability of 67.87%, 1.00x slower at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250726-macm4pro-arm64-python-a852c7bdd48979218a0c-3.15.0a0-a852c7b-vs-3.13.0rc2.md)
- [📈time plot](bm-20250726-macm4pro-arm64-python-a852c7bdd48979218a0c-3.15.0a0-a852c7b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.010x slower (HPT: reliability of 96.33%, 1.00x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20250726-macm4pro-arm64-python-a852c7bdd48979218a0c-3.15.0a0-a852c7b-vs-base-mem.svg)
- [📄table](bm-20250726-macm4pro-arm64-python-a852c7bdd48979218a0c-3.15.0a0-a852c7b-vs-base.md)
- [📈time plot](bm-20250726-macm4pro-arm64-python-a852c7bdd48979218a0c-3.15.0a0-a852c7b-vs-base.svg)

