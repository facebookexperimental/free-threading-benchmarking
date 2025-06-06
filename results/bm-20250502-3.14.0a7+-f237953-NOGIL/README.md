# Results

- fork: python/f2379535fe2d2219b716
- version: 3.14.0a7+
- config: NOGIL
- commit hash: [f237953](https://github.com/python/cpython/commit/f237953)
- commit date: 2025-05-02T13:24:57Z
- commit merge base: [4701ff92d747002d04b67688c7a581b1952773ac](https://github.com/python/cpython/commit/4701ff92d747002d04b67688c7a581b1952773ac)
- commit date: 2025-05-02T13:24:57+00:00
- ref: f2379535fe2d2219b716

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14796977487)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250502-vultr-x86_64-python-f2379535fe2d2219b716-3.14.0a7%2B-f237953.json)

### vs. 3.12.6

- Geometric mean: 1.015x faster (HPT: reliability of 86.32%, 1.00x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250502-vultr-x86_64-python-f2379535fe2d2219b716-3.14.0a7%2B-f237953-vs-3.12.6.md)
- [📈time plot](bm-20250502-vultr-x86_64-python-f2379535fe2d2219b716-3.14.0a7%2B-f237953-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.018x slower (HPT: reliability of 96.07%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250502-vultr-x86_64-python-f2379535fe2d2219b716-3.14.0a7%2B-f237953-vs-3.13.0rc2.md)
- [📈time plot](bm-20250502-vultr-x86_64-python-f2379535fe2d2219b716-3.14.0a7%2B-f237953-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.095x slower (HPT: reliability of 100.00%, 1.08x slower at 99th %ile)
- Memory usage: 1.20x
- new benchmarks: html5lib
- [🧠memory plot](bm-20250502-vultr-x86_64-python-f2379535fe2d2219b716-3.14.0a7%2B-f237953-vs-base-mem.svg)
- [📄table](bm-20250502-vultr-x86_64-python-f2379535fe2d2219b716-3.14.0a7%2B-f237953-vs-base.md)
- [📈time plot](bm-20250502-vultr-x86_64-python-f2379535fe2d2219b716-3.14.0a7%2B-f237953-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14796977487)
- cpu model: missing
- platform: macOS-15.4.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250502-macm4pro-arm64-python-f2379535fe2d2219b716-3.14.0a7%2B-f237953.json)

### vs. 3.12.6

- Geometric mean: 1.073x faster (HPT: reliability of 81.25%, 1.00x faster at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250502-macm4pro-arm64-python-f2379535fe2d2219b716-3.14.0a7%2B-f237953-vs-3.12.6.md)
- [📈time plot](bm-20250502-macm4pro-arm64-python-f2379535fe2d2219b716-3.14.0a7%2B-f237953-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.005x slower (HPT: reliability of 93.83%, 1.00x slower at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250502-macm4pro-arm64-python-f2379535fe2d2219b716-3.14.0a7%2B-f237953-vs-3.13.0rc2.md)
- [📈time plot](bm-20250502-macm4pro-arm64-python-f2379535fe2d2219b716-3.14.0a7%2B-f237953-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.019x slower (HPT: reliability of 99.63%, 1.00x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20250502-macm4pro-arm64-python-f2379535fe2d2219b716-3.14.0a7%2B-f237953-vs-base-mem.svg)
- [📄table](bm-20250502-macm4pro-arm64-python-f2379535fe2d2219b716-3.14.0a7%2B-f237953-vs-base.md)
- [📈time plot](bm-20250502-macm4pro-arm64-python-f2379535fe2d2219b716-3.14.0a7%2B-f237953-vs-base.svg)

