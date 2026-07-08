# Results

- fork: python/35c6779c7b5c4c2e2d97
- version: 3.16.0a0
- config: 
- commit hash: [35c6779](https://github.com/python/cpython/commit/35c6779)
- commit date: 2026-07-06T23:54:16+00:00
- commit merge base: [d7275d356916f839dc96aaa43a75e0bbde25732e](https://github.com/python/cpython/commit/d7275d356916f839dc96aaa43a75e0bbde25732e)
- ref: 35c6779c7b5c4c2e2d97

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/28833612973)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260706-vultr-x86_64-python-35c6779c7b5c4c2e2d97-3.16.0a0-35c6779.json)

### vs. 3.12.6

- Geometric mean: 1.069x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260706-vultr-x86_64-python-35c6779c7b5c4c2e2d97-3.16.0a0-35c6779-vs-3.12.6.md)
- [📈time plot](bm-20260706-vultr-x86_64-python-35c6779c7b5c4c2e2d97-3.16.0a0-35c6779-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.033x faster (HPT: reliability of 99.99%, 1.00x faster at 99th %ile)
- Memory usage: 1.13x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260706-vultr-x86_64-python-35c6779c7b5c4c2e2d97-3.16.0a0-35c6779-vs-3.13.0rc2.md)
- [📈time plot](bm-20260706-vultr-x86_64-python-35c6779c7b5c4c2e2d97-3.16.0a0-35c6779-vs-3.13.0rc2.svg)

