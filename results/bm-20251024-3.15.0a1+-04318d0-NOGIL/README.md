# Results

- fork: kumaraditya303/interp_tls
- version: 3.15.0a1+
- config: NOGIL
- commit hash: [04318d0](https://github.com/kumaraditya303/cpython/commit/04318d0)
- commit date: 2025-10-24T20:31:37+05:30
- commit merge base: [95e5d596308620acbd860ec25a40ef95c2b62eaa](https://github.com/python/cpython/commit/95e5d596308620acbd860ec25a40ef95c2b62eaa)
- ref: interp_tls

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18784042880)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1%2B-04318d0.json)

### vs. 3.12.6

- Geometric mean: 1.016x slower (HPT: reliability of 84.31%, 1.00x slower at 99th %ile)
- Memory usage: 1.42x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1%2B-04318d0-vs-3.12.6.md)
- [📈time plot](bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1%2B-04318d0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.049x slower (HPT: reliability of 96.32%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1%2B-04318d0-vs-3.13.0rc2.md)
- [📈time plot](bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1%2B-04318d0-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.001x slower (HPT: reliability of 76.86%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1%2B-04318d0-vs-base-mem.svg)
- [📄table](bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1%2B-04318d0-vs-base.md)
- [📈time plot](bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1%2B-04318d0-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.090x slower (HPT: reliability of 100.00%, 1.06x slower at 99th %ile)
- Memory usage: 1.20x
- [📄table](bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1%2B-04318d0-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20251024-vultr-x86_64-kumaraditya303-interp_tls-3.15.0a1%2B-04318d0-vs-default_base_vs_NOGIL.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/18784042880)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1%2B-04318d0.json)

### vs. 3.12.6

- Geometric mean: 1.071x faster (HPT: reliability of 92.77%, 1.00x faster at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1%2B-04318d0-vs-3.12.6.md)
- [📈time plot](bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1%2B-04318d0-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.006x slower (HPT: reliability of 78.32%, 1.00x slower at 99th %ile)
- Memory usage: 1.29x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1%2B-04318d0-vs-3.13.0rc2.md)
- [📈time plot](bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1%2B-04318d0-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.004x slower (HPT: reliability of 100.00%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1%2B-04318d0-vs-base-mem.svg)
- [📄table](bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1%2B-04318d0-vs-base.md)
- [📈time plot](bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1%2B-04318d0-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.011x slower (HPT: reliability of 96.81%, 1.00x slower at 99th %ile)
- Memory usage: 1.13x
- [📄table](bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1%2B-04318d0-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1%2B-04318d0-vs-default_base_vs_NOGIL.svg)

