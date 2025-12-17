# Results

- fork: python/89729f2ef7f9473d9e4b
- version: 3.15.0a3+
- config: NOGIL
- commit hash: [89729f2](https://github.com/python/cpython/commit/89729f2)
- commit date: 2025-12-17T00:12:32+00:00
- commit merge base: [434525398196db692196661d15e678b3d514aa54](https://github.com/python/cpython/commit/434525398196db692196661d15e678b3d514aa54)
- ref: 89729f2ef7f9473d9e4b

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20287346144)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20251217-vultr-x86_64-python-89729f2ef7f9473d9e4b-3.15.0a3%2B-89729f2.json)

### vs. 3.12.6

- Geometric mean: 1.021x slower (HPT: reliability of 73.67%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251217-vultr-x86_64-python-89729f2ef7f9473d9e4b-3.15.0a3%2B-89729f2-vs-3.12.6.md)
- [📈time plot](bm-20251217-vultr-x86_64-python-89729f2ef7f9473d9e4b-3.15.0a3%2B-89729f2-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.055x slower (HPT: reliability of 93.27%, 1.00x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251217-vultr-x86_64-python-89729f2ef7f9473d9e4b-3.15.0a3%2B-89729f2-vs-3.13.0rc2.md)
- [📈time plot](bm-20251217-vultr-x86_64-python-89729f2ef7f9473d9e4b-3.15.0a3%2B-89729f2-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.098x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20251217-vultr-x86_64-python-89729f2ef7f9473d9e4b-3.15.0a3%2B-89729f2-vs-base-mem.svg)
- [📄table](bm-20251217-vultr-x86_64-python-89729f2ef7f9473d9e4b-3.15.0a3%2B-89729f2-vs-base.md)
- [📈time plot](bm-20251217-vultr-x86_64-python-89729f2ef7f9473d9e4b-3.15.0a3%2B-89729f2-vs-base.svg)

