# Results

- fork: python/a2c999bd8b4d77528679
- version: 3.16.0a1+dev
- config: NOGIL
- commit hash: [a2c999b](https://github.com/python/cpython/commit/a2c999b)
- commit date: 2026-10-17T00:36:48Z
- commit merge base: [967fb3afc7e2f706d757925e9346f0bc8aab3c46](https://github.com/python/cpython/commit/967fb3afc7e2f706d757925e9346f0bc8aab3c46)
- commit date: 2026-10-17T00:36:48+00:00
- ref: a2c999bd8b4d77528679

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/38987263799)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261017-vultr-x86_64-python-a2c999bd8b4d77528679-3.16.0a1%2Bdev-a2c999b.json)

### vs. 3.12.6

- Geometric mean: 1.038x slower (HPT: reliability of 77.48%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261017-vultr-x86_64-python-a2c999bd8b4d77528679-3.16.0a1%2Bdev-a2c999b-vs-3.12.6.md)
- [📈time plot](bm-20261017-vultr-x86_64-python-a2c999bd8b4d77528679-3.16.0a1%2Bdev-a2c999b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.071x slower (HPT: reliability of 97.19%, 1.00x slower at 99th %ile)
- Memory usage: 1.34x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261017-vultr-x86_64-python-a2c999bd8b4d77528679-3.16.0a1%2Bdev-a2c999b-vs-3.13.0rc2.md)
- [📈time plot](bm-20261017-vultr-x86_64-python-a2c999bd8b4d77528679-3.16.0a1%2Bdev-a2c999b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.110x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20261017-vultr-x86_64-python-a2c999bd8b4d77528679-3.16.0a1%2Bdev-a2c999b-vs-base-mem.svg)
- [📄table](bm-20261017-vultr-x86_64-python-a2c999bd8b4d77528679-3.16.0a1%2Bdev-a2c999b-vs-base.md)
- [📈time plot](bm-20261017-vultr-x86_64-python-a2c999bd8b4d77528679-3.16.0a1%2Bdev-a2c999b-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/38987263799)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261017-macm4pro-arm64-python-a2c999bd8b4d77528679-3.16.0a1%2Bdev-a2c999b.json)

### vs. 3.12.6

- Geometric mean: 1.057x faster (HPT: reliability of 83.87%, 1.00x faster at 99th %ile)
- Memory usage: 1.29x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261017-macm4pro-arm64-python-a2c999bd8b4d77528679-3.16.0a1%2Bdev-a2c999b-vs-3.12.6.md)
- [📈time plot](bm-20261017-macm4pro-arm64-python-a2c999bd8b4d77528679-3.16.0a1%2Bdev-a2c999b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.021x slower (HPT: reliability of 93.10%, 1.00x slower at 99th %ile)
- Memory usage: 1.25x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261017-macm4pro-arm64-python-a2c999bd8b4d77528679-3.16.0a1%2Bdev-a2c999b-vs-3.13.0rc2.md)
- [📈time plot](bm-20261017-macm4pro-arm64-python-a2c999bd8b4d77528679-3.16.0a1%2Bdev-a2c999b-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.107x slower (HPT: reliability of 100.00%, 1.11x slower at 99th %ile)
- Memory usage: 1.11x
- new benchmarks: coverage
- [🧠memory plot](bm-20261017-macm4pro-arm64-python-a2c999bd8b4d77528679-3.16.0a1%2Bdev-a2c999b-vs-base-mem.svg)
- [📄table](bm-20261017-macm4pro-arm64-python-a2c999bd8b4d77528679-3.16.0a1%2Bdev-a2c999b-vs-base.md)
- [📈time plot](bm-20261017-macm4pro-arm64-python-a2c999bd8b4d77528679-3.16.0a1%2Bdev-a2c999b-vs-base.svg)

