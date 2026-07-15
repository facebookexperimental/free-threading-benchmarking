# Results

- fork: python/2dc1a91af801ea896e21
- version: 3.16.0a0
- config: NOGIL
- commit hash: [2dc1a91](https://github.com/python/cpython/commit/2dc1a91)
- commit date: 2026-07-14T06:38:43+08:00
- commit merge base: [701a7c5408f689b26c46ed7ed13879375fa82959](https://github.com/python/cpython/commit/701a7c5408f689b26c46ed7ed13879375fa82959)
- ref: 2dc1a91af801ea896e21

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/29296491735)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260714-vultr-x86_64-python-2dc1a91af801ea896e21-3.16.0a0-2dc1a91.json)

### vs. 3.12.6

- Geometric mean: 1.043x slower (HPT: reliability of 96.89%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260714-vultr-x86_64-python-2dc1a91af801ea896e21-3.16.0a0-2dc1a91-vs-3.12.6.md)
- [📈time plot](bm-20260714-vultr-x86_64-python-2dc1a91af801ea896e21-3.16.0a0-2dc1a91-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.075x slower (HPT: reliability of 99.86%, 1.01x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260714-vultr-x86_64-python-2dc1a91af801ea896e21-3.16.0a0-2dc1a91-vs-3.13.0rc2.md)
- [📈time plot](bm-20260714-vultr-x86_64-python-2dc1a91af801ea896e21-3.16.0a0-2dc1a91-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.112x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20260714-vultr-x86_64-python-2dc1a91af801ea896e21-3.16.0a0-2dc1a91-vs-base-mem.svg)
- [📄table](bm-20260714-vultr-x86_64-python-2dc1a91af801ea896e21-3.16.0a0-2dc1a91-vs-base.md)
- [📈time plot](bm-20260714-vultr-x86_64-python-2dc1a91af801ea896e21-3.16.0a0-2dc1a91-vs-base.svg)

