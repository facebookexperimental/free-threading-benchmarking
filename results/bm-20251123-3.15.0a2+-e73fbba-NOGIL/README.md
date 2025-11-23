# Results

- fork: python/e73fbbacbba0dc65f852
- version: 3.15.0a2+
- config: NOGIL
- commit hash: [e73fbba](https://github.com/python/cpython/commit/e73fbba)
- commit date: 2025-11-23T00:26:50Z
- commit merge base: [227b9d326ec7eba35942a4eb451c7db244a33a6c](https://github.com/python/cpython/commit/227b9d326ec7eba35942a4eb451c7db244a33a6c)
- ref: e73fbbacbba0dc65f852

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/19603381702)
- cpu model: missing
- platform: macOS-26.0.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2%2B-e73fbba.json)

### vs. 3.12.6

- Geometric mean: 1.112x faster (HPT: reliability of 99.96%, 1.02x faster at 99th %ile)
- Memory usage: 1.37x
- missing benchmarks: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2%2B-e73fbba-vs-3.12.6.md)
- [📈time plot](bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2%2B-e73fbba-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.026x faster (HPT: reliability of 58.93%, 1.00x faster at 99th %ile)
- Memory usage: 1.32x
- missing benchmarks: chameleon, connected_components, djangocms, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2%2B-e73fbba-vs-3.13.0rc2.md)
- [📈time plot](bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2%2B-e73fbba-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.003x faster (HPT: reliability of 58.54%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: 🔴 asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list
- [🧠memory plot](bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2%2B-e73fbba-vs-base-mem.svg)
- [📄table](bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2%2B-e73fbba-vs-base.md)
- [📈time plot](bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2%2B-e73fbba-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.025x slower (HPT: reliability of 99.83%, 1.00x slower at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2%2B-e73fbba-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20251123-macm4pro-arm64-python-e73fbbacbba0dc65f852-3.15.0a2%2B-e73fbba-vs-default_base_vs_NOGIL.svg)

