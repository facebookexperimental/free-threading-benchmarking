# Results

- fork: python/3dab11f888fda34c0273
- version: 3.15.0a1+
- config: NOGIL
- commit hash: [3dab11f](https://github.com/python/cpython/commit/3dab11f)
- commit date: 2025-10-26T22:35:21Z
- commit merge base: [9d34623eb11c4c6f8ba0ba8eb4e920dd8444be42](https://github.com/python/cpython/commit/9d34623eb11c4c6f8ba0ba8eb4e920dd8444be42)
- commit date: 2025-10-26T22:35:21+00:00
- ref: 3dab11f888fda34c0273

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18826098085)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251026-vultr-x86_64-python-3dab11f888fda34c0273-3.15.0a1%2B-3dab11f.json)

### vs. 3.12.6

- Geometric mean: 1.014x slower (HPT: reliability of 75.96%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251026-vultr-x86_64-python-3dab11f888fda34c0273-3.15.0a1%2B-3dab11f-vs-3.12.6.md)
- [📈time plot](bm-20251026-vultr-x86_64-python-3dab11f888fda34c0273-3.15.0a1%2B-3dab11f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.047x slower (HPT: reliability of 92.82%, 1.00x slower at 99th %ile)
- Memory usage: 1.40x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251026-vultr-x86_64-python-3dab11f888fda34c0273-3.15.0a1%2B-3dab11f-vs-3.13.0rc2.md)
- [📈time plot](bm-20251026-vultr-x86_64-python-3dab11f888fda34c0273-3.15.0a1%2B-3dab11f-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.095x slower (HPT: reliability of 100.00%, 1.07x slower at 99th %ile)
- Memory usage: 1.20x
- [🧠memory plot](bm-20251026-vultr-x86_64-python-3dab11f888fda34c0273-3.15.0a1%2B-3dab11f-vs-base-mem.svg)
- [📄table](bm-20251026-vultr-x86_64-python-3dab11f888fda34c0273-3.15.0a1%2B-3dab11f-vs-base.md)
- [📈time plot](bm-20251026-vultr-x86_64-python-3dab11f888fda34c0273-3.15.0a1%2B-3dab11f-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18826098085)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251026-macm4pro-arm64-python-3dab11f888fda34c0273-3.15.0a1%2B-3dab11f.json)

### vs. 3.12.6

- Geometric mean: 1.079x faster (HPT: reliability of 95.03%, 1.00x faster at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251026-macm4pro-arm64-python-3dab11f888fda34c0273-3.15.0a1%2B-3dab11f-vs-3.12.6.md)
- [📈time plot](bm-20251026-macm4pro-arm64-python-3dab11f888fda34c0273-3.15.0a1%2B-3dab11f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.001x faster (HPT: reliability of 77.33%, 1.00x slower at 99th %ile)
- Memory usage: 1.29x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251026-macm4pro-arm64-python-3dab11f888fda34c0273-3.15.0a1%2B-3dab11f-vs-3.13.0rc2.md)
- [📈time plot](bm-20251026-macm4pro-arm64-python-3dab11f888fda34c0273-3.15.0a1%2B-3dab11f-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.025x slower (HPT: reliability of 99.35%, 1.00x slower at 99th %ile)
- Memory usage: 1.13x
- [🧠memory plot](bm-20251026-macm4pro-arm64-python-3dab11f888fda34c0273-3.15.0a1%2B-3dab11f-vs-base-mem.svg)
- [📄table](bm-20251026-macm4pro-arm64-python-3dab11f888fda34c0273-3.15.0a1%2B-3dab11f-vs-base.md)
- [📈time plot](bm-20251026-macm4pro-arm64-python-3dab11f888fda34c0273-3.15.0a1%2B-3dab11f-vs-base.svg)

