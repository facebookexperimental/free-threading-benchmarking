# Results

- fork: python/448d7b96c181d13ca7f8
- version: 3.15.0a8+
- config: NOGIL
- commit hash: [448d7b9](https://github.com/python/cpython/commit/448d7b9)
- commit date: 2026-04-23T22:07:28+03:00
- commit merge base: [4629c2215a9a4b3d1ec4a306cd4dd7d11dcfebb4](https://github.com/python/cpython/commit/4629c2215a9a4b3d1ec4a306cd4dd7d11dcfebb4)
- ref: 448d7b96c181d13ca7f8

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/24866451116)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260423-vultr-x86_64-python-448d7b96c181d13ca7f8-3.15.0a8%2B-448d7b9.json)

### vs. 3.12.6

- Geometric mean: 1.013x slower (HPT: reliability of 70.61%, 1.00x slower at 99th %ile)
- Memory usage: 1.44x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260423-vultr-x86_64-python-448d7b96c181d13ca7f8-3.15.0a8%2B-448d7b9-vs-3.12.6.md)
- [📈time plot](bm-20260423-vultr-x86_64-python-448d7b96c181d13ca7f8-3.15.0a8%2B-448d7b9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.046x slower (HPT: reliability of 88.38%, 1.00x slower at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260423-vultr-x86_64-python-448d7b96c181d13ca7f8-3.15.0a8%2B-448d7b9-vs-3.13.0rc2.md)
- [📈time plot](bm-20260423-vultr-x86_64-python-448d7b96c181d13ca7f8-3.15.0a8%2B-448d7b9-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.094x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20260423-vultr-x86_64-python-448d7b96c181d13ca7f8-3.15.0a8%2B-448d7b9-vs-base-mem.svg)
- [📄table](bm-20260423-vultr-x86_64-python-448d7b96c181d13ca7f8-3.15.0a8%2B-448d7b9-vs-base.md)
- [📈time plot](bm-20260423-vultr-x86_64-python-448d7b96c181d13ca7f8-3.15.0a8%2B-448d7b9-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/24866451116)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260423-macm4pro-arm64-python-448d7b96c181d13ca7f8-3.15.0a8%2B-448d7b9.json)

### vs. 3.12.6

- Geometric mean: 1.120x faster (HPT: reliability of 99.95%, 1.02x faster at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260423-macm4pro-arm64-python-448d7b96c181d13ca7f8-3.15.0a8%2B-448d7b9-vs-3.12.6.md)
- [📈time plot](bm-20260423-macm4pro-arm64-python-448d7b96c181d13ca7f8-3.15.0a8%2B-448d7b9-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.039x faster (HPT: reliability of 74.80%, 1.00x faster at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260423-macm4pro-arm64-python-448d7b96c181d13ca7f8-3.15.0a8%2B-448d7b9-vs-3.13.0rc2.md)
- [📈time plot](bm-20260423-macm4pro-arm64-python-448d7b96c181d13ca7f8-3.15.0a8%2B-448d7b9-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.049x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: 1.11x
- [🧠memory plot](bm-20260423-macm4pro-arm64-python-448d7b96c181d13ca7f8-3.15.0a8%2B-448d7b9-vs-base-mem.svg)
- [📄table](bm-20260423-macm4pro-arm64-python-448d7b96c181d13ca7f8-3.15.0a8%2B-448d7b9-vs-base.md)
- [📈time plot](bm-20260423-macm4pro-arm64-python-448d7b96c181d13ca7f8-3.15.0a8%2B-448d7b9-vs-base.svg)

