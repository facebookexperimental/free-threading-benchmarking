# Results

- fork: python/f76742309542a255af56
- version: 3.16.0a1+dev
- config: 
- commit hash: [f767423](https://github.com/python/cpython/commit/f767423)
- commit date: 2026-11-07T14:48:59-08:00
- commit merge base: [5f46ac97490ddfd8f7a4d01b9f765cccd00d0e72](https://github.com/python/cpython/commit/5f46ac97490ddfd8f7a4d01b9f765cccd00d0e72)
- ref: f76742309542a255af56

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/42428775380)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [pystats raw](bm-20261107-vultr-x86_64-python-f76742309542a255af56-3.16.0a1%2Bdev-f767423-pystats.json)
- [pystats table](bm-20261107-vultr-x86_64-python-f76742309542a255af56-3.16.0a1%2Bdev-f767423-pystats.md)
- [raw results](bm-20261107-vultr-x86_64-python-f76742309542a255af56-3.16.0a1%2Bdev-f767423.json)

### vs. 3.12.6

- Geometric mean: 1.089x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261107-vultr-x86_64-python-f76742309542a255af56-3.16.0a1%2Bdev-f767423-vs-3.12.6.md)
- [📈time plot](bm-20261107-vultr-x86_64-python-f76742309542a255af56-3.16.0a1%2Bdev-f767423-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.053x faster (HPT: reliability of 99.87%, 1.00x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261107-vultr-x86_64-python-f76742309542a255af56-3.16.0a1%2Bdev-f767423-vs-3.13.0rc2.md)
- [📈time plot](bm-20261107-vultr-x86_64-python-f76742309542a255af56-3.16.0a1%2Bdev-f767423-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/42428775380)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261107-macm4pro-arm64-python-f76742309542a255af56-3.16.0a1%2Bdev-f767423.json)

### vs. 3.12.6

- Geometric mean: 1.200x faster (HPT: reliability of 100.00%, 1.10x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20261107-macm4pro-arm64-python-f76742309542a255af56-3.16.0a1%2Bdev-f767423-vs-3.12.6.md)
- [📈time plot](bm-20261107-macm4pro-arm64-python-f76742309542a255af56-3.16.0a1%2Bdev-f767423-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.109x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20261107-macm4pro-arm64-python-f76742309542a255af56-3.16.0a1%2Bdev-f767423-vs-3.13.0rc2.md)
- [📈time plot](bm-20261107-macm4pro-arm64-python-f76742309542a255af56-3.16.0a1%2Bdev-f767423-vs-3.13.0rc2.svg)

