# Results

- fork: python/4f325168048fda89cef8
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [4f32516](https://github.com/python/cpython/commit/4f32516)
- commit date: 2025-03-21T11:10:07-04:00
- commit merge base: [5d8e981c8477ce483374b2fe6cd309a08c956299](https://github.com/python/cpython/commit/5d8e981c8477ce483374b2fe6cd309a08c956299)
- ref: 4f325168048fda89cef8

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14040037497)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250321-vultr-x86_64-python-4f325168048fda89cef8-3.14.0a6%2B-4f32516.json)

### vs. 3.12.6

- Geometric mean: 1.044x slower (HPT: reliability of 99.99%, 1.03x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250321-vultr-x86_64-python-4f325168048fda89cef8-3.14.0a6%2B-4f32516-vs-3.12.6.md)
- [📈time plot](bm-20250321-vultr-x86_64-python-4f325168048fda89cef8-3.14.0a6%2B-4f32516-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.075x slower (HPT: reliability of 99.98%, 1.04x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250321-vultr-x86_64-python-4f325168048fda89cef8-3.14.0a6%2B-4f32516-vs-3.13.0rc2.md)
- [📈time plot](bm-20250321-vultr-x86_64-python-4f325168048fda89cef8-3.14.0a6%2B-4f32516-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.003x slower (HPT: reliability of 100.00%, 1.00x slower at 99th %ile)
- Memory usage: 0.98x
- [🧠memory plot](bm-20250321-vultr-x86_64-python-4f325168048fda89cef8-3.14.0a6%2B-4f32516-vs-base-mem.svg)
- [📄table](bm-20250321-vultr-x86_64-python-4f325168048fda89cef8-3.14.0a6%2B-4f32516-vs-base.md)
- [📈time plot](bm-20250321-vultr-x86_64-python-4f325168048fda89cef8-3.14.0a6%2B-4f32516-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14040042956)
- cpu model: missing
- platform: macOS-15.3.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20250321-macm4pro-arm64-python-4f325168048fda89cef8-3.14.0a6%2B-4f32516.json)

### vs. 3.12.6

- Geometric mean: 1.012x slower (HPT: reliability of 98.67%, 1.00x slower at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250321-macm4pro-arm64-python-4f325168048fda89cef8-3.14.0a6%2B-4f32516-vs-3.12.6.md)
- [📈time plot](bm-20250321-macm4pro-arm64-python-4f325168048fda89cef8-3.14.0a6%2B-4f32516-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.083x slower (HPT: reliability of 99.97%, 1.04x slower at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250321-macm4pro-arm64-python-4f325168048fda89cef8-3.14.0a6%2B-4f32516-vs-3.13.0rc2.md)
- [📈time plot](bm-20250321-macm4pro-arm64-python-4f325168048fda89cef8-3.14.0a6%2B-4f32516-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.062x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.01x
- [🧠memory plot](bm-20250321-macm4pro-arm64-python-4f325168048fda89cef8-3.14.0a6%2B-4f32516-vs-base-mem.svg)
- [📄table](bm-20250321-macm4pro-arm64-python-4f325168048fda89cef8-3.14.0a6%2B-4f32516-vs-base.md)
- [📈time plot](bm-20250321-macm4pro-arm64-python-4f325168048fda89cef8-3.14.0a6%2B-4f32516-vs-base.svg)

