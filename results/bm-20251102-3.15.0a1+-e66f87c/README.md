# Results

- fork: python/e66f87ca73516efb4aec
- version: 3.15.0a1+
- config: 
- commit hash: [e66f87c](https://github.com/python/cpython/commit/e66f87c)
- commit date: 2025-11-02T15:15:47-08:00
- commit merge base: [31de83d5e2e17f4e9a37e08b384bab916e1da7c1](https://github.com/python/cpython/commit/31de83d5e2e17f4e9a37e08b384bab916e1da7c1)
- ref: e66f87ca73516efb4aec

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19020478409)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1%2B-e66f87c.json)

### vs. 3.12.6

- Geometric mean: 1.079x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1%2B-e66f87c-vs-3.12.6.md)
- [📈time plot](bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1%2B-e66f87c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.043x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1%2B-e66f87c-vs-3.13.0rc2.md)
- [📈time plot](bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1%2B-e66f87c-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19020478409)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251102-macm4pro-arm64-python-e66f87ca73516efb4aec-3.15.0a1%2B-e66f87c.json)

### vs. 3.12.6

- Geometric mean: 1.115x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251102-macm4pro-arm64-python-e66f87ca73516efb4aec-3.15.0a1%2B-e66f87c-vs-3.12.6.md)
- [📈time plot](bm-20251102-macm4pro-arm64-python-e66f87ca73516efb4aec-3.15.0a1%2B-e66f87c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.034x faster (HPT: reliability of 97.18%, 1.00x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251102-macm4pro-arm64-python-e66f87ca73516efb4aec-3.15.0a1%2B-e66f87c-vs-3.13.0rc2.md)
- [📈time plot](bm-20251102-macm4pro-arm64-python-e66f87ca73516efb4aec-3.15.0a1%2B-e66f87c-vs-3.13.0rc2.svg)

