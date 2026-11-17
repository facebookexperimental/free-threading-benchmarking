# Results

- fork: python/910a92babf40b7b34baa
- version: 3.16.0a2+dev
- config: 
- commit hash: [910a92b](https://github.com/python/cpython/commit/910a92b)
- commit date: 2026-11-16T14:38:31-05:00
- commit merge base: [5e18bfcf3e27d69731384f7240e063f7eac4ef50](https://github.com/python/cpython/commit/5e18bfcf3e27d69731384f7240e063f7eac4ef50)
- ref: 910a92babf40b7b34baa

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/43987491893)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261116-vultr-x86_64-python-910a92babf40b7b34baa-3.16.0a2%2Bdev-910a92b.json)

### vs. 3.12.6

- Geometric mean: 1.092x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261116-vultr-x86_64-python-910a92babf40b7b34baa-3.16.0a2%2Bdev-910a92b-vs-3.12.6.md)
- [📈time plot](bm-20261116-vultr-x86_64-python-910a92babf40b7b34baa-3.16.0a2%2Bdev-910a92b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.055x faster (HPT: reliability of 99.69%, 1.00x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261116-vultr-x86_64-python-910a92babf40b7b34baa-3.16.0a2%2Bdev-910a92b-vs-3.13.0rc2.md)
- [📈time plot](bm-20261116-vultr-x86_64-python-910a92babf40b7b34baa-3.16.0a2%2Bdev-910a92b-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/43987491893)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261116-macm4pro-arm64-python-910a92babf40b7b34baa-3.16.0a2%2Bdev-910a92b.json)

### vs. 3.12.6

- Geometric mean: 1.202x faster (HPT: reliability of 100.00%, 1.10x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261116-macm4pro-arm64-python-910a92babf40b7b34baa-3.16.0a2%2Bdev-910a92b-vs-3.12.6.md)
- [📈time plot](bm-20261116-macm4pro-arm64-python-910a92babf40b7b34baa-3.16.0a2%2Bdev-910a92b-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.110x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261116-macm4pro-arm64-python-910a92babf40b7b34baa-3.16.0a2%2Bdev-910a92b-vs-3.13.0rc2.md)
- [📈time plot](bm-20261116-macm4pro-arm64-python-910a92babf40b7b34baa-3.16.0a2%2Bdev-910a92b-vs-3.13.0rc2.svg)

