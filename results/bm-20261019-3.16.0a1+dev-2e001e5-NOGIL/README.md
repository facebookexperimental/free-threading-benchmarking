# Results

- fork: DinoV/2e001e5dfdb655ce1fab
- version: 3.16.0a1+dev
- config: NOGIL
- commit hash: [2e001e5](https://github.com/DinoV/cpython/commit/2e001e5)
- commit date: 2026-10-19T23:32:34-07:00
- commit merge base: [415ebffc47e8303d61cf97faf4ddb474334d736d](https://github.com/python/cpython/commit/415ebffc47e8303d61cf97faf4ddb474334d736d)
- ref: 2e001e5dfdb655ce1fab

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/39383094114)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261019-vultr-x86_64-DinoV-2e001e5dfdb655ce1fab-3.16.0a1%2Bdev-2e001e5.json)

### vs. 3.12.6

- Geometric mean: 1.046x slower (HPT: reliability of 84.93%, 1.00x slower at 99th %ile)
- Memory usage: 1.45x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261019-vultr-x86_64-DinoV-2e001e5dfdb655ce1fab-3.16.0a1%2Bdev-2e001e5-vs-3.12.6.md)
- [📈time plot](bm-20261019-vultr-x86_64-DinoV-2e001e5dfdb655ce1fab-3.16.0a1%2Bdev-2e001e5-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.078x slower (HPT: reliability of 93.47%, 1.00x slower at 99th %ile)
- Memory usage: 1.44x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261019-vultr-x86_64-DinoV-2e001e5dfdb655ce1fab-3.16.0a1%2Bdev-2e001e5-vs-3.13.0rc2.md)
- [📈time plot](bm-20261019-vultr-x86_64-DinoV-2e001e5dfdb655ce1fab-3.16.0a1%2Bdev-2e001e5-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.011x slower (HPT: reliability of 99.74%, 1.00x slower at 99th %ile)
- Memory usage: 1.06x
- [🧠memory plot](bm-20261019-vultr-x86_64-DinoV-2e001e5dfdb655ce1fab-3.16.0a1%2Bdev-2e001e5-vs-base-mem.svg)
- [📄table](bm-20261019-vultr-x86_64-DinoV-2e001e5dfdb655ce1fab-3.16.0a1%2Bdev-2e001e5-vs-base.md)
- [📈time plot](bm-20261019-vultr-x86_64-DinoV-2e001e5dfdb655ce1fab-3.16.0a1%2Bdev-2e001e5-vs-base.svg)

