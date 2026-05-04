# Results

- fork: python/3efd2f4db6de0990136a
- version: 3.15.0a8+
- config: NOGIL
- commit hash: [3efd2f4](https://github.com/python/cpython/commit/3efd2f4)
- commit date: 2026-05-04T01:02:33+01:00
- commit merge base: [2e94f14310e8ab62f41dd01276f2c69cb3d36da2](https://github.com/python/cpython/commit/2e94f14310e8ab62f41dd01276f2c69cb3d36da2)
- ref: 3efd2f4db6de0990136a

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/25295846376)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260504-vultr-x86_64-python-3efd2f4db6de0990136a-3.15.0a8%2B-3efd2f4.json)

### vs. 3.12.6

- Geometric mean: 1.022x slower (HPT: reliability of 81.81%, 1.00x slower at 99th %ile)
- Memory usage: 1.41x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260504-vultr-x86_64-python-3efd2f4db6de0990136a-3.15.0a8%2B-3efd2f4-vs-3.12.6.md)
- [📈time plot](bm-20260504-vultr-x86_64-python-3efd2f4db6de0990136a-3.15.0a8%2B-3efd2f4-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.057x slower (HPT: reliability of 94.34%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260504-vultr-x86_64-python-3efd2f4db6de0990136a-3.15.0a8%2B-3efd2f4-vs-3.13.0rc2.md)
- [📈time plot](bm-20260504-vultr-x86_64-python-3efd2f4db6de0990136a-3.15.0a8%2B-3efd2f4-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.082x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20260504-vultr-x86_64-python-3efd2f4db6de0990136a-3.15.0a8%2B-3efd2f4-vs-base-mem.svg)
- [📄table](bm-20260504-vultr-x86_64-python-3efd2f4db6de0990136a-3.15.0a8%2B-3efd2f4-vs-base.md)
- [📈time plot](bm-20260504-vultr-x86_64-python-3efd2f4db6de0990136a-3.15.0a8%2B-3efd2f4-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/25295846376)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260504-macm4pro-arm64-python-3efd2f4db6de0990136a-3.15.0a8%2B-3efd2f4.json)

### vs. 3.12.6

- Geometric mean: 1.111x faster (HPT: reliability of 99.86%, 1.01x faster at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: 2to3, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260504-macm4pro-arm64-python-3efd2f4db6de0990136a-3.15.0a8%2B-3efd2f4-vs-3.12.6.md)
- [📈time plot](bm-20260504-macm4pro-arm64-python-3efd2f4db6de0990136a-3.15.0a8%2B-3efd2f4-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.026x faster (HPT: reliability of 78.78%, 1.00x faster at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: 2to3, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260504-macm4pro-arm64-python-3efd2f4db6de0990136a-3.15.0a8%2B-3efd2f4-vs-3.13.0rc2.md)
- [📈time plot](bm-20260504-macm4pro-arm64-python-3efd2f4db6de0990136a-3.15.0a8%2B-3efd2f4-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.025x slower (HPT: reliability of 96.32%, 1.00x slower at 99th %ile)
- Memory usage: 1.15x
- [🧠memory plot](bm-20260504-macm4pro-arm64-python-3efd2f4db6de0990136a-3.15.0a8%2B-3efd2f4-vs-base-mem.svg)
- [📄table](bm-20260504-macm4pro-arm64-python-3efd2f4db6de0990136a-3.15.0a8%2B-3efd2f4-vs-base.md)
- [📈time plot](bm-20260504-macm4pro-arm64-python-3efd2f4db6de0990136a-3.15.0a8%2B-3efd2f4-vs-base.svg)

