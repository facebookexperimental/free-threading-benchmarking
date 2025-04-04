# Results

- fork: tom-pytel/579bd08e9f4db18fbbe0
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [579bd08](https://github.com/tom%2dpytel/cpython/commit/579bd08)
- commit date: 2025-03-30T18:13:59-04:00
- commit merge base: [96ef4c511f3ec763dbb06a1f3c23c658a09403a1](https://github.com/python/cpython/commit/96ef4c511f3ec763dbb06a1f3c23c658a09403a1)
- ref: 579bd08e9f4db18fbbe0

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14264982634)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-55-generic-x86_64-with-glibc2.39
- [raw results](bm-20250330-vultr-x86_64-tom%252dpytel-579bd08e9f4db18fbbe0-3.14.0a6%2B-579bd08.json)

### vs. 3.12.6

- Geometric mean: 1.046x slower (HPT: reliability of 100.00%, 1.03x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250330-vultr-x86_64-tom%252dpytel-579bd08e9f4db18fbbe0-3.14.0a6%2B-579bd08-vs-3.12.6.md)
- [📈time plot](bm-20250330-vultr-x86_64-tom%252dpytel-579bd08e9f4db18fbbe0-3.14.0a6%2B-579bd08-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.078x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250330-vultr-x86_64-tom%252dpytel-579bd08e9f4db18fbbe0-3.14.0a6%2B-579bd08-vs-3.13.0rc2.md)
- [📈time plot](bm-20250330-vultr-x86_64-tom%252dpytel-579bd08e9f4db18fbbe0-3.14.0a6%2B-579bd08-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14264979175)
- cpu model: missing
- platform: macOS-15.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20250330-macm4pro-arm64-tom%252dpytel-579bd08e9f4db18fbbe0-3.14.0a6%2B-579bd08.json)

### vs. 3.12.6

- Geometric mean: 1.057x faster (HPT: reliability of 63.16%, 1.00x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250330-macm4pro-arm64-tom%252dpytel-579bd08e9f4db18fbbe0-3.14.0a6%2B-579bd08-vs-3.12.6.md)
- [📈time plot](bm-20250330-macm4pro-arm64-tom%252dpytel-579bd08e9f4db18fbbe0-3.14.0a6%2B-579bd08-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.020x slower (HPT: reliability of 96.12%, 1.00x slower at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20250330-macm4pro-arm64-tom%252dpytel-579bd08e9f4db18fbbe0-3.14.0a6%2B-579bd08-vs-3.13.0rc2.md)
- [📈time plot](bm-20250330-macm4pro-arm64-tom%252dpytel-579bd08e9f4db18fbbe0-3.14.0a6%2B-579bd08-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.007x faster (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 0.99x
- [🧠memory plot](bm-20250330-macm4pro-arm64-tom%252dpytel-579bd08e9f4db18fbbe0-3.14.0a6%2B-579bd08-vs-base-mem.svg)
- [📄table](bm-20250330-macm4pro-arm64-tom%252dpytel-579bd08e9f4db18fbbe0-3.14.0a6%2B-579bd08-vs-base.md)
- [📈time plot](bm-20250330-macm4pro-arm64-tom%252dpytel-579bd08e9f4db18fbbe0-3.14.0a6%2B-579bd08-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.010x slower (HPT: reliability of 99.13%, 1.00x slower at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: dask
- [📄table](bm-20250330-macm4pro-arm64-tom%252dpytel-579bd08e9f4db18fbbe0-3.14.0a6%2B-579bd08-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20250330-macm4pro-arm64-tom%252dpytel-579bd08e9f4db18fbbe0-3.14.0a6%2B-579bd08-vs-default_base_vs_NOGIL.svg)

