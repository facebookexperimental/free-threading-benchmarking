# Results

- fork: python/85bc489b649fe261f962
- version: 3.14.0a6+
- config: CLANG
- commit hash: [85bc489](https://github.com/python/cpython/commit/85bc489)
- commit date: 2025-04-05T15:56:01-07:00
- commit merge base: [ad6a032cebf59d1668caa7e726aa5da72e1cbb5c](https://github.com/python/cpython/commit/ad6a032cebf59d1668caa7e726aa5da72e1cbb5c)
- ref: 85bc489b649fe261f962

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/14287076184)
- cpu model: missing
- platform: macOS-15.4-arm64-arm-64bit-Mach-O
- [raw results](bm-20250405-macm4pro-arm64-python-85bc489b649fe261f962-3.14.0a6%2B-85bc489.json)

### vs. 3.12.6

- Geometric mean: 1.168x faster (HPT: reliability of 100.00%, 1.09x faster at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250405-macm4pro-arm64-python-85bc489b649fe261f962-3.14.0a6%2B-85bc489-vs-3.12.6.md)
- [📈time plot](bm-20250405-macm4pro-arm64-python-85bc489b649fe261f962-3.14.0a6%2B-85bc489-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.083x faster (HPT: reliability of 100.00%, 1.03x faster at 99th %ile)
- Memory usage: 1.08x
- missing benchmarks: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
- new benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list
- [📄table](bm-20250405-macm4pro-arm64-python-85bc489b649fe261f962-3.14.0a6%2B-85bc489-vs-3.13.0rc2.md)
- [📈time plot](bm-20250405-macm4pro-arm64-python-85bc489b649fe261f962-3.14.0a6%2B-85bc489-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.063x faster (HPT: reliability of 100.00%, 1.04x faster at 99th %ile)
- Memory usage: 0.99x
- [🧠memory plot](bm-20250405-macm4pro-arm64-python-85bc489b649fe261f962-3.14.0a6%2B-85bc489-vs-base-mem.svg)
- [📄table](bm-20250405-macm4pro-arm64-python-85bc489b649fe261f962-3.14.0a6%2B-85bc489-vs-base.md)
- [📈time plot](bm-20250405-macm4pro-arm64-python-85bc489b649fe261f962-3.14.0a6%2B-85bc489-vs-base.svg)

