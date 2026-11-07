# Results

- fork: python/ce4ac8c0459eba99459f
- version: 3.16.0a1+dev
- config: NOGIL
- commit hash: [ce4ac8c](https://github.com/python/cpython/commit/ce4ac8c)
- commit date: 2026-11-07T01:23:58+01:00
- commit merge base: [5106b9195fefa8eb954741661c7b3362e20f0953](https://github.com/python/cpython/commit/5106b9195fefa8eb954741661c7b3362e20f0953)
- ref: ce4ac8c0459eba99459f

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/42317897956)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261107-vultr-x86_64-python-ce4ac8c0459eba99459f-3.16.0a1%2Bdev-ce4ac8c.json)

### vs. 3.12.6

- Geometric mean: 1.028x slower (HPT: reliability of 75.17%, 1.00x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261107-vultr-x86_64-python-ce4ac8c0459eba99459f-3.16.0a1%2Bdev-ce4ac8c-vs-3.12.6.md)
- [📈time plot](bm-20261107-vultr-x86_64-python-ce4ac8c0459eba99459f-3.16.0a1%2Bdev-ce4ac8c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.060x slower (HPT: reliability of 90.53%, 1.00x slower at 99th %ile)
- Memory usage: 1.30x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261107-vultr-x86_64-python-ce4ac8c0459eba99459f-3.16.0a1%2Bdev-ce4ac8c-vs-3.13.0rc2.md)
- [📈time plot](bm-20261107-vultr-x86_64-python-ce4ac8c0459eba99459f-3.16.0a1%2Bdev-ce4ac8c-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.110x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.14x
- [🧠memory plot](bm-20261107-vultr-x86_64-python-ce4ac8c0459eba99459f-3.16.0a1%2Bdev-ce4ac8c-vs-base-mem.svg)
- [📄table](bm-20261107-vultr-x86_64-python-ce4ac8c0459eba99459f-3.16.0a1%2Bdev-ce4ac8c-vs-base.md)
- [📈time plot](bm-20261107-vultr-x86_64-python-ce4ac8c0459eba99459f-3.16.0a1%2Bdev-ce4ac8c-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/42317897956)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261107-macm4pro-arm64-python-ce4ac8c0459eba99459f-3.16.0a1%2Bdev-ce4ac8c.json)

### vs. 3.12.6

- Geometric mean: 1.080x faster (HPT: reliability of 97.99%, 1.00x faster at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261107-macm4pro-arm64-python-ce4ac8c0459eba99459f-3.16.0a1%2Bdev-ce4ac8c-vs-3.12.6.md)
- [📈time plot](bm-20261107-macm4pro-arm64-python-ce4ac8c0459eba99459f-3.16.0a1%2Bdev-ce4ac8c-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.001x faster (HPT: reliability of 77.38%, 1.00x slower at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261107-macm4pro-arm64-python-ce4ac8c0459eba99459f-3.16.0a1%2Bdev-ce4ac8c-vs-3.13.0rc2.md)
- [📈time plot](bm-20261107-macm4pro-arm64-python-ce4ac8c0459eba99459f-3.16.0a1%2Bdev-ce4ac8c-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.101x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.08x
- new benchmarks: coverage
- [🧠memory plot](bm-20261107-macm4pro-arm64-python-ce4ac8c0459eba99459f-3.16.0a1%2Bdev-ce4ac8c-vs-base-mem.svg)
- [📄table](bm-20261107-macm4pro-arm64-python-ce4ac8c0459eba99459f-3.16.0a1%2Bdev-ce4ac8c-vs-base.md)
- [📈time plot](bm-20261107-macm4pro-arm64-python-ce4ac8c0459eba99459f-3.16.0a1%2Bdev-ce4ac8c-vs-base.svg)

