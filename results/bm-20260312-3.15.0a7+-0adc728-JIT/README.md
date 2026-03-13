# Results

- fork: python/0adc7289c3ab097b5608
- version: 3.15.0a7+
- config: JIT
- commit hash: [0adc728](https://github.com/python/cpython/commit/0adc728)
- commit date: 2026-03-12T21:53:29-04:00
- commit merge base: [08a018ebe0d673e9c352f790d2e4604d69604188](https://github.com/python/cpython/commit/08a018ebe0d673e9c352f790d2e4604d69604188)
- ref: 0adc7289c3ab097b5608

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/23045034349)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260312-vultr-x86_64-python-0adc7289c3ab097b5608-3.15.0a7%2B-0adc728.json)

### vs. 3.12.6

- Geometric mean: 1.136x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260312-vultr-x86_64-python-0adc7289c3ab097b5608-3.15.0a7%2B-0adc728-vs-3.12.6.md)
- [📈time plot](bm-20260312-vultr-x86_64-python-0adc7289c3ab097b5608-3.15.0a7%2B-0adc728-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.098x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260312-vultr-x86_64-python-0adc7289c3ab097b5608-3.15.0a7%2B-0adc728-vs-3.13.0rc2.md)
- [📈time plot](bm-20260312-vultr-x86_64-python-0adc7289c3ab097b5608-3.15.0a7%2B-0adc728-vs-3.13.0rc2.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/23045034349)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260312-macm4pro-arm64-python-0adc7289c3ab097b5608-3.15.0a7%2B-0adc728.json)

### vs. 3.12.6

- Geometric mean: 1.244x faster (HPT: reliability of 100.00%, 1.11x faster at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260312-macm4pro-arm64-python-0adc7289c3ab097b5608-3.15.0a7%2B-0adc728-vs-3.12.6.md)
- [📈time plot](bm-20260312-macm4pro-arm64-python-0adc7289c3ab097b5608-3.15.0a7%2B-0adc728-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.153x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260312-macm4pro-arm64-python-0adc7289c3ab097b5608-3.15.0a7%2B-0adc728-vs-3.13.0rc2.md)
- [📈time plot](bm-20260312-macm4pro-arm64-python-0adc7289c3ab097b5608-3.15.0a7%2B-0adc728-vs-3.13.0rc2.svg)

