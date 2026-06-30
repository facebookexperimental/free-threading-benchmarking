# Results

- fork: python/f57d3d6db39ea0bd3974
- version: 3.16.0a0
- config: NOGIL
- commit hash: [f57d3d6](https://github.com/python/cpython/commit/f57d3d6)
- commit date: 2026-06-28T17:27:15-07:00
- commit merge base: [2d0003c0b28dca86197f4b74810966856a27dc60](https://github.com/python/cpython/commit/2d0003c0b28dca86197f4b74810966856a27dc60)
- ref: f57d3d6db39ea0bd3974

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/28342320109)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260628-vultr-x86_64-python-f57d3d6db39ea0bd3974-3.16.0a0-f57d3d6.json)

### vs. 3.12.6

- Geometric mean: 1.044x slower (HPT: reliability of 96.09%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260628-vultr-x86_64-python-f57d3d6db39ea0bd3974-3.16.0a0-f57d3d6-vs-3.12.6.md)
- [📈time plot](bm-20260628-vultr-x86_64-python-f57d3d6db39ea0bd3974-3.16.0a0-f57d3d6-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.077x slower (HPT: reliability of 99.77%, 1.01x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260628-vultr-x86_64-python-f57d3d6db39ea0bd3974-3.16.0a0-f57d3d6-vs-3.13.0rc2.md)
- [📈time plot](bm-20260628-vultr-x86_64-python-f57d3d6db39ea0bd3974-3.16.0a0-f57d3d6-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.116x slower (HPT: reliability of 100.00%, 1.12x slower at 99th %ile)
- Memory usage: 1.18x
- [🧠memory plot](bm-20260628-vultr-x86_64-python-f57d3d6db39ea0bd3974-3.16.0a0-f57d3d6-vs-base-mem.svg)
- [📄table](bm-20260628-vultr-x86_64-python-f57d3d6db39ea0bd3974-3.16.0a0-f57d3d6-vs-base.md)
- [📈time plot](bm-20260628-vultr-x86_64-python-f57d3d6db39ea0bd3974-3.16.0a0-f57d3d6-vs-base.svg)

