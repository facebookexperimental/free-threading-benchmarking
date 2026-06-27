# Results

- fork: python/55bc3126e0a09a8e940d
- version: 3.16.0a0
- config: NOGIL
- commit hash: [55bc312](https://github.com/python/cpython/commit/55bc312)
- commit date: 2026-06-25T18:06:07+00:00
- commit merge base: [bef570622263ecd58563f0474693c19c8545de73](https://github.com/python/cpython/commit/bef570622263ecd58563f0474693c19c8545de73)
- ref: 55bc3126e0a09a8e940d

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/28210458820)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260625-vultr-x86_64-python-55bc3126e0a09a8e940d-3.16.0a0-55bc312.json)

### vs. 3.12.6

- Geometric mean: 1.033x slower (HPT: reliability of 92.67%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260625-vultr-x86_64-python-55bc3126e0a09a8e940d-3.16.0a0-55bc312-vs-3.12.6.md)
- [📈time plot](bm-20260625-vultr-x86_64-python-55bc3126e0a09a8e940d-3.16.0a0-55bc312-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.066x slower (HPT: reliability of 99.08%, 1.00x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260625-vultr-x86_64-python-55bc3126e0a09a8e940d-3.16.0a0-55bc312-vs-3.13.0rc2.md)
- [📈time plot](bm-20260625-vultr-x86_64-python-55bc3126e0a09a8e940d-3.16.0a0-55bc312-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.107x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20260625-vultr-x86_64-python-55bc3126e0a09a8e940d-3.16.0a0-55bc312-vs-base-mem.svg)
- [📄table](bm-20260625-vultr-x86_64-python-55bc3126e0a09a8e940d-3.16.0a0-55bc312-vs-base.md)
- [📈time plot](bm-20260625-vultr-x86_64-python-55bc3126e0a09a8e940d-3.16.0a0-55bc312-vs-base.svg)

