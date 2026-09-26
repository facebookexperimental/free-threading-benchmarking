# Results

- fork: python/a000129df30819c3b762
- version: 3.16.0a0
- config: NOGIL
- commit hash: [a000129](https://github.com/python/cpython/commit/a000129)
- commit date: 2026-09-26T01:02:29+02:00
- commit merge base: [b71989d65780683dbbcc3882afc0ef0d794a6ddb](https://github.com/python/cpython/commit/b71989d65780683dbbcc3882afc0ef0d794a6ddb)
- ref: a000129df30819c3b762

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/36205712057)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260926-vultr-x86_64-python-a000129df30819c3b762-3.16.0a0-a000129.json)

### vs. 3.12.6

- Geometric mean: 1.044x slower (HPT: reliability of 86.07%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260926-vultr-x86_64-python-a000129df30819c3b762-3.16.0a0-a000129-vs-3.12.6.md)
- [📈time plot](bm-20260926-vultr-x86_64-python-a000129df30819c3b762-3.16.0a0-a000129-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.077x slower (HPT: reliability of 98.25%, 1.00x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260926-vultr-x86_64-python-a000129df30819c3b762-3.16.0a0-a000129-vs-3.13.0rc2.md)
- [📈time plot](bm-20260926-vultr-x86_64-python-a000129df30819c3b762-3.16.0a0-a000129-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.102x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20260926-vultr-x86_64-python-a000129df30819c3b762-3.16.0a0-a000129-vs-base-mem.svg)
- [📄table](bm-20260926-vultr-x86_64-python-a000129df30819c3b762-3.16.0a0-a000129-vs-base.md)
- [📈time plot](bm-20260926-vultr-x86_64-python-a000129df30819c3b762-3.16.0a0-a000129-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/36205712057)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260926-macm4pro-arm64-python-a000129df30819c3b762-3.16.0a0-a000129.json)

### vs. 3.12.6

- Geometric mean: 1.008x faster (HPT: reliability of 82.09%, 1.00x slower at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260926-macm4pro-arm64-python-a000129df30819c3b762-3.16.0a0-a000129-vs-3.12.6.md)
- [📈time plot](bm-20260926-macm4pro-arm64-python-a000129df30819c3b762-3.16.0a0-a000129-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.067x slower (HPT: reliability of 99.81%, 1.02x slower at 99th %ile)
- Memory usage: 1.29x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260926-macm4pro-arm64-python-a000129df30819c3b762-3.16.0a0-a000129-vs-3.13.0rc2.md)
- [📈time plot](bm-20260926-macm4pro-arm64-python-a000129df30819c3b762-3.16.0a0-a000129-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.112x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.11x
- new benchmarks: coverage
- [🧠memory plot](bm-20260926-macm4pro-arm64-python-a000129df30819c3b762-3.16.0a0-a000129-vs-base-mem.svg)
- [📄table](bm-20260926-macm4pro-arm64-python-a000129df30819c3b762-3.16.0a0-a000129-vs-base.md)
- [📈time plot](bm-20260926-macm4pro-arm64-python-a000129df30819c3b762-3.16.0a0-a000129-vs-base.svg)

