# Results

- fork: DinoV/a8e2a422fb35ab5cbf5b
- version: 3.16.0a1+dev
- config: NOGIL
- commit hash: [a8e2a42](https://github.com/DinoV/cpython/commit/a8e2a42)
- commit date: 2026-10-20T14:05:20-07:00
- commit merge base: [f5bd07700ecd0f02cc424666b871f51de03b9232](https://github.com/python/cpython/commit/f5bd07700ecd0f02cc424666b871f51de03b9232)
- ref: a8e2a422fb35ab5cbf5b

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/39497633255)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20261020-vultr-x86_64-DinoV-a8e2a422fb35ab5cbf5b-3.16.0a1%2Bdev-a8e2a42.json)

### vs. 3.12.6

- Geometric mean: 1.040x slower (HPT: reliability of 87.86%, 1.00x slower at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261020-vultr-x86_64-DinoV-a8e2a422fb35ab5cbf5b-3.16.0a1%2Bdev-a8e2a42-vs-3.12.6.md)
- [📈time plot](bm-20261020-vultr-x86_64-DinoV-a8e2a422fb35ab5cbf5b-3.16.0a1%2Bdev-a8e2a42-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.073x slower (HPT: reliability of 95.55%, 1.00x slower at 99th %ile)
- Memory usage: 1.38x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20261020-vultr-x86_64-DinoV-a8e2a422fb35ab5cbf5b-3.16.0a1%2Bdev-a8e2a42-vs-3.13.0rc2.md)
- [📈time plot](bm-20261020-vultr-x86_64-DinoV-a8e2a422fb35ab5cbf5b-3.16.0a1%2Bdev-a8e2a42-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.002x slower (HPT: reliability of 94.81%, 1.00x slower at 99th %ile)
- Memory usage: 1.03x
- [🧠memory plot](bm-20261020-vultr-x86_64-DinoV-a8e2a422fb35ab5cbf5b-3.16.0a1%2Bdev-a8e2a42-vs-base-mem.svg)
- [📄table](bm-20261020-vultr-x86_64-DinoV-a8e2a422fb35ab5cbf5b-3.16.0a1%2Bdev-a8e2a42-vs-base.md)
- [📈time plot](bm-20261020-vultr-x86_64-DinoV-a8e2a422fb35ab5cbf5b-3.16.0a1%2Bdev-a8e2a42-vs-base.svg)

