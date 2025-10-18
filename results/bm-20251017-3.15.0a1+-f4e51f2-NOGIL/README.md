# Results

- fork: python/f4e51f253ad6c2758343
- version: 3.15.0a1+
- config: NOGIL
- commit hash: [f4e51f2](https://github.com/python/cpython/commit/f4e51f2)
- commit date: 2025-10-17T21:57:51Z
- commit merge base: [92025ea2c8a10aa0e3dd5a2a1548f9bb17fe7dbc](https://github.com/python/cpython/commit/92025ea2c8a10aa0e3dd5a2a1548f9bb17fe7dbc)
- commit date: 2025-10-17T21:57:51+00:00
- ref: f4e51f253ad6c2758343

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18607953265)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251017-vultr-x86_64-python-f4e51f253ad6c2758343-3.15.0a1%2B-f4e51f2.json)

### vs. 3.12.6

- Geometric mean: 1.018x slower (HPT: reliability of 83.84%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251017-vultr-x86_64-python-f4e51f253ad6c2758343-3.15.0a1%2B-f4e51f2-vs-3.12.6.md)
- [📈time plot](bm-20251017-vultr-x86_64-python-f4e51f253ad6c2758343-3.15.0a1%2B-f4e51f2-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.052x slower (HPT: reliability of 94.38%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251017-vultr-x86_64-python-f4e51f253ad6c2758343-3.15.0a1%2B-f4e51f2-vs-3.13.0rc2.md)
- [📈time plot](bm-20251017-vultr-x86_64-python-f4e51f253ad6c2758343-3.15.0a1%2B-f4e51f2-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.088x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20251017-vultr-x86_64-python-f4e51f253ad6c2758343-3.15.0a1%2B-f4e51f2-vs-base-mem.svg)
- [📄table](bm-20251017-vultr-x86_64-python-f4e51f253ad6c2758343-3.15.0a1%2B-f4e51f2-vs-base.md)
- [📈time plot](bm-20251017-vultr-x86_64-python-f4e51f253ad6c2758343-3.15.0a1%2B-f4e51f2-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18607953265)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251017-macm4pro-arm64-python-f4e51f253ad6c2758343-3.15.0a1%2B-f4e51f2.json)

### vs. 3.12.6

- Geometric mean: 1.093x faster (HPT: reliability of 98.73%, 1.00x faster at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251017-macm4pro-arm64-python-f4e51f253ad6c2758343-3.15.0a1%2B-f4e51f2-vs-3.12.6.md)
- [📈time plot](bm-20251017-macm4pro-arm64-python-f4e51f253ad6c2758343-3.15.0a1%2B-f4e51f2-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.014x faster (HPT: reliability of 59.96%, 1.00x slower at 99th %ile)
- Memory usage: 1.30x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251017-macm4pro-arm64-python-f4e51f253ad6c2758343-3.15.0a1%2B-f4e51f2-vs-3.13.0rc2.md)
- [📈time plot](bm-20251017-macm4pro-arm64-python-f4e51f253ad6c2758343-3.15.0a1%2B-f4e51f2-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.025x slower (HPT: reliability of 99.75%, 1.01x slower at 99th %ile)
- Memory usage: 1.15x
- [🧠memory plot](bm-20251017-macm4pro-arm64-python-f4e51f253ad6c2758343-3.15.0a1%2B-f4e51f2-vs-base-mem.svg)
- [📄table](bm-20251017-macm4pro-arm64-python-f4e51f253ad6c2758343-3.15.0a1%2B-f4e51f2-vs-base.md)
- [📈time plot](bm-20251017-macm4pro-arm64-python-f4e51f253ad6c2758343-3.15.0a1%2B-f4e51f2-vs-base.svg)

