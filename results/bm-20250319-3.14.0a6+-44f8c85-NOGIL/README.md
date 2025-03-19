# Results

- fork: colesbury/gh_128421_frame
- version: 3.14.0a6+
- config: NOGIL
- commit hash: [44f8c85](https://github.com/colesbury/cpython/commit/44f8c85)
- commit date: 2025-03-19T20:27:45+00:00
- commit merge base: [a4832f6b9a62771725b159bc7cd6c49fb45e3bc8](https://github.com/python/cpython/commit/a4832f6b9a62771725b159bc7cd6c49fb45e3bc8)
- ref: gh_128421_frame

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/13956179961)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-51-generic-x86_64-with-glibc2.39
- [raw results](bm-20250319-vultr-x86_64-colesbury-gh_128421_frame-3.14.0a6%2B-44f8c85.json)

### vs. 3.12.6

- Geometric mean: 1.050x slower (HPT: reliability of 99.99%, 1.03x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250319-vultr-x86_64-colesbury-gh_128421_frame-3.14.0a6%2B-44f8c85-vs-3.12.6.md)
- [📈time plot](bm-20250319-vultr-x86_64-colesbury-gh_128421_frame-3.14.0a6%2B-44f8c85-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.081x slower (HPT: reliability of 100.00%, 1.04x slower at 99th %ile)
- Memory usage: 1.35x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20250319-vultr-x86_64-colesbury-gh_128421_frame-3.14.0a6%2B-44f8c85-vs-3.13.0rc2.md)
- [📈time plot](bm-20250319-vultr-x86_64-colesbury-gh_128421_frame-3.14.0a6%2B-44f8c85-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.002x slower (HPT: reliability of 99.47%, 1.00x faster at 99th %ile)
- Memory usage: 0.99x
- [🧠memory plot](bm-20250319-vultr-x86_64-colesbury-gh_128421_frame-3.14.0a6%2B-44f8c85-vs-base-mem.svg)
- [📄table](bm-20250319-vultr-x86_64-colesbury-gh_128421_frame-3.14.0a6%2B-44f8c85-vs-base.md)
- [📈time plot](bm-20250319-vultr-x86_64-colesbury-gh_128421_frame-3.14.0a6%2B-44f8c85-vs-base.svg)

