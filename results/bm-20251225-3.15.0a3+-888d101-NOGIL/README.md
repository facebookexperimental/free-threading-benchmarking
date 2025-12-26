# Results

- fork: python/888d101445c72c7cf239
- version: 3.15.0a3+
- config: NOGIL
- commit hash: [888d101](https://github.com/python/cpython/commit/888d101)
- commit date: 2025-12-25T19:21:16Z
- commit merge base: [ea3fd785cbbc422188833358fbc7ff162d8401f2](https://github.com/python/cpython/commit/ea3fd785cbbc422188833358fbc7ff162d8401f2)
- commit date: 2025-12-25T19:21:16+00:00
- ref: 888d101445c72c7cf239

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20513055091)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20251225-vultr-x86_64-python-888d101445c72c7cf239-3.15.0a3%2B-888d101.json)

### vs. 3.12.6

- Geometric mean: 1.030x slower (HPT: reliability of 87.52%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251225-vultr-x86_64-python-888d101445c72c7cf239-3.15.0a3%2B-888d101-vs-3.12.6.md)
- [📈time plot](bm-20251225-vultr-x86_64-python-888d101445c72c7cf239-3.15.0a3%2B-888d101-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.063x slower (HPT: reliability of 97.54%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251225-vultr-x86_64-python-888d101445c72c7cf239-3.15.0a3%2B-888d101-vs-3.13.0rc2.md)
- [📈time plot](bm-20251225-vultr-x86_64-python-888d101445c72c7cf239-3.15.0a3%2B-888d101-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.102x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20251225-vultr-x86_64-python-888d101445c72c7cf239-3.15.0a3%2B-888d101-vs-base-mem.svg)
- [📄table](bm-20251225-vultr-x86_64-python-888d101445c72c7cf239-3.15.0a3%2B-888d101-vs-base.md)
- [📈time plot](bm-20251225-vultr-x86_64-python-888d101445c72c7cf239-3.15.0a3%2B-888d101-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20513055091)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251225-macm4pro-arm64-python-888d101445c72c7cf239-3.15.0a3%2B-888d101.json)

### vs. 3.12.6

- Geometric mean: 1.130x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251225-macm4pro-arm64-python-888d101445c72c7cf239-3.15.0a3%2B-888d101-vs-3.12.6.md)
- [📈time plot](bm-20251225-macm4pro-arm64-python-888d101445c72c7cf239-3.15.0a3%2B-888d101-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.048x faster (HPT: reliability of 90.94%, 1.00x faster at 99th %ile)
- Memory usage: 1.30x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251225-macm4pro-arm64-python-888d101445c72c7cf239-3.15.0a3%2B-888d101-vs-3.13.0rc2.md)
- [📈time plot](bm-20251225-macm4pro-arm64-python-888d101445c72c7cf239-3.15.0a3%2B-888d101-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.060x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: 🔴 dask
- [🧠memory plot](bm-20251225-macm4pro-arm64-python-888d101445c72c7cf239-3.15.0a3%2B-888d101-vs-base-mem.svg)
- [📄table](bm-20251225-macm4pro-arm64-python-888d101445c72c7cf239-3.15.0a3%2B-888d101-vs-base.md)
- [📈time plot](bm-20251225-macm4pro-arm64-python-888d101445c72c7cf239-3.15.0a3%2B-888d101-vs-base.svg)

