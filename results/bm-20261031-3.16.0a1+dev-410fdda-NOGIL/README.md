# Results

- fork: python/410fdda081ba1ca95be0
- version: 3.16.0a1+dev
- config: NOGIL
- commit hash: [410fdda](https://github.com/python/cpython/commit/410fdda)
- commit date: 2026-10-31T17:18:16-07:00
- commit merge base: [47c249adf3bc2ae3264a7373f7f1f5e7c4d84955](https://github.com/python/cpython/commit/47c249adf3bc2ae3264a7373f7f1f5e7c4d84955)
- ref: 410fdda081ba1ca95be0

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/41257083931)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1%2Bdev-410fdda.json)

### vs. 3.12.6

- Geometric mean: 1.090x faster (HPT: reliability of 99.10%, 1.00x faster at 99th %ile)
- Memory usage: 1.27x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1%2Bdev-410fdda-vs-3.12.6.md)
- [📈time plot](bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1%2Bdev-410fdda-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.010x faster (HPT: reliability of 73.08%, 1.00x slower at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1%2Bdev-410fdda-vs-3.13.0rc2.md)
- [📈time plot](bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1%2Bdev-410fdda-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.001x faster (HPT: reliability of 96.24%, 1.00x faster at 99th %ile)
- Memory usage: 1.00x
- missing benchmarks: 🔴 asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list
- [🧠memory plot](bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1%2Bdev-410fdda-vs-base-mem.svg)
- [📄table](bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1%2Bdev-410fdda-vs-base.md)
- [📈time plot](bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1%2Bdev-410fdda-vs-base.svg)

### vs. default_base_vs_NOGIL

- Geometric mean: 1.100x slower (HPT: reliability of 100.00%, 1.10x slower at 99th %ile)
- Memory usage: 1.12x
- missing benchmarks: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list
- new benchmarks: coverage
- [📄table](bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1%2Bdev-410fdda-vs-default_base_vs_NOGIL.md)
- [📈time plot](bm-20261031-macm4pro-arm64-python-410fdda081ba1ca95be0-3.16.0a1%2Bdev-410fdda-vs-default_base_vs_NOGIL.svg)

