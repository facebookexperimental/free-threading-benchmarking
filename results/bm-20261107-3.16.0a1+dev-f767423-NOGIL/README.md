# Results

- fork: python/f76742309542a255af56
- version: 3.16.0a1+dev
- config: NOGIL
- commit hash: [f767423](https://github.com/python/cpython/commit/f767423)
- commit date: 2026-11-07T14:48:59-08:00
- commit merge base: [5f46ac97490ddfd8f7a4d01b9f765cccd00d0e72](https://github.com/python/cpython/commit/5f46ac97490ddfd8f7a4d01b9f765cccd00d0e72)
- ref: f76742309542a255af56

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/42428775380)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261107-vultr-x86_64-python-f76742309542a255af56-3.16.0a1%2Bdev-f767423.json)

### vs. 3.12.6

- Geometric mean: 1.029x slower (HPT: reliability of 78.94%, 1.00x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261107-vultr-x86_64-python-f76742309542a255af56-3.16.0a1%2Bdev-f767423-vs-3.12.6.md)
- [📈time plot](bm-20261107-vultr-x86_64-python-f76742309542a255af56-3.16.0a1%2Bdev-f767423-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.062x slower (HPT: reliability of 91.88%, 1.00x slower at 99th %ile)
- Memory usage: 1.30x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261107-vultr-x86_64-python-f76742309542a255af56-3.16.0a1%2Bdev-f767423-vs-3.13.0rc2.md)
- [📈time plot](bm-20261107-vultr-x86_64-python-f76742309542a255af56-3.16.0a1%2Bdev-f767423-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.113x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.14x
- [🧠memory plot](bm-20261107-vultr-x86_64-python-f76742309542a255af56-3.16.0a1%2Bdev-f767423-vs-base-mem.svg)
- [📄table](bm-20261107-vultr-x86_64-python-f76742309542a255af56-3.16.0a1%2Bdev-f767423-vs-base.md)
- [📈time plot](bm-20261107-vultr-x86_64-python-f76742309542a255af56-3.16.0a1%2Bdev-f767423-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/42428775380)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261107-macm4pro-arm64-python-f76742309542a255af56-3.16.0a1%2Bdev-f767423.json)

### vs. 3.12.6

- Geometric mean: 1.077x faster (HPT: reliability of 97.10%, 1.00x faster at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20261107-macm4pro-arm64-python-f76742309542a255af56-3.16.0a1%2Bdev-f767423-vs-3.12.6.md)
- [📈time plot](bm-20261107-macm4pro-arm64-python-f76742309542a255af56-3.16.0a1%2Bdev-f767423-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.003x slower (HPT: reliability of 85.17%, 1.00x slower at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20261107-macm4pro-arm64-python-f76742309542a255af56-3.16.0a1%2Bdev-f767423-vs-3.13.0rc2.md)
- [📈time plot](bm-20261107-macm4pro-arm64-python-f76742309542a255af56-3.16.0a1%2Bdev-f767423-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.099x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.08x
- new benchmarks: coverage
- [🧠memory plot](bm-20261107-macm4pro-arm64-python-f76742309542a255af56-3.16.0a1%2Bdev-f767423-vs-base-mem.svg)
- [📄table](bm-20261107-macm4pro-arm64-python-f76742309542a255af56-3.16.0a1%2Bdev-f767423-vs-base.md)
- [📈time plot](bm-20261107-macm4pro-arm64-python-f76742309542a255af56-3.16.0a1%2Bdev-f767423-vs-base.svg)

