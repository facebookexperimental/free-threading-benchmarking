# Results

- fork: python/b85e10fd12b2f2517a8e
- version: 3.15.0a1+
- config: NOGIL
- commit hash: [b85e10f](https://github.com/python/cpython/commit/b85e10f)
- commit date: 2025-10-29T21:21:26Z
- commit merge base: [c74793c450249b90dd8aa01889a33b3d236c6aa9](https://github.com/python/cpython/commit/c74793c450249b90dd8aa01889a33b3d236c6aa9)
- commit date: 2025-10-29T21:21:26+00:00
- ref: b85e10fd12b2f2517a8e

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18925989865)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251029-vultr-x86_64-python-b85e10fd12b2f2517a8e-3.15.0a1%2B-b85e10f.json)

### vs. 3.12.6

- Geometric mean: 1.018x slower (HPT: reliability of 88.84%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251029-vultr-x86_64-python-b85e10fd12b2f2517a8e-3.15.0a1%2B-b85e10f-vs-3.12.6.md)
- [📈time plot](bm-20251029-vultr-x86_64-python-b85e10fd12b2f2517a8e-3.15.0a1%2B-b85e10f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.051x slower (HPT: reliability of 93.88%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251029-vultr-x86_64-python-b85e10fd12b2f2517a8e-3.15.0a1%2B-b85e10f-vs-3.13.0rc2.md)
- [📈time plot](bm-20251029-vultr-x86_64-python-b85e10fd12b2f2517a8e-3.15.0a1%2B-b85e10f-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.098x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20251029-vultr-x86_64-python-b85e10fd12b2f2517a8e-3.15.0a1%2B-b85e10f-vs-base-mem.svg)
- [📄table](bm-20251029-vultr-x86_64-python-b85e10fd12b2f2517a8e-3.15.0a1%2B-b85e10f-vs-base.md)
- [📈time plot](bm-20251029-vultr-x86_64-python-b85e10fd12b2f2517a8e-3.15.0a1%2B-b85e10f-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18925989865)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251029-macm4pro-arm64-python-b85e10fd12b2f2517a8e-3.15.0a1%2B-b85e10f.json)

### vs. 3.12.6

- Geometric mean: 1.078x faster (HPT: reliability of 95.07%, 1.00x faster at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251029-macm4pro-arm64-python-b85e10fd12b2f2517a8e-3.15.0a1%2B-b85e10f-vs-3.12.6.md)
- [📈time plot](bm-20251029-macm4pro-arm64-python-b85e10fd12b2f2517a8e-3.15.0a1%2B-b85e10f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.000x slower (HPT: reliability of 73.72%, 1.00x slower at 99th %ile)
- Memory usage: 1.29x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251029-macm4pro-arm64-python-b85e10fd12b2f2517a8e-3.15.0a1%2B-b85e10f-vs-3.13.0rc2.md)
- [📈time plot](bm-20251029-macm4pro-arm64-python-b85e10fd12b2f2517a8e-3.15.0a1%2B-b85e10f-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.030x slower (HPT: reliability of 99.78%, 1.00x slower at 99th %ile)
- Memory usage: 1.13x
- [🧠memory plot](bm-20251029-macm4pro-arm64-python-b85e10fd12b2f2517a8e-3.15.0a1%2B-b85e10f-vs-base-mem.svg)
- [📄table](bm-20251029-macm4pro-arm64-python-b85e10fd12b2f2517a8e-3.15.0a1%2B-b85e10f-vs-base.md)
- [📈time plot](bm-20251029-macm4pro-arm64-python-b85e10fd12b2f2517a8e-3.15.0a1%2B-b85e10f-vs-base.svg)

