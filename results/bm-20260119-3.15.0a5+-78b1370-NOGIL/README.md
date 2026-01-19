# Results

- fork: python/78b1370de96bab5eee82
- version: 3.15.0a5+
- config: NOGIL
- commit hash: [78b1370](https://github.com/python/cpython/commit/78b1370)
- commit date: 2026-01-19T00:28:38+02:00
- commit merge base: [c879b2a7a52549dd310aa1cca1a00ff8f36a25ba](https://github.com/python/cpython/commit/c879b2a7a52549dd310aa1cca1a00ff8f36a25ba)
- ref: 78b1370de96bab5eee82

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21121397975)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260119-vultr-x86_64-python-78b1370de96bab5eee82-3.15.0a5%2B-78b1370.json)

### vs. 3.12.6

- Geometric mean: 1.030x slower (HPT: reliability of 81.89%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260119-vultr-x86_64-python-78b1370de96bab5eee82-3.15.0a5%2B-78b1370-vs-3.12.6.md)
- [📈time plot](bm-20260119-vultr-x86_64-python-78b1370de96bab5eee82-3.15.0a5%2B-78b1370-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.063x slower (HPT: reliability of 92.28%, 1.00x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260119-vultr-x86_64-python-78b1370de96bab5eee82-3.15.0a5%2B-78b1370-vs-3.13.0rc2.md)
- [📈time plot](bm-20260119-vultr-x86_64-python-78b1370de96bab5eee82-3.15.0a5%2B-78b1370-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.106x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20260119-vultr-x86_64-python-78b1370de96bab5eee82-3.15.0a5%2B-78b1370-vs-base-mem.svg)
- [📄table](bm-20260119-vultr-x86_64-python-78b1370de96bab5eee82-3.15.0a5%2B-78b1370-vs-base.md)
- [📈time plot](bm-20260119-vultr-x86_64-python-78b1370de96bab5eee82-3.15.0a5%2B-78b1370-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21121397975)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260119-macm4pro-arm64-python-78b1370de96bab5eee82-3.15.0a5%2B-78b1370.json)

### vs. 3.12.6

- Geometric mean: 1.120x faster (HPT: reliability of 99.99%, 1.02x faster at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260119-macm4pro-arm64-python-78b1370de96bab5eee82-3.15.0a5%2B-78b1370-vs-3.12.6.md)
- [📈time plot](bm-20260119-macm4pro-arm64-python-78b1370de96bab5eee82-3.15.0a5%2B-78b1370-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.039x faster (HPT: reliability of 79.71%, 1.00x faster at 99th %ile)
- Memory usage: 1.30x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260119-macm4pro-arm64-python-78b1370de96bab5eee82-3.15.0a5%2B-78b1370-vs-3.13.0rc2.md)
- [📈time plot](bm-20260119-macm4pro-arm64-python-78b1370de96bab5eee82-3.15.0a5%2B-78b1370-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.056x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.11x
- [🧠memory plot](bm-20260119-macm4pro-arm64-python-78b1370de96bab5eee82-3.15.0a5%2B-78b1370-vs-base-mem.svg)
- [📄table](bm-20260119-macm4pro-arm64-python-78b1370de96bab5eee82-3.15.0a5%2B-78b1370-vs-base.md)
- [📈time plot](bm-20260119-macm4pro-arm64-python-78b1370de96bab5eee82-3.15.0a5%2B-78b1370-vs-base.svg)

