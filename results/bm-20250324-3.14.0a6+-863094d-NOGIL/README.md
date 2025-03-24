# Results

- fork: Yhg1s/frame_threadsafety
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [863094d](https://github.com/Yhg1s/cpython/commit/863094d)
- commit date: 2025-03-24T02:04:52+01:00
- commit merge base: [d3f6063af18a008e316e4342492e877ee51463e2](https://github.com/python/cpython/commit/d3f6063af18a008e316e4342492e877ee51463e2)
- ref: frame_threadsafety

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14025027080)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250324-vultr-x86_64-Yhg1s-frame_threadsafety-3.14.0a6%2B-863094d.json)

### vs. 3.12.6

- Geometric mean: 1.049x slower (HPT: reliability of 99.99%, 1.03x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250324-vultr-x86_64-Yhg1s-frame_threadsafety-3.14.0a6%2B-863094d-vs-3.12.6.md)
- [📈time plot](bm-20250324-vultr-x86_64-Yhg1s-frame_threadsafety-3.14.0a6%2B-863094d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.080x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250324-vultr-x86_64-Yhg1s-frame_threadsafety-3.14.0a6%2B-863094d-vs-3.13.0rc2.md)
- [📈time plot](bm-20250324-vultr-x86_64-Yhg1s-frame_threadsafety-3.14.0a6%2B-863094d-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14025024588)
- cpu model: missing
- platform: macOS-15.3.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250324-macm4pro-arm64-Yhg1s-frame_threadsafety-3.14.0a6%2B-863094d.json)

### vs. 3.12.6

- Geometric mean: 1.021x slower (HPT: reliability of 99.82%, 1.01x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250324-macm4pro-arm64-Yhg1s-frame_threadsafety-3.14.0a6%2B-863094d-vs-3.12.6.md)
- [📈time plot](bm-20250324-macm4pro-arm64-Yhg1s-frame_threadsafety-3.14.0a6%2B-863094d-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.091x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250324-macm4pro-arm64-Yhg1s-frame_threadsafety-3.14.0a6%2B-863094d-vs-3.13.0rc2.md)
- [📈time plot](bm-20250324-macm4pro-arm64-Yhg1s-frame_threadsafety-3.14.0a6%2B-863094d-vs-3.13.0rc2.svg)

