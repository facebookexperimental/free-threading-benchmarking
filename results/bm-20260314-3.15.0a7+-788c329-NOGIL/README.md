# Results

- fork: python/788c3291172b55efa7cf
- version: 3.15.0a7+
- config: NOGIL
- commit hash: [788c329](https://github.com/python/cpython/commit/788c329)
- commit date: 2026-03-14T11:28:49-07:00
- commit merge base: [31c41a61f1afb7929d2698e48894264d8e2df86b](https://github.com/python/cpython/commit/31c41a61f1afb7929d2698e48894264d8e2df86b)
- ref: 788c3291172b55efa7cf

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/23099572549)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260314-vultr-x86_64-python-788c3291172b55efa7cf-3.15.0a7%2B-788c329.json)

### vs. 3.12.6

- Geometric mean: 1.022x slower (HPT: reliability of 60.77%, 1.00x slower at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260314-vultr-x86_64-python-788c3291172b55efa7cf-3.15.0a7%2B-788c329-vs-3.12.6.md)
- [📈time plot](bm-20260314-vultr-x86_64-python-788c3291172b55efa7cf-3.15.0a7%2B-788c329-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.055x slower (HPT: reliability of 87.61%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260314-vultr-x86_64-python-788c3291172b55efa7cf-3.15.0a7%2B-788c329-vs-3.13.0rc2.md)
- [📈time plot](bm-20260314-vultr-x86_64-python-788c3291172b55efa7cf-3.15.0a7%2B-788c329-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.092x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20260314-vultr-x86_64-python-788c3291172b55efa7cf-3.15.0a7%2B-788c329-vs-base-mem.svg)
- [📄table](bm-20260314-vultr-x86_64-python-788c3291172b55efa7cf-3.15.0a7%2B-788c329-vs-base.md)
- [📈time plot](bm-20260314-vultr-x86_64-python-788c3291172b55efa7cf-3.15.0a7%2B-788c329-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/23099572549)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260314-macm4pro-arm64-python-788c3291172b55efa7cf-3.15.0a7%2B-788c329.json)

### vs. 3.12.6

- Geometric mean: 1.101x faster (HPT: reliability of 99.86%, 1.01x faster at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260314-macm4pro-arm64-python-788c3291172b55efa7cf-3.15.0a7%2B-788c329-vs-3.12.6.md)
- [📈time plot](bm-20260314-macm4pro-arm64-python-788c3291172b55efa7cf-3.15.0a7%2B-788c329-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.021x faster (HPT: reliability of 57.94%, 1.00x faster at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260314-macm4pro-arm64-python-788c3291172b55efa7cf-3.15.0a7%2B-788c329-vs-3.13.0rc2.md)
- [📈time plot](bm-20260314-macm4pro-arm64-python-788c3291172b55efa7cf-3.15.0a7%2B-788c329-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.060x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20260314-macm4pro-arm64-python-788c3291172b55efa7cf-3.15.0a7%2B-788c329-vs-base-mem.svg)
- [📄table](bm-20260314-macm4pro-arm64-python-788c3291172b55efa7cf-3.15.0a7%2B-788c329-vs-base.md)
- [📈time plot](bm-20260314-macm4pro-arm64-python-788c3291172b55efa7cf-3.15.0a7%2B-788c329-vs-base.svg)

