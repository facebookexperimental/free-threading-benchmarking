# Results

- fork: python/854295809ad5a42c9461
- version: 3.16.0a0
- config: 
- commit hash: [8542958](https://github.com/python/cpython/commit/8542958)
- commit date: 2026-09-18T00:32:50Z
- commit merge base: [5539c2a5437acc4f4719aabac375368e0d310bd9](https://github.com/python/cpython/commit/5539c2a5437acc4f4719aabac375368e0d310bd9)
- commit date: 2026-09-18T00:32:50+00:00
- ref: 854295809ad5a42c9461

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/35292190542)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260918-vultr-x86_64-python-854295809ad5a42c9461-3.16.0a0-8542958.json)

### vs. 3.12.6

- Geometric mean: 1.064x faster (HPT: reliability of 99.99%, 1.03x faster at 99th %ile)
- Memory usage: 1.16x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260918-vultr-x86_64-python-854295809ad5a42c9461-3.16.0a0-8542958-vs-3.12.6.md)
- [📈time plot](bm-20260918-vultr-x86_64-python-854295809ad5a42c9461-3.16.0a0-8542958-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.028x faster (HPT: reliability of 99.98%, 1.01x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260918-vultr-x86_64-python-854295809ad5a42c9461-3.16.0a0-8542958-vs-3.13.0rc2.md)
- [📈time plot](bm-20260918-vultr-x86_64-python-854295809ad5a42c9461-3.16.0a0-8542958-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/35292190542)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260918-macm4pro-arm64-python-854295809ad5a42c9461-3.16.0a0-8542958.json)

### vs. 3.12.6

- Geometric mean: 1.135x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260918-macm4pro-arm64-python-854295809ad5a42c9461-3.16.0a0-8542958-vs-3.12.6.md)
- [📈time plot](bm-20260918-macm4pro-arm64-python-854295809ad5a42c9461-3.16.0a0-8542958-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.049x faster (HPT: reliability of 99.23%, 1.00x faster at 99th %ile)
- Memory usage: 1.17x
- missing benchmarks: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260918-macm4pro-arm64-python-854295809ad5a42c9461-3.16.0a0-8542958-vs-3.13.0rc2.md)
- [📈time plot](bm-20260918-macm4pro-arm64-python-854295809ad5a42c9461-3.16.0a0-8542958-vs-3.13.0rc2.svg)

