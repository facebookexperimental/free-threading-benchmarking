# Results

- fork: DinoV/f5bd07700ecd0f02cc42
- version: 3.16.0a1+dev
- config: 
- commit hash: [f5bd077](https://github.com/DinoV/cpython/commit/f5bd077)
- commit date: 2026-10-20T11:55:45-07:00
- commit merge base: [88d922ad982c4e00f8cb936cffba154d8d5fb697](https://github.com/python/cpython/commit/88d922ad982c4e00f8cb936cffba154d8d5fb697)
- ref: f5bd07700ecd0f02cc42

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/39538970966)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261020-vultr-x86_64-DinoV-f5bd07700ecd0f02cc42-3.16.0a1%2Bdev-f5bd077.json)

### vs. 3.12.6

- Geometric mean: 1.081x faster (HPT: reliability of 99.99%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261020-vultr-x86_64-DinoV-f5bd07700ecd0f02cc42-3.16.0a1%2Bdev-f5bd077-vs-3.12.6.md)
- [📈time plot](bm-20261020-vultr-x86_64-DinoV-f5bd07700ecd0f02cc42-3.16.0a1%2Bdev-f5bd077-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.044x faster (HPT: reliability of 99.41%, 1.00x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261020-vultr-x86_64-DinoV-f5bd07700ecd0f02cc42-3.16.0a1%2Bdev-f5bd077-vs-3.13.0rc2.md)
- [📈time plot](bm-20261020-vultr-x86_64-DinoV-f5bd07700ecd0f02cc42-3.16.0a1%2Bdev-f5bd077-vs-3.13.0rc2.svg)

