# Results

- fork: python/86513f6c2ebdd1fb692c
- version: 3.15.0a1+
- config: NOGIL
- commit hash: [86513f6](https://github.com/python/cpython/commit/86513f6)
- commit date: 2025-11-10T21:35:47Z
- commit merge base: [ed0a5fd8cacb1964111d03ff37627f6bea5e6026](https://github.com/python/cpython/commit/ed0a5fd8cacb1964111d03ff37627f6bea5e6026)
- commit date: 2025-11-10T21:35:47+00:00
- ref: 86513f6c2ebdd1fb692c

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19250695906)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251110-vultr-x86_64-python-86513f6c2ebdd1fb692c-3.15.0a1%2B-86513f6.json)

### vs. 3.12.6

- Geometric mean: 1.021x slower (HPT: reliability of 84.88%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251110-vultr-x86_64-python-86513f6c2ebdd1fb692c-3.15.0a1%2B-86513f6-vs-3.12.6.md)
- [📈time plot](bm-20251110-vultr-x86_64-python-86513f6c2ebdd1fb692c-3.15.0a1%2B-86513f6-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.054x slower (HPT: reliability of 93.93%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: many_optionals, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251110-vultr-x86_64-python-86513f6c2ebdd1fb692c-3.15.0a1%2B-86513f6-vs-3.13.0rc2.md)
- [📈time plot](bm-20251110-vultr-x86_64-python-86513f6c2ebdd1fb692c-3.15.0a1%2B-86513f6-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.094x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20251110-vultr-x86_64-python-86513f6c2ebdd1fb692c-3.15.0a1%2B-86513f6-vs-base-mem.svg)
- [📄table](bm-20251110-vultr-x86_64-python-86513f6c2ebdd1fb692c-3.15.0a1%2B-86513f6-vs-base.md)
- [📈time plot](bm-20251110-vultr-x86_64-python-86513f6c2ebdd1fb692c-3.15.0a1%2B-86513f6-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19250695906)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1%2B-86513f6.json)

### vs. 3.12.6

- Geometric mean: 1.069x faster (HPT: reliability of 92.52%, 1.00x faster at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1%2B-86513f6-vs-3.12.6.md)
- [📈time plot](bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1%2B-86513f6-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.015x slower (HPT: reliability of 87.86%, 1.00x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1%2B-86513f6-vs-3.13.0rc2.md)
- [📈time plot](bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1%2B-86513f6-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.041x slower (HPT: reliability of 99.99%, 1.01x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1%2B-86513f6-vs-base-mem.svg)
- [📄table](bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1%2B-86513f6-vs-base.md)
- [📈time plot](bm-20251110-macm4pro-arm64-python-86513f6c2ebdd1fb692c-3.15.0a1%2B-86513f6-vs-base.svg)

