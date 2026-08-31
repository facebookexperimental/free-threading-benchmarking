# Results

- fork: kumaraditya303/gen_gi_frame_thread_
- version: 3.16.0a0
- config: NOGIL
- commit hash: [1928144](https://github.com/kumaraditya303/cpython/commit/1928144)
- commit date: 2026-08-19T19:36:45+05:30
- commit merge base: [20e6c2fc7c174342214d561845419c4030f8638f](https://github.com/python/cpython/commit/20e6c2fc7c174342214d561845419c4030f8638f)
- ref: gen_gi_frame_thread_

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/33439585676)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260819-vultr-x86_64-kumaraditya303-gen_gi_frame_thread_-3.16.0a0-1928144.json)

### vs. 3.12.6

- Geometric mean: 1.050x slower (HPT: reliability of 93.08%, 1.00x slower at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260819-vultr-x86_64-kumaraditya303-gen_gi_frame_thread_-3.16.0a0-1928144-vs-3.12.6.md)
- [📈time plot](bm-20260819-vultr-x86_64-kumaraditya303-gen_gi_frame_thread_-3.16.0a0-1928144-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.082x slower (HPT: reliability of 98.14%, 1.00x slower at 99th %ile)
- Memory usage: 1.36x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260819-vultr-x86_64-kumaraditya303-gen_gi_frame_thread_-3.16.0a0-1928144-vs-3.13.0rc2.md)
- [📈time plot](bm-20260819-vultr-x86_64-kumaraditya303-gen_gi_frame_thread_-3.16.0a0-1928144-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.013x slower (HPT: reliability of 100.00%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20260819-vultr-x86_64-kumaraditya303-gen_gi_frame_thread_-3.16.0a0-1928144-vs-base-mem.svg)
- [📄table](bm-20260819-vultr-x86_64-kumaraditya303-gen_gi_frame_thread_-3.16.0a0-1928144-vs-base.md)
- [📈time plot](bm-20260819-vultr-x86_64-kumaraditya303-gen_gi_frame_thread_-3.16.0a0-1928144-vs-base.svg)

