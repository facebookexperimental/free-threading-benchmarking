# Results

- fork: python/cc0e59f17d0fcd8ed9f3
- version: 3.16.0a2+dev
- config: NOGIL
- commit hash: [cc0e59f](https://github.com/python/cpython/commit/cc0e59f)
- commit date: 2026-11-25T15:49:29-08:00
- commit merge base: [102a03c42058f40f2e3ad1ae546c4aaa86643247](https://github.com/python/cpython/commit/102a03c42058f40f2e3ad1ae546c4aaa86643247)
- ref: cc0e59f17d0fcd8ed9f3

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/45728515395)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261125-vultr-x86_64-python-cc0e59f17d0fcd8ed9f3-3.16.0a2%2Bdev-cc0e59f.json)

### vs. 3.12.6

- Geometric mean: 1.022x slower (HPT: reliability of 66.13%, 1.00x slower at 99th %ile)
- Memory usage: 1.31x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261125-vultr-x86_64-python-cc0e59f17d0fcd8ed9f3-3.16.0a2%2Bdev-cc0e59f-vs-3.12.6.md)
- [📈time plot](bm-20261125-vultr-x86_64-python-cc0e59f17d0fcd8ed9f3-3.16.0a2%2Bdev-cc0e59f-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.056x slower (HPT: reliability of 85.84%, 1.00x slower at 99th %ile)
- Memory usage: 1.30x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261125-vultr-x86_64-python-cc0e59f17d0fcd8ed9f3-3.16.0a2%2Bdev-cc0e59f-vs-3.13.0rc2.md)
- [📈time plot](bm-20261125-vultr-x86_64-python-cc0e59f17d0fcd8ed9f3-3.16.0a2%2Bdev-cc0e59f-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.116x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.14x
- [🧠memory plot](bm-20261125-vultr-x86_64-python-cc0e59f17d0fcd8ed9f3-3.16.0a2%2Bdev-cc0e59f-vs-base-mem.svg)
- [📄table](bm-20261125-vultr-x86_64-python-cc0e59f17d0fcd8ed9f3-3.16.0a2%2Bdev-cc0e59f-vs-base.md)
- [📈time plot](bm-20261125-vultr-x86_64-python-cc0e59f17d0fcd8ed9f3-3.16.0a2%2Bdev-cc0e59f-vs-base.svg)

