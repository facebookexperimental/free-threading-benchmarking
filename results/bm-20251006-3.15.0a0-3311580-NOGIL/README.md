# Results

- fork: python/331158065b7426a79121
- version: 3.15.0a0
- config: NOGIL
- commit hash: [3311580](https://github.com/python/cpython/commit/3311580)
- commit date: 2025-10-06T20:41:08+01:00
- commit merge base: [171f787a297ec4b02cfe8b3ebab8374018391f20](https://github.com/python/cpython/commit/171f787a297ec4b02cfe8b3ebab8374018391f20)
- ref: 331158065b7426a79121

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18298247294)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251006-vultr-x86_64-python-331158065b7426a79121-3.15.0a0-3311580.json)

### vs. 3.12.6

- Geometric mean: 1.015x slower (HPT: reliability of 84.65%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251006-vultr-x86_64-python-331158065b7426a79121-3.15.0a0-3311580-vs-3.12.6.md)
- [📈time plot](bm-20251006-vultr-x86_64-python-331158065b7426a79121-3.15.0a0-3311580-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.048x slower (HPT: reliability of 90.40%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251006-vultr-x86_64-python-331158065b7426a79121-3.15.0a0-3311580-vs-3.13.0rc2.md)
- [📈time plot](bm-20251006-vultr-x86_64-python-331158065b7426a79121-3.15.0a0-3311580-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.092x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20251006-vultr-x86_64-python-331158065b7426a79121-3.15.0a0-3311580-vs-base-mem.svg)
- [📄table](bm-20251006-vultr-x86_64-python-331158065b7426a79121-3.15.0a0-3311580-vs-base.md)
- [📈time plot](bm-20251006-vultr-x86_64-python-331158065b7426a79121-3.15.0a0-3311580-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18298247294)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251006-macm4pro-arm64-python-331158065b7426a79121-3.15.0a0-3311580.json)

### vs. 3.12.6

- Geometric mean: 1.076x faster (HPT: reliability of 93.60%, 1.00x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251006-macm4pro-arm64-python-331158065b7426a79121-3.15.0a0-3311580-vs-3.12.6.md)
- [📈time plot](bm-20251006-macm4pro-arm64-python-331158065b7426a79121-3.15.0a0-3311580-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.002x slower (HPT: reliability of 82.14%, 1.00x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251006-macm4pro-arm64-python-331158065b7426a79121-3.15.0a0-3311580-vs-3.13.0rc2.md)
- [📈time plot](bm-20251006-macm4pro-arm64-python-331158065b7426a79121-3.15.0a0-3311580-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.023x slower (HPT: reliability of 99.78%, 1.00x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20251006-macm4pro-arm64-python-331158065b7426a79121-3.15.0a0-3311580-vs-base-mem.svg)
- [📄table](bm-20251006-macm4pro-arm64-python-331158065b7426a79121-3.15.0a0-3311580-vs-base.md)
- [📈time plot](bm-20251006-macm4pro-arm64-python-331158065b7426a79121-3.15.0a0-3311580-vs-base.svg)

