# Results

- fork: python/47b01da4ccedd9c00fad
- version: 3.15.0a0
- config: NOGIL
- commit hash: [47b01da](https://github.com/python/cpython/commit/47b01da)
- commit date: 2025-07-12T21:15:04+03:00
- commit merge base: [9be3649f5eccfbda1b3c9c3195927951a9ae9b90](https://github.com/python/cpython/commit/9be3649f5eccfbda1b3c9c3195927951a9ae9b90)
- ref: 47b01da4ccedd9c00fad

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16243391313)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json)

### vs. 3.12.6

- Geometric mean: 1.028x slower (HPT: reliability of 95.20%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da-vs-3.12.6.md)
- [📈time plot](bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.060x slower (HPT: reliability of 97.03%, 1.00x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da-vs-3.13.0rc2.md)
- [📈time plot](bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.096x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da-vs-base-mem.svg)
- [📄table](bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da-vs-base.md)
- [📈time plot](bm-20250712-vultr-x86_64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/16243391313)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json)

### vs. 3.12.6

- Geometric mean: 1.090x faster (HPT: reliability of 96.07%, 1.00x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da-vs-3.12.6.md)
- [📈time plot](bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.011x faster (HPT: reliability of 85.32%, 1.00x slower at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da-vs-3.13.0rc2.md)
- [📈time plot](bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.012x slower (HPT: reliability of 98.73%, 1.00x slower at 99th %ile)
- Memory usage: 1.11x
- [🧠memory plot](bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da-vs-base-mem.svg)
- [📄table](bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da-vs-base.md)
- [📈time plot](bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da-vs-base.svg)

