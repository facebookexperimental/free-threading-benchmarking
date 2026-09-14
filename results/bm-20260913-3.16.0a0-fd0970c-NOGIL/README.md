# Results

- fork: python/fd0970c0ab7eb8c685ef
- version: 3.16.0a0
- config: NOGIL
- commit hash: [fd0970c](https://github.com/python/cpython/commit/fd0970c)
- commit date: 2026-09-13T20:45:34Z
- commit merge base: [ae0d6cc79118114f70afe5f65e5ab3a8d33359cc](https://github.com/python/cpython/commit/ae0d6cc79118114f70afe5f65e5ab3a8d33359cc)
- commit date: 2026-09-13T20:45:34+00:00
- ref: fd0970c0ab7eb8c685ef

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/34793684275)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260913-vultr-x86_64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c.json)

### vs. 3.12.6

- Geometric mean: 1.049x slower (HPT: reliability of 92.03%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260913-vultr-x86_64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c-vs-3.12.6.md)
- [📈time plot](bm-20260913-vultr-x86_64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.081x slower (HPT: reliability of 99.26%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260913-vultr-x86_64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c-vs-3.13.0rc2.md)
- [📈time plot](bm-20260913-vultr-x86_64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.107x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.19x
- [🧠memory plot](bm-20260913-vultr-x86_64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c-vs-base-mem.svg)
- [📄table](bm-20260913-vultr-x86_64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c-vs-base.md)
- [📈time plot](bm-20260913-vultr-x86_64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/34793684275)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260913-macm4pro-arm64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c.json)

### vs. 3.12.6

- Geometric mean: 1.084x faster (HPT: reliability of 98.19%, 1.00x faster at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260913-macm4pro-arm64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c-vs-3.12.6.md)
- [📈time plot](bm-20260913-macm4pro-arm64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.005x faster (HPT: reliability of 87.71%, 1.00x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260913-macm4pro-arm64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c-vs-3.13.0rc2.md)
- [📈time plot](bm-20260913-macm4pro-arm64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.043x slower (HPT: reliability of 100.00%, 1.03x slower at 99th %ile)
- Memory usage: 1.12x
- new benchmarks: coverage
- [🧠memory plot](bm-20260913-macm4pro-arm64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c-vs-base-mem.svg)
- [📄table](bm-20260913-macm4pro-arm64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c-vs-base.md)
- [📈time plot](bm-20260913-macm4pro-arm64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c-vs-base.svg)

