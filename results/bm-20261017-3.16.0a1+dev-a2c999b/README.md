# Results

- fork: python/a2c999bd8b4d77528679
- version: 3.16.0a1+dev
- config: 
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

- Geometric mean: 1.077x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261017-vultr-x86_64-python-a2c999bd8b4d77528679-3.16.0a1%2Bdev-a2c999b-vs-3.12.6.md)
- [📈time plot](bm-20261017-vultr-x86_64-python-a2c999bd8b4d77528679-3.16.0a1%2Bdev-a2c999b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.040x faster (HPT: reliability of 99.61%, 1.00x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261017-vultr-x86_64-python-a2c999bd8b4d77528679-3.16.0a1%2Bdev-a2c999b-vs-3.13.0rc2.md)
- [📈time plot](bm-20261017-vultr-x86_64-python-a2c999bd8b4d77528679-3.16.0a1%2Bdev-a2c999b-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/38987263799)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261017-macm4pro-arm64-python-a2c999bd8b4d77528679-3.16.0a1%2Bdev-a2c999b.json)

### vs. 3.12.6

- Geometric mean: 1.189x faster (HPT: reliability of 100.00%, 1.10x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261017-macm4pro-arm64-python-a2c999bd8b4d77528679-3.16.0a1%2Bdev-a2c999b-vs-3.12.6.md)
- [📈time plot](bm-20261017-macm4pro-arm64-python-a2c999bd8b4d77528679-3.16.0a1%2Bdev-a2c999b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.098x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261017-macm4pro-arm64-python-a2c999bd8b4d77528679-3.16.0a1%2Bdev-a2c999b-vs-3.13.0rc2.md)
- [📈time plot](bm-20261017-macm4pro-arm64-python-a2c999bd8b4d77528679-3.16.0a1%2Bdev-a2c999b-vs-3.13.0rc2.svg)

