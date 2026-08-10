# Results

- fork: corona10/gh_129752
- version: 3.16.0a0
- config: NOGIL
- commit hash: [d644555](https://github.com/corona10/cpython/commit/d644555)
- commit date: 2026-08-11T02:01:32+09:00
- commit merge base: [e4b22adf24996d15366b8ff91ec0707ae0f606df](https://github.com/python/cpython/commit/e4b22adf24996d15366b8ff91ec0707ae0f606df)
- ref: gh_129752

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/31427162577)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260811-vultr-x86_64-corona10-gh_129752-3.16.0a0-d644555.json)

### vs. 3.12.6

- Geometric mean: 1.041x slower (HPT: reliability of 87.76%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260811-vultr-x86_64-corona10-gh_129752-3.16.0a0-d644555-vs-3.12.6.md)
- [📈time plot](bm-20260811-vultr-x86_64-corona10-gh_129752-3.16.0a0-d644555-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.073x slower (HPT: reliability of 99.72%, 1.01x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260811-vultr-x86_64-corona10-gh_129752-3.16.0a0-d644555-vs-3.13.0rc2.md)
- [📈time plot](bm-20260811-vultr-x86_64-corona10-gh_129752-3.16.0a0-d644555-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.004x slower (HPT: reliability of 91.71%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20260811-vultr-x86_64-corona10-gh_129752-3.16.0a0-d644555-vs-base-mem.svg)
- [📄table](bm-20260811-vultr-x86_64-corona10-gh_129752-3.16.0a0-d644555-vs-base.md)
- [📈time plot](bm-20260811-vultr-x86_64-corona10-gh_129752-3.16.0a0-d644555-vs-base.svg)

