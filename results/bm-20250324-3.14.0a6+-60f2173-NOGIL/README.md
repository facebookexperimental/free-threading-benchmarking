# Results

- fork: Yhg1s/uniqref_critsection
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [60f2173](https://github.com/Yhg1s/cpython/commit/60f2173)
- commit date: 2025-03-24T13:35:38+01:00
- commit merge base: [af29d5cfd19bf2656955b9bb782cc89c7aa7000f](https://github.com/python/cpython/commit/af29d5cfd19bf2656955b9bb782cc89c7aa7000f)
- ref: uniqref_critsection

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14035454086)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250324-vultr-x86_64-Yhg1s-uniqref_critsection-3.14.0a6%2B-60f2173.json)

### vs. 3.12.6

- Geometric mean: 1.041x slower (HPT: reliability of 99.98%, 1.02x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250324-vultr-x86_64-Yhg1s-uniqref_critsection-3.14.0a6%2B-60f2173-vs-3.12.6.md)
- [📈time plot](bm-20250324-vultr-x86_64-Yhg1s-uniqref_critsection-3.14.0a6%2B-60f2173-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.073x slower (HPT: reliability of 99.98%, 1.03x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250324-vultr-x86_64-Yhg1s-uniqref_critsection-3.14.0a6%2B-60f2173-vs-3.13.0rc2.md)
- [📈time plot](bm-20250324-vultr-x86_64-Yhg1s-uniqref_critsection-3.14.0a6%2B-60f2173-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14035449911)
- cpu model: missing
- platform: macOS-15.3.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250324-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6%2B-60f2173.json)

### vs. 3.12.6

- Geometric mean: 1.015x slower (HPT: reliability of 99.44%, 1.00x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250324-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6%2B-60f2173-vs-3.12.6.md)
- [📈time plot](bm-20250324-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6%2B-60f2173-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.086x slower (HPT: reliability of 99.98%, 1.05x slower at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250324-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6%2B-60f2173-vs-3.13.0rc2.md)
- [📈time plot](bm-20250324-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6%2B-60f2173-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.005x faster (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20250324-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6%2B-60f2173-vs-base-mem.svg)
- [📄table](bm-20250324-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6%2B-60f2173-vs-base.md)
- [📈time plot](bm-20250324-macm4pro-arm64-Yhg1s-uniqref_critsection-3.14.0a6%2B-60f2173-vs-base.svg)

