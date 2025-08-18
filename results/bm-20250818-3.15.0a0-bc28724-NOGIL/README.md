# Results

- fork: python/bc2872445b2aee4bb4e0
- version: 3.15.0a0
- config: NOGIL
- commit hash: [bc28724](https://github.com/python/cpython/commit/bc28724)
- commit date: 2025-08-18T07:57:15+08:00
- commit merge base: [8e3244d39b8cd3d7cef5a315247d45e801b35869](https://github.com/python/cpython/commit/8e3244d39b8cd3d7cef5a315247d45e801b35869)
- ref: bc2872445b2aee4bb4e0

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17027861921)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250818-vultr-x86_64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724.json)

### vs. 3.12.6

- Geometric mean: 1.026x slower (HPT: reliability of 95.15%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250818-vultr-x86_64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724-vs-3.12.6.md)
- [📈time plot](bm-20250818-vultr-x86_64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.058x slower (HPT: reliability of 97.75%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250818-vultr-x86_64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724-vs-3.13.0rc2.md)
- [📈time plot](bm-20250818-vultr-x86_64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.098x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20250818-vultr-x86_64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724-vs-base-mem.svg)
- [📄table](bm-20250818-vultr-x86_64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724-vs-base.md)
- [📈time plot](bm-20250818-vultr-x86_64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/17027861921)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250818-macm4pro-arm64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724.json)

### vs. 3.12.6

- Geometric mean: 1.080x faster (HPT: reliability of 93.78%, 1.00x faster at 99th %ile)
- Memory usage: 1.26x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250818-macm4pro-arm64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724-vs-3.12.6.md)
- [📈time plot](bm-20250818-macm4pro-arm64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.002x faster (HPT: reliability of 78.97%, 1.00x slower at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250818-macm4pro-arm64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724-vs-3.13.0rc2.md)
- [📈time plot](bm-20250818-macm4pro-arm64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.011x slower (HPT: reliability of 97.74%, 1.00x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20250818-macm4pro-arm64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724-vs-base-mem.svg)
- [📄table](bm-20250818-macm4pro-arm64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724-vs-base.md)
- [📈time plot](bm-20250818-macm4pro-arm64-python-bc2872445b2aee4bb4e0-3.15.0a0-bc28724-vs-base.svg)

