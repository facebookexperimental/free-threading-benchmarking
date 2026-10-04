# Results

- fork: python/9d22a5334bd5273962ad
- version: 3.16.0a0
- config: 
- commit hash: [9d22a53](https://github.com/python/cpython/commit/9d22a53)
- commit date: 2026-10-03T23:51:37Z
- commit merge base: [880696af1aff6f4170fbacdfb8aa73a84be73da5](https://github.com/python/cpython/commit/880696af1aff6f4170fbacdfb8aa73a84be73da5)
- commit date: 2026-10-03T23:51:37+00:00
- ref: 9d22a5334bd5273962ad

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/37166758476)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [pystats raw](bm-20261003-vultr-x86_64-python-9d22a5334bd5273962ad-3.16.0a0-9d22a53-pystats.json)
- [pystats table](bm-20261003-vultr-x86_64-python-9d22a5334bd5273962ad-3.16.0a0-9d22a53-pystats.md)
- [raw results](bm-20261003-vultr-x86_64-python-9d22a5334bd5273962ad-3.16.0a0-9d22a53.json)

### vs. 3.12.6

- Geometric mean: 1.070x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261003-vultr-x86_64-python-9d22a5334bd5273962ad-3.16.0a0-9d22a53-vs-3.12.6.md)
- [📈time plot](bm-20261003-vultr-x86_64-python-9d22a5334bd5273962ad-3.16.0a0-9d22a53-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.033x faster (HPT: reliability of 99.76%, 1.00x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261003-vultr-x86_64-python-9d22a5334bd5273962ad-3.16.0a0-9d22a53-vs-3.13.0rc2.md)
- [📈time plot](bm-20261003-vultr-x86_64-python-9d22a5334bd5273962ad-3.16.0a0-9d22a53-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/37166758476)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261003-macm4pro-arm64-python-9d22a5334bd5273962ad-3.16.0a0-9d22a53.json)

### vs. 3.12.6

- Geometric mean: 1.162x faster (HPT: reliability of 100.00%, 1.09x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20261003-macm4pro-arm64-python-9d22a5334bd5273962ad-3.16.0a0-9d22a53-vs-3.12.6.md)
- [📈time plot](bm-20261003-macm4pro-arm64-python-9d22a5334bd5273962ad-3.16.0a0-9d22a53-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.074x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20261003-macm4pro-arm64-python-9d22a5334bd5273962ad-3.16.0a0-9d22a53-vs-3.13.0rc2.md)
- [📈time plot](bm-20261003-macm4pro-arm64-python-9d22a5334bd5273962ad-3.16.0a0-9d22a53-vs-3.13.0rc2.svg)

