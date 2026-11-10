# Results

- fork: nascheme/ft_ra_memory_order
- version: 3.16.0a1+dev
- config: CLANG,NOGIL
- commit hash: [f14d6e1](https://github.com/nascheme/cpython/commit/f14d6e1)
- commit date: 2026-11-09T17:27:51-07:00
- commit merge base: [e891a9117985888df3e5d48145cf07ddda098335](https://github.com/python/cpython/commit/e891a9117985888df3e5d48145cf07ddda098335)
- ref: ft_ra_memory_order

## darwin arm64 (macm4pro)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/42729379128)
- cpu model: missing
- platform: macOS-26.6.1-arm64-arm-64bit-Mach-O
- [raw results](bm-20261109-macm4pro-arm64-nascheme-ft_ra_memory_order-3.16.0a1%2Bdev-f14d6e1.json)

### vs. 3.12.6

- Geometric mean: 1.130x faster (HPT: reliability of 99.99%, 1.03x faster at 99th %ile)
- Memory usage: 1.23x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261109-macm4pro-arm64-nascheme-ft_ra_memory_order-3.16.0a1%2Bdev-f14d6e1-vs-3.12.6.md)
- [📈time plot](bm-20261109-macm4pro-arm64-nascheme-ft_ra_memory_order-3.16.0a1%2Bdev-f14d6e1-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: 1.047x faster (HPT: reliability of 73.08%, 1.00x faster at 99th %ile)
- Memory usage: 1.20x
- missing benchmarks: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
- new benchmarks: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile
- [📄table](bm-20261109-macm4pro-arm64-nascheme-ft_ra_memory_order-3.16.0a1%2Bdev-f14d6e1-vs-3.13.0rc2.md)
- [📈time plot](bm-20261109-macm4pro-arm64-nascheme-ft_ra_memory_order-3.16.0a1%2Bdev-f14d6e1-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: 1.004x slower (HPT: reliability of 100.00%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20261109-macm4pro-arm64-nascheme-ft_ra_memory_order-3.16.0a1%2Bdev-f14d6e1-vs-base-mem.svg)
- [📄table](bm-20261109-macm4pro-arm64-nascheme-ft_ra_memory_order-3.16.0a1%2Bdev-f14d6e1-vs-base.md)
- [📈time plot](bm-20261109-macm4pro-arm64-nascheme-ft_ra_memory_order-3.16.0a1%2Bdev-f14d6e1-vs-base.svg)

