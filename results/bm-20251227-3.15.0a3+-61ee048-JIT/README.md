# Results

- fork: python/61ee04834b096be00678
- version: 3.15.0a3+
- config: JIT
- commit hash: [61ee048](https://github.com/python/cpython/commit/61ee048)
- commit date: 2025-12-27T14:57:13Z
- commit merge base: [84fcdbd86ecd81f7cc793e22268a029ac6cf29c2](https://github.com/python/cpython/commit/84fcdbd86ecd81f7cc793e22268a029ac6cf29c2)
- commit date: 2025-12-27T14:57:13+00:00
- ref: 61ee04834b096be00678

## linux x86_64 (vultr)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20546241821)
- cpu model: Intel(R) Xeon(R) E-2286G CPU @ 4.00GHz
- platform: Linux-6.8.0-87-generic-x86_64-with-glibc2.39
- [raw results](bm-20251227-vultr-x86_64-python-61ee04834b096be00678-3.15.0a3%2B-61ee048.json)

### vs. 3.12.6

- Geometric mean: 1.120x faster (HPT: reliability of 100.00%, 1.06x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251227-vultr-x86_64-python-61ee04834b096be00678-3.15.0a3%2B-61ee048-vs-3.12.6.md)
- [📈time plot](bm-20251227-vultr-x86_64-python-61ee04834b096be00678-3.15.0a3%2B-61ee048-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.082x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.18x
- missing benchmarks: aiohttp, chameleon, dask, flaskblogging, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers
- [📄table](bm-20251227-vultr-x86_64-python-61ee04834b096be00678-3.15.0a3%2B-61ee048-vs-3.13.0rc2.md)
- [📈time plot](bm-20251227-vultr-x86_64-python-61ee04834b096be00678-3.15.0a3%2B-61ee048-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.035x faster (HPT: reliability of 93.76%, 1.00x faster at 99th %ile)
- Memory usage: 1.03x
- [🧠memory plot](bm-20251227-vultr-x86_64-python-61ee04834b096be00678-3.15.0a3%2B-61ee048-vs-base-mem.svg)
- [📄table](bm-20251227-vultr-x86_64-python-61ee04834b096be00678-3.15.0a3%2B-61ee048-vs-base.md)
- [📈time plot](bm-20251227-vultr-x86_64-python-61ee04834b096be00678-3.15.0a3%2B-61ee048-vs-base.svg)

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/20546241821)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251227-macm4pro-arm64-python-61ee04834b096be00678-3.15.0a3%2B-61ee048.json)

### vs. 3.12.6

- Geometric mean: 1.262x faster (HPT: reliability of 100.00%, 1.14x faster at 99th %ile)
- Memory usage: 1.24x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20251227-macm4pro-arm64-python-61ee04834b096be00678-3.15.0a3%2B-61ee048-vs-3.12.6.md)
- [📈time plot](bm-20251227-macm4pro-arm64-python-61ee04834b096be00678-3.15.0a3%2B-61ee048-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.171x faster (HPT: reliability of 100.00%, 1.07x faster at 99th %ile)
- Memory usage: 1.19x
- missing benchmarks: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20251227-macm4pro-arm64-python-61ee04834b096be00678-3.15.0a3%2B-61ee048-vs-3.13.0rc2.md)
- [📈time plot](bm-20251227-macm4pro-arm64-python-61ee04834b096be00678-3.15.0a3%2B-61ee048-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.065x faster (HPT: reliability of 100.00%, 1.02x faster at 99th %ile)
- Memory usage: 1.02x
- new benchmarks: dask, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list
- [🧠memory plot](bm-20251227-macm4pro-arm64-python-61ee04834b096be00678-3.15.0a3%2B-61ee048-vs-base-mem.svg)
- [📄table](bm-20251227-macm4pro-arm64-python-61ee04834b096be00678-3.15.0a3%2B-61ee048-vs-base.md)
- [📈time plot](bm-20251227-macm4pro-arm64-python-61ee04834b096be00678-3.15.0a3%2B-61ee048-vs-base.svg)

