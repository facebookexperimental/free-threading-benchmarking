# Results

- fork: python/e682141c495c2e52368c
- version: 3.15.0a5+
- config: JIT
- commit hash: [e682141](https://github.com/python/cpython/commit/e682141)
- commit date: 2026-02-07T23:14:18Z
- commit merge base: [934997218e55714003276a70090a710cb3beeb61](https://github.com/python/cpython/commit/934997218e55714003276a70090a710cb3beeb61)
- commit date: 2026-02-07T23:14:18+00:00
- ref: e682141c495c2e52368c

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21789333217)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260207-vultr-x86_64-python-e682141c495c2e52368c-3.15.0a5%2B-e682141.json)

### vs. 3.12.6

- Geometric mean: 1.129x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260207-vultr-x86_64-python-e682141c495c2e52368c-3.15.0a5%2B-e682141-vs-3.12.6.md)
- [📈time plot](bm-20260207-vultr-x86_64-python-e682141c495c2e52368c-3.15.0a5%2B-e682141-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.092x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260207-vultr-x86_64-python-e682141c495c2e52368c-3.15.0a5%2B-e682141-vs-3.13.0rc2.md)
- [📈time plot](bm-20260207-vultr-x86_64-python-e682141c495c2e52368c-3.15.0a5%2B-e682141-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.045x faster (HPT: reliability of 98.03%, 1.00x faster at 99th %ile)
- Memory usage: 1.04x
- missing benchmarks: 🔴 genshi_text, genshi_xml
- [🧠memory plot](bm-20260207-vultr-x86_64-python-e682141c495c2e52368c-3.15.0a5%2B-e682141-vs-base-mem.svg)
- [📄table](bm-20260207-vultr-x86_64-python-e682141c495c2e52368c-3.15.0a5%2B-e682141-vs-base.md)
- [📈time plot](bm-20260207-vultr-x86_64-python-e682141c495c2e52368c-3.15.0a5%2B-e682141-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/21789333217)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260207-macm4pro-arm64-python-e682141c495c2e52368c-3.15.0a5%2B-e682141.json)

### vs. 3.12.6

- Geometric mean: 1.259x faster (HPT: reliability of 100.00%, 1.14x faster at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260207-macm4pro-arm64-python-e682141c495c2e52368c-3.15.0a5%2B-e682141-vs-3.12.6.md)
- [📈time plot](bm-20260207-macm4pro-arm64-python-e682141c495c2e52368c-3.15.0a5%2B-e682141-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.167x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260207-macm4pro-arm64-python-e682141c495c2e52368c-3.15.0a5%2B-e682141-vs-3.13.0rc2.md)
- [📈time plot](bm-20260207-macm4pro-arm64-python-e682141c495c2e52368c-3.15.0a5%2B-e682141-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.066x faster (HPT: reliability of 100.00%, 1.01x faster at 99th %ile)
- Memory usage: 1.03x
- missing benchmarks: 🔴 genshi_text, genshi_xml
- [🧠memory plot](bm-20260207-macm4pro-arm64-python-e682141c495c2e52368c-3.15.0a5%2B-e682141-vs-base-mem.svg)
- [📄table](bm-20260207-macm4pro-arm64-python-e682141c495c2e52368c-3.15.0a5%2B-e682141-vs-base.md)
- [📈time plot](bm-20260207-macm4pro-arm64-python-e682141c495c2e52368c-3.15.0a5%2B-e682141-vs-base.svg)

