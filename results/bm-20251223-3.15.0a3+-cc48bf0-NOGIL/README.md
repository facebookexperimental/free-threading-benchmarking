# Results

- fork: python/cc48bf0fde8025d60a57
- version: 3.15.0a3+
- config: NOGIL
- commit hash: [cc48bf0](https://github.com/python/cpython/commit/cc48bf0)
- commit date: 2025-12-23T21:47:12Z
- commit merge base: [cbe0cb779ae0b50c5b5653e9279ba451cc9e8557](https://github.com/python/cpython/commit/cbe0cb779ae0b50c5b5653e9279ba451cc9e8557)
- commit date: 2025-12-23T21:47:12+00:00
- ref: cc48bf0fde8025d60a57

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20474810343)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20251223-vultr-x86_64-python-cc48bf0fde8025d60a57-3.15.0a3%2B-cc48bf0.json)

### vs. 3.12.6

- Geometric mean: 1.027x slower (HPT: reliability of 78.28%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251223-vultr-x86_64-python-cc48bf0fde8025d60a57-3.15.0a3%2B-cc48bf0-vs-3.12.6.md)
- [📈time plot](bm-20251223-vultr-x86_64-python-cc48bf0fde8025d60a57-3.15.0a3%2B-cc48bf0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.060x slower (HPT: reliability of 93.08%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251223-vultr-x86_64-python-cc48bf0fde8025d60a57-3.15.0a3%2B-cc48bf0-vs-3.13.0rc2.md)
- [📈time plot](bm-20251223-vultr-x86_64-python-cc48bf0fde8025d60a57-3.15.0a3%2B-cc48bf0-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.093x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20251223-vultr-x86_64-python-cc48bf0fde8025d60a57-3.15.0a3%2B-cc48bf0-vs-base-mem.svg)
- [📄table](bm-20251223-vultr-x86_64-python-cc48bf0fde8025d60a57-3.15.0a3%2B-cc48bf0-vs-base.md)
- [📈time plot](bm-20251223-vultr-x86_64-python-cc48bf0fde8025d60a57-3.15.0a3%2B-cc48bf0-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20474810343)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3%2B-cc48bf0.json)

### vs. 3.12.6

- Geometric mean: 1.093x faster (HPT: reliability of 98.73%, 1.00x faster at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3%2B-cc48bf0-vs-3.12.6.md)
- [📈time plot](bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3%2B-cc48bf0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.013x faster (HPT: reliability of 60.34%, 1.00x slower at 99th %ile)
- Memory usage: 1.29x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3%2B-cc48bf0-vs-3.13.0rc2.md)
- [📈time plot](bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3%2B-cc48bf0-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.045x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3%2B-cc48bf0-vs-base-mem.svg)
- [📄table](bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3%2B-cc48bf0-vs-base.md)
- [📈time plot](bm-20251223-macm4pro-arm64-python-cc48bf0fde8025d60a57-3.15.0a3%2B-cc48bf0-vs-base.svg)

