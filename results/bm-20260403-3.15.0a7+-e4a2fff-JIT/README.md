# Results

- fork: kumaraditya303/jit_inline_funcptr
- version: 3.15.0a7+
- config: JIT
- commit hash: [e4a2fff](https://github.com/kumaraditya303/cpython/commit/e4a2fff)
- commit date: 2026-04-03T19:51:07+05:30
- commit merge base: [3908593039bde9d4b591ab09919003ee57418d64](https://github.com/python/cpython/commit/3908593039bde9d4b591ab09919003ee57418d64)
- ref: jit_inline_funcptr

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/23949828264)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260403-vultr-x86_64-kumaraditya303-jit_inline_funcptr-3.15.0a7%2B-e4a2fff.json)

### vs. 3.12.6

- Geometric mean: 1.159x faster (HPT: reliability of 100.00%, 1.08x faster at 99th %ile)
- Memory usage: 1.21x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260403-vultr-x86_64-kumaraditya303-jit_inline_funcptr-3.15.0a7%2B-e4a2fff-vs-3.12.6.md)
- [📈time plot](bm-20260403-vultr-x86_64-kumaraditya303-jit_inline_funcptr-3.15.0a7%2B-e4a2fff-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.120x faster (HPT: reliability of 100.00%, 1.05x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260403-vultr-x86_64-kumaraditya303-jit_inline_funcptr-3.15.0a7%2B-e4a2fff-vs-3.13.0rc2.md)
- [📈time plot](bm-20260403-vultr-x86_64-kumaraditya303-jit_inline_funcptr-3.15.0a7%2B-e4a2fff-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.004x slower (HPT: reliability of 98.47%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20260403-vultr-x86_64-kumaraditya303-jit_inline_funcptr-3.15.0a7%2B-e4a2fff-vs-base-mem.svg)
- [📄table](bm-20260403-vultr-x86_64-kumaraditya303-jit_inline_funcptr-3.15.0a7%2B-e4a2fff-vs-base.md)
- [📈time plot](bm-20260403-vultr-x86_64-kumaraditya303-jit_inline_funcptr-3.15.0a7%2B-e4a2fff-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/23949828264)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260403-macm4pro-arm64-kumaraditya303-jit_inline_funcptr-3.15.0a7%2B-e4a2fff.json)

### vs. 3.12.6

- Geometric mean: 1.282x faster (HPT: reliability of 100.00%, 1.15x faster at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260403-macm4pro-arm64-kumaraditya303-jit_inline_funcptr-3.15.0a7%2B-e4a2fff-vs-3.12.6.md)
- [📈time plot](bm-20260403-macm4pro-arm64-kumaraditya303-jit_inline_funcptr-3.15.0a7%2B-e4a2fff-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.189x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.22x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20260403-macm4pro-arm64-kumaraditya303-jit_inline_funcptr-3.15.0a7%2B-e4a2fff-vs-3.13.0rc2.md)
- [📈time plot](bm-20260403-macm4pro-arm64-kumaraditya303-jit_inline_funcptr-3.15.0a7%2B-e4a2fff-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.005x faster (HPT: reliability of 100.00%, 1.00x faster at 99th %ile)
- Memory usage: 0.99x
- [🧠memory plot](bm-20260403-macm4pro-arm64-kumaraditya303-jit_inline_funcptr-3.15.0a7%2B-e4a2fff-vs-base-mem.svg)
- [📄table](bm-20260403-macm4pro-arm64-kumaraditya303-jit_inline_funcptr-3.15.0a7%2B-e4a2fff-vs-base.md)
- [📈time plot](bm-20260403-macm4pro-arm64-kumaraditya303-jit_inline_funcptr-3.15.0a7%2B-e4a2fff-vs-base.svg)

