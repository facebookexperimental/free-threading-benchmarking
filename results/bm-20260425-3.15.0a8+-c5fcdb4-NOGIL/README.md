# Results

- fork: python/c5fcdb4a9bd04b88f363
- version: 3.15.0a8+
- config: NOGIL
- commit hash: [c5fcdb4](https://github.com/python/cpython/commit/c5fcdb4)
- commit date: 2026-04-25T16:02:51-07:00
- commit merge base: [b2f126c4a0bad66d4b51028e8754a18e59ad84bb](https://github.com/python/cpython/commit/b2f126c4a0bad66d4b51028e8754a18e59ad84bb)
- ref: c5fcdb4a9bd04b88f363

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/24944241491)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8%2B-c5fcdb4.json)

### vs. 3.12.6

- Geometric mean: 1.013x slower (HPT: reliability of 64.41%, 1.00x slower at 99th %ile)
- Memory usage: 1.44x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8%2B-c5fcdb4-vs-3.12.6.md)
- [📈time plot](bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8%2B-c5fcdb4-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.046x slower (HPT: reliability of 85.76%, 1.00x slower at 99th %ile)
- Memory usage: 1.43x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8%2B-c5fcdb4-vs-3.13.0rc2.md)
- [📈time plot](bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8%2B-c5fcdb4-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.096x slower (HPT: reliability of 100.00%, 1.09x slower at 99th %ile)
- Memory usage: 1.21x
- [🧠memory plot](bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8%2B-c5fcdb4-vs-base-mem.svg)
- [📄table](bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8%2B-c5fcdb4-vs-base.md)
- [📈time plot](bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8%2B-c5fcdb4-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/24944241491)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8%2B-c5fcdb4.json)

### vs. 3.12.6

- Geometric mean: 1.103x faster (HPT: reliability of 99.67%, 1.01x faster at 99th %ile)
- Memory usage: 1.39x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8%2B-c5fcdb4-vs-3.12.6.md)
- [📈time plot](bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8%2B-c5fcdb4-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.023x faster (HPT: reliability of 60.82%, 1.00x faster at 99th %ile)
- Memory usage: 1.33x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8%2B-c5fcdb4-vs-3.13.0rc2.md)
- [📈time plot](bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8%2B-c5fcdb4-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.054x slower (HPT: reliability of 100.00%, 1.05x slower at 99th %ile)
- Memory usage: 1.12x
- [🧠memory plot](bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8%2B-c5fcdb4-vs-base-mem.svg)
- [📄table](bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8%2B-c5fcdb4-vs-base.md)
- [📈time plot](bm-20260425-macm4pro-arm64-python-c5fcdb4a9bd04b88f363-3.15.0a8%2B-c5fcdb4-vs-base.svg)

