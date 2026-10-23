# Results

- fork: DinoV/72a0e105328febfcb481
- version: 3.16.0a1+dev
- config: 
- commit hash: [72a0e10](https://github.com/DinoV/cpython/commit/72a0e10)
- commit date: 2026-10-22T16:15:52-07:00
- commit merge base: [60e956e18b6d23de777f964010b11adddf147750](https://github.com/python/cpython/commit/60e956e18b6d23de777f964010b11adddf147750)
- ref: 72a0e105328febfcb481

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/39871753163)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261022-vultr-x86_64-DinoV-72a0e105328febfcb481-3.16.0a1%2Bdev-72a0e10.json)

### vs. 3.12.6

- Geometric mean: 1.082x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.15x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261022-vultr-x86_64-DinoV-72a0e105328febfcb481-3.16.0a1%2Bdev-72a0e10-vs-3.12.6.md)
- [📈time plot](bm-20261022-vultr-x86_64-DinoV-72a0e105328febfcb481-3.16.0a1%2Bdev-72a0e10-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.045x faster (HPT: reliability of 99.61%, 1.00x faster at 99th %ile)
- Memory usage: 1.14x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261022-vultr-x86_64-DinoV-72a0e105328febfcb481-3.16.0a1%2Bdev-72a0e10-vs-3.13.0rc2.md)
- [📈time plot](bm-20261022-vultr-x86_64-DinoV-72a0e105328febfcb481-3.16.0a1%2Bdev-72a0e10-vs-3.13.0rc2.svg)

